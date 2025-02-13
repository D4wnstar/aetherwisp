The **Lorentz force** is the force applied onto an [[electric charge]] in the presence of both an [[Electric field|electric]] and [[magnetic field]]. It is a more general case of [[Interazione elettromagnetica|Coulomb's law]], to which it goes back to if there is no magnetic field. It is
$$\mathbf{F}=Q[\mathbf{E}+(\mathbf{v}\times \mathbf{B})]$$
where $\mathbf{v}$ is the velocity of the test charge $Q$. These fields refer to external source fields.

If only a magnetic field is present, the law becomes $\mathbf{F}_\text{mag}=Q(\mathbf{v}\times \mathbf{B})$. This in an important distinction: since the application of magnetic forces is always perpendicular to motion, they do no work . In fact
$$dW_\text{mag}=\mathbf{F}_\text{mag}\cdot d\mathbf{r}=Q(\mathbf{v}\times \mathbf{B})\cdot \mathbf{v}dt=0$$
because $\mathbf{v}\times \mathbf{B}$ is always perpendicular to $\mathbf{v}$. The work is actually always carried out by the electric part of the force due to the charges having to move "counter-current" against the magnetic field. In this sense, a magnetic force just redirects an electric force, but it does no work itself, in the same way a normal force over a sloped surface redirects a force to push an object up against gravity but doesn't do work itself.
### As a force density
It is possible to rewrite the Lorentz force as a force density over a volume. To do so, first notice that $Q\mathbf{v}=I\mathbf{s}$, where $\mathbf{s}$ is a length of space in which the [[electric current]] $I$ runs. So
$$\mathbf{F}=Q\mathbf{E}+I\mathbf{s}\times \mathbf{B}$$
If we divide by volume $V$ and notice that $I\mathbf{s}/V=\mathbf{J}$, being the volume current density, and using $Q/V=\rho$ the volume charge density, we have
$$\mathbf{f}=\rho \mathbf{E}+\mathbf{J}\times \mathbf{B}$$
This is the force density. The amount $\mathbf{f}dV$ is the Lorentz force applied to the volume element $dV$.