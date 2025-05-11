---
wiki-publish: true
---
The **Frenet-Serret equations** are a set of three equations for the derivatives of the [[basis]] vectors of the [[Moving frame]] in three-dimensional [[Cartesian coordinates]]. Given the tangent, normal and binormal unit vectors $\mathbf{T}$, $\mathbf{N}$ and $\mathbf{B}$, we have
$$\frac{d\mathbf{T}}{ds}=\kappa\mathbf{N}, \quad \frac{d\mathbf{N}}{ds}=-\kappa\mathbf{T}+\tau\mathbf{B}, \quad \frac{d\mathbf{B}}{ds}=-\tau\mathbf{N}$$
with $\kappa$ as the [[curvatura|curvature]] and $\tau$ the [[torsion]] of the trajectory [[Curve|curve]]. They can be put into [[Matrice simmetrica|antisymmetric]] matrix form like
$$\begin{pmatrix}\dot{\mathbf{T}} \\ \dot{\mathbf{N}} \\ \dot{\mathbf{B}}\end{pmatrix}=\begin{pmatrix}0 & \kappa & 0 \\ -\kappa & 0 & \tau \\ 0 & -\tau & 0\end{pmatrix}\begin{pmatrix}\mathbf{T} \\ \mathbf{N} \\ \mathbf{B}\end{pmatrix}$$
