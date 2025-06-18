---
wiki-publish: true
aliases:
  - invertible
  - inverse matrix
---
A square [[matrix]] is said to be **invertible** if there exists another square matrix that, when multiplied with it, yields the [[identity matrix]]. In symbols, $\mathrm{A}$ is invertible $n\times n$ matrix if there exists another $n\times n$ matrix $\mathrm{A}^{-1}$ such that
$$\mathrm{A}\mathrm{A}^{-1}=\mathrm{A}^{-1}\mathrm{A}=\mathrm{I}_{n}$$
$\mathrm{A}^{-1}$ is known as the **inverse** of $\mathrm{A}$.
### Characterization
There are a lot of ways to determine if a matrix is invertible. The following are a few and all equivalent to each other and to the definition above:
- $\mathrm{A}$ has a full [[rank]] $\mathrm{A}$.
- The [[transposition|transpose]] of $\mathrm{A}$, $\mathrm{A}^{T}$, is invertible.
- The [[determinant]] of $\mathrm{A}$ is nonzero, $\det \mathrm{A}\neq0$.
- All of the columns of $\mathrm{A}$ are [[Linear independence|linearly independent]].
- All of the rows of $\mathrm{A}$ are linearly independent.
- The number $0$ is not an [[Equazione agli autovalori|eigenvalue]] of $\mathrm{A}$.
### Properties
- $(\mathrm{A}^{-1})^{-1}=\mathrm{A}$
- $(c\mathrm{A})^{-1}=c^{-1}\mathrm{A}^{-1}$
- $(\mathrm{A}^{T})^{-1}=(\mathrm{A}^{-1})^{T}$
- $\det(\mathrm{A}^{-1})=(\det \mathrm{A})^{-1}$
- If $\mathrm{A}$ and $\mathrm{B}$ are both invertible $n\times n$ matrices, $(\mathrm{A}\mathrm{B})^{-1}=\mathrm{A}^{-1}\mathrm{B}^{-1}$
### Diagonalization
If $\mathrm{A}$ can be [[Diagonalization|eigendecomposed]] into $\mathrm{A}=\mathrm{S}\Lambda \mathrm{S}^{-1}$ then the inverse can be found by inverting the eigenvalue matrix only:
$$\mathrm{A}^{-1}=\mathrm{S}\Lambda^{-1}\mathrm{S}^{-1}$$
