Si dice **operatore** o **trasformazione lineare** $T$ un [[operatore]] tra due [[spazio di Hilbert|spazi di Hilbert]] $H$ e $H'$ per il quale vale
$$T(\alpha x +\beta y)=\alpha T(x)+\beta T(y)\quad\text{dove}\quad \alpha,\beta\in\mathbb{C},\;x,y\in H$$
Un operatore lineare biettivo si dice anche **isomorfismo**. Se invece è da $H$ in $H$ è detto **endomorfismo**. Se è sia un isomorfismo che un endomorfismo si dice **automorfismo**.
### Continuità
Un operatore lineare si dice *continuo* in $x_{0}$ se
$$\lim\limits_{x \rightarrow x_{0}} Tx = Tx_{0}$$
o in termini di [[norma]]
$$\lim\limits_{||x-x_{0}||\rightarrow0} ||Tx-Tx_{0}|| = 0$$
Per dimostrare che un operatore sia continuo ovunque, in realtà basta dimostrare che sia continuo in un solo punto.

Ad esempio, l'operatore derivata $d/dx$ è lineare ma non continuo.
### Limitatezza
Un operatore lineare $T$ si dice *limitato* se la quantità $||Tx||/||x||$ al variare di $x$ nel dominio $D$ dell'operatore si mantiene limitata. In simboli
$$\sup\limits_{x\in D} \frac{||Tx||}{||x||}=K<+\infty$$
Si esclude il caso $x=0$, dove $T(0)=0$. La quantità $K$ si dice *norma* dell'operatore e si indica con $||T||$, ed è effettivamente una norma applicata allo spazio vettoriale degli operatori lineari limitati in uno spazio di Hilbert. Vale la disuguaglianza
$$||Tx||\leq||T||\;||x||$$
Un caso importante sono gli "operatori di moltiplicazione" $Tf(x)=h(x)f(x)$ con $f(x)$ funzione [[Metodi Matematici della Fisica/Spazi di Hilbert/Spazi Lp#Spazio $L {2}$|a quadrato sommabile]] $L^{2}(I)$ e $h=h(x)$ è una funzione assegnata. In questi casi, vale $||T||=\sup\limits_{x\in I} |h(x)|$, infatti
$$||Tf||^{2}=\int_{I}|h(x)f(x)|^{2}dx\leq\sup\limits_{x\in I}|h(x)|^{2}||f||^{2}$$
### Equivalenza
Si dimostra che continuità e limitatezza sono proprietà equivalenti, ossia un operatore lineare continuo è anche limitato e viceversa.
### Forma matriciale
Scegliamo per semplicità $H=H'$ e prendiamo un [[sistema ortonormale completo]] $\{e_{i}\}$ in $H$. I [[Prodotto scalare|prodotti scalari]] $(e_{i},Te_{j})=T_{ij}$ sono gli elementi della matrice rappresentativa dell'operatore lineare $T$. Nel caso $T$ sia limitato, è possibile calcolare le componenti del vettore trasformato usando questi elementi. Posto $x'=Tx$, le componenti $x_{i}'$ di $x'$ sono
$$x'_{i}=\sum\limits_{j=1}^{\infty}T_{ij}x_{j}$$
Ciò non è necessariamente vero se $T$ non è limitato.