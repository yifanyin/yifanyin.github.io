---
title: "OpenMP"
aliases:
- OpenMP
tags:
- 
---

- OpenMP
    - Open multi-processing
    - Industry standard
    - Shared memory parallelization
    - Computing model
        - Thread-based parallelism
        - Explicit parallelism
        - Fork-join model
            - OpenMP uses the fork-join model of parallel execution
                - ![](https://hpc.llnl.gov/sites/default/files/fork_join2.gif)  
            - All OpenMP programs begin as a single process: the master thread. The master thread executes sequentially until the first parallel region construct is encountered.
            - **FORK**: the master thread then creates a team of parallel threads. The statements in the program that are enclosed by the parallel region construct are then executed in parallel among the various team threads.
            - **JOIN**: When the team threads complete the statements in the parallel region construct, they synchronize and terminate, leaving only the master thread.
            - The number of parallel regions and the threads that comprise them are arbitrary.
    - Data scoping
        - Because OpenMP is a shared memory programming model, **most data within a parallel region is shared by default.**
        - All threads in a parallel region can access this shared data simultaneously.
        - OpenMP provides a way for the programmer to explicitly specify how data is "scoped" if the default shared scoping is not desired.
        - This topic is covered in more detail in the Data Scope Attribute Clauses section.