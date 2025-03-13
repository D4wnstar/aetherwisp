A **binding** is a constraint put on a [[Physical system|system]] that prevents it from moving in certain locations in space. Applying a binding to a system reduces the number of unknowns of that systems, leading to a simplified description. A bound system can only move in a subset of the space it would have otherwise had access to: this space is called [[configuration space]] and denoted $Q$.

Most mechanical bindings can be described as [[force|forces]] with [[Newton's laws|Newton's second law]]:
$$m\mathbf{a}=\mathbf{F}+\Phi$$
$m$ is [[mass]], $\mathbf{a}$ is acceleration, $\mathbf{F}$ is an **active force**, which is *known*, and $\Phi$ is a **constraint reaction**, which is *not known*.
### Properties
A binding is said to be **ideal** if configuration space is "smooth", that is, if the constraint reaction in any point $P$ is always orthogonal to $Q$. Mathematically, this is like saying that the [[scalar product]] of $\Phi$ and any tangent element $\delta \mathbf{r}$ is always zero:
$$\Phi\cdot \delta\mathbf{r}=0\quad\forall P\in \mathbb{R}^{n}\text{ and }\forall \delta \mathbf{r}\in T_{P}Q\quad\Leftrightarrow\quad \Phi\cdot \frac{ \partial \mathbf{r} }{ \partial q_{i} } \text{ where }i=1\ldots,n$$
where $T_{P}Q$ is the [[tangent space]] of $Q$ in the point $P$.