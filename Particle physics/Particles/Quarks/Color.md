---
wiki-publish: true
aliases:
  - color charge
  - quark shower
---
**Color**, often called **color charge**, is the physical property of a [[quark]] or [[gluon]] that causes it exhibit [[strong interaction]]. It is the fundamental quantity in the theory of [[quantum chromodynamics]] (QCD) and underlies much of the behavior of [[hadron|hadrons]].

Color value determines how a colored particle interacts with other colored particles. In many ways, color is to the strong force what [[electric charge]] is to [[electromagnetism]], but now there's three of them. This is why it's also called color charge.

Color is a new [[Degrees of freedom|degree of freedom]] and [[quantum number]] for quarks and gluon and it exists in three varieties: **red**, **green** and **blue**. There are also three anticolors for antiquarks which are named after the opposites of three normal colors: **antired**, **antigreen** and **antiblue**. They can be represented as a 3-vector:
$$r=\begin{pmatrix}
1 \\ 0 \\ 0
\end{pmatrix},\qquad g=\begin{pmatrix}
0 \\ 1 \\ 0
\end{pmatrix},\qquad b=\begin{pmatrix}
0 \\ 0 \\ 1
\end{pmatrix}$$
The color state of a hadron is the joint color state of all valence quarks. A couple of examples:
$$\ket{r\bar{r}}\text{ (red-antired meson)},\quad \ket{rgb} \text{ (red-green-blue baryon)} $$
Hadrons must always have net zero color, meaning that not all combinations of internal color charges are allowed, only those that sum to zero net color. For instance, the only allowed color states of a [[meson]]'s quarks are $\ket{r\bar{r}}$, $\ket{g\bar{g}}$ or $\ket{b\bar{b}}$.
### History and discovery
The two common quarks are up and down. They were the first to be discovered (alongside strange) and are by far the most common. All ordinary [[matter]] is composed of ups and downs due to [[proton|protons]] and [[neutron|neutrons]] being made of these. However, there's a fundamental problem. Theoretical estimates of the mass of these two leads to tiny masses: 2 to 5 [[Electronvolt|MeV]] to be exact. But then how come protons and neutrons, being made of only three of these, can have masses nearly 1000 MeV strong? That's nearly a 100 times difference!

Estimating quark mass is incredibly difficult. Quarks make up hadrons and are not found in isolation, so there's no hope of, say, cracking a proton and measuring its quarks one by one. Thus, we're stuck with either theoretical formulas or computer simulations, both of which are limited by our understanding of nature.

Another related problem is the very existence of the $\Delta^{++}$ [[delta resonance]]. It's supposed to be made of three up quarks ($uuu$), but it's really hard to fit in a simplistic view of the quark model. To see why, consider the three components of its ground state [[wavefunction]] (spatial, spin, flavor):
- It is the lightest [[baryon]] with no ground state orbital angular momentum, so the spatial component is [[Permutation operator|symmetric]] under quark exchange.
- It is a spin 3/2 fermion made of three 1/2 quarks. The quarks must therefore all be spin-aligned (to sum to 3/2), so exchanging quarks leaves the state unchanged: $\ket{\uparrow\uparrow\uparrow}\to\ket{\uparrow\uparrow\uparrow}$. The spin component is symmetric.
- It is a baryon made of three identical quarks, so of course reordering the quarks doesn't change the state: $\ket{uuu}\to \ket{uuu}$. The flavor component is then also symmetric.

But then all components are symmetric and thus so is the entire wavefunction
$$\psi _{\Delta^{++}}=\psi _\text{spatial}\psi _\text{spin}\psi _\text{flavor}\quad\text{(symmetric)}$$
But fermions can't be symmetric, that's the whole definition! It's a violation of the [[Pauli exclusion principle]]. The $\Delta^{++}$ would have to be a boson for this to be true, but we know that's not true. There must be something missing, a phantom component that we don't observe but must be there.

This new component is called **color**. It is a new [[quantum number]] and the fourth and final piece to the quark puzzle. It is an additional [[degrees of freedom|degree of freedom]] that's unique to strong-interacting particles and in fact determines the interaction itself. Critically, the color component is *antisymmetric*, which makes the new wavefunction antisymmetric
$$\psi _{\Delta^{++}}=\psi _\text{spatial}\psi _\text{spin}\psi _\text{flavor}\psi _\text{color}\quad\text{(antisymmetric!)}$$
Color also serves to explain the mass problem, though the reason why is much more complicated. See [[#Quark dynamics and hadron structure]] below for more.
### Proof of existence
Whereas the electric charge's existence is "obvious", quarks are subatomic [[particle|particles]] that are (mostly) impossible to isolate, so while color as a theoretical object certainly sounds nice, proving its existence is a whole problem of its own. Thankfully, there's not one, but two ways of proving it exists empirically.
#### Electron-positron collisions
The first way is to study the initial and final [[stato|states]] of electromagnetic interactions like $e^{-}+e^{+}\to \mu^{-}+\mu^{+}$, which, from the perspective of quantum numbers, are almost equivalent to processes like $e^{-}+e^{+}\to q+\bar{q}$.[^1] The only real differences are that quarks have different electric charge from [[muon|muons]] and that quarks should have color.

We start by calculating the [[cross section]] of these processes. In the first process, the cross section is proportional to $\sqrt{ \alpha }$, with $\alpha$ the [[Fine-structure constant|electromagnetic coupling constant]]. In the second, the cross section is not only dependent on $\alpha$ but also to this presumed color-related dependency, $\sqrt{ \alpha }\cdot\text{color}$. We can measure these two cross sections and then take their ratio to find the color proportionality. This ratio $R$ leads to a new color-related dependency that comes out to be directly proportional to the squares of quark fractional charges $Q_{q}$:
$$R=\frac{\sigma(e^{+}+e^{-}\to q+\bar{q})}{\sigma(e^{+}+e^{-}\to \mu^{+}+\mu^{-})}=N_{C}\sum_{q}Q_{q}^{2}$$
where $N_{C}$ is a constant of proportionality representing the number of colors. The sum goes over all quarks that are energetically allowed by the [[center-of-mass energy]] of the process. Being unable to study quarks independently, we must sum the charge components over all possible colors and in so doing. $N_{C}$ can then be measured experimentally.

The process that generates $q+\bar{q}$ creates a new meson of neutral charge when the quark pair combines. Regardless of the type of meson created, this process is seen experimentally and all data collected from these reactions that is [[Parameter estimation|fit]] with the proportionality factor  ends up returning a value of 3; precisely the number of colors.
#### Pion decay
The second way is essentially the first but in reverse. Instead of creating quarks, we're destroying them. Start with a $\pi^{0}$ neutral [[pion]]. This is known to decay in two [[Photon|photons]] as per
$$\pi^{0}\to \gamma+\gamma$$
This process is deceptively difficult and the [[Feynman diagram]] for it involves some rather confusing physics. Suffice to say that the two quarks that make up $\pi^{0}$ distribute themselves in a time loop of 2 up quarks and a down quark, which will interact electromagnetically to emit two photons.

If color truly exists, then this decay must have *some* relation to it, considering that quarks are involved. This is a decay, so the "cross section" is its [[Breit-Wigner distribution|decay width]]. We know that like the cross section it is proportional to the [[matrix element]] of the [[state transition]]:
$$\Gamma \propto \lvert \braket{ \psi_{f} | \mathcal{M}_{fi} | \psi_{i} }  \rvert ^{2}$$
This is measured to be
$$\Gamma(\pi^{0}\to2\gamma)=f_{\pi} \frac{N_{C}}{\sqrt{ 2 }}\left( \frac{4}{9}e^{2}- \frac{1}{9}e^{2} \right)$$
where $f_{\pi}$ is the pion decay *constant*, $N_{C}$ is the number of colors and the parenthesis is related to the quark electric charge. Inverting to extract $N_{C}$ and measuring $\Gamma$ experimentally ($\Gamma _\text{exp}=(7.7\pm 0.6)\text{ eV}$) yields
$$N_{C}=2.99\pm 0.12$$
Perfectly compatible with 3.
### Quark dynamics and hadron structure
Color is key to understanding the strong interaction. Quarks "talk" to each other through gluons, the [[force carrier]] of the strong force. Since quarks confined inside of a hadron as in constant interaction, we can readily assume that there's a constant stream of gluons within the hadron. Strong force being, well, strong, these would carry a considerable amount of energy which is an inherent part of the hadron but is unaccounted for by individual the quarks that make it up. The fact is, hadron internal structure is a lot weirder than it might seem.

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
