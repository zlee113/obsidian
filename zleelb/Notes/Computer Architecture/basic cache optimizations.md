Date: 2024-09-23
Hub: [[Computer Architecture]]
Tags: #book
URL/Title: Computer Architecture - A Quantitative Approach
Chapter: 2.1.1

There are six basic ways to improve cache:

1) Larger block size to reduce miss rate: Logically increasing the size of the cache block will make it hit more as we can have more space to hit. This will increase capacity and conflict misses. Block size is complex and has trade offs
2) Bigger caches to reduce miss rate: Bigger cache means less misses, but costs more in time and power. 
3) Higher associativity to reduce miss rate: Costs an increase in hit time and power consumption
4) Multilevel caches to reduce miss penalty: Allows intermediary caches so you don't have to rush towards accessing cache but don't have to directly increase a high speed cache by having secondary ones. 
5) Giving priority to read misses over writes to reduce miss penalty: Read after write hazards can slow things down so priority to reads before writes can reduce that. This has little effect on power consumption.
6) Avoiding address translation during indexing of the cache to reduce hit time: page offset which is identical in both virtual and physical addresses to index cache.