Links : [[021 RHCSA Index]]

# Types of Process

- There are fundamentally two types of processes in Linux :
	- **Foreground processes** - By default, every process that you start runs in the foreground. It gets it's input from the keyboard and sends it's output to the screen
	- **Background processes** - These processes are not connected to a terminal; they don't except any user input
- There are various states of a process
	- **Running (R)** - In this state, the process is actively executing task using the CPU cycles
	- **Waiting/Sleep (I/S)** - in this state, a process is sleeping (not using CPU cycles) and waiting for an event to occur so that it can change to running state and perform execution
		**Sleep processes are further divided into 2 types**
		- **Interruptible** - can be interrupted or called by another process
		- **Uninterruptible** - cannot be interrupted from sleep state
	- **Stopped (T)** - In this state, a process is still on RAM but has been stopped or suspended. Such processes cannot run automatically. We need to start or resume them manually
	- **Zombie (D)** - this is a dead or corrupted process