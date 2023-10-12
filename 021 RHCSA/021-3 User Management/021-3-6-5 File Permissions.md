Links : [[021 RHCSA Index]]

# File permissions

- All the concept of permissions that we saw for a directory is same for a file as well
- The only difference is that the maximum permission level for a **directory** is **777** while for a **file** is **666**
- All files except program files are called regular files.
- On a regular file, a user can only perform read and write operation
- Hence, on all regular files combination of only read and write is used for all categories 
	![[021-3-5-5 File Permissions 2023-09-23 21.21.19.excalidraw|800]]
- Formula to calculate default permission is **maximum permission level - umask**
- maximum permission level for file is **666**
- In case of root creating a file :
	==666 - 022 = 644==   rw-r--r--
- In case of local user creating a file :
	==666- 022 =664==   rw-rw-r--