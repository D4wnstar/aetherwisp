Il **prodotto tensoriale** è un'operazione tra due [[spazio vettoriale|spazi vettoriali]] $V$ e $W$ denotata con $V\otimes W$ che ha come risultato un terzo spazio vettoriale a cui è associata una funzione bilineare $V\times W \rightarrow V\otimes W$ che trasforma una coppia di elementi $(v,w)\in V\times W$ ad un elemento di $V\otimes W$, scritto $v\otimes w$. Solitamente ci si riferisce a $v\otimes w$ stesso come il prodotto tensoriale.

In meccanica quantistica, uno spazio vettoriale rappresenta un sistema, generato dalla [[base]] degli [[Equazione agli autovalori|autostati]]. Allora il prodotto tensoriale ci dà un metodo matematico per esprimere la combinazione di due sistemi. Presi due sistemi $S_{1}:|\psi_{1}\rangle\in H$ e $S_{2}:|\psi_{2}\rangle\in H$ in uno [[spazio di Hilbert]], la somma dei due sistemi è
$$S_{1}+S_{2}:|\psi_{1}\otimes\psi_{2}\rangle\equiv |\psi_{1}\rangle\otimes |\psi_{2}\rangle\equiv |\psi_{1},\psi_{2}\rangle$$
detto [[stato]] accoppiato.
### Tra vettori
Tra spazi a dimensione finita, e quindi tra due vettori $v$ e $w$, il prodotto tensoriale può essere rappresentato in due modi (prendendo $\mathbb{C}^{2}\otimes\mathbb{C}^{2}=\mathbb{C}^{4}$ come esempio):
$$v\otimes w=\pmatrix{v_{1}\\ v_{2}}\otimes\pmatrix{w_{1} \\ w_{2}}=\pmatrix{v_{1} & \pmatrix{w_{1} \\ w_{2}} \\ v_{2} & \pmatrix{w_{1} \\ w_{2}}}=\pmatrix{v_{1}w_{1} \\ v_{1}w_{2} \\ v_{2}w_{1} \\ v_{2}w_{2}}$$
oppure
$$v\otimes w=\pmatrix{v_{1}\\ v_{2}}\otimes\pmatrix{w_{1} \\ w_{2}}=\pmatrix{w_{1} & \pmatrix{v_{1} \\ v_{2}} \\ w_{2} & \pmatrix{v_{1} \\ v_{2}}}=\pmatrix{w_{1}v_{1} \\ w_{1}v_{2} \\ w_{2}v_{1} \\ w_{2}v_{2}}$$
ossia invertendo quale vettore "va prima". Le due rappresentazioni sono equivalenti, fintantoché non le si mischia.

A livello pratico, un prodotto tensoriale è il vettore contente i termini di un prodotto tra polinomi. Infatti
$$(v_{1}+v_{2})(w_{1}+w_{2})=v_{1}w_{1}+v_{1}w_{2}+v_{2}w_{1}+v_{2}w_{2}$$
$$\pmatrix{v_{1}\\ v_{2}}\otimes\pmatrix{w_{1} \\ w_{2}}=\pmatrix{v_{1}w_{1} \\ v_{1}w_{2} \\ v_{2}w_{1} \\ v_{2}w_{2}}$$
#### Proprietà
E' lineare, nel senso che la combinazione lineare di prodotti tensoriale è essa stessa un prodotto tensoriale nello stesso spazio. Presi $v_{1},v_{2}\in V$ e $w_{1},w_{2}\in W$, vale
$$v_{1}\otimes w_{1}\in V\otimes W$$
ma anche
$$\alpha(v_{1}\otimes w_{1})+ \beta (v_{2}\otimes w_{2})\in V\otimes W$$
con $\alpha$ e $\beta$ delle costanti qualunque.

Vale
$$\langle \psi_{1}\otimes\psi_{2}|\phi_{1}\otimes\phi_{2}\rangle=\langle \psi_{1}|\phi_{1}\rangle \langle \psi_{2}|\phi_{2}\rangle$$

La norma quadra è
$$||\;|\phi_{1}\otimes\phi_{2}\rangle\;||^{2}=||\phi_{1}||^{2}\;||\phi_{2}||^{2}$$

Presi due [[operatori locali]] $\hat{A}_{1}:H_{1} \rightarrow H_{1}$ e $\hat{A}_{2}:H_{2} \rightarrow H_{2}$ si ha
$$\hat{A}_{1}\otimes\hat{A}_{2}\;|\psi_{1}\otimes\psi_{2}\rangle=\hat{A}_{1}|\psi_{1}\rangle\otimes\hat{A}_{2}|\psi_{2}\rangle$$

La media di un prodotto tensoriale di due operatori è la sua [[traccia]]
$$\langle \hat{A}_{1}\otimes \hat{A}_{2} \rangle=\mbox{Tr}(\hat{A}_{1}\otimes\hat{A}_{2})=\sum\limits_{mn}(\langle \phi_{m}|\otimes \langle \varphi_{n}|)(\hat{A}_{1}\otimes\hat{A}_{2})(|\phi_{n}\rangle\otimes |\varphi_{n}\rangle)=$$
$$=\sum\limits_{mn}\langle \phi_{m}|\hat{A}_{1}|\phi_{n}\rangle \langle \varphi_{n}|\hat{A}_{2}|\varphi_{n}\rangle=\sum\limits_{m}\langle \phi_{m}|\hat{A}_{1}|\phi_{m}\rangle \sum\limits_{n}\langle \varphi_{n}|\hat{A}_{2}|\varphi_{n}\rangle=\mbox{Tr}^{(1)}\hat{A}_{1}\mbox{Tr}^{(2)}\hat{A}_{2}$$

La dimensione dello spazio risultante è la somma degli spazi iniziali, ossia
$$\dim(V\otimes W)=\dim V+\dim W$$

Il prodotto tensoriale elemento per elemento di una [[base]] di $V$ con una base di $W$ dà una base di $V\otimes W$.
#### Separabilità
I tensori ottenuti dal prodotto tensoriale non sono necessariamente descrivibili come due oggetti separati. Per esempio, considerato un tensore $|\psi_{12}\rangle\in V\otimes W$, esso viene detto **separabile** se può essere espresso come $|\psi_{12}\rangle=|\psi_{1}\rangle\otimes |\psi_{2}\rangle$. Se non è possibile, lo stato viene detto **intrecciato** (**entangled**). L'[[entanglement quantistico]] è descritto come stati quantistici tra loro inseparabili e quindi non descrivibili mediante un prodotto tensoriale tra due stati indipendenti.

Per esempio, consideriamo un sistema con due [[particella|particelle]] con [[spin#Spin 1/2|spin 1/2]]. Per ciascuna particella, gli autostati sono solo due, lo spin up e lo spin down, e lo stato generico $\chi$ può essere espresso come
$$\chi=\pmatrix{a \\ b}=a |\uparrow\;\rangle+b |\downarrow\;\rangle$$
con
$$|\uparrow\;\rangle=\pmatrix{1 \\0 }, \quad |\downarrow\;\rangle=\pmatrix{0 \\ 1}$$
L'accoppiamento delle due particelle si mostra compiendo il prodotto tensoriale tra gli autostati. Per esempio, si può avere
$$|\uparrow\otimes\downarrow\;\rangle+|\downarrow\otimes\uparrow\;\rangle=\pmatrix{1 \\ 0}\otimes\pmatrix{0 \\ 1}+\pmatrix{0 \\ 1}\otimes\pmatrix{1 \\ 0}=\pmatrix{0 \\ 1 \\ 1 \\ 0}$$
Vogliamo idealmente ridurre la precedente equazione ad un singolo prodotto tensoriale, anziché una combinazione lineare di prodotti. Per fare ciò, prendiamo i vettori generici
$$|\chi_{1}\rangle=\pmatrix{a_{1} \\ a_{2}}, \quad |\chi_{2}\rangle=\pmatrix{b_{1} \\ b_{2}}$$
quindi nello spazio prodotto tensoriale
$$|\chi_{1}\otimes\chi_{2}\rangle=\pmatrix{a_{1}b_{1} \\ a_{1}b_{2} \\ a_{2}b_{1} \\ a_{2}b_{2}}=\pmatrix{0 \\ 1 \\ 1 \\ 0}$$
ma non esiste alcun insieme di $a_{1}$, $a_{2}$, $b_{1}$, $b_{2}$ che può soddisfare questa relazione. L'accoppiamento è dunque intrecciato e lo stato delle due particelle è legato fra loro per effetto quantistico.
### Tra matrici e operatori
È possibile compiere un prodotto tensoriale anche tra matrici quadrate e [[Operatore lineare|operatori lineari]]. Come per i vettori, esistono due rappresentazioni. Prendendo per esempio $\mathbf{A}$ e $\mathbf{B}$ matrici $2\times2$ con elementi in $\mathbb{C}$ abbiamo
$$\mathbf{A}\otimes\mathbf{B}=\pmatrix{a_{11}\mathbf{B} & a_{12}\mathbf{B} \\ a_{21}\mathbf{B} & a_{22}\mathbf{B}}$$
oppure
$$\mathbf{A}\otimes\mathbf{B}=\pmatrix{b_{11}\mathbf{A} & b_{12}\mathbf{A} \\ b_{21}\mathbf{A} & b_{22}\mathbf{A}}$$
#### Proprietà
La dimensione dello spazio risultante è
$$\dim V=n\times n, \quad \dim W=m\times m, \quad \dim(V\otimes W)=nm\times nm$$