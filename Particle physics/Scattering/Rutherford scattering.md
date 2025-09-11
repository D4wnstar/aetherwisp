---
wiki-publish: true
---
**Rutherford scattering** is an elastic [[particle scattering]] process where an [[electron]] scatters from an [[atomic nucleus]]. It is an [[Electromagnetism|electromagnetic]] scattering process. It has both classical and quantum formulations.
### Kinematics
The collision occurs in the relativistic regime, so we use the [[Four-vector|four-vector]] notation. The spacetime and energy-momentum four-vectors are
$$x=(x_{0},x_{1},x_{2},x_{3}),\quad p=(p_{0},p_{1},p_{2},p_{3})=\left( \frac{E}{c}, \mathbf{p}\right)$$

We know $p^{2}$ is a [[Relativistic invariant]], so
$$p^{2}=pp=\frac{E^{2}}{c^{2}}-\mathbf{p}^{2}$$
and also $p^{2}=m^{2}c^{4}$ in the rest frame where $\mathbf{p}=0$, $E=mc^{2}$. We define the [[Invariant mass]] $m=|\mathbf{p}|/c$. At rest, $E^{2}-\mathbf{p}^{2}c^{2}=m^{2}c^{4}$, but for relativistic energies we can approximate
$$\text{if }E\gg mc^{2} \Rightarrow E\sim|\mathbf{p}|c$$

![[Schema Diffusione di Rutherford|80%|center]]

The initial energy-momentum four-vectors are $p=(E/c, \mathbf{p})$ and $P=(Mc^{2}/c,0)$ for the electron and nucleus, respectively. Energy and momentum are conserved:
$$p+P=p'+P'=\left(\frac{E'}{c},\mathbf{p}'\right)+\left(\frac{E'_{n}}{c},\mathbf{P}'\right)\tag{*}$$

Assume elastic scattering. Then $m_{e}$ and $M$ are unchanged after the collision. Thus
$$p^{2}=p'^{2}=m_{e}^{2}c^{2},\quad P^{2}=P'^{2}=M^{2}c^{2}\quad \rightarrow \quad p\cdot P=p'\cdot P'$$
$$p\cdot P=p'(p+P-p')=p'\cdot p+p'\cdot P-m_{e}^{2}c^{2}\tag{1}$$

In frame $(*)$, using $(1)$:
$$(p\cdot P)c^{2}=(p'\cdot p+p'\cdot P-m_{e}c^{2})c^{2}=E'E+\mathbf{p}\cdot\mathbf{p}'+E'Mc^{2}-m_{e}^{2}c^{4}$$

At relativistic energies, $E\sim|\mathbf{p}|c$, so we neglect $m_{e}^{2}c^{4}$. We are left with
$$EMc^{2}=E'E(1-\cos\theta)+E'Mc^{2}$$

In the laboratory frame $(*)$:
$$E'=\frac{E}{\frac{E}{Mc^{2}}(1-\cos\theta)}$$
where $\theta$ is the scattering angle. This quantity is very important because it is easily measurable.

Consider a collision of an electron with a nucleus of charge $Ze$. We find the Rutherford [[cross section]].

*graph of Rutherford collision here*

#### Classical Method

The electron follows a hyperbolic trajectory ($\propto 1/r^{2}$). When far from the nucleus, it experiences no Coulomb repulsion. The potential is $V=0$, and kinetic energy is $T=\frac{1}{2}mv_{0}^{2}$. The angular momentum is $l=|\mathbf{r}\times m\mathbf{v}|=mv_{0}b$.

Here, $b$ is the impact parameter and $r_{min}$ is the minimum distance between the electron and nucleus. If $b=0$, it is a head-on collision and $r_{min}$ is minimized:
$$\frac{1}{2}mv_{0}^{2}=\frac{1}{4\pi\epsilon_{0}} \frac{zZe^{2}}{d}$$

Energy is conserved at any point along the trajectory:
$$\frac{1}{2}mv_{0}^{2}=\frac{1}{2}mv^{2}+ \frac{1}{4\pi\epsilon_{0}} \frac{zZe^{2}}{r}$$

*graph of cylindrical symmetry here*

There is cylindrical symmetry. Particles incident in the ring $b+db$ are distributed into a ring $d\theta$ on a detector at distance $r$. Let $df$ be the fraction of incident particles crossing the ring of area $2\pi bdb$:
$$df=nx(2\pi bdb)\tag{2}$$
where $n$ is the number of nuclei and $x$ is the foil thickness.

For impact parameters $<b$, the fraction is $f=nx\pi b^{2}$. The momenta $\mathbf{p}_{i}$ and $\mathbf{p}_{f}$ change direction. Far from the nucleus, $|\mathbf{p}|=mv_{0}$. Assuming a heavy nucleus, recoil is negligible.

*another graph here*

We use instantaneous coordinates $\mathbf{r}$ and $\beta$, where $\beta$ is the angle between the bisector and $\mathbf{r}$, with $\mathbf{r}$ locating the particle. Then
$$|\Delta\mathbf{p}|=2mv_{0}\sin\left(\frac{\theta}{2}\right)=2\pi v_{0}\cos\left(\frac{\pi-\theta}{2}\right)\tag{3}$$
assuming $|\mathbf{p}_{i}|=|\mathbf{p}_{f}|$. Now apply Newton’s second law $F=dp/dt$:
$$\Delta p =\int dp=\int Fdt=\frac{zZe^{2}}{4\pi\epsilon_{0}}\int \frac{\cos(\beta)}{r^{2}}dt\tag{4}$$
At $t=0$, $\beta=- (\pi-\theta)/2$; at $t=\infty$, $\beta= (\pi-\theta)/2$.

Compute instantaneous velocity $\mathbf{v}$:
$$\mathbf{v}=\frac{dr}{dt}\hat{r}+r \frac{d\beta}{dt}\hat{\beta}$$
Only the tangential component contributes near the nucleus:
$$l(\text{near nucleus})=|m\mathbf{r}\times\mathbf{v}|=mr^{2} \frac{d\beta}{dt}$$
$$l(\text{far away})=mv_{0}b$$

By conservation of angular momentum:
$$mr^{2} \frac{d\beta}{dt}=mv_{0}b \quad\rightarrow \quad \frac{dt}{r^{2}}=\frac{d\beta}{v_{0}b}$$

Substitute into $(4)$:
$$\Delta p = \frac{zZe^{2}}{4\pi\epsilon_{0}}\int_{-(\pi-\theta)/2}^{(\pi-\theta)/2} \cos\beta d\beta= \frac{zZe^{2}}{4\pi\epsilon_{0}v_{0}b} \cos\left(\frac{\theta}{2}\right)$$

Combine with $(3)$:
$$b=\frac{d}{2}\cot\left(\frac{\theta}{2}\right)$$

Then combine with $(2)$:
$$|df|=\pi nx \frac{d^{2}}{4}\cot\left(\frac{\theta}{2}\right)\csc^{2}\left(\frac{\theta}{2}\right)d\theta=\pi nx \frac{d^{2}}{4}\cot\left(\frac{\theta}{2}\right) \frac{1}{\sin^{2}\left(\frac{\theta}{2}\right)}d\theta\tag{5}$$

Now find the cross section:
$$\frac{d\sigma}{d\Omega}=\frac{1}{nx} \frac{df}{d\Omega}$$
where $nx$ is the number of nuclei per unit area and $df/d\Omega$ is the number of incident particles per solid angle. For annular geometry, $d\Omega=2\pi\sin\theta d\theta$.

Using $(1)$ and $(5)$:
$$\frac{d\sigma}{d\Omega}=\left(\frac{zZe^{2}}{8\pi\epsilon_{0}T}\right)^{2} \frac{\cot\left(\frac{\theta}{2}\right)}{2\sin\theta \sin^{2}\left(\frac{\theta}{2}\right)}=\left(\frac{zZe^{2}}{16\pi\epsilon_{0}T}\right)^{2} \frac{1}{\sin^{4}\left(\frac{\theta}{2}\right)}$$

Thus, the Rutherford cross section is:
$$\frac{d\sigma}{d\Omega}=\left(\frac{zZe^{2}}{4\pi\epsilon_{0}}\right)^{2} \left(\frac{1}{4T}\right)^{2} \frac{1}{\sin^{4}\left(\frac{\theta}{2}\right)}$$
It scales as $\propto z^{2}T^{-2}\sin^{-4}(\theta/2)$. These dependencies were experimentally confirmed by Geiger and Marsden.

#### Quantum Method

In the quantum regime, the [[Heisenberg uncertainty principle|uncertainty principle]] applies. Uncertainty $\Delta b$ in $b$ implies $\Delta p\sim \hbar/\Delta b$. The classical derivation holds if $\Delta b\ll b$ and $\Delta p\ll p$, i.e.
$$b\Delta p\gg \hbar \quad \rightarrow\quad \frac{b\Delta p}{\hbar}\gg 1$$

If $b\sim0$ and projectile energy is very high, the strong force becomes relevant, and Rutherford scattering breaks down. This can be used to estimate the nuclear radius.

To compute the Rutherford cross section via quantum mechanics, assume:
- nuclear recoil is negligible.
- initially, a point charge impinges on the atomic nucleus.
- the *Born approximation*: $Z\alpha\ll1$, where $\alpha=1/137$ is the [[Fine-structure constant]].

The incoming and outgoing electron [[wave function|wave functions]] are [[plane wave|plane waves]]:
$$\psi_{i}=\frac{1}{\sqrt{V}}e^{i \mathbf{p}\cdot\mathbf{r}/\hbar},\quad \psi_{f}=\frac{1}{\sqrt{V}}e^{i \mathbf{p}'\cdot\mathbf{r}/\hbar}$$
with $V$ the normalization volume. Electrons are free at $t=0$ and $t=+\infty$.

Treat discrete electron structures as continuous:
$$V=\frac{N}{n}$$
where $N$ is the number of scattering centers (effectively [[Nucleon|nucleons]]) and $n$ is the density. For large volume:
$$\int_{V}|\psi_{i}|^{2}dV=nV$$

Fermi’s golden rule gives the reaction rate:
$$W=\frac{\sigma v_{e}}{V}=\frac{2\pi}{\hbar}|\langle \psi_{f}|\mathcal{M}_{int}|\psi_{i}\rangle|^{2} \frac{dn}{dE_{f}}$$

Final-state energy $E_{f}$ satisfies $dE_{f}=dE'$.

The [[phase space]] density is:
$$dn(|\mathbf{p'}|)=\frac{4\pi |\mathbf{p'}|d |\mathbf{p'}|}{(2\pi\hbar)^{3}}V$$

The cross section for the electron into solid angle $d\Omega$ is:
$$d\sigma \frac{N}{V}=\frac{2\pi}{\hbar}|\langle \psi_{f}|\mathcal{H}_{int}|\psi_{i}\rangle|^{2} \frac{V |\mathbf{p'}|^{2}d |\mathbf{p'}|}{(2\pi\hbar)^{3}dE_{f}}d\Omega$$

Substitute $v \to c$ (relativistic limit, $|\mathbf{p'}|\sim E'/c$):
$$\frac{d\sigma}{d\Omega}=\frac{V^{2}}{(2\pi)^{2}} \frac{E'^{2}}{(\hbar c)^{4}} |\langle \psi_{f}|\mathcal{H}_{int}|\psi_{i}\rangle|^{2}$$

The interaction Hamiltonian is:
$$\mathcal{H}_{int}=\phi(\mathbf{r})$$
where $\phi(\mathbf{r})$ is the electric potential. The transition matrix is:
$$\mathcal{M}_{fi}=\langle \psi_{f}|\mathcal{H}_{int}|\psi_{i}\rangle=\frac{1}{V}\int e^{-i \mathbf{p}'\cdot \mathbf{r}/\hbar}V(\mathbf{r})e^{i\mathbf{p}\cdot \mathbf{r}/\hbar}d\mathbf{r}$$

Define the *transferred momentum* $\mathbf{q}\equiv\mathbf{p}-\mathbf{p}'$. Then:
$$\mathcal{M}_{fi}=\frac{1}{V}\int V(\mathbf{r}) e^{-i\mathbf{q}\cdot\mathbf{r}/\hbar}d\mathbf{r}$$
and
$$|\mathbf{q}|=2 |\mathbf{p}|\sin\left(\frac{\theta}{2}\right)$$
since $|\mathbf{p'}|=|\mathbf{p}|$ and $1-\cos\theta=2\sin^{2}(\theta/2)$. Then:
$$|\mathbf{q}|^{2}=4 |\mathbf{p}|^{2}\sin^{2}\left(\frac{\theta}{2}\right)$$

For a point charge with spherical symmetry:
$$V(\mathbf{r})= \frac{zZe^{2}}{4\pi\epsilon_{0}}\int \frac{\rho(\mathbf{r'})}{|\mathbf{r}-\mathbf{r'}|}d\mathbf{r'}$$

The matrix becomes:
$$\mathcal{M}_{fi}=\frac{zZe^{2}}{4\pi\epsilon_{0}V}\int e^{i\mathbf{q}\cdot\mathbf{r}/\hbar}\frac{1}{|\mathbf{r}-\mathbf{r'}|}d\mathbf{r}\int \rho(\mathbf{r'}) e^{i\mathbf{q}\cdot\mathbf{r}/\hbar}d\mathbf{r'}$$

Switch to spherical coordinates ($\alpha$: polar, $\phi$: azimuthal):
$$\int \frac{e^{i\mathbf{q}\cdot\mathbf{r}/\hbar}}{r}d\mathbf{r}=2\pi\int_{-1}^{1}d(\cos\alpha)\int_{0}^{\infty} e^{iqr\cos\alpha/\hbar}dr=2\pi\int_{0}^{\infty}\sin x dx$$
with $x=qr/\hbar$. This diverges. Introduce $e^{-\lambda x}$:
$$\int_{0}^{\infty}e^{-\lambda x}\sin xdx=\frac{1}{1+\lambda^{2}}$$
As $\lambda \to 0$, this gives 1. Then:
$$\int e^{iqD/\hbar} \frac{1}{D}dD=4\pi \left(\frac{\hbar}{q}\right)^{2}$$

The matrix becomes:
$$\mathcal{M}_{fi}=\frac{zZe^{2}}{\epsilon_{0}V} \frac{\hbar^{2}}{|\mathbf{q}|^{2}}\int \rho(\mathbf{r'}) e^{i\mathbf{q}\cdot\mathbf{r}/\hbar}d\mathbf{r'}$$

The integral is the [[Form factor]] $F(\mathbf{q})$.

For a point charge:
$$\mathcal{M}_{fi}=\frac{zZe^{2}}{\epsilon_{0}V} \frac{\hbar^{2}}{|\mathbf{q}|^{2}}$$
and the cross section is:
$$\frac{d\sigma}{d\Omega}=\left(\frac{zZe^{2}}{16\pi\epsilon_{0}}\right) \frac{4E'^{2}}{p^{4}c^{4}} \frac{1}{\sin^{4}(\frac{\theta}{2})}$$

In the relativistic limit ($E'=|\mathbf{p'}|c$):
$$\frac{d\sigma}{d\Omega}=\left(\frac{zZe^{2}}{8\pi\epsilon_{0}E'}\right)^{2} \frac{1}{\sin^{4}(\frac{\theta}{2})}$$

In the non-relativistic limit ($p=mv$, $E_{cin}=\frac{1}{2}mv^{2}$, $E'\sim mc^{2}$):
$$\frac{d\sigma}{d\Omega}=\left(\frac{zZe^{2}}{4\pi\epsilon_{0}}\right)^{2} \frac{1}{(4E_{cin})^{2}} \frac{1}{\sin^{4}(\frac{\theta}{2})}$$
matching the classical result.