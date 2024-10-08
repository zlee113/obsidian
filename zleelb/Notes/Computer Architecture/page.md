Date: 2024-09-24
Hub: [[Computer Architecture]]
Tags: #book
URL/Title: Computer Architecture - A Quantitative Approach
Chapter: Appendix B

Fixed sized blocks, each page will reside in either main memory or disk.

A palt or page fault occurs when the processor references an item within a page that isn't present in the cache or main memory. This will be handled by software. 

Date: 2024-10-07
Hub: [[Computer Architecture]]
Tags: #web
URL/Title: https://www.geeksforgeeks.org/paging-in-operating-system/

Splits the physical memory into fixed blocks called [[page frames]]. When a process requests memory, the operating system allocates one or more page frames to process and map the process's logical pages into the physical page frames.

The page table maintains this mapping which is used by the memory management unit to translate the logical addresses into physical ones. 

##### Terms
- Logical or Virtual address: Deal generated through the CPU and used by a technique to get the right of entry to reminiscence. 
- Virtual Address space: Set of all addresses generated, normally represented in phrases or bytes and split into pages in a paging scheme
- Physical address: Corresponds to a bodily place in reminiscence
- Physical Address Space: Set of all bodily addresses that correspond to virtual addresses