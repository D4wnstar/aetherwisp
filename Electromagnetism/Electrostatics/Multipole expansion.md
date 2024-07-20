**Multipole expansion** is a way of approximating the [[electric potential]] of an arbitrary [[electric charge]] distribution using a [[serie di potenze|power series]] in $1/r$, with $r$ being the distance from the distribution. It exploits the fact that the potential of multipole systems depends on higher and higher inverse powers of the distance as more charges are added, starting from $\sim 1/r$ for a point charge and going to $\sim 1/r^{2}$ for an [[electric dipole]] and so on.

The formula for the potential multipole expansion of a charge distribution $\rho$ is
$$V(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\sum_{n=0}^{\infty} \frac{1}{r^{n+1}}\int(r')^{n}P_{n}(\cos \alpha)\rho(\mathbf{r}')\ d\tau'$$
where $P_{n}(\cos \alpha)$ represents the $n$-th [[Polinomi di Legendre|Legendre polynomial]] and $\alpha$ is the angle between $\mathbf{r}$ and $\mathbf{r}'$. The terms of the expansion are named after the multipoles: *monopole* term, *dipole* term, *quadrupole* term, and so on. The monopole term is precise at large distances; as one gets closer, further terms provide a more precise description.

The dependency in the integral is the position vector of the source charges. This means that the multipole expansion is strongly dependent on the [[frame of reference]] and origin that are chosen (as is the potential). Thus, moving the origin (or, equivalently, moving the charges) can drastically alter the multipole expansion, despite the system being physically identical. There is an important exception: if the total charge of the system is zero, then the multipole expansion is origin-independent.
### Derivation
We start from the potential of a volume charge distribution
$$V(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\int \frac{1}{\mathfrak{r}}\rho(\mathbf{r}')\ d\tau'$$
Using the [[Law of cosines]] we get
$$\mathfrak{r}^{2}=r^{2}+(r')^{2}-2rr'\cos \alpha=r^{2}\left[ 1+\left( \frac{r'}{r} \right)^{2}-2\left( \frac{r'}{r} \right)\cos \alpha \right]$$
where $\alpha$ is the angle between $\mathbf{r}$ and $\mathbf{r}'$. Thus
$$\mathfrak{r}=r\sqrt{ 1+\epsilon }\quad\text{where}\quad \epsilon\equiv\left( \frac{r'}{r} \right)\left( \frac{r'}{r}-2\cos \alpha \right)$$
For points well outside the charge distribution, $r$ is very large, so $\epsilon$ becomes negligible. This suggest the use of the [[binomial theorem]]:
$$\frac{1}{\mathfrak{r}}=\frac{1}{r} \frac{1}{\sqrt{ 1+\epsilon }}=\frac{1}{r}\left( 1- \frac{1}{2}\epsilon+ \frac{3}{8}\epsilon ^{2}- \frac{5}{16}\epsilon ^{3}+\ldots \right)$$
and replacing $\epsilon$
$$\frac{1}{\mathfrak{r}}=\frac{1}{r}\left[ 1- \frac{1}{2}\left( \frac{r'}{r} \right)\left( \frac{r'}{r}-2\cos \alpha \right) + \frac{3}{8}\left( \frac{r'}{r} \right)^{2}\left( \frac{r'}{r}-2\cos \alpha \right)^{2}-\ldots \right]=$$
$$=\frac{1}{r}\left( 1+\left( \frac{r'}{r} \right)\cos \alpha+ \left( \frac{r'}{r} \right)^{2} \frac{3\cos ^{2}\alpha-1}{2}+\ldots \right)$$
where we collected powers of $r'/r$ in the second step. As it happens, the coefficients for each term are actually the Legendre polynomials, so we can express the previous formula as
$$\frac{1}{\mathfrak{r}}=\frac{1}{r}\sum_{n=0}^{\infty} \left( \frac{r'}{r}^{n}P_{n}(\cos \alpha) \right)$$
If we substitute this expansion in the potential formula, we get the multipole expansion:
$$V(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\sum_{n=0}^{\infty} \frac{1}{r^{n+1}}\int(r')^{n}P_{n}(\cos \alpha)\rho(\mathbf{r}')\ d\tau'$$
### The monopole term
The monopole terms is, in general, the dominant one:
$$\boxed{V_\text{mon}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}} \frac{Q}{r}}$$
This is what we expect from a point charge, or for distributions like spheres which are identical *at large distances*. In fact, since a point charge *is* a monopole, this is the only term for its expansion and is an exact result.

This is also the only term that is independent on the choice of origin, as there is no mention of the source charge's position vector $\mathbf{r'}$.
### The dipole term
The dipole term is the second largest and can become dominant in case the total charge $Q$ is zero, in which chase the monopole term vanishes. The term is
$$V_\text{dip}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}} \frac{1}{r^{2}}\int r'\cos \alpha \rho(\mathbf{r}')\ d\tau'$$
Since $\alpha$ is the angle between $\mathbf{r}'$ and $\mathbf{r}$ we can write
$$r'\cos \alpha=\hat{\mathbf{r}}\cdot \mathbf{r}'$$
and the dipole term becomes
$$V_\text{dip}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}} \frac{1}{r^{2}}\hat{\mathbf{r}}\cdot \int \mathbf{r}'\rho(\mathbf{r}')\ d\tau'$$
The integral is defined as the [[electric dipole moment]] $\mathbf{p}$ of the distribution:
$$\mathbf{p}\equiv \int \mathbf{r}'\rho(\mathbf{r}')\ d\tau'$$
In this notation, the dipole potential becomes
$$\boxed{V_\text{dip}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}} \frac{\mathbf{p}\cdot\hat{\mathbf{r}}}{r^{2}}}$$
Since the dipole moment and potentials depend directly on $\rho$, they carry a geometric dependence from the shape, size and density of the source charge. Of course, the same can be defined for point charges, [[curva|lines]] and [[Superficie|surfaces]]. For example, for a system of point charges:
$$\mathbf{p}=\sum_{i=1}^{n} q_{i}\mathbf{r}_{i}'$$
For a *physical* dipole specifically (i.e. both charges are equal and opposite $q$ and $-q$) it becomes
$$\mathbf{p}=q\mathbf{r}'_{+}-q\mathbf{r}'_{-}=q(r'_{+}-r'_{-})=q\mathbf{d}$$
where $\mathbf{d}$ is the vector from the negative charge to the positive one.