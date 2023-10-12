Links : [[021 RHCSA Index]]

# Tar Backup

- It is always a best practice to take backup of critical system files and user data to avoid a disaster
- In all Linux flavors we have a data archive utility to backup files and folders into a single archive file
- This utility is called tar
- tar is a data archive manager which easily pack multiple files and folders in a single archive 
- The original files and folders remain as it is, and the new archive file gets created. Hence it is called data backup

## Commands

- Create a data backup archive:
	`# tar cf /data.tar /usr/bin`
	==here, /data.tar is new archive file and /usr/bin is the folder whose backup will be done==
- List data in an archive 
	`# tar tvf /data.tar`
- Extract all data from an archive
	`# tar xf /data.tar`
- Extract selected files from an archive
	`# tar xf /data.tar abc.txt xyz.txt`
	==here, abc.txt and xyz.txt are files that are to b extracted from /data.tar archive==