---
wiki-publish: true
---
The **Lorentz force** is the force applied onto an [[electric charge]] in the presence of both an [[Electric field|electric]] and [[magnetic field]]. It is a more general case of [[Interazione elettromagnetica|Coulomb's law]], to which it goes back to if there is no magnetic field. It is
$$\mathbf{F}=q[\mathbf{E}+(\mathbf{v}\times \mathbf{B})]$$
where $\mathbf{v}$ is the velocity of the test charge $q$. These fields refer to external source fields.
### As a force density
It is possible to rewrite the Lorentz force as a force density over a volume. To do so, first notice that $q\mathbf{v}=I\mathbf{s}$, where $\mathbf{s}$ is a length of space in which the [[electric current]] $I$ runs. So
$$\mathbf{F}=q\mathbf{E}+I\mathbf{s}\times \mathbf{B}$$
If we divide by volume $V$ and notice that $I\mathbf{s}/V=\mathbf{J}$, being the volume current density, and using $q/V=\rho$ the volume charge density, we have
$$\mathbf{f}=\rho \mathbf{E}+\mathbf{J}\times \mathbf{B}$$
This is the force density. The amount $\mathbf{f}dV$ is the Lorentz force applied to the volume element $dV$.
### Using the Maxwell stress tensor
The Lorentz force can also be written in an extremely general and manifestly time-dependent form using the [[Maxwell stress tensor]] $T$ and the [[Poynting vector]] $\mathbf{S}$. The force is
$$\mathbf{F}=\oint_{\mathcal{S}}T\cdot d\mathbf{a}-\varepsilon_{0}\mu_{0}\frac{d}{dt} \int_{\mathcal{V}}\mathbf{S}\ d\tau$$
which reduces to
$$\mathbf{F}=\oint_{\mathcal{S}}T\cdot d\mathbf{a}$$
in static, time-independent contexts. Here, $\mathcal{V}$ is some volume and $\mathcal{S}$ is the bounding [[surface]] of that volume. The force density instead reads
$$\mathbf{f}=\nabla\cdot T-\varepsilon_{0} \mu_{0} \frac{ \partial \mathbf{S} }{ \partial t } $$
### Work done
The Lorentz force does do [[work]], but only the electric part does. Magnetic forces do no work. In fact, the work per unit distance $d\mathbf{s}$ is
$$dW=\mathbf{F}\cdot d\mathbf{s}=q(\mathbf{E}+\mathbf{v}\times \mathbf{B})\cdot d\mathbf{s}=q\mathbf{E}\cdot d\mathbf{s}+q(\mathbf{v}\times \mathbf{B})\cdot d\mathbf{s}$$
The electric field can be in any direction, so $\mathbf{E}\cdot d\mathbf{s}$ gives *something*. Meanwhile, the (instantaneous) velocity has at any moment the same direction as $d\mathbf{s}$, since it's defined as $\mathbf{v}=d\mathbf{s}/dt$. But remember that the [[Vector product|vector product]] is always perpendicular to both of its arguments, so $\mathbf{v}\times \mathbf{B}$ has to be perpendicular to $d\mathbf{s}=\mathbf{v}dt$, which means that the [[Scalar product|scalar product]] is always zero: $(\mathbf{v}\times \mathbf{B})\cdot d\mathbf{s}=0$. So what we're left with is
$$dW=q\mathbf{E}\cdot d\mathbf{s}$$
The total work is then given by integrating this over any path.

The work is always carried out by the electric part of the force due to the charges having to move "counter-current" against the magnetic field. In this sense, a magnetic force just redirects an electric force, but it does no work itself, in the same way a normal force over a sloped surface redirects a force to push an object up against gravity but doesn't do work itself.
### Conservation of linear momentum
According to the general form [[Newton's laws|Newton's second law]], the force on an object is the time derivative of its [[Linear momentum|momentum]]:
$$\mathbf{F}=\frac{d\mathbf{p}_\text{mech}}{dt}$$
Here we are specifically calling the momentum "mechanical": you'll see why in a moment. Since we know $\mathbf{F}$, we can see where this leads. We'll use the stress tensor form:
$$\frac{d\mathbf{p}_\text{mech}}{dt}=-\varepsilon_{0}\mu_{0}\frac{d}{dt} \int_{\mathcal{V}}\mathbf{S}\ d\tau+\oint_{\mathcal{S}}T\cdot d\mathbf{a}$$
This expression is remarkably similar to [[Poynting's theorem]] and it is sensible to interpret it in a similar manner. The volume integral must then be the momentum "stored" in the fields and the surface integral must be the momentum flowing in through the surface. This equation expresses conservation of momentum due to electromagnetic forces: if momentum "enters" through the surface, then the total "stored" momentum must increase.

Just like in Poynting's theorem, it is interesting to express the same statement using a density instead, in this case the **momentum density** $\mathbf{g}$. Dividing the first term by volume (and ignoring the sign) we get
$$\mathbf{g}=\varepsilon_{0}\mu_{0}\mathbf{S}=\varepsilon_{0}(\mathbf{E}\times \mathbf{B})$$
Meanwhile, the momentum [[flux]] transported by the fields must be $-T$.

If we keep the momentum static, such as when we are in empty space, we find
$$\frac{d\mathbf{g}}{dt}=\nabla\cdot T$$
This is the momentum continuity equation for electrodynamics. Just like energy, charges and fields constantly exchange momentum.