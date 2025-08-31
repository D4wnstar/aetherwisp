---
wiki-publish: true
---
The **Fermi gas model** of the [[Atomic nucleus|nucleus]] is a model of the internal structure of an atomic nucleus that treats [[proton|protons]] and [[neutron|neutrons]] as independent [[Fermi gas|Fermi gases]]. It is a basic model that works only for nuclei in the ground [[stato|state]] or in lightly exited states. For a more complete model, see [[Nuclear shell model]].

This model relies on two assumptions:
1. protons and neutrons are independent systems;
2. the nucleons move freely inside the nucleus.
### Formulation  
The [[potential]] felt by each [[nucleon]] is the superposition of the potentials produced by all the other nucleons. For the Fermi gas, *we assume the resulting potential is a finite rectangular well*:

![[Grafico Buca di potenziale rettangolare|70%|center]]

Because of the [[Heisenberg uncertainty principle|uncertainty principle]], a [[Particle]] occupies a volume $h^{3}=(2\pi\hbar)^{3}$ in [[Phase space]] (six-dimensional, position + momentum). Take a spatial volume $V$ and a momentum shell $4\pi p^{2}dp$ with radius $p$ and thickness $dp$. The accessible [[state|states]] are
$$dn=\frac{4\pi p^{2}dp}{(2\pi\hbar)^{3}}V.$$
In the ground state (at absolute zero) all the lowest states are filled up to a maximum momentum called the **Fermi momentum** $p_{F}$. Integrating the above expression gives the number of such states:
$$n=\int_{0}^{p_{F}}n(p)dp=\frac{V p_{F}^{3}}{6\pi^{2}\hbar^{3}}.$$
By the [[Pauli exclusion principle]], each state can hold at most two [[Fermion|fermions]] of the same type. Since both protons and neutrons are fermions, the effective number of states is  
$$n=2\frac{V p_{F}^{3}}{6\pi^{2}\hbar^{3}},$$
and the numbers of neutrons and protons are
$$N=\frac{V(p_{F}^{n})^{3}}{3\pi^{2}\hbar^{3}},\qquad Z=\frac{V(p_{F}^{p})^{3}}{3\pi^{2}\hbar^{3}}\tag{1}$$
*Assuming* the nuclear radius is the experimentally determined value $R=R_{0}A^{1/3}$ (with $A$ the atomic [[Atom|mass number]] and $R_{0}=1.21$ fm), we also have
$$V=\frac{4}{3}\pi R^{3}=\frac{4}{3}\pi R_{0}^{3}A\tag{2}.$$
*We assume* the potential wells for protons and neutrons have the same radius and that the atom is neutral, i.e. $N=Z=A/2$. Using (1) and (2) we obtain the Fermi momentum
$$\boxed{p_{F}=p_{F}^{n}=p_{F}^{p}=\frac{\hbar}{R_{0}}\left(\frac{9\pi}{8}\right)^{1/3}\simeq250\ \text{MeV}/c},$$
a very large momentum for a nucleus. The energy of the highest occupied state, the **Fermi energy** $E_{F}$, is
$$\boxed{E_{F}=\frac{p_{F}^{2}}{2M}\simeq33\ \text{MeV}},$$
with $M=m_{n}$ or $m_{p}$.

The depth of the well at the top level $B'$ equals the average binding energy per nucleon $B/A$ and is about $7-8$ [[Electronvolt|MeV]]/nucleon. Adding the Fermi energy gives the bottom of the well $V_{0}=B'+E_{F}\simeq40$ MeV, independent of $A$.

The highest occupied state is the same for protons and neutrons (since $p_{F}^{n}=p_{F}^{p}$), but the Fermi energy (hence the well depth) is *slightly* different because $m_{n}>m_{p}$, so $E_{F}^{n}>E_{F}^{p}$. Consequently the neutron well is a bit deeper, and protons appear less bound than neutrons, likely because protons are positively charged and repel each other via [[Electromagnetism]]. The Fermi-gas model also lets us compute the binding-energy dependence on neutron excess.

First we compute the average kinetic energy per nucleon
$$\langle E_{\text{kin}}\rangle=\frac{\int_{0}^{p_{F}}E_{\text{kin}}p^{2}dp}{\int_{0}^{p_{F}}p^{2}dp}= \frac{\frac{1}{5}\frac{1}{2m}p_{F}^{5}}{\frac{1}{3}p_{F}^{3}}=\frac{3}{10}\frac{p_{F}^{2}}{m}\sim20\ \text{MeV}.$$
The total kinetic energy is
$$E_{\text{kin}}=N\langle E_{n}\rangle+Z\langle E_{p}\rangle=\frac{3}{10M}\bigl[N(p_{F}^{n})^{2}+Z(p_{F}^{p})^{2}\bigr]=\frac{3}{10M}(N+Z)p_{F}^{2}.$$
Inserting $p_{F}$ gives
$$E_{\text{kin}}(N,Z)=\frac{3}{10M}\frac{\hbar^{2}}{R_{0}^{2}}\left(\frac{9}{4}\pi\right)^{2/3}\frac{N^{5/3}+Z^{5/3}}{A^{2/3}},$$
valid for fixed $A$. Varying $N$ and $Z$, the function has its minimum at $N=Z$, so the binding energy decreases when $N\neq Z$. In practice, asymmetry in the nucleon composition weakens the nucleus. Setting
$$N=\frac{A+\Delta}{2},\qquad Z=\frac{A-\Delta}{2},\qquad \Delta\equiv N-Z,$$
we obtain
$$E_{\text{kin}}(A)=\frac{3}{10M}\frac{\hbar^{2}}{R_{0}^{2}}\left(\frac{9}{4}\pi\right)^{2/3}\!\left(A+\frac{5}{9}\frac{(N-Z)^{2}}{A}+\dots\right),$$
where the $A$ term contributes to the volume term in the [[Semi-empirical mass formula]], while the second term is the asymmetry correction, growing with the square of the neutron excess.