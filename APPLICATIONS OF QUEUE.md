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
# APPLICATIONS OF QUEUE - CPU PROCESS SCHEDULING

def CalculateWaitingTime(at, bt, N):
    wt = [0] * N
    wt[0] = 0
    total_waiting_time = 0

    print("P.No.\tArrival Time\tBurst Time\tWaiting Time")
    print(f"1\t\t{at[0]}\t\t{bt[0]}\t\t{wt[0]}")

    for i in range(1, N):
        wt[i] = (at[i - 1] + bt[i - 1] + wt[i - 1]) - at[i]
        if wt[i] < 0:
            wt[i] = 0
        print(f"{i+1}\t\t{at[i]}\t\t{bt[i]}\t\t{wt[i]}")

    total_waiting_time = sum(wt)
    average = total_waiting_time / N
    print("\nAverage Waiting Time:", round(average, 2))


# Main Program
N = 5
at = [0, 1, 2, 3, 4]
bt = []

print("Enter Burst Times for 5 Processes:")
for i in range(N):
    bt.append(int(input(f"Burst Time for P{i+1}: ")))

CalculateWaitingTime(at, bt, N)

```

### OUTPUT
```
Enter Burst Times for 5 Processes:
Burst Time for P1: 5
Burst Time for P2: 3
Burst Time for P3: 8
Burst Time for P4: 6
Burst Time for P5: 2

P.No.   Arrival Time   Burst Time   Waiting Time
1       0              5            0
2       1              3            4
3       2              8            6
4       3              6            13
5       4              2            16

Average Waiting Time: 7.8

```

### RESULT
Thus, the Python program to implement CPU Process Scheduling using Queue was successfully executed and verified.

