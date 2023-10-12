Links : [[000 Home]]

# Quota Management

- A disk quota is a limit that sets the maximum storage space available for each user in a Linux system
- Setting up such a limit prevents users from filling the entire file system in a multi-user environment and disadvantaging other users in the system
- Disk quotas can be configured for individual users as well as user groups
- In addition, quotas can be set not just to control the number of disk blocks consumed but to control the number of inodes
- Because inodes are used to contain file-related information, this allows control over the number of files that can be created
- Quota limits :
	- **Soft limit** : On exceeding this limit, user gets a grace period of 6 days to create more data
	- **Hard limit** : On exceeding this limit, user is immediately denied to create more data