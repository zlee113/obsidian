Date: 2024-09-19
Hub: [[Computer Architecture]]
Tags: #class
URL/Title: Memory Hierarchy Design

##### Caches
- Direct Mapped: Cache block only has one slot, makes very easy to find but not flexible on where to place 
- Fully associative: Opposite of Direct mapped, every tag must be compared but cache blocks can go anywhere
- Set associative: An in-between of the previous two, blocks can hold 2 or 4 cache blocks.

https://csillustrated.berkeley.edu/PDFs/handouts/cache-3-associativity-handout.pdf

##### Cache Miss Terms
- Compulsory Misses: When starting the first time accessing will always miss 
- Capacity Misses: Cache has to eject some lines based on size issues so misses off that
- Conflict Misses: In set associativity checking a set and missing
- Coherence Misses: multiprocessor (details in future lectures)

##### Cache Write Policy
- Write through: Value is written to cache line and lower level memory
	- Writes to cache and a write buffer so the processor doesn't need to wait for the DRAM to confirm
- Write back: Value is only written to cache line, only written to main memory when replaced

##### On Write Miss
- Write allocate
	- Line is allocated followed by write hit
	- write misses first act like read miss
- No write allocate
	- Write misses dont interfere with cache
	- line is modified in lower level memory
	- Used with write through mostly

##### Cache Replacement Policy
- Random: Replace random line
- FIFO: Replace oldest line
- LRU: Replace least recently used line
	- Expensive for speed and hardware
	- O(log N!)
	- Pseudo LRU instead, approximate policy based on binary tree
		- Faster and uses less hardware
		- tree based decision
		- Implemented in cache today
- NRU: Replace one line that wasn't recently used

##### Advanced Optimizations for Caching
- Reduce Miss Rate
	- Code optimization
	- have more locality in the code
- Reduce Hit time
- increase cache bandwidth
- reduce miss penalty
- reduce miss penalty or miss rate via parallelism

##### Direct Mapped bits
- offset is exponent of 2 ^ number of bytes per line or block
- Index is the exponent of 2 ^ number of lines or blocks
- tag is the number of bits in the physical address minus the calculated offset and index