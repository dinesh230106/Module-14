# Exp.No:40  
## APPLICATIONS OF QUEUE

---

### AIM  
To write a Python program to implement CPU Process Scheduling using a queue.

---

### ALGORITHM  

1. Start the program.  
2. Define the function `CalculateWaitingTime(at, bt, N)`.  
3. Initialize a list `wt` of size `N` with all values set to 0.  
4. Set `wt[0] = 0` for the first process.  
5. Print the table header: "P.No.", "Arrival Time", "Burst Time", "Waiting Time".  
6. Print the values for the first process.  
7. For each process from index `1` to `N-1`:  
   - Calculate `wt[i] = (at[i - 1] + bt[i - 1] + wt[i - 1]) - at[i]`.  
   - Print the process number, arrival time, burst time, and waiting time.  
8. Initialize `total_waiting_time = 0`.  
9. Add up all waiting times.  
10. Calculate average waiting time as `average = total_waiting_time / N`.  
11. Print the average waiting time.  
12. Get burst times as input from the user for 5 processes.  
13. Call `CalculateWaitingTime()` with `at`, `bt`, and `N`.  
14. End the program.

---

### PROGRAM  

```
# Reg.No: 212223060057
# Name: DINESH KUMAR A
# Exp.No: 40
# Function to Calculate waiting time
# and average waiting time
def CalculateWaitingTime(at, bt, N):

	# Declare the array for waiting
	# time
	wt = [0]*N;

	# Waiting time for first process
	# is 0
	wt[0] = 0;

	# Print waiting time process 1
	print("P.No.\tArrival Time\t" , "Burst Time\tWaiting Time");
	print("1" , "\t\t" , at[0] , "\t\t" , bt[0] , "\t\t" , wt[0]);

	# Calculating waiting time for
	# each process from the given
	# formula #code here
	for i in range(1,5):
		wt[i] = (at[i - 1] + bt[i - 1] + wt[i - 1]) - at[i];

		# Print the waiting time for
		# each process
		print(i + 1 , "\t\t" , at[i] , "\t\t" , bt[i] , "\t\t" , wt[i]);
	

	# Declare variable to calculate
	# average
	average = 0.0;
	sum = 0;

	# Loop to calculate sum of all
	
	#code here# waiting time
	for i in range(5):
		sum = sum + wt[i];
	
	# Find average waiting time

	# by dividing it by no. of process
	#code here
	average = sum / 5;

	# Print Average Waiting Time
	print("Average waiting time = " , average);


# Driver code

	# Number of process
N = 5;

	# Array for Arrival time
at = [ 0, 1, 2, 3, 4 ];

	# Array for Burst Time
bt=[]
for i in range(0, 5):
    ele = int(input())
    bt.append(ele)
	

	# Function call to find
	# waiting time
CalculateWaitingTime(at, bt, N);
```

### OUTPUT
<img width="1087" height="481" alt="image" src="https://github.com/user-attachments/assets/42471791-3439-4a33-a4f6-ee71baf49e6e" />


### RESULT
Thus, the Python program to implement CPU Process Scheduling using Queue was successfully executed and verified.

