# Exp No: 36  
## Circular Queue 
---

### AIM  
To write a Python program with a function to insert float values into a Circular Queue.

---

### ALGORITHM

1. Start  
2. Check if the Circular Queue is full  
   - If `size == max_size`, print `"Queue is full"` and exit the function  
3. If the queue is not full:  
   - Read the element to be inserted  
   - Convert it to float  
   - Insert the element at the `tail` position  
   - Update tail using: `tail = (tail + 1) % max_size` (circular increment)  
   - Increment `size` by 1  
4. End

---

### PROGRAM

```

# Reg.No: 212223060057
# Name: DINESH KUMAR A
# Exp.No: 36 - Circular Queue Implementation

class CircularQueue:
    def __init__(self, max_size):
        self.max_size = max_size
        self.queue = [0] * max_size
        self.head = 0
        self.tail = 0
        self.size = 0

    def insert(self, value):
        if self.size == self.max_size:
            print("Queue is full")
            return
        self.queue[self.tail] = float(value)
        self.tail = (self.tail + 1) % self.max_size
        self.size += 1
        print(f"Inserted {value} into the queue.")

    def display(self):
        if self.size == 0:
            print("Queue is empty")
            return
        print("Queue elements: ", end="")
        i = self.head
        count = 0
        while count < self.size:
            print(self.queue[i], end=" ")
            i = (i + 1) % self.max_size
            count += 1
        print()

# Main Program
max_size = int(input("Enter the size of the Circular Queue: "))
cq = CircularQueue(max_size)

# Insert elements
n = int(input("Enter number of elements to insert: "))
for _ in range(n):
    val = input("Enter a float value to insert: ")
    cq.insert(val)

# Display the queue
cq.display()


```

### OUTPUT
```
Enter the size of the Circular Queue: 5
Enter number of elements to insert: 4
Enter a float value to insert: 1.2
Inserted 1.2 into the queue.
Enter a float value to insert: 3.4
Inserted 3.4 into the queue.
Enter a float value to insert: 5.6
Inserted 5.6 into the queue.
Enter a float value to insert: 7.8
Inserted 7.8 into the queue.
Queue elements: 1.2 3.4 5.6 7.8

```

### RESULT
Thus, the Python program to insert float values into a Circular Queue was successfully executed and verified.
