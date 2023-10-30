Cerchiamo predizioni per il sistema $S$. $ME$ sta per *mondo esterno*.

![[Sistema in Mondo Esterno|center]]
Abbiamo che l'[[Hamiltoniana]] del sistema è $\hat{H}_{0}=\hat{H}_{S}+\hat{H}_{ME}+\hat{V}$. Prendiamo l'equazione agli autovalori
$$\hat{H}_{ME}|\phi_{n}\rangle=E_{n}|\phi_{n}\rangle$$
con $n$ l'indice di stato. Per il sistema isolato vale anche
$$\hat{H}_{S}|\varphi_{n}\rangle=\mathcal{E}_{n}|\varphi_{n}\rangle$$
Noi cerchiamo l'equazione
$$\hat{H}_{v}|\psi_{n}\rangle=\mathbb{E} |\psi_{n}\rangle$$
Considero i set degli stati di $S$ e $ME$
$$\{|\phi_{n}\rangle\},\quad\{|\varphi_{n}\rangle\}$$
e dico che sono [[sistemi ortonormali completi]].
Pongo il sistema in una dimensioni e prendo l'Hamiltoniana della particella libera
$$\left[ - \frac{\hbar^{2}}{2m}\frac{\partial ^{2}}{\partial x^{2}}+U(x) \right]\psi(x)=E \psi(x))$$
Uso la relazione di completezza dei [[Proiettore|proiettori]] 
$$\sum\limits_{x}|x\rangle\langle x|\psi\rangle=\sum\limits_{x}\psi(x)|x\rangle$$
con $\psi(x)=\langle x|\psi\rangle$ la rappresentazione in $x$ di $\psi$. Riscrivo $\psi(x)$ come [[trasformata di Fourier]] 
$$\psi(x)=\frac{1}{2\pi}\int dq\; e^{iqx}\tilde{\psi}(q)$$
e la sua antitrasformata
$$\tilde{\psi}(q)=\int dx\;e^{-iqx}\psi(x)$$
Estendo al caso bidimensionale, l'equazione da risolvere è
$$\left[ - \frac{\hbar^{2}}{2m}\bar{v}^{2}+U(\bar{r}) \right]\psi(x,y)=E \psi(x,y))$$
e la trasformata diventa
$$\psi(x,y)= \frac{1}{(2\pi)^{2}}\int dq_{x}\int dq_{y}\;e^{i(q_{x}x+q_{y}y)}\tilde{\psi}(q_{x},q_{y})$$
Uso il [[prodotto tensoriale]] per collegare gli stati del sistema e del mondo esterno
$$\{|\phi_{m}\rangle\otimes |\psi_{n}\rangle\}$$
Assumo che questo oggetto sia un sistema ortonormale completo. Allora posso esprimere lo stato $|\psi\rangle$ come
$$|\psi\rangle=\sum\limits_{m,n}c_{m,n}|\phi_{m}\rangle\otimes\ |\varphi_{n}\rangle$$
