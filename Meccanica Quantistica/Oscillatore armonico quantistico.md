L'Hamiltoniana di un oscillatore armonico ad una particella è
$$H=\frac{\bar{p}^{2}}{2m}+U(\bar{q})=\frac{\bar{p}^{2}}{2m}+ \frac{m\omega^{2}}{2}\bar{q}^{2}$$
con $(\bar{p},\bar{q})\in\mathbb{R}^{N}\times\mathbb{R}^{N}$, $\bar{p}=m\bar{v}$ e $\bar{q}^{2}=||\bar{q}||^{2}$. Questa risolve le equazioni canoniche di Hamilton
$$\begin{cases} \dot{\bar{q}}=\partial_{\bar{q}}H=\frac{d}{dt}\bar{q}\\
\dot{\bar{p}}=-\partial_{\bar{q}}H=\frac{d}{dt}\bar{p} \\
\end{cases}$$
Definiamo
$$\phi=(\bar{q},\bar{p})\quad,\quad \dot{\phi}=\frac{d\phi}{dt}=\{\phi,H\}$$
dove $\{x,y\}$ sono le [[Parentesi di Poisson]]. Abbiamo, in generale
$$\dot{q}_{1}=\{q_{1},H\}=\partial_{p_{1}}H\quad;\quad \dot{p}_{1}=\{p_{1},H\}=-\partial_{q_{1}}H$$
Dalle scoperte di De Broglie, posso interpretare una particella come un'onda di lunghezza d'onda $\lambda=\frac{h}{p}$ e numero d'onda $k=\frac{2\pi}{\lambda}$. Prendiamo un'onda piana
$$e^{ikx}=e^{i\frac{2\pi}{\lambda}x}=e^{i \frac{p}{h}2\pi x}=e^{\frac{i}{\hbar}px}$$
con $\hbar=\frac{h}{2\pi}$ la [[Costante di Planck|costante di Planck ridotta]]. Per estrarre la $p$ dalla funzione d'onda, possiamo derivare e moltiplicare per una costante
$$-i\hbar\partial_{x}e^{\frac{i}{\hbar}px}=pe^{\frac{i}{\hbar}px}$$
Ma quindi abbiamo trovato un operatore che converte un valore in sé stesso, ma moltiplicato per una costante. Dunque abbiamo trovato una *relazione agli autovalori*.
$$\hat{A}(\bar{v}):\bar{v}\in\mathbb{C}^{n} \longrightarrow\hat{A}\bar{v}\in\mathbb{C}^{n}$$
Usiamo la [[Notazione Braket|notazione ket]] per descrivere i vettori colonna come $\bar{v}$
$$|v\rangle\in\mathbb{C}^{n} \longrightarrow^{\hat{A}} \hat{A}|{v}\rangle\in\mathbb{C}^{n}$$
$\hat{A}$ è una matrice $n$-dimensionale su $\mathbb{C}$ con elementi $A_{ij}$. Abbiamo dunque la relazione
$$\hat{A}|v\rangle=a|v\rangle$$
dove $a$ è l'**autovalore** di $\hat{A}$ e $|v\rangle$ è l'**autovettore** o **autoket** di $\hat{A}$. Tuttavia, nella relazione dell'onda sembrano esserci due scalari, non due vettori. Definisco allora
$$\boxed{\psi_{p}(x)=e^{\frac{i}{\hbar}px}}$$
e scrivo $(-i\hbar\partial_{x}\psi_{p})(x)=p\psi_{p}(x)$. Però si può vedere una funzione come una sorta di "vettore continuo", che abbia infiniti elementi che il valore della funzione $\psi_{p}(x)$ sia l'$x$-esimo "componente" di questo vettore. Ci basta che la norma di questo vettore infinito sia finita. In pratica, vogliamo che la funzione $\psi_{p}$ sia *a quadrato sommabile*, cioè che sia in $L^{2}$. Nel nostro caso, la funzione non è quadrato-sommabile:
$$\int_{-\infty}^{\infty}|\psi_{p}(x)|^{2}dx=|A|^{2}\int_{-\infty}^{\infty}dx$$
In genere, questo accade quando si parla di oggetti che sono liberi di andare da $-\infty$ a $+\infty$. In ogni caso, è possibile trovare un estensione anche per questi casi, usando ciò che si chiamano **pseudoket**.

Nel caso si normalizzi la funzione d'onda
$$\psi(x)\rightarrow\phi(x)=\frac{\psi(x)}{||\psi(x)||}$$
si trovano *distribuzioni di probabilità*. In sostanza, lo [[Stato]] del sistema è **stocastico**.

Abbiamo che la *funzione momento quantistica* $\hat{p}$ sarà quella funzione tale per cui è vera
$$(\hat{p}\psi)(x)=-i\hbar\partial_{x}\psi(x)$$
$$\boxed{\hat{p}=-i\hbar\partial_{x}}$$
Nel caso vettoriale, si passa semplicemente al gradiente
$$\boxed{\hat{\bar{p}}=-i\hbar\nabla_{\bar{r}}}$$
Per un sistema quantistico, le variabili di stato sono $q$, la posizione, e $p$, la fase.