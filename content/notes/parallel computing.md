---
title: "Parallel Computing"
tags:
- computing
- coding
aliases: Parallel Computing
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
    - Multiple instructions, single data
    - Different processes execute on the same data.
- MIMD: every computer now
    - Where we are now
    - Many MIMD architectures also include SIMD execution sub-components

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
## Gustavson's law
- Weak scaling
- See if the problem size per core stay the same, bigger problem just takes more cores.

## Scaleup
- larger problem with more processors in the same time span.
- The code that consist more fraction that cam be parallelized is more "scalable."
    - Strong scaling: faster calculation with more cores
    - Weak scaling: problem size per core stays the same and solving time remains as more core join.
    - However hardware plays a huge role in the scalability
- And there is the cost of programmer time
- There is overhead in parallel code execution

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

# Parallel Programming Models
- Parallel programming models exist as an abstraction above hardware and memory architectures
- Shared memory model
## Thread model
![](file:///Users/yifan/remnote/remnote-62d766e2363402d17336dfe3/files/WXgx4yUjFCo5JO79hEo5WSGjLjblJehmG6CG28VgfmNpD_6IfCF9ivSIyc1eIlStjlffWB9YAvnwhHZhJ81f_vgRmM8m6I6BNutcxBTAIbzqASonNvenmkK30-cxzwYh.png)
- A thread's work may best be described as a subroutine within the main program.
- In the threads model of parallel programming, a single "heavy weight" process can have multiple "light weight", concurrent execution paths.
- Threads communicate with each other through global memory (updating address locations). This requires synchronization constructs to ensure that more than one thread is not updating the same global address at any time.
- Threads can come and go, but **a.out** remains present to provide the necessary shared resources until the application has completed.
- Threading is good for IO-bound calculation (in python with GIL)
- POSIX Threads
    - Or Pthreads
    - C only
- [[OpenMP]]
- Other threaded implementations 
    - Microsoft threads
    - Java, [[python]] threads
    - CUDA threads for GPUs
## Distributed Memory / Message Passing Model
- A set of tasks that use their own local memory during computation. Multiple tasks can reside on the same physical machine and/or across an arbitrary number of machines.
- Tasks exchange data through communications by sending and receiving messages.
- Data transfer usually requires cooperative operations to be performed by each process. For example, a send operation must have a matching receive operation.
- 
## Data Parallel Model
## Hybrid Model
- MPI between nodes and OpenMP within nodes
- Another similar and increasingly popular example of a hybrid model is using MPI with CPU-GPU (graphics processing unit) programming.
    - MPI tasks run on CPUs using local memory and communicating with each other over a network.
    - Computationally intensive kernels are off-loaded to GPUs on-node.
    - Data exchange between node-local memory and GPUs uses [[CUDA]] (or something equivalent).

# Designing parallel programs
- Automatic parallelization
    - Done by compilers, mostly on loops.
- Manually using compiler directives
- Understand the problem and the program
    - hotspots that require the most calculation
    - bottlenecks that slow down the wall time
        - IO
    - Inhibitors of parallelizing
        - data dependence
        - Investigate other algorithms if possible. This may be the single most important consideration when designing a parallel application.
    - 
## Decomposition
### Domain decomposition
- Cut the mesh
### Functional decomposition
- Distribute the separate tasks
- e.g., climate models are decomposed into atmospheric model, ocean model and hydrology model.

- Communication
- Latency v.s. bandwidth

# Resources
- [[OpenMP|OpenMP]]
- MPI
    - Message passing interface
    - Distributed memory parallelization
    - A [tutorial](https://rchg.github.io/computing-blog/OpenMPI/) from R. Checa-Garcia
    - Initialize and finalize
- See also
    - [[notes/fortran|Fortran]]
    - [[C and C++]]