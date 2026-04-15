---
aliases:
  - thread
---
A **thread**, in computer science, is an independent instance of code execution within a [[Process (computer science)|process]]. A thread shares the same code, memory address space and resources of its parent process, but it has its own stack, [[instruction pointer]] and [[stack pointer]]. There is a common [[heap (computer science)|heap]] shared by all threads and thus threads operate in shared-memory environment. Threads also have access to the parent's thread stack. They may run on the same processing unit (core) as the parent or in a different unit in the same [[non-uniform memory access|NUMA]] region.

Threads are used for shared-memory [[Parallel programming|parallelism]], similarly to [[multi-process programming]]. The technique is called **multithreading**. Although threads are less independent and less powerful than whole processes, they are also much less expensive to spawn.
## OpenMP
**OpenMP** is a standard API for shared-memory parallelism using [[compiler]] directives. It is most commonly used in C, C++ and Fortran. The benefit of using OpenMP is that it abstracts away the technicalities of the specific hardware implementation of multithreading and of `pthread` (on POSIX platforms). It is therefore a much more approachable solution with a shallower learning curve than programming with `pthread` directly.