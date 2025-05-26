---
wiki-publish: true
---
**Graphene** is a sheet of carbon [[atom|atoms]] in a hexagonal (honeycomb) pattern. It is precisely one atom thick and can therefore be regarded as two-dimensional. It is a well-studied system due to both its geometric simplicity and its practical use cases in physics and engineering.

![[Graphene lattice.png]]

The honeycomb lattice is not a [[Bravais lattice]]. The Bravais lattice is actually two-fold: there are two *triangular* Bravais sublattices (blue and red in the figure) that superimpose to form what we see.

Chemically speaking, all the carbon atoms have the exact same chemical bonds. All of them have hybrid $sp^{2}$ bonds (one $2s$ [[orbital]] alongside the $2p_{x}$ and $2p_{y}$ orbitals form three hybrid $sp^{2}$). They all form $\sigma$ bonds with other carbons and are each occupied by two [[electron|electrons]], one [[spin]] up and one spin down. One electron per carbon remains in the $2p_{z}$ orbital, which sticks out of the lattice and permits $\pi$ bonds between atoms. It also permits stronger bonds across layers of graphene (stacked layers of graphene make the much more common **graphite**).
### Tight binding
The structure of graphene, specifically that of the $\pi$ bonds it forms, can be explained with the [[tight binding]] model. The $\mathbf{a}$ vector is about $\mathbf{a}=2.46\ \mathring{\mathrm{A}}$. We define some convenience vectors as follows:
$$\boldsymbol{\eta}_{1}=\frac{\mathbf{a}}{\sqrt{ 3 }}\hat{\mathbf{x}},\quad \boldsymbol{\eta}_{2}=\frac{\mathbf{a}}{\sqrt{ 3 }}\left( - \frac{1}{2}\hat{\mathbf{x}}+ \frac{\sqrt{ 3 }}{2}\hat{\mathbf{y}} \right),\quad \boldsymbol{\eta}_{3}=\frac{\mathbf{a}}{\sqrt{ 3 }}\left( - \frac{1}{2}\hat{\mathbf{x}}- \frac{\sqrt{ 3 }}{2}\hat{\mathbf{y}} \right)$$
These identify the nearest neighbors of each carbon atom in the $A$ sublattice (blue), starting from that atom. $\boldsymbol{\eta}_{1}$ is the atom to the right, $\boldsymbol{\eta}_{2}$ and $\boldsymbol{\eta}_{3}$ are to the top left and bottom left respectively.

Given each atom contributes one $2p_{z}$ orbital, our tight binding trial function will be
$$\psi_{\mathbf{k}}(\mathbf{r})=\sum_{\mathbf{R}} \frac{e^{i\mathbf{k}\cdot \mathbf{R}}}{\sqrt{ N }}[c_{pzA}(\mathbf{k})e^{i\mathbf{k}\cdot \mathbf{d}_{1}}\phi_{pzA}(\mathbf{r}-\mathbf{R}-\mathbf{d}_{1})+c_{zpB}(\mathbf{k})e^{i\mathbf{k}\cdot \mathbf{d}_{2}}\phi_{pzB}(\mathbf{r}-\mathbf{R}-\mathbf{d}_{2})]$$
Recall that the Bloch wavefunction is
$$\psi_{\mathbf{k}}(\mathbf{r})=\frac{1}{\sqrt{ N }}\sum_{\mathbf{R}} e^{i\mathbf{k}\cdot \mathbf{R}}\phi_{n}(\mathbf{r}-\mathbf{R})$$
We insert this is the [[Equazione di Schrödinger|Schrödinger equation]] $\hat{H}\ket{\psi_{\mathbf{k}}(\mathbf{r})}=E\ket{\psi_{\mathbf{k}}(\mathbf{r})}$, then apply the [[Notazione braket|bra]] of each orbital independently. This leads to a system of equations with a number of equations equal to the number of orbitals per [[primitive cell]].

...

:::image
![[Graphene electron band gap.png]]
Upper caption: $\pi$ bands in self-standing graphene
Lower caption: Graphene is a semimetal (or zero gap semiconductor): the Fermi level intersects the $\pi$ band in a point ($K$) of the Brillouin zone.
:::

We can see that the band gap of the graphene structure is *exactly* zero. Not around zero, but precisely zero. This is the cause of the interesting behavior of graphene: it is not quite a metal, not quite a [[dielectric]], not quite a [[semiconductor]]. It is a special class of material known as a **[[semimetal]]** (or **zero gap semiconductor**).

Furthermore, see the cone in the right figure. Those are the points of contact in the left plot (point $K$). Note how the behavior of the energy near the cone is about linear: this means that the dispersion relation between energy and [[wavenumber]] must itself be approximately linear, $E\sim k$: it must a Dirac dispersion relation, something that is only possible in two-dimensional systems.