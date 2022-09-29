---
title: "Parallel Computing"
tags:
- computing
- coding
---

# Intro
- The [tutorial](https://hpc.llnl.gov/documentation/tutorials/introduction-parallel-computing-tutorial) from the Lawrence Livermore National Laboratory
- And [the one](https://scicomp.ethz.ch/wiki/Parallel_computing) from ETH

## Parallel computer taxonomy by Flynn
- SISD: Base case of a single instruction stream and single data stream
- SIMD
	- Single instruction: all processing units execute the same instruction at any given clock cycle
	- Multiple data: Each processing unit can operate on a different data element
- MISD: multiband filter, code cracking
- MIMD: every computer now

## Jargons
- A node = a computer in a box
- execution units
- hardware threads

# Speedup and scalability
## Amdahl's law
- Strong scaling
- If a fraction $p$ of your code execution time can be parallelized, then ideally the best speedup from parallelize it is $\frac{1}{1-p}$.
    - So if 50% of the time the code is doing serial work, parallelizing it makes the maximum speedup as 2, or two times faster.
- However this is what you can achieve with $s$-part parallelization if efficiency grows linearly with process number.$$S_\text{latency}=\frac{1}{1-p+\frac{p}{s}}$$
    - Then the above example with 4 cores gives $S_\text{max}$ = 1/(1-0.5+0.5/4)=1.6, or 1.6 time speedup
- And there is the cost of programmer time
- There is overhead in parallel code execution

## Gustavson
- Weak scaling
- Problem size per core stay the same

# Parallel memory architectures
## Shared memory
Describes a computer architecture where all processors have direct access to common physical memory. In a programming sense, it describes a model where parallel tasks all have the same "picture" of memory and can directly address and access the same logical memory locations regardless of where the physical memory actually exists.

### Uniform Memory Access (UMA)
- **Symmetric Multiprocessor (SMP)** machines with Identical processors and equal access and access times to memory
- Cache coherent

### Non-Uniform Memory Access (NUMA)
- Often made by physically linking two or more SMPs
- One SMP can directly access memory of another SMP
- When more SMPs exist, the geometrically increasing linkage becomes harder to manage.

## Distributed memory
- No global address space known to individual processors
- No cache coherency
- When a processor needs access to data in another processor, it is usually the task of the programmer to explicitly define how and when data is communicated. Synchronization between tasks is likewise the programmer's responsibility.

### Advantages
- Memory is scalable with the number of processors. Increase the number of processors and the size of memory increases proportionately.
- Each processor can rapidly access its own memory without interference and without the overhead incurred with trying to maintain global cache coherency.
- Cost effectiveness: can use commodity, off-the-shelf processors and networking.

### Disadvantages
- The programmer is responsible for many of the details associated with data communication between processors.
- It may be difficult to map existing data structures, based on global memory, to this memory organization.
- Non-uniform memory access times: data residing on a remote node takes longer to access than node local data.

Most of the clusters today are combinations of shared-memory machines networked together as a distributed memory system. Very convenient to build but hard to program. 

# Resources
