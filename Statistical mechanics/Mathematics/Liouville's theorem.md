**Liouville's theorem** provides a local conservation law for [[Phase space|representative points]] in [[phase space]] of a [[dynamical system]]. It states that the density of representative points near a point in phase space is constant in time. In other words, state density is stationary and representative points behave like an incompressible fluid, in that their density does not change in time.

> [!info] Liouville's theorem
> Consider an [[ensemble]] with density function $\rho(q,p,t)$. The density function obeys the following equality:
> $$\frac{d\rho}{dt}=\frac{ \partial \rho }{ \partial t } +\sum_{i=1}^{3N} \left( \frac{ \partial \rho }{ \partial p_{i} } \dot{p}_{i}+ \frac{ \partial \rho }{ \partial q_{i} } \dot{q}_{i} \right)=\frac{ \partial \rho }{ \partial t } +\{ \rho,H \}=0$$
> where the curly braces are [[Parentesi di Poisson|Poisson brackets]] between $\rho$ and the [[Hamiltoniana|Hamiltonian]]. Alternatively, we can write
> $$\frac{ \partial \rho }{ \partial t } =\{ H,\rho \}$$
> This means that the number of representative points in [[Phase space|phase space]] is conserved, both globally and in a given volume.

This theorem only holds in [[conservative system|conservative systems]], i.e. systems where the phase space [[measure]] is constant over time.
### Proof
(TODO: Finish this) Calling $\mathbf{v}=(\dot{p}_{1},\ldots,\dot{p}_{3N},\dot{q}_{1},\ldots,\dot{q}_{3N})$, we have, by the continuity equation,
$$- \frac{d}{dt}\int_{\omega}\rho\ d\omega=\int_{S}\mathbf{\hat{n}}\cdot \mathbf{v}\ \rho\ dS$$
where $\omega$ is some volume of the phase space $\Gamma$, $S$ is the bounding surface of $\omega$ and $\hat{\mathbf{n}}$ is the normal vector from the surface. Then, using the [[Teorema della divergenza|divergence theorem]], we get
$$\int_{S}\hat{\mathbf{n}}\cdot \mathbf{v}\rho\ dS=$$
$$\int_{\omega}[\rho +\nabla \cdot(\rho \mathbf{v})]\ d\omega=0$$
for any $\omega$. So at this point we can state
$$- \frac{d\rho}{dt}=\nabla(\rho \mathbf{v})=\sum_{i=1}^{3N} \left[ \frac{ \partial  }{ \partial \rho } (p \dot{p}_{i})+ \frac{ \partial \omega }{ \partial q_{i} } (pq_{i}) \right]=\sum_{i=1}^{3N} p\underbrace{ \left( \frac{ \partial p }{ \partial p_{i} } +\frac{ \partial q }{ \partial q_{i} }  \right) }_{ =0 \text{ (Hamilton eqs.)}}+$$
### Quantum form
In quantum physics, the Liouville theorem takes on a similar form. Given a [[Hamiltonian]] $\hat{H}$ and a [[Matrice di densità|density matrix]] $\hat{\rho}$, an equivalent statement is
$$i\hbar \frac{ \partial \rho }{ \partial t } =[\hat{H},\hat{\rho}]$$
where $[\cdot,\cdot]$ is the [[Commutatore|commutator]] and $\hbar$ is the [[Costante di Planck|reduced Planck constant]]. This follows from the  [[Parentesi di Poisson|Poisson bracket]] conversion $\{ \cdot,\cdot \}\to \frac{1}{i\hbar} [\cdot,\cdot]$.
### Examples
> [!example] Damped harmonic oscillator
> Consider a [[Oscillatore armonico|damped harmonic oscillator]] (like a pendulum). It is described by $\dot{q}=p/m$ and $\dot{p}=-\gamma p-k\sin q$, where $\gamma$ is the dampening constant. We have
> $$-\gamma=\frac{ \partial \dot{p} }{ \partial p } +\frac{ \partial \dot{q} }{ \partial q } =0 $$
> and the [[Hamilton equations]]
> $$\dot{p}=-\frac{ \partial H }{ \partial q } ,\qquad \dot{q}=-\frac{ \partial H }{ \partial p }$$
> We want to check if the Liouville theorem holds and what $d\rho/dt$ is. To do so, we want to see if there exist a Hamiltonian for which the following holds:
> $$\frac{ \partial ^{2}H }{ \partial q\partial p } =\frac{ \partial \dot{q} }{ \partial q } ,\qquad \frac{ \partial ^{2}H }{ \partial q\partial p } =\frac{ \partial \dot{p} }{ \partial p } $$
> (TODO: Apparently we proved this, idk)
> 
> To find $d\rho/dt$ we use the continuity equations, which is always true, so
> $$\frac{ \partial \rho }{ \partial t } +\nabla\cdot(\mathbf{v}p)=0$$
> With some mathemagics we get
> $$\frac{ \partial \rho }{ \partial t } =-\frac{ \partial  }{ \partial q } (\rho \dot{q})-\frac{ \partial  }{ \partial p } (p \dot{p})=-\frac{ \partial \rho }{ \partial q } \dot{q}-\frac{ \partial \rho }{ \partial p } \dot{p}-\rho\left( \frac{ \partial \dot{q} }{ \partial q } + \frac{ \partial \dot{p} }{ \partial p }  \right)$$
> Since we know $\dot{q}$ and $\dot{p}$ this becomes
> $$\frac{ \partial \rho }{ \partial t } =\gamma \rho$$
