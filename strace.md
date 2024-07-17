Date: 2024-07-17
Hub: [[linux]]
Tags: #book
URL/Title: Learning Modern Linux

Strace runs a specified command to completion and intercepts and records the system calls. Very useful diagnostically and instructionally to debug and see whats happening under the hood for commands. 

Example of a trace with the c flag

strace -c curl -s https://mhausenblas.info > /dev/null 
% time     seconds  usecs/call     calls    errors syscall

 27.97    0.000311           5        52           poll
 11.24    0.000125           1        76        14 openat
 ​￼10.25    0.000114           1       110           rt_sigaction
  5.85    0.000065           0        76           close
  5.85    0.000065           0       154           mmap
  4.41    0.000049           0       160         9 read
  ....................................................................
  0.00    0.000000           0         1           set_tid_address
  0.00    0.000000           0         1           set_robust_list
  0.00    0.000000           0         1           rseq

100.00    0.001112           1       902        34 total

Shows us additional overview stats like time it takes for each syscall.