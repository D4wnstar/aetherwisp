Le **matrici di Pauli** sono un insieme di tre matrici $2\times2$ in $\mathbb{C}^{2}$ che, date nella rappresentazione standard, sono
$$\hat{\sigma}_{x}=\pmatrix{0 & 1 \\ 1 & 0},\;\hat{\sigma}_{y}=\pmatrix{0 & -i \\ i & 0},\;\hat{\sigma}_{z}=\pmatrix{1 & 0 \\ 0 & -1}$$
Sono tutte e tre [[Operatore autoaggiunto|autoaggiunte]], ossia $\hat{\sigma}_{i}^{\dagger}=\hat{\sigma}_{i}$. Questo è un fatto importante e necessario dato che queste matrici sono derivate dallo studio dello [[Spin#Spin 1/2|spin 1/2]] delle [[Particella|particelle]]. Infatti, dato che lo spin è un [[osservabile]], l'[[operatore]] associato ad esso deve essere autoaggiunto.

I quadrati sono tutti unitari:
$$\hat{\sigma}_{x}^{2}=\left(\matrix{0 & 1 \\ 1 & 0}\right)\left(\matrix{0 & 1 \\ 1 & 0}\right)=\left(\matrix{1 & 0 \\ 0 & 1}\right)=\hat{\mathbb{1}}$$
$$\hat{\sigma}_{y}^{2}=\left(\matrix{0 & -i \\ i & 0}\right)\left(\matrix{0 & -i \\ i & 0}\right)=\left(\matrix{1 & 0 \\ 0 & 1}\right)=\hat{\mathbb{1}}$$
$$\hat{\sigma}_{z}=\pmatrix{1 & 0 \\ 0 & -1}\pmatrix{1 & 0 \\ 0 & -1}=\pmatrix{1 & 0 \\ 0 & 1}=\hat{\mathbb{1}}$$
Prendendo i vettori di spin up e down
$$|\uparrow z\rangle=\left(\matrix{1 \\ 0}\right)\;,\;|\downarrow z\rangle=\left(\matrix{0 \\ 1}\right)$$
$$\hat{\sigma}_{z}|\uparrow z\rangle=|\uparrow z\rangle\;,\;\hat{\sigma}_{z}|\downarrow z\rangle=-|\downarrow z\rangle$$
$$\hat{\sigma}_{x}|\uparrow z\rangle=|\downarrow z\rangle\;,\;\hat{\sigma}_{z}|\downarrow z\rangle=|\uparrow z\rangle$$
Quindi $\hat{\sigma}_{x}$ è il gate NOT (almeno in informazione quantistica).
$$\frac{|\uparrow z\rangle+|\downarrow z\rangle}{\sqrt{2}}=|\uparrow x\rangle= \frac{1}{\sqrt{2}} \left(\matrix{1 \\ 1}\right)$$
$$\frac{|\uparrow z\rangle-|\downarrow z\rangle}{\sqrt{2}}=|\downarrow x\rangle=\frac{1}{\sqrt{2}} \left(\matrix{1 \\ -1}\right)$$
che sono gli [[Equazione agli autovalori|autovettori]] di $\hat{\sigma}_{x}$, quindi sono la base per cui $\hat{\sigma}_{x}$ è diagonale. Questi due vettori formano la [[matrice di Hadamard]].

La rappresentazione formale di $\hat{\sigma}_{z}$ è
$$\hat{\tilde{\sigma}}_{z}=\left(\matrix{\langle\uparrow x|\hat{\sigma}_{z}|\uparrow x\rangle & \langle\uparrow x|\hat{\sigma}_{z}|\downarrow x\rangle \\ \langle\downarrow x|\hat{\sigma}_{z}|\uparrow x\rangle & \langle\downarrow x|\hat{\sigma}_{z}|\downarrow x\rangle}\right)=\left(\matrix{0 & 1 \\ 1 & 0}\right)$$

I commutatori tra le matrici sono
$$[\sigma_{1},\sigma_{2}]=2i\sigma_{3}, \quad [\sigma_{2},\sigma_{3}]=2i\sigma_{1}, \quad [\sigma_{3},\sigma_{1}]=2i\sigma_{2}$$
o più in generale
$$[\sigma_{i},\sigma_{j}]=2i\epsilon_{ijk}\sigma_{k}$$
dove $\epsilon_{ijk}$ è il [[tensore di Levi-Civita]]. Le tre relazioni precedenti si ritrovano quando $i$, $j$ e $k$ sono diversi fra loro o se c'è un numero pari di scambi fra loro. Inoltre, le matrici anticommutano
$$\{\sigma_{i},\sigma_{j}\}=2\delta_{ij}$$

Dai commutatori si ottengono anche le relazioni
$$\sigma_{1}\sigma_{2}=-\sigma_{2}\sigma_{1}, \quad \sigma_{2}\sigma_{3}=-\sigma_{3}\sigma_{2}, \quad \sigma_{1}\sigma_{3}=-\sigma_{3}\sigma_{1}$$