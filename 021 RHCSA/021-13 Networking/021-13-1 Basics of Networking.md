Links : [[021 RHCSA Index]]

# Network Basics

- A **N**etwork **I**nterface **C**ard is required on every device to get connected on network
- A NIC is also known as **ethernet card**
- There can be multiple ethernet cards on a server
- Since ethernet card is hardware, it will need device driver to function on the OS
- Linux kernel assigns `/dev/eth` series drivers to ethernet cards
	- e.g. `/dev/eth0`, `/dev/eth1`, `/dev/eth2` and so on
- `dmesg | grep eth` is used to know the available ethernet cards
- Both kernel and the BIOS assigns device drivers to ethernet cards
- From kernel version 3.x onwards, the udevd utility renames kernel assigned drivers with BIOS assign drivers
- Sometimes, it is difficult to remember this drivers
- We can stop this renaming of drivers by performing following steps,
```bash
vi /etc/sysconfig/grub # for RHEL 9 the path is '/etc/default/grub'
# add net.ifnames=0 biosdevname=0 at the end of line starting with CMDLINE_LINUX

grub2-mkconfig -o /boot/grub2/grub.cfg

reboot
```
- Every ethernet card has a globally unique 48bit address called **MAC address** (2a:3b:1c:09:34:d8)
- Also, every device needs an **IP address** for communication
- There are 2 families of IP address: **IPv4** and **IPv6**
- **IPv4** is a 32-bit decimal address divided into 4 octets
- IPv4 range : **0.0.0.0 - 255.255.255.255** 
- **IANA** divided IPv4 addresses into multiple Class

| Class | Range     | Prefix | Mask          | IP scope                          |
| ----- | --------- | ------ | ------------- | --------------------------------- |
| A     | 1 - 126   | /8     | 255.0.0.0     | 16,7777,216 addresses per network |
| B     | 128 - 191 | /16    | 255.255.0.0   | 65,536 addresses per network      |
| C     | 192 - 223 | /24    | 255.255.255.0 | 256 addresses per network                                  |

- IANA also divided IPv4 addresses into 2 types : **Private IP** and **Public IP**
- **Private IP** addresses can be used within a **private network**
- Private IP cannot travel on public network like internet
- For communication on **internet**, only **Public IP** must be used
- IPv6 addresses are 128-bit long hexa-decimal address with a default fixed mask of 64 bits
- ![[021-13-1 Basics of Networking 2023-10-08 17.04.19.excalidraw]]
- Devices can communicate directly only if their IP address belong to same network
- For devices that are in different network to communicate with each other, we need a **Router**
- Router can also connect a private network with internet
- Router's IP address is called **default gatewat address** in the OS
- To secure access of a network or resources in a network from hackers and unauthorized access we need to deploy a **Firewall**
- Firewall filters the incoming and outgoing traffic of a network using various factors
	- Manual &rarr; admin assigned
	- auto &rarr; DHCP assignes
- All IP addresses of Class A, B and C are public, but IANA has range of addresses in each class as private
- **Private IP** address ranges are :
	- **10.0.0.0 - 255.255.255**
	- **172.16.0.0 - 172.31.255.255**
	- **192.168.0.0 - 192.168.255.255**
- **127.0.0.0/8** is reserved for loopback purpose
- Every computer has a default logical network called **loopback** interface with IP address <span style="color:tomato">127.0.0.1</span>
