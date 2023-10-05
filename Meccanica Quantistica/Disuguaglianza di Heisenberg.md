Prendo $X=\{x_{i}\}^{d}_{i}$ un set di $d$ variabili casuali.
Definisco $F:X \rightarrow\mathbb{R}\quad x_{i} \rightarrow F(x_{i})$ una distribuzione che agisce sulle $X$. Non potendo conoscere $X$ esattamente, non possiamo conoscere nemmeno $F$ esattamente. Possiamo però calcolare i *momenti* della distribuzione $F$
$$\langle F\rangle_{\pi}=\sum\limits_{i=1}^{d}p_{i}F(x_{i})$$
$$\langle F^{2}\rangle_{\pi}=\sum\limits_{i=1}^{d}p_{i}F^{2}(x_{i})$$
$$\Delta_{\pi}F=\langle F^{2}\rangle_{\pi}-\langle F\rangle^{2}_{\pi}$$
In meccanica classica è possibile misurare qualunque cosa, almeno in linea di principio, con precisione arbitraria. In meccanica quantistica, invece, si trova che gli errori su $\hat{p}$ e $\hat{q}$ sono
$$\boxed{\Delta\hat{p}\Delta\hat{q}\geq\frac{\hbar}{2}}$$
che è la **disuguaglianza di Heisenberg**.
Dunque è impossibile misurare traiettorie per particelle quantistiche, in quanto servirebbe avere misure precise sia per $\hat{p}$ e $\hat{q}$.

Se prendiamo la distribuzione di Gibbs che descrive uno [[stato]] misto
$$\rho_{p}(q,p)=\frac{e^{-\beta H(q,p)}}{z_{\beta}}$$
abbiamo il valore di aspettazione
$$\langle F\rangle_{\rho_{\beta}}=\int_{\mathbb{R}^{2}}\rho_{\beta}(q,p)F(q,p)dqdp$$
Possiamo rappresentare un punto nello spazio delle fasi come la distribuzione *[[delta di Dirac]]*
$$(q,p)\rightarrow\delta(q-q_{0}),\;\delta(p-p_{0})$$
Dunque posso pensare ad un punto come appartenere alla stessa "classe" delle distribuzioni nello [[spazio delle fasi]]. Allora abbiamo
$$\langle F\rangle_{\rho_{\beta}}=\int_{\mathbb{R}^{2}}\rho_{\beta}(q,p)F(q,p)dqdp=F(q_{0},p_{0})$$
Naturalmente la notazione di funzione della delta di Dirac $\delta(x-x_{0})$ è un'approssimazione comoda della notazione rigorosa da distribuzione $\delta_{x_{0}}[f]=f(x_{0})$.