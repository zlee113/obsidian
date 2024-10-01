Date: 2024-09-24
Hub: [[Computer Architecture]]
Tags: #class
URL/Title: Memory Hierarchy

##### Reduce Miss Rate: Code Optimization
- Misses occur if accesses happen from different cache lines
- Relies on programmers or compilers
- Examples:
	- Loop Interchange: In nested loops outer and inner switch
	- Loop blocking: partition large array into smaller blocks, enhances cache reuse
- Classically increase cache size
- if cache is fixed can also increase associativity