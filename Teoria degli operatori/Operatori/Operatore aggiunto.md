---
wiki-publish: true
aliases:
  - aggiunto
---
Presi due [[Spazio di Hilbert|spazi di Hilbert]] $H$ e $H'$, si dice **operatore aggiunto** $T^{+}$ (anche solo **aggiunto**, anche scritto $T^{\dagger}$) di un [[Operatore lineare]] $T:H \rightarrow H'$ un operatore per il quale vale
$$T^{+}:H'\rightarrow H\quad;\quad(y,Tx)=(T^{+}y,x)\quad\forall\;x,y\in H$$
Se l'operatore $T$ è limitato, allora ha sempre un aggiunto $T^{+}$ ed è anch'esso limitato e vale $||T||=||T^{+}||$. Inoltre, il dominio di $T^{+}$ coincide con tutto $H'$.
### Proprietà
Valgono le seguenti proprietà per due operatori limitati $T$ ed $S$
1. $(T^{+})^{+}=T$
2. $(T+S)^{+}=T^{+}+S^{+}$
3. $(\lambda T)^{+}=\lambda^{*}T^{+}$
4. $(TS)^{+}=S^{+}T^{+}$
### Forma matriciale
Dato che gli operatori aggiunti sono lineari, possono essere espressi in forma matriciale. In particolare, calcolando esplicitamente gli elementi si trova
$$(T^{+})_{ij}=(e_{i},T^{+}e_{j})=(Te_{i},e_{j})=(e_{j},Te_{i})^{*}=T_{ji}^{*}$$
ossia la matrice associata ad un operatore aggiunto è [[Matrice hermitiana|hermitiana]].
### Indipendenza da rappresentazione
L'aggiunto di un operatore $A$ è *indipendente dalla rappresentazione*.
$$\langle \phi|\hat{A}\psi\rangle=\langle A^{\dagger}\phi|\psi\rangle\;\forall|\phi\rangle,|\psi\rangle\in H$$
con $H$ [[spazio di Hilbert]].
$$\begin{align}\langle \phi|\hat{A}\psi\rangle&=\sum\limits_{i=1}^{n}\phi_{i}^{\ast}(\hat{A}\psi)_{i}=\sum\limits_{i=1}^{n}\sum\limits_{j=1}^{n}\phi_{i}^{\ast}(\hat{A}^{\ast}_{ij})^{\ast}\psi_{j}=\sum\limits_{i=1}^{n}\sum\limits_{j=1}^{n}(\phi_{i}\hat{A}^{\ast}_{ij})^{\ast}\psi_{j}\\
&=\sum\limits_{i=1}^{n}\sum\limits_{j=1}^{n}((\hat{A}^{\ast})^{T}_{ij}\phi_{i})\psi_{j} = \ldots=\langle \hat{A}^{\dagger}\psi|\phi\rangle
\end{align}$$
Abbiamo $|\chi\rangle\in H:\hat{A}=\hat{P}_{\chi}$ con $\hat{P}_{\chi}$ un [[proiettore]]. $\hat{P}_{\chi}|\phi\rangle=|\psi\rangle \langle \psi|\phi\rangle$. Allora ho
$$\langle \psi|\hat{P}_{\chi}\phi\rangle=\langle \psi|\langle \chi|\phi\rangle \chi\rangle=\langle \chi|\phi\rangle \langle \psi|\chi\rangle=\langle \langle \chi|\psi \chi\rangle|\phi\rangle=\langle \hat{P}_{\chi}\psi|\phi\rangle$$
Vogliamo anche provare che $\langle \hat{A}\psi|\phi\rangle=\langle \hat{B}\psi|\phi\rangle \Leftrightarrow \hat{A}=\hat{B}$. Consideriamo l'$ij$-esimo elemento $\langle i|\hat{A}|j\rangle=A_{ij}=\langle \hat{A}^{\dagger}i|j\rangle$ usando l'autoaggiuntezza.
$$0=\langle (\hat{A}-\hat{B})\psi|(\hat{A}-\hat{B})\psi\rangle=||(\hat{A}-\hat{B})\psi||^{2}\quad\forall\|\psi\rangle,|\phi\rangle\in H$$
dunque $\hat{A} = \hat{B}$.