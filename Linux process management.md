Date: 2024-07-16
Hub: [[linux]]
Tags: #book
URL/Title: Learning Modern Linux

How does linux do process management:
- Sessions: Contain process groups that represent high-level user-facing unit. Kernel identifies this session with a session id (sid)
- Process groups: Contains as least one process identified with process group id (pgid)
- Processes: An abstraction to group multiple resources which the kernel exposes to the user with /proc/self and identifies with process id (pid)
- Threads: Implemented by the kernel as a process, a thread is a process that shares certain resources and identified with thread ids (tid) and thread group ids (tgid). 
- Tasks: A data structure in the kernel defined in sched.h that forms the basis of implementing processes and threads.
You can see these various groups using the [[ps]] command. 