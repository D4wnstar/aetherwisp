**Liouville's theorem** proves that the density of [[Gibbs ensemble|representative points]] near a point is constant and that the points behave like an incompressible fluid, in that their density does not change in time.

> [!info] Liouville's theorem
> Consider an [[ensemble]] with density function $\rho(q,p,t)$. The density function obeys the following equality:
> $$\frac{ \partial \rho }{ \partial t } +\sum_{i=1}^{3N} \left( \frac{ \partial \rho }{ \partial p_{i} } \dot{p}_{i}+ \frac{ \partial \rho }{ \partial q_{i} } \dot{q}_{i} \right)=0=\frac{d\rho}{dt}$$
> This means that the number of representative points in [[spazio delle fasi|phase space]] is conserved, both globally and in a given volume. Formally, the terms inside the sum are a [[Parentesi di Poisson|Poisson bracket]] between $\rho$ and the [[Hamiltoniana|Hamiltonian]], $\{ \rho,H \}$.
### Proof
(TODO: Finish this) Calling $\mathbf{v}=(\dot{p}_{1},\ldots,\dot{p}_{3N},\dot{q}_{1},\ldots,\dot{q}_{3N})$, we have, by the continuity equation,
$$- \frac{d}{dt}\int_{\omega}\rho\ d\omega=\int_{S}\mathbf{\hat{n}}\cdot \mathbf{v}\ \rho\ dS$$
where $\omega$ is some volume of the phase space $\Gamma$, $S$ is the bounding surface of $\omega$ and $\hat{\mathbf{n}}$ is the normal vector from the surface. Then, using the [[Teorema della divergenza|divergence theorem]], we get
$$\int_{S}\hat{\mathbf{n}}\cdot \mathbf{v}\rho\ dS=$$
$$\int_{\omega}[\rho +\nabla \cdot(\rho \mathbf{v})]\ d\omega=0$$
for any $\omega$. So at this point we can state
$$- \frac{d\rho}{dt}=\nabla(\rho \mathbf{v})=\sum_{i=1}^{3N} \left[ \frac{ \partial  }{ \partial \rho } (p \dot{p}_{i})+ \frac{ \partial \omega }{ \partial q_{i} } (pq_{i}) \right]=\sum_{i=1}^{3N} p\underbrace{ \left( \frac{ \partial p }{ \partial p_{i} } +\frac{ \partial q }{ \partial q_{i} }  \right) }_{ =0 \text{ (Hamilton eqs.)}}+$$
