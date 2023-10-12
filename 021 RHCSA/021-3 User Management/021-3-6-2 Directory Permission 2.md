Links : [[021 RHCSA Index]]

# Directory Permission 2

**For all files and directories, all the users on a server are divided into 3 catogeries :**

- user &rarr; owner of the file or directory
- group &rarr; members of co-owner of the file or directory
- others &rarr; Rest users

1. /data owner = ram ; co-owner = hr
2. /data owner = ajay ; co-owner = accounts
3. /data owner = geeta ; co-owner = sales
4. /data owner = shyam ; co-owner = accounts

![[021-3-5-2 Directory Permission 2 2023-09-23 19.53.47.excalidraw]]


| scenario | user  | group        | others              |
| -------- | ----- | ------------ | ------------------- |
| 1        | ram   | seeta, geeta | shyam, ajay, vijay  |
| 2        | ajay  | ram, shyam   | vijay, seeta, geeta |
| 3        | geeta | ajay, vijay  | seeta, ram, shyam   |
| 4        | shyam | ram, shyam   | seeta, geeta, ajay, vijay                     |


==The user that creates a directory becomes the owner and his primary group becomes the co-owner root can change owner and co-owner of a directory using chown and chgrp command==

`# chown ganesh /data`
`# chgrp hr /data`
`# chown ganesh:hr /data`


![[021-3-5-2 Directory Permission 2 2023-09-23 20.04.59.excalidraw|800]]