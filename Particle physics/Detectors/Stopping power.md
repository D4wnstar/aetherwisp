---
wiki-publish: true
aliases:
  - Bethe-Bloch formula
  - energy straggling
  - radiation length
  - Bohr formula
---
The **stopping power** $S$ is the rate at which a material slows down and eventually stops an incident [[Particle|particle]]. Mathematically, it is the opposite of the [[mean]] of the space derivative of [[kinetic energy]]:
$$S(K) = - \left\langle \frac{dK}{dx} \right\rangle$$
The mean is needed because the interaction of particles inside of matter is extremely complex and [[random]], so we can only afford to quantify the average behavior.

This rate was first calculated by Bohr for heavy particles ([[mass]] much bigger than [[electron|electrons]]) in a classical framework. This lead to the **Bohr formula** for stopping power. It was later extended to a quantum mechanical treatment by Bethe and Bloch, who are the namesake of the **Bethe-Bloch formula** for stopping power:
$$S(K) = 4\pi m_{e}c^{2}r^{2}_{e}N_{A} \frac{\rho Z}{A} \frac{z^{2}}{\beta^{2}} \left[ \ln\left( \frac{\beta^{2} \gamma^{2} m_{e}c^{2}}{h\nu} \right) - \beta^{2} - \frac{\delta(\gamma)}{2} \right]$$
This is a complicated formula: see the main body for a proper description. The Bohr formula is the same, but lacks the $\beta ^{2}$ and $\delta(\gamma)/2$ terms, which are relativistic corrections.

For light particles, the behavior comes out to be much simpler and reminiscent of the classical [[Beer-Lambert law]] for [[irradiance]]:
$$S(K) = \frac{K}{L_{R}}$$
where $L_{R}$ is the **radiation length**. In fact, if you integrate for $K$, you get an exponential decay: $K(x) = K_{0} e^{-x / L_{R}}$.

Stopping power is of great importance in [[detector]] physics, since the detector picks up the energy that the particle loses and uses that to determine the presence of a particle. It's also fundamental to [[radiation protection]] to prevent [[radiation]] damage to humans and objects.

> [!question] A note on notation
> It's very common to use $E$ instead of $K$ to denote the kinetic energy. I find this notation unnecessary and confusing, since it mixes up kinetic and total energy, not to mention electric fields, so Aetherwisp uses $K$. However, be aware that in other texts $E$ is the more common letter.
## Mechanism
Stopping power is essentially a macroscopic average of microscopic interactions. As such, the stopping power is not just dependent on the incoming energy, but also on the kind of incident particle. Most discussion on stopping power is surrounding [[Electric charge|charged particles]] and their energy loss due to [[electromagnetism]], since that's the most common and most impactful [[fundamental interaction]]. In this context, there's two primary ways a particle can lose energy. [[Particle scattering]] is the obvious one: particles collide and are deflected. This is the main cause of energy loss for heavy particles. [[Bremmstrahlung]] is the other. This is the main cause for light particles. We explore these two independently.
### Collisional energy loss  
Consider a heavy particle of charge $ze$ colliding with a bound electron. Assume the particle has a constant velocity $\mathbf{v}$ much greater than that of the electron, so that we can treat the electron as approximately stationary. Also assume that the projectile does not get noticeably deflected from its trajectory. This allows us to only consider the [[electric field]] perpendicular (transverse) to the motion, since the parallel component integrates to zero over the whole undeflected trajectory (the repulsion slows down on entry just as much as it speeds up on exit). The projectile enacts an electrostatic [[Lorentz force]] $\mathbf{F}=-e\mathbf{E}_{\perp}$ on the electron. The momentum variation is, as per [[Newton's laws|Newton's second law]],
$$\Delta \mathbf{p}=\int \mathbf{F}dt=-e\int \mathbf{E}_{\perp}dt=-e\int \mathbf{E}_{\perp} \frac{dt}{dx}dx=- \frac{e}{v}\int \mathbf{E}_{\perp}dx$$
In order to solve the integral, we consider a [[cylinder]] of infinite length coaxial with the trajectory, we can use [[Gauss' law]] to determine the [[flux]] of the electric field:
$$\Phi(\mathbf{E}) = \int_{S} \mathbf{E} \cdot d\mathbf{a} = 2\pi b \int \mathbf{E}_{\perp} dx = \frac{ze}{\varepsilon_{0}}$$
where $b$ is the radius of the cylinder, equal to the distance between the axis (i.e. trajectory) and the electron. To take a term out of Rutherford's book, this is the **impact parameter** of the scattering, analogous to the one in [[Rutherford scattering]]. Reorder to get
$$\int \mathbf{E}_{\perp}dx=\frac{ze}{2\pi \varepsilon_{0}b}$$
and so
$$|\Delta\mathbf{p}| = \Delta p = \frac{ze^{2}}{2\pi b\varepsilon_{0}v} = \left( \frac{ze^{2}}{4\pi b^{2}\varepsilon_{0}} \right) \left( \frac{2b}{v} \right)$$
The first term is the electrostatic force at the point of closest approach (distance $b$) and the second is the time scale of the interaction $\tau$. Unsurprisingly, this time scale is tiny. If $b=0.1\ \mathring{\text{A}}$ and $v=14\ 000\text{ km/s}$ (typical velocity of $K\sim 1\text{ MeV}$), we get $\tau=2b/v=1.43\times 10^{-18}\text{ s}$. The interaction happens in a minuscule fraction of a second.

The kinetic energy acquired by the electron, and thus lost by the projectile, is
$$K_{x}(b) = \frac{\Delta p^{2}}{2m_{e}} = \frac{e^{4}}{8\pi^{4}\varepsilon_{0}m_{e}} \frac{z^{2}}{v^{2}b^{2}}= 2m_{e}c^{2}r_{e}^{2}\frac{z^{2}}{\beta^{2}b^{2}}$$
using the [[Lorentz transformation|relativistic]] $\beta=v/c$ and defining the classical electron radius
$$r_{e}=\frac{e^{2}}{4\pi \varepsilon_{0}m_{e}c^{2}}\simeq 2.82\text{ fm}$$
From this, we infer that:
- Energy transfer decreases the farther the projectile is, that is, as $b$ increases.
- Faster projectiles lose less energy.
- The inverse dependence on mass of the target (here an electron) implies that collisions with [[Atomic nucleus|nuclei]] are negligible compared to electrons, due to the much larger mass of nuclei. This is why we started with the assumption that the collision was with an electron.
- Higher projectile charge means more energy loss. However, most particles have $z=\pm 1$, so this mostly doesn't matter.

This is the loss for a single interaction. We now want to jump to the loss for a macroscopic material. We'll need to estimate the number of interactions per unit distance. In a thin target of thickness $dx$, with $n_{0}$ electron volume density, the energy loss is due to all electrons surrounding the trajectory. The system possesses cylindrical symmetry, as all electrons at the same radius from the trajectory contribute the same amount. As such, the energy loss per unit thickness per unit radius is
$$-d^{2}K(b) = n_{0} \ 2\pi b db\ dx \ K_{x}(b)$$
where $db$ is the thickness of the ring around the trajectory and $2\pi bdb$ is its area. Inverting
$$- \frac{d^{2}K(b)}{dxdb}=2\pi bn_{0}K_{x}(b)$$
To get the energy loss from all electrons over a thin sheet we integrate over all relevant $b$:
$$S(K)=- \frac{dK}{dx} = \int_{b_{\text{min}}}^{b_{\text{max}}} 2\pi bn_{0} K_{x}(b)db = 4\pi m_{e}c^{2}r_{e}^{2}\frac{n_{0} z^{2} }{\beta^{2}} \ln\left( \frac{b_{\text{max}}}{b_{\text{min}}} \right)$$
The limits $b_{\text{min}}$ and $b_{\text{max}}$ must are not 0 and $\infty$ as you might expect. The problem is that for $b_\text{min}=0$, the logarithm blows up and we'd have infinite energy transfer. For $b_\text{max}\to \infty$, the interaction time scale would grow very large, which goes against our assumption of stationary electrons. Thus, we need to pick these values carefully:
- $b_{\text{max}}$ can be chosen to be $\simeq \gamma v / \nu$ where $\nu$ is the orbital [[frequency]] of the electron and $\gamma$ is the relativistic quantity. This more or less says "fast enough for the electron to be sort of stationary". More formally, this follows from the [[adiabatic invariance principle]], which states that the interaction must be fast compared to the electron’s orbital period, faster than $T=1/\nu$. The interaction time is $\tau\sim b/v$, so $b\sim \tau v$. We want at most $\tau \simeq T=1/\nu$. Adding in [[time dilation]] concerns ($T\to \gamma T$), we have $b_\text{max}\simeq \gamma v/\nu$.
- $b_{\text{min}}$ cannot be smaller than the electron’s "radius", in the sense of its [[de Broglie formula|de Broglie wavelength]] $\lambda_{e}=h/p=h/\beta \gamma m_{e}c$, and so since $b \geq \lambda_{e}$ we take $b_{\text{min}} \simeq h / \beta \gamma m_{e}c$.

Plugging these definitions in the stopping power gets us
$$S(K)= 4\pi m_{e}c^{2}r_{e}^{2}\frac{n_{0} z^{2} }{\beta^{2}} \ln\left( \frac{\beta ^{2} \gamma ^{2} m_{e} c^{2}}{h\nu} \right)$$
One last step: the electron density for now is a somewhat cryptic quantity. We can express it in terms of the [[Avogadro number]] $N_{A}$, mass density $\rho$, [[Atom|mass number]] $A$ and [[Atom|atomic number]] $Z$:
$$n_{0} = N_{A}\frac{\rho Z}{A}$$
Plug this into into the stopping power to get
$$\boxed{S(K)=- \frac{dK}{dx} = 4\pi m_{e}c^{2}r^{2}_{e}N_{A} \frac{\rho Z}{A} \frac{z^{2}}{\beta^{2}} \ln\left( \frac{\beta^{2} \gamma^{2}m_{e}c^{2}}{h\nu} \right)}$$
This is the **Bohr formula** for stopping power. The quantity $h\nu\equiv I$ is the **mean excitation energy** of the material. It's sometimes expressed in terms of the **mass thickness** $X=\rho x$:
$$S_{\text{MT}}(K) = - \frac{dK}{dX} = 4\pi m_{e}c^{2}r^{2}_{e}N_{A} \frac{Z}{A} \frac{z^{2}}{\beta^{2}} \ln\left( \frac{\beta^{2} \gamma^{2}m_{e}c^{2} }{h\nu} \right)$$
Be aware that this version is measured in $\text{MeV}/\text{g cm}$ instead of $\text{MeV}/\text{cm}$ like the normal form. The value of this form is that it makes it apparent that the collisional stopping power is actually quite independent of *both* the type of projectile *and* the material's properties. The only factors left are the value of $Z/A$, which is $\simeq0.5$ for more or less every [[chemical element]] except the superheavy ones ($Z/A< 0.5$) and hydrogen ($Z/A=1$); $z^{2}$, which as we've said is pretty much always $\pm 1$ outside of twice-or-more ionized atoms; and $\nu$, which does admittedly change a good bit between atoms, but is inside a heavily suppressed logarithmic term which is more or less a constant factor for any velocity beyond ultrarelativistic ones. The rest is all constants, with the exception of $\beta$. Basically, we can see that the mass-thickness stopping power is almost exclusively determined from the velocity of the projectile, regardless of the what the projectile even is or what it's smashing into. This is not true only for the heaviest materials like uranium and for ultrarelativistic particles. Of course, the regular stopping power also has a linear dependence on mass density, so dense materials like solid lead will stop much more than light ones like gases.

In terms of the curve it makes when plotted over speed, it's essentially $1/\beta ^{2}$ for most speeds and then transitions into $\ln(\beta ^{2}\gamma ^{2})$ for relativistic speeds when the logarithm starts dominating. See the plot further below.

> [!success] Stopping power dependence
> Collisional stopping power is almost entirely determined by the mass density of the target and the speed of the projectile. Other factors only start to matter at the absolute extremes: superheavy elements, pure hydrogen, heavily ionized atoms and ultrarelativistic particles. As such, the stopping power profile with respect to projectile speed is to be considered universal across almost all materials.

It might be useful to know that the first chunk of the formula is just one big constant:
$$4\pi m_{e}c^{2}r_{e}^{2}N_{A}\simeq0.3\ \frac{\text{MeV cm}^{2}}{\text{g}}$$
A more accurate version of the Bohr formula can be derived with quantum-mechanical considerations:
$$\boxed{S(K) = 4\pi m_{e}c^{2}r^{2}_{e}N_{A} \frac{\rho Z}{A} \frac{z^{2}}{\beta^{2}} \left[ \ln\left( \frac{\beta^{2} \gamma^{2} m_{e}c^{2}}{I} \right) - \beta^{2} - \frac{\delta(\gamma)}{2} \right]}$$
This is called the **Bethe-Bloch formula**. As you can see, it only differs from the Bohr formula due to the addition of two extra relativistic terms. The first, $-\beta ^{2}$, shows a noticeable stopping power reduction at high relativistic speeds ($\beta \simeq 1$). The second, $-\delta(\gamma)/2$, is dependent on a function $\delta(\gamma)$ of the relativistic $\gamma$. This term represents a density correction due to the [[dielectric polarization]] of the medium and further decreases stopping power at relativistic speeds. There is also a mass thickness variant:
$$S_\text{MT}(K) = - \frac{dK}{dX} = 4\pi m_{e}c^{2}r^{2}_{e}N_{A} \frac{Z}{A} \frac{z^{2}}{\beta^{2}} \left[ \ln\left( \frac{\beta^{2} \gamma^{2} m_{e}c^{2}}{I} \right) - \beta^{2} - \frac{\delta(\gamma)}{2} \right]$$
All considerations regarding the Bohr formula apply here too, with the difference that the additional terms suppress ultrarelativistic stopping power even more than it already was.

:::image
![[Plot Stopping power collisional|80%|center]]
A plot of Bethe-Bloch stopping power with respect to projectile velocity (expressed as $\beta \gamma$). This profile is mostly universal across materials. The $x$-axis is in log10 scale.
:::

From the figure we can see that stopping power decreases to a minimum and then rises again due to relativistic effects. A particle whose velocity is just right to be in the local minimum of stopping power ($\beta \gamma \simeq 3\textendash4$) is called a **minimum ionizing particle** (**MIP**). The minimum energy loss is also quite universal, hovering in the range $1\textendash 2\text{ MeV cm}^{2}\text{/g}$.

Something interesting (and very useful) appears when we look at stopping power in terms of momentum instead of speed. Actually, it occurs for any variable dependent on speed and mass (e.g. kinetic energy; momentum just happens to be the most used). Since $p=mv$ and $v$ determines the behavior by itself, there's a "push and pull effect" between projectile mass and momentum. What I'm trying to say is that, in a plot of $S(K)$ vs. $p$ (or $S(K)$ vs. $K$), the mass *does* play a role in the profile (it needs to in order to cancel out the mass in the other variable). That means we get distinctly different curves for different masses.

:::image
![[Plot Stopping power collisional for p|80%]]
A stopping power plot in terms of kinetic energy for a charged [[kaon]] and a [[proton]].
:::

This is extremely useful, because it provides us with a way to discriminate different particles. Since mass is essentially the only property that's truly unique to each particle, by plotting out these curves experimentally, we can measure the mass of the particle indirectly. If we recognize the mass, then we've identified the particle!

Note that for larger masses, the plot gets [[translation|shifted]] to the right, meaning it generally loses more energy as the minimum gets pushed further into relativistic territory. The difference is biggest in low-energy, nonrelativistic range. Unfortunately, many particle detections are well into the relativistic range, so the differences actually seen in practice can require a high level of precision to discern or be outright impossible to use for really high speeds. This is especially true since the energy loss given by the Bethe-Bloch formula is a mean: the real loss will be a distribution around it. As such, the actual measurements will not find *curves* but rather *bands* with a certain width around the curve. When two bands are close enough, they tend to overlap, making distinction hard.

:::image
![[BetheBlochExpBands.png]]
Theoretical values of the Bethe-Bloch (left) and experimental bands (right).
:::
#### Energy straggling
The energy loss due to many collisions is inherently random. If the incident beam is monoenergetic, meaning all incident particles have the same energy, the energy loss distribution is found to be a [[Poisson distribution]]. As per the [[central limit theorem]], when the number of collisions is large (i.e., the material is sufficiently thick), the energy loss distribution becomes a [[Gaussian distribution|Gaussian]]. This phenomenon is known as **energy straggling**. In thin materials, where the central limit theorem does not apply, we find [[Landau-Vavilov distribution]] instead, which has a high tail for high-energy losses.

If the material is thick enough, the stopping power might cause the particle to lose all of its energy and get "stuck" in the material. Since the energy loss is random, so is the distance at which it happens. We call this the **[[range]]** of the particle and its randomness is called **range straggling**.
#### Bragg peaks
The collisional energy loss scales as $\sim1/\beta ^{2}\sim 1/v^{2} \sim 1/K$. Because of this, the majority of energy lost occurs where the particle is slowest, which means at the end of its travel distance right before it stops. A plot of energy loss versus depth shows a sharp peak around the mean range, a shape known as a **Bragg peak**.
### Radiative energy loss  
Collisional stopping power is a good measure for all particles of comparable mass to [[electron|electrons]]. For electrons themselves (and all charged particle of same or similar mass, e.g. positrons), however, our assumptions lose validity: this is because electrons tend to be heavily deflected by the fields of atoms due to having quite small mass. Because of this, the main energy loss of electrons is dominated by [[bremmstrahlung]], which is a form of [[electromagnetic radiation]] that occurs when particles decelerate. This loss also happens in heavy particles, but since their deflections are so small, it is minimal compared to collisions and can be safely ignored[^1].

The theory for the radiative energy loss for an electron of kinetic energy $K_{0}$ was developed by Bethe and Heitler in 1934, the result of which is:
$$\boxed{S_\text{rad}(K)=- \left.\frac{dK}{dx}\right|_{\text{rad}} = \frac{K}{L_{R}}}$$
The value $L_{R}$ is a constant known as the **radiation length**:
$$\frac{1}{L_{R}} = \ln\left( \frac{183}{Z^{1/3}} \right) \frac{4 r_{e}^{2} N_{A}^{2} Z^{2} \alpha \rho}{A}$$
$N_{A}$ is the [[Avogadro number]], $r_{e}$ is the classical electron radius, $\alpha$ is the [[fine-structure constant]], $Z$ and $A$ are the atomic and mass number of the material, and $\rho$ is the density of the material.

This quantity is the distance over which the electron's energy is reduced by a factor of $1/e$ due to bremmstrahlung. Note the important dependence on $Z^{2}$: it means that heavier elements are much, much better than lighter ones at stopping electrons. Some common values are 36 cm for $\ce{H_{2}O}$, 9 cm for $\ce{Al}$, 1.7 cm for $\ce{Fe}$, and 0.56 cm for $\ce{Pb}$. This explains why metals, lead especially, are such effective radiation shields.

Radiative stopping power is a pretty easy first-order *linear* [[ordinary differential equation]], which solves to
$$K(x) = K_{0} e^{-x / L_{R}}$$
This is a form reminiscent of the [[Beer-Lambert law]], here for kinetic energy. In fact, $L_{R}$ is essentially the bremmstrahlung absorption coefficient. Importantly, the energy loss is *exponential* with distance traveled. As such, when radiative losses dominate, they stop particles far faster than any collision.

The photons emitted can in theory carry any energy between 0 and $K_{0}$. Also, as always with bremmstrahlung, the spatial distribution of the photons that are emitted is characteristic and uniquely defined by the electron's speed and deceleration.  Their mean angle of emission with respect to the axis of deceleration is $\langle \theta \rangle\simeq m_{e}c^{2}/K_{0}$.

The energy loss due to bremmstrahlung is exponential, and at high energies, it dominates over ionization. At low energies, ionization is more significant. The larger the mass of the particle, the higher the threshold is for radiation to start dominating. This threshold, where both processes contribute equally, is known as the **critical energy** $K_C$, which is known to be
$$K_{C}\simeq \frac{600}{Z}\text{ MeV}$$

:::image
![[Plot Stopping power col vs rad|80%|center]]  
Comparison of radiative and collisional stopping power. The two cross at the critical energy, after which radiative loss dominates. The $\beta \gamma$ axis is logarithmic.
:::

If electrons are at high energies, the ionization loss can be completely ignored in favor of a pure radiative contribution. However, since radiative loss is proportional to[^2]
$$\frac{dK}{dx}\propto \frac{Z^{2}}{m_{e}^{2}}K$$
if we change the particle to something else, the mass $m_{e}$ changes. Thus, we can compare the electron radiative loss to other, heavier particles' radiative loss. For some heavier mass $M>m_{e}$ we have
$$\frac{dK}{dx}(M)\propto \frac{Z^{2}}{M^{2}}K$$
We can ask at what kind of energy the heavier particle radiates as much as an electron, which is like asking when the heavier particle's energy loss is overwhelmingly radiative:
$$\frac{Z^{2}}{m_{e}^{2}}K_{e}=\frac{Z^{2}}{M^{2}}K\quad\Rightarrow \quad K=\left( \frac{M}{m_{e}} \right)^{2}K_{e}$$
where we wrote $K_{e}$ to differentiate the electron's energy from the heavier particle's one. Evidently, the kinetic energy leading to pure radiative loss increases with the square of the ratio of the particle-to-electron mass. Since electrons are quite light, this number is usually enormous; for a proton it is $(938\text{ MeV}/0.51\text{ MeV})^{2}=3.4\times 10^{6}$. So, for a proton to radiate as much energy as an electron, it would need to have energies several million times larger. To radiate as much as a 10 MeV electron, it would need 34 TeV! You can also see this in reverse, as saying that at the same energy, a proton would radiate several million times less than an electron, which is a more useful way of seeing it in practice.

[^1]: Though in extreme ultrarelativistic conditions at TeV-scale particles, it becomes primary for heavy particles too, something that the Bethe-Bloch formula alone misses! There's a number of corrections to Bethe-Bloch at both low and high energy, but this can be see by comparing the two; see below.

[^2]: $Z^{2}$ and $K$ are obvious from the Bethe-Heitler formula. The $m_{e}^{-2}$ is hidden inside the classical electron radius $r_{e}^{2}$.
