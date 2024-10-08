Date: 2024-10-07
Hub: [[Computer Architecture]]
Tags: #paper
URL/Title: Limits of instruction-Level Parallelism

## Main Contributions
- Branch predicition in hardware or software is very important to increasing instruction level parallelism
- Jump prediction is important for reducing penalty of indirect jumps, but overall not significant for parallelism of non-penalty cycles
- Register renaming can be useful for parallelism, but can be handled by a compiler
- Models that are using multiple techniques together are still disappointing
## Strengths
- Despite the age the techniques are still commonly used and googling most of them yielded results and how they are used today
- Variety of techniques, the paper truly lists several different methodologies and explains how they affect different aspects that an architect might want to take into account
- The experiments and tests were built off other papers such as the cited 1989 study of Jouppi and Wall or Tjaden and Flynn, furthering those while having a solid baseline
- Had several benchmarks to use for measuring during testing, so lots of things to gauge the experiment results and data. 
## Weaknesses
- Two genres of techniques are given, within blocks or crossing block boundaries, but within blocks is lacking and has less techniques than its counterpart
- Did not explore in the study all the techniques mentioned, notably not finding a good way to model loop unrolling
- The study is forced to make assumptions to simplify and be able to produce results, such as all operations have a latency of one cycle or unlimited resources like a perfect cache. Some of these could change the results to be less significant by as much as as third of the result

#### Intro
- Parallelism for instruction level requires no reliance on each instruction in order to perform, so if one instruction uses r1 the next can't or it will have to be pipelined to be used. 
- [[superscalar]] machine is one that can issue multiple instructions in the same cycle
- [[superpipelined]] machine issues one instruction per cycle but the cycle time is set much shorter
- [[vliw]] machine is similar to superscalar but the instructions must be explicitly packaged by compiler into long instruction words
- Adding superscalar to a machine that has pipelining is only useful if theres more parallelism available than the pipelining uses.

#### Increasing parallelism
- Increasing parallelism within blocks:
	- [[register renaming]]: Hardware solution that dynamically allocates registers to allow better flow so parallelism can occur more, ie not replacing a registers value in the next instruction 
		- This can also increase the branch penalties of the machine. 
	- [[alias analysis]]: helps decide when two memory references are independent, but is imprescise. 

#### Crossing Block Boundaries
- Instructions between branches on average is low, so we need to be able to issue instructions from different basic blocks in parallel
- [[branch prediction]]: common hardware technique that maintains a table to predict when it should branch
	- often used to keep a pipeline full, with fetch and decode happening after a branch
	- 