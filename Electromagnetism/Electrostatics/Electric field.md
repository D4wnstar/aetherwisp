The **electric field** $\mathbf{E}$ is the [[Campo vettoriale|vector field]] that describes the action of an [[electric charge]] onto other charges. For a test charge $Q$, the force applied to it by another charged object is determined through the electric field as
$$\mathbf{F}=Q\mathbf{E}$$
### Point charges
Given a system of source point charges $q_{1}$, $q_{2}$, ..., the electric field is the quantity
$$\mathbf{E}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\sum\limits_{i=1}^{n} \frac{q_{i}}{\mathscr{r}_{i}^{2}}\hat{\mathscr{r}}_{i}\quad \left[\frac{\text{N}}{\text{C}}\right]$$
where $\epsilon_{0}$ is the [[Costante dielettrica del vuoto|permittivity of free space]] and $\mathscr{r}_{i}=|\mathbf{r}-\mathbf{r}'|$ is the distance between the $i$-th source charge (at position $\mathbf{r}'$) and the test charge (at position $\mathbf{r}$). $\hat{\mathscr{r}}$ is the unit vector that points from that charge to the test charge.
### Continuous charges
For continues charges, the field is derived by integration as
$$\mathbf{E}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\int \frac{1}{\mathscr{r}^{2}}\hat{\mathscr{r}}dq$$
where the domain of integration is the charge distribution in space. This is expressed in one, two and three dimensions as [[Integrale su una curva|line integrals]], [[Integrale su una superficie|surface integrals]] and volume integrals. 

For a linear charge distribution $dq=\lambda dt'$, with $\lambda$ the linear charge density and $dt'$ the line element onto the charge [[curva|curve]] $\gamma$, we have
$$\mathbf{E}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\int_{\gamma} \frac{\lambda(\mathbf{r}')}{\mathscr{r}^{2}}\hat{\mathscr{r}}dt'$$
For a surface charge distribution $dq=\sigma da'$ with $\sigma$ the surface charge density and $da'$ the area element onto the [[Superficie|surface]] $\Phi$, we have
$$\mathbf{E}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\int_{\Phi}\frac{\sigma(\mathbf{r}')}{\mathscr{r}^{2}}\hat{\mathscr{r}}da'$$
For a volume charge distribution $dq=\rho d\tau'$ with $\rho$ the volume charge density and $d\tau'$ the area element onto the volume $V$, we have
$$\mathbf{E}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\int_{V}\frac{\rho(\mathbf{r}')}{\mathscr{r}^{2}}\hat{\mathscr{r}}d\tau'$$
In all of the above, $\mathscr{r}$ is the distance between the test charge and the charge object element.
### Divergence
We can calculate the [[divergence]] of the electric field starting from the volume charge. The volume $V$ may be extended to cover all space as $\rho$ is zero outside the charged object anyway, so it makes no difference. The divergence then is
$$\nabla\cdot\mathbf{E}=\frac{1}{4\pi\varepsilon_{0}}\int\nabla\cdot\left(\frac{\hat{\mathscr{r}}}{\mathscr{r}^{2}}\right)\rho(\mathbf{r}')\ d\tau'$$
(the divergence "targets" $\mathbf{r}$, so $\mathscr{r}$ is part of the calculation, but $\rho$ is not). We therefore need to find the divergence of $\hat{r}/r^{2}$.
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
$$\nabla\cdot\mathbf{E}=\frac{1}{4\pi\varepsilon_{0}}\int4\pi\delta^{3}(\mathscr{r})\rho(\mathbf{r}')d\tau'=\frac{1}{\varepsilon_{0}}\rho(\mathbf{r})$$
which is just [[Gauss' law]] in differential form, here calculated explicitly.
### Notable cases
#### Wire under charge
Consider a wire with uniform linear charge density $\lambda$ running on the $x$ axis and a test charge on the $z$ axis at distance $z$. The wire is symmetrical around the origin and has a length of $2L$, on $x\in[-L,L]$. The electric field applied on the test charge by the wire is entirely on the $z$ axis and is
$$\mathbf{E}=\frac{1}{4\pi\varepsilon_{0}} \frac{2\lambda Lz}{z\sqrt{z^{2}+ L^{2}}}\hat{\mathbf{z}}$$
If the wire is only on one side of the origin, on $x\in[0,L]$, then the field is
$$\mathbf{E}=\frac{1}{4\pi\varepsilon_{0}} \frac{\lambda}{z}\left[\left(-1 + \frac{z}{\sqrt{z^{2}+L^{2}}}\right)\hat{\mathbf{x}}+\frac{L}{\sqrt{z^{2}+L^{2}}}\hat{\mathbf{z}}\right]$$
#### Square loop
Consider a test charge on the $z$ axis at distance $z$ over a wire with uniform linear charge density $\lambda$ in a square loop around the origin. The edge of the loop has a length of $a$. The field applied onto the charge is
$$\mathbf{E}=\frac{1}{4\pi\varepsilon_{0}} \frac{4\lambda az}{(z^{2}+ \frac{a^{2}}{4})\sqrt{z^{2}+ \frac{a^{2}}{2}}}\hat{\mathbf{z}}$$
#### Circular loop
Same as the square loop, but the loop is circular and has a radius of $R$. The field is
$$\mathbf{E}=\frac{1}{2\varepsilon_{0}} \frac{\lambda rz}{(r^{2}+z^{2})^{3/2}}\hat{\mathbf{z}}$$
#### Circular disk
Same as the circular loop, but it's a disk with uniform surface charge density $\sigma$. The field is
$$\mathbf{E}=\frac{\sigma}{2\varepsilon_{0}}\left(1- \frac{z}{\sqrt{R^{2}+z^{2}}}\right)\hat{\mathbf{z}}$$
#### Infinite plane
The infinite plane is a special case of the circular disk where the radius goes to infinity, $R \rightarrow \infty$. In this case, the second term vanishes and we get
$$\mathbf{E}=\frac{\sigma}{2\varepsilon_{0}}\hat{\mathbf{z}}$$
#### Spherical surface
Consider a empty sphere of radius $R$ with a uniform surface charge density $\sigma$ and a test charge at distance $r$ in any direction. If the test charge is outside of the sphere, so $r>R$, the field is
$$\mathbf{E}=\frac{1}{4\pi\varepsilon_{0}} \frac{Q}{r^{2}}\hat{\mathbf{r}} \qquad \text{if }r>R$$
where $Q$ is the total charge on the surface, $Q=4\pi R^{2}\sigma$. This shows that a charge sphere acts identically to a point charge for test charges outside of it.

If the test charge is inside, so $r<R$, the field is null:
$$\mathbf{E}=0 \qquad \text{if }r<R$$
#### Ball
Consider a ball of radius $R$ with uniform volume charge density $\rho$ and a test charge at distance $r$ in any direction. The field on the test charge is
$$\mathbf{E}=\frac{1}{4\pi\varepsilon_{0}} \frac{Q_{int}}{r^{2}}\hat{\mathbf{r}}$$
where $Q_{int}$ is the total charge contained within the spherical surface of radius $r$ that the test charge sits on. If the test charge is outside of the ball, so $r>R$, this is the total charge of the ball and $Q_{int}=Q=\frac{4}{3}\pi R^{3}\rho$. Just like a sphere, a ball acts as a point charge for test charges outside of it.

If the charge is inside the ball, so $r<R$, it's the ratio between the interior volume and total volume, so
$$Q_{int}=\frac{\frac{4}{3}\pi r^{3}}{\frac{4}{3}\pi R^{3}}Q=\frac{r^{3}}{R^{3}}Q$$
and the field becomes
$$\mathbf{E}=\frac{1}{4\pi\varepsilon_{0}} \frac{r}{R^{3}}Q\hat{\mathbf{r}}$$
