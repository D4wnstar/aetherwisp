---
wiki-publish: true
aliases:
  - steady current
  - continuity equation
---
The **electric current** $\mathbf{I}$ is the rate of change of [[electric charge]] in a given point. In other words, it's how much charge is passing through a location. It is measured in Amperes, which are Coulombs per second:
$$\text{A}\equiv \frac{\text{C}}{\text{s}}$$
By convention, negative charges moving to the left count the same as positive charges moving to the right. This is to reflect the physical fact that almost all laws regarding charge movement depend on the product of charge and velocity, so if you reverse the signs of both, the phenomenon doesn't change. For an example, see the [[Lorentz force]]. In practice, it's usually [[Elettrone|electrons]] that move and they do so in the opposite direction of the current.

A current is said to be **steady** or **stationary** if it does not vary with time:
$$\frac{\partial \mathbf{J}}{\partial t}=0$$
This are of major important as they constitute the basis of the entirety of magnetostatics.  In fact, a temporally constant current produces only constant magnetic fields and is the magnetic equivalent of a stationary charge for electrostatics. They are also good approximations of household currents.
### Linear current
The most common case of current is one going through a wire. In this case, we can represent the charge as a line density:
$$I=\lambda v$$
because a segment of length $v\Delta t$ carrying charge $\lambda v\Delta t$ goes through a point $P$ in a time interval $\Delta t$. This derivation shows that current is actually a vector
$$\mathbf{I}=\lambda \mathbf{v}$$
though since current is usually constrained to a very specific path (like the aforementioned wire), it's common practice to just use the scalar form and give the direction for granted. When it comes to surface and volume currents however, the distinction must be clear.

The magnetic force on a current carrying wire subject to a [[magnetic field]] $\mathbf{B}$ is
$$\mathbf{F}_\text{mag}=\int(\mathbf{v}\times \mathbf{B})\ dq=\int(\mathbf{v}\times \mathbf{B})\lambda\ dl=\int(\mathbf{I}\times \mathbf{B})\ dl$$
Since $\mathbf{I}$ and $d\mathbf{I}$ point in the same direction, we can rewrite the result as
$$\mathbf{F}_\text{mag}=\int I(d\mathbf{I}\times \mathbf{B})$$
Since the current is often constant, the force usually is
$$\mathbf{F}_\text{mag}=I\int(d\mathbf{I}\times \mathbf{B})$$
### Surface current
A current may also move over a surface instead of a line. In this case, we can defined the **surface current density** $\mathbf{K}$. Consider a "ribbon" of infinitesimal width $dl_{\perp}$, running parallel to the flow like a surfer on a wave. If the (linear) current (density) in the ribbon is $d\mathbf{I}$, then the surface current density is
$$\mathbf{K}\equiv \frac{d\mathbf{I}}{dl_{\perp}}$$
In other words, it's the current per unit width of the surface. If we have a surface charge density $\sigma$ moving at a velocity $\mathbf{v}$, then the current density is
$$\mathbf{K}=\sigma \mathbf{v}$$
The magnetic force on the surface current is
$$\mathbf{F}_\text{mag}=\int(\mathbf{v}\times \mathbf{B})\sigma\ da=\int(\mathbf{K}\times \mathbf{B})\ da$$
As with the electric force on a [[conductor]], the magnetic field suffers a discontinuity across the surface and we instead use the average of the fields above and below.
### Volume current
A current may also move in space. Here we define the **volume current density** $\mathbf{J}$. Consider a "tube" of infinitesimal cross-section $da_{\perp}$ running parallel to the flow like an airplane in a wind current. If the current in the tube is $\mathbf{I}$, then the volume current density is
$$\mathbf{J}\equiv \frac{d\mathbf{I}}{da_{\perp}}$$
Like the surface density, it's the current per unit area of the volume. If the volume charge $\rho$ is moving at a velocity $\mathbf{v}$, then the current density is
$$\mathbf{J}=\rho \mathbf{v}$$
and the magnetic force on the volume current is
$$\mathbf{F}_\text{mag}=\int(\mathbf{v}\times \mathbf{B})\rho\ d\tau=\int(\mathbf{J}\times \mathbf{B})\ d\tau$$
### Continuity equation
The volume current density allows us to reach a fundamental result for currents. Rewrite the linear current in terms of the volume density
$$I=\int_{S}Jda_{\perp}=\int_{S}\mathbf{J}\cdot d\mathbf{a}$$
We can then apply the [[Divergence theorem|divergence theorem]] to get
$$\oint_{S}\mathbf{J}\cdot d\mathbf{a}=\int_{V}\nabla\cdot\mathbf{J}\ d\tau$$
which is the the charge per unit time leaving the surface $S$. But charge is always conserved, so the charge the exits must leave a deficit of charge behind:
$$\int_{V}\nabla\cdot\mathbf{J}\ d\tau=- \frac{d}{dt}\int_{V}\rho\ d\tau=-\int_{V}\frac{ \partial \rho }{ \partial t }\ d\tau$$
Since there is no requirement on the volume chosen, we can extract the integrands to get the **continuity equation**:
$$\boxed{\nabla\cdot\mathbf{J}=- \frac{ \partial \rho }{ \partial t } }$$
This is the mathematical statement that encapsulates local charge conservation. In the magnetostatic case, it becomes
$$\nabla\cdot\mathbf{J}=0$$
