La meccanica quantistica è sostanzialmente un'applicazione dell'algebra lineare a dimensioni infinita e della teoria degli [[Operatore|operatori]]. Si usa quindi una certa notazione che porta a semplificare la parte grafica della matematica necessaria per i calcoli.

La [[notazione braket]] è la base su cui si costruisce tutta la meccanica quantistica. Serve a rappresentare vettori e funzioni, finiti o infiniti, assieme ai loro [[Scalar product|prodotti scalari]] in modo conciso.

Le [[Osservabile|osservabili]] sono proprietà di un oggetto quantistico che possono essere misurate. Queste sono rappresentate come variabili nel senso classico. In particolare, si usano le convenzioni della meccanica razionale e in particolare quella [[Hamiltoniana]]:
- la posizione generalizzata è rappresentata con una $q$ (o $\vec{q}$ o $\vec{r}$ in più dimensioni)
- la quantità di moto è rappresentata con una $p$

Ad ogni osservabile è associato un [[operatore autoaggiunto]] che si denota con un cappuccio: $\hat{q}$ per l'operatore posizione, $\hat{p}$ per l'operatore quantità di moto, e via avanti. Ciò permette di distinguere l'osservabile dall'operatore che agisce sul sistema quantistico, che sono oggetti distinti. Dall'autoaggiuntezza si sa che
$$\langle \Psi| \hat{Q} \Psi \rangle=\langle \hat{Q} \Psi|\Psi \rangle$$
Questo implica il valor medio dell'osservabile associata deve essere reale
$$\left\langle Q \right\rangle=\left\langle Q \right\rangle^{*}$$
con $*$ il coniugato complesso

Dato che la meccanica quantistica è una teoria statistica, è comune cercare il valore di aspettazione di un'osservabile. In notazione braket, il valor medio di un'osservabile in uno stato $\Psi$ è
$$\left\langle Q \right\rangle_{\Psi}=\langle \Psi|\hat{Q}|\Psi\rangle$$
dove $\Psi$ è formalmente una qualunque funzione [[Spazi Lp#Spazio $L {2}$|L^2]], ma quasi sempre una [[funzione d'onda]].

Gli operatori autoaggiunti più comuni sono l'operatore posizione $\hat{q}$, quantità di moto $\hat{p}$ e Hamiltoniana $\hat{H}$, che hanno la forma
$$\hat{q}\equiv q, \quad \hat{p}\equiv \frac{\hbar}{i} \frac{\partial }{\partial q}, \quad \hat{H}\equiv - \frac{\hbar^{2}}{2m} \frac{d^{2}}{dq^{2}} + V(q)$$
con $V(x)$ un [[Potenziale]]. In tre dimensioni hanno invece la forma
$$\hat{\vec{q}}\equiv\vec{q}, \quad \hat{p}_{x}\equiv \frac{\hbar}{i}\frac{\partial }{\partial x}, \quad \hat{p}_{y}\equiv \frac{\hbar}{i}\frac{\partial }{\partial y}, \quad \hat{p}_{z}\equiv \frac{\hbar}{i}\frac{\partial }{\partial z}, \quad \hat{\vec{p}}=\frac{\hbar}{i}\nabla$$
$$\hat{H}\equiv - \frac{\hbar^{2}}{2m}\left(\frac{\partial^{2} }{\partial x^{2}}+\frac{\partial^{2} }{\partial y^{2}}+\frac{\partial^{2} }{\partial z^{2}}\right)+V(\vec{q})=- \frac{\hbar^{2}}{2m}\nabla^{2} + V(\vec{q})$$
con $\nabla^{2}$ il [[Laplacian]].