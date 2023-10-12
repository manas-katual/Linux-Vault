Links : [[021 RHCSA Index]]

# Linux Access modes

- **GUI** for desktop purpose
- **CLI** for server purpose 
- From RHEL 7 Redhat introduced 1st ever **"Web UI"** mode  to manage Linux servers In-built cockpit service is used to provide web UI access
- `systemctl enable --now cockpit.socket` command is used to enable cockpit
- Client can use `https://<serverip>:9090` url to access WebUI of server
- We can also download cockpit in another Linux distros

# Terminals

- In Linux login screens are called **Terminals**
- There are two types of terminals :
	> &rarr; **GUI**
	 &rarr; **CLI**
- There are total 6 Local Terminals on RHEL (this applies for all other daily driver linux distro)
- If **Graphics** is **ON** &rarr; **1 GUI & 5 CLI**
- If **Graphics** is **OFF** &rarr; **6 CLI**
- "ctrl + alt + <abbr title="here fn means f1-f6">fn key</abbr>" is used to switch between local terminals
- If Graphics is ON &rarr; f1 for GUI and f2.......f6 CLI
- If Graphics is OFF &rarr; f1......f6 CLI
- Multiple CLI terminals for running parallel tasks

