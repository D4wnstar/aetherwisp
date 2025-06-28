---
wiki-publish: true
---
The **Drude model** or **Drude-Lorentz model** is an approximate model of electrical conduction within a material, primarily metals. It is a kinetic gas model using [[electron|electrons]] as neutral [[particella|particles]] in metal.
### Qualitative description
Consider a metallic [[conductor]], for which the [[electric charge]] carriers are the valence [[Elettrone|electrons]] of the [[Atom|atoms]]. The mass and charge of the carriers therefore are [[massa dell'elettrone|electron mass]] $m=m_{e}$ and [[Elementary charge|elementary charge]] $q=-e$ respectively. Let's start by representing the electrons in the wire as a [[ideal gas]]. As in all kinetic gas models, the velocity of the electrons $\mathbf{v}_{\text{rand}}$ is completely random and isotropic and its average is zero: $\langle \mathbf{v}_{\text{rand}} \rangle=0$. Say, then, we apply an [[electric field]] $\mathbf{E}$ to the gas. The electrons respond by being attracted or repelled depending on the sign of the field and their velocity changes to
$$\langle \mathbf{v} \rangle_\text{drift}=\langle \mathbf{v}_{\text{rand}} \rangle + \frac{q\mathbf{E}}{m_{}}\langle t \rangle =\frac{q\mathbf{E}}{m}\tau $$
where $\langle t \rangle=\tau$ is the average time between collisions. Because the collisions are chaotic and unpredictable, the *directions* are again uniformly distributed, but the *magnitudes* are skewed in the direction of the electric field. So while the electrons [[Diffusione di particelle|scatter]] in all directions isotropically, they tend to move faster in the direction of the field, causing a general (albeit very slow) collective motion in that direction. This is known as the **drift velocity**.

As a whole, the electrons are sufficiently many to constitute a volume charge density $\rho$ moving at a velocity $\langle \mathbf{v} \rangle_\text{drift}$, which produces a volume [[Electric current|current]] density
$$\mathbf{J}=-Nq\langle \mathbf{v} \rangle_\text{drift}=\frac{Nq^{2}\tau}{m}\mathbf{E} \simeq\rho \langle \mathbf{v} \rangle_\text{drift} $$
where $N$ is the total number of electrons. But this is just [[Ohm's law]] in differential form, so we can express the [[electrical conductivity]] of a metallic conductor as
$$\sigma_{C}=\frac{Nq^{2}\tau}{m}$$
We know empirically that $\sigma_{C}$ is mostly constant, so since $N$, $q$ and $m$ are all themselves constant, $\tau$ too must be constant[^1], at least within the same limits as $\sigma_{C}$.

The linear connection between electric field and *velocity* is noteworthy as the field is inherently linear to *acceleration* (by way of [[Interazione elettromagnetica|Coulomb's law]] and [[Newton's laws|Newton's second law]]), not a velocity. The fact that velocity is constant for a given field intensity suggests that there's something "pushing back", preventing the electrons from accelerating to higher speeds. This behavior can be succinctly explained by interactions with the lattice of the material, which exchanges energy with the electrons through mostly random thermal interactions, and is a remarkably simple way of explaining the [[Joule effect]].
### Quantitative explanation
The Drude model is an inherently classical system, and although it was developed three years after the discovery of the electron, it does not rely on much of the electron's properties besides its charge and the fact it is a particle. In fact, we won't consider the electron to be a quantum object for this model, as quantum physics was not even thought of at the time.

The Drude model is based on four major assumptions:
1. The positive charge is localized on stationary [[Nucleo atomico|nuclei]]. Electrons can collide with nuclei and bounce off, but they do so as rigid neutral particles. They do not interact at any range other than with collisions (**free electron assumption**).
2. Electrons do not collide with each other. They do not interact with each other (**independent electron assumption**).
3. There exists some time $\tau$ which is the [[mean]] time between collisions. The probability of collision is $1/\tau$.
4. Electrons reach [[thermal equilibrium]] with their surroundings exclusively through collisions. The velocity that the electron has after a collision is completely random and unrelated to the previous one. This velocity obeys the local [[probability distribution]] of velocities at the point of impact.

This is a classical model, so defining what a collision is rather straightforward: two electron colliding with each other. The [[mean free path]] of an electron between collisions is just $\lambda=\tau v_{t}$, where $v_{t}$ is the thermal (i.e. random and isotropic) velocity of the electrons. Since we are considering the electrons as a neutral gas (read: [[ideal gas]]), we can use the [[equipartition theorem]] to get the velocity from the equation
$$\frac{1}{2}mv_{t}^{2}=\frac{3}{2}k_{B}T\quad\Rightarrow \quad v_{t}=\sqrt{ \frac{3k_{B}T}{m} }$$
where $m$ is the [[mass]] of the electron, $k_{B}$ is the [[Boltzmann constant]] and $T$ is the [[temperature]] of the gas[^2]. Using typical values for a metal, we get something like $v_{t}\simeq 10^{5}\text{ m/s}$. $\tau$ is a fundamental quantity which is not derived by the Drude model. It depends on metal, but it's usually in the order of $10^{-14}$ seconds, which corresponds with a mean free path of about $\lambda\sim1\text{ nm}$. Considering that the size of [[atom|atoms]] is in the order of $\sim 0.1\text{ nm}$, this is a pretty sensible range.

This is what happens in gas (i.e. electrons in metal) at rest. If we apply a constant [[electric field]] $\mathbf{E}$, the electrons are pushed or pulled by it. Beyond the thermal velocity, we get another extra term which is due to this field. A [[Lorentz force]] equated with [[Newton's laws|Newton's second law]] on an electron yields
$$\mathbf{F}=-e\mathbf{E}=m\mathbf{a}\quad\Rightarrow \quad \mathbf{a}=-\frac{e}{m}\mathbf{E}\quad\Rightarrow \quad \mathbf{v}_{el}=-\frac{et}{m}\mathbf{E}+\mathbf{v}_{0}$$
where $e$ is the [[elementary charge]]. Now, in total we get
$$\mathbf{v}=\mathbf{v}_{t}+\mathbf{v}_{el}$$
This is an inherently random quantity due to $\mathbf{v}_{t}$ being a [[random variable]]. It is then more useful to consider the mean of this velocity:
$$\mathbf{v}_{avg}=\langle \mathbf{v} \rangle =\langle \mathbf{v}_{t} \rangle +\langle \mathbf{v}_{el} \rangle =- \frac{e\tau}{m}\mathbf{E}$$
since $\langle \mathbf{v}_{t} \rangle=0$ by definition of the kinetic model (isotropic motion), $\langle t \rangle=\tau$ and $\langle \mathbf{E} \rangle=\mathbf{E}$ since it's constant. We can define the **mobility** $\mu\equiv e \tau/m$ to write the velocity of the electrons as a simple linear function of $\mathbf{E}$:
$$\mathbf{v}_{avg}=\mu \mathbf{E}$$
With a reasonable field of $\mathbf{E}\sim 10\text{ V/m}$, the speed comes out at a *tiny* $0.01\text{ m/s}$, far smaller than the one due to thermal excitation, $\sim 10^{5}\text{ m/s}$. This proves that electrons move across a metal *exceptionally slowly*. While their motion is very fast, it's chaotic and isotropic, so it tends to make the electrons stay around some average position and bounce around it by continuous collisions. When an electric is applied, say by a battery trying to make an [[electric current]] through a wire, the electrons *do* move in the direction of the field, but it takes them forever to go through the wire itself. The actual "information" of the current is carried by electrons colliding with others preferentially in the direction of the electric field, leading to a net flow of current in that direction[^3].

Each electron carries charge $-e$, so the density of $n$ electrons moving through some surface $A$ is $-en\mathbf{v}_{avg}A$. Take the derivative by $A$ and you get the current density
$$\mathbf{J}=-en\mathbf{v}_{avg}=\frac{ne^{2}\tau}{m}\mathbf{E}$$
But this is just [[Ohm's law]], with a specific shape for the [[electrical conductivity]]:
$$\sigma=\frac{Ne^{2}\tau}{m}$$
If we flip this upside down for resistivity we get
$$\boxed{\rho=\frac{1}{\sigma}=\frac{m}{Ne^{2}\tau}}$$
This is the resistivity as given by the Drude model. This form of Ohm's law, $\mathbf{E}=\rho \mathbf{J}$, is linear. As one might imagine, this is not the best description, as the real phenomenon is found to not be really linear. However, it does behave as a rather good approximation for metals, in which the free nature of electrons makes smooth motion possible.

The theory is valid for metals and homogeneous semiconductors (like $\mathrm{Si}$ and $\mathrm{Ge}$), but not inhomogeneous semiconductors (like $\mathrm{GaAs}$ or $\mathrm{InAs}$) and in contact points between metals and semiconductors. In these cases, quantum effects cannot be neglected.
### Results
Being a basic theory of conductivity, the Drude model can be used to derive several other effects. One of them is the Hall effect, which has its own article at [[Hall effect]]. Another is the reflectivity of metals, which is described below here.
#### Reflectivity of metals
When an [[electromagnetic wave]] hits a material, it splits between a reflected and transmitted wave, as described by the [[Fresnel coefficients]]. We'll use a generic [[Plane wave]] of equation $\mathbf{E}(z,t)=\mathbf{E}_{0}e^{i(kz-\omega t)}$ for this discussion. The [[wavenumber]] $k$ can be written in terms of the [[wavelength]] $\lambda_{0}$ as
$$k=\frac{2\pi N}{\lambda_{0}}$$
where $N=n+i\kappa$ is the complex [[refractive index]]. Using Maxwell's relation for refractive index, we have $N=\sqrt{ \varepsilon }=\sqrt{ \varepsilon_{r}+i\varepsilon_{i} }$, where $\varepsilon$ is the complex [[permittivity]]. The wave then is
$$\mathbf{E}(z,t)=\mathbf{E}_{0}e^{i((2\pi N/\lambda_{0})z-\omega t)}=\mathbf{E}_{0}e^{i((\omega \sqrt{ \varepsilon }/c)z-\omega t)}$$
(TODO: Finish this with PDF for Drude model results)
### Limitations
The Drude model fails in several situations. For instance, it fails to predict the conductivity of alloys, which is very inconsistent and certainly not a linear average of the two pure metals' conductivity. It also fails when temperatures become very low, such as metals bathed in liquid nitrogen.

Nevertheless, the fact that the model can even produce good results at all is quite staggering given that the assumptions it is based on are completely *wrong*. It assumes that electrons neither interact with each other, nor with ions, which sounds nonsensical on paper, and yet it still provides reasonably correct values in many common conditions. This, in a way, is the key takeaway of the Drude model. Free electron behavior is weird and does not work as one would intuitively expect, but to fully understand why, we need more advanced models. Historically, the next step after the Drude model is the [[Sommerfeld model]], which is an actually quantum-native description that uses a [[Fermi gas]] to model the electrons. As H. A. Lorentz put it:

> In a theory which gives results like this, there must certainly be a great deal of truth.

[^1]: The actual value is, unsurprisingly, tiny. For copper, it's in the ballpark of $2.5\times10^{-14}$ seconds.

[^2]: The actual meaning of temperature is a bit complicated. In a better model, we'd be talking about a [[Fermi gas]] and using quantum statistical mechanics to get the temperature, but this is an old, fully classical model, so we'll give pretend none of that exists and take temperature for granted.

[^3]: Though do note that current follows in the direction of the field only in ohmic materials. The Drude model does not predict any form of non-ohmic conduction.
