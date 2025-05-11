---
wiki-publish: true
---
**Clausius' theorem** states

> [!info] Clausius' theorem
> For every [[Thermodynamic transformation|thermodynamic cycle]], the following inequality holds:
> $$\oint \frac{dQ}{T}\leq0$$
> If the cycle is reversible, then equality holds.
#### Proof
Let's consider a cyclical transformation $\theta$ and let's divide it in $n$ steps. In every step, we bring the system in contact with $n$ [[heat reservoir|heat reservoirs]] at temperatures $T_{1},\ldots,T_{n}$. The reservoirs absorb [[heat]] $Q_{1},\ldots,Q_{n}$. Let's define $n$ [[Carnot engine|Carnot engines]] $C_{1},\ldots,C_{n}$ such that $C_{i}$ operates between reservoirs $T_{\theta}$ and $T_{i}$ by absorbing heat $Q_{i}^{\theta}$ from $T_{\theta}$ and dumping heat $Q_{i}$ in $T_{i}$. The total heat absorbed from $T_{\theta}$ is
$$Q_{\theta}=\sum_{i=1}^{n} Q_{i}^{\theta}=\sum_{i=1}^{n} T_{0} \frac{Q_{i}}{T_{i}}$$
and therefore
$$\sum_{i=1}^{n} \frac{Q_{i}}{T_{i}}\leq 0$$
For an infinite amount if steps $n\to \infty$, the sum becomes an integral and thus
$$\oint \frac{dQ}{T}\leq 0$$
### Corollary
Clausius' theorem implicitly states the following corollary:

> [!info] Corollary
> The integral $\int \frac{dQ}{T}$ is independent of path. It is uniquely determined by the start and end [[stato|states]].

#### Proof
Consider a generic integration loop between points $A$ and $B$, divided in two paths $I$ and $II$, each representing a reversible transformation. Let's call $-II$ the reverse path of $II$. The joint path $I\to -II$ forms a reversible cycle. But from Clausius' theorem we know that
$$\int_{I\to -II} \frac{dQ}{T}=\int_{I} \frac{dQ}{T}+\int_{-II} \frac{dQ}{T}=\int_{I} \frac{dQ}{T}-\int_{II} \frac{dQ}{T}=0$$
and so
$$\int_{I} \frac{dQ}{T}=\int_{II} \frac{dQ}{T}$$
