# Exp.No:37  
## PRIORITY QUEUE

---

### AIM  
To write a Python program for simple implementation of Priority Queue using Queue.

---

### ALGORITHM

1. Start the program.  
2. Define a class `PriorityQueue` with an initializer to create an empty list `queue`.  
3. Define the `__str__` method to return queue elements as a string separated by spaces.  
4. Define the `isEmpty()` method to check if the queue is empty.  
5. Define the `insert(data)` method to append the given data to the queue.  
6. Define the `delete()` method to:  
   - Initialize `max_val` as 0.  
   - Loop through the queue and find the index of the maximum value.  
   - Delete and return the element at that index.  
7. In the main code, take integer input `n` for number of elements.  
8. Loop `n` times to take input values and insert them into the priority queue.  
9. Print the contents of the queue.  
10. While the queue is not empty, call `delete()` and print each returned element.  
11. End the program.

---

### PROGRAM

```
# Reg.No: 212223060057
# Name: DINESH KUMAR A
# Exp.No: 37 - Priority Queue

class PriorityQueue:
    def __init__(self):
        self.queue = []

    def __str__(self):
        return ' '.join([str(i) for i in self.queue])

    def isEmpty(self):
        return len(self.queue) == 0

    def insert(self, data):
        self.queue.append(data)

    def delete(self):
        if self.isEmpty():
            return "Queue is empty"
        max_val = max(self.queue)
        self.queue.remove(max_val)
        return max_val

# Main Program
pq = PriorityQueue()
n = int(input("Enter number of elements to insert: "))
for i in range(n):
    val = int(input(f"Enter element {i+1}: "))
    pq.insert(val)

print("\nPriority Queue elements:")
print(pq)

print("\nDeleting elements in priority order:")
while not pq.isEmpty():
    print(pq.delete(), end=' ')

```

### OUTPUT
```
Enter number of elements to insert: 5
Enter element 1: 10
Enter element 2: 30
Enter element 3: 20
Enter element 4: 50
Enter element 5: 40

Priority Queue elements:
10 30 20 50 40

Deleting elements in priority order:
50 40 30 20 10

```

### RESULT
Thus, the Python program for simple implementation of Priority Queue using a list was successfully executed and verified.
