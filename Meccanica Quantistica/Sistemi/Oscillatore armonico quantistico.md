L'**oscillatore armonico quantistico** è l'analogo quantistico dell'[[oscillatore armonico]] classico, ossia un sistema quantistico con un [[punto di equilibrio]] soggetto ad una forza di ritorno $F$ una volta perturbato.
## Soluzione
Il caso dell'oscillatore armonico consiste nel risolvere l'[[equazione di Schrödinger]] per una [[particella]] immersa nel [[potenziale]]
$$V(x)=\frac{1}{2}m\omega^{2}x^{2}$$
Partiamo dunque dall'equazione indipendente dal tempo, che prende la forma
$$- \frac{\hbar^{2}}{2m} \frac{d^{2}\psi}{dx^{2}}+ \frac{1}{2}m\omega^{2}x^{2}\psi=E\psi\tag{1}$$
Esistono due modi comuni per risolvere questa equazione: un modo semplice e "di forza bruta" che sfrutta le [[serie di potenze]] e un metodo algebrico che sfrutta le cosiddette operazioni a scala.
### Metodo algebrico
Riscriviamo la $(1)$ in un modo più comodo, usando l'[[operatore]] di quantità di moto $p\equiv (\hbar/i)d/dx$:
$$\frac{1}{2m}[p^{2}+(m\omega x)^{2}]\psi=E\psi$$
da cui otteniamo la nota [[Hamiltoniana]] dell'oscillatore armonico
$$H=\frac{1}{2m}[p^{2}+(m\omega x)^{2}]$$
L'idea è fattorizzare l'Hamiltoniana usando
$$z^{2}+w^{2}=(iz+w)(-iz+w)$$
ma bisogna fare particolare attenzione, dato che $x$ e $p$ *non* sono numeri, bensì operatori, e perché la precedente equazione sia vera bisogna che valga la commutatività. Per il prodotto tra scalari è garantita, ma per due operatori in genere no, nel senso che $xp\neq px$. Detto ciò, possiamo comunque analizzare le seguenti quantità
$$a_{\pm}\equiv \frac{1}{\sqrt{2\hbar m\omega}}(\mp ip+m\omega x)$$
Il fattore di scala iniziale è solo per comodità. Controlliamo il prodotto $a_{-}a_{+}$:
$$a_{+}a_{-}=\frac{1}{2\hbar m \omega}(-ip+m\omega x)(ip+m\omega x)=\frac{1}{2\hbar m\omega}[p^{2}+(m\omega x)^{2}-im\omega(xp-px)]$$
dove ritroviamo il [[commutatore]] di $x$ e $p$ al terzo termine nelle parentesi. Estraendo l'ultimo termine e esplicitando il commutatore otteniamo
$$a_{+}a_{-}=\frac{1}{2\hbar m\omega}[p^{2}+(m\omega x)^{2}] - \frac{i}{2\hbar}[x,p]\tag{2}$$
Calcoliamo allora il commutatore tra $x$ e $p$, aggiungendo una funzione di test dato che sono operatori:
$$[x,p]\varphi(x)=\left[x \frac{\hbar}{i} \frac{d\varphi}{dx}- \frac{\hbar}{i} \frac{d}{dx} (x\varphi)\right]=\frac{\hbar}{i}\left(x \frac{d\varphi}{dx}-x \frac{d\varphi}{dx}-\varphi\right)=i\hbar\varphi$$
da cui si trova la relazione commutativa canonica
$$\boxed{[x,p]=i\hbar}$$
Tornando alla $(2)$, abbiamo
$$a_{+}a_{-}=\frac{1}{\hbar \omega}H- \frac{1}{2}$$
Riconoscendo che $[a_{+},a_{-}]=1$, possiamo esprimere l'Hamiltoniana come
$$H=\hbar\omega\left(a_{+}a_{-}+ \frac{1}{2}\right)$$
che possiamo sostituire nell'equazione di Schrödinger
$$\hbar\omega\left(a_{\pm}a_{\mp}\pm \frac{1}{2}\right)\psi=E\psi\tag{3}$$
Si dimostra[^1] che se $\psi$ soddisfa l'equazione di Schrödinger per l'energia $E$, allora $(a_{+}\psi)$ soddisfa l'equazione per energia $E+\hbar\omega$. Allo stesso modo, $(a_{-}\psi)$ soddisfa l'equazione per $E-\hbar\omega$. Gli operatori $a_{\pm}$ sono detti [[operatori di creazione e distruzione|operatori scaletta]] e permettono di aumentare e diminuire lo stato di energia.

Applicando a catena l'operatore di discesa si arriva eventualmente ad una soluzione non normalizzabile: questa non è altro che lo stato fondamentale del sistema. Per questa, vale $a_{-}\psi_{0}=0$. Da qui in poi, l'operatore di discesa smette di darci nuove soluzioni, dato che $a_{-}(0)=0$. Possiamo così determinare la funzione d'onda (spaziale) dello stato fondamentale:
$$\frac{1}{\sqrt{2\hbar m\omega}}\left(\hbar \frac{d}{dx}+m\omega x\right)\psi_{0}=0\quad \rightarrow \quad \frac{d\psi_{0}}{dx}=- \frac{m\omega}{\hbar} x\psi_{0}$$
L'equazione differenziale è facilmente risolvibile per quadratura:
$$\int \frac{d\psi_{0}}{\psi_{0}}=- \frac{m\omega}{\hbar}\int xdx \quad\rightarrow \quad\ln\psi_{0}=- \frac{m\omega}{2\hbar} x^{2}+K$$
con $K$ una costante. Allora
$$\psi_{0}(x)=Ae^{-(m\omega/2\hbar) x^{2}}$$
con $A$ la costante di normalizzazione (che ha assorbito $K$). Possiamo trovare $A$ velocemente
$$1=|A|^{2}\int_{-\infty}^{+\infty} e^{-m\omega x^{2}/\hbar}dx=|A|^{2}\sqrt{\frac{\pi\hbar}{m\omega}} \quad\rightarrow\quad A=\left(\frac{m\omega}{\pi\hbar}\right)^{1/4}$$
quindi la funzione d'onda spaziale dello stato fondamentale è
$$\boxed{\psi_{0}(x)=\left(\frac{m\omega}{2\hbar}\right)^{1/4}e^{-(m\omega/2\hbar)x^{2}}}$$
Possiamo determinarne l'energia sostituendola nell'equazione di Schrödinger $(3)$:
$$\hbar\omega\left(a_{\pm}a_{\mp}\pm \frac{1}{2}\right)\psi_{0}=E_{0}\psi_{0} \quad \rightarrow \quad E_{0}=\frac{1}{2}\hbar \omega$$
Ora che abbiamo una base, trovare gli altri stati è banale: basta applicare l'operatore di salita a catena per trovare l'$n$-esimo stato eccitato, aumentando l'energia di $\hbar\omega$ ogni salto. Abbiamo quindi trovato due cose: l'equazione d'onda spaziale di tutti gli stati dell'oscillatore armonico quantistico e tutte le energie permesse a loro associate:
$$\psi_{n}(x)=A_{n}(a_{+})^{n}\psi_{0}(x)\quad\text{con}\quad E_{n}=\left(n+ \frac{1}{2}\right)\hbar\omega$$
con $A_{n}$ la costante di normalizzazione dell'$n$-esimo stato.

In realtà è anche possibile derivare le costanti $A_{n}$ algebricamente, usando gli operatori scaletta. Consideriamo il fatto che i due operatori scaletta sono l'[[Operatore aggiunto|aggiunto]] l'un dell'altro, quindi $(\psi,a_{\pm}\varphi,a_{\mp}\psi,\varphi)$, usando il [[Prodotto scalare|prodotto hermitiano]] $\langle \cdot|\cdot\rangle$. Sappiamo che $a_{\pm}\psi_{n}$ è proporzionale a $\psi_{n+1}$ tramite le relazioni
$$a_{+}\psi_{n}=c_{n}\psi_{n+1}, \quad a_{-}\psi_{n}=d_{n}\psi_{n-1}\tag{4}$$
Vogliano conoscere le costanti $c_{n}$ e $d_{n}$. Vale
$$\langle a_{\pm}\psi_{n}|a_{\pm}\psi_{n}\rangle=\langle a_{\mp}a_{\pm}\psi_{n}|\psi_{n}\rangle$$
Ma sappiamo che $a_{+}a_{-}\psi_{n}=n\psi_{n}$ e $a_{-}a_{+}\psi_{n}=(n+1)\psi_{n}$, da cui
$$\langle a_{+}a_{-}\psi_{n}|\psi_{n}\rangle=\langle n\psi_{n}|\psi_{n}\rangle=n\int_{-\infty}^{+\infty}|\psi_{n}|^{2}dx$$
$$\langle a_{-}a_{+}\psi_{n}|\psi_{n}\rangle=\langle(n+1)\psi_{n}|\psi_{n}\rangle=(n+1)\int_{-\infty}^{+\infty}|\psi_{n}|^{2}dx$$
Ma le $\psi_{n}$ sono normalizzate, quindi $n+1=|c_{n}|^{2}$ e $n=|d_{n}|^{2}$. Mettendole nella $(4)$, si ha
$$\boxed{a_{+}\psi_{n}=\sqrt{n+1}\psi_{n+1},\quad a_{-}\psi_{n}=\sqrt{n}\psi_{n-1}}$$
da cui la forma definitiva del $n$-esimo stato dell'oscillatore armonico quantistico:
$$\boxed{\psi_{n}=\frac{1}{\sqrt{n!}}(a_{+})^{n}\psi_{0}=\frac{1}{\sqrt{n!}}(a_{+})^{n}\left(\frac{m\omega}{2\hbar}\right)^{1/4}e^{-(m\omega/2\hbar)x^{2}}\quad\text{con}\quad E_{n}=\left(n+ \frac{1}{2}\right)\hbar\omega}$$

L'energia potenziale media è[^2]
$$\left\langle V \right\rangle=\left\langle \frac{1}{2}m\omega^{2}x^{2} \right\rangle=\frac{1}{2}m\omega^{2} \left\langle x^{2} \right\rangle=\ldots=\frac{1}{2}\hbar\omega\left(n+ \frac{1}{2}\right)$$
cioè esattamente metà dell'energia totale, come nel caso classico.
## Risultati
Le $\psi_{n}$ così trovate sono curiosamente diverse dalle soluzioni del moto classico: da una parte, abbiamo che l'energia è quantizzata; dall'altra, notiamo fenomeni che né si osservano né si spiegano in meccanica classica, come il fatto che la probabilità che la particella si trovi al di fuori dell'ampiezza (classica) dell'oscillatore *non* è zero e che la probabilità di trovarsi al centro dell'oscillatore negli stati dispari è *sempre* 0.

Si nota anche che per stati di energia sufficientemente alti ($n\gg1$), la probabilità di osservare la particella in una data posizione è approssimativamente uguale quella classica, se si prende la media.

![[Stati stazionari oscillatore armonico quantistico.png]]
*Da Introduction to Quantum Mechanics di Griffiths*


---

L'[[Hamiltoniana]] di un oscillatore armonico ad una particella è
$$H=\frac{\bar{p}^{2}}{2m}+U(\bar{q})=\frac{\bar{p}^{2}}{2m}+ \frac{m\omega^{2}}{2}\bar{q}^{2}$$
con $(\bar{p},\bar{q})\in\mathbb{R}^{N}\times\mathbb{R}^{N}$, $\bar{p}=m\bar{v}$ e $\bar{q}^{2}=||\bar{q}||^{2}$. Questa risolve le equazioni canoniche di Hamilton
$$\begin{cases} \dot{\bar{q}}=\partial_{\bar{q}}H=\frac{d}{dt}\bar{q}\\
\dot{\bar{p}}=-\partial_{\bar{q}}H=\frac{d}{dt}\bar{p} \\
\end{cases}$$
Definiamo
$$\phi=(\bar{q},\bar{p})\quad,\quad \dot{\phi}=\frac{d\phi}{dt}=\{\phi,H\}$$
dove $\{x,y\}$ sono le [[parentesi di Poisson]]. Abbiamo, in generale
$$\dot{q}_{1}=\{q_{1},H\}=\partial_{p_{1}}H\quad;\quad \dot{p}_{1}=\{p_{1},H\}=-\partial_{q_{1}}H$$
Dalle scoperte di De Broglie, posso interpretare una particella come un'onda di lunghezza d'onda $\lambda=\frac{h}{p}$ e numero d'onda $k=\frac{2\pi}{\lambda}$. Prendiamo un'onda piana
$$e^{ikx}=e^{i\frac{2\pi}{\lambda}x}=e^{i \frac{p}{h}2\pi x}=e^{\frac{i}{\hbar}px}$$
con $\hbar=\frac{h}{2\pi}$ la [[Costante di Planck|costante di Planck ridotta]]. Per estrarre la $p$ dalla funzione d'onda, possiamo derivare e moltiplicare per una costante
$$-i\hbar\partial_{x}e^{\frac{i}{\hbar}px}=pe^{\frac{i}{\hbar}px}$$
Ma quindi abbiamo trovato un operatore che converte un valore in sé stesso, ma moltiplicato per una costante. Dunque abbiamo trovato una *relazione agli autovalori*.
$$\hat{A}(\bar{v}):\bar{v}\in\mathbb{C}^{n} \longrightarrow\hat{A}\bar{v}\in\mathbb{C}^{n}$$
Usiamo la [[notazione braket|notazione ket]] per descrivere i vettori colonna come $\bar{v}$
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
si trovano *distribuzioni di probabilità*. In sostanza, lo [[stato]] del sistema è **stocastico**.

Abbiamo che la *funzione momento quantistica* $\hat{p}$ sarà quella funzione tale per cui è vera
$$(\hat{p}\psi)(x)=-i\hbar\partial_{x}\psi(x)$$
$$\boxed{\hat{p}=-i\hbar\partial_{x}}$$
Nel caso vettoriale, si passa semplicemente al gradiente
$$\boxed{\hat{\bar{p}}=-i\hbar\nabla_{\bar{r}}}$$
Per un sistema quantistico, le variabili di stato sono $q$, la posizione, e $p$, la fase.


[^1]: Soddisfare l'equazione di Schrödinger significa che vale $H\psi=E\psi$, quindi vogliamo trovare $H(a_{+}\psi)=(E+\hbar\omega)\psi$. Difatti, si ha$$H(a_{+}\psi)=\hbar\omega\left(a_{+}a_{-}+ \frac{1}{2}\right)(a_{+}\psi)=\hbar\omega\left(a_{+}a_{-}a_{+}+ \frac{1}{2}a_{+}\right)\psi=\hbar\omega a_{+}\left(a_{-}a_{+}+ \frac{1}{2}\right)\psi=$$$$=a_{+}\left[\hbar\omega\left(\underbrace{a_{+}a_{-}+1}\limits_{*}+ \frac{1}{2}\right)\psi\right]=a_{+}(H+\hbar\omega)\psi=a_{+}(E+\hbar\omega)\psi=(E+\hbar\omega)(a_{+}\psi)$$dove in $*$ abbiamo usato il commutatore $[a_{+},a_{-}]=1$ per affermare $a_{-}a_{+}=a_{+}a_{-}+1$.

[^2]: L'integrale che compare da $\left\langle x^{2} \right\rangle=\int_{-\infty}^{+\infty}\psi_{0}^{*}x^{2}\psi_{0}\;dx$ può essere risolto usando tecniche per [[integrali di posizione e quantità di moto]].