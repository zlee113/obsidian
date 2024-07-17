Date: 2024-07-17
Hub: [[linux]]
Tags: #book
URL/Title: Learning Modern Linux

A module is a program that you can load into a kernel on demand. Meaning you don't need to recompile or reboot in order to use. 

You can see all the modules in the /lib/modules folder, specifically using the [[find]] command you can see thousands of modules like so:
```
find /lib/modules/$(uname -r) -type f -name '*.ko*'
```
And in order to see the modules the kernel actually loads you can use [[lsmod]] command which will show the module, size, and what uses it like this:
```
Module                  Size  Used by
bnep                   28672  2
nfnetlink_queue        28672  0
nfnetlink_log          24576  0
cfg80211             1097728  0
bluetooth             884736  7 bnep
ecdh_generic           16384  1 bluetooth
ecc                    40960  1 ecdh_generic
```
You can find similar information inside of /proc/modules and you can use [[modprobe]] to manipulate kernel modules.