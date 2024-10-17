Le **matrici di Pauli** sono un insieme di tre matrici $2\times2$ in $\mathbb{C}^{2}$ che, date nella rappresentazione standard, sono
$$\hat{\sigma}_{x}=\pmatrix{0 & 1 \\ 1 & 0},\quad\hat{\sigma}_{y}=\pmatrix{0 & -i \\ i & 0},\quad\hat{\sigma}_{z}=\pmatrix{1 & 0 \\ 0 & -1}$$
Sono tutte e tre [[Operatore autoaggiunto|autoaggiunte]], ossia $\hat{\sigma}_{i}^{\dagger}=\hat{\sigma}_{i}$, e [[Operatore unitario|unitarie]]. Questo è un fatto importante e necessario dato che queste matrici sono derivate dallo studio dello [[Spin#Spin 1/2|spin 1/2]] delle [[Particella|particelle]]. Infatti, dato che lo spin è un [[osservabile]], l'[[operatore]] associato ad esso deve essere autoaggiunto.
### Proprietà
I quadrati sono tutti unitari:
$$\hat{\sigma}_{x}^{2}=\left(\matrix{0 & 1 \\ 1 & 0}\right)\left(\matrix{0 & 1 \\ 1 & 0}\right)=\left(\matrix{1 & 0 \\ 0 & 1}\right)=\hat{\mathbb{1}}$$
$$\hat{\sigma}_{y}^{2}=\left(\matrix{0 & -i \\ i & 0}\right)\left(\matrix{0 & -i \\ i & 0}\right)=\left(\matrix{1 & 0 \\ 0 & 1}\right)=\hat{\mathbb{1}}$$
$$\hat{\sigma}_{z}=\pmatrix{1 & 0 \\ 0 & -1}\pmatrix{1 & 0 \\ 0 & -1}=\pmatrix{1 & 0 \\ 0 & 1}=\hat{\mathbb{1}}$$

Prendendo i vettori di [[Equazione agli autovalori|autostato]] spin up e down
$$|\uparrow z\rangle=\left(\matrix{1 \\ 0}\right)\qquad|\downarrow z\rangle=\left(\matrix{0 \\ 1}\right)$$
possiamo trovare i loro autovalori rispetto alla matrici $z$
$$\hat{\sigma}_{z}|\uparrow z\rangle=|\uparrow z\rangle,\qquad\hat{\sigma}_{z}|\downarrow z\rangle=-|\downarrow z\rangle$$
che quindi sono $1$ e $-1$. Se invece cerchiamo i [[Proiettore|proiettori]] su questi autostati troviamo
$$\hat{P}_{\uparrow}=\ket{\uparrow z} \bra{\uparrow z} =\begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix}\qquad \hat{P}_{\downarrow}=\ket{\downarrow z} \bra{\downarrow z} =\begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix}$$
Per una particella, lo stato di spin è un vettore in $\mathbb{C}^{2}$. Le probabilità di essere in uno stato di spin sono tali che
$$\lvert \braket{ \uparrow z | \psi } \rvert^{2} + \lvert \braket{ \downarrow z | \psi }  \rvert ^{2}=1 $$
e usando la [[rappresentazione spettrale]] troviamo
$$\ket{\psi} =\braket{ \uparrow z | \psi } \ket{\uparrow z} +\braket{ \downarrow z | \psi } \ket{\downarrow z} = \hat{P}_{\uparrow}\ket{\psi} +\hat{P}_{\downarrow}\ket{\psi} $$
Possiamo anche facilmente definire la [[matrice di densità]] come
$$\rho=\braket{ \uparrow z| \psi }\hat{P}_{\uparrow} +\braket{ \downarrow | \psi } \hat{P}_{\downarrow}=\begin{pmatrix}
\lvert \braket{ \uparrow z | \psi }  \rvert ^{2} & 0 \\
0 & \lvert \braket{ \downarrow z | \psi }  \rvert ^{2}
\end{pmatrix}$$

Se invece applichiamo la matrice $x$ troviamo
$$\hat{\sigma}_{x}|\uparrow z\rangle=|\downarrow z\rangle,\qquad\hat{\sigma}_{x}|\downarrow z\rangle=|\uparrow z\rangle$$
Quindi $\hat{\sigma}_{x}$ è il gate NOT (almeno in informazione quantistica).
$$\frac{|\uparrow z\rangle+|\downarrow z\rangle}{\sqrt{2}}=|\uparrow x\rangle= \frac{1}{\sqrt{2}} \left(\matrix{1 \\ 1}\right)$$
$$\frac{|\uparrow z\rangle-|\downarrow z\rangle}{\sqrt{2}}=|\downarrow x\rangle=\frac{1}{\sqrt{2}} \left(\matrix{1 \\ -1}\right)$$
che sono gli [[Equazione agli autovalori|autovettori]] di $\hat{\sigma}_{x}$, quindi sono la base per cui $\hat{\sigma}_{x}$ è diagonale. Questi due vettori formano la [[matrice di Hadamard]].
### Rappresentazione formale
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