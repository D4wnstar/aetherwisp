---
wiki-publish: true
---
The **Lagrange-Dirichlet theorem** gives a condition to find stable [[Equilibrium point|equilibrium points]] in mechanical systems.

> [!info] Lagrange-Dirichlet theorem
> Let $L(\mathbf{q},\dot{\mathbf{q}})=T(\mathbf{q},\dot{\mathbf{q}})-V(\mathbf{q})$ be the [[Lagrangian]] of a [[conservative system]], where
> $$T=\frac{1}{2}\sum_{i,j=1}^{n}a_{ij}(\mathbf{q})\dot{q}_{i}\dot{q}_{j}$$
> is the [[kinetic energy]] as given by the [[Kinetic energy|kinetic matrix]] $\mathrm{a}$ and $V$ is a velocity-independent [[potential]]. Then, if $V$ has a strict minimum, that minimum is a stable [[equilibrium point]].

> [!quote]- Proof
> Let $\mathbf{q}^{*}$ be the minimum of $V$. Then it is a [[Punto critico|stationary point]] of $V$:
> $$\frac{ \partial V }{ \partial q_{i} } (\mathbf{q}^{*})=0,\quad  \forall\ i=1,\ldots,n$$
> This guarantees that it is an equilibrium point. To prove stability, we use [[Ljapunov's theorem]] with $E(\mathbf{q},\dot{\mathbf{q}})=T(\mathbf{q},\dot{\mathbf{q}})-V(\mathbf{q})$ as a Ljapunov function. Then
> - In a neighborhood of $\mathbf{c}=(\mathbf{q}^{*},0)$ we must have $E>V(\mathbf{q}^{*})$.
> - $E(\mathbf{q},\dot{\mathbf{q}})$ is a [[constant of motion]], so $\mathcal{L}_{f}E=0$, where $f$ is the [[vector field]] of the system (as in $\dot{\mathbf{x}}=f(\mathbf{x})$).
>   
> This satisfies Ljapunov's theorem, so it is stable.

Some notes:
- The theorem can also be proven to be valid for velocity dependent potentials $V(\mathbf{q},\dot{\mathbf{q}})=V_{0}(\mathbf{q})+V_{1}(\mathbf{q},\dot{\mathbf{q}})$. In that case, the Ljapunov function must be $E=T-V_{0}$ instead.
- A lesser form of the theorem is also valid in nonconservative systems, but the stability is only guaranteed in the future.