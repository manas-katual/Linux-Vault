Links : [[021 RHCSA Index]]

# Termination and Sigterms

- The fundamental way of controlling processes in Linux is by sending signals to them
- There are multiple signals that you can send to a process, to view all the signals run command `kill -l`
- And most signals are for internal use by the system, or for programmers when they write code
- The following are signals which are useful to a system user :
	- **HUP (1) :**
		- It stands for "Hangup".
		- It is used to kill a foreground process when it's terminal is closed
		- example; it is the parent process it first kill all the child process and then it kills itself
	- **INT (2) :**
		- It stands for "Interrupt".
		- It is used to kill a process when user does "ctrl + c"
	- **KILL (3) :**
		- It is used to abruptly (forcefully) kill a process
	- **TERM (15) :**
		- It stands for "Terminate".
		- It is used to kill a process gracefully.
		- Example; If we run a application it process also runs after we quit from it then it's process also get's terminated automatically.
	- **CONT (18) :**
		- It stands for "Continue"
		- It is used to resume/start a suspended/stopped process
	- **STOP (19) :**
		- It is used to stop/suspend a process
- `kill` `killall` or `pkill` commands are used to send signals and manage processes
- kill only understand PID of a process whereas killall only understands the process by name
- pkill is mostly used to manage processes of a particular user

>[!tip]
**top** command is used in all Linux flavors to perform live monitoring of running processes
 

