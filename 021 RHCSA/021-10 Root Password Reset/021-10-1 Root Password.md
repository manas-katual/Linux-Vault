Links : [[021 RHCSA Index]]

# Root Password Reset

## There are 2 methods to reset root password 

1. **Old Linux versions (before rhel 9)** :
	- Reboot the server
	- interrupt the boot menu timer (if doesn't show just press and hold shift key to show the grub menu)
	- select the 1st title
	- press e
	- at the end of the line starting with Linux, add 
	- **rd.break enforcing 0**
	- ctrl + x
```bash
mount -o remount, rw /sysroot

chroot /sysroot

passwd

touch /.autorelabel

exit

exit
```

2. **On rhel 9** :
	- reboot the server
	- interrupt the boot menu timer (if doesn't show just press and hold shift key to show the grub menu)
	- select the 1st title
	- press e
	- at the end of the line starting with linux, add
	- **rw init=/bin/bash**
	- ctrl + x
```bash
passwd 

touch /.autorelabel

/sbin/reboot -f (-f stands for "forcefully")
```