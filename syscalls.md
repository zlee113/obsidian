Date: 2024-07-17
Hub: [[linux]]
Tags: #book
URL/Title: Learning Modern Linux

INTERACTIVE SYSCALL TABLE URL:
https://filippo.io/linux-syscall-table/

Short for system calls and is to represent the interface the kernel exposes that users use. These are usually called from the [[c]] standard library with wrapper functions. 
Example:
![[Pasted image 20240717142512.png]]
This follows these steps:
1. In a syscall.h header file the kernel uses a syscall table (function pointers in memory)
2. With system_call() function it saves the hardware context and then jumps to the function pointed to by the syscall number index in the syscall table
3. After the sysexit is called the wrapper library restores the hardware context and the program execution resumes

To see a more practical example we can use the [[strace]] command to get some more background:
![[Pasted image 20240717143201.png]]
1. The command is asking strace to capture the syscall that ls uses.
2. The syscall "execve" executes /usr/bin/ls replacing the shell
3. the brk syscall (outdated) allocates memory. [[malloc]] is the preferred way which is not a syscall but will use a syscall
4. Access syscall checks if the process can access the file
5. Openat opens the file /etc/ld.so.cache 
6. Read syscall reads from a file descriptor into a buffer

Some example syscalls and their category:
![[Pasted image 20240717144441.png]]
