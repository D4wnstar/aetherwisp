---
wiki-publish: true
aliases:
  - scleronomous constraint
  - rheonomous constraint
  - holonomic constraint
---
A **constraint** is a limitation put on a [[Physical system|system]] that prevents it from moving in certain locations in space. Applying a constraint to a system reduces the number of unknowns of that systems, leading to a simplified description of the same phenomenon. A bound system can only move in a subset of the space it would have otherwise had access to. In mathematical terms, each constraint shrinks the [[configuration space]] of the system by reducing the [[degrees of freedom]]: one constraint removes one degree of freedom.

Most mechanical bindings can be described as [[force|forces]] with [[Newton's laws|Newton's second law]]:
$$m\mathbf{a}=\mathbf{F}+\Phi$$
$m$ is [[mass]], $\mathbf{a}$ is acceleration, $\mathbf{F}$ is an **active force**, which is *known*, and $\Phi$ is a **constraint reaction**, which is *not known*.
### Properties
A constraint is said to be **ideal** if the configuration space is "smooth", that is, if the constraint reaction in any [[Generalized coordinates|configuration]] $P$ is always [[Orthogonality|orthogonal]] to $Q$. Mathematically, this is like saying that the [[scalar product]] of $\Phi$ and any tangent element $\delta \mathbf{r}$ is always zero:
$$\Phi\cdot \delta\mathbf{r}=0\quad\forall P\in \mathbb{R}^{n}\text{ and }\forall \delta \mathbf{r}\in T_{P}Q\quad\Leftrightarrow\quad \Phi\cdot \frac{ \partial \mathbf{r} }{ \partial q_{i} } \text{ where }i=1\ldots,n$$
where $T_{P}Q$ is the [[tangent space]] of $Q$ in the point $P$. If the constraint applies to $N$ point masses, only the total reaction needs to be orthogonal:
$$\sum_{i=1}^{N} \Phi\cdot \delta\mathbf{r}_{i}=0\quad \forall \delta \mathbf{r}_{i}\in T_{P}Q$$

A constraint is said to be **scleronomous** (or **mobile**) if it changes in time, otherwise it is **rheonomous** (or **fixed**). In other words, the equation of a scleronomous constraint is explicitly dependent on time, whereas a rheonomous one isn't. An example of scleronomous constraint would be an object attached to an elevator: the object is always constrained in the same way but the elevator (the constraint) moves, pulling the object with it.

A constraint is said to be **holonomic** if it can be expressed as a function of [[generalized coordinates]] and potentially time that is set to zero: $f(q_{1},\ldots,q_{N},t)=0$. Common examples are forcing a particle to move on a [[curve]] or [[surface]], in which case the equation of the curve or surface is the constraint.