---
aliases:
  - principio di indeterminazione
---
La **disuguaglianza di Heisenberg**, o **principio di indeterminazione**, è una disuguaglianza che mostra come il prodotto tra l'errore sulla posizione $q$ e quello sulla quantità di moto $p$ di una [[particella]] quantistica ha un minimo costante. Ciò implica che le due quantità non possono essere determinate con precisione arbitraria allo stesso tempo e che misurare con precisione una rende la seconda molto imprecisa. Matematicamente,
$$\Delta\hat{q}\Delta\hat{p}\geq\frac{\hbar}{2}$$
L'errore qui definito non è quello della strumentazione, ma quello intrinseco dovuto alla [[funzione d'onda]] della particella, dato che misure uguali su sistemi preparati allo stesso modo *non* danno lo stesso risultato. È una manifestazione dell'[[indeterminatezza quantistica]].
## Forma generale
Consideriamo un'[[osservabile]] $A$ e il suo [[operatore autoaggiunto]] $\hat{A}$ per una funzione d'onda $\Psi$. Allora la sua varianza è
$$\sigma_{A}^{2}=\langle (\hat{A}-\left\langle A \right\rangle)\Psi\;|\; (\hat{A}-\left\langle A \right\rangle)\Psi\rangle=\langle f|f\rangle$$
con $f=(\hat{A}-\left\langle A \right\rangle)\Psi$. Per un'altra osservabile $B$ si ha
$$\sigma_{B}^{2}=\langle g|g\rangle$$
con $g=(\hat{B}-\left\langle B \right\rangle)\Psi$. Usando la [[disuguaglianza di Schwarz-Hölder]] vale
$$\sigma_{A}^{2}\sigma_{B}^{2}=\langle f|f\rangle \langle g|g\rangle\geq |\langle f|g\rangle|^{2}$$
Per ogni numero complesso $z$ vale
$$|z|^{2}=|\text{Re}(z)^{2}|+|\text{Im}(z)|^{2}=\left[\frac{1}{2i}(z-z^{*})\right]^{2}$$
Dunque dato che $\langle f|g\rangle$ è un valore complesso $z$, si ha
$$\sigma_{A}^{2}\sigma_{B}^{2}=\left(\frac{1}{2i}[\langle f|g\rangle-\langle g|f\rangle]\right)^{2}$$
Compiendo esplicitamente i calcoli per $\langle f|g\rangle$ troviamo
$$\langle f|g\rangle=\langle (\hat{A}-\left\langle A \right\rangle)\Psi| (\hat{B}-\left\langle B \right\rangle)\Psi\rangle=\langle \Psi|(\hat{A}-\left\langle A \right\rangle)(\hat{B}-\left\langle B \right\rangle)\Psi\rangle=$$
$$=\langle \Psi|(\hat{A}\hat{B}-\hat{A}\left\langle B \right\rangle-\hat{B}\left\langle A \right\rangle+\left\langle A \right\rangle \left\langle B \right\rangle \Psi\rangle=$$
$$=\langle \Psi|\hat{A}\hat{B}\Psi\rangle-\left\langle B \right\rangle \langle \Psi|\hat{A}\Psi\rangle-\left\langle A \right\rangle \langle \Psi|\hat{B}\Psi\rangle+\left\langle A \right\rangle \left\langle B \right\rangle \langle \Psi|\Psi\rangle=$$
$$=\langle \hat{A}\hat{B} \rangle + \left\langle B \right\rangle \left\langle A \right\rangle - \left\langle A \right\rangle \left\langle B \right\rangle + \left\langle A \right\rangle \left\langle B \right\rangle= \langle \hat{A}\hat{B} \rangle - \left\langle A \right\rangle \left\langle B \right\rangle$$
usando la normalizzazione della funzione d'onda $\langle \Psi|\Psi\rangle=1$. Con lo stesso procedimento
$$\langle g|f\rangle=\langle \hat{B}\hat{A}\rangle - \left\langle A \right\rangle \left\langle B \right\rangle$$
quindi
$$\langle f|g\rangle-\langle g|f\rangle=\langle [\hat{A},\hat{B}] \rangle$$
che è il valor medio del [[commutatore]] delle due osservabili. Allora possiamo scrivere la disuguaglianza di Heisenberg come
$$\boxed{\sigma_{A}^{2}\sigma_{B}^{2}\geq \left(\frac{1}{2i} \langle[\hat{A},\hat{B}]\rangle\right)^{2}}\tag{1}$$
Il commutatore di due operatori autoaggiunti ha valore di aspettazione immaginario, quindi la $i$ al denominatore si semplifica e il valore è reale e positivo, come ci si aspetta. Allora il principio di indeterminazione è un concetto più generale che si applica a *tutte le coppie di osservabili che hanno commutatore non nullo*. Queste coppie si dicono **osservabili incompatibili**. Se invece il commutatore è nullo, non si applica il principio di indeterminazione e si dicono **osservabili compatibili**. Osservabili compatibili ammettono un [[sistema completo]] di [[Equazione agli autovalori|autofunzioni]] condivise, mentre quelle incompatibili no.[^1]

Se decidiamo $A=q$ e $B=p$ si ha che il commutatore fra le due è $[\hat{q},\hat{p}]=i\hbar$ e quindi la $(1)$ diventa
$$\sigma_{p}^{2}\sigma_{q}^{2}\geq \frac{\hbar^{2}}{4}$$
che è il quadrato della disuguaglianza di Heisenberg.
 
---

Prendo $X=\{x_{i}\}^{d}_{i}$ un insieme di $d$ variabili casuali. Definisco una [[distribuzione]] $F:X \rightarrow\mathbb{R}$, $x_{i} \rightarrow F(x_{i})$ che agisce sulle $X$. Dato che le $X$ sono determinate casualmente, non è esiste alcun "valore" di $X$. Al meglio, possiamo definire il valore di aspettazione o quantità simili. Ciò significa anche che non possiamo nemmeno determinare $F$, al di là di una media. Calcoliamo allora proprio questa, o meglio i *momenti* della distribuzione $F$ nello [[stato]] $\pi$
$$\langle F\rangle_{\pi}=\sum\limits_{i=1}^{d}p_{i}F(x_{i})$$
$$\langle F^{2}\rangle_{\pi}=\sum\limits_{i=1}^{d}p_{i}F^{2}(x_{i})$$
$$\Delta_{\pi}F=\langle F^{2}\rangle_{\Psi}-\langle F\rangle^{2}_{\pi}$$
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

[^1]: L'equivalente finito-dimensionale di questa affermazione è che due [[Matrice hermitiana|matrici autoaggiunte]] che non commutano fra loro ($\mathbf{A}\mathbf{B}\neq \mathbf{B}\mathbf{A}$) non possono essere [[diagonalizzazione|diagonalizzate]] simultaneamente dalla stessa trasformazione simile.