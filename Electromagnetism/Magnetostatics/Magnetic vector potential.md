The **magnetic vector potential** $\mathbf{A}$ is a [[Potenziale vettore|vector potential]] function whose [[curl]] is the [[magnetic field]] $\mathbf{B}$:
$$\nabla\times\mathbf{A}=\mathbf{B}$$
### Divergence and curl
The curl of the magnetic vector potential is obvious: it's just the definition. The [[divergence]] is more interesting. A vector potential remains such even after another function with no curl is added onto it
$$\tilde{\mathbf{A}}=\mathbf{A}+\mathbf{F}\quad\text{where}\quad \nabla\times\mathbf{F}=0$$
but a function whose curl is zero is always the [[gradient]] of a scalar function
$$\mathbf{F}=\nabla V$$
This allows us to state that the divergence of the vector potential is always zero:
$$\nabla\cdot\mathbf{A}=0$$
(same as the magnetic field). To rigorously prove this is true, suppose our original potential, $\mathbf{A}_{0}$, is *not* divergenceless. If we add to it the gradient of some function $G$ we get the new divergence
$$\nabla\cdot\mathbf{A}=\nabla\cdot\mathbf{A}_{0}+\nabla ^{2}V$$
For this to be zero, we must have $\nabla ^{2}V=-\nabla\cdot\mathbf{A}_{0}$. This is just [[Poisson's equation]] (if a bit foreign-looking) with $f=-\nabla\cdot\mathbf{A}_{0}$. If $\nabla\cdot\mathbf{A}_{0}$ goes to zero at infinity, solution then is
$$V=\frac{1}{4\pi}\int_{\mathcal{V}} \frac{\nabla\cdot\mathbf{A}_{0}}{\mathfrak{r}}\ d\tau'$$
which is the exact function that makes the $\nabla ^{2}V=-\nabla\cdot\mathbf{A}_{0}$ or, in other words, makes the divergence of $\mathbf{A}$ always zero. Since $V$ obeys Poisson's equation, and we can always solve Poisson's equation in some way or another, we can always find a $V$ for which the divergence of $\mathbf{A}$ is zero. In fact, we could pick a $V$ for which $\nabla\cdot\mathbf{A}$ is nonzero, but it's typically just plain easier to set $\nabla\cdot\mathbf{A}=0$ and pretend it doesn't exist, so we might as well.

This gives us permission to express [[Ampere's law]] like this:
$$\nabla\times\mathbf{B}=\nabla\times(\mathbf{\nabla\times\mathbf{A}})=\nabla(\nabla\cdot\mathbf{A})-\nabla ^{2}\mathbf{A}=-\mu_{0}\mathbf{J}$$
### Boundary conditions
Unlike the magnetic field, the vector potential does not exhibit a discontinuity across a surface current density $\mathbf{K}$. In fact, the lack of divergence implies that the normal component of the vector is continuous, whereas the curl
$$\oint \mathbf{A}\cdot d\mathbf{r}=\int \mathbf{B}\cdot d\mathbf{a}=\Phi$$
tells us that the tangential components are also continuous because the Amperian loop that we're using can be shrunk to be arbitrarily small, therefore continuously reducing the flux through the surface until it is zero. Therefore we can state
$$\mathbf{A}_\text{above}=\mathbf{A}_\text{below}$$
However, the (normal) derivative of $\mathbf{A}$ does inherit $\mathbf{B}$'s discontinuity:
$$\frac{ \partial \mathbf{A}_\text{above} }{ \partial n } -\frac{ \partial \mathbf{A}_\text{below} }{ \partial n } =-\mu_{0}\mathbf{K}$$
### Multipole expansion
The vector potential can be expanded in a [[Multipole expansion|multipole series]] in the same way the [[electric potential]] can. Given the position vector $\mathbf{r}$, the source vector $\mathbf{r}'$ and the angle $\alpha$ between the two, the vector potential of a current loop can be written as
$$\mathbf{A}(\mathbf{r})=\frac{\mu_{0}I}{4\pi}\oint \frac{1}{\mathfrak{r}}d\mathbf{r}'=\frac{\mu_{0}I}{4\pi}\sum_{n=0}^{\infty} \frac{1}{r^{n+1}}\oint(r')^{n}P_{n}(\cos \alpha)d\mathbf{r}'$$
where $P(\cos \alpha)$ are the [[Polinomi di Legendre|Legendre polynomials]]. Notably, the monopole term is just the displacement around a closed loop, which is always zero:
$$\oint d\mathbf{r}=0$$
which is an important confirmation of the fact that magnetic monopoles are not known to exist in nature and, beyond that, [[Maxwell's laws|Maxwell's equation]] $\nabla\cdot\mathbf{B}=0$ implicitly requires this to be so. Since the monopole term vanishes, the smallest terms is the dipole one:
$$\mathbf{A}_\text{dip}(\mathbf{r})=\frac{\mu_{0}I}{4\pi}\oint r'\cos \alpha \ d\mathbf{r}'=\frac{\mu_{0}I}{4\pi}\oint(\hat{\mathbf{r}}\cdot \mathbf{r}')d\mathbf{r}'$$
This can be written in a more illuminating way by seeing that
$$\oint(\hat{\mathbf{r}}\cdot \mathbf{r}')\ d\mathbf{r}'=-\hat{\mathbf{r}}\times \int d\mathbf{a}'$$
and thus
$$\boxed{\mathbf{A}_\text{dip}(\mathbf{r})=\frac{\mu_{0}}{4\pi} \frac{\mathbf{m}\times \mathbf{r}'}{r^{2}}}$$
where $\mathbf{m}$ is the [[magnetic dipole moment]]:
$$\mathbf{m}=I\int d\mathbf{a}=I\mathbf{a}$$
Unlike the [[electric dipole moment]], this one is completely independent on the choice of origin. This is due to the monopole moment being zero all the time. The magnetic field of a pure dipole (with infinitesimal area) is
$$\mathbf{B}_\text{dip}(\mathbf{r})=\nabla\times\mathbf{A}=\frac{\mu_{0}m}{4\pi r^{3}}(2\cos \theta \hat{\mathbf{r}}+\sin \theta \hat{\boldsymbol{\phi}})$$
in [[Cartesian coordinates]]. It can be rewritten in coordinate-free form as
$$\boxed{\mathbf{B}_\text{dip}(\mathbf{r})=\frac{\mu_{0}}{4\pi} \frac{1}{r^{3}}[3(\mathbf{m}\cdot \hat{\mathbf{r}})\hat{\mathbf{r}}-\mathbf{m}]}$$
