Links : [[021 RHCSA Index]]

# Process 

- Operating System has 2 parts : **user space and kernel space**
- ![[021-8-2 Process part 3 2023-10-06 16.28.47.excalidraw]]
- When the operating system starts, both it's user space and kernel space are loaded
- **systemd** process loads the entire user space ^803dfd
- **kthreadd** process loads the entire kernel space
- systemd is the first process that runs on System start up and kthreadd is the second
- Hence, PID 1 is always given to systemd and **PID 2** to **kthreadd**
- systemd and kthreadd are started by the kernel itself
- Hence, their **PPID is always 0**