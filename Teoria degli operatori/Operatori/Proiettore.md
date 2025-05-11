---
wiki-publish: true
aliases:
  - autoproiettore
  - relazione di completezza
---
Si chiama **proiettore** $\hat{P}_{\psi}$ l'[[operatore lineare]] che, applicato ad un elemento di uno [[Vector space]], risulta nella componente di quell'elemento che giace sulla direzione $\psi$ di una [[base]] [[Orthonormality|ortonormale]]. Usando la [[notazione braket]], si scrive
$$\hat{P}_\psi=|\psi\rangle\langle\psi|$$
e applicato ad un vettore $|\phi\rangle$ si scrive
$$\hat{P}_{\psi}|\phi\rangle=\langle\psi|\phi\rangle|\psi\rangle$$
Il numero risultante (se si proietta su uno spazio 1D) appartiene al sottospazio unidimensionale generato da $|\psi\rangle$. In sostanza, il proiettore individua la componente di un vettore su una certa dimensione e lo applica al vettore stesso.

In meccanica quantistica, i proiettori sono comunemente usati per rappresentare la riduzione di uno stato non osservato ad un suo [[Equazione agli autovalori|autostato]] a seguire di una misura. Un proiettore che proietta su un vettore di autostato è anche detto **autoproiettore**.
### Proprietà
Un proiettore è un operatore [[idempotence|idempotente]]
$$\hat{P}_{\psi}^{2}=\hat{P}_{\psi}\hat{P}_{\psi}=(|\psi\rangle\langle \psi|)(|\psi\rangle\langle \psi|)=\langle \psi|\psi\rangle|\psi\rangle\langle \psi|=\hat{P}_{\psi}$$
usando che $\braket{ \psi | \psi }=1$ ($\psi$ è componente di una base ortonormale) e vale $\hat{P}_{\psi}^{0}=0$.

È [[Operatore autoaggiunto|hermitiano]], infatti
$$\langle \phi|\hat{P}_{x}\psi\rangle=\langle \hat{P}_{x}\phi+\phi-\tilde{\phi}|\hat{P}_{x}\psi\rangle=\langle \hat{P}_{x}\phi|\hat{P}_{x}\psi\rangle=\langle \hat{P}_{x}\phi|\hat{P}_{x}\psi+\psi-\tilde{\psi}\rangle=\langle \hat{P}_{x}\phi|\psi\rangle$$

Sono [[Orthogonality|ortogonali]] fra loro, ossia presi due proiettori su vettori ortogonali $\phi_{1}$ e $\phi_{2}$, si ha
$$\braket{ \phi_{1} | \phi_{2} } =0\quad\Rightarrow \quad \hat{P}_{\phi_{1}}\hat{P}_{\phi_{2}}=0$$
infatti
$$\hat{P}_{\phi_{1}}\hat{P}_{\phi_{2}}\ket{\psi} =\braket{ \phi_{1} | \hat{P}_{\phi_{2}}\psi }\ket{\phi_{1}} =\braket{ \phi_{1} | \braket{ \phi_{2} | \psi } \phi_{2} }\ket{\phi_{1}} =\braket{ \phi_{2} | \psi } \underbrace{ \braket{ \phi_{1} | \phi_{2} } }_{ 0 } \ket{\phi_{1}} =0  $$
e più in generale si può scrivere
$$\hat{P}_{\phi_{i}}\hat{P}_{\phi _{j}}=\delta_{ij}\hat{P}_{\phi_{i}}$$

Ha [[Traccia]] unitaria
$$\text{Tr}(\hat{P}_{\psi})=1$$
e gli [[Equazione agli autovalori|autovalori]] sono sempre 0 e 1.

Poiché sono autoaggiunti, hanno traccia unitaria e autovalori 0 e 1, i proiettori possono essere rappresentati come [[Matrice di densità|matrici di densità]].

Per dimostrare che un operatore è un proiettore bisogna dimostrare
- l'autoaggiuntezza
- l'idempotenza
### Relazione di completezza
La **relazione di completezza** è una relazione particolarmente utile associata ai proiettori. Si verifica sia su sistemi ortonormali discreti che continui.
#### Caso discreto
Presa una base ortonormale discreta costituita da $\{|\phi_{i}\rangle\}^{n}_{i=1}$ definita su uno [[spazio di Hilbert]] $\mathcal{H}$, ogni vettore generico $\ket{\psi}$ di $\mathcal{H}$ può essere rappresentato come una combinazione lineare degli elementi della base in [[Serie di Fourier]]:
$$\ket{\psi} =\sum_{i=1}^{n} \braket{ \phi_{i} | \psi } \ket{\phi_{i}} $$
dove $\braket{ \phi_{i} | \psi }$ sono i [[Serie di Fourier|coefficienti di Fourier]]. Dovrebbe essere evidente il parallelo con il proiettore. Se definiamo il proiettore sulla direzione  come
$$\hat{P}_{\phi_{i}}=\ket{\phi_{i}} \bra{\phi_{i}} $$
la sua applicazione su generico vettore $\ket{\psi}$ è $\hat{P}_{\phi_{i}}=\braket{ \phi_{i} | \psi }\ket{\phi_{i}}$. Ma questo non è altro che il singolo termine della serie di Fourier, che può infatti essere scritta in forma proiettiva come
$$\ket{\psi} =\sum_{i=1}^{n} \hat{P}_{\phi_{i}}\ket{\psi} $$
Da qui si vede che la somma di tutte le proiezioni su una base di un vettore ci ritorna il vettore stesso. In pratica, la somma di tutti i proiettori su una base ortonormale "non fa nulla". Se consideriamo i proiettori in maniera astratta, senza applicarli al vettore, possiamo tirare quest'ultimo fuori dalla somma (dato che non dipende da $i$), il che implica la seguente relazione
$$\boxed{\sum\limits_{i=1}^{n}\hat{P}_{\phi_{i}}=\hat{\mathbf{1}}}$$
dove $\hat{\mathbf{1}}$ è l'operatore identico. Questa è detta relazione di completezza ed è universalmente valida per qualunque base ortonormale discreta.
#### Caso continuo
Il caso continuo richiede degli accorgimenti. Possiamo dimostrare la relazione partendo da concetti quantistici: prendiamo da una [[funzione d'onda]] $\psi \in L^{2}(\mathbb{R})$ e la [[Rappresentazioni dello stato|rappresentiamo in posizione]] come 
$$\psi(x)=\braket{ x | \psi }=\int_{-\infty}^{\infty} \delta(y-x)\psi(y) \ dy=\ldots$$
usando la [[delta di Dirac]]. È anche vero che $\braket{ x | y }=\delta(x-y)$, allora
$$\ldots=\int_{-\infty}^{\infty} \braket{ x | y } \braket{ y | \psi }  \ dx =\bra{x} \left( \int_{-\infty}^{\infty} \underbrace{ \ket{y} \bra{y} }_{ \hat{P}_{y} }  \ dy  \right)\ket{\psi} $$
che possiamo fare per la linearità dell'integrale. Dato che gli autostati di posizione sono continui e non discreti (e quindi non [[Normalization|normalizzabili]]), l'argomento dell'integrale $\hat{P}_{y}$ non può essere un proiettore, e viene invece detto **pseudoproiettore**, in quanto condivide diverse proprietà di un proiettore, ma non è idempotente. Infatti, il quadrato di una delta di Dirac non esiste, neanche come distribuzione, quindi il quadrato di un pseudoproiettore è anch'esso indefinito.

Detto questo, si può vedere subito che l'integrale non può avere alcun'azione sul $\ket{\psi}$, altrimenti non potrebbe essere uguale a $\braket{ x | \psi }$. Ci ritroviamo nella stessa situazione del caso discreto e allo stesso modo possiamo affermare
$$\boxed{\int_{-\infty}^{\infty} \hat{P}_{x} \ dx=\int_{-\infty}^{\infty} \ket{x} \bra{x}  \ dx  =\hat{\mathbf{1}}}$$
Questo risultato vale su un [[sistema ortonormale completo]], con l'ortonormalità intesa [[Orthonormality|nel senso della delta di Dirac]].
### Risultati utili
Un vettore proiettato su sé stesso dà sé stesso:
$$\hat{P}_{\psi}|\psi\rangle=\langle \psi|\psi\rangle|\psi\rangle=|\psi\rangle$$

La proiezione di un vettore su un vettore ortogonale ad esso è sempre nulla:
$$\braket{ \phi | \psi } =0 \quad\Rightarrow \quad\hat{P}_{\psi}|\phi\rangle=\langle \psi|\phi\rangle|\psi\rangle=0$$

L'esponenziale di un proiettore ha una forma particolare per merito dell'idempotenza
$$e^{\hat{P}_{\psi}}=\sum\limits_{n=0}^{\infty} \frac{1}{n!}(\hat{P}_{\psi})^{n}=\hat{\mathbf{1}}+\left(\sum\limits_{n=1}^{\infty} \frac{1}{n!}\right)\hat{P}_{\psi}=\hat{\mathbf{1}}+(e-1)\hat{P}_{\psi}$$
usando la [[Serie esponenziale]].