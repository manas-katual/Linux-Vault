Links : [[021 RHCSA Index]]

# Advance user management 2

**Default values that useradd command use while creating a user are stored in 2 files**

<u>/etc/default/useradd</u>
home = /home
shell = /bin/bash
inactive = -1

<u>/etc/login.defs</u>
min uid 1000
max uid 60000


min gid 1000
max gid 60000


min age 0
max age 99999
warn age 7

![[Advance User Management 3|500]]