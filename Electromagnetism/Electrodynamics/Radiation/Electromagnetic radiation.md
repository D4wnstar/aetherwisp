---
wiki-publish: true
aliases:
  - electromagnetic spectrum
---
**Electromagnetic radiation** is [[radiation]] of [[electromagnetic wave|electromagnetic waves]]. It occurs when [[Electric charge|charged particles]] accelerate, which causes them to emit [[energy]] that is carried off to infinity through electromagnetic waves[^1].

Electromagnetic waves can be of any [[frequency]]. Since this leads to a massive (infinite, actually) range of possible waves, called the **electromagnetic spectrum**, they are conventionally categorized in seven "types", from most to least energetic:
1. Gamma rays
2. X-rays
3. Ultraviolet light
4. Visible light
5. Infrared light
6. Microwaves
7. Radio waves
### Sources
Consider a localized source near the origin. To determine the energy radiated from the source at some time $t_{0}$, we encase the source in a sphere of very large radius $r$, large enough that the source looks like a point at the center of the sphere. The [[radiant power]] passing through the surface is given, according to [[Poynting's theorem]], by integrating the [[Poynting vector]] over the surface
$$P(r,t)=\oint_{\mathcal{S}} \mathbf{S}\cdot d\mathbf{a}=\frac{1}{\mu_{0}}\oint_{\mathcal{S}}(\mathbf{E}\times \mathbf{B})\cdot d\mathbf{a}$$
since the electromagnetic energy density does not change in time. Since electromagnetic waves travel at the [[speed of light]], thus causing the fields $\mathbf{E}$ and $\mathbf{B}$ to depend not on current time but on [[retarded time]], the energy that we feel now at the surface was emitted by the source in the past, at the retarded time $t_{0}=t-r/c$. The power radiated is then
$$P_\text{rad}(t_{0})=\lim_{ r \to \infty } P\left( r,t_{0}+ \frac{r}{c} \right)$$
where $t_{0}$ is held constant. This is the power that is radiated from the source in a spherical fashion up to infinity. This transfer is irreversible: radiation is emitted and never comes back.

The area of the sphere goes like $\sim r^{2}$, so for the power not to vanish at $r\to \infty$, the Poynting vector must decrease *at most* like $\sim r^{-2}$. Any faster and it dilutes to zero at infinity when spread over a spherical surface. Since $\mathbf{S}\propto \mathbf{E}\times \mathbf{B}$, this is like saying the the product of $E$ and $B$ must decrease at most like $\sim r^{-2}$.

Let's see what happens with static fields: [[Electric field|Coulomb's law]] says that electrostatic fields go like $\sim r^{-2}$ and the [[Biot-Savart law]] says the same for magnetostatic fields. Their product, then, is $\sim r^{-4}$; way too fast for what we need. Clearly then, it is *impossible* for a static configuration to radiate: it just cuts out too fast.

When we add in a *time-dependent* source, it's [[Jefimenko's equations]] that tell us the fields. These include our previous static terms, but also include terms that go like $\sim r^{-1}$. Multiply them together and you get something that satisfies our condition of not decreasing faster than $\sim r^{-2}$. It is these terms alone that are responsible for all electromagnetic radiation; everything else is not and can be safely ignored.

A discussion on the physics of radiation from an arbitrary source can be found below. That said, starting from the general case is probably not a good idea; [[Electric dipole#Radiation]] and [[Magnetic dipole#Radiation]] are probably a better choice.
### Radiation from an arbitrary source
In an ideal world, we'd be able to determine the exact radiation at any point from any source analytically. This is a bit of a dream scenario and in practice it's not at all possible to solve for most source distributions. That said, not all hope is lost. While we can't solve *everything*, we can do some truly general considerations.

To start, let's consider some generic charge distribution of any shape whatsoever, with our only prerequisite being that it's a finite volume near the origin.

![[Diagram Electromagnetic radiation from arbitrary source|50%]]

The retarded [[electric potential|scalar potential]] is
$$V(\mathbf{r},t)=\frac{1}{4\pi \varepsilon_{0}}\int \frac{\rho(\mathbf{r}',t- \mathfrak{r}/c)}{\mathfrak{r}}d\tau' $$
where $\mathfrak{r}=\sqrt{ r^{2}+r'^{2}-2\mathbf{r}\cdot \mathbf{r}' }$. As in most situations, we care about radiation far from the source, in the **radiation zone**. Here, we can do approximation 1: $r\gg r'$, where we mean that $r'$ is always small compared to $r$ throughout integration. This is the mathematical statement of "the source object is really small compared to how far we are from it". In this approximation we get
$$\mathfrak{r}\simeq r\left( 1- \frac{\mathbf{r}\cdot\mathbf{r}'}{r^{2}} \right)$$
from which using the first order [[Taylor series|Taylor series]] $(1-x)^{-1}\simeq1+x$ when $\lvert x \rvert\ll1$:
$$\frac{1}{\mathfrak{r}}\simeq \frac{1}{r}\left( 1+ \frac{\mathbf{r}\cdot\mathbf{r}'}{r^{2}} \right)$$
and so
$$\rho\left( \mathbf{r}',t- \frac{\mathfrak{r}}{c} \right)\simeq \rho\left( \mathbf{r}',t- \frac{r}{c}+ \frac{\hat{\mathbf{r}}\cdot\mathbf{r}'}{c} \right)$$
Another Taylor series, this time of $t$ in about the [[Retarded time]] at the origin
$$t_{0}\equiv t- \frac{r}{c}$$
yields
$$\rho\left( \mathbf{r}',t- \frac{\mathfrak{r}}{c} \right)\simeq \rho(\mathbf{r}',t_{0})+\dot{\rho}(\mathbf{r}',t_{0})\left( \frac{\hat{\mathbf{r}}\cdot\mathbf{r}'}{c} \right)+\ldots$$
We can afford to truncate at the first order if we accept approximation 2:
$$r'\ll \frac{c}{\lvert \ddot{\rho}/\dot{\rho} \rvert },\ldots$$
and other further terms.

[^1]: Radiation as expressed here makes sense only in the context a localized source, that is, a source of finite extent, since the idea of "energy carried off to infinity" no longer makes sense when the source itself extends to infinity. Such shapes of course do not exist in the real world, but are common in simplified formulations of phenomena, such as infinite wires, infinite planes, etc.
