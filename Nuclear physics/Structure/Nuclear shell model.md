---
wiki-publish: true
aliases:
  - shell
---
The **nuclear shell model** is a mean field model of the [[atomic nucleus]]. Reminiscent of its sibling the [[electron shell model]], which is for [[Electron|electrons]] around an [[atom]], the model describes the [[Atomic nucleus|nucleons]] as having discrete [[Stationary state|energy states]], which are progressively occupied in order from least to most energetic until they complete a so-called **shell**, which is a particularly stable configuration of nucleons. The states cannot be occupied by too more than two nucleons each due to the [[Pauli exclusion principle]]. Similarly to how valence electrons are sufficient to determine most of the behavior of an atom, "valence nucleons" in the outermost shell are enough to determine most of the behavior of the nucleus, namely [[spin]] and [[parity]].

The main result of the shell model is explaining the presence of anomalous stability present in some nuclei containing specific numbers of [[proton|protons]] and [[neutron|neutrons]], known as [[Magic number|magic numbers]].
## Formulation
The nuclear shell model is based on two basic ideas:
1. each nucleon is a quantum object with a defined energy eigenstate which occupies a well-defined **shell** inside the nucleus, a shell being a theoretical configuration of nucleons that, when filled, leads to a particularly stable state;
2. the nucleons are subject to a mean [[potential]], which originates from the other nucleons[^1].

Moreover, a few approximations are made to render the system tenable in a mathematical manner:
1. the motion of the nucleons is taken to be non-[[Lorentz transformation|relativistic]] to avoid having to invoke relativistic quantum mechanics and the [[Dirac equation]];
2. nuclei are considered to be spherical.

As a consequence of the latter approximation, the predictions made by this model are only valid if the outermost shell contains exactly one unpaired nucleon, be it one too many or one too few. This is because the spherical approximation is only true for nearly complete shells. Incomplete shells lack the symmetry required for this kind of treatment.

Different versions of the shell models use different potentials. In fact, the choice of potentials is rather complicated compared to the electron shell model as we do not currently have an analytical form for nucleon-nucleon interaction. Whereas the choice in the atom is easy (the central potential is just the [[electric potential]] of a [[Electric charge|point charge]]), with nucleons not so much, as we must consider an $n$-body problem governed by the [[strong interaction]] and therefore go through quantum chromodynamics, which is *much* more complicated.
### Gaussian potential
For small nuclei ($A\leq7$), the nucleon distribution can roughly be taken to be [[Gaussian distribution|Gaussian]], so we can approximate the potential with a Gaussian spatial profile. In other words, we have a three-dimensional [[Oscillatore armonico quantistico|quantum harmonic oscillator]] whose potential, when expressed in [[spherical coordinates]], is
$$V(r)=\frac{1}{2}kr^{2}$$
which depends only on the radial coordinate. The [[Schrödinger equation]] is then solved in the usual manner for central potentials, leading to an angular part given by the [[spherical harmonics]] $Y_{l}^{m}(\theta,\phi)$. The energy eigenvalues are
$$E_{N}=\hbar\omega_{0}\left(N+\frac{3}{2}\right)$$
where $N=0,1,2,\ldots$ is the energy-level [[quantum number]]. Introducing the number of nodes $n=1,2,3\ldots$ (which counts the number of states with the given value of $l$) and the orbital quantum number $l=0,1,2\ldots$ (which satisfies $l\leq N$), the energy levels can be written as
$$N=2(n-1)+l$$
The energy-level [[degenerazione|degeneracy]] is $2l+1$, or $2(2l+1)$ when considering [[spin]] 1/2 nucleons. This is important: a shell is a collection of degenerate states, so the degeneracy basically tells us how many nucleons fit inside the shell of energy level $N$ (it's not one-to-one, there are more states than nucleons; the number of nucleons per shell is called the **capacity**). Even more importantly, since magic numbers are associated with filled shells, it's the degeneracy that works as the predictor for magic numbers, the discovery of which is ultimately one of the main goals of the shell model.

This simple model is quite reminiscent of the [[Hydrogen atom|hydrogenic atom]], so it's common to employ [[spectroscopic notation]] here too, namely the usage of the letters $s$, $p$, $d$, $f$, etc. for the orbital quantum number. For instance, the first three energy levels/shells are:
- Shell $N=0$ has $n=1$ and $l=0$, hence corresponds to the $1s$ state. It has a degeneracy of 2, meaning it can contain up to two nucleons.
- Shell $N=1$ has $n=1$ and $l=1$, hence corresponds to the $1p$ state. It has a degeneracy of 8.
- Shell $N=2$ either has $n=1$ and $l=2$ or $n=2$ and $l=0$, and hence corresponds to the $1d$ and $2s$ states. It has a degeneracy of 12.

:::image
![[Diagram Nuclear shell model Gaussian|80%|center]]
A diagram showing the behavior of the first four shells, according to the Gaussian mean potential. The first three shells correctly predict magic numbers (2, 8, 20), but already by the fourth it goes off track (40 is not a magic number, but 28 is).
:::
### Woods–Saxon potential
For larger nuclei, we'll need a more realistic potential. A far better choice in modern day is the [[Woods-Saxon potential]], which you can see below.

![[Plot Woods-Saxon potential]]

Calculation of the actual energy levels is a lot more complicated compared to the harmonic oscillator. The idea is still the same however: solve the Schrödinger equation in spherical coordinates with this potential to find the energy eigenstates (shells) and their degeneracy (nucleons admitted by the shell). It should be mentioned that when a lot of splitting is introduced (and therefore many energy levels/shells), magic number stop being plain closed shells, but rather closed shells that are distant in energy from the next one over.

:::image
![[Closed shells Woods-Saxon.png|300]]
A diagram showing shells according to the Woods-Saxon mean potential. The main difference is the lifting of degeneracy over $l$, which leads to a lot more energy levels (since same $N$ but different $nl$ have different energies). Like the Gaussian distribution, it gets the first magic numbers right, but goes off track by the fourth.
:::
#### Spin–orbit coupling
The Woods-Saxon is known to have a physically accurate form, so why does it not predict the magic numbers? The answer is that while the potential is right, we're neglecting other effects that incur further degeneracy lifting: relativistic effects. Just like in the [[hydrogen atom]], to further refine our model we introduce a **spin-orbit coupling** term[^2]. A spin-orbit term takes the interaction between spin and [[angular momentum]] into account, in this case that of the nucleons.

The SO term is added on top of our mean Woods-Saxon potential $V_\text{WS}$:
$$V_{\text{tot}}(r)=V_{\text{WS}}(r)+V_{ls}(r)\frac{\langle\mathbf{L}\cdot\mathbf{S}\rangle}{\hbar^{2}}$$
where $\mathbf{L}$ is the orbital angular momentum with respect to the nuclear center and $\mathbf{S}$ is the nucleon spin. $l$ and $s$ are their related [[norm]], i.e. their [[quantum number|quantum numbers]].

Luckily, nucleons are protons and neutrons, which we know to be [[fermion|fermions]] with spin 1/2. As such, $s=1/2$ for all nucleons (though remember both spin directions, $\pm1/2$). We define the total angular momentum as $\mathbf{J}=\mathbf{L}+\mathbf{S}$, with quantum number $j=l\pm 1/2$. There's an exception for $l=0$, where $j=1/2$ is the only allowed value[^3]. The square is
$$j^{2}=(\mathbf{L}+\mathbf{S})^{2}=(L^{2}+2\mathbf{L}\cdot\mathbf{S}+S^{2})\quad\Rightarrow\quad\mathbf{L}\cdot\mathbf{S}=\frac{1}{2}(J^{2}-L^{2}-S^{2})$$
Inserting the expectation values for angular momenta square norms ($L^{2}\psi=\hbar^{2}l(l+1)\psi$, etc.):
$$\langle\mathbf{L}\cdot\mathbf{S}\rangle=\frac{\hbar^{2}}{2}\bigl[j(j+1)-l(l+1)-s(s+1)\bigr]$$
We know that $j=l\pm 1/2$ is, so
$$\langle \mathbf{L}\cdot \mathbf{S} \rangle =\hbar^{2}\begin{cases}
j=l+\frac{1}{2}\quad\Rightarrow \quad+\frac{l}{2}\\
j=l-\frac{1}{2}\quad\Rightarrow \quad-\frac{l+1}{2}
\end{cases}$$
The energy splitting of the levels is given by the difference between these values, multiplied by the average SO potential:
$$\Delta E_{l,s}=\Bigl[\langle\mathbf{L}\cdot\mathbf{S}\rangle_{j=l+\frac{1}{2}}-\langle\mathbf{L}\cdot\mathbf{S}\rangle_{j=l-\frac{1}{2}}\Bigr]\langle V_{ls}(r)\rangle=\frac{2l+1}{2}\langle V_{ls}(r)\rangle$$
We can see that the difference increases linearly with angular momentum. Experimentally we find that $V_{ls}(r)$ is negative, so the $j=l+1/2$ level always lies below the $j=l-1/2$ level.

The effect of this correction is pronounced, as it makes important changes to the ordering of magic numbers. All levels with nonzero $l$, which are $p,d,f,g\ldots$, are split into two new levels.

:::image
![[Closed shells spin-orbit.png|400]]
A diagram showing shells according to the spin-orbit-corrected Woods-Saxon mean potential. The left side shows the shells predicted by uncorrected Woods-Saxon. Notice how all known magic numbers (2, 8, 20, 28, 50, 82, 126) are reproduced, and how much splitting SO coupling introduces. By the way, the number 184 is possibly correct theoretical prediction of a new magic number!
:::

In notation, the quantum number $j$ is usually specified by an additional subscript. For example, for the state $n=1$ and $l=3$ (i.e. the level $1f$), one would write the two possible states as
$$\begin{cases}
j=\dfrac{5}{2}\rightarrow\text{level }1f_{5/2}\\[4pt]
j=\dfrac{7}{2}\rightarrow\text{level }1f_{7/2}
\end{cases}$$
This model is very precise for $A<150$ and $190<A<220$. Outside this range other methods should be used, such as accounting for nuclear deformation.
## Applications
The shell model is quite useful to make predictions regarding the stability of nuclei. To illustrate, consider two [[Isotope|isotopes]] of oxygen: $\ce{^{15}_{8}O}$ and $\ce{^{17}_{8}O}$. Both have 8 protons, but one has 7 neutrons and the other has 9. Recall that 8 is a magic number, so these are both magic nuclei for protons and *almost* magic in neutrons. In the first case there is one too few neutrons; in the second one too many. Recall also that nucleons like to paired: this means that one proton will be unpaired in oxygen-15 and one neutron will be unpaired in oxygen-17. The missing nucleon of a pair is often called a **hole** in the shell.

![[Oxygen shells.png]]

It is customary to write the overall nuclear state as $J^{P}$, where $J$ is the total angular momentum and $P$ is the [[parity]], denoted by $+$ and $-$. The parity of the [[wavefunction]] of a nucleus with a single hole is $(-1)^{l}$, where $l$ is the shell with the hole. Similarly, the total angular momentum is that of the shell with the hole.

In $\ce{^{15}_{8}O}$ the unpaired proton is in the $1p_{1/2}$ shell, so there is a hole in the equivalent neutron shell. The ground state of the nucleus should therefore have $J=1/2$ and parity $P=(-1)^{1}=-1$. In proper notation: $J^{P}=\tfrac{1}{2}^{-}$.

In $\ce{^{17}_{8}O}$ the hole is in the $1d_{5/2}$ shell, so the momentum should be $J=5/2$ and the parity should be $P=(-1)^{2}=+1$. In proper notation: $J^{P}=\tfrac{5}{2}^{+}$.
## Beyond the shell model
The shell model isn't capable of giving predictions in all cases. For instance, it lacks predictive capabilities outside nearly complete shells. Some considerations can be made for nuclei beyond this scope.
### Deformed nuclei
The shell model expects spherical symmetry to hold. However, if the nucleus is deformed, we need to extend the model to consider the shape of the nucleus too. This is a major factor especially in the ranges $150<A<190$ and $A>230$.
### Even-even nuclei
For nuclei with both $Z$ and $N$ even, regardless of which states are occupied, the ground state will always be $J_{0}^{P}=0^{+}$ and the first excited state will always be $J^{P}_{1}=2^{+}$. Because they are paired, they parity is guaranteed to be positive.
### Odd-odd nuclei  
For nuclei with both $Z$ and $N$ odd, the total spin is obtained as usual for a two-particle system with spins $j_{1}$ and $j_{2}$: the possible values range from $|j_{1}-j_{2}|$ to $j_{1}+j_{2}$ in integer steps. The parity is $(-1)^{l_{1}+l_{2}}$, with $l_{1}$ and $l_{2}$ the orbital angular momenta of the unpaired proton and neutron.

For example, $^{6}_{3}\text{Li}_{3}$ has both an unpaired proton and an unpaired neutron in $1p_{3/2}$, so $l_{1}=l_{2}=l=1$. The parity is then $(-1)^{1+1}=+1$. The spin ranges from $|3/2-3/2|=0$ to $3/2+3/2=3$, so it can take the values 0, 1, 2, or 3. In total the possible states are
$$J^{P}=0^{+},\,1^{+},\,2^{+},\,3^{+}$$
## State transitions  
Just like electrons, nucleons can undergo a [[state transition]] to move up or down shells. When receiving energy from an external source, a nucleon can reach an excited state in two ways:
1. by being promoted to the next subshell;
2. by being coupled with another nucleon from a more inner subshell.

Case 2 requires much more energy.

For example, in $\ce{^{7}_{3}Li_{4}}$ (state: $J^{P}=\tfrac{3}{2}^{+}$) there is one unpaired neutron in $1p_{3/2}$ and it can
1. move up to $1p_{1/2}$, making the nucleus end up in $J^{P}=\tfrac{1}{2}^{-}$;
2. couple with the neutron in $1s_{1/2}$, ending up in $J^{P}=\tfrac{1}{2}^{+}$.

[^1]: This is the main difference with the electron shell model, which has to deal with a primary central potential from the nucleus *and* secondary inter-electron potentials.

[^2]: You can do this with any mean potential. For instance, we could've added an SO term to the quantum harmonic oscillator from before and it would've improved our findings.

[^3]: Combining angular momenta follows the universal triangle rule that the allowed values of a combination are given by $j=\lvert j_{1}-j_{2} \rvert,\lvert j_{1}-j_{2} \rvert+1,\ldots,j_{1}+j_{2}$, where $j_{1}$ and $j_{2}$ are any angular momenta, be it orbital, spin, same particle, different particles, etc. Here we have $j_{1}=l$ and $j_{2}=s$, so for $l=0$, $j=\lvert 0- 1/2 \rvert, 0+ 1/2=1/2$, which leaves only possible value.
