---
wiki-publish: true
aliases:
  - electron capture
  - beta plus decay
  - beta minus decay
---
**Beta decay** is a mode of [[Nuclear decay|decay]] in which a [[Atomic nucleus|nucleus]] corrects an excess of [[proton|protons]] or [[neutron|neutrons]] by converting one into the other. The conversion can occur in both directions, known as $\beta^{+}$ and $\beta^{-}$:
$$\begin{align}
\beta^{+}\text{ decay:}\quad &p\to n+e^{+}+\nu_{e}\\
\beta^{-}\text{ decay:}\quad &n\to p+e^{-}+\bar\nu_{e}
\end{align}$$
where $e^{-}$ is an [[electron]], $e^{+}$ a [[Electron|positron]] and $\nu_{e}$ and $\bar{\nu}_{e}$ are [[neutrino|electron neutrinos]] and antineutrinos respectively.

There exists a third process associated with $\beta$ decay called **electron capture** (**EC** for short):
$$\text{EC:}\quad p+e^{-}\to n+\nu_{e}$$
Electron capture does exactly what the name suggests: it captures an electron, typically from an inner [[electron shell model|electron shell]], and consumes it to convert a proton into a neutron.

$\beta$ decay is governed by the [[weak interaction]]. Specifically, it consists of the emission of a [[W boson]] from an [[up quark|up]] or [[down quark]], converting it to the other flavor and therefore converting a proton into a neutron or viceversa. The W boson then [[particle decay|decays]] into an electron/antineutrino or positron/neutrino pair depending on its charge.

Since $\beta$ decay is a conversion process and does not change the number of nucleons, the decay products are guaranteed to be [[Isobar|isobars]].

Examples of $\beta$ decays include:
- $\beta^{-}$: $\ce{_{53}^{131}I_{78}}\ \to\ \ce{_{54}^{131}Xe_{77}}$ with a [[half-life]] of $t_{1/2}=8.0\text{ d}$.
- $\beta^{+}$: $\ce{_{13}^{25}Al_{12}}\ \to\ \ce{_{12}^{25}Mg_{13}}$ with a half-life of $t_{1/2}=7.2\text{ d}$.
- EC:  $\ce{_{25}^{54}Mn_{29}}\ \to\ \ce{_{24}^{54}Cr_{30}}$ with a half-life of $t_{1/2}=312\text{ d}$.
## Mechanisms
There are three decay processes that need to analyzed: $\beta^{+}$, $\beta^{-}$ and EC. $\beta^{+}$ and $\beta^{-}$ largely work the same way and can be treated in unison. EC require its own section.
### $\beta^{+}$ and $\beta^{-}$
Start by writing the [[semi-empirical mass formula]] as
$$M(Z,A)=\alpha A-\beta Z+\gamma Z^{2}+\delta$$
where
$$\begin{align}
\alpha&=m_{n}-a_{v}+a_{s}A^{-1/3}+\frac{a_{a}}{4}\\[2pt]
\beta&=a_{a}+(m_{n}-m_{p}-m_{e})\\[2pt]
\gamma&=\frac{a_{a}}{A}+\frac{a_{c}}{A^{1/3}}
\end{align}$$
This allows us to factor terms based on their proton count and this is useful because $\beta$ decay occurs among isobars, so we can take $A$ to be constant. The only variable in $\beta$ decay is $Z$ (since $N$ is given by $N=A-Z$). Then, $\alpha,\beta,\gamma$ and $\alpha A$ are also all constants. Two different behaviors can be identified based on the parity of $A$:
- If $A$ is odd, then $M(Z)$ draws a single [[parabola]].
- If $A$ is even, then $M(Z)$ draws two distinct parabolas, one for even-even nuclei and one for odd-odd nuclei. This is due to the behavior of the $\delta$ term which inverts sign depending on whether a nucleus is even-even or odd-odd. The odd-odd parabola lies $2\delta$ above the even-even one.

In both cases, the parabola has a minimum at $Z=\beta/2\gamma$.

Note that the mass $M$ is the [[atom]] mass, not the nucleus mass. This is an important distinction because atomic mass automatically takes the created electron/positron into account. Neutrino masses are negligible.

:::image
![[Plot Beta decay odd A|90%]]
Decay behavior of $A=101$ isobars. The parabola minimum corresponds with $\ce{_{44}Ru}$, to which all the other isobars converge to. Isobars with too few protons create new ones with $\beta^{-}$ at the expense of protons. Conversely, ones with too many convert them into neutrons with $\beta^{+}$.
:::

:::image
![[Plot Beta decay even A|90%]]
Decay behavior of $A=106$ isobars. The lower parabola shows even-even nuclei, the upper one odd-odd nuclei. The minimum corresponds with $\ce{_{46}Pd}$. Each $\beta$ decay jumps from one parabola to the other. Notice how $\ce{_{48}Cd}$ also happens to be a *local* minimum to $\ce{_{47}Ag}$ and $\ce{_{49}In}$ and ends up being stable too. This is allowed by the $2\delta$ energy difference between the two parabolas, making it possible for there to be local minima on top of a global one. It is possible, albeit extremely rare, for $\ce{_{48}Cd}$ to decay into $\ce{_{46}Pd}$ through double $\beta^{+}$ decay.
:::
### Electron capture
Because of the [[Disuguaglianza di Heisenberg|uncertainty principle]], an electron always has a non-zero [[probability]] of being found inside the nucleus. As such, there is always a non-zero probability of an interaction between the electron and a proton. Since the mass of the proton is slightly smaller than that of the neutron, it's possible for a proton and electron to "merge" to form a neutron, emitting a neutrino as a byproduct.

Electron capture is more probable for heavy nuclei, as bigger nuclei get closer and closer to the innermost electron shell. As one might expect, captured electrons come almost exclusively from inner shells ($1s$, $2p$, etc.), as they are the closest to the nucleus. The hole left in the shell due to the capture causes a cascade of [[State transition|state transitions]] as higher-shell electrons "fall" to lower shells to fill the hole. This results in a cascade of X-ray [[photon|photons]] being released jointly with the EC event.

You might notice that $\beta^{+}$ and EC result in the same outcome: one proton is converted to one neutron. This is quite relevant, as the two modes compete energetically, meaning that one of the two (the most energetically efficient one) is going to occur more often than the other despite having the same effect. The condition for EC to happen is simply
$$M(A,Z)>M(A,Z-1)-B_{e^{-}}$$
under the assumption that $M$ is the *atomic* mass and not the nuclear mass. $B_{e^{-}}$ is the binding energy of the electron that's captured. We'll pretend it doesn't exist for now, but see [[#Electron capture in the nucleus]] for more. Meanwhile, the condition for $\beta^{+}$ is
$$M(A,Z)>M(A,Z-1)+2m_{e}c^{2}$$
There's an additional $2m_{e}c^{2}$ that comes due to the creation of the positron (one $m_{e}c^{2}$) and due to one electron being lost from a shell since one proton was removed and the charge is imbalanced (the other $m_{e}c^{2}$). Thus, EC is about $2m_{e}c^{2}\simeq 1\text{ MeV}$ more energy-efficient than $\beta^{+}$. When the difference between $M(A,Z)$ and $M(A,Z-1)$ is less than $1\text{ MeV}$, $\beta^{+}$ is completely suppressed, whereas EC is allowed: in these [[Nuclide|nuclides]], EC is the only way that protons can be converted into neutrons. In all others, both processes can occur, but the [[branching ratio]] of EC is pretty much always higher than $\beta^{+}$.
### Lifetimes
$\beta$ decay [[half-life|half-lives]] span a massive range: from a few milliseconds to $10^{16}$ years. It all depends on available energy and nuclear properties.

Probably the most important example of a decently fast $\beta^{-}$ decay is the free-neutron decay:
$$n\to p+e^{-}+\bar\nu_{e}$$
This occurs for free neutrons floating in the vacuum, has a [[Q value]] of about $0.78\text{ MeV}$ and has [[mean lifetime]] of around $\tau=889$ seconds, or about 15 minutes. This is why we don't see free neutrons floating through space: they all decay into protons far before they can get anywhere. Note that this only happens in the vacuum: in nuclei neutrons are generally kept stable by the [[Strong interaction|strong force]]. When they do decay, it's due to circumstance.

An example of some very slow processes is $\ce{^{40}_{19}K}$. This nuclide is $\beta$-unstable in every way: it can $\beta^{+}$, $\beta^{-}$ *and* EC. The branching ratios greatly favor $\beta^{-}$ and EC, with $\beta^{+}$ being a distant possibility. The potassium-40 half-life is about $t_{1/2}=1.27\times 10^{9}$ years.

:::image
![[Diagram Beta decay potassium-40|80%|center]]
Possible decay paths of $\ce{^{40}K}$ and their branching ratios. Notice how suppressed $\beta^{+}$ is compared to EC. The numbers near the energy levels are the $J^{P}$ nuclear state (total angular momentum + parity). $\gamma$ refers to [[gamma decay]]. The bend in the $\beta^{+}$ arrow indicates the extra $2m_{e}c^{2}$ energy cost over EC used up in handling electrons.
:::

The reaction formulas are
$$\begin{align}
\beta^{-}:\ &^{40}_{19}\text{K}\to\,^{40}_{20}\text{Ca}+e^{-}+\bar\nu_{e}\\[2pt]
\beta^{+}:\ &^{40}_{19}\text{K}\to\,^{40}_{18}\text{Ar}+e^{+}+\nu_{e}\\[2pt]
\text{EC}:\ &^{40}_{19}\text{K}+e^{-}\to\,^{40}_{18}\text{Ar}+\nu_{e}
\end{align}$$
## Energy conservation
Energy conservation arguments provide some useful insight in the different modes of $\beta$ decay. As a reference, $\beta^{+}$ and $\beta^{-}$ have Q values in the order of $\sim 1\text{ MeV}$.
### $\beta^{-}$ in the vacuum
A free neutron in the vacuum may $\beta^{-}$ decay as
$$n\to p+e^{-}+\bar\nu_{e}$$
The Q value is
$$\boxed{Q=(m_{n}-m_{p}-m_{e}-m_{\nu})c^{2}\simeq 0.8\ \text{MeV}}$$
(neutrino mass is basically zero). Assuming the neutron is at rest
$$Q=T_{p}+T_{e}+T_{\bar\nu}$$
The proton recoil energy is known to be tiny: $T_{p}\simeq 0.3\text{ keV}$, so it's negligible. The remaining $0.8\text{ MeV}$ is shared between the electron and the antineutrino. Since the neutrino is essentially massless, it's guaranteed to be relativistic. Similarly, the electron is also surely relativistic since $Q$ is comparable to its rest energy of $m_{e}c^{2}\simeq 0.5\text{ MeV}$. So in short we have
- small, non-relativistic proton recoil: $E_{p}=T_{p}\simeq 0.3\text{ keV}$.
- high electron [[relativistic energy]]: $E_{e}=T_{e}+m_{e}c^{2}\sim 1\text{ MeV}$.
- high neutrino relativistic energy: $E_{\nu}=T_{\nu}$.
### $\beta^{+}$ in the vacuum
A free proton in the vacuum *cannot* $\beta^{+}$ decay. This is because in the vacuum there is no external energy input, so the proton is solely responsible for respecting conservation of energy. However, the mass (and thus rest energy) of the proton is *smaller* than that of the neutron, so without energy coming in from the environment, decaying in the vacuum would require creating energy from nothing, and is therefore strictly impossible.
### $\beta^{-}$ in the nucleus
A bound neutron in some nucleus $\ce{^{A}_{Z}X_{N}}$ may $\beta^{-}$ decay, leading to a new daughter nucleus $\ce{^{A}_{Z+1}X'_{N-1}}$ according to
$$^{A}_{Z}\text{X}_{N}\to\,^{A}_{Z+1}\text{X}'_{N-1}+e^{-}+\bar\nu_{e}$$
The Q value is, using nuclear masses $M_{N}$:
$$Q=[M_{N}(^{A}_{Z}\text{X})-M_{N}(^{A}_{Z+1}\text{X}')-m_{e}]c^{2}.$$
(ignoring neutrino mass). It's convenient to use atomic masses instead:
$$M(\ce{^{A}X})c^{2}=[M_{N}(\ce{^{A}_{Z}X})+Zm_{e}]c^{2}-\sum_{i=1}^{Z}B_{i}$$
where $B_{i}$ is the binding energy of the $i$-th electron. So, extracting $M_{N}$,
$$M_{N}(\ce{^{A}_{Z}X})c^{2}=[M(\ce{^{A}X})-Zm_{e}]c^{2}+\sum_{i=1}^{Z} B_{i}$$
Then by substitution
$$Q=[M(\ce{^{A}X})-Zm_{e}-(M(\ce{^{A}X'})-(Z+1)m_{e})-m_{e}]c^{2}+\left( \sum_{i=1}^{Z} B_{i}-\sum_{i=1}^{Z+1} B_{i} \right)$$
Notice that the electron masses cancel out. The binding energies also cancel out with the exception of a single $-B_{Z+1}$ term. Outer shell electronic binding energy is very small ($\sim 10-100\text{ eV}$), so we might as well drop it. We're left with
$$\boxed{Q=[M(\ce{^{A}X})-M(\ce{^{A}X}')]c^{2}}$$
For example, $\ce{^{210}Bi}$ decays into $\ce{^{210}Po}$. The Q value is
$$Q=[M(\ce{^{210}Bi})-M(\ce{^{210}Po})]c^{2}=1.161\text{ MeV}$$
### $\beta^{+}$ in the nucleus
A bound proton in some nucleus $\ce{^{A}_{Z}X_{N}}$ may $\beta^{+}$ decay, leading to a new daughter nucleus $\ce{^{A}_{Z-1}X'_{N+1}}$ according to
$$^{A}_{Z}\text{X}_{N}\to\,^{A}_{Z-1}\text{X}'_{N+1}+e^{+}+\nu_{e}$$
Running the same procedure as the $\beta^{-}$ cases gives
$$\boxed{Q=[m(^{A}\text{X})-m(^{A}\text{X}')-2m_{e}]c^{2}}$$
Just like we saw when discussing EC, there is a $2m_{e}c^{2}$ term that distinguishes $\beta^{+}$. This comes up because, unlike in $\beta^{-}$, there isn't a perfect cancellation of electron masses. This makes $\beta^{+}$ $Q$ values universally smaller by about $\sim 1\text{ MeV}$ compared to $\beta^{-}$ decays. Since $\beta^{-}$ $Q$ values are already about $1\text{ MeV}$ in scale, this explains the rarity of $\beta^{+}$[^1] and why sometimes it's just not possible at all, as opposed to EC. For $Q$ to be positive and hence $\beta^{+}$ to be allowed, the mass difference between atoms must be greater than $2m_{e}c^{2}=1.022\text{ MeV}$.
### Electron capture in the nucleus
A bound proton in some nucleus $\ce{^{A}_{Z}X_{N}}$ may capture an electron from a shell, typically the innermost or second innermost shells, leading to a new daughter nucleus $\ce{^{A}_{Z-1}X'_{N+1}}$ according to
$$^{A}_{Z}\text{X}_{N}+e^{-}\to\,^{A}_{Z-1}\text{X}'_{N+1}+\nu_{e}$$
The energy of the neutrino is insignificant, so the $Q$ value ends up being almost identical to the $\beta^{-}$ decay
$$\boxed{Q=[m(^{A}\text{X})-m(^{A}\text{X}')]c^{2}-B_{e^{-}}}$$
$B_{e^{-}}$ is the binding energy of the electron that's being captured. Normally you'd ignore electronic binding energies, but since we're talking about innermost shells, the most tightly bound ones, it's possible in some atoms for $B_{e^{-}}$ to climb into the $\sim100\text{ keV}=0.1\text{ MeV}$ range, which is no longer negligible. $B_{e^{-}}$ becomes higher the more shells are filled in the atom, which means that it is most important in very heavy atoms[^2]. In smaller atoms, it can safely be neglected, in which case EC has the same $Q$ value as $\beta^{-}$. As such, EC also often has $Q$ values in the range of $\sim 1\text{ MeV}$, though take care of $B_{e^{-}}$.

As we've mentioned, the capture of an electron causes a cascade of high-energy photons. The first photon has energy $B_{e^{-}}$, the second has whatever energy is emitted due to the second transition, and so on and so forth. Since you're climbing into higher shells with each photon, the energy gets progressively lower and lower.

[^1]: Remember that the likelihood of a decay is proportional to the $Q$ value. Bigger $Q$ values make the decay more energetically efficient and therefore more likely to occur. Conversely, such as in this case, a tiny $Q$ value makes the decay technically possible but very unlikely.

[^2]: For instance, the highest $B_{e^{-}}$ I could find is in the $1s$ electron in uranium, which is $116\text{ keV}$. See [here](https://xdb.lbl.gov/Section1/Table_1-1.pdf).
