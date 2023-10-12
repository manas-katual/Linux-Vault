Links : [[021 RHCSA Index]]

# Directory Permission 4

### Permissions to numbers :

- read &rarr; 4
- write &rarr; 2
- execute &rarr; 1

### Permissions to permission level :

- rwx &rarr; 421 &rarr; 4+2+1 &rarr; 7
- r-x &rarr; 401 &rarr; 4+0+1 &rarr; 5
- --x &rarr; 001 &rarr; 0+0+1 &rarr; 1

**e.g.**

1. rwxrwxrwx &rarr; 421421421 &rarr; 4+2+1 4+2+1 4+2+1 &rarr; 777 &rarr; maximum permission level
2. rwxr-xr-x &rarr; 421401401 &rarr; 4+2+1 4+0+1 4+0+1 &rarr; 755
3. r-x--x--- &rarr; 401001000 &rarr; 4+0+1 1+0+0 0+0+0 &rarr; 510

---

## Umask
- When root creates a directory, the default permission is **rwxr-xr-x (755)**
- When local users create a directory, then default permission is **rwxrwxr-x (755)**
- The default permission is calculated using **umask**
- **umask** is a number used to calculate default permission

![[021-3-5-4 Directory Permission 4 2023-09-23 20.57.58.excalidraw]]

- **Formula** to calculate default permission is **maximum permission level - umask**
- Maximum permission level for directory is **777**
- In case of root creating a directory
	==777 - 022 = 755==
- In case of local user creating a directory 
	==777 - 022 = 775==
- To check current umask of a user :
	`# umask`
- To change umask of a user
	`# umask 027`  (temporary) every user can change its umask

==Umask set using umask command is not persistent. To set umask persistently you have edit .bashrc file==

---

- chmod command is used to change category permissions of a directory
- There are 2 methods of using chmod command
	1. numeric &rarr; permissions are set using permission level
	2. alphabetic &rarr; permissions are set using alphabets
- If we want to apply rwxr-x--x  permission on /data directory using numeric method, then the command would be chmod 751 /data
- If we want to allow write access for others on /data directory using alphabetic method, then the command would be chmod o+w /data ==here o stands for other and w stands for write==
- If we want to allow write access for others and remove access for group on /data directory using alphabetic method, then the command would be chmod o+w,g-r /data **"(+ allow) (- deny)"**
