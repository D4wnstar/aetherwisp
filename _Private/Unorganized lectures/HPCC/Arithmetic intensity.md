---
wiki-publish: true
---
**Arithmetic intensity** is the ratio between the number of operations performed by a computer $f(n)$ and the amount of data processed by those operations $n$:
$$A_{I}=\frac{f(n)}{n}$$
It is usually measured in FLOPS/byte. It is a useful metric for code optimization. Ideally, arithmetic intensity should be as small as possible without sacrificing correctness (fewest operations per unit data).
## Examples
> [!example] $O(N)/O(N)$
> A typical case of operations and data both increasing linearly are operations on 1-level loops (single loops): [[Scalar product|scalar products]], [[Vector space|vector]] additions, [[sparse matrix]] additions and more.

> [!example] $O(N^{2})/O(N^{2})$
> A typical case of operations and data both increasing quadratically are operations on 2-level loops (double nested loops): [[matrix]]-vector multiplications, matrix additions, and more.

> [!example] $O(N^{3})/O(N^{2})$
> Cases where operations increase cubically but data increases quadratically are extremely compute intensive: the prototypical case is matrix-matrix multiplication, which is at the heart of a huge number of [[algorithm|algorithms]] and also their primary computational limitation.
