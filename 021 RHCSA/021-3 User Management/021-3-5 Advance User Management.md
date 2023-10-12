Links : [[021 RHCSA Index]]

# Advance User Management

![[Advance User Management|300]]

- When a user is created its group also get created and his association will be primary
- And also its UID & GID get created 
- UID stands for User ID
- GID stands for Group ID
- Every users UID is unique & Every Groups GID is unique
- Minimum UID & GID value for local users and group is 100 it is incremental by 1
- UID and GID '0' is always assigned to root and its group
- 1-999 is reserved for system users & groups.
- Default maximum limit for UID and GID is 60000. But it is changeable it can be increased or decreased.
- Every user is given profile files. Profiles are loaded every time when a user will login. Profile files are always hidden and are stored in user's home directory. It is called ".bashrc"


![[Advance User Management 2|800]]