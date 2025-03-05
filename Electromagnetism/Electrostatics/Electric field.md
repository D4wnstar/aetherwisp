The **electric field** $\mathbf{E}$ is the [[conservative force|conservative]] [[Campo vettoriale|vector field]] that describes the action of an [[electric charge]] onto other charges. For a test charge $Q$, the force applied to it by another charged object is determined through the electric field as
$$\mathbf{F}=Q\mathbf{E}$$
 Electric fields obey the [[superposition principle]]. If there are two charges producing fields $\mathbf{E}_{1}$ and $\mathbf{E}_{2}$, their combined field is simply $\mathbf{E}=\mathbf{E}_{1}+\mathbf{E}_{2}$.

If the charges are allowed to move, as in materials, the electric field of the [[Physical system|system]] can become quite complicated. This is because electric fields change the distribution of charges around them by moving them around, and this change tends to render systems that are normally neutral no longer neutral, which in turn makes them produce an electric field of their own. The original field is called the **source** or **stimulus field** and the one generated as consequence is called the **response field**. It is also possible in some particular structures (like semiconductors) for there to be a permanent electric field due to the conformation of the material (kind of like how permanent magnets have a permanent [[magnetic field]]). These are generally known as **built-in fields** and also play a role[^1]. In the most general case, using the superposition principle, an electric field is a linear combination of all three of these:
$$\mathbf{E}_\text{total}=\mathbf{E}_\text{source}+\mathbf{E}_\text{response}+\mathbf{E}_\text{built-in}$$
If dealing with response fields, it is typically easiest to work with [[electric displacement]]. If dealing specifically with [[Dielectric|dielectrics]], this amounts to using [[dielectric polarization]].
### Point charges
Given a system of source point charges $q_{1}$, $q_{2}$, ..., the electric field is the quantity
$$\mathbf{E}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\sum\limits_{i=1}^{n} \frac{q_{i}}{\mathfrak{r}_{i}^{2}}\hat{\mathfrak{r}}_{i}\quad \left[\frac{\text{N}}{\text{C}}\right]$$
where $\epsilon_{0}$ is the [[Costante dielettrica del vuoto|permittivity of free space]] and $\mathfrak{r}_{i}=|\mathbf{r}-\mathbf{r}'|$ is the distance between the $i$-th source charge (at position $\mathbf{r}'$) and the test charge (at position $\mathbf{r}$). $\hat{\mathfrak{r}}$ is the unit vector that points from that charge to the test charge.
### Continuous charges
For continues charges, the field is derived by integration as
$$\mathbf{E}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\int \frac{1}{\mathfrak{r}^{2}}\hat{\mathfrak{r}}\ dq$$
where the domain of integration is the charge distribution in space. This is expressed in one, two and three dimensions as [[Integrale su una curva|line integrals]], [[Integrale su una superficie|surface integrals]] and volume integrals. 

For a linear charge distribution $dq=\lambda dt'$, with $\lambda$ the linear charge density and $dt'$ the line element onto the charge [[curva|curve]] $\gamma$, we have
$$\mathbf{E}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\int_{\gamma} \frac{\lambda(\mathbf{r}')}{\mathfrak{r}^{2}}\hat{\mathfrak{r}}\ dt'$$
For a surface charge distribution $dq=\sigma da'$ with $\sigma$ the surface charge density and $da'$ the area element onto the [[Superficie|surface]] $\Phi$, we have
$$\mathbf{E}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\int_{\Phi}\frac{\sigma(\mathbf{r}')}{\mathfrak{r}^{2}}\hat{\mathfrak{r}}\ da'$$
For a volume charge distribution $dq=\rho d\tau'$ with $\rho$ the volume charge density and $d\tau'$ the area element onto the volume $V$, we have
$$\mathbf{E}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\int_{V}\frac{\rho(\mathbf{r}')}{\mathfrak{r}^{2}}\hat{\mathfrak{r}}\ d\tau'$$
In all of the above, $\mathfrak{r}$ is the distance between the test charge and the charge object element.
### Divergence
We can calculate the [[divergence]] of the electric field starting from the volume charge. The volume $V$ may be extended to cover all space as $\rho$ is zero outside the charged object anyway, so it makes no difference. The divergence then is
$$\nabla\cdot\mathbf{E}=\frac{1}{4\pi\varepsilon_{0}}\int\nabla\cdot\left(\frac{\hat{\mathfrak{r}}}{\mathfrak{r}^{2}}\right)\rho(\mathbf{r}')\ d\tau'$$
(the divergence "targets" $\mathbf{r}$, so $\mathfrak{r}$ is part of the calculation, but $\rho$ is not). We therefore need to find the divergence of $\hat{r}/r^{2}$.
#### Divergence of $\hat{r}/r^{2}$
The divergence of $\hat{r}/r^{2}$ explodes in 0, so the divergence cannot be calculated directly without making a mistake. The flux of $\hat{r}/r^{2}$ is $4\pi$ for any surface $S$:
$$\oint_{S} \frac{\hat{r}}{r^{2}}\cdot d\mathbf{a}=\int_{S}\left(\frac{1}{R^{2}}\hat{r}\right)\cdot(R^{2}\sin\theta d\theta d\phi\hat{r})=\left(\int_{0}^{\pi}\sin\theta d\theta\right)\left(\int_{0}^{2\pi}d\phi\right) =4\pi$$
but the divergence itself is *zero*:
$$\nabla\cdot \left(\frac{\hat{r}}{r^{2}}\right)=\frac{1}{r^{2}}\frac{\partial }{\partial r}\left(r^{2} \frac{1}{r^{2}}\right)=0$$
If we apply the [[Teorema della divergenza|divergence theorem]], we get
$$\int_{V}\nabla\cdot\left(\frac{\hat{r}}{r^{2}}\right)=\oint_{S} \frac{\hat{r}}{r^{2}}\cdot d\mathbf{a}=4\pi$$
which seems paradoxical. How can the integral of something we calculate as zero be $4\pi$? The only way this can be true is if the divergence contains the (three-dimensional) [[delta di dirac|Dirac delta]] [[Distribuzione|distribution]], as its integral over all space is one. Thus
$$\nabla\cdot\left(\frac{\hat{r}}{r^{2}}\right)=4\pi\delta^{3}(\mathbf{r})$$
and since
$$\iiint \delta^{3}(\mathbf{r})\ d\mathbf{r}=1$$
this makes the previous statements not paradoxical.
#### Divergence of the electric field
Knowing this, we can go back to the electric field. We then get
$$\boxed{\nabla\cdot\mathbf{E}=\frac{1}{4\pi\varepsilon_{0}}\int4\pi\delta^{3}(\mathfrak{r})\rho(\mathbf{r}')d\tau'=\frac{1}{\varepsilon_{0}}\rho(\mathbf{r})}$$
which is just [[Gauss' law]] in differential form, here calculated explicitly.
### Curl
The [[curl]] is easier to derive than the divergence. Consider the electric field of a point charge
$$\mathbf{E}=\frac{1}{4\pi\varepsilon_{0}} \frac{q}{r^{2}}\hat{\mathbf{r}}$$
Let's calculate the line integral of this from point $\mathbf{a}$ to point $\mathbf{b}$:
$$\int_{\mathbf{a}}^{\mathbf{b}} \mathbf{E}\cdot d\mathbf{r}$$
In [[Spherical coordinates]] we have $d\mathbf{r}=dr\hat{\mathbf{r}}+rd\theta\hat{\mathbf{\theta}}+r\sin\phi d\phi\hat{\mathbf{\phi}}$, so
$$\mathbf{E}\cdot d\mathbf{r}=\frac{1}{4\pi\varepsilon_{0}} \frac{q}{r^{2}}dr$$
therefore
$$\int_{\mathbf{a}}^{\mathbf{b}}\mathbf{E}\cdot d\mathbf{r}=\frac{1}{4\pi\varepsilon_{0}}\int_{\mathbf{a}}^{\mathbf{b}} \frac{q}{r^{2}}dr=\frac{1}{4\pi\varepsilon_{0}}\left(\frac{q}{r_{a}}- \frac{q}{r_{b}}\right)$$
For a closed integral we have $r_{a}=r_{b}$, so
$$\oint \mathbf{E}\cdot d\mathbf{r}=0$$
and using the [[Teorema del rotore|curl theorem]] we find
$$\boxed{\nabla\times \mathbf{E}=0}$$
So the electric field of a point charge is irrotational, which means, among other things, that the force caused by it is conservative. In fact, due to the superposition principle, this holds for *any* distribution of charge, be it discrete or continuous.
### Notable cases
> [!example] Wire
> Consider a wire with uniform linear charge density $\lambda$ running on the $x$ axis and a test charge on the $z$ axis at distance $z$. The wire is symmetrical around the origin and has a length of $2L$, on $x\in[-L,L]$. The electric field applied on the test charge by the wire is entirely on the $z$ axis and is
> $$\mathbf{E}=\frac{1}{4\pi\varepsilon_{0}} \frac{2\lambda L}{z\sqrt{z^{2}+ L^{2}}}\hat{\mathbf{z}}$$
> If the wire is only on one side of the origin, on $x\in[0,L]$, then the field is
> $$\mathbf{E}=\frac{1}{4\pi\varepsilon_{0}} \frac{\lambda}{z}\left[\left(-1 + \frac{z}{\sqrt{z^{2}+L^{2}}}\right)\hat{\mathbf{x}}+\frac{L}{\sqrt{z^{2}+L^{2}}}\hat{\mathbf{z}}\right]$$

> [!example] Square loop
> Consider a test charge on the $z$ axis at distance $z$ over a wire with uniform linear charge density $\lambda$ in a square loop around the origin. The edge of the loop has a length of $a$. The field applied onto the charge is
> $$\mathbf{E}=\frac{1}{4\pi\varepsilon_{0}} \frac{4\lambda az}{(z^{2}+ \frac{a^{2}}{4})\sqrt{z^{2}+ \frac{a^{2}}{2}}}\hat{\mathbf{z}}$$

> [!example] Circular loop
> Same as the square loop, but the loop is circular and has a radius of $R$. The field is
> $$\mathbf{E}=\frac{1}{2\varepsilon_{0}} \frac{\lambda rz}{(r^{2}+z^{2})^{3/2}}\hat{\mathbf{z}}$$

> [!example] Circular disk
> Same as the circular loop, but it's a disk with uniform surface charge density $\sigma$. The field is
> $$\mathbf{E}=\frac{\sigma}{2\varepsilon_{0}}\left(1- \frac{z}{\sqrt{R^{2}+z^{2}}}\right)\hat{\mathbf{z}}$$

> [!example] Infinite plane
> The infinite plane is a special case of the circular disk where the radius goes to infinity, $R \rightarrow \infty$. In this case, the second term vanishes and we get
> $$\mathbf{E}=\frac{\sigma}{2\varepsilon_{0}}\hat{\mathbf{z}}$$

 > [!example] Spherical surface
> Consider a empty sphere of radius $R$ with a uniform surface charge density $\sigma$ and a test charge at distance $r$ in any direction. If the test charge is outside of the sphere, so $r>R$, the field is
> $$\mathbf{E}=\frac{1}{4\pi\varepsilon_{0}} \frac{Q}{r^{2}}\hat{\mathbf{r}} \qquad \text{if }r>R$$
> where $Q$ is the total charge on the surface, $Q=4\pi R^{2}\sigma$. This shows that a charge sphere acts identically to a point charge for test charges outside of it.
> 
> If the test charge is inside, so $r<R$, the field is null:
> $$\mathbf{E}=0 \qquad \text{if }r<R$$

> [!example] Ball
> Consider a ball of radius $R$ with uniform volume charge density $\rho$ and a test charge at distance $r$ in any direction. The field on the test charge is
> $$\mathbf{E}=\frac{1}{4\pi\varepsilon_{0}} \frac{Q_{int}}{r^{2}}\hat{\mathbf{r}}$$
> where $Q_{int}$ is the total charge contained within the spherical surface of radius $r$ that the test charge sits on. If the test charge is outside of the ball, so $r>R$, this is the total charge of the ball and $Q_{int}=Q=\frac{4}{3}\pi R^{3}\rho$. Just like a sphere, a ball acts as a point charge for test charges outside of it.
>
> If the charge is inside the ball, so $r<R$, it's the ratio between the interior volume and total volume, so
> $$Q_{int}=\frac{\frac{4}{3}\pi r^{3}}{\frac{4}{3}\pi R^{3}}Q=\frac{r^{3}}{R^{3}}Q$$
> and the field becomes
> $$\mathbf{E}=\frac{1}{4\pi\varepsilon_{0}} \frac{r}{R^{3}}Q\hat{\mathbf{r}}$$
### Discontinuities
Since one- and two-dimensional objects do not actually exist in our three-dimensional world, their usage with the electric field can cause some issues. Namely, it's the cause behind the discontinuity that the field experiences when, say, it passes through a charged surface. To find the actual discontinuity, we can just use Gauss' law on a arbitrarily thin pillbox shape
$$\oint_{S}\mathbf{E}\cdot d\mathbf{a}=\frac{1}{\varepsilon_{0}}\sigma A$$
The sides contribute nothing to the field, as they are parallel to the outgoing field when in close proximity to the surface (hence why we need a thin enough pillbox). Thus, we only have the fields passing through the top and bottom of the box:
$$E_{\text{above}}^{\perp}-E_{\text{below}}^{\perp}=\frac{1}{\varepsilon_{0}}\sigma$$
where the two components denote the perpendicular component of the outgoing field from the surface above and below it. This is also the discontinuity for the field for any surface, not just a plane. This also only applies for surface charges, as there is no such discontinuity when passing through the surface of a charged solid, such as a ball.

On the contrary, the parallel component of $\mathbf{E}$ is always continuous. This is because the electric field is irrotational. In fact, since the curl is zero, the integral on a closed loop is also always zero:
$$\oint \mathbf{E}\cdot d\mathbf{r}=0$$
If we pick the loop to be on an edge of the pillbox that passes through the surface, the edges going through add nothing (as they are arbitrarily small) and the edges parallel to the surface give $(\mathbf{E}_\text{above}^{\parallel}-\mathbf{E}_\text{below}^{\parallel})l$, where $l$ is the length of the pillbox. In other words,
$$\mathbf{E}_\text{above}^{\parallel}=\mathbf{E}_\text{below}^{\parallel}$$
which shows that there is no difference between parallel fields when going through the surface.

We can combine these two formulas into a single vector one as
$$\boxed{\mathbf{E}_\text{above}-\mathbf{E}_\text{below}=\frac{\sigma}{\varepsilon_{0}}\hat{\mathbf{n}}}$$
where $\hat{\mathbf{n}}$ is the normal vector from the surface. Notably, for a charge that is *on* the surface, that is, on the discontinuity itself, the force per unit area $\mathbf{f}=\sigma \mathbf{E}$ applied onto seems at first undefined. After all, if the electric field is discontinuous, the force caused by it must act weird. Turns out, the correct field to use is the average between the field above and below:
$$\mathbf{f}=\frac{1}{2}\sigma(\mathbf{E}_\text{above}+\mathbf{E}_\text{below})$$
#### Transmission angle
The presence of a discontinuity implies that the field incident on a surface changes direction as it passes through the surface (i.e. it is transmitted).

![[Schema Electric field transmission|90%]]

When an electric field passes through the surface, the component parallel to the surface is conserved. We can use this to connect the incidence angle $\alpha_{\text{ext}}$ and the transmission angle $\alpha_{\text{int}}$. We can express the parallel components in terms of the cosines of these two angles:
$$E_\text{ext}\cos \alpha _\text{ext}=E_\text{int}\cos \alpha _\text{int}$$
Since we're working in materials, we can employ the [[electric displacement]] $\mathbf{D}$, which instead conserves the perpendicular component to the surface, which means the sines:
$$D_\text{ext}\sin \alpha _\text{ext}=D_\text{int}\sin \alpha _\text{int}$$
We can divide the second equation by the first:
$$\frac{D_\text{ext}}{E_\text{ext}}\tan \alpha _\text{ext}=\frac{D_\text{int}}{E_\text{int}}\tan \alpha _\text{int}$$
This is a general relation that applies for most dielectrics[^2]. If we specifically say that we are working with linear and homogeneous dielectrics, we can claim that $\mathbf{D}=\varepsilon_{0}\varepsilon_{r}\mathbf{E}$, using the [[permittivity]] of the materials. If we make the substitution we find
$$\boxed{\varepsilon_{r,\text{ext}}\tan \alpha _\text{ext}=\varepsilon_{r,\text{int}}\tan \alpha _\text{int}}$$
In general, the bigger the difference between permittivities, the larger the difference in angle will be. If the internal permittivity is higher than the external one, the field will tend to align flush to the surface.

Given the relative permittivities of the materials and one of the two angles, we can find the other. We can also measure the angles themselves to figure out the dielectric constant of one the materials, if we know the other.

[^1]: To be more rigorous, the source, response and built-in fields are generated by their respective source, response and built-in charge distributions. Physically speaking, these come first and the fields are created by them. The source distribution is typically artificial and corresponds to the free charge distribution. The response distribution is only present in materials subject to a field and corresponds to the bound charge distribution. The built-in distribution is always present, however due to the net neutrality of [[Atomo|atoms]], it is almost always zero and therefore can be safely ignored. It is non-zero only in more niche cases, like [[ionization|ionized]] materials or semiconductors.

[^2]: This equation assumes that the fields $\mathbf{E}$ and $\mathbf{D}$ do not reverse direction when passing through the surface. In these cases, more care should be taken to keep the signs consistent.