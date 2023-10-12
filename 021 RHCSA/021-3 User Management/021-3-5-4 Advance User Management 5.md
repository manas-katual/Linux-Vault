Links : [[021 RHCSA Index]]

# Advance User Management 5

**/etc/passwd is actual user database file A user's existence depends on this file /etc/passwd is a file with 7 fields delimited by ':'**

![[021-3-4-6-4 Advance User Management 5 2023-09-23 18.21.45.excalidraw]]

The 7 different fields are :
- login name
- password
- uid
- gid of primary group
- gecos (finger info)
- default directory
- default shell

---

- Login name will contain login name
- password will not contain anything it will redirect to shadow
- uid will contain userid
- gid will be gid of primary group