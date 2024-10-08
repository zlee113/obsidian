Date: 2024-10-07
Hub: [[Computer Architecture]]
Tags: #web
URL/Title: https://www.geeksforgeeks.org/cache-memory-in-computer-organization/

Cache memory is small high speed storage in a computer. There are various independent caches in the CPU, and they are faster than RAM.

##### Characteristics
- Extremely fast memory that is a buffer between RAM and the CPU
- Cache holds frequently requested data
- Costlier than maon or disk memory but more economical than CPU registers
- Used to speed up and synchronize CPU

##### Levels of Memory
- Level 1: Register, Type in which data is stored and accepted 
- Level 2: Cache memory, fastest memory 
- Level 3: Main memory, where the computer works currently, small in size and deletes when computer turns off
- Level 4: Secondary memory, external memory thats slower than main but stays permanently

##### Cache performance
If processor needs to read or write it first checks cache
- If it finds the memory location in cache its a [[cache hit]]
- Otherwise its a [[cache miss]], then that memory location is copied from main memory into cache
- [[hit rate]] or ratio is the measured quantity that cache is hit and accessed. 

##### Cache Mapping
- Direct mapping
	- Simplest technique
	- Each block of main memory into only one possible cache line
	- If line is taken it has to be trashed and replaced
	- Address space is split into index tag and offset
- Associative mapping
	- Any block can go in any line of the cache
	- fastest and most flexible form
	- Index bits are always zero
- Set associative mapping
	- Instead of mapping one line to one block it maps to a set which is a grouping of lines
	- Allows each word two or more words in main memory with the same index address
	- Combines the best of direct and associative cache mapping techniques