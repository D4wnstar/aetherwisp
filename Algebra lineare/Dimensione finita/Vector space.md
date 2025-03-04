---
aliases:
  - vector
  - linearly dependent
  - linearly independent
---
A **vector space** $V$ is a [[set]] containing elements called **vectors**, on which are defined two linear operations:
- given $\mathbf{v}_{1}, \mathbf{v}_{2}\in V$, there exists a sum $\mathbf{v}_{1}+\mathbf{v}_{2}\in V$
- given $\mathbf{v}\in V$ and $\alpha \in \mathbb{R}$, there exists a scalar multiplication $\alpha \mathbf{v}\in V$

A set of vectors $\{ \mathbf{v}_{1},\ldots,\mathbf{v}_{n} \}\in V$ are said to be **linearly dependent** if there exist a set $\{ \alpha_{1},\ldots,\alpha_{n} \}\in \mathbb{R}$ for which their [[linear combination]] is zero:
$$\alpha_{1}\mathbf{v}_{1}+\ldots+\alpha_{n}\mathbf{v}_{n}=\sum_{i=1}^{n} \alpha_{i}\mathbf{v}_{i}=0$$
If such a set does not exist, the vectors are **linearly independent**.