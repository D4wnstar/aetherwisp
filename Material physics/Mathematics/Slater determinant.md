The **Slater determinant** is a method of determining the [[Funzione d'onda|wave function]] of a [[Physical system|system]] of many [[Fermion|fermions]] through the [[determinant]] of a matrix. It is useful because it inherently satisfies the [[Permutation operator|antisymmetry]] under [[particella|particle]] exchange of fermionic states due to the [[Pauli exclusion principle]]. For a system of $N$ fermions it reads
$$\Psi(q_{1},q_{2},\ldots,q_{N})=\frac{1}{\sqrt{ N! }}\begin{vmatrix}
u_{\alpha}(q_{1}) & u_{\beta}(q_{1}) & \ldots & u_{\nu}(q_{1}) \\
u_{\alpha}(q_{2}) & u_{\beta}(q_{2}) & \ldots & u_{\nu}(q_{2}) \\
\vdots \\
u_{\alpha}(q_{N}) & u_{\beta}(q_{N}) & \ldots & u_{\nu}(q_{N})
\end{vmatrix}$$
where $q_{1},\ldots,q_{N}$ are the [[generalized coordinates]] representing both position and [[spin]] and $u(q)$ are the single-particle wave functions for both position and spin. The subscripts $\alpha,\beta, \ldots,\nu$ denote the [[Numero quantico|quantum numbers]] that uniquely determine the simultaneous space and spin state of the fermion.

The usage of a determinant succinctly enforces antisymmetry and the exclusion principle: if any two $u_{i}$ and $u_{j}$ are equal, or if they are exchanged, the set $\{ u_{i} \}$ becomes [[Linear independence|linearly dependent]], the rank of the matrix is no longer maximum and the whole determinant, which is the wave function, becomes zero everywhere.