Una [[Distribuzione]] si dice **temperata** se è un *funzionale* lineare e continuo definito sullo [[Spazio di Schwartz]] in $\mathbb{C}$. In altre parole, $T:\mathcal{S}\rightarrow C$ è una distribuzione temperata se è lineare rispetto alla struttura di [[spazio vettoriale]] di $\mathcal{S}$ e continua nella convergenza ivi definita, ovvero
$$T(\varphi_{n})\rightarrow T(\varphi)\quad\text{se}\quad\varphi_{n} \rightarrow\varphi\text{ in }\mathcal{S}$$
Lo spazio delle distribuzioni temperate si indica con $\mathcal{S}'$ ed è lo [[spazio duale]] di $\mathcal{S}$.

Si usa anche la notazione $\langle T,\varphi\rangle$ per rappresentare $T(\varphi)$. Se la distribuzione è associata ad una funzione $u$, si usa denotare la distribuzione con $T_{u}(\varphi)$ e talvolta con la forma impropria ma comoda $\langle u,\varphi\rangle$.
### Esempi
La [[Delta di Dirac]] $\delta_{x_{0}}$ è una distribuzione temperata definita come $\langle \delta_{x_{0}},\varphi\rangle=\varphi(x_{0})$. Va notato che è una distribuzione *singolare*, ossia non è associata ad una funzione. Si usa scrivere in modo un po' improprio
$$\langle \delta_{x_{0}},\varphi\rangle=\int_{-\infty}^{+\infty}\delta(x-x_{0})\varphi(x)dx=\varphi(x_{0})$$

Il prodotto di una distribuzione temperata $T$ ed un polinomio $P(x)$ è a sua volta una distribuzione temperata. Infatti, dato che $P(x)\varphi(x)\in\mathcal{S}$, $\langle P(x)T,\varphi\rangle=\langle T,P(x)\varphi\rangle$.
### Convergenza debole
Sia $T_{n}$ una successione di distribuzioni temperate. Si dice che $T_{n}$ *converge in senso debole*, *in senso delle distribuzioni* o *in senso $\mathcal{S}'$* a $T\in\mathcal{S}'$ se, per ogni fissata $\varphi\in\mathcal{S}$, si ha $\langle T_{n},\varphi\rangle \rightarrow \langle T,\varphi\rangle$. Questa definizione rende lo spazio di Schwartz uno [[Spazio metrico completo|spazio completo]].

Ha diverse proprietà utili:
1. se $u_{n}(x)$ è una successione di funzioni $L^{2}$ che converge a $u(x)$ nella norma $L^{2}$ o anche debolmente in $L^{2}$, allora la successione delle distribuzioni associate $T_{u_{n}}$ converge in senso delle distribuzioni a $T_{u}$.
2. lo stesso vale se $u_{n}(x)$ converge ad $u(x)$ in $L^{1}$ [[Convergenza puntuale|puntualmente]] quasi ovunque ed è soddisfatta la [[Teorema della convergenza dominata|convergenza dominata]].
3. lo stesso vale se le $u_{n}(x)$ sono localmente [[Spazi Lp|sommabili]] e limitate (o anche solo maggiorate da un polinomio).
4. in alcuni casi, è possibile che le $u_{n}(x)$ non convergano ad $u(x)$ in senso più tradizionale (come in norma $L^{1}$ o $L^{2}$), ma che individuino delle distribuzioni che convergono ad una distribuzione in senso $\mathcal{S}'$.
5. Sia $e^{inx}$ che $x^{k}e^{inx}$ con $x\in\mathbb{R}$ convergono a 0 in senso $\mathcal{S}'$ per $n \rightarrow\pm\infty$ per ogni fissato $k\in\mathbb{N}$.
### Derivata
La derivata in senso delle distribuzioni è definita come
$$\langle T',\varphi\rangle=-\langle T,\varphi'\rangle$$
Nel caso dell'$n$-esima derivata
$$\langle D^{n}T,\varphi\rangle=(-1)^{n}\langle T,D^{n}\varphi\rangle$$
dove $D^{n}T$ è a sua volta una distribuzione temperata per ogni $n\in\mathbb{N}$. Ciò significa che tutte le distribuzioni sono infinitamente derivabili, anche se associate a funzioni discontinue. In particolare, la derivata distribuzionale di una distribuzione associata ad una funzione continua è singolare. Più in generale, distribuzioni in spazi multidimensionali come $\mathcal{S}(\mathbb{R}^{N})$ sono anche parzialmente derivabili in qualunque variabile infinite volte e vale il [[Teorema di Schwarz]].
### Trasformata di Fourier
La [[Trasformata di Fourier]] e l'antitrasformata sono un automorfismo nello spazio di Schwartz (ossia è lineare biettiva da $\mathcal{S}$ in $\mathcal{S}$) e sono continue usando la convergenza nel senso delle distribuzioni. Si ha allora *per definizione*
$$\langle \mathscr{F}T,\varphi\rangle=\langle T,\mathscr{F}\varphi\rangle$$
che è valida dato che $\mathscr{F}(\varphi)\in\mathcal{S}$. La trasformata $\mathscr{F}T$ è a sua volta una distribuzione temperata. Analogamente
$$\langle \mathscr{F}^{-1}T,\varphi\rangle=\langle T,\mathscr{F}^{-1}\varphi\rangle$$
Presa una successione di distribuzioni temperate $T_{n}\in\mathcal{S}'$ vale anche la continuità
$$\widehat{T}_{n} \rightarrow \widehat{T}$$
