Link : [[021 RHCSA Index]]

# Storage

- Data is stored physically on hard drives and other storage devices
- We need to access data logically from storage device via operating system 
- Every operating system has a logical access point to access storage devices
- This access points are called mount points
- In windows operating system, mount points are in the form of drive letters

![[Basic Storage Concept]]

- Linux does not support drive letters
- In Linux empty directories can be used as mount points

![[Basic Storage Concept 2]]

- When we install operating system on a hard drive, a default directory structure gets created that contains various system files and can also be used to store user data.
- This default directory structure is called a file system.
- Windows file system start from **C: drive** and contains directories like windows, program files and users
- Since there is no drive letter support in Linux, Linux directory structure starts from a directory called slash directory **"/"** 
- **"/"** is the root directory of Linux file system.
- All other files & directories always fall inside **"/"** directory.
- Various Linux directories that fall directly under **"/"** directory include [[021-2 File Management#^3f0f81|boot]], [[021-2 File Management#^3a09c4|dev]], [[021-2 File Management#^21fa6c|var]], [[021-2 File Management#^2a7a7d|usr]], [[021-2 File Management#^8accbb|lib]], [[021-2 File Management#^c3f9f7|etc]], [[021-2 File Management#^5df4b4|proc]], [[021-2 File Management#^19ef98|home]], [[021-2 File Management#^3ad100|root]], and [[021-2 File Management#^3be19b|tmp]]

==for better understanding see below diagram==

![[Basic Storage Concept 3]]