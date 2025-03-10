The **Maxwell stress tensor** is a symmetric second-order [[tensor]] in three dimensions used to simplify the equations of electrodynamics into shorter forms. It exploits the symmetries found between the [[electric field]] $\mathbf{E}$ and the [[magnetic field]] $\mathbf{B}$. It is defined through its components as
$$T_{ij}=\varepsilon_{0}\left( E_{i}E_{j}- \frac{1}{2}\delta_{ij}E^{2} \right)+ \frac{1}{\mu_{0}}\left( B_{i}B_{j}- \frac{1}{2}\delta_{ij}B^{2} \right)$$
where $\varepsilon_{0}$ is the [[vacuum permittivity]], $\mu_{0}$ is the [[vacuum permeability]] and $\delta_{ij}$ is the [[Kronecker delta]].
### Derivation
The motivation behind the tensor is that equations that we reach by applying the [[Lorentz force]] directly, despite being correct, quickly become extremely verbose and complicated. We want a way to explain the same phenomena without getting embroiled in a notational nightmare.

To start, of course, we write down the Lorentz force, specifically in density form.
$$\mathbf{f}=\rho \mathbf{E}+\mathbf{J}\times \mathbf{B}$$
Ideally, we want the most generic, expressive form that this equation can take. Then, we can seek simplifications to group up in a common quantity. Using [[Gauss' law]] and the [[Ampere's law|Ampere-Maxwell law]] we get
$$\mathbf{f}=(\varepsilon_{0}\nabla\cdot\mathbf{E})\mathbf{E}+ \left( \frac{1}{\mu_{0}}\nabla\times\mathbf{B}-\varepsilon_{0} \frac{ \partial \mathbf{E} }{ \partial t }  \right)\times \mathbf{B}$$
Let's tackle the the terms one by one, using known vector calculus equations. Starting from
$$\frac{ \partial  }{ \partial t } (\mathbf{E}\times \mathbf{B})=\left( \frac{ \partial \mathbf{E} }{ \partial t } \times \mathbf{B} \right)+\left( \mathbf{E}\times \frac{ \partial \mathbf{B} }{ \partial t }  \right)$$
we can invert the equation to find
$$\frac{ \partial \mathbf{E} }{ \partial t } \times \mathbf{B}=\frac{ \partial }{ \partial t } (\mathbf{E}\times \mathbf{B})-\mathbf{E}\times \frac{ \partial \mathbf{B} }{ \partial t } =\frac{ \partial  }{ \partial t } (\mathbf{E}\times \mathbf{B})+\mathbf{E}\times(\nabla\times\mathbf{E})$$
using [[Faraday's law]]. Conveniently, this is the very last term of $\mathbf{f}$, barring $\varepsilon_{0}$. If we plug it in we get
$$\mathbf{f}=\varepsilon_{0}(\nabla\cdot\mathbf{E})\mathbf{E}+ \frac{1}{\mu_{0}}(\nabla\times\mathbf{B})\times \mathbf{B}-\varepsilon_{0}\frac{ \partial  }{ \partial t } (\mathbf{E}\times \mathbf{B})-\varepsilon_{0}\mathbf{E}\times(\nabla\times\mathbf{E})$$
Using the anticommutative property of the vector product, we can write $(\nabla\times\mathbf{B})\times \mathbf{B}=-\mathbf{B}\times(\nabla\times\mathbf{B})$, so that the magnetic term is symmetrical to the electric one (the last one). Moreover, for the sake of symmetry, we can make the term $\frac{1}{\mu_{0}}(\nabla\cdot\mathbf{B})\mathbf{B}$ appear out of nowhere since $\nabla\cdot\mathbf{B}=0$ anyway. We get
$$\begin{align}
\mathbf{f}&=\varepsilon_{0}(\nabla\cdot\mathbf{E})\mathbf{E}-\varepsilon_{0}\mathbf{E}\times(\nabla\times\mathbf{E}) \\
&+ \frac{1}{\mu_{0}}(\nabla\cdot\mathbf{B})\mathbf{B}- \frac{1}{\mu_{0}}\mathbf{B}\times(\nabla\times\mathbf{B}) \\
&-\varepsilon_{0}\frac{ \partial  }{ \partial t } (\mathbf{E}\times \mathbf{B})
\end{align}$$

> [!tip] Gradient of a scalar product
> The [[gradient]] of a [[Scalar product|scalar product]] is
> $$\nabla(\mathbf{A}\cdot \mathbf{B})=\mathbf{A}\times(\nabla\times\mathbf{B})+\mathbf{B}\times(\nabla\times\mathbf{A})+(\mathbf{A}\cdot \nabla)\mathbf{B}+(\mathbf{B}\cdot \nabla)\mathbf{A}$$
> If $\mathbf{A}=\mathbf{B}=\mathbf{E}$ we find
> $$\nabla(E^{2})=2\mathbf{E}\times(\nabla\times\mathbf{E})+2(\mathbf{E}\cdot \nabla)\mathbf{E}\quad\Rightarrow \quad \mathbf{E}\times(\nabla\times\mathbf{E})=\frac{1}{2}\nabla(E^{2})-(\mathbf{E}\cdot \nabla)\mathbf{E}$$
> Similarly if $\mathbf{A}=\mathbf{B}=\mathbf{B}$ (the first $\mathbf{B}$ is the generic vector, the second is the magnetic field) we get the same result: $\mathbf{B}\times(\nabla\times\mathbf{B})=\frac{1}{2}\nabla(B^{2})-(\mathbf{B}\cdot \nabla)\mathbf{B}$.

With the above box and the definition of the [[Poynting vector]] $\mathbf{S}$, we now have pretty much everything to rewrite the force density in three major terms:
$$\begin{align}
\mathbf{f}&=\varepsilon_{0}\left[ (\nabla\cdot\mathbf{E})\mathbf{E}+(\mathbf{E}\cdot \nabla)\mathbf{E}- \frac{1}{2}\nabla(E^{2}) \right] \\
&+\frac{1}{\mu_{0}}\left[(\nabla\cdot\mathbf{B})\mathbf{B}+(\mathbf{B}\cdot \nabla)\mathbf{B} -\frac{1}{2}\nabla(B^{2}) \right] \\
&-\varepsilon_{0}\varepsilon_{0}\frac{ \partial \mathbf{S} }{ \partial t } 
\end{align}$$
As foreshadowed, this is a very lengthy equation, with seven total terms. That said, as we had hoped, we can very easily spot a symmetry between the electric and magnetic fields: in fact, if it weren't for the constants $\varepsilon_{0}$ and $1/\mu_{0}$, the terms would be identical, just with $\mathbf{E}$ changed to $\mathbf{B}$. Physically speaking, this is not random chance, and mathematically it can be exploited to express the equation in a much simpler form. To do so, we introduce the **Maxwell stress tensor** $T$, defined by its elements
$$T_{ij}=\varepsilon_{0}\left( E_{i}E_{j}- \frac{1}{2}\delta_{ij}E^{2} \right)+ \frac{1}{\mu_{0}}\left( B_{i}B_{j}- \frac{1}{2}\delta_{ij}B^{2} \right)$$
where $\delta_{ij}$ is the [[Kronecker delta]].