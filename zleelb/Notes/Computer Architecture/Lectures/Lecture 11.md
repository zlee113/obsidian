Date: 2024-10-08
Hub: [[Computer Architecture]]
Tags: #class 
URL/Title: Virtual memory and addressing

##### Page Hierarchy
- Similar to cache hierarchy, multiple access that takes longer as it goes down
- PPN: physical page number

##### Cache
Should cache use virtual or physical address?
- VIVT: Cache completely uses virtual address
	- Processor core uses virtual address, so only on cache miss we have to translate to get physical address for main memory
	- Homonym: Same virtual address maps to different physical address
		- Occurs when there is a [[context switch]]
	- Synonym: Different virtual addresses map to the same physical address, they have a shared page
		- Solution:
			- write through to fix duplicated issue
			- Flush cache when context switching
- PIPT: Cache completely uses physical address
	- Processor uses VA to go to [[tlb]] to get physical address
	- Slower, always translates address before accessing memory
	- simpler for data coherence
- VIPT: Cache used virtual index and physical tag
	- Cache lookup, index is used before tag
	- Do lookup on virtual index and at the same time use tlb to look up the physical address of the tag
- PIVT