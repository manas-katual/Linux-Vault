Links : [[021 RHCSA Index]]

# Run Levels 

- In Linux the current operating state of the OS is known as Run-level
- Run-level defines what all services can run on the system
- Run-levels are known by numbers and there are total **7 Run-levels** :
	- **Run-level 0** &rarr;  ^27b2cc
		- Also known as halt. 
		- It is used to power-off the server
	- **Run-level 1** &rarr;  ^af6df5
		- It is used to rescue a server
		- Fox example; for some reason if the OS is not booting because of any configuration changes in the OS then we have to boot the OS using Run-level 1 so we can have root powers and make changes to the file
	- **Run-level 2** &rarr; ^bd8387
		- It is used to run a Linux server with minimal services (w/o networking) i.e. CLI
	- **Run-level 3** &rarr;
		- It is used to run a full-fledged Linux server but (w/o graphics)
		- Pure CLI no GUI 
		- Mainly used in companies for servers
	- **Run-level 4** &rarr; ^0ae377
		- unused
		- It is kept unused for other companies or individual if they want to create their own OS with Linux Kernel or we can say Linux as a base
	- **Run-level 5** &rarr; ^1f4167
		- It is used to run a Linux server with graphics
	- **Run-level 6** &rarr; ^c1c2ef
		- It is used to reboot a server

<hr>

## Commands

- To know previous and current run-level
	`runlevel`

- To switch to a run-level
	`init 3`

<hr>

>[!Note]
Run -levels are no longer used after Linux version 3, So the commands may not work