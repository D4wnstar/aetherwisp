---
wiki-publish: true
---
**Cherenkov radiation** or **Cherenkov effect** is a form of [[electromagnetic radiation]] that occurs when the speed of a [[Electric charge|charged]] [[Particle|particle]] in a medium exceeds the [[speed of light]] in that medium. The particle emits bluish radiation in a cone that expands at a well-defined angle around its axis of velocity.

The [[energy]] radiated is rather small, but is quite as a particle [[detector]] since it only occurs above certain speeds. It is therefore used to determine if a particle is going above or below a certain speed.
### Mechanism
Consider a medium with [[refractive index]] $n(\omega)$. When a charged particle passes through, its [[electric field]] affects the positive and negative charges of the [[Atom|atoms]], creating [[Electric dipole|electric dipoles]] that [[polarization|polarize]] the medium. As the particle leaves, the medium depolarizes. The time-variant polarization creates oscillating dipoles that emit dipole radiation in a [[spherical wave]] centered on the location where the particle passed. This occurs continuously throughout the entire trajectory of the particle, creating a [[wavefront]] that is the outer rim of many infinitesimally delayed spherical waves.

:::image
![[Diagram Cherenkov radiation|80%]]
A diagram of how Cherenkov radiation is released. This is a 2D cross section. The actual wavefront is conical (rotate the purple lines around the axis to see it).
:::image

This happens every time charged particles pass through [[matter]], but we don't see Cherenkov radiation normally. So what? The reason is that these waves cause destructive [[interference]] with each other and cancel out shortly after emission, leaving no real radiation as a whole. The difference occurs when the particle's speed exceed the speed of light in the medium:
$$v> \frac{c}{n(\omega)}$$
In this case, the particle moves faster than the wave can propagate, which causes them to sum *coherently* and not cancel out, thus letting the radiation reach far distances.

The angular opening $\theta_{C}$ of the conical wavefront is called the **Cherenkov emission angle**. It can be found through purely geometrical considerations.

![[Diagram Cherenkov radiation geometry|80%]]


$\beta ct$ is the hypotenuse and $ct/n$ is its cosine so
$$\frac{c}{n}t=\beta ct\cos \theta_{C}$$
Rearrange
$$\boxed{\cos\theta_{C}=\frac{1}{n\beta}}$$
There's a few considerations to make:
1. The velocity must be $\beta\geq1/n$, otherwise $1/n\beta>1$ which is impossible for a cosine. In other words, this is true only if the particle moves faster than the speed of light in the medium, as we claimed before.
2. Since $n$ is assumed to be known, measuring $\theta_{C}$ is equivalent to measuring $\beta$. Measuring $\theta_{C}$ is easier than measuring $\beta$ directly.
3. The maximum angle occurs when $\beta=1$, in which $\theta_{C}=\arccos(1/n)$. For regular glass ($n=1.52$), this is about $\theta_{C,\text{max}}=48.9°$.
4. There's no requirement on what $n$ needs to be. Any transparent material can be exhibit Cherenkov radiation.

Cherenkov radiation is also inversely proportional to the wavelength (not proven here, search "Frank-Tamm formula" if you're curious) and it emits a continuous spectrum straddling ultraviolet and visible light, with a peak at 420 nm. For this reason, Cherenkov radiation is visible to the naked eye and appears blue/violet. It's a common sight in nuclear reactor pools, which is why blue is often used in nuclear energy logos and symbols.

This phenomenon is geometrically identical to a sonic boom in [[sound]] or the wake formed by a boat moving faster than [[gravity waves|sea waves]].
#### Energy loss
The energy loss due to Cherenkov radiation depends on the number of photons emitted per unit path length. The number $N$ of these in turn depends on $\theta_{C}$ (indeed the number emitted per unit length is $dN/dx\propto \sin^{2}\theta_{C}$). It turns out that the energy lost per unit path is
$$\frac{dE}{dx}\simeq z^{2}\sin^{2}\theta_{C}$$
usually measured in [[Electronvolt|keV]]/cm, a thousand times smaller than [[Stopping power|collisional loss]]. For this reason, it can be neglected.
### Detectors
It's sometimes useful to express the threshold speed as a gamma:
$$\gamma _\text{min}=\frac{1}{\sqrt{ 1-\beta _\text{min}^{2} }}=\frac{n}{\sqrt{ n^{2}-1 }}$$
Particle speeds can be quite intense, so using $\gamma$ is often advised to avoid having to deal with minuscule differences between $\beta$ and $c$. The threshold $\gamma$ increases as $n\to 1$, meaning as the materials stops refracting and just lets light through. As such, barely-refracting materials can be used to make very high speed Cherenkov thresholds, useful to fine-tune the value for experimental use in [[detector|detectors]]. For instance, pressurized gases can be used to manipulate $n$ to be very near one. This is particularly useful at very high speeds where the [[Stopping power|Bethe-Bloch formula]] stops providing clear distinctions between particles[^1].

The emission angle can be measured using a photosensitive screen or ring on which the radiation cone impacts. From the radius of the circle measured on the screen, we can determine the emission angle.

[^1]: Remember that you can use speed to estimate [[mass]] if you know the [[kinetic energy]]. This is why we care about speed distinctions.
