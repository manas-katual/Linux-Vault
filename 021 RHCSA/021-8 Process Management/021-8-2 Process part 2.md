Links : [[021 RHCSA Index]]

# Process 

- When we issue a command, bash finds the program's binary on hard drive and loads it on RAM.
- On RAM, the process of the program starts
- Linux is a multi-user system which means different users can run various programs, each running instance of a program must be identified uniquely by the kernel.
- Hence, system assigns a maximum **5-digit ID** to every process called PID (process ID)
- PIDs can range from **1 to 99999**
- PID of each process on the system is unique and is incremental by 1
- Once all PIDs are used up, system will repeat the PID numbers which are released by previous processes
- At any point of time, no two processes with the same PID exist in the system because it is the PID that Linux uses to track each process
- If 2 users paralleling start vi editor, the name of both processes will be same but their PIDs will be unique
- Processes run in parent child hierarchy
	- **Parent processes** - These are processes that create other processes during run-time
	- **Child processes** - These processes are created by other processes during run-time
- Every process has two ID numbers assigned to it. The process ID (**PID**) and the Parent process ID (**PPID**)
- Most of the commands that you run have the shell (bash) as their parent
- If the parent process is killed then it's child process will also killed
- And if there is only the child process running then it will not kill any parent process (I know these doesn't make any sense)

==If possible will try to provide diagram==