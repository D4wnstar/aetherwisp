---
wiki-publish: true
aliases:
  - orthonormal
  - Dirac orthonormality
  - Dirac-orthonormal
---
Given a set of functions $\{ f_{n} \}_{n\in \mathbb{N}}$ or [[Vector space|vectors]] $\{ v_{n} \}_{n\in \mathbb{N}}$ from a space equipped with a [[Scalar product]], the set is said to be **orthonormal** if all of the elements are individually [[Normalization|normalized]] and also [[Orthogonality|orthogonal]] to each other. In other words, the scalar product between any two elements $m$ and $n$ must be the [[Kronecker delta]]:
$$(f_{m},f_{n})=\delta_{mn}=\begin{cases}
1&\text{if }m=n \\
0&\text{if }m\neq n
\end{cases}$$
This definition applies to discrete sets, but it can be extended to also provide a similar form of "continuous orthonormality". Given a continuous set $\{ f_{z} \}_{z\in \mathbb{R}}$ of functions or vectors, the scalar product between any two elements $z$ and $w$ must be the [[Delta di Dirac]]:
$$(f_{z},f_{w})=\delta(z-w)=\begin{cases}
\infty&\text{if }z=w \\
0&\text{if }z\neq w
\end{cases}$$
This form of orthonormality is sometimes refereed to with a different name, such as **Dirac orthonormality**[^1], to distinguish it from the discrete case.

[^1]: This name is from Griffiths' *Introduction to Quantum Mechanics, 2nd ed.*.