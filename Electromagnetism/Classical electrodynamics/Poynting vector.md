---
wiki-publish: true
---
The **Poynting vector** $\mathbf{S}$ is a vector that points in the direction of the flow of electromagnetic [[energy]]. It is defined as
$$\mathbf{S}\equiv \frac{1}{\mu_{0}}\mathbf{E}\times \mathbf{B}$$
where $\mathbf{E}$ is the [[electric field]] and $\mathbf{B}$ is the [[magnetic field]]. An interesting phenomenon to notice is that even static fields can lead to a movement of energy.

> [!example] Cylinder
> Consider a cylinder with a length of $L$ and radius $a$, an internal electric field $\mathbf{E}$ going through the length of the cylinder created by an [[electric potential]] difference $V$ between the ends of the cylinder, and a magnetic field $\mathbf{B}$ created by a current $I$ going through the cylinder.
> 
> ![[Diagram Poynting vector cylinder|80%]]
> 
> The electric field is uniform
> $$\mathbf{E}=\frac{V}{L}\hat{\mathbf{z}},\qquad\text{inside the wire}$$
> The magnetic field is dependent on the distance $s$ from the center of the cylinder
> $$\mathbf{B}(s)=\frac{\mu_{0}I}{2\pi s}\hat{\boldsymbol{\phi}},\qquad 0\leq s\leq a$$
> 
> The Poynting vector therefore is
> $$\mathbf{S}=\frac{1}{\mu_{0}}\mathbf{E}\times \mathbf{B}=\frac{1}{\mu_{0}} \frac{V}{L} \frac{\mu_{0}I}{2\pi s} \hat{\mathbf{z}}\times \hat{\boldsymbol{\phi}}=- \frac{VI}{2\pi L} \frac{1}{s}\hat{\mathbf{s}}$$
> Numerical value aside, notice the presence of the minus sign: it means that the vector is going towards the *inside* of the cylinder. In a way, energy is being "sucked in" by the center of the cylinder. This is what happens in, say, a simple electrical wire.

> [!example] Coaxial cylinders
> A similar situation is with two cylinders, with one embedded inside of the other. The length is still $L$ for both, with small and large radii $a$ and $b$. The electric potential difference $V$ is now applied in between the cylinders, so the electric field goes out radially. The current is still passing through the center, so the magnetic field is the same when $a\leq s\leq b$. This is the standard form of a cylindrical [[capacitor]].
> 
> ![[Diagram Poynting vector coaxial cylinders|80%]]
> 
> The electric field can be found by integrating the potential using the definition from $a$ to $b$ (remember the minus sign in front of the integral!), which gives the line charge density, and then through the usual field for a line charge density.
> $$V=-\int_{a}^{b}\mathbf{E}\cdot d\mathbf{s}=\frac{\lambda}{2\pi \varepsilon_{0}}\ln\left( \frac{b}{a} \right)\quad\Rightarrow \lambda=\frac{2\pi \varepsilon_{0}V}{\ln(b/a)}$$
> Assuming we're dealing with a large $L$, we can use the field for an infinite straight wire
> $$\mathbf{E}=\frac{\lambda}{2\pi \varepsilon_{0}s}\hat{\mathbf{s}}=\frac{V}{s\ln(b/a)}\hat{\mathbf{s}}$$
> The Poynting vector is
> $$S=\frac{1}{\mu_{0}} \frac{\mu_{0}I}{2\pi s} \frac{V}{s\ln(b/a)}\hat{\mathbf{s}}\times \hat{\boldsymbol{\phi}}=\frac{VI}{2\pi s^{2}\ln(b/a)}\hat{\mathbf{z}}$$
> The energy now goes down the length of the cylinders.
