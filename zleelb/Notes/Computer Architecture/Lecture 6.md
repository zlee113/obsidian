Date: 2024-09-12
Hub: [[Computer Architecture]]
Tags: #class
URL/Title: Memory Hierarchy

ISA are streamlined to have limits, but extensions are built and can be built to fit an applications need. 

### Memory Hierarchy
##### Stats from the years
- CPU performance is increasing around 60% a year since 1996. 
- DRAM is much slower at around 9% a year, 2x / 10 years
- This creates an unbalanced systems where the io and memory is slower than the processor
##### Metrics for memory:
- Latency: Time to move through the longest circuit path
- Bandwidth: Number of bits transported at one time
- Capacity: Size of memory
- Energy: Cost of accessing memory, like reading or writing

##### Model for Memory Hierarchy
![[Pasted image 20240912095950.png]]
- Cache: Very quick but usually not as much space
- Main Memory: More space but slower
- Disk: Most space but slowest
![[Pasted image 20240912100353.png]]
Cache focused lecture!!!

##### Principle of Locality
- Two types of locality
	- Temporal Locality: If an address is referenced, it tends to be referenced again like loops with i
	- Spatial Locality: If an address is referenced, the neighboring addresses tend to as well. Like arrays being accessed element by element.
- Hardware relies on locality for speed and is exploited in machine design

##### History of CPU chips
- Started with around at least half the board being cache
- Even within cores their would be additional cache for instructions etc
- As time went on the chips divided into more specific and less room for cache

##### Cache terms
- Hit: Data is in some block
	- Hit rate: Fraction of memory accesses found in the level
	- Hit Time: Time to access the level, RAM access time and time to determine hit or not
- Miss: Data is in a block in a lower level of memory
	- Miss rate: 1 - hit rate
	- Miss Penalty: Time to replace block in upper level
- Hit time << Miss Penalty
- Avg memory access time is: hit time + miss rate /* miss penalty
- Miss Penalty: time to fetch a block from lower level
	- access time: function of latency
	- transfer time: function of bandwidth between levels
- On Die: The CPU package itself
- In the memory hierarchy its layered as the largest the cache the longer it takes to access so its normal to hierarchy several cache storages of increasing sizes as that will still be quicker than going to memory

##### Cache Operations
- Look up address
- return hit data
- return miss data
- update cache content, replacement (temporal locality)

##### Direct Mapping and Cache Lookup
- DM: Memory value can only be placed at corresponding location in cache
- CL: Look up address at corresponding location but need 1 comparison