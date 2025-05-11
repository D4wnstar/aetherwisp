---
wiki-publish: true
---
La **rappresentazione spettrale** di un [[operatore]] è una decomposizione in [[Serie]] dell'operatore nella [[base]] creata dai suoi stessi [[Equazione agli autovalori|autostati]].
### Spettro discreto
Consideriamo un [[operatore autoaggiunto]] $\hat{A}=\hat{A}^{+}$ nello [[spazio di Hilbert]] $\mathcal{H}=\mathbb{C}^{n}$. Diciamo che questo operatore ha [[Spettro]] discreto. Allora, i suoi [[Equazione agli autovalori|autostati]] (che sono [[Orthonormality|ortonormali]]) costituiscono una [[base]] ortonormale in $\mathcal{H}$, $\{ \ket{a_{i}} \}_{i=1}^{n}$. ha autovalori reali, infatti presa l'[[equazione agli autovalori]]
$$\hat{A}\ket{a_{i}} =a_{i}\ket{a_{i}} $$
vale
$$a_{i}=\overline{a_{i}}\quad\Leftrightarrow\quad a_{i}\in \mathbb{R}$$
e anche
$$\braket{ a_{i} | a_{j} } =\delta_{ij}$$
usando la [[Kronecker delta]]. Un qualunque vettore $\ket{\psi}\in \mathcal{H}$ può essere rappresentato come [[Serie di Fourier]] in questa base:
$$\ket{\psi} =\sum_{i=1}^{n} \braket{ a_{i} | \psi } \ket{a_{i}}=\left( \sum_{i=1}^{n} \ket{a_{i}} \bra{a_{i}}  \right)\ket{\psi} =\sum_{i=1}^{n} \hat{P}_{a_{i}}\ket{\psi}  $$
usando il [[proiettore]] $\hat{P}_{a_{i}}=\ket{a_{i}} \bra{a_{i}}$ sull'autostato $\ket{a_{i}}$ (un proiettore su un autostato è detto **autoproiettore**). Allora possiamo esprimere l'azione dell'operatore come
$$\hat{A}\ket{\psi} =\sum_{i=1}^{n} a_{i}\braket{ a_{i} | \psi } \ket{a_{i}} =\sum_{i=1}^{n} a_{i}\ket{a_{i}} \bra{a_{i}} \ket{\psi} =\left( \sum_{i=1}^{n} a_{i}\hat{P}_{a_{i}} \right)\ket{\psi} $$
ma allora possiamo scrivere
$$\boxed{\hat{A}=\sum_{i=1}^{n} a_{i}\hat{P}_{a_{i}}}$$
che è la **rappresentazione spettrale**, ossia una decomposizione in [[Serie]] di un operatore nella base creata dai suoi stessi autostati.