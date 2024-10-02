Date: 2024-10-02
Hub: [[Computer Architecture]]
Tags: #book
URL/Title: Computer Architecture - A Quantitative Approach
Chapter: Appendix B

What happens on a write?

Two policies when distinguishing cache design:
- Write through: Info is written to both block in cache and block in lower memory
	- Easier to implement
- Write back: Info is written only to block in cache, and written to main memory when replaced

Dirty bit: status bit shows if bit is dirty or clean with dirty being modified while in the cache, if its clean then write backs don't need to happen since identical info is found on the lower levels

Write buffer: Allows stalls to not be a factor by placing in buffer first to be handled as soon as written

Two options for write miss:
- Write allocate: Block allocated on write miss, acts like read misses
- No-write allocate: write miss do not affect cache and the block is modified only in lower level memory

