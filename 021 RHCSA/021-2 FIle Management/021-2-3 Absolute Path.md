Links : [[021 RHCSA Index]]

# Absolute Path

- Complete path from current location to reach a destination file or directory is called absolute path

![[Absolute Path|500]]

**. dot**  &rarr; it represents current directory
**.. double dot** &rarr; it represents previous directory
**~ tilda** &rarr; it represents user's home directory

- In Linux if we want to change our directory we start from **"/"** 
- for e.g. If we want to go to conf directory the command will be "/etc/httpd/conf" (refer to above diagram)
- If we are in a directory (etc) and we want to go to totally different directory (sbin) then we have to give its absolute path e.g. "cd /usr/local/sbin"
- if we want to go to previous directory (one step back) the command will be "cd .." if we want to go 2 step back then it will be "cd ../.."

---
- root user (home directory) :-
	/root/Desktop
	OR
	/~/Desktop

If we want to go to our home directory we simply press ~(Tilda) symbol in keyboard (This doesn't worked for me)


## Commands

1. ls /usr &rarr; it will show content in /usr
2. ls /usr /home /etc/default &rarr; It will show contents in 3 diffrent paths
3. mkdir /usr/d1 &rarr; It will create directory in /usr
4. mkdir -p /linux/distros/redhat &rarr; It will create a path with directories *'here -p stands for parent directory'*
5. mkdir /linux/distros/{centos,ubuntu,kali,Arch,Gentoo} &rarr; It will create subdirectories inside /linux/distros 
6. cp /usr1.txt /linux/distros/redhat &rarr; it will copy the file 
7. cp -r /usr/d1 /linux/distros/redhat &rarr; it will copy subdirectories and its content
8. mv /usr
9. rm 
10. rm -f
11. rm -rf
