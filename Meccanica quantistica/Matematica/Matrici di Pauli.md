Le **matrici di Pauli** sono un insieme di tre matrici $2\times2$ in $\mathbb{C}^{2}$ che, date nella rappresentazione standard, sono
$$\hat{\sigma}_{x}=\pmatrix{0 & 1 \\ 1 & 0},\quad\hat{\sigma}_{y}=\pmatrix{0 & -i \\ i & 0},\quad\hat{\sigma}_{z}=\pmatrix{1 & 0 \\ 0 & -1}$$
Sono tutte e tre [[Operatore autoaggiunto|autoaggiunte]], ossia $\hat{\sigma}_{i}^{\dagger}=\hat{\sigma}_{i}$, e [[Operatore unitario|unitarie]]. Questo è un fatto importante e necessario dato che queste matrici sono derivate dallo studio dello [[Spin#Spin 1/2|spin 1/2]] delle [[Particella|particelle]]. Infatti, dato che lo spin è un [[osservabile]], l'[[operatore]] associato ad esso deve essere autoaggiunto. In rappresentazione standard, $\hat{\sigma}_{z}$ è diagonale, mentre le altre due no.

È comune anche usare gli indici $(1,2,3)$ anziché $(x,y,z)$.
### Proprietà
I quadrati sono tutti unitari:
$$\hat{\sigma}_{x}^{2}=\left(\matrix{0 & 1 \\ 1 & 0}\right)\left(\matrix{0 & 1 \\ 1 & 0}\right)=\left(\matrix{1 & 0 \\ 0 & 1}\right)=\hat{\mathbf{1}}$$
$$\hat{\sigma}_{y}^{2}=\left(\matrix{0 & -i \\ i & 0}\right)\left(\matrix{0 & -i \\ i & 0}\right)=\left(\matrix{1 & 0 \\ 0 & 1}\right)=\hat{\mathbf{1}}$$
$$\hat{\sigma}_{z}^{2}=\pmatrix{1 & 0 \\ 0 & -1}\pmatrix{1 & 0 \\ 0 & -1}=\pmatrix{1 & 0 \\ 0 & 1}=\hat{\mathbf{1}}$$
### Matrice $\hat{\sigma}_{z}$
Tutte le matrici hanno una rappresentazione nella [[base]] dei propri [[Equazione agli autovalori|autovettori]]. Per la matrice $\hat{\sigma}_{z}$, gli [[Equazione agli autovalori|autostati]] spin up e down sull'asse $z$ sono
$$|\uparrow z\rangle=\left(\matrix{1 \\ 0}\right)\qquad|\downarrow z\rangle=\left(\matrix{0 \\ 1}\right)$$
e possiamo trovare i loro autovalori rispetto alla matrici $z$
$$\hat{\sigma}_{z}|\uparrow z\rangle=|\uparrow z\rangle,\qquad\hat{\sigma}_{z}|\downarrow z\rangle=-|\downarrow z\rangle$$
che quindi sono $1$ e $-1$. Possiamo anche cercare i [[Proiettore|proiettori]] su questi autostati:
$$\hat{P}_{\uparrow}=\ket{\uparrow z} \bra{\uparrow z} =\begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix}\qquad \hat{P}_{\downarrow}=\ket{\downarrow z} \bra{\downarrow z} =\begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix}$$
In questa base, $\hat{\sigma}_{z}$ è una matrice diagonale. È possibile trovare gli autostati di ciascuna matrice e rappresentarle tutte in quella base per scegliere quale delle tre è diagonale. In genere le si tiene rappresentate nella base di $\hat{\sigma}_{z}$, nella quale $\hat{\sigma}_{x}$ e $\hat{\sigma}_{y}$ non sono diagonali.

Per una particella, lo stato di spin è un vettore in $\mathbb{C}^{2}$. Le probabilità di essere in uno stato di spin sono tali che
$$\lvert \braket{ \uparrow z | \psi } \rvert^{2} + \lvert \braket{ \downarrow z | \psi }  \rvert ^{2}=1 $$
e usando la [[rappresentazione spettrale]] troviamo
$$\ket{\psi} =\braket{ \uparrow z | \psi } \ket{\uparrow z} +\braket{ \downarrow z | \psi } \ket{\downarrow z} = \hat{P}_{\uparrow}\ket{\psi} +\hat{P}_{\downarrow}\ket{\psi} $$
Possiamo anche trovare la [[matrice di densità]] come
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

La rappresentazione formale di $\hat{\sigma}_{z}$ è nella base degli autostati di $\hat{\sigma}_{x}$:
$$\hat{\tilde{\sigma}}_{z}=\left(\matrix{\langle\uparrow x|\hat{\sigma}_{z}|\uparrow x\rangle & \langle\uparrow x|\hat{\sigma}_{z}|\downarrow x\rangle \\ \langle\downarrow x|\hat{\sigma}_{z}|\uparrow x\rangle & \langle\downarrow x|\hat{\sigma}_{z}|\downarrow x\rangle}\right)=\left(\matrix{0 & 1 \\ 1 & 0}\right)$$
nella quale non è più diagonale.
### Commutatori
I [[Commutatore|commutatori]] tra le matrici sono
$$[\sigma_{1},\sigma_{2}]=2i\sigma_{3}, \quad [\sigma_{2},\sigma_{3}]=2i\sigma_{1}, \quad [\sigma_{3},\sigma_{1}]=2i\sigma_{2}$$
o più in generale
$$[\sigma_{i},\sigma_{j}]=2i\epsilon_{ijk}\sigma_{k}$$
dove $\epsilon_{ijk}$ è il [[tensore di Levi-Civita]]. Le tre relazioni precedenti si ritrovano quando $i$, $j$ e $k$ sono diversi fra loro o se c'è un numero pari di scambi fra loro. Inoltre, le matrici anticommutano
$$\{\sigma_{i},\sigma_{j}\}=2\delta_{ij}$$

Dai commutatori si ottengono anche le relazioni
$$\sigma_{1}\sigma_{2}=-\sigma_{2}\sigma_{1}, \quad \sigma_{2}\sigma_{3}=-\sigma_{3}\sigma_{2}, \quad \sigma_{1}\sigma_{3}=-\sigma_{3}\sigma_{1}$$
Questa ciclicità è molto simile a quello che accade con le [[Poisson bracket]] del momento angolare in meccanica classica. Non per altro, le matrici di Pauli rappresentano lo spin di un sistema quantistico.
### Forma in assi arbitrari
Considera un generico versore in spazio tridimensionale:
$$\hat{\mathbf{n}}=(n_{x},n_{y},n_{z})\in \mathbb{R}^{3}$$
Questa denota una qualche direzione nello spazio. Introduciamo dunque la matrice $\hat{\sigma}_{n}$ come
$$\hat{\sigma}_{n}=\hat{\mathbf{n}}\cdot \hat{\boldsymbol{\sigma}}=n_{x}\hat{\sigma}_{x}+n_{y}\hat{\sigma}_{y}+n_{z}\hat{\sigma}_{z}$$
dove $\hat{\boldsymbol{\sigma}}$ è il vettore $(\hat{\sigma}_{x},\hat{\sigma}_{y},\hat{ \sigma}_{z})$ e $\cdot$ è il [[prodotto scalare]]. In rappresentazione standard questo dà
$$\hat{\sigma}_{n}=\begin{pmatrix}
 n_{z} & n_{x}-in_{y} \\
n_{x}+in_{y}  & -n_{z}
\end{pmatrix}$$
Questa è la forma generica proiettata sulla direzione $\hat{\mathbf{n}}$ delle matrici di Pauli. Se aggiungiamo un $\hbar/2$ davanti a $\hat{\boldsymbol{\sigma}}$, questo diventa il vettore momento angolare della particella (a spin 1/2) e $(\hbar/2)\hat{\sigma}_{n}$ è la proiezione di quel momento angolare sulla direzione $\hat{\mathbf{n}}$. Naturalmente, se $\hat{\mathbf{n}}$ è pari ad uno degli assi cartesiani, $\hat{\sigma}_{n}$ diventa uguale a $\hat{\sigma}_{x}$, $\hat{\sigma}_{y}$ o $\hat{\sigma}_{z}$ e ritorna la componente del momento angolare intrinseco su quell'asse.

La matrice $\hat{\sigma}_{n}$ è importante per poter trattare momenti angolari non disposti su un asse. Se si trovassero altri due versori [[Ortonormalità|ortonormali]] ad $\hat{\mathbf{n}}$ (per esempio mediante [[ortonormalizzazione di Gram-Schmidt]]), si costruirebbe una nuova terna di assi ortonormali [[Rotation|ruotata]] rispetto a quella standard cartesiana.

> [!example] Due versori
> Consideriamo due versori $\hat{\mathbf{n}}_{1}$ e $\hat{\mathbf{n}}_{2}$ in $\mathbb{R}^{3}$. Le componenti di un momento angolare su questi due assi saranno rispettivamente $\hat{\sigma}_{n_{1}}=\hat{\mathbf{n}}_{1}\cdot \hat{\boldsymbol{\sigma}}$ e $\hat{\sigma}_{n_{2}}=\hat{\mathbf{n}}_{2}\cdot \hat{\boldsymbol{\sigma}}$. Vogliamo trovare il prodotto delle matrici $\hat{\sigma}_{n_{1}}$ e $\hat{\sigma}_{n_{2}}$.
> 
> Usiamo la definizione di prodotto riga per colonna
> $$\hat{\sigma}_{n_{1}}\hat{\sigma}_{n_{2}}=\sum_{j=x,y,z;\ k=x,y,z} \hat{\sigma}_{j}n_{1,j}\hat{\sigma}_{k}n_{2,k}=\ldots$$
> Distinguiamo questa somma in due somme, una quando gli indici sono uguali e una quando gli indici sono diversi
> $$\ldots=\sum_{j=k} \underbrace{ \hat{\sigma}_{j}\hat{\sigma}_{j} }_{ \hat{\mathbf{1}} }n_{1,j}n_{2,j}+\sum_{j\neq k} \hat{\sigma}_{j}\hat{\sigma}_{k}n_{1,j}n_{2,k}=\ldots$$
> dato che il quadrato di una matrice di Pauli è la matrice identica. Ma allora il primo termine diventa
> $$\ldots=\hat{\mathbf{n}}_{1}\cdot\hat{\mathbf{n}}_{2}+\sum_{j\neq k} \hat{\sigma}_{j}\hat{\sigma}_{k}n_{1,j}n_{2,k}=\ldots$$
> dove è stata omessa la matrice identica per semplicità (più correttamente, il primo termine dovrebbe essere $(\hat{\mathbf{n}}_{1}\cdot \hat{\mathbf{n}}_{2})\hat{\mathbf{1}}$). Per il secondo termine possiamo usare la relazione con il tensore di Levi-Civita
> $$\ldots=\hat{\mathbf{n}}_{1}\cdot \hat{\mathbf{n}}_{2}+i\sum_{i=j}\epsilon_{ijk}n_{i}n_{j}\hat{\sigma}_{k}=\ldots$$
> ma i termini della somma sono solo [[prodotto vettoriale|prodotti vettoriali]] in forma tensoriale:
> $$\ldots=\hat{\mathbf{n}}_{1}\cdot \hat{\mathbf{n}}_{2}+\sum_{i=x,y,z}(\hat{\mathbf{n}}_{1}\times \hat{\mathbf{n}}_{2})\hat{\sigma}_{i}$$
> ma la seconda somma adesso è un prodotto scalare, quindi ci rimane
> $$\hat{\sigma}_{n_{1}}\hat{\sigma}_{n_{2}}=\hat{\mathbf{n}}_{1}\cdot \hat{\mathbf{n}}_{2}+(\hat{\mathbf{n}}_{1}\times \hat{\mathbf{n}}_{2})\cdot \hat{\boldsymbol{\sigma}}$$
> Questa matrice continua ad essere hermitiana e con quadrato unitario $(\hat{\sigma}_{n_{1}}\hat{\sigma}_{n_{2}})^{2}=\hat{\mathbf{1}}$.

È interessare studiare quali sono i due [[Proiettore|proiettori]] di $\hat{\sigma}_{n}$, $\hat{P}_{+n}$ e $\hat{P}_{-n}$. Dato che gli autovalori di $\hat{\sigma}_{n}$ sono sempre $1$ e $-1$, possiamo usare la [[rappresentazione spettrale]]:
$$\hat{\sigma}_{n}=\hat{P}_{+n}-\hat{P}_{-n}$$
Vogliamo quindi trovare che forma hanno i proiettori. Intanto, vale la relazione di completezza $\hat{P}_{+n}+\hat{P}_{-n}=\hat{\mathbf{1}}$ e sappiamo che $\hat{\sigma}_{n}$ è la differenza tra due proiettori. Ora abbiamo due equazioni che possiamo risolvere:
$$\begin{cases}
\hat{\sigma}_{n}=\hat{P}_{+n}-\hat{P}_{-n} \\
\hat{\mathbf{1}}=\hat{P}_{+n}+\hat{P}_{-n}
\end{cases}\quad\Rightarrow \quad \begin{cases}
\hat{P}_{+n}=\frac{\hat{\mathbf{1}}+\hat{\sigma}_{n}}{2} \\
\hat{P}_{-n}=\frac{\hat{\mathbf{1}}-\hat{\sigma}_{n}}{2}
\end{cases}$$
Per essere sicuri che questi siano effettivamente gli autoproiettori di $\hat{\sigma}_{n}$, dobbiamo verificare che siano [[idempotence|idempotenti]] e [[Ortogonalità|ortogonali]] fra loro. Per l'idempotenza
$$\hat{P}_{\pm n}^{2}=\frac{1}{4} (\hat{\mathbf{1}}+\hat{\mathbf{1}} \pm2\hat{\sigma}_{n})=\frac{\hat{\mathbf{1}}\pm\hat{\sigma}_{n}}{2}=\hat{P}_{\pm n}$$
che dimostra siano proiettori, e per l'ortogonalità
$$\hat{P}_{+n}\hat{P}_{-n}=\frac{1}{4}(\hat{\mathbf{1}}-\hat{\mathbf{1}}-\hat{\sigma}_{n}+\hat{\sigma}_{n})=0$$
che dimostra siano autoproiettori.
### Esempi fisici
> [!example] Magnetone di Bohr
> Un corpo elettricamente [[Electric charge|carico]] in [[Rotation|rotazione]] produce un [[Magnetic field|campo magnetico]] per via del moto delle cariche. Le particelle elementari come l'[[elettrone]] non hanno un'estensione spaziale ben definita per via dell'[[indeterminatezza quantistica]], ma sono comunque cariche e possiedono uno spin. È ragionevole dunque assumere che possano produrre un campo magnetico caratteristico della particella. La [[Hamiltonian|Hamiltoniana]] di una particella di spin 1/2 sull'asse $\hat{\mathbf{n}}$ con pulsazione $\omega$ è
> $$\hat{H}=- \frac{\hbar}{2}\omega \hat{\sigma}_{n}$$
> Ricordiamo che l'Hamiltoniana classica di un oggetto carico in rotazione è
> $$H=-\boldsymbol{\mu}\cdot \mathbf{B}$$
> dove $\boldsymbol{\mu}$ è il [[magnetic dipole moment|momento di dipolo magnetico]] e $\mathbf{B}$ è il campo magnetico. Se sono entrambe allineati sull'asse $\hat{\mathbf{n}}$, si semplifica a $H=-\mu_{n}B_{n}$.
>
> Ci interessa trovare come questo sistema evolve nel tempo. Possiamo trovare l'[[evolutore]] dell'Hamiltoniana quantistica:
> $$\hat{U}_{t}=e^{-i \hat{H}t/\hbar}=e^{i (\hbar/2)\omega \hat{\sigma}_{n}t/\hbar}=e^{i\omega t\hat{\sigma}_{n}/2}$$
> Usando la [[serie esponenziale]] abbiamo
> $$e^{i\omega t \hat{\sigma}_{n}/2}=\sum_{n=1}^{\infty} \frac{\left( i \frac{\omega t}{2} \hat{ \sigma}_{n} \right)^{n}}{n!}=\sum_{n=1}^{\infty} \frac{\left( i \frac{\omega t}{2} \right)^{2n}}{(2n)!}\hat{\mathbf{1}}+\sum_{n=1}^{\infty} \frac{\left( i \frac{\omega t}{2} \right)^{2n+1}}{(2n+1)!} \hat{\sigma}_{n}=\ldots$$
> dato che $\hat{\sigma}_{n}^{2}=\hat{\mathbf{1}}$ e dividendo la serie in due serie, una in indici pari e una in indici dispari. Ricordando che $i^{2n}=(i^{2})^{n}=(-1)^{n}$ e $i^{2n+1}=ii^{2n}=i(-1)^{n}$ abbiamo
> $$\ldots=\hat{\mathbf{1}}\sum_{n=1}^{\infty} \frac{(-1)^{n}}{(2n)!} \left( \frac{\omega t}{2} \right)^{2n}+\hat{\sigma}_{n}i\sum_{n=1}^{\infty} \frac{(-1)^{n}}{(2n+1)!}\left( \frac{\omega t}{2} \right)^{2n}$$
> Ma queste sono le [[sine and cosine series|serie del seno e del coseno]], quindi
> $$\hat{U}_{t}=e^{i\omega t \hat{ \sigma}_{n}/2}=\cos \frac{\omega t}{2}\hat{\mathbf{1}}+i \hat{\sigma}_{n}\sin \frac{\omega t}{2}$$
> Allora, se partiamo dallo [[stato]] $\ket{\psi}$, al tempo $t$ saremo nello stato
> $$\ket{\psi_{t}}=\left(\cos \frac{\omega t}{2}\hat{\mathbf{1}}+i \hat{\sigma}_{n}\sin \frac{\omega t}{2}\right)\ket{\psi} $$
> Essendo un sistema a spin 1/2, ci sono solo due possibili autostati, $\ket{\uparrow n}$ e $\ket{\downarrow n}$. Vogliamo sapere che [[Probability|probabilità]] abbiamo di trovarci nell'uno o nell'altro al tempo $t$. Assumendo che lo spin sia sull'asse $z$ e che si parta dallo stato $\ket{\uparrow z}$, la probabilità di essere in $\ket{\uparrow z}$ dopo del tempo $t$ è
> $$\text{Prob}(\uparrow z|\uparrow z)=\lvert \braket{ \uparrow z | \hat{U}_{t} \uparrow z } \rvert^{2} $$
> che rappresenta la [[Conditional distribution function|probabilità condizionata]] di avere lo stato $\ket{\uparrow z}$ al tempo $t$ sapendo di partire dallo stato $\ket{\uparrow z}$. Analogamente per ogni altra combinazione di spin up o down.
