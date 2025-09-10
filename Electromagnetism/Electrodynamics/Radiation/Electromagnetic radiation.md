---
wiki-publish: true
aliases:
  - electromagnetic spectrum
  - light
---
**Electromagnetic radiation** is [[radiation]] of [[electromagnetic wave|electromagnetic waves]]. It occurs when [[Electric charge|charged particles]] accelerate, which causes them to emit [[energy]] that is carried off to infinity through electromagnetic waves[^1].

Electromagnetic waves can be of any [[frequency]]. Since this leads to a massive (infinite, actually) range of possible waves, called the **electromagnetic spectrum**, they are conventionally categorized in seven "types", from most to least energetic:
1. **Gamma rays**
2. **X-rays**
3. **Ultraviolet light**
4. **Visible light**, or simply just **light**
5. **Infrared light**
6. **Microwaves**
7. **Radio waves**
### Sources
Consider a localized source near the origin. To determine the energy radiated from the source at some time $t_{0}$, we encase the source in a sphere of very large radius $r$, large enough that the source looks like a point at the center of the sphere. The [[radiant power]] passing through the surface is given, according to [[Poynting's theorem]], by integrating the [[Poynting vector]] over the surface
$$P(r,t)=\oint_{\mathcal{S}} \mathbf{S}\cdot d\mathbf{a}=\frac{1}{\mu_{0}}\oint_{\mathcal{S}}(\mathbf{E}\times \mathbf{B})\cdot d\mathbf{a}$$
since the electromagnetic energy density does not change in time. Since electromagnetic waves travel at the [[speed of light]], thus causing the fields $\mathbf{E}$ and $\mathbf{B}$ to depend not on current time but on [[retarded time]], the energy that we feel now at the surface was emitted by the source in the past, at the retarded time $t_{0}=t-r/c$. The power radiated is then
$$P_\text{rad}(t_{0})=\lim_{ r \to \infty } P\left( r,t_{0}+ \frac{r}{c} \right)$$
where $t_{0}$ is held constant. This is the power that is radiated from the source in a spherical fashion up to infinity. This transfer is irreversible: radiation is emitted and never comes back.

The area of the sphere goes like $\sim r^{2}$, so for the power not to vanish at $r\to \infty$, the Poynting vector must decrease *at most* like $\sim r^{-2}$. Any faster and it dilutes to zero at infinity when spread over a spherical surface. Since $\mathbf{S}\propto \mathbf{E}\times \mathbf{B}$, this is like saying the the product of $E$ and $B$ must decrease at most like $\sim r^{-2}$.

Let's see what happens with static fields: [[Electric field|Coulomb's law]] says that electrostatic fields go like $\sim r^{-2}$ and the [[Biot-Savart law]] says the same for magnetostatic fields. Their product, then, is $\sim r^{-4}$; way too fast for what we need. Clearly then, it is *impossible* for a static configuration to radiate: it just cuts out too fast.

When we add in a *time-dependent* source, it's [[Jefimenko's equations]] that tell us the fields. These include our previous static terms, but also include terms that go like $\sim r^{-1}$. Multiply them together and you get something that satisfies our condition of not decreasing faster than $\sim r^{-2}$. It is these terms alone that are responsible for all electromagnetic radiation; everything else cuts out too fast and can be safely ignored.

A discussion on the physics of radiation from an arbitrary source can be found below. That said, starting from the general case is probably not a good idea; [[Electric dipole#Radiation]] and [[Magnetic dipole#Radiation]] are probably a better choice.
### Radiation from an arbitrary source
In an ideal world, we'd be able to determine the exact radiation at any point from any source analytically. This is a bit of a dream scenario and in practice it's not at all possible to solve for most source distributions. That said, not all hope is lost. While we can't solve *everything*, we can do some truly general considerations.

To start, let's consider some generic charge distribution of any shape whatsoever, with our only prerequisite being that it's a finite volume near the origin.

![[Diagram Electromagnetic radiation from arbitrary source|50%]]

#### Potentials
The [[Retarded potentials|retarded scalar potential]] is
$$V(\mathbf{r},t)=\frac{1}{4\pi \varepsilon_{0}}\int_{\mathcal{V}} \frac{\rho(\mathbf{r}',t- \mathfrak{r}/c)}{\mathfrak{r}}d\tau' $$
where $\mathfrak{r}=\sqrt{ r^{2}+r'^{2}-2\mathbf{r}\cdot \mathbf{r}' }$. As in other situations, like [[Electric dipole#Radiation]] and [[Magnetic dipole#Radiation]], we are going to consider the source as very small compared to the distances that we are considering
$$r'\ll r\tag{Small source approximation}$$
Since $r'$ is a variable of integration, this means that $r'\ll r$ at all points during the integration, i.e. the entire source is small. In this approximation we get
$$\mathfrak{r}=r\sqrt{ 1- 2\frac{\hat{\mathbf{r}}\cdot \mathbf{r}'}{r}+ \frac{r'^{2}}{r^{2}}}$$
Careful with the change from $\mathbf{r}$ to $\hat{\mathbf{r}}$ in the cross-term! $r'^{2}/r^{2}$ is second-order and therefore negligible in the small source approximation. The rest of the root can use the [[Binomial theorem|binomial expansion]] to first order ($\sqrt{ 1-x }\simeq1-x/2$):
$$\mathfrak{r}\simeq r\left( 1- \frac{\hat{\mathbf{r}}\cdot\mathbf{r}'}{r} \right)$$
and so our distribution is actually dependent on
$$\rho\left( \mathbf{r}',t- \frac{\mathfrak{r}}{c} \right)\simeq \rho\left( \mathbf{r}',t- \frac{r}{c}+ \frac{\hat{\mathbf{r}}\cdot\mathbf{r}'}{c} \right)$$
Expanding $\rho$ in a [[Taylor series]] in $t$ about the [[retarded time]] at the origin
$$t_{0}\equiv t- \frac{r}{c}$$
yields
$$\rho\left( \mathbf{r}',t- \frac{\mathfrak{r}}{c} \right)\simeq \rho(\mathbf{r}',t_{0})+\dot{\rho}(\mathbf{r}',t_{0})\left( \frac{\hat{\mathbf{r}}\cdot\mathbf{r}'}{c} \right)+ \frac{1}{2}\ddot{\rho}\left( \frac{\hat{\mathbf{r}}\cdot \mathbf{r}'}{c} \right)^{2}+ \frac{1}{3!}\dddot{\rho}\, \left( \frac{\hat{\mathbf{r}}\cdot \mathbf{r}'}{c} \right)^{3}+\ldots$$
using dot notation for time derivatives. We do this because we wish to truncate to first order, but to do so must accept a second approximation:
$$r'\ll \frac{c}{\lvert \ddot{\rho}/\dot{\rho} \rvert }, \frac{c}{\lvert \dddot{\rho},\dot{\rho }\rvert^{1/2} }, \frac{c}{\lvert \ \ddddot{\rho}\ ,\dot{\rho} \rvert^{1/3} }\ldots\tag{Approximation 2}$$
and other further terms. Now, interpreting this is not an easy task, as we do not have an a priori idea of what $\rho$ is, besides some charge distribution. To gather some insight, recall that in simple oscillating systems, like electric and magnetic dipoles, these all end up being $c/\omega$, with $\omega$ the [[Frequency|angular frequency]] of oscillation, which is directly proportional to the [[wavelength]] $\lambda$. In those cases, we call it the large wavelength approximation, as it expects us to keep the wavelength larger than the size of the dipole. We can generalize this idea to mean "keep the size of *whatever* distribution small compared to the wavelength that's being emitted", with "size" being a vague, qualitative term more so than a precise quantity. But in general, we can't be so precise. In practice, this approximation, alongside the small source approximation, really just means "only keep the first-order terms in $r'$, that is, $(r')^{\pm1}$".

We now put the expansion of $\rho$, to first order only, alongside
$$\frac{1}{\mathfrak{r}}\simeq \frac{1}{r}\left( 1+ \frac{\hat{\mathbf{r}}\cdot\mathbf{r}'}{r} \right)=\frac{1}{r}\left( 1+ \frac{\mathbf{r}\cdot \mathbf{r}'}{r^{2}} \right)$$
in the formula for the retarded potential:
$$\begin{align}
V(\mathbf{r},t)&\simeq\frac{1}{4\pi \varepsilon_{0}}\int_{\mathcal{V}} \frac{1}{r}\left( 1+ \frac{\mathbf{r}\cdot \mathbf{r}'}{r^{2}} \right)\left[ \rho(\mathbf{r}',t_{0})+ \dot{\rho}(\mathbf{r}',t_{0})\left( \frac{\hat{\mathbf{r}}\cdot \mathbf{r}'}{c} \right) \right]d\tau' \\
&=\frac{1}{4\pi \varepsilon_{0}r}\int_{\mathcal{V}}\Big[ \rho(\mathbf{r}',t_{0})+\rho(\mathbf{r}',t_{0})\left( \frac{\mathbf{r}\cdot \mathbf{r}'}{r^{2}} \right)+ \\
&\qquad \qquad \quad+\dot{\rho}(\mathbf{r}',t_{0})\left( \frac{\hat{\mathbf{r}}\cdot \mathbf{r}'}{c} \right)+ \frac{\mathbf{r}\cdot \mathbf{r}'}{r^{2}}\dot{\rho}(\mathbf{r},t_{0})\left( \frac{\hat{\mathbf{r}}\cdot \mathbf{r}}{c} \right)\Big] \\
&=\ldots
\end{align}$$
The last term in the integral drops out because it is second order in $\mathbf{r}'$ (since we have $(\hat{\mathbf{r}}\cdot \mathbf{r}')(\hat{\mathbf{r}}\cdot \mathbf{r}')$). We are left with
$$V(\mathbf{r},t)\simeq \frac{1}{4\pi \varepsilon_{0}r}\left[ \int_{\mathcal{V}}\rho(\mathbf{r}',t_{0})d\tau'+ \frac{\hat{\mathbf{r}}}{r}\cdot \int_{\mathcal{V}}\mathbf{r}'\rho(\mathbf{r}',t_{0})d\tau'+  \frac{\hat{\mathbf{r}}}{c}\cdot \frac{d}{dt} \int_{\mathcal{V}}\mathbf{r}'\rho(\mathbf{r}',t_{0})d\tau' \right]$$
The first integral is just the total charge $Q$ at time $t_{0}$, and since charge is a conserved quantity, it remains the same at all times. The other two integrals are the [[electric dipole moment]] $\mathbf{p}(t_{0})$ at time $t_{0}$, so
$$\boxed{V(\mathbf{r},t)\simeq \frac{1}{4\pi \varepsilon_{0}}\left[ \frac{Q}{r}+ \frac{\hat{\mathbf{r}}\cdot \mathbf{p}(t_{0})}{r^{2}}+ \frac{\hat{\mathbf{r}}\cdot \dot{\mathbf{p}}(t_{0})}{rc} \right]}$$
What we got here is basically an extended [[multipole expansion]], truncated at the first order. The first term is the monopole term, the second is the dipole term, and the third is a new term that does not appear in the multipole expansion. That is because the multipole expansion is considered in static scenarios where $\dot{\mathbf{p}}=0$.

We now move on to the retarded vector potential
$$\mathbf{A}(\mathbf{r},t)=\frac{\mu_{0}}{4\pi}\int_{\mathcal{V}} \frac{\mathbf{J}(\mathbf{r}',t- \mathfrak{r}/c)}{\mathfrak{r}}d\tau'$$
To first order in $r'$, we can just replace $\mathfrak{r}$ with $r$ (i.e. a zeroth order approximation, you'll see why in a moment), so
$$\mathbf{A}(\mathbf{r},t)\simeq \frac{\mu_{0}}{4\pi r}\int_{\mathcal{V}}\mathbf{J}\left( \mathbf{r}', t_{0} \right)d\tau'$$
Now, it can be found that
$$\int_{\mathcal{V}}\mathbf{J}d\tau'=\dot{\mathbf{p}}$$
by evaluating $\int_{\mathcal{V}}\nabla\cdot(x\mathbf{J})d\tau$. So
$$\boxed{\mathbf{A}(\mathbf{r},t)\simeq \frac{\mu_{0}}{4\pi r}\dot{\mathbf{p}}(t_{0})}$$
This is why we could accept a zeroth order approximation $\mathfrak{r}\simeq r$, since $\mathbf{p}$ is already first order in $r'$. A first order approximation of $\mathfrak{r}$ would've ended up becoming a second (or higher) order one.
#### Fields
As for the fields, we only really care about the radiation zone, so
$$r^{-2}\text{ terms and below are negligible}\tag{Far field approximation}$$
In the [[electric field]], we need to take the [[gradient]] of $V$. Because of the far field approximation, the first term drops out ($\nabla r^{-1}\propto r^{-2}$). The second term is already second order on its own so it also drops out. The third term requires us to take the gradient of $t_{0}$:
$$\nabla t_{0}=- \frac{1}{c}\nabla r=- \frac{1}{c}\hat{\mathbf{r}}$$
and hence
$$V(\mathbf{r},t)\simeq \nabla\left[ \frac{1}{4\pi \epsilon_{0}} \frac{\hat{\mathbf{r}}\cdot \dot{\mathbf{p}}(t_{0})}{rc} \right]\simeq \frac{1}{4\pi \varepsilon_{0}}\frac{\hat{\mathbf{r}}\cdot \ddot{\mathbf{p}}(t_{0})}{c}\nabla t_{0}=- \frac{\hat{\mathbf{r}}\cdot \ddot{\mathbf{p}}(t_{0})}{4\pi \varepsilon_{0}c^{2}}\hat{\mathbf{r}}$$
The time derivative of $\mathbf{A}$ is
$$\frac{ \partial \mathbf{A} }{ \partial t } = \frac{\mu_{0}}{4\pi r} \ddot{\mathbf{p}}(t_{0})$$
So
$$\boxed{\mathbf{E}(\mathbf{r},t)\simeq \frac{\mu_{0}}{4\pi r}[(\hat{\mathbf{r}}\cdot \ddot{\mathbf{r}})\hat{\mathbf{r}}-\ddot{\mathbf{p}}]=\frac{\mu_{0}}{4\pi r}\hat{\mathbf{r}}\times(\hat{\mathbf{r}}\times \ddot{\mathbf{p}})}$$
The [[curl]] of $\mathbf{A}$ is
$$\nabla\times \mathbf{A}=\frac{\mu_{0}}{4\pi r}[\nabla \times \dot{\mathbf{p}}(t_{0})]=\frac{\mu_{0}}{4\pi r}[(\nabla t_{0})\times \ddot{\mathbf{p}}(t_{0})]=- \frac{\mu_{0}}{4\pi cr}[\hat{\mathbf{r}}\times \ddot{\mathbf{p}}(t_{0})]$$
and so
$$\boxed{\mathbf{B}(\mathbf{r},t)\simeq - \frac{\mu_{0}}{4\pi cr}\hat{\mathbf{r}}\times \ddot{\mathbf{p}}=- \frac{1}{c}\hat{\mathbf{r}}\times \mathbf{E}}$$
The fields are in [[phase]], mutually [[Orthogonality|perpendicular]] and transverse. The ratio of their [[amplitude|amplitudes]] is exactly the speed of light: $E_{0}/B_{0}=c$. This matches the behavior that an [[electromagnetic wave]] in the vacuum is supposed to have.
#### Electromagnetic waves
Analyzing the electromagnetic waves is more complicated than in a simple oscillating case, as we don't have a clear [[Frequency|angular frequency]] $\omega$ to use. Either way, we can make some general statements. We'll write the fields in [[spherical coordinates]], with the $z$ axis in the direction of $\ddot{\mathbf{p}}(t_{0})$:
$$\mathbf{E}(r,\theta,t)\simeq \frac{\mu_{0}\ddot{p}(t_{0})}{4\pi r}\sin \theta\ \hat{\boldsymbol{\theta}},\qquad \mathbf{B}(r,\theta,t)\simeq \frac{\mu_{0}\ddot{p}(t_{0})}{4\pi cr} \sin \theta\ \hat{\boldsymbol{\phi}}$$
The [[Poynting vector]] is
$$\mathbf{S}(\mathbf{r},t)\simeq \frac{\mu_{0}}{16\pi ^{2}cr^{2}}[\ddot{p}(t_{0})]^{2}\sin ^{2}\theta\ \hat{\mathbf{r}}$$
The [[radiant power]] passing through a large [[sphere]] of radius $r$ is
$$P(r,t)=\oint_{\mathcal{S}}\mathbf{S}(\mathbf{r},t)\cdot d\mathbf{a}=\frac{\mu_{0}}{6\pi c}\left[ \ddot{p}\left( t- \frac{r}{c} \right) \right]^{2}$$
and the total radiated power is
$$P_\text{rad}(t_{0})=\lim_{ r \to \infty } P(r,t)\simeq \frac{\mu_{0}}{6\pi c}[\ddot{p}(t_{0})]^{2}$$

We can see that if $p(t)=p_{0}\cos(\omega t)$, we get $\ddot{p}(t)=-\omega ^{2}p_{0}\cos(\omega t)$. Substitute this in the formulas above to get the electric dipole radiation again. More generally, set $\mathbf{p}(t)=q\mathbf{r}(t)$, where $q$ is an electric charge and $\mathbf{r}(t)$ is the distance of $q$ from the origin. Then $\ddot{\mathbf{p}}(t)=q\mathbf{a}(t)$, where $\mathbf{a}(t)$ is the acceleration of the charge, so the power is
$$P_\text{rad}(t_{0})=\frac{\mu_{0}q^{2}a^{2}}{6\pi c}$$
This is known as the **[[Larmor formula]]**, which gives the radiant power of an accelerating point charge. Notice how it is dependent on the *square* of the acceleration.

[^1]: Radiation as expressed here makes sense only in the context a localized source, that is, a source of finite extent, since the idea of "energy carried off to infinity" no longer makes sense when the source itself extends to infinity. Such shapes of course do not exist in the real world, but are common in simplified formulations of phenomena, such as infinite wires, infinite planes, etc.
