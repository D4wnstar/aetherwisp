The **Lorentz force** is the force applied onto an [[electric charge]] in the presence of both an [[Electric field|electric]] and [[magnetic field]]. It is a more general case of [[Interazione elettromagnetica|Coulomb's law]], to which it goes back to if there is no magnetic field. It is
$$\mathbf{F}=q[\mathbf{E}+(\mathbf{v}\times \mathbf{B})]$$
where $\mathbf{v}$ is the velocity of the test charge $q$. These fields refer to external source fields.
### As a force density
It is possible to rewrite the Lorentz force as a force density over a volume. To do so, first notice that $q\mathbf{v}=I\mathbf{s}$, where $\mathbf{s}$ is a length of space in which the [[electric current]] $I$ runs. So
$$\mathbf{F}=q\mathbf{E}+I\mathbf{s}\times \mathbf{B}$$
If we divide by volume $V$ and notice that $I\mathbf{s}/V=\mathbf{J}$, being the volume current density, and using $q/V=\rho$ the volume charge density, we have
$$\mathbf{f}=\rho \mathbf{E}+\mathbf{J}\times \mathbf{B}$$
This is the force density. The amount $\mathbf{f}dV$ is the Lorentz force applied to the volume element $dV$.
### Work done
The Lorentz force does do [[work]], but only the electric part does. Magnetic forces do no work. In fact, the work per unit distance $d\mathbf{s}$ is
$$dW=\mathbf{F}\cdot d\mathbf{s}=q(\mathbf{E}+\mathbf{v}\times \mathbf{B})\cdot d\mathbf{s}=q\mathbf{E}\cdot d\mathbf{s}+q(\mathbf{v}\times \mathbf{B})\cdot d\mathbf{s}$$
The electric field can be in any direction, so $\mathbf{E}\cdot d\mathbf{s}$ gives *something*. Meanwhile, the (instantaneous) velocity has at any moment the same direction as $d\mathbf{s}$, since it's defined as $\mathbf{v}=d\mathbf{s}/dt$. But remember that the [[Vector product|vector product]] is always perpendicular to both of its arguments, so $\mathbf{v}\times \mathbf{B}$ has to be perpendicular to $d\mathbf{s}=\mathbf{v}dt$, which means that the [[Scalar product|scalar product]] is always zero: $(\mathbf{v}\times \mathbf{B})\cdot d\mathbf{s}=0$. So what we're left with is
$$dW=q\mathbf{E}\cdot d\mathbf{s}$$
The total work is then given by integrating this over any path.

The work is always carried out by the electric part of the force due to the charges having to move "counter-current" against the magnetic field. In this sense, a magnetic force just redirects an electric force, but it does no work itself, in the same way a normal force over a sloped surface redirects a force to push an object up against gravity but doesn't do work itself.
### Conservation of linear momentum
In a typical [[Physical system|system]] of [[point mass|point masses]], the [[linear momentum]] is conserved. This is because the forces between different point masses are assumed to lie on the axis connecting the points. If the forces are due to the Lorentz force however, this is no longer true, courtesy of the vector product in the equation. So does this mean that linear momentum fails to be conserved even in a [[conservative system]]? Well, if that happened the energy difference due to a changing total momentum would have to go *somewhere*, since conservation of energy can't be broken. But where?