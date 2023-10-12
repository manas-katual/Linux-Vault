Links : [[021 RHCSA Index]]

# Symlinks | Symbolic links | Soft links : 

- Alternate path of an existing path
- ![[021-11-2 Symlinks and HardLinks 2023-10-08 13.22.35.excalidraw]]
- Symlink uses unique inode to reach parent path
- There can be multiple symlinks of a file
- They can be created across (can be created on different partitions) the partitions
- Data is lost if parent is deleted, move or rename
- Symlink with parent path missing is called orphaned link

# Hardlinks :

- Alternate path to an existing file
- Link to the physical object
- Every hard link works like the parent file
- All hardlinks of a file share same inode
- Data is safe till all hardlinks are deleted
- ![[021-11-2 Symlinks and HardLinks 2023-10-08 13.30.54.excalidraw]]
- They cannot be created across (cannot be created on different partitions)

