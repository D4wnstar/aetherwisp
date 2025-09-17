---
wiki-publish: true
aliases:
  - color charge
  - quark shower
---
**Color**, often called **color charge**, is the physical property of a [[quark]] that causes it exhibit [[strong interaction]]. It is the fundamental quantity in the theory of [[quantum chromodynamics]] (QCD) and underlies much of the behavior of [[hadron|hadrons]].

Color is a new [[Degrees of freedom|degree of freedom]] and [[quantum number]] for quarks and it exists in three kinds: **red**, **green** and **blue**. There are also three opposite colors for antiquarks which, as anyone who's studied art and color theory can confirm, are of course **antired**, **antigreen** and **antiblue**. They can be represented as a 3-vector:
$$r=\begin{pmatrix}
1 \\ 0 \\ 0
\end{pmatrix},\qquad g=\begin{pmatrix}
0 \\ 1 \\ 0
\end{pmatrix},\qquad b=\begin{pmatrix}
0 \\ 0 \\ 1
\end{pmatrix}$$
Color may be positive or negative and its type and value determines how a quark interacts with other quarks. In many ways, color is to the strong force what [[electric charge]] is to [[electromagnetism]], but now there's three of them. This is why it's called color charge.
### Proof of existence
Whereas the electric charge's existence is "obvious", quarks are subatomic [[particle|particles]] that are impossible to isolate, so while color as a theoretical object certainly sounds nice, proving its existence is a whole problem of its own. Thankfully, there's not one, but two ways of proving it exists.
#### Electron-positron collisions
The first way is to study the initial and final [[stato|states]] of electromagnetic interactions like $e^{-}+e^{+}\to \mu^{-}+\mu^{+}$, which, from the perspective of quantum numbers, are equivalent to processes like $e^{-}+e^{+}\to q+\bar{q}$.[^1] We start by calculating the [[cross section]] of these processes. In both vertices of the first process, the cross section is proportional to $\sqrt{ \alpha }$, with $\alpha$ the [[fine-structure constant]]. In the second, the cross section is by hypothesis also dependent on color, $\sqrt{ \alpha }\cdot\text{color}$. We can measure the ratio between these two cross sections, which leads to a new color-related dependency $R$ that comes out to be directly proportional to the sum of the squares of quark charges:
$$R=\frac{\sigma(e^{+}+e^{-}\to \mu^{+}+\mu^{-})}{\sigma(e^{+}+e^{-}\to q+\bar{q})}=N_{C}\sum_{q}Q_{q}^{2}$$
- [ ] where $N_{C}$ is the constant of proportionality, representing the number of colors. Being unable to study quarks independently, we must sum the charge components over all possible colors and in so doing,  just happens to be 3. Precisely the number of colors.

The process that generates $q+\bar{q}$ creates a new [[meson]] of neutral charge. Regardless of the type of meson created, this process is seen experimentally and all data collected from these reactions that is [[Parameter estimation|fit]] with a proportionality factor $R$ ends up returning 3. Thus, both theory and experiment agree that the proportionality between electric charge and color charge must be 3 (colors).
#### Pion decay
The second way is essentially the first but in reverse. Instead of creating quarks, we're destroying them. Start with a $\pi^{0}$ neutral [[pion]]. This is known to decay in two [[photon|photons]] as per
$$\pi^{0}\to \gamma+\gamma$$
This process is deceptively difficult and the [[Feynman diagram]] for it involves some rather confusing physics. Suffice to say that the two quarks that make up $\pi^{0}$ distribute themselves in a time loop of 2 up quarks and a down quark, which will interact electromagnetically to emit two photons.

If color truly exists, then this decay must have *some* relation to it, considering that quarks are involved. This is a decay, so the "cross section" is its [[Breit-Wigner distribution|decay width]]. We know that like the cross section it is proportional to the [[matrix element]] of the [[state transition]]:
$$\Gamma \propto \lvert \braket{ \psi_{f} | \mathcal{M}_{fi} | \psi_{i} }  \rvert ^{2}$$
This is measured to be
$$\Gamma(\pi^{0}\to2\gamma)=f_{\pi} \frac{N_{C}}{\sqrt{ 2 }}\left( \frac{4}{9}e^{2}- \frac{1}{9}e^{2} \right)$$
where $f_{\pi}$ is a multiplicative factor, $N_{C}$ is the number of colors and the parenthesis is related to the quark electric charge. Inverting to extract $N_{C}$ and measuring $\Gamma$ experimentally ($\Gamma _\text{exp}=(7.7\pm 0.6)\text{ eV}$) yields
$$N_{C}=2.99\pm 0.12$$
Perfectly compatible with 3.
### Quark dynamics and hadron structure
Color is key to understanding the strong interaction. Quarks "talk" to each other through [[gluon|gluons]], the [[force carrier]] of the strong force. Since quarks confined inside of a hadron as in constant interaction, we can readily assume that there's a constant stream of gluons within the hadron. Strong force being, well, strong, these would carry a considerable amount of energy which is an inherent part of the hadron but is unaccounted for by individual the quarks that make it up. The fact is, hadron internal structure is a lot weirder than it might seem.

The two or three quarks we know to make up the hadron are called **valence quarks**. They are the primary inhabitants of the hadrons, but are *not the only ones*. The storm of gluons we mentioned before are more inhabitants, but there's a third piece: the [[Disuguaglianza di Heisenberg|uncertainty principle]] allows for particles to pop in and out of existence as long as they do so below the [[Planck units|Planck time]] and it also permits [[Pair production]] from the [[quantum vacuum]]. Quarks, like [[Electron|electrons]], are light enough that they can be pair produced from thin air. The energy-dense environment of the inner hadron provides a perfect environment for this to happen and happen it does, to an *extreme* degree. Quark-antiquark pairs are constantly being produced and reabsorbed in the vacuum, making it so the inner hadron is less like two or three quarks bound to each other and more like three islands trying to stay afloat in a stormy sea of quark pairs. This background is called the **quark sea** and it is the third and final inhabitant of the hadron.

To recap, a hadron's energy budget is spent on three things:
1. The valence quarks, which take up a ludicrously small fraction of the total mass;
2. The gluon streams;
3. The sea quarks.

Only when you combine all three do you get sensible mass predictions. Quarks interact between themselves through something we'll call QCD potential $V_\text{QCD}$ which, just like color, is suggestive but not quite the same as the [[electric potential|electromagnetic equivalent]]. It takes the form
$$V_\text{QCD}=- \frac{4}{3} \frac{\alpha_{S}}{r}+kr$$
$\alpha_{S}$ is the strong coupling constant. If color charges being three instead of wasn't already confusing, let me point your attention to how there's a positive and negative component: this means that the *same* color charge can be both repulsive *and* attractive at the same time, with distance being the only factor that determines which is more powerful. This means that the potential increase linearly at a distance ($kr$, a [[Harmonic oscillator|Hooke's law]]-like term) and decreases like a Coulomb potential when close ($- \frac{4}{3} \frac{\alpha_{S}}{r}$). Moreover, because the potential *increases* with distance (unlike literally any other non-strong potential in the universe), this means that there's a distance threshold over which the potential grows so large it permits pair production: the spring breaks and becomes two smaller springs. This is similar to how breaking a magnet doesn't make a north and south magnet, it just makes two smaller magnets by "creating a new pair of poles".

As the distance grows, more and more pairs are produced, something called a **quark shower**. This shower stops when the individual quarks that make it up find a bound state to settle in. A bound state of quarks is just a hadron though, so the shower stops when quarks start to form hadrons: this process is called **[[hadronization]]** and it happens spontaneously. The consequence is staggering: quarks "refuse" to remain free and spontaneously combine into hadrons to always be in a bound state. This impossibility of finding free-roaming quarks is called **[[quark confinement]]** and is the reason why quarks are so hard to work with.

Now, recall how the potential was made of two pieces. When the positive "spring" potential grows large, it triggers a quark shower, hadronization and eventual confinement. For this reason, the region where the potential is positive and large enough to do this is called the **confinement zone**. But when the negative potential is large, the whole potential goes subzero. In here, as $r\to 0$, potentials are less and less bound to each other, with diminishing interactions, until they become completely null: this low-distance region is called the **[[asymptotic freedom]] zone**.

The variable strength of interaction is reflected by the fact that the strong coupling constant $\alpha_{S}$ is, in fact, not constant. It depends on the distance (or energy, it's equivalent). When $r\to 0$, $\alpha_{S}\to 0$ and when $r\to \infty$, $\alpha_{S}$ grows large, though due to hadronization it's never allowed to go infinite. Energy behavior is the converse: when $E\to \infty$, $\alpha_{S} \to0$ and when $E\to 0$ then hadronization occurs. This has major cosmological implications, as in the first instants of the [[Universe]], after the [[Big Bang]], energy must have been globally high enough for all existing quarks to be well into the asymptotic freedom zone, meaning quark confinement just wasn't a thing back then.

[^1]: Don't be fooled by the fact that we're talking about quarks and color: both of these are electromagnetic interactions. There's no strong interactions here.
