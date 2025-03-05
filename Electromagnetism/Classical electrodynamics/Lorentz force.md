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
The electric field can be in any direction, so $\mathbf{E}\cdot d\mathbf{s}$ gives *something*. Meanwhile, the (instantaneous) velocity has at any moment the same direction as $d\mathbf{s}$, since it's defined as $\mathbf{v}=d\mathbf{s}/dt$. But remember that the [[Prodotto vettoriale|vector product]] is always perpendicular to both of its arguments, so $\mathbf{v}\times \mathbf{B}$ has to be perpendicular to $d\mathbf{s}=\mathbf{v}dt$, which means that the [[Prodotto scalare|scalar product]] is always zero: $(\mathbf{v}\times \mathbf{B})\cdot d\mathbf{s}=0$. So what we're left with is
$$dW=q\mathbf{E}\cdot d\mathbf{s}$$
The total work is then given by integrating this over any path.

The work is always carried out by the electric part of the force due to the charges having to move "counter-current" against the magnetic field. In this sense, a magnetic force just redirects an electric force, but it does no work itself, in the same way a normal force over a sloped surface redirects a force to push an object up against gravity but doesn't do work itself.

We can also express work through the [[electric current]] density. If we take an infinitesimal volume $dV$, the charge inside is $dq=\rho dV$:
$$dq\mathbf{E}\cdot \mathbf{v}dt=\rho dV\ \mathbf{E}\cdot \mathbf{v}dt=\mathbf{E}\cdot \rho \mathbf{v}\ dVdt=\mathbf{E}\cdot \mathbf{J}\ dVdt=d^{2}W$$
(the square on the work [[differential]] is because there are two infinitesimals now). If we pull "divide" by $dt$ and integrate over the volume we get the power:
$$P=\frac{dW}{dt}=\int_{V}\mathbf{E}\cdot \mathbf{J}\ dV$$
We can elaborate on $\mathbf{E}\cdot \mathbf{J}$:
$$\begin{align}
\mathbf{E}\cdot \mathbf{J}&=\mathbf{E}\cdot \frac{\nabla\times\mathbf{B}}{\mu_{0}}-\varepsilon_{0}\mathbf{E}\frac{ \partial \mathbf{E} }{ \partial t } \\
&=\mathbf{E}\cdot \frac{\nabla\times\mathbf{B}}{\mu_{0}}- \frac{\varepsilon_{0}}{2}\frac{ \partial E^{2} }{ \partial t }  \\
&=\frac{\mathbf{B}\cdot(\nabla\times\mathbf{E})}{\mu_{0}}- \frac{\nabla\cdot(\mathbf{E}\times \mathbf{B})}{\mu_{0}}- \frac{\varepsilon_{0}}{2} \frac{ \partial E^{2} }{ \partial t }  \\
&=- \frac{1}{\mu_{0}} \left( \mathbf{B}\cdot \frac{ \partial \mathbf{B} }{ \partial t } \right) - \frac{1}{\mu_{0}}(\nabla \cdot(\mathbf{E}\times \mathbf{B}))- \frac{\varepsilon_{0}}{2}\frac{ \partial E^{2} }{ \partial t } \\
&=- \frac{1}{2\mu_{0}}\frac{ \partial B^{2} }{ \partial t } - \frac{\varepsilon_{0}}{2}\frac{ \partial E^{2} }{ \partial t } -\nabla\cdot \mathbf{S}
\end{align}$$
where we used $\frac{ \partial E^{2} }{ \partial t }=\frac{ \partial  }{ \partial t }(\mathbf{E}\cdot \mathbf{E})=2\mathbf{E}\frac{ \partial \mathbf{E} }{ \partial t }$, expanded $\mathbf{E}\cdot \nabla\times\mathbf{B}$ using vector calculus, used [[Faraday's law]] and defined the [[Poynting vector]]
$$\mathbf{S}=\frac{1}{\mu_{0}}\mathbf{E}\times \mathbf{B}$$
