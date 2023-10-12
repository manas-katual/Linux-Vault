Links : [[021 RHCSA Index]]

# Introduction

- When we install a program, it gets stored on hard drive.
- This installed program on hard drives is of no direct use to us.
- In order to use a program, we must run it.
- System runs program on RAM.
- This running instance of a Program is called a process.
- When a process of a program starts, the system creates a special environment for that program.
- This environment contains everything needed for the system to run the program as if no other program were running on the system.
- There are 100's or 1000's of processes are running on a server.
- Every process require some configuration file to run which is located in /etc directory.
- Some process also needs plugins, kernel modules, drivers it depends on what it needs for example, if it's a media player it needs some plugins to run or if it's a editor it needs to load device drivers like keyboard to run
**For better understanding refer below diagram**

![[021-8 Process Management 2023-10-06 16.11.59.excalidraw|800]]