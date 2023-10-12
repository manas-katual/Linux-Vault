Links : [[021 RHCSA Index]]

# Device drivers

- Linux kernel supports all types of storage devices and assigns them the device drivers
- For **IDE hard drives** (not used anymore), kernel assigns drivers in the series of /dev/hd
		e.g. /dev/hda, /dev/hdb, /dev/hdc, /dev/hdd
- For **SCSI, SAS, SATA, SSD and USB drives**, kernel assigns drivers in the series of /dev/sd
		e.g. /dev/sda, /dev/sdb, /dev/sdc, /dev/sdd, /dev/sde, etc.
- For **nvme devices,** kernel assigns driver in the series of /dev/nmve0
		e.g. /dev/nmve0n1, /dev/nmve0n2, etc..
- For **DVD-ROM**, kernel assigns driver in the series of /dev/sr
		e.g. /dev/sr0, /dev/sr1, etc..
- Incase of hard drives and USB devices, kernel assigns device drivers to the partitions along with the drive
- ![[Device drivers 2023-10-06 15.28.30.excalidraw|800]]
>[!tip] 
>Linux Virtual Machine Drives &rarr; /dev/vd
>e.g. vda, vdb, vdc, vdd
>virtual machines like kvm/Qemu HyperVisor