# cisc-121-final-project

# Merge Sort





https://github.com/user-attachments/assets/cff857ac-c1ee-4e6a-ae2a-db4f16d44cd6




I chose to implement merge sort because it is a very efficient sort (O(nlogn)) and is not too complex. It is also complex enough that if one can understand merge sort, they can understand other simple sorts.

The merge sort algorithm, given a list of numbers, performed as follows:

- Divide the list into two halves 
- Recursively repeat this process on each half until each sublist contains only one element
- Merge the smaller sublists back together in sorted order by comparing elements
- During the merge step:
    - Define two pointers, one for each sublist (left and right)
    - Compare the elements at each pointer
    - Place the smaller value into the next position of the merged list
        - If the left value is smaller, move the left pointer forward
        - If the right value is smaller, move the right pointer forward
        - If one sublist is exhausted, append the remaining elements from the other sublist
- Repeat the merging process until all sublists have been combined into one sorted list

## Abstraction
The goal is to create an app designed to help users understand the merge sort algorithm with digestible visuals.

The user inteferface shows a visual for each step as well as an execution log for further understanding. 

## Design
The program is designed to allow the user to generate a random array of minimum length 5 and maximum length 25.

The user can then generate an animation which shows a bar graph with value on the y axis and index on the x axis. 

# Problem Breakdown
We need a random input array of some length with some range of elements. The length will have a maximum of 25 to reduce complexity and ensure reasonable runtime but a minimum length of 5 so the animation still remains useful

We need to return the list sorted from least to greatest. This will be achieved using the merge sort recursive function.

## Testing
- All possible cases were tested (and demonstrated to be handled) to avoid confusion for users:

    - Smallest allowed list length (5 elements)
    <img width="1725" height="540" alt="TestCase1" src="https://github.com/user-attachments/assets/35c73bcb-678c-402f-95d0-34a3a48422e9" />

    - Largest allowed list length (25 elements):

    <img width="1687" height="535" alt="TestCases2" src="https://github.com/user-attachments/assets/1a70076c-4500-420c-8106-924f999bc089" />


    - Example of animation:

    ![merge_sort_animation](https://github.com/user-attachments/assets/206fc3c6-e11f-44a3-bb2e-22a43ecf6dbc)



- Here is an example of an execution log that users find in usage of the app:

<img width="1662" height="448" alt="ExecutionLog" src="https://github.com/user-attachments/assets/764d5d18-a85e-4a22-a711-dd15d016f94a" />

## How to run
### Clone the repository and install gradio using pip with:
```
pip install -r requirements.txt
```
or 
```
python -m pip install -r requirements.txt
```
Then run 
```
python app.py
``` 
in the repository and follow the localhost link provided.

### Alternatively:
Follow the hugging face link to access the app: https://huggingface.co/spaces/wadecodez/CISC121_Proj

## Acknowledgement
The implementation was in part coded by ChatGPT 5 using prompts based on this README.
