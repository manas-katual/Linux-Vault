Link : [[021 RHCSA Index]]

# Linux File System

  
1. **/** →
    - It is the root directory of Linux file system. It is the mount point of the system partition. All other files & directories are always **"/"** directory.
    - In Linux everything starts with **"/"** directory and end in **"/"** directory.
2. **/boot** → ^3f0f81
    - It contains all the boot files required to start the OS.
    - When we power on the server OS cannot start automatically.
    - OS cannot start automatically no matter what.
    - First the boot files are loaded and after that the operating system boots.
    - It is advisable not to do anything with **/boot** file or store any private data unless we are given task
3. **/dev** → ^3a09c4
    - It contains all the device driver files needed by hardware devices. The OS cannot use hardware devices. The OS cannot use hardware directly. Device driver is a link between the OS and hardware.
    - Every OS cannot directly talk to the devices like mouse, keyboard, Network, cd-rom, Hard drive it needs device drivers.
    - First OS
4. **/lib** &rarr; ^8accbb
	- It contains all the library files. They are known as kernel modules in Linux. File extension of kernel modules are ".ko" ".so"
	- In every OS there are 2 space kernel space & user space "/lib" is the kernel space and every other directories are user space
	- In Linux we have a dedicated directory for kernel it is called /lib
5. **/usr** &rarr; ^2a7a7d
	- It contains all the commands and some optional config files.
	- Commands in Linux are of 2 types.
	- BIN (binary) - binaries stored in /usr/bin, can be used by all users
	- SBIN (superbinary) - binaries stored in /usr/sbin, can only be used by root
	- /usr doesn't contain files directly it contains sub directories 
	- User will give the command through shell to the user space and then it will search the commands in /usr/bin or /usr/sbin and it will pass the message to kernel space. Execution will happen at the kernel space and it will then show the output/error to the user space
	- ![[File Management  1]]
1. **/var** → ^21fa6c
    - It contains all the logs and messages related to system, hardware and applications.
    - Its structure is like
    - ==Diagram space==
2. **/proc** → ^5df4b4
    - It is a mount point to ram. Information of all the running process is stored in this directory.
    - It is task manager of Linux.
3. **/etc** → ^c3f9f7
    - It contains all the config files of applications and system. Almost all type of administrative task in Linux is done from this directory.
    - Linux Administrators spend most of the time in **/etc**
    - Every directories configuration is stored in **/etc**
    - For e.g. _/boot, /proc, /var etc._
4. **/home** → ^19ef98
    - It contains the home directory of all local users  
        e.g. → /home/ganesh  
        → /home/ramesh
    - /home is like a building and Ganesh & Ramesh have their seperate Room inside home
    - They cannot enter in other rooms
10. **/root** → ^3ad100
    - It is the home directory for root user
    - It doesn't come under /home directory
    - root user can access all users directory (it can enter in any other rooms)
    - root is the king of Linux
11. **/tmp** → ^3be19b
    - It is a public directory where all users can create data.
    - for e.g. ganesh creates a directory in /tmp it will be accessible to Ramesh
    - You can see each others data but you cannot modify it without their permission