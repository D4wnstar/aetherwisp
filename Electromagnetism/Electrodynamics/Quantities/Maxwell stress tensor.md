---
wiki-publish: true
---
The **Maxwell stress tensor** is a three-dimensional symmetric second-order [[tensor]] used to simplify the equations of electrodynamics into shorter forms. In plain terms, it's a $3\times3$ [[symmetric matrix]]. It exploits the symmetries found between the [[electric field]] $\mathbf{E}$ and the [[magnetic field]] $\mathbf{B}$. It is defined through its components as
$$T_{ij}=\varepsilon_{0}\left( E_{i}E_{j}- \frac{1}{2}\delta_{ij}E^{2} \right)+ \frac{1}{\mu_{0}}\left( B_{i}B_{j}- \frac{1}{2}\delta_{ij}B^{2} \right)$$
where $\varepsilon_{0}$ is the [[vacuum permittivity]], $\mu_{0}$ is the [[vacuum permeability]] and $\delta_{ij}$ is the [[Kronecker delta]]. Being symmetrical, $T_{ij}=T_{ji}$ for all $i$ and $j$.

Physically, the Maxwell stress tensor binds [[Lorentz force|electromagnetic forces]] to [[Linear momentum|momentum]]. Each component $ij$ has the units of a force per unit area, i.e. a [[pressure]] (negative pressure, to be exact). Each component can be interpreted as the negative pressure on the $i$-th axis applied onto a surface that is normal to the $j$-th axis. For instance, the $T_{xx}$ component is a pressure directed on the $x$ axis applied on a surface perpendicular to the $x$ axis. The easiest cases to imagine are the ones on the diagonals, $T_{xx}$, $T_{yy}$ and $T_{zz}$, since the forces are perpendicular to the surfaces. Off-diagonal elements like $T_{xy}$ and $T_{zx}$ instead represent [[shear]], a force parallel to the surface. Note that the pressure is negative: these forces *pull* the surface, not push it (though of course it depends on the signs of the electric and magnetic fields, but the force is always reversed, so to speak).

![[Diagram Maxwell stress tensor components]]

> [!question] A note on notation
> Like much of the literature using tensors, these notes generally use the "sum over repeated indexes" notation popularized by Einstein, known as [[Einstein notation]]. Normally, a [[scalar product]] between the $j$-th column of a tensor $T$ and a vector $\mathbf{a}$ would be written as
> $$(T\cdot \mathbf{a})_{j}=\sum_{i=1}^{3} T_{ij}a_{i}$$
> For brevity, whenever two identical indices appear in the same expression, the summation will be *implied*:
> $$\sum_{i=1}^{3} T_{ij}a_{i}\quad\to \quad T_{ij}a_{i}$$
> As such, scalar products (and really any operation dealing with sums of components) is written much more briefly:
> $$(T\cdot \mathbf{a})_{j}=T_{ij}a_{i}$$
> 
> It is common in tensor calculus to split indexes between subscript and superscript, such as for instance writing $T^{i}_{j}$ instead of $T_{ij}$. In certain contexts, the location of the index (above or below) is given a special meaning, but this is not relevant in the classical part of electrodynamics, so it will be unused in this part of the notes. It is however be used in notes on the theory of relativity.
### Derivation
The motivation behind the tensor is that equations that we reach by applying the [[Lorentz force]] directly, despite being correct, quickly become extremely verbose and complicated. We want a way to explain the same phenomena without getting embroiled in a notational nightmare.

To start, we write the Lorentz force in density form:
$$\mathbf{f}=\rho \mathbf{E}+\mathbf{J}\times \mathbf{B}$$
Ideally, we want the most generic, expressive form that this equation can take. Using [[Gauss' law]] and the [[Ampere's law|Ampere-Maxwell law]] we get
$$\mathbf{f}=(\varepsilon_{0}\nabla\cdot\mathbf{E})\mathbf{E}+ \left( \frac{1}{\mu_{0}}\nabla\times\mathbf{B}-\varepsilon_{0} \frac{ \partial \mathbf{E} }{ \partial t }  \right)\times \mathbf{B}$$
Let's tackle the the terms one by one, using known vector calculus equations. The derivative of a [[curl]] is
$$\frac{ \partial  }{ \partial t } (\mathbf{E}\times \mathbf{B})=\left( \frac{ \partial \mathbf{E} }{ \partial t } \times \mathbf{B} \right)+\left( \mathbf{E}\times \frac{ \partial \mathbf{B} }{ \partial t }  \right)$$
we can invert the equation to find
$$\frac{ \partial \mathbf{E} }{ \partial t } \times \mathbf{B}=\frac{ \partial }{ \partial t } (\mathbf{E}\times \mathbf{B})-\mathbf{E}\times \frac{ \partial \mathbf{B} }{ \partial t } =\frac{ \partial  }{ \partial t } (\mathbf{E}\times \mathbf{B})+\mathbf{E}\times(\nabla\times\mathbf{E})$$
using [[Faraday's law]]. Conveniently, this is the very last term of $\mathbf{f}$, barring $\varepsilon_{0}$. If we plug it in we get
$$\mathbf{f}=\varepsilon_{0}(\nabla\cdot\mathbf{E})\mathbf{E}+ \frac{1}{\mu_{0}}(\nabla\times\mathbf{B})\times \mathbf{B}-\varepsilon_{0}\frac{ \partial  }{ \partial t } (\mathbf{E}\times \mathbf{B})-\varepsilon_{0}\mathbf{E}\times(\nabla\times\mathbf{E})$$
Using the anticommutative property of the [[vector product]], we can write $(\nabla\times\mathbf{B})\times \mathbf{B}=-\mathbf{B}\times(\nabla\times\mathbf{B})$, so that the magnetic term is symmetrical to the electric one (the last one). Moreover, for the sake of symmetry, we can make the term $\frac{1}{\mu_{0}}(\nabla\cdot\mathbf{B})\mathbf{B}$ appear out of nowhere since $\nabla\cdot\mathbf{B}=0$ anyway. We get
$$\begin{align}
\mathbf{f}&=\varepsilon_{0}(\nabla\cdot\mathbf{E})\mathbf{E}-\varepsilon_{0}\mathbf{E}\times(\nabla\times\mathbf{E}) \\
&+ \frac{1}{\mu_{0}}(\nabla\cdot\mathbf{B})\mathbf{B}- \frac{1}{\mu_{0}}\mathbf{B}\times(\nabla\times\mathbf{B}) \\
&-\varepsilon_{0}\frac{ \partial  }{ \partial t } (\mathbf{E}\times \mathbf{B})
\end{align}$$
The [[gradient]] of a [[Scalar product|scalar product]] is
$$\nabla(\mathbf{V}\cdot \mathbf{W})=\mathbf{V}\times(\nabla\times\mathbf{W})+\mathbf{W}\times(\nabla\times\mathbf{V})+(\mathbf{V}\cdot \nabla)\mathbf{W}+(\mathbf{W}\cdot \nabla)\mathbf{V}$$
If $\mathbf{V}=\mathbf{W}=\mathbf{E}$ we find
$$\nabla(E^{2})=2\mathbf{E}\times(\nabla\times\mathbf{E})+2(\mathbf{E}\cdot \nabla)\mathbf{E}$$
and so
$$\mathbf{E}\times(\nabla\times\mathbf{E})=\frac{1}{2}\nabla(E^{2})-(\mathbf{E}\cdot \nabla)\mathbf{E}$$
Similarly, if $\mathbf{V}=\mathbf{W}=\mathbf{B}$ we get the same result:
$$\mathbf{B}\times(\nabla\times\mathbf{B})=\frac{1}{2}\nabla(B^{2})-(\mathbf{B}\cdot \nabla)\mathbf{B}$$
With this and the definition of the [[Poynting vector]] $\mathbf{S}$, we now have pretty much everything to rewrite the force density in three major terms:
$$\begin{align}
\mathbf{f}&=\varepsilon_{0}\left[ (\nabla\cdot\mathbf{E})\mathbf{E}+(\mathbf{E}\cdot \nabla)\mathbf{E}- \frac{1}{2}\nabla(E^{2}) \right] \\
&+\frac{1}{\mu_{0}}\left[(\nabla\cdot\mathbf{B})\mathbf{B}+(\mathbf{B}\cdot \nabla)\mathbf{B} -\frac{1}{2}\nabla(B^{2}) \right] \\
&-\varepsilon_{0}\mu_{0}\frac{ \partial \mathbf{S} }{ \partial t } 
\end{align}\tag{1}$$
As foreshadowed, this is a very lengthy equation, with seven total terms. That said, as we had hoped, we can very easily spot a symmetry between the electric and magnetic fields: in fact, if it weren't for the constants $\varepsilon_{0}$ and $1/\mu_{0}$, the terms would be identical, just with $\mathbf{E}$ changed to $\mathbf{B}$. Physically speaking, this is not random chance, and mathematically, we can use this fact to express the equation in a much simpler form. To do so, we introduce the **Maxwell stress tensor** $\mathrm{T}$, defined by its elements
$$\boxed{T_{ij}=\varepsilon_{0}\left( E_{i}E_{j}- \frac{1}{2}\delta_{ij}E^{2} \right)+ \frac{1}{\mu_{0}}\left( B_{i}B_{j}- \frac{1}{2}\delta_{ij}B^{2} \right)}$$
where $\delta_{ij}$ is the [[Kronecker delta]].
#### Divergence
As it stands, it is unclear how $T_{ij}$ can help us in simplifying anything, much less $\mathbf{f}$. The reason why it is useful is hidden behind the [[divergence]] of $\mathrm{T}$ as a whole. The divergence is usually only defined on [[Vector space|vectors]], but can be specified more broadly over tensors as an operation that reduces the order of the tensor by one. Since vectors are first-order tensors, their divergence is a zeroth-order tensor, i.e. a [[scalar]]. The divergence of a second-order tensor like $\mathrm{T}$ therefore must be a first-order tensor, i.e. a vector.

Unfortunately, tensors are very complicated objects and calculating their divergence is everything but straightforward. What we can do is calculate the divergence for each axis $j$. In this context, the divergence over the $j$-th axis is given by $(\nabla\cdot \mathrm{T})_{j}=\sum_{i=1}^{3}\partial_{i}T_{ij}$, which means[^1]
$$(\nabla\cdot \mathrm{T})_{j}=\sum_{i=1}^{3} \partial_{i}\left[ \varepsilon_{0}\left( E_{i}E_{j}- \frac{1}{2}\delta_{ij}E^{2} \right) + \frac{1}{\mu_{0}}\left( B_{i}B_{j}- \frac{1}{2}\delta_{ij}B^{2} \right)\right]$$
The electric and magnetic components behave identically, so we'll just cover the electric part here. The first term yields
$$\begin{align}
\sum_{i=1}^{3} \partial_{i}(E_{i}E_{j})&=\sum_{i=1}^{3} [(\partial_{i}E_{i})E_{j}+E_{i}(\partial_{i}E_{j})] \\
&=\left( \sum_{i=1}^{3} \partial_{i}E_{i} \right)E_{j}+\left( \sum_{i=1}^{3} E_{i}\partial_{i} \right)E_{j} \\
&=(\nabla\cdot \mathbf{E})E_{j}+(\mathbf{E}\cdot \nabla)E_{j}
\end{align}$$
Recalling that $E^{2}=E^{2}_{x}+E^{2}_{y}+E^{2}_{z}=\sum_{i=1}^{3}E^{2}_{i}$, the second term goes like
$$\sum_{i=1}^{3} \partial_{i}\left( - \frac{1}{2}\delta_{ij}E^{2} \right)=- \frac{1}{2} \partial_{j}E^{2}$$
The usage of the partial derivative symbols $\partial_{i}$ works well so long we are in [[Cartesian coordinates]] (since we use the definition of divergence in those coordinates), but in other systems ([[Polar coordinates|polar]], [[Cylindrical coordinates|cylindrical]], etc.), we can't rely on them since axes can move. To generalize the result to curvilinear coordinates, it is common to use the nabla symbol $\nabla _i$ instead[^2]. In Cartesian coordinates, $\nabla_{i}=\partial_{i}$, but this not true elsewhere. Still, the result we got is correct either way.

Knowing this, the divergence finally is
$$\begin{align}
(\nabla\cdot \mathrm{T})_{j}&=\varepsilon_{0}\left[ (\nabla\cdot \mathbf{E})E_{j}+(\mathbf{E}\cdot \nabla)E_{j}- \frac{1}{2}\nabla_{j}E^{2} \right] \\
&+ \frac{1}{\mu_{0}}\left[ (\nabla\cdot \mathbf{B})B_{j}+(\mathbf{B}\cdot \nabla)B_{j}- \frac{1}{2}\nabla_{j}B^{2} \right]
\end{align}$$
Quite conveniently then, if we combine the three $j$ components into a vector $\nabla\cdot \mathrm{T}$ we get precisely the first two lines of $(1)$. Armed with this knowledge, we can state the Lorentz force by area is
$$\boxed{\mathbf{f}=\nabla\cdot \mathrm{T}-\varepsilon_{0} \mu_{0} \frac{ \partial \mathbf{S} }{ \partial t } }$$
Integration over a volume and usage of the [[divergence theorem]] gives us the force itself:
$$\boxed{\mathbf{F}=\oint_{\mathcal{S}}\mathrm{T}\cdot d\mathbf{a}-\varepsilon_{0}\mu_{0}\frac{d}{dt} \int_{\mathcal{V}}\mathbf{S}\ d\tau}$$
If we are in static conditions, the time derivative cancels and we are left with
$$\mathbf{F}=\oint_{\mathcal{S}}\mathrm{T}\cdot d\mathbf{a}$$
### Examples
The stress tensor is primarily used to determine forces acting on charges.

> [!example] Equal charges between plane
> The easiest case is, as always, two point charges. Of course, this would be easier to solve using [[Interazione elettromagnetica|Coulomb's law]] directly, but for the sake of example, we'll solve it using the stress tensor also. Consider two electric charges $q$ on the $z$ axis at an equal distance $2a$ from the origin. Find the Maxwell stress tensor and integrate over it to find the force of one charge over another.
>
>![[Exercise Maxwell stress tensor equal charges]]
> 
> We can start from [[Newton's laws|Newton's second law]]:
> $$\frac{d\mathbf{p}}{dt}=\mathbf{F}=\oint_{S} T\cdot d\mathbf{a}-\cancel{ \mu_{0}\varepsilon_{0} \frac{d}{dt} \int _{V}\mathbf{S}\ d\tau }$$
> The second term vanishes because the Poynting vector is constant. There is no magnetic field, so the stress tensor is just $(1)$ without the magnetic term
> $$T_{ij}=\varepsilon_{0}\left( E_{i}E_{j}- \frac{1}{2}\delta_{ij}E^{2} \right)$$
> We can also understand from the configuration of the charges that the force between the two is on the $z$ axis, so we only need to find the $z$ component:
> $$F_{z}=\oint _{S}(T\cdot d\mathbf{a})_{z}=\oint_{S}T_{iz}da_{i}$$
> written in both standard notation and Einstein notation. This scalar product is
> $$(T\cdot d\mathbf{a})_{z}=T_{iz}da_{i}=(T_{xz}da_{x}+T_{yz}da_{y}+T_{zz}da_{z})=T_{zz}da_{z}=\varepsilon_{0}\left( E_{z}^{2}- \frac{1}{2}E^{2} \right)(-rdrd\varphi)$$
> where we recognized that all terms off the $z$ axis vanish when evaluating on the $xy$ plane and then wrote $da$ in [[polar coordinates]]. We now need the electric field, specifically over $xy$. We can find using usual trigonometry:
> $$\mathbf{E}=\frac{q}{4\pi \varepsilon_{0}} \frac{1}{\mathfrak{r}^{2}}2\cos \theta\ \hat{\boldsymbol{\mathfrak{r}}}$$
> where $\theta$ is the angle between $\hat{\boldsymbol{\mathfrak{r}}}$ and the plane. Since $\cos \theta=r/\mathfrak{r}$ and $\mathfrak{r}=\sqrt{ r^{2}+a^{2}}$ we get
> $$\lvert \mathbf{E} \rvert=E =\frac{q}{4\pi \varepsilon_{0}} \frac{1}{\mathfrak{r}^{2}}2 \frac{r}{\mathfrak{r}}=\frac{q}{2\pi \varepsilon_{0}} \frac{r}{\mathfrak{r}^{3}}=\frac{q}{2\pi \varepsilon_{0}} \frac{r}{(r^{2}+a^{2})^{3/2}}$$
> Also note that $E_{z}=0$ for any point on the $xy$ plane since the above and below charges cancel out $z$ components exactly. With this, we just need to solve the integral:
> $$\begin{align}
> F_{z}&=-\oint_{S} \frac{\varepsilon_{0}}{2}E^{2}rdrd\varphi \\
> &=-\frac{\varepsilon_{0}}{2} \left( \frac{q}{2\pi \varepsilon_{0}} \right)^{2}2\pi \int_{0}^{\infty} \frac{r^{3}}{(r^{2}+a^{2})^{3}}dr \\
> (r^{2}= u)&=\frac{q^{2}}{8\pi \varepsilon_{0}}\int_{0}^{\infty} \frac{u}{(u+a^{2})^{3}}du \\
> &=\frac{q^{2}}{8\pi \varepsilon_{0}}\left[ - \frac{1}{u+a^{2}}+ \frac{a^{2}}{2(u+a^{2})^{3}} \right]_{0}^{\infty} \\
> &=\frac{q^{2}}{8\pi \varepsilon_{0}}\left[ 0+ \frac{1}{a^{2}}- \frac{a^{2}}{2a^{4}} \right] \\
> &=\frac{q^{2}}{4\pi \varepsilon_{0}} \frac{1}{(2a)^{2}}
> \end{align}$$
> (We could have avoided using a known integral by substituting $u+a^{2}=v$ and solving that instead.)
> 
> If the charges are opposite, $q$ and $-q$, the fields don't cancel on the plane; they double, and do so specifically on the $z$ axis, oriented towards the negative side of the plane. For the same reason, the field on the plane is now *exclusively* on the $z$ axis, which means $E^{2}=E_{z}^{2}$ and so $E^{2}- \frac{1}{2}E_{z}^{2}=\frac{1}{2}E_{z}^{2}$. We now solve
> $$\begin{align}
> F_{z}&=\frac{\varepsilon_{0}}{2} \left( \frac{qa}{2\pi \varepsilon_{0}} \right)^{2}2\pi \int_{0}^{\infty} \frac{r}{(r^{2}+a^{2})^{3}}dr \\
> &=- \frac{q^{2}a^{2}}{4\pi \varepsilon_{0}}\left[ - \frac{1}{4} \frac{1}{(r^{2}+a^{2})}^{2} \right]_{0}^{\infty} \\
> &=- \frac{q^{2}a^{2}}{4\pi \varepsilon_{0}}\left[ 0+ \frac{1}{4a^{4}} \right] \\
> &=- \frac{q^{2}}{4\pi \varepsilon_{0}} \frac{1}{(2a)^{2}}
> \end{align}$$

[^1]: A couple of notes. Firstly, we are using the definition of divergence in Cartesian coordinates because it's easier and equivalent to other coordinates. Secondly, this is not using Einstein notation. If it did, the sum $\sum_{i=1}^{3}$ would be implicit, relying on the fact that the index $i$ appears on both $\nabla_{i}$ and the terms inside the square brackets.

[^2]: Actually, this also sets up the formula to be used in the **covariant formulation of electromagnetism**, a more advanced way of writing the Maxwell equations that also works in special and general relativity with curved [[Spacetime|spacetime]]. This is because $\nabla_{i}$ represent the more complicated [[covariant derivative|covariant derivatives]] in those contexts. Of course, none of this is significant outside of relativity, where $\nabla_{i}=\partial_{i}$.
