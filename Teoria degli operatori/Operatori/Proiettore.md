Si chiama **proiettore** $\hat{P}_{\psi}$ l'[[operatore lineare]] che, applicato ad un elemento di uno [[spazio vettoriale]], risulta nella componente di quell'elemento che giace sulla direzione $\psi$. Usando la [[notazione braket]], si scrive
$$\hat{P}_\psi=|\psi\rangle\langle\psi|$$
e applicato ad un vettore $|\phi\rangle$ si scrive
$$\hat{P}_{\psi}|\phi\rangle=\langle\psi|\phi\rangle|\psi\rangle$$
Il numero risultante (se si proietta su uno spazio 1D) appartiene al sottospazio unidimensionale generato da $|\psi\rangle$. In sostanza, il proiettore individua la componente di un vettore su una certa dimensione e lo applica al vettore stesso.
### Proprietà
Un proiettore è un operatore [[idempotenza|idempotente]]
$$\hat{P}_{\psi}^{2}=\hat{P}_{\psi}\hat{P}_{\psi}=(|\psi\rangle\langle \psi|)(|\psi\rangle\langle \psi|)=\langle \psi|\psi\rangle|\psi\rangle\langle \psi|=\hat{P}_{\psi}$$
usando che $\braket{ \psi | \psi }=1$ e vale $\hat{P}_{\psi}^{0}=0$.

È [[Operatore autoaggiunto|autoaggiunto]], infatti
$$\langle \phi|\hat{P}_{x}\psi\rangle=\langle \hat{P}_{x}\phi+\phi-\tilde{\phi}|\hat{P}_{x}\psi\rangle=\langle \hat{P}_{x}\phi|\hat{P}_{x}\psi\rangle=\langle \hat{P}_{x}\phi|\hat{P}_{x}\psi+\psi-\tilde{\psi}\rangle=\langle \hat{P}_{x}\phi|\psi\rangle$$

Ha [[traccia]] unitaria
$$\text{Tr}(\hat{P}_{\psi})=1$$
e gli [[Equazione agli autovalori|autovalori]] sono sempre 0 e 1.

Poiché sono autoaggiunti, hanno traccia unitaria e autovalori 0 e 1, i proiettori possono essere rappresentati come [[Matrice di densità|matrici di densità]].

Per dimostrare che un operatore è un proiettore bisogna dimostrare
- l'autoaggiuntezza
- l'idempotenza
### Proiettore su base ortonormale
I proiettori sono particolarmente utili quando si deve trovare la rappresentazione di un vettore o funzione rispetto ad una [[base]]. Infatti, presa una [[base]] [[Ortonormalità|ortonormale]] costituita da $\{|\phi_{i}\rangle\}^{n}_{i=1}$ definita su uno [[spazio di Hilbert]] $\mathcal{H}$, ogni vettore generico $\ket{\psi}$ di $\mathcal{H}$ può essere rappresentato come una combinazione lineare degli elementi della base
$$\ket{\psi} =\sum_{i=1}^{n} \braket{ \phi_{i} | \psi } \ket{\phi_{i}} $$
dove $\braket{ \phi_{i} | \psi }$ sono i [[Serie di Fourier|coefficienti di Fourier]]. Lo stesso vale per una base in uno spazio infinito dimensionale e continuo, come ad esempio [[Spazi Lp|L^2]], come
$$\ket{\psi} =\int_{-\infty}^{\infty} \braket{ x | \psi } \ket{\psi}  \ dx $$
Ma dovrebbe essere evidente il parallelo con il proiettore. Se definiamo il proiettore sulla direzione $\ket{\phi_{i}}$ come
$$\hat{P}_{\phi_{i}}=\ket{\phi_{i}} \bra{\phi_{i}} $$
la sua applicazione su generico vettore $\ket{\psi}$ è $\hat{P}_{\phi_{i}}=\braket{ \phi_{i} | \psi }\ket{\phi_{i}}$. Ma questo non è altro che il singolo termine della serie di Fourier con il quale espandiamo un vettore in una base ortonormale. Vale infatti
$$\ket{\psi} =\sum_{i=1}^{n} \hat{P}_{\phi_{i}}\ket{\psi} $$
Ma da questo si può anche ricavare un risultato molto importante. Applicare tutti i proiettori sui vettori di una base su un vettore ci ritorna il vettore stesso. In pratica, la somma di tutti i proiettori su una base ortonormale "non fa nulla". Questo fatto è formalizzato nella **relazione di completezza**
$$\sum\limits_{i=1}^{n}\hat{P}_{\psi_{i}}=\hat{\mathbf{1}}$$
dove $\hat{\mathbf{1}}$ è l'operatore identico.

Questo risultato si estende immediatamente anche al caso a dimensione infinita discreta, prendendo un [[sistema ortonormale completo]]. Nel caso di un sistema a dimensione infinita continua, c'è bisogno che sia [[Ortonormalità|Dirac-ortonormale]], in qual caso la relazione di completezza diventa
$$\int_{-\infty}^{+\infty}|e_{z}\rangle\langle e_{z}|dz=\hat{\mathbb{1}}$$
### Risultati utili
La somma di tutte le proiezioni su una base ortonormale è il vettore stesso, grazie alla completezza:
$$|\psi\rangle=\sum\limits_{i=1}^{n}\langle i|\psi\rangle|i\rangle=\sum\limits_{i=1}^{n}|i\rangle\langle i|\psi\rangle=\left(\sum\limits_{i=1}^{n}\hat{P}_{i}\right)|\psi\rangle$$
che è una serie di Fourier.

Un vettore proiettato su sé stesso dà sé stesso:
$$\hat{P}_{\psi}|\psi\rangle=\langle \psi|\psi\rangle|\psi\rangle=|\psi\rangle$$

Un vettore proiettato su un altro vettore ortogonale ad esso dà sempre 0:
$$\hat{P}_{\psi}|\phi\rangle=\langle \psi|\phi\rangle|\psi\rangle=0\quad\text{con}\quad|\phi\rangle\in\{|\psi\rangle\}^{\perp} \Rightarrow\langle \phi|\psi\rangle=0$$

Considero l'esponenziale
$$e^{\hat{P}_{\psi}}=\sum\limits_{n=0}^{\infty} \frac{1}{n!}(\hat{P}_{\psi})^{n}=\hat{\mathbb{1}}+\left(\sum\limits_{n=1}^{\infty} \frac{1}{n!}\right)\hat{P}_{\psi}=\hat{\mathbb{1}}+(e-1)\hat{P}_{\psi}$$
ricordando l'idempotenza.