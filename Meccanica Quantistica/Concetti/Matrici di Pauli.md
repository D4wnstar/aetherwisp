Le **matrici di Pauli** sono un insieme di tre matrici $2\times2$ in $\mathbb{C}^{2}$ che, date nella rappresentazione standard, sono
$$\hat{\sigma}_{x}=\left(\matrix{0 & 1 \\ 1 & 0}\right),\;\hat{\sigma}_{y}=\left(\matrix{0 & -i \\ i & 0}\right),\;\hat{\sigma}_{z}=\left(\matrix{1 & 0 \\ 0 & -1}\right)$$
Sono tutte e tre [[Operatore autoaggiunto|autoaggiunte]], ossia $\hat{\sigma}_{i}^{\dagger}=\hat{\sigma}_{i}$. Questo è un fatto importante e necessario dato che queste matrici sono derivate dallo studio dello [[Spin#Spin 1/2|spin 1/2]] delle [[Particella|particelle]]. Dato che lo spin è un [[osservabile]], l'[[operatore]] associato ad esso deve essere autoaggiunto.

I quadrati sono
$$\hat{\sigma}_{x}^{2}=\left(\matrix{0 & 1 \\ 1 & 0}\right)\left(\matrix{0 & 1 \\ 1 & 0}\right)=\left(\matrix{1 & 0 \\ 0 & 1}\right)=\hat{\mathbb{1}}$$
$$\hat{\sigma}_{y}^{2}=\left(\matrix{0 & -i \\ i & 0}\right)\left(\matrix{0 & -i \\ i & 0}\right)=\left(\matrix{1 & 0 \\ 0 & 1}\right)=\hat{\mathbb{1}}$$
$$\hat{\sigma}_{z}=\hat{\mathbb{1}}$$
Prendendo i vettori di spin up e down
$$|\uparrow z\rangle=\left(\matrix{1 \\ 0}\right)\;,\;|\downarrow z\rangle=\left(\matrix{0 \\ 1}\right)$$
$$\hat{\sigma}_{z}|\uparrow z\rangle=|\uparrow z\rangle\;,\;\hat{\sigma}_{z}|\downarrow z\rangle=-|\downarrow z\rangle$$
$$\hat{\sigma}_{x}|\uparrow z\rangle=|\downarrow z\rangle\;,\;\hat{\sigma}_{z}|\downarrow z\rangle=|\uparrow z\rangle$$
Quindi $\hat{\sigma}_{x}$ è il gate NOT (almeno in informazione quantistica).
$$\frac{|\uparrow z\rangle+|\downarrow z\rangle}{\sqrt{2}}=|\uparrow x\rangle= \frac{1}{\sqrt{2}} \left(\matrix{1 \\ 1}\right)$$
$$\frac{|\uparrow z\rangle-|\downarrow z\rangle}{\sqrt{2}}=|\downarrow x\rangle=\frac{1}{\sqrt{2}} \left(\matrix{1 \\ -1}\right)$$
che sono gli autostati di $\hat{\sigma}_{x}$, quindi sono la base per cui $\hat{\sigma}_{x}$ è diagonale. Questi due vettori formano la [[Matrice di Hadamard]].

Formalmente $\hat{\sigma}_{z}$ è
$$\hat{\tilde{\sigma}}_{z}=\left(\matrix{\langle\uparrow x|\hat{\sigma}_{z}|\uparrow x\rangle & \langle\uparrow x|\hat{\sigma}_{z}|\downarrow x\rangle \\ \langle\downarrow x|\hat{\sigma}_{z}|\uparrow x\rangle & \langle\downarrow x|\hat{\sigma}_{z}|\downarrow x\rangle}\right)=\left(\matrix{0 & 1 \\ 1 & 0}\right)$$

L'aggiunto di una matrice $A$ è *indipendente dalla rappresentazione*.
$$\langle \phi|\hat{A}\psi\rangle=\langle A^{\dagger}\phi|\psi\rangle\;\forall|\phi\rangle,|\psi\rangle\in\mathbb{H}$$
con $\mathbb{H}$ [[Spazio di Hilbert]].
$$\begin{align}\langle \phi|\hat{A}\psi\rangle&=\sum\limits_{i=1}^{n}\phi_{i}^{\ast}(\hat{A}\psi)_{i}=\sum\limits_{i=1}^{n}\sum\limits_{j=1}^{n}\phi_{i}^{\ast}(\hat{A}^{\ast}_{ij})^{\ast}\psi_{j}=\sum\limits_{i=1}^{n}\sum\limits_{j=1}^{n}(\phi_{i}\hat{A}^{\ast}_{ij})^{\ast}\psi_{j}\\
&=\sum\limits_{i=1}^{n}\sum\limits_{j=1}^{n}((\hat{A}^{\ast})^{T}_{ij}\phi_{i})\psi_{j} = \ldots=\langle \hat{A}^{\dagger}\psi|\phi\rangle
\end{align}$$
Abbiamo $|\chi\rangle\in\mathbb{H}:\hat{A}=\hat{P}_{\chi}$ con $\hat{P}_{\chi}$ un [[Proiettore]]. $\hat{P}_{\chi}|\phi\rangle=|\psi\rangle \langle \psi|\phi\rangle$. Allora ho
$$\langle \psi|\hat{P}_{\chi}\phi\rangle=\langle \psi|\langle \chi|\phi\rangle \chi\rangle=\langle \chi|\phi\rangle \langle \psi|\chi\rangle=\langle \langle \chi|\psi \chi\rangle|\phi\rangle=\langle \hat{P}_{\chi}\psi|\phi\rangle$$
Vogliamo anche provare che $\langle \hat{A}\psi|\phi\rangle=\langle \hat{B}\psi|\phi\rangle \Leftrightarrow \hat{A}=\hat{B}$. Consideriamo l'$ij$-esimo elemento $\langle i|\hat{A}|j\rangle=A_{ij}=\langle \hat{A}^{\dagger}i|j\rangle$ usando l'autoaggiuntezza.
$$0=\langle (\hat{A}-\hat{B})\psi|(\hat{A}-\hat{B})\psi\rangle=||(\hat{A}-\hat{B})\psi||^{2}\quad\forall\|\psi\rangle,|\phi\rangle\in\mathbb{H}$$
dunque $\hat{A} = \hat{B}$.