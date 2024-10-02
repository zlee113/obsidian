Date: 2024-10-01
Hub: [[Computer Architecture]]
Tags: #book
URL/Title: Computer Architecture - A Quantitative Approach
Chapter: Appendix B

Which block should be replaced on a cache miss?

Used for anything that isn't direct mapping since we know theres only one spot to be replaced.

Strategies:
- Random: spread allocation uniformly, picks at random what to replace
- Least recently used (LRU): Reduce chances of replacing something used often we can replace the least accessed element. LRU relies on locality
- First in, first out (FIFO): LRU can be complicated to calculate, so replaced oldest block
- Pseudo LRU: creates a tree to pseudo do lru but don't have to take as much time for a similar result