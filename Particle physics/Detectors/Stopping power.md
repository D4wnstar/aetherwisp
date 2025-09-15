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
$$S(K)=- \frac{dK}{dx} = 4\pi m_{e}c^{2}r^{2}_{e}N_{A} \frac{\rho Z}{A} \frac{z^{2}}{\beta^{2}} \ln\left( \frac{\beta^{2} \gamma^{2}m_{e}c^{2}}{h\nu} \right)$$
This is a complicated formula: see the main body for a proper description. The Bohr formula is the same, but lacks the $\beta ^{2}$ and $\delta(\gamma)/2$ terms, which are relativistic corrections.

For light particles, the behavior comes out to be much simpler and reminiscent of the classical [[Beer-Lambert law]] for [[irradiance]]:
$$S(K) = \frac{K}{L_{R}}$$
where $L_{R}$ is the **radiation length**. In fact, if you integrate for $K$, you get an exponential decay: $K(x) = K_{0} e^{-x / L_{R}}$.

Stopping power is of great importance in [[detector]] physics, since the detector picks up the energy that the particle loses and uses that to determine the presence of a particle. It's also fundamental to [[radiation protection]] to prevent [[radiation]] damage to humans and objects.

> [!question] A note on notation
> It's very common to use $E$ instead of $K$ to denote the kinetic energy. I find this notation unnecessary and confusing, since it mixes up kinetic and total energy, not to mention electric fields, so Aetherwisp uses $K$. However, in other texts be aware the $E$ is the more common letter.
## Mechanism
Stopping power is essentially a macroscopic average of microscopic interactions. As such, the stopping power is not just dependent on the incoming energy, but also on the kind of incident particle. Most discussion on stopping power is surrounding [[Electric charge|charged particles]] and their energy loss due to [[electromagnetism]], since that's the most common and most impactful [[fundamental interaction]]. In this context, there's two primary ways a particle can lose energy. [[Particle scattering]] is the obvious one: particles collide and are deflected. This is the main cause of energy loss for heavy particles. Absorption and other similar phenomena are the other. This is the main for light particles. We explore these two independently.
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
Be aware that this version is measured in $\text{MeV}/\text{g cm}$ instead of $\text{MeV}/\text{cm}$ like the normal form. The value of this form is that it makes it apparent that the collisional stopping power is actually quite independent of *both* the type of projectile *and* the material's properties. The only factors left are the value of $Z/A$, which is $\simeq0.5$ for more or less every [[chemical element]] except the superheavy ones, $z^{2}$, which as we've said is pretty much always $\pm 1$, and $\nu$, which does admittedly change a good bit between atoms, but is inside a heavily suppressed logarithmic term which is more or less a constant factor for any velocity beyond ultrarelativistic ones. The rest is all constants, with the exception of $\beta$. Basically, we can see that the mass-thickness stopping power is almost exclusively determined from the velocity of the projectile, regardless of the what the projectile even is or what it's smashing into. This is not true only for the heaviest materials like uranium and for ultrarelativistic particles. Of course, the regular stopping power also has a linear dependence on mass density, so dense materials like lead will stop much more than slim ones like carbon.

In terms of the curve it makes when plotted over speed, it's essentially $1/\beta ^{2}$ for most speeds and then transitions into $\ln(\beta ^{2}\gamma ^{2})$ for relativistic speeds when the logarithm starts dominating. See the plot further below.

> [!success] Stopping power dependence
> Collisional stopping power is almost entirely determined by the mass density of the target and the speed of the projectile. Other factors only start to matter at the absolute extremes: superheavy elements and ultrarelativistic particles. As such, the stopping power profile with respect to projectile speed is to be considered universal across almost all materials.

It might be useful to know that the first chunk of the formula is just one big constant:
$$4\pi m_{e}c^{2}r_{e}^{2}N_{A}\simeq0.3\ \frac{\text{MeV cm}^{2}}{\text{g}}$$
A more accurate version of the Bohr formula can be derived with quantum-mechanical considerations:
$$\boxed{S(K) = 4\pi m_{e}c^{2}r^{2}_{e}N_{A} \frac{\rho Z}{A} \frac{z^{2}}{\beta^{2}} \left[ \ln\left( \frac{\beta^{2} \gamma^{2} m_{e}c^{2}}{I} \right) - \beta^{2} - \frac{\delta(\gamma)}{2} \right]}$$
This is called the **Bethe-Bloch formula**. As you can see, it only differs from the Bohr formula due to the addition of two extra relativistic terms. The first, $-\beta ^{2}$, shows a noticeable stopping power reduction at high relativistic speeds ($\beta \simeq 1$). The second, $-\delta(\gamma)/2$, is dependent on a function $\delta(\gamma)$ of the relativistic $\gamma$. This term represents a density correction due to the [[dielectric polarization]] of the medium and further decreases stopping power at relativistic speeds. There is also a mass thickness variant:
$$S_\text{MT}(K) = - \frac{dK}{dX} = 4\pi m_{e}c^{2}r^{2}_{e}N_{A} \frac{\rho Z}{A} \frac{z^{2}}{\beta^{2}} \left[ \ln\left( \frac{\beta^{2} \gamma^{2} m_{e}c^{2}}{I} \right) - \beta^{2} - \frac{\delta(\gamma)}{2} \right]$$
All considerations regarding the Bohr formula apply here too, with the difference that the additional terms suppress ultrarelativistic stopping power even more than it already was.

:::image
![[Plot Stopping power collisional|80%|center]]
A plot of Bethe-Bloch stopping power with respect to projectile velocity (expressed as $\beta \gamma$). This profile is mostly universal across materials. The $x$-axis is in log10 scale.
:::

From the figure we can see that stopping power decreases to a minimum and then rises again due to relativistic effects. A particle whose velocity is just right to be in the local minimum of stopping power ($\beta \gamma \simeq 3$) is called a **minimum ionizing particle** (**MIP**).

Something interesting (and very useful) appears when we look at stopping power in terms of momentum instead of speed. Actually, it occurs for any variable dependent on speed and mass (e.g. kinetic energy; momentum just happens to be the most used). Since $p=mv$ and $v$ determines the behavior by itself, there's a "push and pull effect" between projectile mass and momentum. What I'm trying to say is that, in a plot of $S(K)$ vs. $p$ (or $S(K)$ vs. $K$), the mass *does* play a role in the profile (it needs to in order to cancel out the mass in the other variable). However, if we do manage to measure and plot $S(K)$ in terms of momentum, that means we get distinctly different curves for different masses.

:::image
![[Plot Stopping power collisional for p|80%]]
A stopping power plot in terms of kinetic energy for a [[kaon]] and a [[proton]].
:::

This is extremely useful, because it provides us with a way to discriminate between different particles. Since mass is essentially the only property that's truly unique to each particle, by plotting out these curves experimentally, we can measure the mass of the particle indirectly. If we recognize the mass, then we've identified the particle!

Note that for larger masses, the plot gets [[translation|shifted]] to the right, meaning it generally loses more energy as the minimum gets pushed further into relativistic territory. The difference is biggest in low-energy, nonrelativistic range.
#### Energy straggling
The energy loss due to many collisions is inherently random. If the incident beam is monoenergetic, meaning all incident particles have the same energy, the energy loss distribution is found to be a [[Poisson distribution]]. As per the [[central limit theorem]], when the number of collisions is large (i.e., the material is sufficiently thick), the energy loss distribution becomes a [[Gaussian distribution|Gaussian]]. This phenomenon is known as **energy straggling**. In thin materials, where the central limit theorem does not apply, we find [[Landau-Vavilov distribution]] instead, which has a high tail for high-energy losses.

If the material is thick enough, the stopping power might cause the particle to lose all of its energy and get "stuck" in the material. Since the energy loss is random, so is the distance at which it happens. We call this the **[[Range]]** of the particle and its randomness is called **range straggling**.
### Radiative energy loss  
The stopping power for [[electron|electrons]] is not well described by the Bethe-Bloch formula. This is because electrons in the beam are identical to those in the target, and their mass is very small. The Bethe-Bloch formula is valid only for heavy particles. For electrons, energy loss is dominated by [[Bremsstrahlung|Bremsstrahlung radiation]]. This loss mechanism is negligible for heavy particles because their deflections are minimal.

Radiative energy loss for a particle of energy $E_{0}$ follows a form of the [[Beer-Lambert law]]:

$$
- \left.\frac{dE}{dx}\right|_{\text{rad}} = \frac{E}{L_{R}}
$$

leading to:

$$
E(x) = E_{0} e^{-x / L_{R}}
$$

with

$$
L_{R}^{-1} = \ln\left( \frac{183}{Z^{1/3}} \right) \frac{4 r_{0}^{2} N_{A} Z^{2} \alpha \rho}{A}
$$

where:
- $r_{0}$ is the classical radius of the electron.
- $N_A$ is the [[Avogadro number]].
- $\alpha$ is the [[Fine-structure constant]].
- $\rho$ is the material's density.
- $Z$ is the atomic number.
- $A$ is the atomic mass.

$L_{R}$ is the **radiation length**, the distance over which the electron’s energy decreases to $1/e$ of its initial value. It strongly depends on the atomic number of the material.

The energy loss due to Bremsstrahlung is exponential, and at high energies, it dominates over ionization. At low energies, ionization is more significant. The energy at which both processes contribute equally is known as the **critical energy** $E_C$.

![[Stopping power and radiation|80%|center]]  
*The $x$-axis is in log10 scale*

Some examples of $L_{R}$ for various materials are: 3.6 cm for $H_{2}O$, 9 cm for $Al$, 1.7 cm for $Fe$, and 0.56 cm for $Pb$. This explains why lead is such an effective shield.

The [[Photon|photon]] [[Energy spectrum|energy spectrum]] emitted via Bremsstrahlung ranges from 0 to $E_{0}$, with an average angular deviation $\left\langle \theta \right\rangle \simeq mc^{2}/E_{0}$, independent of the photon’s energy. The critical energy is approximately $E_C \sim 600/Z$ MeV.

For a particle of mass $M$, the Bremsstrahlung energy loss scales as $\propto 1/M^{2}$. This means that radiative losses are significant only for very light particles (such as electrons) or at extremely high energies (ultrarelativistic regime).