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
### Poynting's theorem
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
If we extract and merge the time derivative from the first two terms, we are left with the electromagnetic energy density by volume $u$:
$$- \frac{1}{2\mu_{0}}\frac{ \partial B^{2} }{ \partial t } - \frac{\varepsilon_{0}}{2}\frac{ \partial E^{2} }{ \partial t }=-\frac{ \partial  }{ \partial t } \left( \frac{1}{2\mu_{0}}B^{2} + \frac{\varepsilon_{0}}{2}E^{2} \right)=-\frac{ \partial u }{ \partial t }$$
If we plug this back into the power expression, we get
$$P=-\frac{ \partial  }{ \partial t } \int_{V}u\ d\tau-\int_{V}\nabla\cdot\mathbf{S}=-\frac{ \partial  }{ \partial t } \int_{V}u\ d\tau-\oint_{S}\mathbf{S}\cdot d\mathbf{a}$$
where we used the [[Teorema della divergenza|divergence theorem]]. This final expression in commonly known as **Poynting's theorem**:
$$\boxed{P=-\frac{ \partial  }{ \partial t } \int_{V}u(\mathbf{r})\ d\tau-\oint_{S}\mathbf{S}\cdot d\mathbf{a}}$$
### Conservation of linear momentum
In a typical [[Physical system|system]] of [[point mass|point masses]], the [[linear momentum]] is conserved. This is because the forces between different point masses are assumed to lie on the axis connecting the points. If the forces are due to the Lorentz force however, this is no longer true, courtesy of the vector product in the equation. So does this mean that linear momentum fails to be conserved even in a [[conservative system]]? Well, if that happened the energy difference due to a changing total momentum would have to go *somewhere*, since conservation of energy can't be broken. But where?

To describe the problem quantitatively, let's start the Lorentz force in density form and, using [[Gauss' law]] and the [[Ampere's law|Ampere-Maxwell law]],
$$\mathbf{f}=\rho \mathbf{E}+\mathbf{J}\times \mathbf{B}=(\varepsilon_{0}\nabla\cdot\mathbf{E})\mathbf{E}+ \left( \frac{1}{\mu_{0}}\nabla\times\mathbf{B}-\varepsilon_{0} \frac{ \partial \mathbf{E} }{ \partial t }  \right)\times \mathbf{B}$$
Let's tackle the the terms one by one, using known vector calculus equations. Starting from
$$\frac{ \partial  }{ \partial t } (\mathbf{E}\times \mathbf{B})=\left( \frac{ \partial \mathbf{E} }{ \partial t } \times \mathbf{B} \right)+\left( \mathbf{E}\times \frac{ \partial \mathbf{B} }{ \partial t }  \right)$$
we can invert the equation to find
$$\frac{ \partial \mathbf{E} }{ \partial t } \times \mathbf{B}=\frac{ \partial }{ \partial t } (\mathbf{E}\times \mathbf{B})-\mathbf{E}\times \frac{ \partial \mathbf{B} }{ \partial t } =\frac{ \partial  }{ \partial t } (\mathbf{E}\times \mathbf{B})+\mathbf{E}\times(\nabla\times\mathbf{E})$$
using [[Faraday's law]]. Conveniently, this is the very last term of $\mathbf{f}$, barring $\varepsilon_{0}$. If we plug it in we get
$$\mathbf{f}=\varepsilon_{0}(\nabla\cdot\mathbf{E})\mathbf{E}+ \frac{1}{\mu_{0}}(\nabla\times\mathbf{B})\times \mathbf{B}-\varepsilon_{0}\frac{ \partial  }{ \partial t } (\mathbf{E}\times \mathbf{B})-\varepsilon_{0}\mathbf{E}\times(\nabla\times\mathbf{E})$$
Using the antisymmetric property of the vector product, we can write $(\nabla\times\mathbf{B})\times \mathbf{B}=-\mathbf{B}\times(\nabla\times\mathbf{B})$, so that the magnetic term is symmetrical to the electric one (the last one).

> [!tip] Gradient of a scalar product
> The [[gradient]] of a [[Prodotto scalare|scalar product]] is
> $$\nabla(\mathbf{A}\cdot \mathbf{B})=\mathbf{A}\times(\nabla\times\mathbf{B})+\mathbf{B}\times(\nabla\times\mathbf{A})+(\mathbf{A}\cdot \nabla)\mathbf{B}+(\mathbf{B}\cdot \nabla)\mathbf{A}$$
> If $\mathbf{A}=\mathbf{B}=\mathbf{E}$ we find
> $$\nabla(E^{2})=2\mathbf{E}\times(\nabla\times\mathbf{E})+2(\mathbf{E}\cdot \nabla)\mathbf{E}\quad\Rightarrow \quad \mathbf{E}\times(\nabla\times\mathbf{E})=\frac{1}{2}\nabla(E^{2})-(\mathbf{E}\cdot \nabla)\mathbf{E}$$
> Similarly if $\mathbf{A}=\mathbf{B}=\mathbf{B}$ (the first $\mathbf{B}$ is the generic vector, the second is the magnetic field) we get the same result: $\mathbf{B}\times(\nabla\times\mathbf{B})=\frac{1}{2}\nabla(B^{2})-(\mathbf{B}\cdot \nabla)\mathbf{B}$.

With the above box, and the definition of the Poynting vector $\mathbf{S}$, we now have pretty much everything to rewrite the force density in three major terms:
$$\begin{align}
\mathbf{f}&=\varepsilon_{0}\left[ (\nabla\cdot\mathbf{E})\mathbf{E}+(\mathbf{E}\cdot \nabla)\mathbf{E}- \frac{1}{2}\nabla(E^{2}) \right] \\
&+\frac{1}{\mu_{0}}\left[(\nabla\cdot\mathbf{B})\mathbf{B}+(\mathbf{B}\cdot \nabla)\mathbf{B} -\frac{1}{2}\nabla(\mathbf{B}^{2}) \right] \\
&-\varepsilon_{0}\varepsilon_{0}\frac{ \partial \mathbf{S} }{ \partial t } 
\end{align}$$
This is a very lengthy equation, with seven total terms. That said, we can very easily spot a symmetry between the electric and magnetic fields: in fact, if it weren't for the constants $\varepsilon_{0}$ and $1/\mu_{0}$, the terms would be identical, just with $\mathbf{E}$ changed to $\mathbf{B}$. Physically speaking, this is not random chance, and mathematically it can be exploited to express the equation in a much simpler form. To do so, we introduce the [[Maxwell stress tensor]] $T$, defined by its elements
$$T_{ij}=\varepsilon_{0}\left( E_{i}E_{j}- \frac{1}{2}\delta_{ij}E^{2} \right)+ \frac{1}{\mu_{0}}\left( B_{i}B_{j}- \frac{1}{2}\delta_{ij}B^{2} \right)$$
where $\delta_{ij}$ is the [[Delta di Kronecker]].