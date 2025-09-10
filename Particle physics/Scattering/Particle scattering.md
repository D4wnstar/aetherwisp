---
wiki-publish: true
---
**Particle scattering**, specifically in the context of particle physics, is [[scattering]] that occurs between [[particle|particles]]. Particles are considered to be [[quantum regime|quantum objects]], which makes this a form of quantum scattering, and often they are also considered to be [[Lorentz transformation|relativistic]]. As such, rigorously solving particle scattering behavior can be incredibly complex. Moreover, partly due to quantum physics and partly due to the minuscule scale, particle scattering is a largely [[random]] phenomenon, speaking of the [[probability]] of scattering more so than the certainty of it. Finally, due to [[wave-particle duality]], the participating particles can also be considered [[wave|waves]].

The typical particle scattering process (or reaction) looks like this:
$$a+b\to c+d$$
The letters represent the particles, with $a$ and $b$ being the incident particles and/or the target and $c$ and $d$ being the reaction products. $c$ and $d$ may very well be the same as $a$ and $b$, albeit in a different state. This is just an example of a two-particle interaction resulting in just as many particles. It's absolutely possible for there to be more inputs and outputs to the reaction, and for the number of inputs and outputs to differ from one another.

Particle scattering is ubiquitous. It's the foundation of many physical phenomena that we know, such as the color of the sky ([[Rayleigh scattering]]), and it is a fantastic experimental tool to probe the structure of particles, both as a whole and their internals. High-energy particle scattering is artificially created using a [[particle accelerator]], specifically a **collider**. In colliders specifically, you don't have a single incident particle. Rather, it's an entire **particle beam** being aimed at a **target**, with each particles in the beam being referred to as a **projectile**. The target maybe stationary or moving, with the most common moving targeting being another particle beam going in the opposite direction and made to collide.

Particles involved in scattering may be elementary particles like [[electron|electrons]], composite particles like [[proton|protons]] or even entire [[Atomic nucleus|nuclei]], [[atom|atoms]] or [[ion|ions]].

Particle scattering is often explained through [[Diagramma di Feynman|Feynman diagrams]], which are standardized schematic representations of particle scattering. Being entire diagrams, they can carry much more information than a simple mathematical representation, which is sorely needed given the complexity of many particle interactions.
### Elastic scattering
Particle scattering is elastic when [[kinetic energy]] is conserved (but may be redistributed) and the incident particles do not change in the process. A typical elastic process reads
$$a+b \rightarrow a'+b'$$
where $a'$ and $b'$ are primed just for visual clarity, and are otherwise identical to $a$ and $b$. $b$ is assumed to remain in its ground state, but nevertheless absorb some [[Linear momentum|momentum]] through its recoil.

![[Diagram Particle scattering elastic|60%|center]]

In the context of using scattering for probing the structure of particles, the [[wavelength]] of the incident wave-particle must be smaller than the length scale of the target. We can determine a range by invoking the [[Disuguaglianza di Heisenberg|Heisenberg inequality]]
$$\Delta x\Delta p\geq \frac{\hbar}{2}$$
The momentum is provided by the [[de Broglie formula]]
$$\bar{\lambda}=\frac{\lambda}{2\pi}=\frac{\hbar}{p}\quad\Rightarrow \quad p=\frac{\hbar}{\bar{\lambda}}$$
where $\bar{\lambda}$ is the reduced de Broglie wavelength. If we take the error on momentum to be the same scale as the momentum itself ($p=\Delta p$, not unreasonable for such a small scale), we get
$$\Delta p=p=\frac{\hbar}{\bar{\lambda}}\geq \frac{\hbar}{2\Delta x}\quad\Rightarrow \quad \bar{\lambda}\leq2\Delta x$$
So the reduced wavelength must be in the order of the spatial uncertainty. Recalling that the energy of a wave $E=pc$, we can also write
$$E=pc\geq \frac{\hbar c}{2\Delta x}$$
If we take a $\Delta x$ of a few femtometers (typical radius of the atomic nucleus), we get something between 10 and 100 [[Electronvolt|MeV]]. If we go further and take the [[charge radius]] of an individual proton (0.84 fm) we get just over 100 MeV. To go even deeper and probe the internals of single protons, the energy needs to go even higher, in the order several GeV[^1].
### Inelastic scattering
Particle scattering becomes inelastic when the kinetic energy transferred from $a$ to $b$ results in $b$ [[State transition|transitioning]] into an excited state $b^{*}$. $b^{*}$ then [[particle decay|decays]] into its ground state, emitting a particle or splitting into two or more new particles. Here it splits into $c$ and $d$. In symbols:
$$a+b\ \rightarrow\ a'+b^{*}\ \to\ a'+c+d$$

![[Diagram Particle scattering inelastic 1|60%|center]]

In inelastic scattering, it's also possible for the projectile $a$ to be absorbed by the target $b$ in order to fuse into one or more new particles, such as this:
$$a+b\to c+d+e$$

![[Diagram Particle scattering inelastic 2]]

This is especially common in beam-on-beam collisions in particle colliders (it's also the end goal, generally speaking).

In an experimental setting, if the original projectile $a'$ is the only particle that's detected from the scattering, then it's said to be **inclusive**. If all of the scattering and decay products are detected, it's said to be **exclusive**. Of course, if the projectile is absorbed, the scattering can't be inclusive[^2].
## Rutherford Scattering

Rutherford scattering is the scattering (collision) of $\alpha$ particles off a nucleus. Since $\alpha$ particles are not pointlike, we use electrons instead. The force between the electron and the nucleus is the [[Fundamental interaction#Electromagnetic interaction|electromagnetic interaction]].

### Kinematics of $e^{-}$ Scattering off a Nucleus

The collision occurs in the relativistic regime, so we use the [[Four-vector|four-vector]] notation. The spacetime and energy-momentum four-vectors are
$$x=(x_{0},x_{1},x_{2},x_{3}),\quad p=(p_{0},p_{1},p_{2},p_{3})=\left( \frac{E}{c}, \vec{p}\right)$$

We know $p^{2}$ is a [[Relativistic invariant]], so
$$p^{2}=pp=\frac{E^{2}}{c^{2}}-\vec{p}^{2}$$
and also $p^{2}=m^{2}c^{4}$ in the rest frame where $\vec{p}=0$, $E=mc^{2}$. We define the [[Invariant mass]] $m=|\vec{p}|/c$. At rest, $E^{2}-\vec{p}^{2}c^{2}=m^{2}c^{4}$, but for relativistic energies we can approximate
$$\text{if }E\gg mc^{2} \Rightarrow E\sim|\vec{p}|c$$

![[Schema Diffusione di Rutherford|80%|center]]

The initial energy-momentum four-vectors are $p=(E/c, \vec{p})$ and $P=(Mc^{2}/c,0)$ for the electron and nucleus, respectively. Energy and momentum are conserved:
$$p+P=p'+P'=\left(\frac{E'}{c},\vec{p}'\right)+\left(\frac{E'_{n}}{c},\vec{P}'\right)\tag{*}$$

Assume elastic scattering. Then $m_{e}$ and $M$ are unchanged after the collision. Thus
$$p^{2}=p'^{2}=m_{e}^{2}c^{2},\quad P^{2}=P'^{2}=M^{2}c^{2}\quad \rightarrow \quad p\cdot P=p'\cdot P'$$
$$p\cdot P=p'(p+P-p')=p'\cdot p+p'\cdot P-m_{e}^{2}c^{2}\tag{1}$$

In frame $(*)$, using $(1)$:
$$(p\cdot P)c^{2}=(p'\cdot p+p'\cdot P-m_{e}c^{2})c^{2}=E'E+\vec{p}\cdot\vec{p}'+E'Mc^{2}-m_{e}^{2}c^{4}$$

At relativistic energies, $E\sim|\vec{p}|c$, so we neglect $m_{e}^{2}c^{4}$. We are left with
$$EMc^{2}=E'E(1-\cos\theta)+E'Mc^{2}$$

In the laboratory frame $(*)$:
$$E'=\frac{E}{\frac{E}{Mc^{2}}(1-\cos\theta)}$$
where $\theta$ is the scattering angle. This quantity is very important because it is easily measurable.

Consider a collision of an electron with a nucleus of charge $Ze$. We find the Rutherford [[cross section]].

*graph of Rutherford collision here*

#### Classical Method

The electron follows a hyperbolic trajectory ($\propto 1/r^{2}$). When far from the nucleus, it experiences no Coulomb repulsion. The potential is $V=0$, and kinetic energy is $T=\frac{1}{2}mv_{0}^{2}$. The angular momentum is $l=|\vec{r}\times m\vec{v}|=mv_{0}b$.

Here, $b$ is the impact parameter and $r_{min}$ is the minimum distance between the electron and nucleus. If $b=0$, it is a head-on collision and $r_{min}$ is minimized:
$$\frac{1}{2}mv_{0}^{2}=\frac{1}{4\pi\epsilon_{0}} \frac{zZe^{2}}{d}$$

Energy is conserved at any point along the trajectory:
$$\frac{1}{2}mv_{0}^{2}=\frac{1}{2}mv^{2}+ \frac{1}{4\pi\epsilon_{0}} \frac{zZe^{2}}{r}$$

*graph of cylindrical symmetry here*

There is cylindrical symmetry. Particles incident in the ring $b+db$ are distributed into a ring $d\theta$ on a detector at distance $r$. Let $df$ be the fraction of incident particles crossing the ring of area $2\pi bdb$:
$$df=nx(2\pi bdb)\tag{2}$$
where $n$ is the number of nuclei and $x$ is the foil thickness.

For impact parameters $<b$, the fraction is $f=nx\pi b^{2}$. The momenta $\vec{p}_{i}$ and $\vec{p}_{f}$ change direction. Far from the nucleus, $|\vec{p}|=mv_{0}$. Assuming a heavy nucleus, recoil is negligible.

*another graph here*

We use instantaneous coordinates $\vec{r}$ and $\beta$, where $\beta$ is the angle between the bisector and $\vec{r}$, with $\vec{r}$ locating the particle. Then
$$|\Delta\vec{p}|=2mv_{0}\sin\left(\frac{\theta}{2}\right)=2\pi v_{0}\cos\left(\frac{\pi-\theta}{2}\right)\tag{3}$$
assuming $|\vec{p}_{i}|=|\vec{p}_{f}|$. Now apply Newton’s second law $F=dp/dt$:
$$\Delta p =\int dp=\int Fdt=\frac{zZe^{2}}{4\pi\epsilon_{0}}\int \frac{\cos(\beta)}{r^{2}}dt\tag{4}$$
At $t=0$, $\beta=- (\pi-\theta)/2$; at $t=\infty$, $\beta= (\pi-\theta)/2$.

Compute instantaneous velocity $\vec{v}$:
$$\vec{v}=\frac{dr}{dt}\hat{r}+r \frac{d\beta}{dt}\hat{\beta}$$
Only the tangential component contributes near the nucleus:
$$l(\text{near nucleus})=|m\vec{r}\times\vec{v}|=mr^{2} \frac{d\beta}{dt}$$
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
$$\psi_{i}=\frac{1}{\sqrt{V}}e^{i \vec{p}\cdot\vec{r}/\hbar},\quad \psi_{f}=\frac{1}{\sqrt{V}}e^{i \vec{p}'\cdot\vec{r}/\hbar}$$
with $V$ the normalization volume. Electrons are free at $t=0$ and $t=+\infty$.

Treat discrete electron structures as continuous:
$$V=\frac{N}{n}$$
where $N$ is the number of scattering centers (effectively [[Nucleon|nucleons]]) and $n$ is the density. For large volume:
$$\int_{V}|\psi_{i}|^{2}dV=nV$$

Fermi’s golden rule gives the reaction rate:
$$W=\frac{\sigma v_{e}}{V}=\frac{2\pi}{\hbar}|\langle \psi_{f}|\mathcal{M}_{int}|\psi_{i}\rangle|^{2} \frac{dn}{dE_{f}}$$

Final-state energy $E_{f}$ satisfies $dE_{f}=dE'$.

The [[phase space]] density is:
$$dn(|\vec{p'}|)=\frac{4\pi |\vec{p'}|d |\vec{p'}|}{(2\pi\hbar)^{3}}V$$

The cross section for the electron into solid angle $d\Omega$ is:
$$d\sigma \frac{N}{V}=\frac{2\pi}{\hbar}|\langle \psi_{f}|\mathcal{H}_{int}|\psi_{i}\rangle|^{2} \frac{V |\vec{p'}|^{2}d |\vec{p'}|}{(2\pi\hbar)^{3}dE_{f}}d\Omega$$

Substitute $v \to c$ (relativistic limit, $|\vec{p'}|\sim E'/c$):
$$\frac{d\sigma}{d\Omega}=\frac{V^{2}}{(2\pi)^{2}} \frac{E'^{2}}{(\hbar c)^{4}} |\langle \psi_{f}|\mathcal{H}_{int}|\psi_{i}\rangle|^{2}$$

The interaction Hamiltonian is:
$$\mathcal{H}_{int}=\phi(\vec{r})$$
where $\phi(\vec{r})$ is the electric potential. The transition matrix is:
$$\mathcal{M}_{fi}=\langle \psi_{f}|\mathcal{H}_{int}|\psi_{i}\rangle=\frac{1}{V}\int e^{-i \vec{p}'\cdot \vec{r}/\hbar}V(\vec{r})e^{i\vec{p}\cdot \vec{r}/\hbar}d\vec{r}$$

Define the *transferred momentum* $\vec{q}\equiv\vec{p}-\vec{p}'$. Then:
$$\mathcal{M}_{fi}=\frac{1}{V}\int V(\vec{r}) e^{-i\vec{q}\cdot\vec{r}/\hbar}d\vec{r}$$
and
$$|\vec{q}|=2 |\vec{p}|\sin\left(\frac{\theta}{2}\right)$$
since $|\vec{p'}|=|\vec{p}|$ and $1-\cos\theta=2\sin^{2}(\theta/2)$. Then:
$$|\vec{q}|^{2}=4 |\vec{p}|^{2}\sin^{2}\left(\frac{\theta}{2}\right)$$

For a point charge with spherical symmetry:
$$V(\vec{r})= \frac{zZe^{2}}{4\pi\epsilon_{0}}\int \frac{\rho(\vec{r'})}{|\vec{r}-\vec{r'}|}d\vec{r'}$$

The matrix becomes:
$$\mathcal{M}_{fi}=\frac{zZe^{2}}{4\pi\epsilon_{0}V}\int e^{i\vec{q}\cdot\vec{r}/\hbar}\frac{1}{|\vec{r}-\vec{r'}|}d\vec{r}\int \rho(\vec{r'}) e^{i\vec{q}\cdot\vec{r}/\hbar}d\vec{r'}$$

Switch to spherical coordinates ($\alpha$: polar, $\phi$: azimuthal):
$$\int \frac{e^{i\vec{q}\cdot\vec{r}/\hbar}}{r}d\vec{r}=2\pi\int_{-1}^{1}d(\cos\alpha)\int_{0}^{\infty} e^{iqr\cos\alpha/\hbar}dr=2\pi\int_{0}^{\infty}\sin x dx$$
with $x=qr/\hbar$. This diverges. Introduce $e^{-\lambda x}$:
$$\int_{0}^{\infty}e^{-\lambda x}\sin xdx=\frac{1}{1+\lambda^{2}}$$
As $\lambda \to 0$, this gives 1. Then:
$$\int e^{iqD/\hbar} \frac{1}{D}dD=4\pi \left(\frac{\hbar}{q}\right)^{2}$$

The matrix becomes:
$$\mathcal{M}_{fi}=\frac{zZe^{2}}{\epsilon_{0}V} \frac{\hbar^{2}}{|\vec{q}|^{2}}\int \rho(\vec{r'}) e^{i\vec{q}\cdot\vec{r}/\hbar}d\vec{r'}$$

The integral is the [[Form factor]] $F(\vec{q})$.

For a point charge:
$$\mathcal{M}_{fi}=\frac{zZe^{2}}{\epsilon_{0}V} \frac{\hbar^{2}}{|\vec{q}|^{2}}$$
and the cross section is:
$$\frac{d\sigma}{d\Omega}=\left(\frac{zZe^{2}}{16\pi\epsilon_{0}}\right) \frac{4E'^{2}}{p^{4}c^{4}} \frac{1}{\sin^{4}(\frac{\theta}{2})}$$

In the relativistic limit ($E'=|\vec{p'}|c$):
$$\frac{d\sigma}{d\Omega}=\left(\frac{zZe^{2}}{8\pi\epsilon_{0}E'}\right)^{2} \frac{1}{\sin^{4}(\frac{\theta}{2})}$$

In the non-relativistic limit ($p=mv$, $E_{cin}=\frac{1}{2}mv^{2}$, $E'\sim mc^{2}$):
$$\frac{d\sigma}{d\Omega}=\left(\frac{zZe^{2}}{4\pi\epsilon_{0}}\right)^{2} \frac{1}{(4E_{cin})^{2}} \frac{1}{\sin^{4}(\frac{\theta}{2})}$$
matching the classical result.

[^1]: Unfortunately, I can't give a specific $\Delta x$ to prove this numerically. Protons are [[hadron|hadrons]]; that's to say they are made of [[Quark|quarks]]. So you might ask: how big is a quark? And the answer is: nothing at all. Quarks, to our understanding, have no size, they are point-like. All experimental data seems to suggest so. So the very concept of size and size uncertainty stops making sense at the quark scale. The best that I can give you is "less than 0.84 fm".

[^2]: If this terminology seems horribly confusing and in reverse, then I'm sorry. It's just how it was defined, and you are not alone in confusion. The terms are the way they are because they are talking about the *processes*, not the particles. In an inclusive product, you detect only one particle. As such, there's an entire host of possible scatterings that could lead to this outcome. Then, since you lack the information needed to pinpoint exactly what happened, you *include* all possible processes that could've happened. Similarly, if you manage to detect absolutely everything, then there's no room for debate: there's one and only one process that could've happened and you can *exclude* every other. You might ask why even bother with inclusive scatterings then. The answer is that sometimes you only care about one aspect of a scattering and can ignore everything else, but in many other cases, it's purely down to the fact that detecting subatomic particles is *incredibly hard*, so sometimes you just don't get to detect everything regardless of whether you like it or not. See [here](https://physics.stackexchange.com/questions/1217/whats-the-difference-between-inclusive-and-exclusive-decays) for a discussion.
