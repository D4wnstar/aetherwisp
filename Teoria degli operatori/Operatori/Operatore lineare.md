Si dice **operatore** o **trasformazione lineare** $T$ un [[Operatore]] tra due [[Spazio di Hilbert|spazi di Hilbert]] $H$ e $H'$ per il quale vale
$$T(\alpha x +\beta y)=\alpha T(x)+\beta T(y)\quad\text{dove}\quad \alpha,\beta\in\mathbb{C},\;x,y\in H$$
Un operatore lineare biettivo si dice anche **isomorfismo**. Se invece è da $H$ in $H$ è detto **endomorfismo**. Se è sia un isomorfismo che un endomorfismo si dice **automorfismo**.
### Continuità
Un operatore lineare si dice *continuo* in $x_{0}$ se
$$\lim\limits_{x \rightarrow x_{0}} Tx = Tx_{0}$$
o in termini di [[Norma]]
$$\lim\limits_{||x-x_{0}||\rightarrow0} ||Tx-Tx_{0}|| = 0$$
Per dimostrare che un operatore sia continuo ovunque, in realtà basta dimostrare che sia continuo in un solo punto.

Ad esempio, l'operatore derivata $d/dx$ è lineare ma non continuo.
### Limitatezza
Un operatore lineare $T$ si dice *limitato* se la quantità $||Tx||/||x||$ al variare di $x$ nel dominio $D$ dell'operatore si mantiene limitata. In simboli
$$\sup\limits_{x\in D} \frac{||Tx||}{||x||}=K<+\infty$$
Si esclude il caso $x=0$, dove $T(0)=0$. La quantità $K$ si dice *norma* dell'operatore e si indica con $||T||$, ed è effettivamente una norma applicata allo spazio vettoriale degli operatori lineari limitati in uno spazio di Hilbert. Vale la disuguaglianza
$$||Tx||\leq||T||\;||x||$$
Un caso importante sono gli "operatori di moltiplicazione" $Tf(x)=h(x)f(x)$ con $f(x)$ funzione [[Spazi Lp#Spazio $L {2}$|a quadrato sommabile]] $L^{2}(I)$ e $h=h(x)$ è una funzione assegnata. In questi casi, vale $||T||=\sup\limits_{x\in I} |h(x)|$, infatti
$$||Tf||^{2}=\int_{I}|h(x)f(x)|^{2}dx\leq\sup\limits_{x\in I}|h(x)|^{2}||f||^{2}$$
### Equivalenza
Si dimostra che continuità e limitatezza sono proprietà equivalenti, ossia un operatore lineare continuo è anche limitato e viceversa.
### Forma matriciale
Scegliamo per semplicità $H=H'$ e prendiamo un [[Sistema ortonormale completo]] $\{e_{i}\}$ in $H$. I [[Prodotto scalare|prodotti scalari]] $(e_{i},Te_{j})=T_{ij}$ sono gli elementi della matrice rappresentativa dell'operatore lineare $T$. Nel caso $T$ sia limitato, è possibile calcolare le componenti del vettore trasformato usando questi elementi. Posto $x'=Tx$, le componenti $x_{i}'$ di $x'$ sono
$$x'_{i}=\sum\limits_{j}T_{ij}x_{j}$$
Ciò non è necessariamente vero se $T$ non è limitato. Naturalmente, se l'operatore è infinito-dimensionale, la matrice diventa un concetto più astratto, specialmente se su un sistema continuo e non discreto.
### Decomposizione spettrale
Preso un operatore $T$ con un sistema ortonormale di [[Equazione agli autovalori|autovettori]] $\{e_{n}\}_{n\in\mathbb{N}}$ tali che sia soddisfatta
$$Te_{n}=t_{n}e_{n}$$
con $t_{n}$ gli autovalori associati, è possibile esprimere l'operatore con la sua **decomposizione spettrale**:
$$T=\sum\limits_{n}t_{n} e_{n}^{*}\cdot e_{n}=\sum\limits_{n}t_{n}|e_{n}\rangle \langle e_{n}|=\sum\limits_{n}t_{n}\hat{P}_{e_{n}}$$
dove si è scritto usando il complesso coniugato $*$, la [[notazione braket]] e il [[Proiettore]] sul $n$-esimo vettore di base.