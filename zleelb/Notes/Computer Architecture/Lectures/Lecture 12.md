Date: 2024-10-03
Hub: [[Computer Architecture]]
Tags: #class 
URL/Title: Virtual Address

###### Virtually-Indexed Virtually-Tagged (VIVT) Cache issues - Aliasing
- Different VAs map to same PA
	- Happens when data is shared by multiple processes
- Duplicated cache line in VIPT cache and VIVT$ w/ PID
	- data inconsistent from dupes
- Solution:
	- Write through
	- Flush cache on [[context switch]]

##### Physically-Indexed Physically-Tagged (PIPT) Cache:
- slow, more in [[Lecture 11]]

### Virtually-Indexed Physically-Tagged (VIPT)
![[Pasted image 20241003094557.png]]
- Starts with both tag and index being virtual and then tag goes through tlb before comparator to get the physical address
- Synonym in VIPT
	- If indexes of two VPN page offsets are the same