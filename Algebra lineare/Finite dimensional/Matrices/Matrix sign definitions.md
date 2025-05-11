---
wiki-publish: true
aliases:
  - positive definite
  - positive semidefinite
  - negative semdefinite
  - negative definite
---
An $n\times n$ [[matrix]] $\mathrm{A}$ takes on one of the following definitions if, for any [[Vector space|vector]] $\mathbf{v}\in \mathbb{R}^{n}$, the following holds:
- it is **positive definite** if $\mathbf{v}\cdot \mathrm{A}\mathbf{v}=\mathbf{v}^{T}\mathrm{A}\mathbf{v}>0$
- it is **positive semidefinite** if $\mathbf{v}\cdot \mathrm{A}\mathbf{v}=\mathbf{v}^{T}\mathrm{A}\mathbf{v}\geq0$
- it is **negative semidefinite** if $\mathbf{v}\cdot \mathrm{A}\mathbf{v}=\mathbf{v}^{T}\mathrm{A}\mathbf{v}\leq0$
- it is **negative definite** if $\mathbf{v}\cdot \mathrm{A}\mathbf{v}=\mathbf{v}^{T}\mathrm{A}\mathbf{v}<0$
where $^{T}$ denotes [[transposition]]. If the [[Equazione agli autovalori|eigenvalues]] $\lambda_{i}$ of $\mathrm{A}$ are known, equivalent definitions apply:
- it is **positive definite** if $\lambda_{i}>0$
- it is **positive semidefinite** if $\lambda_{i}\geq0$
- it is **negative semidefinite** if $\lambda_{i}\leq0$
- it is **negative definite** if $\lambda_{i}<0$
for all $i=1,\ldots,n$. Another set of equivalent definitions uses the [[determinant]] of the matrix:
- it is **positive definite** if $\det \mathrm{A}>0$
- it is **positive semidefinite** if $\det \mathrm{A}\geq0$
- it is **negative semidefinite** if $\det \mathrm{A}\leq0$
- it is **negative definite** if $\det \mathrm{A}<0$
An important consequence of these determinant-based definitions is that they show that all positive and negative definite matrices are [[invertible matrix|invertible]], since their determinant is never zero.