**Liouville's theorem** provides a local conservation law for [[Phase space|representative points]] in [[phase space]] of a [[dynamical system]]. It states that the density of representative points near a point in phase space is constant in time. In other words, state density is stationary and representative points behave like an incompressible fluid, in that their density does not change in time.

> [!info] Liouville's theorem
> Consider an [[ensemble]] with density function $\rho(q,p,t)$. The density function obeys the following equality:
> $$\frac{d\rho}{dt}=\frac{ \partial \rho }{ \partial t } +\sum_{i=1}^{3N} \left( \frac{ \partial \rho }{ \partial p_{i} } \dot{p}_{i}+ \frac{ \partial \rho }{ \partial q_{i} } \dot{q}_{i} \right)=\frac{ \partial \rho }{ \partial t } +\{ \rho,H \}=0$$
> where the curly braces are [[Poisson bracket|Poisson bracket]] between $\rho$ and the [[Hamiltoniana|Hamiltonian]]. Alternatively, we can write
> $$\frac{ \partial \rho }{ \partial t } =\{ H,\rho \}$$
> This means that the number of representative points in [[Phase space|phase space]] is conserved, both globally and in a given volume.

This theorem only holds in [[conservative system|conservative systems]], i.e. systems where the phase space [[measure]] is constant over time.
### Proof
Consider an arbitrary volume $\omega$ in some region of phase space. Call $\sigma$ the surface bounding this volume. Then, the rate at which the number of representative points contained in $\omega$ varies is given by the time derivative of the number:
$$\frac{ \partial  }{ \partial t } \int_{\omega}\rho\ d\omega$$
where the number is given by integrating the number density over $\omega$ and $d\omega=d^{3N}qd^{3N}p$. Calling $\mathbf{v}=(\dot{p}_{1},\ldots,\dot{p}_{3N},\dot{q}_{1},\ldots,\dot{q}_{3N})$ the velocity of a representative point, we have, by the [[continuity equation]],
$$- \frac{ \partial  }{ \partial t } \int_{\omega}\rho\ d\omega=\int_{\sigma}\mathbf{\hat{n}}\cdot \mathbf{v}\ \rho\ d\sigma\tag{1}$$
where $\hat{\mathbf{n}}$ is the normal vector from the surface. This is the outflow of representative points from $\omega$ (the decrease in contained points is equal to the number of points passing through the boundary). Then, using the [[Teorema della divergenza|divergence theorem]], we get
$$\int_{\sigma}\hat{\mathbf{n}}\cdot \mathbf{v}\ \rho\ d\sigma =\int_{\omega}\nabla\cdot\mathbf{(\rho \mathbf{v})}\ d\omega\tag{2}$$
Combining $1$ and $2$ we get
$$\frac{ \partial  }{ \partial t } \int_{\omega}\rho\ d\omega=-\int_{\omega}\nabla\cdot\mathbf{(\rho \mathbf{v})}\ d\omega \quad\to \quad \int_{\omega}\left( \frac{ \partial \rho }{ \partial t } +\nabla\cdot\mathbf{(\rho \mathbf{v})} \right)\ d\omega=0$$
Recall that $\omega$ was completely arbitrary. We have proven that this integral vanishes for $\omega$, and so it must vanish for *any* $\omega$, and therefore anywhere in phase space. But for an integral to vanish anywhere, in any subset of space, it must be the integral of zero. So
$$\frac{ \partial \rho }{ \partial t } +\nabla\cdot\mathbf{(\rho \mathbf{v})=0}\tag{3}$$
This is the continuity equation for representative points. The [[divergence]], when written explicitly in this space, reads
$$\nabla\cdot\mathbf{(\rho \mathbf{v})}=\sum_{i=1}^{3N} \left[ \frac{ \partial  }{ \partial q_{i} } (\rho \dot{q}_{i})+ \frac{ \partial  }{ \partial p_{i} } (\rho \dot{p}_{i}) \right]=\underbrace{ \sum_{i=1}^{3N} \left[ \frac{ \partial \rho }{ \partial q_{i} }\dot{q}_{i} +\frac{ \partial \rho }{ \partial p_{i} }\dot{p}_{i}  \right] }_{ \{ \rho,H \} }+\rho\sum_{i=1}^{3N} \left[ \underbrace{ \frac{ \partial \dot{q}_{i} }{ \partial q_{i} } +\frac{ \partial \dot{p}_{i} }{ \partial p_{i} } }_{ 0 }  \right]$$
The second step is by and expanding the derivatives. By the [[Hamilton equations]] of motion, the terms in the second sum are all zero, while the first is the [[Poisson bracket]] of $\rho$ and $H$. Using this knowledge in $(3)$ we can state
$$\frac{ \partial \rho }{ \partial t } +\{ \rho,H \}=0$$
which completes the proof. As an additional statement, since $\rho=\rho(q,p;t)$, we can merge the former statement into the [[Teorema del differenziale totale|total differential]] of $\rho$ and state:
$$\frac{d\rho}{dt}=0$$
which is the most straight-forward form of the theorem.
### Quantum form
In quantum physics, the Liouville theorem takes on a similar form. Given a [[Hamiltonian]] $\hat{H}$ and a [[Matrice di densità|density matrix]] $\hat{\rho}$, an equivalent statement is
$$i\hbar \frac{ \partial \rho }{ \partial t } =[\hat{H},\hat{\rho}]$$
where $[\cdot,\cdot]$ is the [[Commutatore|commutator]] and $\hbar$ is the [[Costante di Planck|reduced Planck constant]]. This follows from the  [[Poisson bracket|Poisson bracket]] conversion $\{ \cdot,\cdot \}\to \frac{1}{i\hbar} [\cdot,\cdot]$.
### Examples
> [!example] Damped harmonic oscillator
> We know that Liouville's theorem only holds for conservatives systems. As a counterpoint, let's examine a non-conservative system to see what happens. Consider a [[Harmonic oscillator|damped harmonic oscillator]] (like a pendulum). It is described by $\dot{q}=p/m$ and $\dot{p}=-\gamma p-k\sin q$, where $\gamma$ is the dampening constant. We have
> $$-\gamma=\frac{ \partial \dot{p} }{ \partial p } +\frac{ \partial \dot{q} }{ \partial q } =0 $$
> and the [[Hamilton equations]]
> $$\dot{p}=-\frac{ \partial H }{ \partial q } ,\qquad \dot{q}=-\frac{ \partial H }{ \partial p }$$
> We want to check if the Liouville theorem holds and what $d\rho/dt$ is. To do so, we want to see if there exist a Hamiltonian for which the following holds:
> $$\frac{ \partial ^{2}H }{ \partial q\partial p } =\frac{ \partial \dot{q} }{ \partial q } ,\qquad \frac{ \partial ^{2}H }{ \partial q\partial p } =\frac{ \partial \dot{p} }{ \partial p } $$
> (TODO: Apparently we proved this, idk)
> 
> To find $d\rho/dt$ we use the continuity equations, which is always true, so
> $$\frac{ \partial \rho }{ \partial t } +\nabla\cdot(\mathbf{v}\rho)=0$$
> With some mathemagics we get
> $$\frac{ \partial \rho }{ \partial t } =-\frac{ \partial  }{ \partial q } (\rho \dot{q})-\frac{ \partial  }{ \partial p } (p \dot{p})=-\frac{ \partial \rho }{ \partial q } \dot{q}-\frac{ \partial \rho }{ \partial p } \dot{p}-\rho\left( \frac{ \partial \dot{q} }{ \partial q } + \frac{ \partial \dot{p} }{ \partial p }  \right)$$
> Since we know $\dot{q}$ and $\dot{p}$ this becomes
> $$\frac{ \partial \rho }{ \partial t } =\gamma \rho$$
