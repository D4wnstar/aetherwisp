Consideriamo un'[[Osservabile]] $A$ e il suo [[Operatore autoaggiunto]] associato $\hat{A}$. Prendo un [[Notazione braket|ket]] $|\psi\rangle\in\mathcal{H}$ con $\mathcal{H}$ uno [[Spazio di Hilbert]] e $\psi$ una [[Funzione d'onda]] che rappresenta lo [[Stato]] del mio sistema. Dato che la meccanica quantistica è una teoria statistica, è conveniente trovare il valor medio di un'osservabile:
$$\boxed{\langle A\rangle_{\psi}=\langle \psi|\hat{A}|\psi\rangle}$$
Per dimostrarlo, ricordiamo che se $\hat{A}$ è autoaggiunto, i suoi autovettori formano una base dello spazio. Abbiamo $\hat{A}|a_{i}\rangle=a_{i}|a_{i}\rangle$ con $a_{i}\in\mathbb{R}$. Riscriviamo l'espressione esprimendo $\psi$ in questa base
$$|\psi\rangle=\sum\limits_{i=1}^{n}\psi_{i}|a_{i}\rangle$$
$$\langle \psi|\hat{A}\psi\rangle=\sum\limits_{i,j=1}^{n}\psi_{i}\psi_{j}^{\ast}\langle a_{j}|\hat{A}|a_{i}\rangle=\sum\limits_{i,j=1}^{n}\psi_{i}\psi_{j}^{\ast}a_{j}\underbrace{\langle a_{j}|a_{i}\rangle}\limits_{\delta_{ij}}$$
Quindi ci rimane
$$\sum\limits_{i=1}^{n}a_{i}|\psi_{i}|^{2}$$
Ma per la normalizzazione è anche vero che
$$\sum\limits_{i=1}^{n}|\psi_{i}|^{2}=1$$
quindi abbiamo trovato che le $a_{i}$ possono essere interpretati come *probabilità* che l'osservabile assuma un certo valore.
$$\boxed{\psi_{i}=\langle a_{i}|\psi\rangle}$$
Allora possiamo anche considerare le varianze
$$\Delta_{\psi}\hat{A}=\langle(\hat{A}-\langle\hat{A}\rangle_{\psi})^{2}\rangle_{\psi}=\langle \psi|(\hat{A}-\langle\hat{A}\rangle_{\psi})^{2}\psi\rangle$$
$$\Delta_{\psi}\hat{B}=\langle(\hat{B}-\langle\hat{B}\rangle_{\psi})^{2}\rangle_{\psi}=\langle \psi|(\hat{B}-\langle\hat{B}\rangle_{\psi})^{2}\psi\rangle$$
Riprendendo la [[Disuguaglianza di Heisenberg]] abbiamo
$$\Delta_{\psi}\hat{A}\Delta_{\psi}\hat{B}\geq\;?$$
dove bisogna trovare il limite inferiore al prodotto delle varianze.
$$\overline{\langle \psi|\hat{A}\psi\rangle}=\langle \hat{A}\psi|\psi\rangle=\langle \psi|\hat{A}\psi\rangle$$
quindi il valor medio è uguale al suo coniugato, quindi è *reale*. Tornando alle disuguaglianze e ricordando che $||\psi||^{2}=\langle \psi|\psi\rangle$
$$\Delta_{\psi}\hat{A}=||(\hat{A}-\langle\hat{A}\rangle_{\psi})|\psi\rangle||^{2}$$
$$\Delta_{\psi}\hat{B}=||(\hat{B}-\langle\hat{B}\rangle_{\psi})|\psi\rangle||^{2}$$
Allora il prodotto è
$$\Delta_{\psi}\hat{A}\Delta_{\psi}\hat{B}=||(\hat{A}-\langle\hat{A}\rangle_{\psi})|\psi\rangle||^{2}+||(\hat{B}-\langle\hat{B}\rangle_{\psi})|\psi\rangle||^{2}\geq\ldots$$
e usando la [[Disuguaglianza di Cauchy-Schwarz]] 
$$\ldots\geq|\langle\hat{A}-\langle\hat{A}\rangle_{\psi})\psi\;|\;(\hat{B}-\langle\hat{B}\rangle_{\psi})\psi\rangle|^{2}\geq\ldots$$
Ricordando che la parte immaginaria di un numero complesso $z$ si può scrivere come
$$\Im(z)= \frac{z-z^{\ast}}{2i}$$
$$\ldots\geq[\Im(|\langle\hat{A}-\langle\hat{A}\rangle_{\psi})\psi\;|\;(\hat{B}-\langle\hat{B}\rangle_{\psi})\psi\rangle|)]^{2}\geq\ldots$$
Possiamo sviluppare il prodotto scalare
$$\langle(\hat{A}-\langle\hat{A}\rangle_{\psi})\psi\;|\;(\hat{B}-\langle\hat{B}\rangle_{\psi})\psi\rangle=\langle \psi|\hat{A}\hat{B}\psi\rangle-\langle \hat{A}\rangle_{\psi}\langle\hat{B}\rangle_{\psi}$$
dove si cancellano alcuni elementi. Prendo il coniugato
$$\overline{\langle\hat{A}-\langle\hat{A}\rangle_{\psi})\psi\;|\;(\hat{B}-\langle\hat{B}\rangle_{\psi})\psi\rangle}=\overline{\langle \psi|\hat{A}\hat{B}\psi\rangle}-\langle \hat{A}\rangle_{\psi}\langle\hat{B}\rangle_{\psi}=\langle \hat{A}\hat{B}\psi|\psi\rangle-\langle \hat{A}\rangle_{\psi}\langle\hat{B}\rangle_{\psi}=$$
$$=\langle \hat{B}\psi|\hat{A}\psi\rangle-\langle \hat{A}\rangle_{\psi}\langle\hat{B}\rangle_{\psi}=\langle \psi|\hat{B}\hat{A}\psi\rangle-\langle \hat{A}\rangle_{\psi}\langle\hat{B}\rangle_{\psi}$$
Allora $\Im(\ldots)$ è
$$\Im(\ldots)=\frac{\langle \psi|\hat{A}\hat{B}\psi\rangle - \langle \psi|\hat{B}\hat{A}\psi\rangle}{2i}=\left(\frac{1}{2i}\langle \psi|[\hat{A},\hat{B}]\psi\rangle\right)^{2}$$
con $[\hat{A},\hat{B}]$ il commutatore. Quindi abbiamo trovato che
$$\boxed{\Delta_{\psi}\hat{A}\Delta_{\psi}\hat{B}=\left(\frac{1}{2i}\langle \psi|[\hat{A},\hat{B}]\psi\rangle\right)^{2}}$$
che è a sua volta reale. Se chiamiamo $\hat{A}=\hat{x}$ e $\hat{B}=\hat{p}_{x}$ allora riotteniamo abbiamo $[\hat{x},\hat{p}_{x}]=i\hbar$ da cui si trova
$$\Delta_{\psi}\hat{x}\Delta_{\psi}\hat{p}_{x}\geq \frac{\hbar^{2}}{4}$$
Vogliamo vedere quali sono le condizioni in cui la disuguaglianza è *saturata*, ossia vale l'uguaglianza al limite. Torniamo indietro fino al passaggio dove abbiamo aggiunto Cauchy-Schwarz. Allora ci chiediamo quando vale
$$||\psi||^{2}||\phi||^{2}=|\langle \psi|\phi\rangle|^{2}$$
dove $\phi$ e $\psi$ non sono necessariamente normalizzati. Questo è vero quando $\psi$ e $\phi$ sono paralleli fra loro, ossia quando
$$|\phi\rangle=\lambda |\psi\rangle$$
$$|\lambda \langle \psi|\psi\rangle|^{2}=|\lambda|^{2}||\psi||^{2}$$
$$||\psi||^{2}||\phi||^{2}=||\psi||^{2}|\lambda|^{2}||\psi||^{2}$$
Mostriamo che l'identità non vale se non sono paralleli. Se è così, allora $\psi$ è scomponibile in una componente parallela a $\phi$ e una perpendicolare.
$$|\phi\rangle=\alpha |\psi\rangle+\beta |\psi^{\perp}\rangle$$
Se $\beta = 0$ si ha che sono paralleli.