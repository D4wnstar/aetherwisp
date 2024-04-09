---
aliases:
  - principio di indeterminazione
---
La **disuguaglianza di Heisenberg**, o **principio di indeterminazione**, è una disuguaglianza che mostra come il prodotto tra l'errore sulla posizione $p$ e quello sulla quantità di moto $q$ di una [[particella]] quantistica ha un minimo costante. Ciò implica che le due quantità non possono essere determinate con precisione arbitraria allo stesso tempo e che misurare con precisione una rende la seconda molto imprecisa. Matematicamente,
$$\Delta\hat{p}\Delta\hat{q}\geq\frac{\hbar}{2}$$
L'errore qui definito non è quello della strumentazione, ma quello intrinseco dovuto alla [[funzione d'onda]] della particella, dato che misure uguali su sistemi preparati allo stesso modo *non* danno lo stesso risultato.
## Derivazione
Prendo $X=\{x_{i}\}^{d}_{i}$ un insieme di $d$ variabili casuali. Definisco una [[distribuzione]] $F:X \rightarrow\mathbb{R}$, $x_{i} \rightarrow F(x_{i})$ che agisce sulle $X$. Dato che le $X$ sono determinate casualmente, non è esiste alcun "valore" di $X$. Al meglio, possiamo definire il valore di aspettazione o quantità simili. Ciò significa anche che non possiamo nemmeno determinare $F$, al di là di una media. Calcoliamo allora proprio questa, o meglio i *momenti* della distribuzione $F$ nello [[stato]] $\Psi$
$$\langle F\rangle_{\Psi}=\sum\limits_{i=1}^{d}p_{i}F(x_{i})$$
$$\langle F^{2}\rangle_{\Psi}=\sum\limits_{i=1}^{d}p_{i}F^{2}(x_{i})$$
$$\Delta_{\Psi}F=\langle F^{2}\rangle_{\Psi}-\langle F\rangle^{2}_{\Psi}$$
In meccanica classica è possibile misurare qualunque cosa, almeno in linea di principio, con precisione arbitraria. In meccanica quantistica, invece, si trova che gli errori su $\hat{p}$ e $\hat{q}$ sono
$$\boxed{\Delta\hat{p}\Delta\hat{q}\geq\frac{\hbar}{2}}$$
che è la **disuguaglianza di Heisenberg**. Per una forma in funzione di due [[Osservabile|osservabili]], vedi [[Misure di osservabili]].
Dunque è impossibile misurare traiettorie per particelle quantistiche, in quanto servirebbe avere misure precise sia per $\hat{p}$ e $\hat{q}$.

Se prendiamo la distribuzione di Gibbs che descrive uno stato misto
$$\rho_{p}(q,p)=\frac{e^{-\beta H(q,p)}}{z_{\beta}}$$
abbiamo il valore di aspettazione
$$\langle F\rangle_{\rho_{\beta}}=\int_{\mathbb{R}^{2}}\rho_{\beta}(q,p)F(q,p)dqdp$$
Possiamo rappresentare un punto nello spazio delle fasi come la distribuzione *[[delta di Dirac]]*
$$(q,p)\rightarrow\delta(q-q_{0}),\;\delta(p-p_{0})$$
Dunque posso pensare ad un punto come appartenere alla stessa "classe" delle distribuzioni nello [[spazio delle fasi]]. Allora abbiamo
$$\langle F\rangle_{\rho_{\beta}}=\int_{\mathbb{R}^{2}}\rho_{\beta}(q,p)F(q,p)dqdp=F(q_{0},p_{0})$$
Naturalmente la notazione di funzione della delta di Dirac $\delta(x-x_{0})$ è un'approssimazione comoda della notazione rigorosa da distribuzione $\delta_{x_{0}}[f]=f(x_{0})$.