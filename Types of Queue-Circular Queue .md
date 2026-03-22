#  Types of Queue-Circular Queue in Python

This project demonstrates the implementation of a **Circular Queue** in Python. The queue accepts 3 user values, performs enqueue and dequeue operations, and displays the removed values.

---

##  Aim

To develop a Python program that implements a Circular Queue:
- Accepts 3 values from the user
- Removes the 3 values from the queue
- Displays the removed values

---

##  Algorithm

1. **Initialize** a circular queue of fixed size (e.g., 5).
2. **Define the following functions**:
   - `enqueue()`: Inserts an element into the queue.
   - `dequeue()`: Removes an element from the queue.
   - `display()`: Shows the queue contents.
3. Accept 3 values from the user using the `enqueue()` method.
4. Remove 3 values using the `dequeue()` method.
5. Print the removed values.

---

##  Program:
```
class MyCircularQueue():
    def __init__(self, k):
        self.k = k
        self.queue = [None] * k
        self.head = -1
        self.tail = -1

    def enqueue(self, data):
        if (self.tail + 1) % self.k == self.head:
            # Queue is full — ignore new element
            return

        if self.head == -1:
            self.head = 0

        self.tail = (self.tail + 1) % self.k
        self.queue[self.tail] = data

    def printCQueue(self):
        if self.head == -1:
            print("Queue is empty")
            return

        i = self.head
        result = []

        while True:
            result.append(self.queue[i])
            if i == self.tail:
                break
            i = (i + 1) % self.k

        print(" ".join(result))


# Main program
obj = MyCircularQueue(5)
n = int(input())

for _ in range(n):
    obj.enqueue(input())

obj.printCQueue()

```

### Output:
<img width="623" height="390" alt="image" src="https://github.com/user-attachments/assets/b6701f4f-7cba-495f-91db-681dba778bf2" />

## Result:
The Program was executed successfully
