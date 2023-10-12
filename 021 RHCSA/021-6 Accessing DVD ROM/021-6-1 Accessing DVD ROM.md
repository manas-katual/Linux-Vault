Links : [[021 RHCSA Index]]

# Accessing DVD ROM

**Steps to access a DVD Rom in Linux**

1. Connect DVD to a VM
	![[DVD.png]]
	![[DVD 2.png]]
1. Detect DVD Rom in Linux
	<abbr title="dmesg shows all hardware information">`# dmesg | grep sr0`</abbr>
3. Mount DVD ROM on Mount point
	`# ls /mnt`
	`# mount /dev/sr0 /mnt`
4. Access data via mount point
	`# ls /mnt`
5. Unmount DVD Rom from mount point
	`# unmount /mnt`
	`# ls /mnt`

<hr>

>[!info]
**Device driver for DVD Rom is /dev/sr0
/mnt is by default available in Linux for mounting DVD Rom or USB drive
Installation DVD of RHEL 8 contains setup of 7000+ opensource software**

