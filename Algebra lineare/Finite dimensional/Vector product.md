---
wiki-publish: true
aliases:
  - cross product
---
The **vector product**, also called **cross product**, is an operation between two [[Vector space|vectors]] that produces a third vector that is [[Orthogonality|orthogonal]] to both. Given two vectors $\mathbf{a}$ and $\mathbf{b}$, the vector product is defined as
$$\mathbf{a}\times\mathbf{b}\equiv \lVert \mathbf{a} \rVert \ \lVert \mathbf{b} \rVert \sin\theta\ \hat{\mathbf{n}}$$
where $\lVert \cdot \rVert$ denotes the [[norm]] of a vector, $\theta$ is the angle between the vectors and $\hat{\mathbf{n}}$ is the unit vector perpendicular to both $\mathbf{a}$ and $\mathbf{b}$. The direction of $\hat{\mathbf{n}}$ can be inferred using the right-hand rule. For other forms, see below.

The vector product is defined in a satisfactory manner only in three dimensional spaces, typically $\mathbb{R}^{3}$. Although there exist generalizations to $N$-dimensional vector spaces, none of them meet all of the properties below are consequently not used.

> [!question] A note on notation
> The vector product is almost always denoted using the cross symbol $\times$. In some texts, especially older ones, it is denoted as $\mathbf{a}\wedge \mathbf{b}$. This notation is never used throughout these notes.
> 
> Moreover, it can be safely assumed that, unless otherwise stated, all vector products in these notes refer to $\mathbb{R}^{3}$.
### Properties
The vector product has the following properties:
1. It is distributive over sums: $\mathbf{a}\times(\mathbf{b}+\mathbf{c})=\mathbf{a}\times\mathbf{b}+\mathbf{a}\times\mathbf{c}$.
2. It is anticommutative: $\mathbf{a}\times\mathbf{b}=-\mathbf{b}\times\mathbf{a}$.
3. The vector product of a vector with itself is always zero: $\mathbf{a}\times\mathbf{a}=0$.
### Matrix representation
Given two vectors $\mathbf{a}$ and $\mathbf{b}$, the vector product $\mathbf{a}\times\mathbf{b}$ can be represented in matrix form. Firstly, define the [[Matrice simmetrica|antisymmetric matrix]] of $\mathbf{a}$:
$$C(\mathbf{a})\equiv\begin{pmatrix}0 & -a_{3} & a_{2} \\ a_{3} & 0 & -a_{1} \\ -a_{2} & a_{1} & 0\end{pmatrix}$$
Then, the vector product is the matrix multiplication with $\mathbf{b}$:
$$\mathbf{a}\times\mathbf{b}\equiv C(\mathbf{a})\mathbf{b}=\begin{pmatrix}0 & -a_{3} & a_{2} \\ a_{3} & 0 & -a_{1} \\ -a_{2} & a_{1} & 0\end{pmatrix}\begin{pmatrix}b_{1} \\ b_{2} \\ b_{3}\end{pmatrix}=\begin{pmatrix}a_{2}b_{3}-a_{3}b_{2} \\ a_{3}b_{1}-a_{1}b_{3} \\ a_{1}b_{2}-a_{2}b_{1}\end{pmatrix}$$
#### In Cartesian coordinates
In [[Cartesian coordinates|Cartesian coordinates]] in particular, a second matrix representation is possible in the form using a pseudomatrix. Calling $\hat{\mathbf{i}}$, $\hat{\mathbf{j}}$ and $\hat{\mathbf{k}}$ the unit vectors of the Cartesian triad, the vector product can be calculated as the [[determinant]] of the following pseudomatrix:
$$\mathbf{a}\times\mathbf{b}\equiv\begin{vmatrix}\hat{\mathbf{i}} & \hat{\mathbf{j}} & \hat{\mathbf{k}} \\ a_{1} & a_{2} & a_{3} \\ b_{1} & b_{2} & b_{3}\end{vmatrix}$$
It can be solved, for example, with [[Sarrus' rule]]:
$$\mathbf{a}\times\mathbf{b}=(a_{2}b_{3}-a_{3}b_{2})\hat{\mathbf{i}}+(a_{3}b_{1}-a_{1}b_{3})\hat{\mathbf{j}}+(a_{1}b_{2}-a_{2}b_{1})\hat{\mathbf{k}}$$
which gives the same result as above.
### Tensor representation
The vector product can also be represented by the [[Tensore di Levi-Civita|Levi-Civita tensor]] $\epsilon$. The $i$-th component of the vector product is
$$(\mathbf{a}\times \mathbf{b})_{i}=\sum_{i,j=1,2,3} \epsilon_{ijk}a_{i}b_{j} $$
### Interaction with rotations
The vector product is distributive with respect to a [[rotation]] $R$:
$$(R\mathbf{a})\times(R\mathbf{b})=R(\mathbf{a}\times\mathbf{b})$$
