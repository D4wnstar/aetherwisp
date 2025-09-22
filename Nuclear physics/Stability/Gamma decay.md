---
wiki-publish: true
aliases:
  - gamma ray
---
**Gamma decay** is a [[Nuclear decay|decay]] mode in which an excited [[Atomic nucleus|nucleon]] drops to a less energetic [[stato|state]] by emitting a [[Photon]]. It is essentially just a [[state transition]] of a nucleon from a higher [[Stationary state|energy eigenstate]] to a lower one. As such, the [[energy]] of the photon equals the difference in energy between states, however it is reduced by a small [[Atomic nucleus|nucleus]] recoil term. It often follows [[Alpha decay|alpha]] or [[Beta decay|beta]] decay, which generally leave one or more nucleons in an excited state.

The nuclear process is
$$\ce{X^{*}}\to \ce{X}+\gamma$$
where $\ce{X}$ is a [[nuclide]] and the asterisks denotes that it is in an excited state. $\gamma$ represents a photon.

Photons emitted by gamma decay are called **gamma rays**. Their energy is extremely high, often in the order of hundreds of [[Electronvolt|keV]] to several MeV, and they comprise the most energetic part of the [[Electromagnetic radiation|electromagnetic spectrum]]. More generally, "gamma ray" refer to any photon in this range of energy. The majority of gamma rays observed on Earth are due to gamma decay, [[cosmic ray|cosmic rays]] or artificially generated due to [[particle accelerator]] collisions.

Like all state transitions that emit a photon, gamma decay is governed by [[electromagnetism]].
### Energy conservation
Consider some nucleus of mass $M$ at rest. It gamma decays from an initial energy eigenstate $E_{i}$ to $E_{f}$. Most of this energy is emitted through a photon, which will carry most of the energy of the decay. We'll call this $E_{\gamma}$. However, since the nucleus is not being held in place, it will suffer some recoil, so the total decay energy is split between the photon and the nuclear recoil because [[Linear momentum|momentum]] must be conserved. Since the nucleus is quite heavy, it's fair to assume that the recoil's [[kinetic energy]] is not [[Lorentz transformation|relativistic]], so we'll call it
$$K_{R}=\frac{p^{2}_{R}}{2M}$$
The conservation of energy and momentum give
$$\begin{cases}
E_{i}=E_{f}+E_{\gamma}+K_{R}\\[2pt]
0=\mathbf p_{R}+\mathbf p_{\gamma}
\end{cases}$$
The bottom simply solves to $\mathbf p_{R}=-\mathbf p_{\gamma}$. In the top equation, we can define $\Delta E\equiv E_{i}-E_{f}$ and use the photon energy $E_{\gamma}=cp_{\gamma}$[^1] to state
$$\Delta E=E_{\gamma}+ \frac{(-p_{\gamma})^{2}}{2M}=E_{\gamma}+\frac{E_{\gamma}^{2}}{2Mc^{2}}$$
This is a quadratic equation in $E_{\gamma}$. Using the quadratic formula gives
$$E_{\gamma}=Mc^{2}\left[ -1\pm\sqrt{1+ \frac{2\Delta E}{Mc^{2}}} \right]$$
Now, we know that $\Delta E$ is in the [[Electronvolt|MeV]] range whereas the nuclear [[Relativistic energy|rest energy]] $Mc^{2}$ is in the GeV range, so we can afford to consider $\Delta E/Mc^{2}$ to be quite small. Approximate the root with the [[Binomial theorem|binomial expansion]] to first order $\sqrt{ 1+x }\simeq 1+x/2$:
$$\sqrt{ 1+ \frac{2\Delta E}{Mc^{2}} }\simeq 1+ \frac{\Delta E}{Mc^{2}}$$
so
$$E_{\gamma}=Mc^{2}\left[ -1\pm 1\pm \frac{\Delta E}{Mc^{2}} \right]=\begin{cases}
\Delta E & (+) \\
-2Mc^{2}- \Delta E & (-)
\end{cases}$$
$\Delta E$ is positive by definition (since in gamma decay $E_{f}<E_{i}$), the minus case would lead to a guaranteed negative photon energy, which makes no sense. Thus, only the positive case is physically valid and we are left with
$$\boxed{E_{\gamma}\simeq\Delta E}$$
This proves that the photon carries nearly all of the decay energy. If we held on to the second term of the square root
$$\sqrt{ 1+ \frac{2\Delta}{Mc^{2}} }\simeq 1+ \frac{x}{2}- \frac{x^{2}}{8}$$
We'd have gotten
$$E_{\gamma}\simeq \Delta E- \frac{(\Delta E)^{2}}{2Mc^{2}}$$
The second term is the recoil correction:
$$\boxed{K_{R}= \frac{(\Delta E)^{2}}{2Mc^{2}}}$$
This is tiny: usually in the order somewhere between and 1 and 100 electronvolts. Nevertheless, it's not insignificant. On the higher end, $100\text{ eV}$ recoils can displace an [[atom]] is a solid state [[crystal]] which can break things at an atomic level. This is commonly known as **radiation damage**.
### Selection rules
Gamma decay results in the emission of [[electromagnetic radiation]] from a nucleus. We can describe this radiation as a superposition of known radiation shapes, namely regarding the polarity of the radiation. We know that radiation from an arbitrary source can be described as a [[multipole expansion]] containing a monopole term, a dipole term, a quadrupole term, etc. Each of these has a characteristic angular distribution, which we can use as a [[basis]] to express any form of radiation.

Electric radiation arises from the variation of the [[Electric charge|charge]] distribution inside the nucleus. Magnetic radiation instead arises from the variation of nuclear magnetic moment, be it orbital [[angular momentum]] or [[spin]]. Within the nucleus, angular momentum (and by extension spin and hence [[parity]]) must be conserved. This conservation requirement forbids some transitions and allows some others: we call **selection rules** the set of rules we use to determine which transitions are allowed.

Consider some gamma decay transition that takes a nucleus from $J_{i}^{P_{i}}$ to $J_{f}^{P_{f}}$. From conservation of angular momentum I have
$$\mathbf{J}_{i}=\mathbf{J}_{f}+\mathbf{L}_{\gamma}$$
since the photon being emitted may very well carry away some of the angular momentum of the nucleus, written $\mathbf{L}_{\gamma}$. The angular momentum depends on the transition. If $L$ is the order of the multipole operator ($L=1$ is dipole, $L=2$ is quadrupole, etc.), the photon is passed $L\hbar$ angular momentum. $L$ may not be zero because a pure monopole (resting point charge) cannot emit radiation.

The values of $L$ give the set of multipole terms that describe the radiation. According to conservation of momentum, the allowed values of $L$ satisfy
$$|J_{i}-J_{f}|\leq L\leq J_{i}+J_{f}$$
For instance, if we start from $J_{i}=3/2$ and end up in $J_{f}=5/2$, the possible transitions are $L=1,2,3,4$. This means that the actual radiation being emitted is some [[linear combination]] of these four terms (dipole, quadrupole, octopole, hexadecapole).

The parity difference instead tells us whether each pole is electric or magnetic. Electric transitions produce photons with parity given by $P_{\gamma}(\text{EL})=(-1)^{L}$ (same parity as $L$) and magnetic transitions have $P_{\gamma}(\text{ML})=(-1)^{L+1}$ (opposite of $L$)[^2]. The total parity must be conserved, so
$$P_{i}=P_{f}\cdot P_{\gamma}(\text{EL or ML})$$
The transition parity supplies the difference between the start and end states, so if nothing changes, you must only pick even-parity transitions ($P_{\gamma}=1$), and if the parity flips, you must only pick odd-parity transitions ($P_{\gamma}=-1$). This results in odd poles being magnetic and even ones being electric if $P_{i}=P_{f}$ and vice versa if $P_{i}\neq P_{f}$. In the previous example, if $P_{i}=P_{f}$, then our $L=1,2,3,4$ transitions become $M_{1},E_{2},M_{3},E_{4}$, but if $P_{i}\neq P_{f}$ they become $E_{1},M_{2},E_{3},M_{4}$.

So to summarize, the selection rules are
1. Gamma radiation is the linear combination of all multipole terms $L$ allowed by $\lvert J_{i}-J_{f} \rvert\leq L\leq J_{i}+J_{f}$, excluding $L=0$.
2. If parity doesn't change, odd poles are electric and even ones are magnetic. If parity changes, odd poles are magnetic and even ones are electric.

> [!example]- Cesium decay
> Cesium-137 [[Beta decay|beta minus decays]] into barium-137 as per
> $$\ce{^{137}Cs}\to \ce{^{137}Ba^{*}}+e^{-}+\bar{\nu}_{e}$$
> $\beta^{-}$ leaves barium in an excited state about 94.4% of the time. It then proceeds to gamma decay into its ground state as per
> $$\ce{^{137}Ba^{*}}\to \ce{^{137}Ba}+\gamma$$
> The excited state is $J^{P}_{i}=\frac{11}{2}^{-}$. The ground state is $J^{P}_{f}=\frac{3}{2}^{+}$. The angular momentum difference determines that the allowed poles are $L=4,5,6,7$. The parity flip then tells us that odds are magnetic and evens are electric. Thus, the gamma radiation produced by this decay is a linear combination of $M_{4},E_{5},M_{6}$ and $E_{7}$.

There's an edge case in the rules: if $J_{i}=J_{f}$, then $L=0$ only. But that's not permitted. In such transitions (which are observed), $L=1$.

Moreover, not all poles are made equal. The behavior of the poles can be succinctly summarized in a few statements
1. The lowest-pole radiation dominates.
2. Electric multipole emission is about 100 times more [[Probability|probable]] than the same-order magnetic.  
3. Emission of order $L+1$ is $\sim 10^{-5}$ times less likely than the previous order $L$.  

Points 2 and 3 can be combined to state:
$$\frac{\text{Prob}(\text{EL}+1)}{\text{Prob}(\text{ML})}=\frac{\text{Prob}(\text{EL}+1)}{\text{Prob}(\text{EL})} \frac{\text{Prob}(\text{EL})}{\text{Prob}(\text{ML})}\simeq 10^{-3}$$
and
$$\frac{\text{Prob}(\text{ML}+1)}{\text{Prob}(\text{EL})}=\frac{\text{Prob}(\text{ML+1})}{\text{Prob}(\text{ML})} \frac{\text{Prob}(\text{ML})}{\text{Prob}(\text{EL})}\simeq 10^{-7}$$
To be clear, this are very rough order-of-magnitude estimates. The probabilities here essentially express the 

[^1]: This follows from the [[Planck formula]] $E=\hbar \omega$ and the [[Formula di de Broglie|de Broglie formula]] $p=\hbar/k$.

[^2]: If you're confused at the physical origin of these, then don't worry, you're not going crazy. The origin comes from deeper in quantum field theory, specifically regarding the properties of the photon field. You should feel free to take these as a given.
