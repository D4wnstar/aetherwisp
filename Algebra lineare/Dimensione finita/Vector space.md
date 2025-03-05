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

> [!question] A note on notation
> There are a lot of ways of representing vectors graphically. Throughout these notes, I've adopted what I think are the most common and also (in my opinion) the most readable notations. For pages on pure mathematics, such as analysis and linear algebra, vectors are typically denoted the same as numbers, like $v$. This is commonplace in math. For pages on physics, vectors are denoted in bold font, like $\mathbf{v}$. Some older pages may also have the equivalent notation $\vec{v}$, although ideally I'll phase those out in favor of $\mathbf{v}$ whenever I get to them since it gets noisy and mixes poorly with other overhead symbols like $\dot{\vec{q}}$ or $\tilde{\vec{v}}$.
> 
> Sometimes I'll use bold even in math pages, such as this one, because I prefer it and sometimes I just forget to have different notation. The split notation is there primarily to keep consistent with common sources.
