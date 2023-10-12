Links : [[021 RHCSA Index]]

# Boot Process

1. 1st Start Process &rarr; H/W on
2. 2nd Boot Process &rarr; OS on

- BIOS Program (Pre-configured) &rarr; To Load any OS
- BIOS has minimum 32 Hardware Interrupts each interrupt has a purpose
- INT 19H performs "[[021-12-1 Boot Process#^e07acc|POST]]" where it checks the hardware configuration and maintain records in the form of a list known as "HCL"
- INT 13H &rarr; to go to the storage device and fetch the OS
- CMOS &rarr; boot order
	- 1st boot device
	- 2nd boor device
	- 3rd boot device
- ![[Boot Process 2023-09-20 15.51.41.excalidraw|500]]
- In older Hardware's/Computers there were only BIOS, but in newer hardware/computer we have UEFI + BIOS. Now it is termed as **Firmware**
- **POST** is known as "Power On Self Test" ^e07acc
	- First it will go to every socket then it will sense the hardware then it will detect the hardware then it will learn the information and lastly it will make entry in HCL (Hardware compatibility List)

---
## Hard Drive

- Bios needs CHS # to fetch a file
- It does not understand partitions/inodes
- CHS # 001 is known as "MBR" (master boot record)
- Size of MBR = 512 BYTES (1 sector size)
- ![[Boot Process 2023-09-20 16.10.17.excalidraw|500]]
- 
---

## Operating System

- Kernel is like an engine
- Firstly, Kernel is loaded on ram
- Kernel then calls the entire OS on ram
- Bootloader is needed to tun the kernel
- Every OS has a boot loader and a kernel
- They are 2 main boot files
- Boot loader is stored in system partition
- Boot loader starts kernel; kernel starts operating syste
- ![[Boot Process 2023-09-20 16.26.55.excalidraw]]
---

## Flow of Boot Process

- When we press power button on a pc, SMPS sends current to motherboard.
- Motherboard sends current to pin 66 of processor.
- Processor takes input from pin 66 and starts generating logical signals.
- Processor then sends signal to BIOS chip located on south bridge of the motherboard.
- BIOS chip executes bios program within.
- BIOS calls it's interrupt 19h.
- Int 19h performs POST through which it will learn current hardware Configuration.
- BIOS will save this hardware config in the form of HCL (Hardware Compatibility List)
- BIOS will search for bootable devices in HCL.
- Since there can be multiple bootable device on a system, BIOS will need boot sequence of the devices.
- It will call it's neighbor program "CMOS".
- CMOS program will say 1st boot device is hard drive.
- BIOS will send it's interrupt 13h to hard disk to get the operating system.
- BIOS understands hard drive in the form of cylinders, heads and sectors.
- Initially INT 13h will go to the hard drive without reference of any CHS.
- It will enter the first sector (MBR) and bring the first file found on RAM.
- The first file found on MBR is none other the boot loader.
- After coming on RAM, boot loader will execute itself and will give CHS number of its kernel.
- INT 13h will again go to the hard drive, but this time on the given CHS number.
- It will fetch the file and bring it on RAM.
- The file arrived now is none other than the kernel file.
- Kernel will execute itself and will take over the boot process.
- BIOS task is done.
- Kernel will start booting the OS.
- ![[Boot Process 2023-09-20 16.53.51.excalidraw]]

---

## Bootloader Process

&rarr; Boot loader of linux is called grub (older version of linux bootloader was known as lilo and the latest version is known as grub2)
&rarr; Kernel of linux is called vmlinuz
&rarr; Grub is stored in the boot sector of MBR whereas vmlinuz is stored in /boot partition

![[Boot Process 2023-09-21 15.39.44.excalidraw|800]]


---

## Kernel Process

- Kernel performs two task :
	- hardware initialization
	- System initialization 
		- systemd (1) &rarr; user space
		- kthreadd (2) &rarr; kernel space
- Hardware initialization means detecting hardware, assigning suitable drivers and making it ready-to-use
- Kernel performs the hardware initialization and records the entire process in the form of logs 
- All hardware logs are stores in **/var/log/dmesg** file
- Real-time hardware changes are also logged in the same file
- Hardware log file is overwritten on every reboot

---

## Folder structure

![[021-12-1 Boot Process 2023-10-08 13.41.10.excalidraw|800]]

- Every service files & target files are located in `/usr/lib/systemd/system`
- `/etc/systemd/system` contains service files and target files symlinks which are needed like **default.target** which is needed for the default desktop view mode in other words it contains files which have been set
- `/etc/systemd/system/multiuser.target.wants` contains

![[021-12-1 Boot Process 2023-10-08 13.54.00.excalidraw]]