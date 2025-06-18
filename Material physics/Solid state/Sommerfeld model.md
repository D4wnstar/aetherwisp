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
The boundary conditions are periodic (**[[Born-von Karman boundary conditions]]**): $\psi(x_{i}+L)=\psi(x_{i})$. The [[Equazione agli autovalori|eigenvalues]] and eigenfunctions are
$$E(\mathbf{k})=\frac{\hbar^{2}k^{2}}{2m},\qquad \psi_{k}(\mathbf{r})=\frac{1}{\sqrt{ V }}e^{i\mathbf{k}\cdot \mathbf{r}}$$
Using the [[Thomas-Fermi approximation]], as outlined in the Fermi gas article, we can find the electron density to be
$$n=\frac{k_{F}^{3}}{3\pi ^{2}}$$
where $k_{F}$ is the [[Fermi energy|Fermi wavevector]], the wavevector of the most energetic electron of the gas. It is also the radius of the [[sphere]] in [[reciprocal space]] that contains all of the possible one-electron levels. A few other notable quantities are the Fermi velocity $v_{F}=\hbar k_{F}/m$, which comes out to be about 1% of the [[speed of light]] for most metals at zero [[temperature]], and the [[Fermi energy]], which is the energy of the most energetic electron in the gas. The surface of the sphere is called the [[Fermi surface]] and it divides occupied states from unoccupied states. It only makes sense at zero temperature; higher temperature cause the boundary to be fuzzy due to thermal excitations. That said, using the Fermi temperature $T_{F}=E_{F}/k_{B}$ gives an estimate of the kind of temperatures needed for thermal excitations to be significant (i.e. blur the Fermi surface a lot). For electrons in metal, this is often in the tens of thousands of Kelvins, $\sim 10^{4}\text{ K}$.

For convenience, we can also define another quantity $r_{S}$ as the radius of a hypothetical sphere whose volume is equal to the [[mean]] volume per free electron. This is *not* the volume of the electrons themselves (as far as we know, electrons are zero-dimensional), it's just a uniform division of space for each electron. It's like having four people in a room, and giving each person a quarter of the room. The four people aren't as large as a quarter of the room, it's just the space that's assigned to each. The definition is as simple as
$$\frac{V}{N}=\frac{1}{n}\simeq \frac{4}{3}\pi r_{S}^{3}\quad\Rightarrow \quad r_{S}=\left( \frac{3}{4\pi n} \right)^{3}$$
$r_{S}$ is known as the **Wigner-Seitz radius**. It is different from the radius of the sphere used in the Thomas-Fermi approximation, as $k_{F}$ is in reciprocal space and $r_{S}$ is in real space, but the two are closely related by
$$k_{F}=\frac{(9\pi/4)^{1/3}}{r_{S}}=\frac{1.92}{r_{S}}$$
It is typically found by determining $n$ and using the formula above. It's often given in units of [[Bohr radius]] to make it a dimensionless parameter: $r_{S}/a_{0}$. Using realistic numbers, it's somewhere between $2$ and $6$ ($2\leq r_{S}/a_{0}\leq 6$).

The [[internal energy]] volume density is given by
$$\frac{E}{V}=\frac{1}{4\pi ^{3}}\int_{k<k_{F}} \frac{\hbar^{2}k^{2}}{2m}d\mathbf{k}=\frac{1}{\pi ^{2}} \frac{\hbar^{2}k_{F}^{5}}{10m}$$
Meanwhile, the internal energy particle density is
$$\frac{E}{N}=\frac{E}{V} \frac{V}{N}=\frac{1}{\pi ^{2}} \frac{\hbar^{2}k^{5}}{10m} \frac{1}{n}=\frac{3}{10} \frac{\hbar^{2}k_{F}^{2}}{m}=\frac{3}{5} k_{B}T_{F}=\frac{3}{5}E_{F}$$
The theory developed until now expects the metal to be at absolute zero (read: temperature very low compared to $T_{F}$). Extending to nonzero temperature (read: temperatures getting close to $T_{F}$) is complicated, as the integrals required become formidable. The solution is to use the [[Sommerfeld expansion]] of the Fermi gas integrals, and that is shown under [[Fermi gas#Nonzero temperature]].