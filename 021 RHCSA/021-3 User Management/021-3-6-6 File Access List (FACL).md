Links : [[021 RHCSA Index]]

# FACL

- chmod command is used to set permissions category-wise
- If we want to assign explicit permissions on a user or a group, we use file access list
- By default, there is no FACL applied on a file or a directory
- setfacl command is used to set ACL permissions for a user or a group on a file or a directory
- getfacl command is used to view current FACL permission
- FACL permissions override category permissions

<hr>

To assign FACL permissions for a group :
`# setfacl -m u:ganesh;rwx /data`  here -m stands for make a policy

To assign FACL permissions for a group :
`# setfacl -m g:sales:rwx /data`

To remove a FACL user rule :
`# setfacl -x u:ganesh /data`

To remove a FACL group rule :
`# setfacl -x g:sales /data`

To remove FACL from a file or directory :
`# setfacl -b /data`

To get info of a FACL from a file or directory :
`# getfacl /data`

![[021-3-5-6 File Access List (FACL) 2023-09-23 21.30.58.excalidraw]]