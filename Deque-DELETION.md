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
import collections
  
n1=input()
n2=input()
n3=input()
# initializing deque
de = collections.deque([n1,n2,n3])



de.popleft()

print ("The deque after deletion is : ")
print (de)
```

### OUTPUT
<img width="1004" height="299" alt="image" src="https://github.com/user-attachments/assets/f10dff16-f9ec-4555-8fad-1139810bce61" />



### RESULT
Thus, the Python program to delete elements at the FRONT END of a deque using built-in functions was successfully executed and verified.
