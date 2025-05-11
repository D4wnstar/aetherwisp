---
wiki-publish: true
aliases:
  - diagonalized
  - eigendecomposition
---
A square [[matrix]] is said to be **diagonal** if it only has nonzero entries on the diagonal. For example, the identity matrix is diagonal
$$\mathrm{I}=\begin{pmatrix}
1 & 0 & \ldots & 0 \\
0 & 1 & \ldots &  0 \\
\vdots & \vdots & \ddots  & \vdots \\
0 & 0 & 0 & 1
\end{pmatrix}$$
An $n\times n$ square matrix is said to be **diagonalizable** if it is [[matrix similarity|similar]] to an $n\times n$ diagonal matrix, that is, given a matrix $\mathrm{A}$ and a diagonal matrix $\mathrm{D}$, $\mathrm{A}$ is diagonalizable if there exists some [[invertible matrix]] $\mathrm{S}$ such that
$$\mathrm{D}=\mathrm{S}^{-1}\mathrm{A}\mathrm{S}$$
**Diagonalization** is the process of finding $\mathrm{D}$ and $\mathrm{S}$, or equivalently finding a [[basis]] of [[Vector space|vectors]] in which $\mathrm{A}$ is diagonal. The vectors that make up this basis are the columns of $\mathrm{S}$ and are known as [[Equazione agli autovalori|eigenvectors]] and the entries of the diagonalized $\mathrm{A}$ are known as its [[Equazione agli autovalori|eigenvalues]]. Since eigenvalues are often very meaningful quantities, it is useful to reverse the previous form to express $\mathrm{A}$ in term of its diagonal (i.e. eigenvalue) matrix. In this context, $\mathrm{D}$ is usually written as $\Lambda$ instead and we get
$$\mathrm{A}=\mathrm{S}\Lambda \mathrm{S}^{-1}$$
This is known as the **eigendecomposition** of $\mathrm{A}$.

The value of diagonalization is that many calculation can be solved either trivially or with much greater ease when a matrix is in diagonal form as compared to its general form. One example is the [[determinant]] of a diagonal matrix, which is just the product of its diagonal entries.
### Properties
- If $\mathrm{A}$ is a [[Matrice simmetrica|symmetric matrix]], then $\mathrm{D}$ is [[orthogonal matrix|orthogonal]], $\mathrm{D}^{-1}=\mathrm{D}^{+}$.
- $\det \mathrm{A}=\sum_{i=1}^{n}\mathrm{D}_{ii}$ where $\mathrm{D}_{ii}$ is the $i$-th element on the diagonal of $\mathrm{D}$.