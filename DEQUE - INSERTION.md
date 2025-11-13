# Exp.No:39  
## DEQUE - INSERTION

---

### AIM  
To write a Python program to insert elements at REAR END of deque using a collection built-in function.

---

### ALGORITHM  

1. Import the `deque` class from the `collections` module.  
2. Initialize an empty deque.  
3. Start an infinite loop using `while True`.  
4. In each iteration, take input from the user.  
5. If the input is an empty string, break the loop.  
6. If the input is not empty, convert it to an integer and append it to the deque.  
7. After the loop ends, append the values `14` and `15` to the deque.  
8. Print the message `"The deque after appending at right is :"`.  
9. Print the contents of the deque.  

---

### PROGRAM  

```
# Reg.No: 212223060057
# Name: DINESH KUMAR A
# Exp.No: 39 - DEQUE Insertion

from collections import deque

dq = deque()

# Taking input from user
print("Enter integers to insert into deque (press Enter to stop):")
while True:
    val = input()
    if val == "":
        break
    dq.append(int(val))

# Appending additional elements at rear
dq.append(14)
dq.append(15)

# Display the deque
print("The deque after appending at right is :")
print(dq)

```

### OUTPUT
```
Enter integers to insert into deque (press Enter to stop):
1
3
5
7

The deque after appending at right is :
deque([1, 3, 5, 7, 14, 15])

```
### RESULT
Thus, the Python program to insert elements at the REAR END of a deque using built-in functions was successfully executed and verified.
