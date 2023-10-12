Links : [[021 RHCSA Index]]

# Storage

- Every server requires storage to store data
- Storage should be high performing and highly scalable
- There are 2 types of storage :
	- **DAS - Direct Attached Storage**  is when a storage device (hard disk, DVD-ROM, USB device) is directly connected to a server. Also, there are DAS systems that can connect directly to a server using SCSI hard drive cable
	- ![[Storage 2023-10-06 12.02.17.excalidraw]]
		- **Advantages** :
			1. Fast access (real HDD performance)
			2. Easy to configure
		- **Disadvantages** :
			1. Not highly scalable
			2. Not shared between servers
			3. Difficult to manage in future
	- **Network storage** - When storage is shared over an IP network
		There are 2 types of network storage :
		- **NAS - Network Attached Storage** is when storage is shared like a folder using applications like file servers (NFS/CIFS), FTP or HTTP
		- ![[Storage 2023-10-06 12.11.18.excalidraw]]
		- **SAN - Storage Area Network** is when storage is shared like a virtual drive using <abbr title="skuzzy">iSCSI</abbr> application
		- ![[Storage 2023-10-06 12.11.18.excalidraw 1]]
			- **Advantages** : 
				1. Shared storage
				2. High scalability
			- **Disadvantages** :
				1. N/W dependencies
				2. Performance issue
