---
aliases:
  - orthonormal basis
---
Given a [[vector space]] $V$, a **basis** is a [[set]] of [[Vector space|linearly independent]] vectors $\{ \mathbf{e}_{1},\ldots,\mathbf{e}_{n} \}\in V$ such that for each vector $\mathbf{v}$ in $V$, there exist a set $\{ \alpha_{1},\ldots,\alpha_{n} \}\in \mathbb{R}$ for which the [[linear combination]] of basis vectors using these values is exactly $\mathbf{v}$. In symbols:
$$\{ \mathbf{e}_{1},\ldots,\mathbf{e}_{n} \}\in V\text{ such that }\forall \mathbf{v}\in V,\exists!\{ \alpha_{1},\ldots,\alpha_{n} \}\text{ such that }\mathbf{v}=\sum_{i=1}^{n} \alpha_{i}\mathbf{e}_{i}$$
All vectors in $V$ can be expressed as a linear combination of the basis vectors, given a suitable set of values. The scalar product between a vector $\mathbf{v}$ and the $i$-th basis vector $\mathbf{e}_{i}$ gives the $i$-th component of $\mathbf{v}$:
$$\mathbf{v}\cdot \mathbf{e}_{i}=\left( \sum_{j=1}^{n} \alpha_{j}\mathbf{e}_{j} \right)\cdot \mathbf{e}_{i}=\sum_{j=1}^{n} \alpha_{j}(\mathbf{e}_{j}\cdot \mathbf{e}_{i})=\sum_{j=1}^{n} \alpha_{j}\delta_{ij}=\alpha_{i}$$

A basis is said to be **orthonormal** if all the vectors in it are [[Normalizzazione|normalized]] and [[Ortogonalità|orthogonal]] to each other.