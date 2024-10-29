La **dualità** in fisica quantistica è la relazione tra la *picture* di Schrödinger, in cui evolvono gli [[Stato|stati]], e la *picture* di Heisenberg, in cui evolvono gli [[Operatore|operatori]]. Questi due punti di vista sono equivalenti e quale viene usato è interamente una questione di preferenza. Si tratta dell'analogo quantistico dell'equivalenza di sistemi di riferimento (come guardare un treno dalla banchina o essere sul treno e guardare fuori).

Nella *picture* di Schrödinger è lo stato ad evolversi nel tempo. Preso uno stato $\psi$, esso si evolve con l'[[evolutore]] con
$$|\psi\rangle \rightarrow |\psi_{t}\rangle=\hat{U}_{t}|\psi_{t}\rangle$$
e il valor medio di una [[osservabile]] $Q$ con [[operatore autoaggiunto]] $\hat{Q}$ si esprime
$$\left\langle Q \right\rangle = \langle \psi_{t}|\hat{Q}|\psi_{t}\rangle$$

Nella *picture* di Heisenberg è l'operatore dell'osservabile a evolvere.
$$\hat{Q}\rightarrow\hat{Q}_{t}=\hat{U}_{t}^{-1} \hat{Q}\hat{U}_{t}$$
e il valor medio si esprime invece
$$\left\langle Q \right\rangle=\langle \psi|\hat{Q}_{t}|\psi\rangle$$

I due valori medi *sono uguali*, come si dimostra
$$\langle \psi_{t}|\hat{A}\psi_{t}\rangle=\langle \hat{U}_{t}\psi|\hat{A}\hat{U}_{t}\psi\rangle=\langle \psi|\hat{U}_{t}^{\dagger}\hat{A}\hat{U}_{t}\psi\rangle=\langle \psi|\hat{A}_{t}\psi\rangle$$

Prendo l'[[Hamiltoniana]] della dinamica libera $\hat{H}=\frac{\hat{\bar{p}}^{2}}{2m}= \frac{\hat{p}^{2}_{x}+\hat{p}^{2}_{y}+\hat{p}^{2}_{z}}{2m}$.
$$\hat{x}_{t}=e^{\frac{i}{\hbar} \frac{\hat{\bar{p}}^{2}}{2m}t}\quad;\quad\hat{x}=e^{-\frac{i}{\hbar} \frac{\hat{\bar{p}}^{2}}{2m}t}$$
$$\partial_{t}\hat{x}_{t}=\frac{i}{\hbar}\left[ \frac{\hat{\bar{p}}^{2}}{2m}, \hat{U}^{\dagger}_{t}\hat{x}\hat{U}_{t} \right]=\frac{i}{\hbar}\hat{U}^{\dagger}_{t}\left[ \frac{\hat{\bar{p}}^{2}}{2m}, \hat{x} \right]\hat{U}_{t}= \frac{i}{2m\hbar}\hat{U}^{\dagger}_{t}\left[ \hat{p}^{2}_{x}, \hat{x} \right]\hat{U}_{t}=\frac{1}{m}\hat{U}^{\dagger}_{t}\hat{p}_{x}\hat{U}_{t}=\frac{\hat{p}_{x}}{m}$$
usando che $[\hat{p}^{2}_{x}, \hat{x}]=\hat{p}_{x}[\hat{p}_{x},\hat{x}]+[\hat{p}_{x},\hat{x}]\hat{p}_{x}=-2i\hbar \hat{p}_{x}$ e
$$\hat{U}_{t}^{\dagger}\hat{p}_{x}=e^{\frac{it}{\hbar} \frac{\hat{\bar{p}}^{2}}{2m}}\hat{p}_{x}=\sum\limits_{i=0}^{\infty}\left( \frac{it}{2\hbar m} \right)\ldots$$
$$\partial_{t}\hat{p}_{x,t}=\left[ \hat{\bar{p}}^{2},\hat{p}^{2}_{x} \right]=0$$
per le proprietà del [[Commutatore]].