Link : [[021 RHCSA Index]]

# Partition Layout

There are two types of partition layout

## Single Partition Layout

- Entire Filesystem is created on a single partition.
- Drawback is that if the partition is corrupted, then all system and user data is lost.
- Suitable for R&D servers

## Multiple Partition Layout

- **"/"** becomes the main system partition and while we have etc, usr, lib, proc, root, tmp and dev directories on itself
- boot, home and var can be declared as mount points of separate partitions

![[Basic Partition Layout|800]]

## Swap Partition

- In Linux there is a special partition called swap partition in other words it is virtual memory. It is also known as paging process.
- It provides extra RAM to the system.
- For example if there is 4gb RAM in the system and all the processes are full (RAM is full) then the system (RAM) borrows some space from the storage and it that storage acts as a RAM.
- It is a temporary RAM

![[Basic Partition Layout 2|800]]


