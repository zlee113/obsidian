Date: 2024-10-01
Hub: [[Computer Architecture]]
Tags: #book
URL/Title: Computer Architecture - A Quantitative Approach
Chapter: Appendix B

How is a block found if it is in the cache?

- tag: address tag on each block frame that gives the block address
	- Checked in parallel to see if it matches the block address from the processor
	- Sometimes include a valid bit to the tag to say whether or not this entry contains a valid address. 
- Block address: Divided into the tag field and the index field
- Block offset: Selects the desired data from the block
	- Should not be used in comparison to select block
	- Checking index is redundant since it was used to select set to be checked
- Index field: Selects the set to get data from
![[Pasted image 20241001162215.png]]