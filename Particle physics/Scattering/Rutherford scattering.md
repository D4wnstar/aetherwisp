---
wiki-publish: true
---
**Rutherford scattering** is an elastic [[particle scattering]] process where an [[Alpha decay|alpha particle]] scatters off of an [[atomic nucleus]]. It is an [[Electromagnetism|electromagnetic]] scattering process with both classical and quantum formulations. The process is
$$\alpha+\ce{X}\to \alpha+\ce{X}$$
where $\ce{X}$ represents the nucleus.
## Kinematics
We assume that the scattering happens in [[Lorentz transformation|relativistic]] regime, so we use [[Four-vector|four-vectors]]. The [[four-momentum]] is
$$p=(p_{0},p_{1},p_{2},p_{3})=\left( \frac{E}{c}, \mathbf{p}\right)$$

![[Diagram Rutherford scattering]]

The alpha particle collides with the nucleus elastically, so momentum is conserved. If we use a laboratory [[frame of reference]] in which the nucleus is at rest, the initial four-momenta are
$$p_{\alpha}=\left( \frac{E_{\alpha}}{c}, \mathbf{p}_{\alpha} \right),\quad p_{N}=\left( \frac{Mc^{2}}{c},0 \right)$$
for the alpha particle and nucleus, respectively. Then, due to conservation:
$$p_{\alpha}+p_{N}=p'_{\alpha}+p'_{N}\tag{1}$$
where we used a prime to denote the state after the scattering. Then
$$\lvert p_{\alpha}+p_{N}\rvert^{2}=\lvert p_{\alpha} \rvert^{2}+\lvert p_{N} \rvert ^{2}+2p_{\alpha}\cdot p_{N} $$
Same goes for the primed momenta. The square [[norm|norms]] are related to the [[Invariant mass|rest masses]] of the particles by
$$\lvert p_{\alpha} \rvert ^{2}=m_{\alpha,0}^{2}c^{2},\qquad \lvert p_{N} \rvert ^{2}=m_{N,0}^{2}c^{2}$$
Since the scattering is elastic, the particles don't change and so these also don't change, $\lvert p_{\alpha} \rvert^{2}=\lvert p_{\alpha}' \rvert^{2}$ and $\lvert p_{N} \rvert^{2}=\lvert p_{N}' \rvert^{2}$. This allows us to state
$$p_{\alpha}\cdot p_{N}=p_{\alpha}'\cdot p_{N}'$$
Now, we can assume that $p_{\alpha}$ and $p_{N}$ are known. $p_{\alpha}'$ can also be measured with a [[detector]]. $p_{N}'$ isn't known, but we can use $(1)$ to express it in terms of all the others:
$$p_{\alpha}\cdot p_{N}=p_{\alpha}'\cdot(p_{\alpha}+p_{N}-p_{\alpha}')=p_{\alpha}'\cdot p_{\alpha}+p_{\alpha}'\cdot p_{N}-m_{\alpha}^{2}c^{2}\tag{2}$$
If we place ourselves in the lab frame, where the nucleus is at rest before the collision, we can write the resulting momenta as
$$p_{\alpha}'=\left( \frac{E'_{\alpha}}{c},\mathbf{p}'_{\alpha} \right),\quad p_{N}'=\left( \frac{E'_{N}}{c},\mathbf{p}'_{N} \right)$$
We've chosen to write $p_{N}'$ in terms of the other three, so we're not going to need it. Knowing this, if we multiply both sides of $(2)$ by $c^{2}$ we get
$$\begin{align}
(p_{\alpha}\cdot p_{N})c^{2}&=(p'_{\alpha}\cdot p_{N}')c^{2} \\
&=(p'_{\alpha}\cdot p_{\alpha}+p'_{\alpha}\cdot p_{N}-m_{\alpha}^{2}c^{2})c^{2} \\
&=(p'_{\alpha}\cdot p_{\alpha})c^{2}+(p'_{\alpha}\cdot p_{N})c^{2}-m_{\alpha}^{2}c^{4} \\
&=E'_{\alpha}E_{\alpha}-(\mathbf{p}'_{\alpha}\cdot\mathbf{p}_{\alpha})c^{2}+E'_{\alpha}Mc^{2}-m_{\alpha}^{2}c^{4}
\end{align}$$
If we assume that the energy of the total energies $E_{\alpha}$ and $E_{\alpha}'$ are much higher than the rest energy $m_{\alpha}c^{2}$, then we can ignore the rest energy. The left hand side becomes $(p_{\alpha}\cdot p_{N})c^{2}=E_{\alpha}Mc^{2}$. In the right hand side, we can write the scalar product explicitly as $\mathbf{p}'_{\alpha}\cdot \mathbf{p}_{\alpha}=p'_{\alpha}p_{\alpha}\cos \theta$, where $\theta$ is the angle between the momentum vectors. In the high-energy regime we're in, the energy is approximately $E=\sqrt{ p^{2}c^{2}+m^{2}c^{4} }\simeq \sqrt{ p^{2}c^{2} }=pc$, so $p_{\alpha}'p_{\alpha}\cos \theta \simeq(E_{\alpha}'E_{\alpha}/c^{2})\cos \theta$. Put this in the right hand side to find
$$E_{\alpha}Mc^{2}=E'_{\alpha}E_{\alpha}(1-\cos\theta)+E'_{\alpha}Mc^{2}$$
Extract the alpha particle's energy to get
$$\boxed{E'_{\alpha}=\frac{E_{\alpha}}{1+\frac{E_{\alpha}}{Mc^{2}}(1-\cos\theta)}}$$
where $\theta$ is the scattering angle. This quantity can be measured through a detector, so it can be useful to invert the relation to find a different quantity in terms of this one.
## Cross section
Rutherford scattering involves a particle coming close to a nucleus, then getting pushed or pulled by electromagnetic forces. This of course occurs whenever the trajectory of the particle comes close enough to the nucleus for the repulsion to be significant. When aiming a particle beam at a target, most of the time the incident particles will be too far away from the nucleus to be significantly affected by it. To express the [[probability]] of a particle being scattered by the nucleus, we define the **Rutherford cross section**. There's two paths to reach this value, a classical one a quantum one. Both are presented below.
### Classical method
We'll use a generic particle as the projectile. Historically, Rutherford used alpha particles in his first experiments on the subject and today [[electron|electrons]] are especially used in real experiments because, being elementary particles, they don't have an internal structure, which makes some subsequent conclusions easier. This said, the results are largely only dependent on the [[Electric charge|charge]] of the projectile, as long as we assume it's smaller then the nucleus by a good margin. The only major difference is that negatively-charged particles are attracted by the nucleus, not repelled, so the scattering angle flips sign and goes in the opposite direction compared to positively-charged ones. The magnitude, however, stays largely the same.

Say our projectile has [[Electric charge|charge]] $ze$ and the nucleus has charge $Ze$, where $e$ is the [[elementary charge]]. We shoot the projectile towards the nucleus with initial velocity $\mathbf{v}_{0}$.

:::image
![[Diagram Rutherford scattering classical|100%]]
A diagram of Rutherford scattering in case of a positively-charge projectile.
:::

Our trajectory isn't likely to be head-on. The distance between the trajectory before scattering and the trajectory that would lead to a head-on collision[^1] is known as the **impact parameter** $b$. Once the projectile gets close to the nucleus, it'll be repelled or attracted by [[Electric field|Coulomb's law]][^2]. As in all non-bound trajectories drawn by a [[force]] that goes like $1/r^{2}$, it ends up being [[hyperbola|hyperbolic]].

To predict the trajectory, we use energy arguments. When far from the nucleus, the projectile experiences no electrostatic force and is a typical [[free particle]]. The [[potential energy]] is $U=0$ and the [[kinetic energy]] is $T=\frac{1}{2}mv_{0}^{2}$. The [[angular momentum]] with respect to the center of the nucleus is $L=|\mathbf{r}\times m\mathbf{v}|=mv_{0}b$.

When the projectile approaches the nucleus, it starts to feel the electrostatic force. It'll reach a point of closest approach, at a distance $r_\text{min}$, and then distance itself. $r_\text{min}$ is dependent on $b$; when $b=0$, you have a head-on collision, which leads to the lowest possible distance $d$. Which can calculate this by using conservation of energy and noting that in $d$, the kinetic energy must be zero (it's inverting direction) and all the energy left is electrostatic potential energy. So
$$\frac{1}{2}mv_{0}^{2}=\frac{1}{4\pi\epsilon_{0}} \frac{zZe^{2}}{d}$$
You can extract $d$ by inverting this:
$$\boxed{d=\frac{1}{2\pi \varepsilon_{0}} \frac{zZe^{2}}{mv_{0}^{2}}}$$
In most cases, energy conservation will gives us a mixture of kinetic and potential energy:
$$\frac{1}{2}mv_{0}^{2}=\frac{1}{2}mv^{2}+ \frac{1}{4\pi\epsilon_{0}} \frac{zZe^{2}}{r}$$

This interaction inherently has cylindrical symmetry. This is because the only geometrical property that the scattering angle depends on is the impact parameter. This means that it behaves the same regardless of where the projectile's trajectory is around the nucleus.

![[Diagram Rutherford scattering cylindrical symmetry|90%]]

In fact, all particles incident on some ring $[b,b+db]$ around the nucleus are scattered into an angular region $d\theta$. This ring has area $2\pi bdb$. A real target has a large number of nuclei and each of them has this ring around it. Call $df$ be the fraction of all incident particles that are going through this ring around *some* nucleus. To determine it, we need the number of nuclei, specifically their density over the impact surface. If $n$ is the volume density of nuclei and $x$ is the thickness of the target (you can imagine it as a thin foil), the surface density of nuclei will be $nx$. Thus, the fraction will be
$$df=nx\ 2\pi bdb\tag{3}$$
The fraction of all particles passing within a ring of radius $b$ (area $\pi b^{2}$) is instead
$$f=nx\ \pi b^{2}$$
If we consider the nucleus to be heavy enough with respect to the projectile to ignore recoil, then the initial and final momenta of the projectile, $\mathbf{p}_{i}$ and $\mathbf{p}_{f}$, are the same in magnitude. The only difference is the trajectory. Far from the nucleus, the magnitude is $\lvert \mathbf{p}_{i} \rvert=mv_{0}=\lvert \mathbf{p}_{f} \rvert$.

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

[^1]: If you want to be geometrically precise, the original trajectory is a straight line. This is because before scattering, the projectile is assumed to be a [[free particle]]. Now draw a parallel line to it and make it pass through the center of the nucleus. The distance between these two lines is the impact parameter.

[^2]: We assume that in case it's attracted, such as with an electron, it does not get captured and end up in a bound state. This is a sensible approximation since most interesting collisions involve high energy projectiles, which would require a much stronger pull to be captured. Nevertheless, it is possible, for instance if the projectile electron has low energy and the target is an [[ion]] that's missing one or more electrons.
