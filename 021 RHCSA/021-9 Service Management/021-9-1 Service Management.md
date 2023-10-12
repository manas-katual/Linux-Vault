Links : [[021 RHCSA Index]]

# Service Management


- **A service is a script** that is responsible to start, stop or restart process of a program
- All service files are stored in `/usr/lib/systemd/system` directory
	- If your server is running with **[[init]]** program, `service` command is used to manage services
- If your server is running with **[[process continuation 2#^803dfd|systemd]]** program, `systemctl` command is used to manage services
- Services can be started, stopped or restarted in run time
- We can also enable a service to start automatically when server boots

![[021-9 Service Management 2023-10-06 16.34.40.excalidraw]]

<hr>

## Commands

&rarr; To list all active services
`systemctl list-units --type=service`

&rarr; To list installed services 
`systemctl list-units --type=service --all`

&rarr; To check status of a service 
`systemctl status crond`

&rarr; To stop a service
`systemctl stop crond`

&rarr; To start a service
`systemctl start crond`

&rarr; To restart a service
`systemctl restart crond`

&rarr; <abbr title="A masked service cannot be started or enabled">To mask a service</abbr>
`systemctl mask crond`

&rarr; To unmask a service
`systemctl unmask crond`

&rarr; To enable a service at every system boot
`systemctl enable --now crond`

&rarr; To disable a service at every system boot
`systemctl disable --now crond`

<hr>

>[!Note]
You can use these commands with any services you want I have showed example of **crond** service




