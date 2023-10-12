Links : [[021 RHCSA Index]]

# Basic Linux Commands

1. whoami &rarr; command is used to check current login name
	```bash
	[root@server1 ~]# whoami
	root
	```
1. hostnamectl &rarr; command is used to check current server name
	```bash
	[root@server1 ~]# hostnamectl
	 Static hostname: server1
       Icon name: computer-vm
         Chassis: vm 🖴
      Machine ID: bb0db4b2137641eea00454bd490cd04a
         Boot ID: ad59e8a420784328a863e37113600487
	  Virtualization: vmware
	Operating System: Red Hat Enterprise Linux 9.2 (Plow)     
     CPE OS Name: cpe:/o:redhat:enterprise_linux:9::baseos
          Kernel: Linux 5.14.0-284.11.1.el9_2.x86_64
    Architecture: x86-64
	 Hardware Vendor: VMware, Inc.
	  Hardware Model: VMware Virtual Platform
	Firmware Version: 6.00
	```
1. hostnamectl set-hostname (name of your choice) &rarr; command is used to change hostname of a server. 
2. date &rarr; command shows current date and time
	```bash
	[root@server2 ~]# date
	Thursday 05 October 2023 04:24:51 PM IST
	```
1. date -s "yyyy-mm-dd hh-mm-ss" &rarr; is used to change date & time
2. cal &rarr; shows current month calender
	```bash
	root@server2 ~]# cal
	    October 2023    
	Su Mo Tu We Th Fr Sa
	 1  2  3  4  5  6  7
	 8  9 10 11 12 13 14
	15 16 17 18 19 20 21
	22 23 24 25 26 27 28
	29 30 31            

	```
1. cal 2023 &rarr; shows whole year calender
	```bash
	[root@server2 ~]# cal 2023
                               2023                               

	       January               February                 March       
	Su Mo Tu We Th Fr Sa   Su Mo Tu We Th Fr Sa   Su Mo Tu We Th Fr Sa
	 1  2  3  4  5  6  7             1  2  3  4             1  2  3  4
	 8  9 10 11 12 13 14    5  6  7  8  9 10 11    5  6  7  8  9 10 11
	15 16 17 18 19 20 21   12 13 14 15 16 17 18   12 13 14 15 16 17 18
	22 23 24 25 26 27 28   19 20 21 22 23 24 25   19 20 21 22 23 24 25
	29 30 31               26 27 28               26 27 28 29 30 31   
                                                                  
	        April                   May                   June        
	Su Mo Tu We Th Fr Sa   Su Mo Tu We Th Fr Sa   Su Mo Tu We Th Fr Sa
                   1       1  2  3  4  5  6                1  2  3
	 2  3  4  5  6  7  8    7  8  9 10 11 12 13    4  5  6  7  8  9 10
	 9 10 11 12 13 14 15   14 15 16 17 18 19 20   11 12 13 14 15 16 17
	16 17 18 19 20 21 22   21 22 23 24 25 26 27   18 19 20 21 22 23 24
	23 24 25 26 27 28 29   28 29 30 31            25 26 27 28 29 30   
	30                                                                
	        July                  August                September     
	Su Mo Tu We Th Fr Sa   Su Mo Tu We Th Fr Sa   Su Mo Tu We Th Fr Sa
	                   1          1  2  3  4  5                   1  2
	 2  3  4  5  6  7  8    6  7  8  9 10 11 12    3  4  5  6  7  8  9
	 9 10 11 12 13 14 15   13 14 15 16 17 18 19   10 11 12 13 14 15 16
	16 17 18 19 20 21 22   20 21 22 23 24 25 26   17 18 19 20 21 22 23
	23 24 25 26 27 28 29   27 28 29 30 31         24 25 26 27 28 29 30
	30 31                                                             
	       October               November               December      
	Su Mo Tu We Th Fr Sa   Su Mo Tu We Th Fr Sa   Su Mo Tu We Th Fr Sa
	 1  2  3  4  5  6  7             1  2  3  4                   1  2
	 8  9 10 11 12 13 14    5  6  7  8  9 10 11    3  4  5  6  7  8  9
	15 16 17 18 19 20 21   12 13 14 15 16 17 18   10 11 12 13 14 15 16
	22 23 24 25 26 27 28   19 20 21 22 23 24 25   17 18 19 20 21 22 23
	29 30 31               26 27 28 29 30         24 25 26 27 28 29 30
	                                              31                  

	```
1. cal 02 2030 &rarr; shows particular month and year
	```bash
	[root@server2 ~]# cal 02 2030
	    February 2030   
	Su Mo Tu We Th Fr Sa
	                1  2
	 3  4  5  6  7  8  9
	10 11 12 13 14 15 16
	17 18 19 20 21 22 23
	24 25 26 27 28      
	```
1. uname &rarr; shows type of kernel
	```bash
	[root@server2 ~]# uname
	Linux
	```
1. uname -r &rarr; shows kernel version
	```bash
	[root@server2 ~]# uname -r
	5.14.0-284.11.1.el9_2.x86_64
	```
1. uname -a &rarr; shows everything about kernel
2. cat /etc/redhat-release &rarr; shows OS version
3. uptime &rarr; command shows server uptime
4. users &rarr; command shows currently logged in username
5. who &rarr; command shows who all are logged in, where and since when
6. w &rarr; command shows who all are logged in, where, since when and what are they doing.
7. watch &rarr; command is used to run a command live of screen. ctrl + c to stop
8. watch w &rarr; means live monitoring of w command.
9. clear &rarr; command clears the screen (ctrl + l)
10. tty &rarr; command shows current terminal number 
11. logout, exit, ctrl + d &rarr; to logout from a terminal
12. poweroff &rarr; command is used to shutdown the server
13. reboot &rarr; command is used to shutdown the server
14. history &rarr; command is used to list history of commands executed by a user
15. history 11  &rarr; command will list last 10 commands
16. history -c &rarr; command is used to clear the history of commands
17. history -r &rarr; command is used to recall the cleared commands again
18. expr &rarr; is used to calculate it is a quick calculator
19. stty -echo &rarr; invisible
20. stty echo &rarr; visible
21. ctrl + r &rarr; reverse-i-search

 for simple calculation
``` bash
 expr 4 + 2
 expr 6 - 3
 expr 9 / 3
 expr 4 \* 5
 expr 2 + 5 \* 7
```
	
	