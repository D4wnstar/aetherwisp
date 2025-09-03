---
wiki-publish: true
---
The **Lorentz force** is the force applied onto an [[electric charge]] in the presence of both an [[Electric field|electric]] and [[magnetic field]]. It is a more general case of [[Electromagnetism|Coulomb's law]], to which it goes back to if there is no magnetic field. It is
$$\mathbf{F}=q[\mathbf{E}+(\mathbf{v}\times \mathbf{B})]$$
where $\mathbf{v}$ is the velocity of the test charge $q$. These fields refer to external source fields.
### As a force density
It is possible to rewrite the Lorentz force as a force density over a volume. To do so, first notice that $q\mathbf{v}=I\mathbf{s}$, where $\mathbf{s}$ is a length of space in which the [[electric current]] $I$ runs. So
$$\mathbf{F}=q\mathbf{E}+I\mathbf{s}\times \mathbf{B}$$
If we divide by volume $\mathcal{V}$ and notice that $I\mathbf{s}/\mathcal{V}=\mathbf{J}$, being the volume current density, and using $q/\mathcal{V}=\rho$ the volume charge density, we have
$$\mathbf{f}=\rho \mathbf{E}+\mathbf{J}\times \mathbf{B}$$
This is the force density. The amount $\mathbf{f}d\tau$ is the Lorentz force applied to the volume element $d\tau$.
### Using the Maxwell stress tensor
The Lorentz force can also be written in an extremely general and manifestly time-dependent form using the [[Maxwell stress tensor]] $\mathrm{T}$ and the [[Poynting vector]] $\mathbf{S}$. The force is
$$\mathbf{F}=\oint_{\mathcal{S}}\mathrm{T}\cdot d\mathbf{a}-\varepsilon_{0}\mu_{0}\frac{d}{dt} \int_{\mathcal{V}}\mathbf{S}\ d\tau$$
which reduces to
$$\mathbf{F}=\oint_{\mathcal{S}}\mathrm{T}\cdot d\mathbf{a}$$
in static, time-independent contexts. Here, $\mathcal{V}$ is some volume and $\mathcal{S}$ is the bounding [[surface]] of that volume. The force density instead reads
$$\mathbf{f}=\nabla\cdot \mathrm{T}-\varepsilon_{0} \mu_{0} \frac{ \partial \mathbf{S} }{ \partial t } $$
### Work done
The Lorentz force does do [[work]], but only the electric part does. Magnetic forces do no work. In fact, the work per unit distance $d\mathbf{s}$ is
$$dW=\mathbf{F}\cdot d\mathbf{s}=q(\mathbf{E}+\mathbf{v}\times \mathbf{B})\cdot d\mathbf{s}=q\mathbf{E}\cdot d\mathbf{s}+q(\mathbf{v}\times \mathbf{B})\cdot d\mathbf{s}$$
The electric field can be in any direction, so $\mathbf{E}\cdot d\mathbf{s}$ gives *something*. Meanwhile, the (instantaneous) velocity has at any moment the same direction as $d\mathbf{s}$, since it's defined as $\mathbf{v}=d\mathbf{s}/dt$. But remember that the [[Vector product|vector product]] is always perpendicular to both of its arguments, so $\mathbf{v}\times \mathbf{B}$ has to be perpendicular to $d\mathbf{s}=\mathbf{v}dt$, which means that the [[Scalar product|scalar product]] is always zero: $(\mathbf{v}\times \mathbf{B})\cdot d\mathbf{s}=0$. So what we're left with is
$$dW=q\mathbf{E}\cdot d\mathbf{s}$$
The total work is then given by integrating this over any path.

The work is always carried out by the electric part of the force due to the charges having to move "counter-current" against the magnetic field. In this sense, a magnetic force just redirects an electric force, but it does no work itself, in the same way a normal force over a sloped surface redirects a force to push an object up against gravity but doesn't do work itself.
### Newton's third law
Consider a point charge $q$ going at speed $v$ down the $x$ axis. Its electric and magnetic fields emit radially, as per the [[Liénard-Wiechert potentials]]. Say then that another charge $q$ travels down the $y$ axis. They would repel each other off the axes of course, but assume they are forced to remain on them through tracks or something of the sort. The electric force between them is clearly repulsive, so let's look at the magnetic one.

![[Diagram Broken Newton 3rd law|80%]]

The magnetic field of the particle 1 goes into the page ($-\hat{\mathbf{z}}$) at the position of particle 2. The force, by right hand rule, is to the right ($\hat{\mathbf{x}}$). Similarly, the magnetic field of 2 goes out of the page ($\hat{\mathbf{z}}$) at the position of 1, so the force is up ($\hat{\mathbf{y}}$). These are manifestly *not* opposites, so they do not cancel out. The action, so to say, does not result in an equal and opposite reaction. There's something very wrong with [[Newton's laws|Newton's third law]] here, because it clearly does not hold in electrodynamics. But that's a problem: the conservation of [[Linear momentum|momentum]] relies on the third law! So how do we fix it? Well, we fix it by saying that it's not just the particles that carry momentum, but also the *fields* themselves.
#### Conservation of linear momentum
According to the general form [[Newton's laws|Newton's second law]], the force on an object is the time derivative of its momentum:
$$\mathbf{F}=\frac{d\mathbf{p}_\text{mech}}{dt}$$
Here we are specifically calling the momentum "mechanical": you'll see why in a moment. Since we know $\mathbf{F}$, we can see where this leads. We'll use the stress tensor form:
$$\frac{d\mathbf{p}_\text{mech}}{dt}=-\varepsilon_{0}\mu_{0}\frac{d}{dt} \int_{\mathcal{V}}\mathbf{S}\ d\tau+\oint_{\mathcal{S}}\mathrm{T}\cdot d\mathbf{a}$$
This expression is remarkably similar to [[Poynting's theorem]] and it is sensible to interpret it in a similar manner. The volume integral must then be the momentum "stored" in the fields
$$\mathbf{p}_\text{field}=\mu_{0}\varepsilon_{0}\int_{\mathcal{V}}\mathbf{S}d\tau$$
and the surface integral must be the momentum flowing in through the surface. The mechanical momentum must be the total of these two. This equation expresses conservation of momentum due to electromagnetic forces: if momentum "enters" through the surface, then the total "stored" momentum must increase.

Just like in Poynting's theorem, it is interesting to express the same statement using a density instead, in this case the **momentum density** $\mathbf{g}$. Dividing the field momentum by volume we get
$$\boxed{\mathbf{g}=\varepsilon_{0}\mu_{0}\mathbf{S}=\varepsilon_{0}(\mathbf{E}\times \mathbf{B})}$$
Meanwhile, the momentum [[flux]] transported by the fields must be $-T$.

If we keep the mechanical momentum static, such as when we are in empty space, the time derivative vanishes and we can rearrange the conservation law to read
$$\frac{\partial \mathbf{g}}{\partial t}=\nabla\cdot \mathrm{T}$$
This is the momentum continuity equation for electrodynamics. Just like with energy and electric charge, individual charges and their fields constantly exchange momentum, with the *total* momentum being conserved.
#### Conservation of angular momentum
Just like how fields carry angular momentum, they also carry [[angular momentum]]. By definition $\mathbf{L}=\mathbf{r}\times \mathbf{p}$, so the **angular momentum density** $\boldsymbol{\ell}$ must be
$$\boxed{\boldsymbol{\ell}=\mathbf{r}\times \mathbf{g}=\varepsilon_{0}[\mathbf{r}\times(\mathbf{E}\times \mathbf{B})]}$$
This is interpreted in the same way as above: it's not just charges that induce an angular momentum, fields themselves also carry it and this amount is mandatory for the conservation law to be upheld.
### Relativity
The Lorentz force has a relativistic expression as a [[Minkowski force]] in [[spacetime]] caused by the [[electromagnetic tensor]] $F^{\mu \nu}$. A charge $q$ moving at [[proper velocity]] $\eta^{\mu}=(\gamma c,\mathbf{v})$ will be subject to a relativistic Lorentz force
$$\boxed{K^{\mu}=q\eta_{\nu}F^{\mu \nu}}$$

> [!quote]- Deriving the classical Lorentz force
> The spatial components of $K^{\mu}$ are given by $\mu=1,2,3$. For $\mu=1$:
> $$\begin{align}
> K^{1}&=q\eta_{\nu}F^{1\nu} \\
> &=q(-\eta^{0}F^{10}+\eta^{1}F^{11}+\eta^{2}F^{12}+\eta^{3}F^{13}) \\
> &=q\left[ \frac{-c}{\sqrt{ 1-v^{2}/c^{2} }}\left( - \frac{E_{x}}{c} \right) + \frac{u_{y}}{\sqrt{ 1-v^{2}/c^{2} }}B_{z}+  \frac{v_{z}}{\sqrt{ 1-v^{2}/c^{2} }}(-B_{y})\right] \\
> &=\frac{q}{\sqrt{ 1-v^{2}/c^{2} }}[\mathbf{E}+(\mathbf{u}\times \mathbf{B})]_{x}
> \end{align}$$
> Thus, with the other two components we get
> $$\mathbf{K}=\frac{q}{\sqrt{ 1-v^{2}/c^{2} }}[\mathbf{E}+(\mathbf{v}\times \mathbf{B})]=\gamma q[\mathbf{E}+(\mathbf{v}\times \mathbf{B})]$$
> and since the spatial components of a Minkowski force are related to the ordinary force by $\mathbf{K}=\gamma\mathbf{F}$ we get
> $$\mathbf{F}=q[\mathbf{E}+(\mathbf{v}\times \mathbf{B})]$$
