# Exp.No:38  
## Deque - DELETION

---

### AIM  
To write a Python program to delete elements at FRONT END of deque using a collection built-in function.

---

### ALGORITHM  

1. Import the `deque` class from the `collections` module.  
2. Create an empty deque.  
3. Define how many elements to input (e.g., 3 inputs as in the example).  
4. Loop through the range of input size:  
   - Read an integer from the user.  
   - Append the integer to the deque.  
5. Remove the front element of the deque using `popleft()`.  
6. Print the final deque after deletion.  

---

### PROGRAM  

```
# Reg.No: 212223060057
# Name: DINESH KUMAR A
# Exp.No: 38 - DEQUE Deletion

from collections import deque

dq = deque()

# Taking input
n = int(input("Enter number of elements to insert: "))
for i in range(n):
    val = int(input(f"Enter element {i+1}: "))
    dq.append(val)

# Removing front element
dq.popleft()

# Display final deque
print("Deque after deleting the front element:")
print(dq)

```

### OUTPUT
```
Enter number of elements to insert: 4
Enter element 1: 10
Enter element 2: 20
Enter element 3: 30
Enter element 4: 40
Deque after deleting the front element:
deque([20, 30, 40])

```


### RESULT
Thus, the Python program to delete elements at the FRONT END of a deque using built-in functions was successfully executed and verified.
