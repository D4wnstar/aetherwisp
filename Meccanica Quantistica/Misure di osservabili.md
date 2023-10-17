Prendiamo un'[[osservabile]] $\hat{A}=\hat{A}^{\dagger}:\mathbb{H}\rightarrow\mathbb{H}$ e una $\hat{B}=\hat{B}^{\dagger}:\mathbb{H}\rightarrow\mathbb{H}$ con $\mathbb{H}$ uno [[Spazio di Hilbert]]. Prendo un [[Notazione Braket|ket]] $|\psi\rangle\in\mathbb{H}$ che rappresenta lo stato del mio sistema. Dato che la meccanica quantistica è una teoria statistica, è conveniente trovare i valori medi delle osservabili: $$\boxed{\langle\hat{A}\rangle_{\psi}=\langle \psi|\hat{A}\psi\rangle}$$
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
Riprendendo la [[disuguaglianza di Heisenberg]] abbiamo
$$\Delta_{\psi}\hat{A}\Delta_{\psi}\hat{B}\geq\;?$$
dove bisogna trovare il limite inferiore al prodotto delle varianze.
$$\overline{\langle \psi|\hat{A}\psi\rangle}=\langle \hat{A}\psi|\psi\rangle=\langle \psi|\hat{A}\psi\rangle$$
quindi il valor medio è uguale al suo coniugato, quindi è *reale*. Tornando alle disuguaglianze e ricordando che $||\psi||^{2}=\langle \psi|\psi\rangle$
$$\Delta_{\psi}\hat{A}=||(\hat{A}-\langle\hat{A}\rangle_{\psi})|\psi\rangle||^{2}$$
$$\Delta_{\psi}\hat{B}=||(\hat{B}-\langle\hat{B}\rangle_{\psi})|\psi\rangle||^{2}$$
Allora il prodotto è
$$\Delta_{\psi}\hat{A}\Delta_{\psi}\hat{B}=||(\hat{A}-\langle\hat{A}\rangle_{\psi})|\psi\rangle||^{2}+||(\hat{B}-\langle\hat{B}\rangle_{\psi})|\psi\rangle||^{2}\geq\ldots$$
e usando la [[disuguaglianza di Schwarz]] 
$$\ldots\geq|\langle\hat{A}-\langle\hat{A}\rangle_{\psi})\psi\;|\;(\hat{B}-\langle\hat{B}\rangle_{\psi})\psi\rangle|^{2}\geq\ldots$$
Ricordando che la parte immaginaria di un numero complesso $z$ si può scrivere come
$$\Im(z)= \frac{z-z^{\ast}}{2i}$$
$$\ldots\geq[\Im(|\langle\hat{A}-\langle\hat{A}\rangle_{\psi})\psi\;|\;(\hat{B}-\langle\hat{B}\rangle_{\psi})\psi\rangle|)]\geq\ldots$$
Possiamo sviluppare il prodotto scalare
$$\langle\hat{A}-\langle\hat{A}\rangle_{\psi})\psi\;|\;(\hat{B}-\langle\hat{B}\rangle_{\psi})\psi\rangle=\langle \psi|\hat{B}\hat{A}\psi\rangle-\langle \hat{A}\rangle_{\psi}\langle\hat{B}\rangle_{\psi}$$
dove si cancellano alcuni elementi. Prendo il coniugato
$$\overline{\langle\hat{A}-\langle\hat{A}\rangle_{\psi})\psi\;|\;(\hat{B}-\langle\hat{B}\rangle_{\psi})\psi\rangle}=\overline{\langle \psi|\hat{B}\hat{A}\psi\rangle}-\langle \hat{A}\rangle_{\psi}\langle\hat{B}\rangle_{\psi}=\langle \hat{B}\hat{A}\psi|\psi\rangle-\langle \hat{A}\rangle_{\psi}\langle\hat{B}\rangle_{\psi=}$$
$$=\langle \hat{A}\psi|\hat{B}\psi\rangle-\langle \hat{A}\rangle_{\psi}\langle\hat{B}\rangle_{\psi}=\langle \psi|\hat{A}\hat{B}\psi\rangle-\langle \hat{A}\rangle_{\psi}\langle\hat{B}\rangle_{\psi}$$
