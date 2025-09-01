---
wiki-publish: true
---
The **nuclear Fermi gas model** is a model of the internal structure of an [[atomic nucleus]] that treats [[proton|protons]] and [[neutron|neutrons]] as independent [[Fermi gas|Fermi gases]]. It is a basic model that works only for nuclei in the ground [[stato|state]] or in lightly exited states. For a more complete model, see [[Nuclear shell model]]. As with the shell model, the Fermi gas model is a mean field theory.

This model relies on two assumptions:
1. protons and neutrons are independent systems;
2. the nucleons move freely inside the nucleus.
### Formulation
The [[potential]] felt by each [[Atomic nucleus|nucleon]] is the superposition of all other potentials produced by all other nucleons. The typical way to overcome this complexity is to make an assumption about the shape of the final resulting potential and assume that all nucleons are subject to this shared potential, called the **mean field**. In the Fermi gas model, we assume that the mean field potential is a [[Buca finita quantistica|finite square well]]. Actually, since we are considering protons and neutrons to be two different systems, there are two potential wells, one for protons and one for neutrons.

![[Diagram Nuclear Fermi gas|70%|center]]

As is usual for Fermi gases, we'll use the [[phase space]] to find the properties. Because of the [[Disuguaglianza di Heisenberg|uncertainty principle]], a [[particle]] occupies a volume $h^{3}=(2\pi\hbar)^{3}$ in phase space. All the particles in a volume $V$, each having a set [[Linear momentum|momentum]] around $p\pm dp$, occupy a phase space region equal to the volume $V$ in the space coordinates a thin spherical shell $4\pi p^{2}dp$ in momentum coordinates. The number of accessible states for this momentum is
$$dn=\frac{4\pi p^{2}dp}{(2\pi\hbar)^{3}}V$$
Nonzero [[temperature]] is complicated, so we'll start by assuming that the nucleus is at absolute zero, which is representative of its ground state. Here, all available states are occupied in a convenient order, from least to most energetic, for as many nucleons as are available. This is due to the [[Pauli exclusion principle]]. We know from the theory of Fermi gases that the highest zero-temperature state has some special properties, namely [[Fermi energy]] and all related quantities.

Let's integrate the above expression to get the number of occupied absolute zero states, which go up to the Fermi momentum $p_{F}$:
$$n=\int_{0}^{p_{F}}n(p)dp=\frac{V p_{F}^{3}}{6\pi^{2}\hbar^{3}}$$
Actually, this is an underestimate, because we are ignoring [[spin]]! Each momentum state hosts *two* nucleons, since they are spin 1/2 particles. Thus, the correct number is double that:
$$n=2\frac{V p_{F}^{3}}{6\pi^{2}\hbar^{3}}=\frac{V p_{F}^{3}}{3\pi^{2}\hbar^{3}}$$
Remember that this is true for both protons and neutrons, and that thanks to being at absolute zero, the number of occupied states is identical to the number of particles in the gas. As such, we can express the proton and neutron number pretty easily in terms of the Fermi momentum:
$$N=\frac{V(p_{F}^{n})^{3}}{3\pi^{2}\hbar^{3}},\qquad Z=\frac{V(p_{F}^{p})^{3}}{3\pi^{2}\hbar^{3}}$$
Now, realistically we start off knowing what $N$ and $Z$ are, and we'd rather find $p_{F}^{n}$ and $p_{F}^{p}$ instead. We can easily invert the equations, but here's an interesting proposition: we know (experimentally) that the nuclear radius goes more or less like $R=R_{0}A^{1/3}$, where $A$ the [[Atom|atomic mass number]] and $R_{0}=1.21\text{ fm}$. Thus, we can express the nuclear volume $V$  in terms of $A$:
$$V=\frac{4}{3}\pi R^{3}=\frac{4}{3}\pi R_{0}^{3}A$$
Put this volume in the above formula and you get
$$\boxed{p_{F}^{n}=\frac{\hbar}{R_{0}}\left( \frac{9\pi N}{4A} \right)^{1/3},\qquad p_{F}^{p}=\frac{\hbar}{R_{0}}\left( \frac{9\pi Z}{4A} \right)^{1/3}}$$
If we assume that both potential wells have the same radius and that the nucleus is balanced, $N=Z=A/2$, the momenta not only become equal, but also a universal constant:
$$p_{F}=p_{F}^{n}=p_{F}^{p}=\frac{\hbar}{R_{0}}\left(\frac{9\pi}{8}\right)^{1/3}\simeq250\ \frac{\text{MeV}}{c}\tag{1}$$
A very large momentum for a nucleus. The Fermi energy then is
$$E_{F}=\frac{p_{F}^{2}}{2M}\simeq33\ \text{MeV}$$
where $M$ is the [[mass]] of the proton or neutron, which differ by very little (but see below). This energy isn't quite the depth of the square well; the piece that is missing is the [[binding energy]]. The difference between $E_{F}$ and the actual well depth (call it $B'$) is something we've seen already in the [[semi-empirical mass formula]], which is a value of around $8\text{ MeV}$, which has few fluctuations for balanced nuclei. As such, the total well depth is more around
$$V_{0}=E_{F}+B\simeq 41\text{ MeV}$$
This is the kind of energy you'd need to blast a zero-energy nucleon with to have a good [[Probability|chance]] at separating it from nucleus. Of course, the nucleons are not at zero energy, with the outermost one being at $E_{F}$, leaving only $B$ to bind it.

Before I mentioned that proton and neutron masses differ: this actually makes the Fermi energy, and hence the well depth, slightly higher for neutrons than for protons. Consequently the protons appear less tightly bound than neutrons, likely due to [[electromagnetism|electromagnetic]] repulsion.
#### Neutron excess
This is for balanced nuclei at least. But the Fermi gas model also lets us compute the effect of neutron excess on binding energy. To do so, first we compute the average [[kinetic energy]] per nucleon
$$\langle E_{\text{kin}}(p_{F})\rangle=\frac{\int_{0}^{p_{F}}E_{\text{kin}}p^{2}dp}{\int_{0}^{p_{F}}p^{2}dp}= \frac{\frac{1}{5}\frac{1}{2M}p_{F}^{5}}{\frac{1}{3}p_{F}^{3}}=\frac{3}{10}\frac{p_{F}^{2}}{M}\sim20\ \text{MeV}$$
Then the total kinetic energy is[^1]
$$E_{\text{kin}}=N\langle E_{n}\rangle+Z\langle E_{p}\rangle=\frac{3}{10M}\bigl[N(p_{F}^{n})^{2}+Z(p_{F}^{p})^{2}\bigr]\simeq\frac{3}{10M}(N+Z)p_{F}^{2}$$
Using $(1)$ gives
$$E_{\text{kin}}(N,Z)=\frac{3}{10M}\frac{\hbar^{2}}{R_{0}^{2}}\left(\frac{9}{4}\pi\right)^{2/3}\frac{N^{5/3}+Z^{5/3}}{A^{2/3}}$$
valid for some constant $A$. When scanning through [[Isobar|isobars]], that is, by varying $N$ and $Z$, the function has a minimum in $N=Z$, so the binding energy evidently decreases when $N\neq Z$. By setting
$$N=\frac{A+\Delta}{2},\qquad Z=\frac{A-\Delta}{2},\qquad \Delta\equiv N-Z$$
and expanding the kinetic energy in powers of $\Delta/A$ we get
$$E_{\text{kin}}(A)=\frac{3}{10M}\frac{\hbar^{2}}{R_{0}^{2}}\left(\frac{9}{4}\pi\right)^{2/3}\left(A-\frac{5}{9}\frac{(N-Z)^{2}}{A}+\dots\right)$$
Compared to the semi-empirical mass formula, we can see the appearance of a volume term and an asymmetry term as the first couple of [[power series]] terms.
### Neutron stars
[[Stella di neutroni|Neutron stars]] have been described in the past through an adaptation of this model, essentially by considering them a massive, star-sized nucleus entirely made up of neutrons, where electromagnetism does not play a role, but [[gravity]] does (leading to higher attraction).

[^1]: You'll notice that we are using the common $p_{F}$ instead of different $p_{F}^{n}$ and $p_{F}^{p}$ despite no longer being in a balanced nucleus. This is because the difference is small compared to the total effect of asymmetry, but you can in principle do the math with both.
