# # Stack-Stack Reversal Program 

This Python program demonstrates how to reverse the values in a stack using basic stack operations like push and pop.

##  Aim

To write a Python program that reverses the values in a stack using standard stack operations.

##  Algorithm

1. Create an empty stack.
2. Read an integer `n` from the user (number of elements to push).
3. Loop `n` times:
   - Read an integer from the user.
   - Push it onto the stack.
4. Create an empty list called `reverse`.
5. While the stack is not empty:
   - Pop the top element.
   - Append it to `reverse`.
6. Print the reversed list.


### Program:
```
from queue import LifoQueue
stack = LifoQueue(maxsize=5)
n= int(input())
for i in range(n):
    stack.put(input())
print(stack.full())
for i in range(n):
    print(stack.get())
```
## 🧪 Sample Input and Output
<img width="401" height="388" alt="image" src="https://github.com/user-attachments/assets/00950e0b-464a-44f8-9279-e3d7f0edba7e" />

## Result
The Program was executed successfully
