---
wiki-publish: true
---
The **Sommerfeld model** is a quantum treatment of free [[electron|electrons]] in metals. It can be seen as a quantum rework of the [[Drude model]]. It is based on three approximations:
1. The $N$ electrons are confined in a cubic volume $V=L^{3}$.
2. The electrons are independent. There is no interaction between electrons.
3. The electrons are free. There is no interaction between electrons and ions.

These assumptions might sound inherently wrong; of course electrons would interact with each other and with ions. But besides making the model mathematically simpler, these are inherited from the older Drude model, which provided good results even with these assumptions.
### Derivation
This model is essentially a [[Fermi gas#3d|3D Fermi gas]] with PBC. See that page for more details. We start from the [[Equazione di Schrödinger|Schrödinger equation]] for the [[Particella libera (quantistica)|free particle]]:
$$- \frac{\hbar^{2}}{2m}\left( \frac{ \partial ^{2} }{ \partial x^{2} } +\frac{ \partial ^{2} }{ \partial y^{2} } +\frac{ \partial ^{2} }{ \partial z^{2} }  \right)\psi(\mathbf{r})=- \frac{\hbar^{2}}{2m}\nabla ^{2}\psi(\mathbf{r})=E\psi(\mathbf{r})$$
The boundary conditions are periodic[^1]: $\psi(x_{i}+L)=\psi(x_{i})$. The [[Equazione agli autovalori|eigenvalues]] and eigenvectors are
$$E(\mathbf{k})=\frac{\hbar^{2}k^{2}}{2m},\qquad \psi_{k}(\mathbf{r})=\frac{1}{\sqrt{ V }}e^{i\mathbf{k}\cdot \mathbf{r}}$$
Using the [[Thomas-Fermi approximation]], as outlined in the Fermi gas article, we can find the electron density to be
$$n=\frac{k_{F}^{3}}{3\pi ^{2}}$$
where $k_{F}$ is the [[Fermi energy|Fermi wavevector]]. For convenience, we can also define another quantity to represent the radius $r_{S}$ of a hypothetical sphere where all of the electrons would be contained in. We have
$$\frac{V}{N}=\frac{1}{n}\simeq \frac{4}{3}\pi r_{S}^{3}\quad\Rightarrow \quad r_{S}=\left( \frac{3}{4\pi n} \right)^{3}$$
$r_{S}$ is known as the **Wigner-Seitz radius**. It is different from the radius of the sphere used in the Thomas-Fermi approximation, as that is in [[reciprocal space]], and its radius is the Fermi wavevector. The two are related by
$$k_{F}=\frac{(9\pi/4)^{1/3}}{r_{S}}=\frac{1.92}{r_{S}}$$
It is typically found indirectly by first determining $n$ and then using the formula above. Using realistic numbers, this radius is generally somewhere between $2$ and $6$ [[Bohr radius|Bohr radii]] ($2\leq r_{S}/a_{0}\leq 6$).

The internal energy volume density is given by
$$\frac{E}{V}=\frac{1}{4\pi ^{3}}\int_{k<k_{F}} \frac{\hbar^{2}k^{2}}{2m}d\mathbf{k}=\frac{1}{\pi ^{2}} \frac{\hbar^{2}k_{F}^{5}}{10m}$$
Meanwhile, the energy particle density is
$$\frac{E}{N}=\frac{E}{V} \frac{V}{N}=\frac{1}{\pi ^{2}} \frac{\hbar^{2}k^{5}}{10m} \frac{1}{n}=\frac{3}{10} \frac{\hbar^{2}k_{F}^{2}}{m}=\frac{3}{5} k_{B}T_{F}=\frac{3}{5}E_{F}$$
where $T_{F}$ is the [[Fermi energy|Fermi temperature]] and $E_{F}$ is the [[Fermi energy]].

[^1]: Also called **Born-Von Karman boundary conditions**.