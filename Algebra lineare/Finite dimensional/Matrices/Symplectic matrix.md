---
wiki-publish: true
aliases:
  - standard symplectic matrix
---
A **symplectic matrix** $\mathrm{M}$ is a $2n\times2n$ [[matrix]] which satisfies the following condition:
$$\mathrm{M}\mathrm{E}\mathrm{M}^{T}=\mathrm{E}$$
where $^{T}$ denotes [[transposition]] and $\mathrm{E}$ is some $2n\times 2n$ [[Matrice simmetrica|antisymmetric]] [[Invertible matrix|invertible]] matrix.

Typically, $\mathrm{E}$ is chosen to be the [[block matrix]]
$$\mathrm{E}=\begin{pmatrix}
0 & -\mathrm{I}_{n} \\
\mathrm{I}_{n} & 0
\end{pmatrix}$$
where $\mathrm{I}_{n}$ is the $n$-dimensional [[identity matrix]]. This is known as the ($2n$-dimensional) **standard symplectic matrix**. In the simplest possible form as a $2\times 2$ matrix, it is
$$\mathrm{E}=\begin{pmatrix}
0 & -1 \\
1 & 0
\end{pmatrix}$$
It appears frequently in areas that deal with [[rotation|rotations]] and symplectic geometry. For example, it is the generating matrix of the [[special orthogonal group]] $SO(2)$. It is also ubiquitous in the treatment of the [[Hamilton equations]] of motions.
### Properties
- Symplectic matrices form a [[group]].
- $\mathrm{E}$ has unit [[determinant]]: $\det \mathrm{E}=1$.