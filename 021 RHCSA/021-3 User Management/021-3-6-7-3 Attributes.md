Links : [[021 RHCSA Index]]

# Attributes

- Permissions restrict local users from accessing files and directories 
- root always has full access of files and directories
- In order to restrict root from accessing files and directories, we can configure attributes
- Attributes are meta-data properties that describe a file or directory's behaviour
- There are plenty of attributes for files and directories
- Few commonly used attributes are :
	- **a** - it means a file can only be appended with new data. Existing data cannot be modified or removed
	- **A** - it means modify time of the file or directory will not update
	- **i** - it means a file or a directory is immutable
- `chattr` command is used to set/unset an attribute
- `lsattr` command is used to list current attributes of a file or a directory

==Attributes restrict access for root as well==