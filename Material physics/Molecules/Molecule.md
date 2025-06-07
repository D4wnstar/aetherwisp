---
wiki-publish: true
---
A **molecule** is a bound [[Physical system|system]] of at least two [[Nucleo atomico|atomic nuclei]] and their [[electron|electrons]]. Molecules containing two nuclei are said to be **diatomic**, whereas ones containing more than two are said to be **polyatomic**. The [[stato|states]] in which the electrons are in are called [[molecular orbital|molecular orbitals]].

Compared to the study of [[atom|atoms]], the study of molecules is greatly complicated by the motion and interaction of the nuclei. Luckily however, much of this problem is lifted since the [[mass]] of the nuclei is considerably larger than that of the electrons, thus causing the nuclear states to be less significant overall. A ballpark estimate using the [[Frequency|angular frequencies]] of electron excitations $\omega_{e}$ and nuclear vibrations $\omega_{N}$ (more on this below) leads to a ratio $\omega_{N}/\omega_{e}\sim 10^{-3}\textendash10^{-5}$, several orders of magnitude less.

Moreover, not all electrons are bound to the nucleus with the same strength. Electrons in complete [[electron shell model|shells]] are bound to the nucleus much more strongly than electrons in the incomplete outermost shell, broadly speaking difference between $\sim 10\text{ eV}$ and $\sim 1\text{ eV}$. As such, only the outer electrons, the *valence* electrons, are assumed to take part in molecular bonding.
### Symmetries in diatomic molecules
Diatomic molecules are certainly the easiest case to deal with, in part due to the [[symmetry|symmetries]] that they present. To illustrate these, call $z$ the axis defined by the line between the two nuclei (the **bond axis**) and $\mathbf{L}$ the [[Momento angolare quantistico|quantum angular momentum]] of [[electron|electrons]] in a certain state. The projection of $\mathbf{L}$ on the $z$ axis and more so its [[Equazione agli autovalori|eigenvalues]] $M_{z}$
$$L_{z}\psi=M\psi,\quad M_{z}=0,\pm1,\pm2,\ldots$$
are a symmetry.

Just like how we use the [[spectroscopic notation]] letters to denote the angular states $l$ of atoms, we also use letters to denote the values of $M_{z}$ for molecular states. For molecular orbitals, we use $\Sigma,\Pi,\Delta$ and $\Phi$. For single-electron orbitals, we use their lowercase equivalents: $\sigma,\pi,\delta$ and $\phi$.

Another symmetry is with respect to the plane passing through the bond axis, such as the $xz$ plane or the $yz$ plane. [[Parità|Parity]] is symmetric about this plane. For instance, if we consider the $xz$ plane, the parity [[transformation]] $A_{y}:y\mapsto -y$ one the $y$ axis is a symmetry (in other words, the $y$ axis looks the same on both sides of the $xz$ plane; it's mirrored). Note that $L_{z}$ and $A_{y}$ do not commute, $[L_{z},A_{y}]\neq 0$. Specifically, applying $A_{y}$ maps $M_{z}$ to $-M_{z}$. This implies that, for any $M>0$, the states $\pm M$ have the same [[energy]].

One last symmetry is again parity, but with respect to the coordinate $r$. The transformation $A_{r}:r\mapsto-r$ is a symmetry.

So we have three symmetries: $L_{z}$, $A_{y}$ and $A_{r}$. The eigenvalues of these help to uniquely identify a state in a molecular system. Given a molecular orbital, say $\Pi$, we typically write these numbers around the orbital's letter, like so
$$1\Pi^{+}_{g}$$
The left number is $M_{z}$. The top left is the $y$ parity. Recall that the parity operator only has two eigenvalues, $\pm 1$, and we denote these as $+$ and $-$, with hopefully obvious meaning. Similarly $r$ parity also has two values, but to distinguish them from the $y$ parity, we use the initials of two German terms: *gerade* and *ungerade*, literally meaning even or odd respectively.

Below are a few examples.

![[Diagram Molecular orbital symmetries|100%]]

