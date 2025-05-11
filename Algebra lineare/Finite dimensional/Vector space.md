---
wiki-publish: true
aliases:
  - vector
---
A **vector space** $V$ is a [[set]] containing elements called **vectors**, defined over a [[field]] $K$, on which are defined two linear operations:
- given $v_{1}, v_{2}\in V$, there exists a sum $v_{1}+v_{2}\in V$.
- given $v\in V$ and $\alpha \in K$, there exists a scalar multiplication $\alpha v\in V$.

In physics, the field is almost always either $\mathbb{R}$ or $\mathbb{C}$.

> [!question] A note on notation
> There are a lot of ways of representing vectors graphically. Throughout these notes, I've adopted what I think are the most common and also (in my opinion) the most readable notations. For pages on pure mathematics, such as analysis and linear algebra, vectors are typically denoted the same as numbers, like $v$. This is commonplace in math. For pages on physics, vectors are denoted in bold font, like $\mathbf{v}$. Unit vectors are denoted using a hat, such as $\hat{\mathbf{i}}$. Some older pages may also have the equivalent notation $\vec{v}$, although ideally I'll phase those out in favor of $\mathbf{v}$ whenever I get to them since it gets noisy and mixes poorly with other overhead symbols like $\dot{\vec{q}}$ or $\tilde{\vec{v}}$.
> 
>  The components for a vector are typically denoted with a subscript index. For instance, $v_{i}$ is the $i$-th component of the vector $\mathbf{v}$. Since the component is a scalar, it never uses bold font.
> 
> Sometimes bold may be used even in math pages, such as this one, for any number of reasons, but it is usually either out of habit, because it makes exposition clearer or because the course it took the notes in used that notation.
> 
> The reason for using different notations is to be consistent with common sources in literature.
