---
wiki-publish: false
aliases:
  - parallelism
---
**Parallel programming** or **parallelism**, in computer science, is the practice of splitting a programming problem into many individual chunks, then solving each chunk simultaneously on separate processors and finally aggregating all results. Parallelism is the standard method in modern computer science and architecture to increase computional power by adding more cores to a machine and splitting the workload among all the cores.

Parallelization of code introduces considerable complexity to regular code (called **serial code**) due to the new need of splitting the problem into suitable pieces and keeping the work synchronized across all processing units (called **workers**). It also introduces the idea of **load balancing**: a parallel algorithm is only as fast as the slowest worker it runs on, so making sure that each worker gets an appropriate amount of work is crucial to getting the most out of the algorithm. In general, when considering the idea of parallelizing code, you should consider these questions:
- How much faster can the problem be solved with $N$ workers instead of one?
- How much more work can be done with $N$ workers instead of one?
- What impact (**overhead**) does synchronization, communication between workers and load balancing have on performance?
- What fraction of the resources is actually being used productively for solving the problem?
- Does parallelization introduce specific issues unique to your problem?

Parallelism isn't the answer to all problems. Besides the added complexity in writing the code, the overhead cost might be high enough to make the end result not worth it. Some problems are also just not prone to splitting into independent parallel chunks (for instance, problems where each step relies on the previous step), load balancing might be arduous or resource allocation requirements might make it difficult to use the given hardware in a productive manner. Finally, some new problems might arise due to the parallelization, such as unexpected [[floating point error|round-off errors]] in [[floating point number|floating point arithmetic]] due to it being non-associative ($a+b\neq b+a$) in computers.