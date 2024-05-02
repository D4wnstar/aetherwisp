Cerchiamo predizioni per il sistema $S$. $ME$ sta per *mondo esterno*. Sistema e mondo esterno insieme fanno l'universo $U$.

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
con $\psi(x)=\langle x|\psi\rangle$ la rappresentazione in $x$ di $\psi$. Riscrivo $\psi(x)$ come [[Trasformata di Fourier]] 
$$\psi(x)=\frac{1}{2\pi}\int dq\; e^{iqx}\tilde{\psi}(q)$$
e la sua antitrasformata
$$\tilde{\psi}(q)=\int dx\;e^{-iqx}\psi(x)$$
Estendo al caso bidimensionale, l'equazione da risolvere è
$$\left[ - \frac{\hbar^{2}}{2m}\bar{v}^{2}+U(\bar{r}) \right]\psi(x,y)=E \psi(x,y))$$
e la trasformata diventa
$$\psi(x,y)= \frac{1}{(2\pi)^{2}}\int dq_{x}\int dq_{y}\;e^{i(q_{x}x+q_{y}y)}\tilde{\psi}(q_{x},q_{y})$$
Uso il [[prodotto tensoriale]] per collegare gli stati del sistema e del mondo esterno
$$\{|\phi_{m}\rangle\otimes |\psi_{n}\rangle\}$$
che ci dà una base completa per l'universo.
Assumo che questo oggetto sia un sistema ortonormale completo. Allora posso esprimere lo stato $|\psi\rangle$ come
$$|\psi\rangle=\sum\limits_{m,n}c_{m,n}|\phi_{m}\rangle\otimes\ |\varphi_{n}\rangle$$
Chiamo $\langle \hat{O}_{S} \rangle$ il valore di aspettazione dell'osservabile che descrive lo stato del sistema
$$\langle \hat{O}_{S} \rangle= \frac{\langle \psi|\hat{I}_{ME}\otimes\hat{O}_{S}|\psi\rangle}{\langle \psi|\psi\rangle}$$
con $\hat{I}_{ME}$ l'identità del mondo esterno. Ora uso l'[[Equazione di Schrödinger]] per descrivere l'evoluzione del sistema
$$i\hbar \frac{\partial }{\partial t}|\psi_{U}\rangle=\hat{H}_{U}|\psi_{U}\rangle$$
$$|\psi_{U}(t)\rangle=e^{-i \frac{\hat{H}_{U}t}{\hbar}}|\psi_{U}(t)\rangle$$
$$\langle \psi(t)|\psi(t)\rangle=\langle \psi(0)|e^{i \frac{\hat{H}t}{\hbar}}e^{-i \frac{\hat{H}t}{\hbar}}|\psi(0)\rangle=\langle \psi(0)|\psi(0)\rangle$$
quindi la norma quadra è costante nel tempo, quindi conserva la normalizzazione.
$$\overline{\langle \hat{O}_{S} \rangle}= \frac{\overline{\langle \psi(t)|\hat{I}_{ME}\otimes\hat{O}_{S}|\psi(t)\rangle}}{\langle \psi(0)|\psi(0)\rangle}$$
Usiamo la completezza della base ottenuta dal prodotto tensoriale per ottenere lo stato al tempo $t$ 
$$|\psi(t)\rangle=\sum\limits_{n,m}c_{mn}(t)|\phi_{m}\rangle\otimes |\psi_{n}\rangle$$
$$\overline{\langle \hat{O}_{S} \rangle}=\frac{\sum\limits_{m,n}\sum\limits_{m',n'}\overline{c^{\ast}_{m'n'}(t)c_{mn}(t)}(\langle \phi_{m'}|\otimes \langle \varphi_{n'}|)\hat{I}_{ME}\otimes\hat{O}_{S}(|\phi_{m}\rangle\otimes |\varphi_{n}\rangle)}{\langle \psi|\psi\rangle}=$$
$$=\frac{\sum\limits_{m,n,m',n'}\overline{c^{\ast}_{m'n'}(t)c_{mn}(t)}\langle \phi_{m'}|\hat{I}_{ME} |\phi_{m}\rangle\langle \varphi_{n'}|\hat{O}_{S} |\varphi_{n}\rangle}{\langle \psi|\psi\rangle}\equiv$$
$$\equiv \frac{\sum\limits_{m,n,m',n'}\overline{c^{\ast}_{m'n'}(t)c_{mn}(t)}O_{S,n'n}}{\langle \psi|\psi\rangle}$$
Vale anche
$$\langle \psi|\psi\rangle=\sum\limits_{m,n}|c_{mn}(t)|^{2}$$
Definisco
$$\rho_{nn'}=\overline{\sum\limits_{m}c^{\ast}_{mn'}(t)c_{mn}(t)}$$
Allora ho
$$\overline{\langle \hat{O}_{S} \rangle}=\frac{\sum\limits_{nn'}\rho_{nn'}O_{S,n'n}}{\sum\limits_{n}\rho_{nn}}=\frac{\mbox{Tr}(\hat{\rho}\hat{O}_{S})}{\mbox{Tr}\hat{\rho}}$$
con $\mbox{Tr}$ la [[Traccia]] di un operatore, con
$$\hat{\rho}=\sum\limits_{nn'}|n\rangle\langle n'|\rho_{nn'}$$
Tornando all'equazione di Schroedinger usiamo
$$|n_{t}\rangle=e^{-i \frac{\hat{H}_{S}t}{\hbar}}|n\rangle \Rightarrow i\hbar \frac{\partial }{\partial t}|n_{t}\rangle=\hat{H}_{S}|n_{t}\rangle$$
Allora
$$i\hbar \frac{\partial }{\partial t}\hat{\rho}=\sum\limits_{nn'}\rho_{nn'}\left[ \left( i\hbar \frac{\partial }{\partial t} |n\rangle\right)\langle n|+|m\rangle i\hbar \frac{\partial }{\partial t} \langle n|\right]$$
$$i\hbar \frac{\partial }{\partial t}\hat{\rho}=\sum\limits_{nn'}\rho_{nn'}(\hat{H}_{S}|n\rangle\langle n'|-|n\rangle\langle n'|\hat{H}_{S})=\sum\limits_{nn'}[\hat{H}_{S},\rho_{nn'}|n\rangle\langle n'|]=[\hat{H}_{S},\hat{\rho}]$$
usando il [[commutatore]]. Va notato che questo risultato è *diverso* dalla [[rappresentazione di Heisenberg]]
$$\begin{align}
i\hbar \frac{\partial \hat{\rho}}{\partial t}&=[\hat{H}_{S},\hat{\rho}] \\
i\hbar \frac{\partial \hat{A}}{\partial t}&=[\hat{A},H] \mbox{ rappresentazione di Heisenberg}
\end{align}$$
