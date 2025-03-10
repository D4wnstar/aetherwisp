The **Maxwell stress tensor** is a three-dimensional symmetrical second-order [[tensor]] used to simplify the equations of electrodynamics into shorter forms. In plain terms, it's a $3\times3$ matrix. It exploits the symmetries found between the [[electric field]] $\mathbf{E}$ and the [[magnetic field]] $\mathbf{B}$. It is defined through its components as
$$T_{ij}=\varepsilon_{0}\left( E_{i}E_{j}- \frac{1}{2}\delta_{ij}E^{2} \right)+ \frac{1}{\mu_{0}}\left( B_{i}B_{j}- \frac{1}{2}\delta_{ij}B^{2} \right)$$
where $\varepsilon_{0}$ is the [[vacuum permittivity]], $\mu_{0}$ is the [[vacuum permeability]] and $\delta_{ij}$ is the [[Kronecker delta]]. Being symmetrical, $T_{ij}=T_{ji}$ for all $i$ and $j$.

Physically, the Maxwell stress tensor binds [[Lorentz force|electromagnetic forces]] to [[Linear momentum|momentum]]. Each component $ij$ has the units of a force per unit area, i.e. a [[pressure]] (negative pressure, to be exact). Each component can be interpreted as the negative pressure parallel to the $i$-th axis applied onto a surface that is normal to the $j$-th axis. For instance, the $T_{xx}$ component is a pressure directed on the $x$ applied on a surface perpendicular to the $x$ axis. The easiest cases to imagine are the ones on the diagonals, $T_{xx}$, $T_{yy}$ and $T_{zz}$, since the forces are perpendicular to the surfaces. Off-diagonal elements like $T_{xy}$ and $T_{zx}$ instead represent [[shear]], a force parallel to the surface. Note that the pressure is negative: these forces *pull* the surface, not push it (though of course it depends on the signs of the electric and magnetic fields, but the force is always reversed, so to speak).

![[Diagram Maxwell stress tensor components]]

> [!question] A note on notation
> Like much of the literature using tensors, these notes generally use the "sum over repeated indexes" notation popularized by Einstein, generally known as [[Einstein notation]]. Normally, a [[scalar product]] between the $j$-th column tensor $T$ and a vector $\mathbf{a}$ would be written as
> $$(T\cdot \mathbf{a})_{j}=\sum_{i=1}^{3} T_{ij}a_{i}$$
> For brevity, whenever two identical indices appear in the same expression, the summation will be *implied*:
> $$\sum_{i=1}^{3} T_{ij}a_{i}\quad\to \quad T_{ij}a_{i}$$
> As such, scalar products (and really any operation dealing with sums of components) is written much more briefly:
> $$(T\cdot \mathbf{a})_{j}=T_{ij}a_{i}$$
> 
> It is common in tensor calculus to split indexes between subscript and superscript, such as for instance writing $T^{i}_{j}$ instead of $T_{ij}$. In certain contexts, the location of the index (above or below) is given a special meaning, but this is not done in the classical part of the electrodynamics notes. It is however done in the relativistic part.
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
#### Divergence
As ti stands, it is unclear how $T_{ij}$ can help us in simplifying anything, much less $\mathbf{f}$. The reason why it is useful is hidden behind the [[divergence]] of $T$ as a whole. The divergence is usually only defined on [[Vector space|vectors]], but can be defined more broadly over tensors as a whole, as an operation that reduces the order of the tensor by one. Since vectors are first order tensors, their divergence is a zero order tensor, i.e. a [[scalar]]. The divergence of a second order tensor like $T$ therefore must be a first order tensor, i.e. a vector.

Unfortunately, tensors are very complicated objects and calculating their divergence is everything but straightforward. What we can do is calculate the divergence for each axis $j$. In this context, the divergence is defined as
$$(\nabla\cdot T)_{j}=\sum_{i=1}^{3} \nabla_{i}\left[ \varepsilon_{0}\left( E_{i}E_{j}- \frac{1}{2}\delta_{ij}E^{2} \right) + \frac{1}{\mu_{0}}\left( B_{i}B_{j}- \frac{1}{2}\delta_{ij}B^{2} \right)\right]$$
where we are taking the [[gradient]] of each $ij$ component and then summing over all of them[^1].

[^1]: This is not using Einstein notation. If it did, the sum $\sum_{i=1}^{3}$ would be implicit, relying on the fact that the index $i$ appears on both $\nabla_{i}$ and the terms inside the square brackets.
