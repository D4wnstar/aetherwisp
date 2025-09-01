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

Moreover, the motion of the nucleons is taken to be non-[[Lorentz transformation|relativistic]] to avoid having to invoke relativistic quantum mechanics and the [[Dirac equation]]. Finally, predictions made by this model are only valid if the outermost shell contains exactly one unpaired nucleon, be it one too many or one too few. Shells that are not complete but contain more than one nucleon, such as those in $^{23}_{11}\text{Na}_{12}$, are not correctly described.

Different versions of the shell models use different potentials. In fact, the choice of potentials is rather complicated compared to the electron shell model as we do not currently have an analytical form for nucleon-nucleon interaction. Whereas the choice in the atom is easy (the central potential is just the [[electric potential]] of a [[Electric charge|point charge]]), with nucleons not so much, as we must consider an $n$-body problem governed by the [[strong interaction]] and therefore go through quantum chromodynamics, which is *much* more complicated.
### Gaussian potential
For small nuclei ($A\leq7$), the nucleon distribution can roughly be taken to be [[Gaussian distribution|Gaussian]], so we can approximate the potential with a Gaussian spatial profile. In other words, we have a three-dimensional [[Oscillatore armonico quantistico|quantum harmonic oscillator]] whose potential, when expressed in [[spherical coordinates]], is
$$V(r)=\frac{1}{2}kr^{2}$$
which depends only on the radial coordinate. The [[Schrödinger equation]] is then solved in the usual manner for central potentials, leading to an angular part given by the [[spherical harmonics]] $Y_{l}^{m}(\theta,\phi)$. The energy eigenvalues are
$$E_{N}=\hbar\omega_{0}\left(N+\frac{3}{2}\right)$$
where $N=0,1,2,\ldots$ is the energy-level [[quantum number]]. Introducing the number of nodes $n=1,2,3\ldots$ (which counts the number of states with the given value of $l$) and the orbital quantum number $l=0,1,2\ldots$ (which satisfies $l\leq N$), the energy levels can be written as
$$N=2(n-1)+l$$
The energy-level [[degenerazione|degeneracy]] is $2l+1$, or $2(2l+1)$ when considering [[spin]] 1/2 nucleons. This is important: a shell is a collection of degenerate states, so the degeneracy basically tells us how many nucleons fit inside the shell of energy level $N$. Even more importantly, since magic numbers are associated with filled shells, it's the degeneracy that works as the predictor for magic numbers, the discovery of which is ultimately one of the main goals of the shell model.

This simple model is quite reminiscent of the [[Hydrogen atom|hydrogenic atom]], so it's common to employ [[spectroscopic notation]] here too, namely the usage of the letters $s$, $p$, $d$, $f$, etc. for the orbital quantum number. For instance, the first three energy levels/shells are:
- Shell $N=0$ has $n=1$ and $l=0$, hence corresponds to the $1s$ state. It has a degeneracy of 2, meaning it can contain up to two nucleons.
- Shell $N=1$ has $n=1$ and $l=1$, hence corresponds to the $1p$ state. It has a degeneracy of 8.
- Shell $N=2$ either has $n=1$ and $l=2$ or $n=2$ and $l=0$, and hence corresponds to the $1d$ and $2s$ states. It has a degeneracy of 12.

:::image
![[Diagram Nuclear shell model Gaussian|80%|center]]
A diagram showing the behavior of the first four shells, according to the Gaussian mean potential. The first three shells correctly predict magic numbers (2, 8, 20), but already by the fourth it goes off track (40 is not a magic number, but 28 is).
:::
### Woods–Saxon potential
A more accurate description requires a better potential. For this purpose one can use the [[Woods–Saxon potential]], which yields more accurate magic numbers.

![[Closed shells Woods–Saxon.png|240]]

Using the Woods–Saxon potential removes the $l$ degeneracy in the shells, because states with the same $N$ but different $nl$ have different energies under this potential. It still does not reproduce all magic numbers exactly, but it is more accurate than the Gaussian potential.

The most accurate shell model ([[Woods–Saxon potential]] with [[Fine structure|spin–orbit coupling]]) is very precise for $A<150$ and $190<A<220$. Outside this range other devices must be used, such as accounting for nuclear deformation (for $150<A<190$ and $A>230$).
### Spin–orbit coupling
Improving the model further is complicated because the Woods–Saxon potential already has the physically correct form, and altering it would spoil the physical interpretation of the model. What we can do is add corrections to this potential. One such correction is **spin–orbit coupling**, incidentally one of the [[fine-structure]] corrections of the [[hydrogen atom]].

Denoting the correction potential by $V_{l,s}$, the corrected potential is  
$$V_{\text{tot}}(r)=V_{\text{cent}}(r)+V_{l,s}(r)\frac{\langle\vec{l}\cdot\vec{s}\rangle}{\hbar^{2}}$$  
where $\vec{l}$ is the orbital angular momentum (with respect to the nuclear center) and $\vec{s}$ is the nucleon spin.

Nucleons are [[Fermion|fermions]] and therefore have spin $1/2$. We define the total angular momentum $\vec{j}$ as $\vec{j}=\vec{l}+\vec{s}$. Since the spin can take only two values, we have  
$$j=l\pm\frac{1}{2},$$  
except for $l=0$, where $j=1/2$. Computing  
$$j^{2}=(\vec{l}+\vec{s})^{2}=(\vec{l}^{2}+2\vec{l}\cdot\vec{s}+\vec{s}^{2})\quad\Rightarrow\quad\vec{l}\cdot\vec{s}=\frac{1}{2}(\vec{j}^{2}-\vec{l}^{2}-\vec{s}^{2})$$  
and solving the [[eigenvalue equation]] and inserting the expectation values,  
$$\langle\vec{l}\cdot\vec{s}\rangle=\frac{\hbar^{2}}{2}\bigl[j(j+1)-l(l+1)-s(s+1)\bigr]=\hbar^{2}\begin{cases}
j=l+\frac{1}{2}\rightarrow+\frac{l}{2}\\[4pt]
j=l-\frac{1}{2}\rightarrow-\frac{l+1}{2}.
\end{cases}$$  
Hence the energy splitting of the levels increases linearly with angular momentum and is  
$$\Delta E_{l,s}=\Bigl[\langle\vec{l}\cdot\vec{s}\rangle_{j=l+\frac{1}{2}}-\langle\vec{l}\cdot\vec{s}\rangle_{j=l-\frac{1}{2}}\Bigr]\langle V_{l,s}(r)\rangle=\frac{2l+1}{2}\langle V_{l,s}(r)\rangle.$$  
Experimentally $V_{l,s}$ is negative, so the $j=l+1/2$ level always lies below the $j=l-1/2$ level.

The effect of this correction is very pronounced, and with it the magic numbers are reproduced perfectly.

![[Closed shells spin–orbit.png|360]]

Now levels with $l>0$ are split into two new levels. The quantum number $j$ is usually specified by an additional subscript on the letter associated with $l$. For example, for the state $n=1$ and $l=3$ ($1f$), which has degeneracy 14, one writes  
$$\begin{cases}
j=\dfrac{5}{2}\rightarrow\text{level }1f_{5/2}\\[4pt]
j=\dfrac{7}{2}\rightarrow\text{level }1f_{7/2}.
\end{cases}$$  
Each of these levels has a **capacity**, i.e. the number of nucleons it can hold. Summing the capacities progressively reproduces every magic number one by one.

### Applications  
Consider two [[Isotope|isotopes]] of oxygen: $^{15}_{8}\text{O}$ and $^{17}_{8}\text{O}$. Both have 8 protons, but one has 7 neutrons and the other 9. In the first case there is an unpaired proton; in the second an unpaired neutron.

![[Oxygen shells.png]]

In $^{15}_{8}\text{O}$ the unpaired proton is in the $1p_{1/2}$ shell. The ground state of the nucleus should therefore have spin $1/2$ and parity $(-1)^{1}=-1$. It is customary to write the nuclear state as $J^{P}$, where $J$ is the angular momentum and $P$ the parity, denoted by $+$ and $-$. In this case we have $J^{P}=\tfrac{1}{2}^{-}$.

In $^{17}_{8}\text{O}$ there is a hole in the $1d_{5/2}$ level, so the spin should be $5/2$ and the parity $(-1)^{2}=+1$, giving $J^{P}=\tfrac{5}{2}^{+}$.

#### Even–even and odd–odd nuclei  
For [[Nuclide|nuclides]] with both $Z$ and $N$ even, regardless of which states are excited, the ground state will be $J^{P}=0^{+}$ and the first excited state will be $J^{P}_{1}=2^{+}$. Because they are paired, they always have positive parity.

For nuclides with both $Z$ and $N$ odd, the total spin is obtained as usual for a two-particle system with spins $j_{1}$ and $j_{2}$: the possible values range from $|j_{1}-j_{2}|$ to $j_{1}+j_{2}$ in integer steps. The parity is $(-1)^{l_{1}+l_{2}}$, with $l_{1}$ and $l_{2}$ the orbital angular momenta of the unpaired proton and neutron.

For example, $^{6}_{3}\text{Li}_{3}$ has both an unpaired proton and an unpaired neutron in $1p_{3/2}$, so $l_{1}=l_{2}=l=1$. The parity is then $(-1)^{1+1}=+1$. The spin ranges from $|3/2-3/2|=0$ to $3/2+3/2=3$, so it can take the values 0, 1, 2, or 3. In total the possible states are  
$$J^{P}=0^{+},\,1^{+},\,2^{+},\,3^{+}.$$

### State transitions  
Just like electrons, nucleons can undergo a [[State transition]] to move up or down shells. A nucleon can reach an excited state in two ways:  
1. by exciting the unpaired nucleon to the next subshell;  
2. by coupling this nucleon with another coming from a deeper subshell.

For example, in $^{7}_{3}\text{Li}_{4}$ ($J^{P}=\tfrac{3}{2}^{+}$) the unpaired neutron is in $1p_{3/2}$ and can  
1. move up to $1p_{1/2}$, becoming $J^{P}=\tfrac{1}{2}^{-}$;  
2. couple with the neutron in $1s_{1/2}$, becoming $J^{P}=\tfrac{1}{2}^{+}$.  
Case 2 requires much more energy.

[^1]: This is the main difference with the electron shell model, which has to deal with a primary central potential from the nucleus *and* secondary inter-electron potentials.
