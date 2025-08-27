---
wiki-publish: false
---
A 10x10x10cm block of iron weighs $m_\text{measured}=7.784 \text{ kg}$. We want to see if we can get this number from purely nuclear quantities.

The most common iron isotope, $^{56}\text{Fe}$, has $Z=26$ protons and $N=30$ neutrons. We'll use natural units until we can for convenience.
- Mass of a proton is $m_{p}=0.938\text{ GeV}$.
- Mass of a neutron is $m_{n}=0.9395\text{ GeV}$.
- Mass of an electron is $m_{e}=0.51\text{ MeV}$.

According to the semiempirical mass formula, the mass of an $^{56}\text{Fe}$ atom is given by
$$m_\text{Fe}(Z,A)=30m_{n}+26m_{p}+26m_{e}- \frac{B(Z,A)}{c^{2}}$$
where the binding energy is
$$B(Z,A)=56a_{v}-(14.64)a_{s}-\frac{650}{3.83}a_{c}-\frac{16}{224}a_{a}+(0.049)a_{p}=0.499\text{ GeV}$$
Putting it all together
$$m_\text{Fe}(Z,A)=52.096\text{ GeV}$$
To go from microscopic to macroscopic we employ crystal physics. Macroscopic iron at room temperature has a BCC crystal lattice, which contains two atoms per unit cell. Empirically, the unit cell has a lattice constant of $286.65\text{ pm}$. In a BCC, the lattice constant is just the cube's side, so the unit cell volume is $(286.65\text{ pm})^{3}=0.0235\text{ nm}^{3}$. This yields an atom density of $2/0.0235= 84.91\text{ atoms/nm}^{3}$. Since the 10x10x10cm block is itself cubic, finding the number of atoms is just a multiplication between block volume and atom density: there are approximately $8.49\times 10^{25}$ atoms in the block.

We'll ignore cohesive energy since it's too small to matter for the precision of this calculation. As such, the total rest energy of the iron is
$$m_\text{block}=8.49\times 10^{25}\text{ atoms} \cdot 52.096\ \frac{\text{GeV}}{\text{atom}}=4.422\times 10^{36}\text{ eV}$$
Converting back to real units:
$$\boxed{m_\text{block}=7.884\text{ kg}}$$
Close! This is overestimated by about $0.10\text{ kg}$. Part of this error is because have only used a single isotope of iron. In reality, there's a few stable isotopes of iron that you find in matter, with $^{56}\text{Fe}$ only accounting for about 91.8% of it all. To be more precise, let's add the other stable isotopes $^{54}\text{Fe}$ (5.85% abundance), $^{57}\text{Fe}$ (2.12% abundance) and $^{58}\text{Fe}$ (0.28% abundance). Using the semiempirical mass formula on these gives
$$m_{54\text{Fe}}=50.239\text{ GeV},\; m_{56\text{Fe}}=52.096\text{ GeV},\; m_{57\text{Fe}}=53.028\text{ GeV},\; m_{58\text{Fe}}=53.956\text{ GeV}$$
The weighed average of their rest energies is
$$m_{\text{Fe}}=52.038\text{ GeV}$$
which is smaller than $^{56}\text{Fe}$. If we use this to find the block's mass we get
$$\boxed{m_\text{block}=7.875\text{ kg}}$$
which is about $0.09\text{ kg}$ over, a small improvement.