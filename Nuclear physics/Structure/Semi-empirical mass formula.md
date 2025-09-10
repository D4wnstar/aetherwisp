---
wiki-publish: true
aliases:
  - Weizsäcker formula
---
The **semi-empirical mass formula**, also known as the **Weizsäcker formula**, provides a theoretical estimate of the [[mass]] and [[binding energy]] of an [[atom]] exclusively through its [[Atomic nucleus|nuclear]] properties:
$$m(Z,A)=N m_n+Z m_p+Z m_e-\frac{B(Z,A)}{c^{2}}$$
where $m_n$, $m_p$, and $m_e$ are the masses of the [[neutron]], [[proton]], and [[electron]]. $B(Z,A)$ is the nuclear binding energy, given by
$$\frac{B(Z,A)}{c^{2}}=a_v A-a_s A^{2/3}-a_{C}\frac{Z(Z-1)}{A^{1/3}}-a_a\frac{(N-Z)^2}{4A}+\delta$$
where
- $Z$, $N$, and $A$ are the [[Atom|atomic number]], the [[Atom|neutron number]], and the [[Atom|atomic mass number]].
- $c$ is the [[speed of light]].
- the $a$ parameters and $\delta$ represent different sources of binding energy and are explained below.

The numerical values of the parameters (Povh et al., Particles and Nuclei, 7th ed.) are[^1]
$$\begin{align}
a_v &= 15.67\,\tfrac{\text{MeV}}{c^{2}}\\
a_s &= 17.23\,\tfrac{\text{MeV}}{c^{2}}\\
a_{C} &= 0.714\,\tfrac{\text{MeV}}{c^{2}}\\
a_a &= 93.15\,\tfrac{\text{MeV}}{c^{2}}\\
a_p &= 34\,\tfrac{\text{MeV}}{c^{2}}
\end{align}$$

This formula is derived from the **liquid drop model** of nuclear structure, which posits that the nucleus behaves like a quantum fluid of neutrons and protons, a [[Fermi liquid]].

Since electronic binding energy is quite negligible compared to nuclear scales of energy, this formula also provides the mass of the atomic nucleus by simply omitting the mass of the electrons.
### Parameterization
The binding energy formula contains five experimentally determined constants, each with a specific interpretation. The two major forces at play are the [[strong interaction]], which is what keeps the nucleons bound, and [[electromagnetism]], which seeks to repel positively charged protons.
1. $a_v A$ is the **volume term**, proportional to $A$. If every [[Atomic nucleus|nucleon]] interacted with every other nucleon, the proportionality would be $B\propto A(A-1)\sim A^{2}$. Experimentally, the nuclear radius scales as $R\propto A^{1/3}$, yet in practice one finds $B\propto A$, indicating that nucleons interact only with their close neighbors.
2. $a_s A^{2/3}$ is the **surface term**. The neighbor-interaction picture holds for nucleons *inside* the nucleus, but those on the surface have fewer neighbors and are less tightly bound, thus contributing less to the total. This term corrects for that deficit by subtracting an amount proportional to the nuclear surface, which experimentally goes like $R^{2}\propto A^{2/3}$.
3. $a_{C} \dfrac{Z(Z-1)}{A^{1/3}}$ is the **Coulomb term**. Protons are all positively charged and repel one another via electromagnetism, weakening their binding. The proportionality is derived from the behavior of the electric [[potential energy]] in a nucleus modeled as a uniformly charged sphere of [[electric charge]] $Ze$:
$$U_{\text{e.m.}}\propto \frac{Z(Z-1)\alpha\hbar c}{R}\propto \frac{Z(Z-1)}{A^{1/3}}$$
4. $a_a\dfrac{(N-Z)^2}{4A}$ is the **asymmetry term**. It accounts for the fact that in heavier nuclei, the neutron–proton symmetry is broken to offset the increasing Coulomb repulsion among protons. This is because neutrons do not contribute to repulsion (they are electrically neutral), but do contribute to strong attraction (they are [[Barione|baryons]]). When protons and neutrons are equal in number this term vanishes, since they are the most stable. Greater asymmetry leads to greater instability (less binding energy).
5. $\delta$ is the **pairing term**. Nuclei are more stable when they contain even numbers of protons and neutrons, which suggests that "pair" with each other in some sort of stable configuration. Indeed, among all known stable nuclei, only four of them have odd $N$ and $Z$ (they are $\ce{^{2}H}$, $\ce{^{6}Li}$, $\ce{^{10}B}$ and $^{14}N$). This term is discontinuous and works as follows:
$$\begin{aligned}
\delta &= +a_p A^{-3/4} &&\text{if }A,Z,N\text{ even}\\
\delta &= 0 &&\text{if }A\text{ odd}\\
\delta &= -a_p A^{-3/4} &&\text{if }A\text{ even and }Z,N\text{ odd}
\end{aligned}$$
It should be noted that unlike with other terms, the $-3/4$ exponent of $A$ is purely empirical, obtained from a [[Parameter estimation|fit]]. In fact, there is debate regarding whether $-1/2$ is a more accurate exponent, as modern data seems to suggest so.

:::image
![[binding_vs_A.png]]
A plot of binding energy per nucleon. Each line adds one more term to the formula. Notice how most $B/A$ values are between $7.2$ and $8.8\text{ MeV}/c^{2}$.
:::

[^1]: This value of $a_{p}$ assumes an exponent of $-3/4$. Povh et al. use an exponent $-1/2$ and give $a_{p}=11.2\text{ MeV}/c^{2}$ instead.
