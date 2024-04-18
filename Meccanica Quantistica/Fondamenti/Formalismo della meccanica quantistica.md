La meccanica quantistica è sostanzialmente un'applicazione dell'algebra lineare a dimensioni infinita e della teoria degli [[operatore|operatori]]. Si usa quindi una certa notazione che porta a semplificare la parte grafica della matematica necessaria per i calcoli.

La [[notazione braket]] è la base su cui si costruisce tutta la meccanica quantistica. Serve a rappresentare vettori e funzioni, finiti o infiniti, assieme ai loro [[Prodotto scalare|prodotti scalari]] in modo conciso.

Le [[Osservabile|osservabili]] sono proprietà di un oggetto quantistico che possono essere misurate. Queste sono rappresentate come variabili nel senso classico. In particolare, si usano le convenzioni della meccanica razionale e in particolare quella [[Hamiltoniana]]:
- la posizione generalizzata è rappresentata con una $q$
- la quantità di moto è rappresentata con una $p$

Ad ogni osservabile è associato un [[operatore autoaggiunto]] che si denota con un cappuccio: $\hat{q}$ per l'operatore posizione, $\hat{p}$ per l'operatore quantità di moto, e via avanti. Ciò permette di distinguere l'osservabile dall'operatore che agisce sul sistema quantistico, che sono oggetti distinti. Dall'autoaggiuntezza si sa che
$$\langle \Psi| \hat{Q} \Psi \rangle=\langle \hat{Q} \Psi|\Psi \rangle$$
con $*$ il coniugato complesso. Questo implica il valor medio dell'osservabile associata deve essere reale
$$\left\langle Q \right\rangle=\left\langle Q \right\rangle^{*}$$

Dato che la meccanica quantistica è una teoria statistica, è comune cercare il valore di aspettazione di un'osservabile. In notazione braket, il valor medio di un'osservabile in uno stato $\Psi$ è
$$\left\langle Q \right\rangle_{\Psi}=\langle \Psi|\hat{Q}|\Psi\rangle$$
dove $\Psi$ è formalmente una qualunque funzione [[Spazi Lp#Spazio $L {2}$|L^2]], ma quasi sempre una [[funzione d'onda]].

Gli operatori autoaggiunti più comuni sono l'operatore posizione $\hat{q}$, quantità di moto $\hat{p}$ e Hamiltoniana $\hat{H}$, che hanno la forma
$$\hat{q}\equiv q, \quad \hat{p}\equiv \frac{i}{\hbar} \frac{\partial }{\partial x}, \quad \hat{H}\equiv - \frac{\hbar^{2}}{2m} \frac{d^{2}}{dx^{2}} + V(x)$$
con $V(x)$ un [[potenziale]].