---
aliases:
  - principio di indeterminazione
  - osservabili compatibili
  - osservabili incompatibili
---
La **disuguaglianza di Heisenberg**, o **principio di indeterminazione**, è una disuguaglianza che mostra come il prodotto tra l'errore sulla posizione $q$ e quello sulla quantità di moto $p$ di una [[particella]] quantistica ha un minimo costante. Ciò implica che le due quantità non possono essere determinate con precisione arbitraria allo stesso tempo e che misurare con precisione una rende la seconda molto imprecisa. Matematicamente, in una dimensione
$$\Delta q\Delta p\geq\frac{\hbar}{2}$$
e in tre dimensioni
$$\Delta x \Delta p_{x}\geq \frac{\hbar}{2}, \quad \Delta y \Delta p_{y}\geq \frac{\hbar}{2}, \quad \Delta z \Delta p_{z}\geq \frac{\hbar}{2}$$

L'errore qui definito non è quello della strumentazione, ma quello intrinseco dovuto alla [[Funzione d'onda]] della particella, dato che misure uguali su sistemi preparati allo stesso modo *non* danno lo stesso risultato. È una manifestazione dell'[[Indeterminatezza quantistica]].
## Forma generale
Consideriamo un'[[Osservabile]] $A$ e il suo [[operatore autoaggiunto]] $\hat{A}$ per una funzione d'onda $\Psi$. Allora la sua varianza è
$$\sigma_{A}^{2}=\langle (\hat{A}-\left\langle A \right\rangle)\Psi\;|\; (\hat{A}-\left\langle A \right\rangle)\Psi\rangle=\langle f|f\rangle$$
con $f=(\hat{A}-\left\langle A \right\rangle)\Psi$. Per un'altra osservabile $B$ si ha
$$\sigma_{B}^{2}=\langle g|g\rangle$$
con $g=(\hat{B}-\left\langle B \right\rangle)\Psi$. Usando la [[disuguaglianza di Schwarz-Hölder]] vale
$$\sigma_{A}^{2}\sigma_{B}^{2}=\langle f|f\rangle \langle g|g\rangle\geq |\langle f|g\rangle|^{2}\tag{1}$$
Per ogni numero complesso $z$ vale
$$|z|^{2}=|\text{Re}(z)^{2}|+|\text{Im}(z)|^{2}\geq |\text{Im}(z)|^{2}=\left[\frac{1}{2i}(z-z^{*})\right]^{2}\tag{2}$$
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
$$\boxed{\sigma_{A}^{2}\sigma_{B}^{2}\geq \left(\frac{1}{2i} \langle[\hat{A},\hat{B}]\rangle\right)^{2}}\tag{3}$$
Il commutatore di due operatori autoaggiunti ha valore di aspettazione immaginario, quindi la $i$ al denominatore si semplifica e il valore è reale e positivo, come ci si aspetta. Allora il principio di indeterminazione è un concetto più generale che si applica a *tutte le coppie di osservabili che hanno commutatore non nullo*. Queste coppie si dicono **osservabili incompatibili**. Se invece il commutatore è nullo, non si applica il principio di indeterminazione e si dicono **osservabili compatibili**. Osservabili compatibili ammettono un [[sistema completo]] di [[Equazione agli autovalori|autofunzioni]] condivise, mentre quelle incompatibili no.[^1]

Se decidiamo $A=q$ e $B=p$ si ha che il commutatore fra le due è $[\hat{q},\hat{p}]=i\hbar$ e quindi la $(3)$ diventa
$$\sigma_{p}^{2}\sigma_{q}^{2}\geq \frac{\hbar^{2}}{4}$$
che è il quadrato della disuguaglianza di Heisenberg.
### Minima incertezza
Si può cercare il caso generale in cui la disuguaglianza diventa un'uguaglianza e quindi l'incertezza è minima. Sappiamo che la disuguaglianza di Schwartz è saturata nel caso $f=cg$ con $g$ una costante complessa. Allora, cerchiamo quando la $(1)$ e la $(2)$ sono uguaglianze. Per la $(2)$, deve essere $\text{Re}(z)=0$. Ciò vale a dire $\text{Re}(\langle f|g\rangle)=\text{Re}(c \langle f|f\rangle)=0$. Dato che $\langle f|f\rangle$ è sempre reale, deve essere che $c$ è immaginaria, quindi $c=ia$, con $a$ una costante reale. Allora la condizione per avere minima incertezza è $g(x)=iaf(x)$.

Nel caso posizione-momento unidimensionale, vale
$$\left(\frac{\hbar}{i} \frac{d}{dx}- \left\langle p \right\rangle\right)\Psi=ia(x- \left\langle x \right\rangle)\Psi$$
che è un'equazione differenziale di $\Psi$ in $x$, la cui soluzione è
$$\Psi(x)=Ae^{-a(x-\left\langle x \right\rangle)^{2}/2\hbar}e^{i\left\langle p \right\rangle x/\hbar}$$
che è una gaussiana. Allora *il pacchetto d'onda di minima incertezza ha sempre una forma gaussiana*.
### Disuguaglianza tempo-energia
Dalla forma generale del principio di indeterminazione possiamo ottenere la legge per la coppia tempo-energia, che ha un significato fisico particolare. Allora partiamo cercando una misura di quanto in fretta un sistema stia cambiano calcolando la derivata temporale del valor medio di un'osservabile $Q(x,p,t)$:
$$\frac{d}{dt}\left\langle Q \right\rangle=\frac{d}{dt}\langle \Psi|\hat{Q}\Psi\rangle=\left\langle \frac{\partial \Psi}{\partial t}|\hat{Q}\Psi\right\rangle+\left\langle \Psi| \frac{\partial \left\langle Q \right\rangle}{\partial t}\Psi\right\rangle + \left\langle \Psi|\hat{Q}\frac{\partial \Psi}{\partial t}\right\rangle$$
L'[[Equazione di Schrödinger]] ha la forma
$$i\hbar \frac{\partial \Psi}{\partial t}=\hat{H}\Psi$$
dove l'[[Hamiltoniana]] è $H=p^{2}/2m+V$. Allora
$$\frac{d}{dt}\left\langle Q \right\rangle=- \frac{1}{i\hbar}\langle \hat{H}\Psi|\hat{Q}\Psi\rangle+ \frac{1}{i\hbar}\langle \Psi|\hat{Q}\hat{H}\Psi\rangle+\left\langle \frac{\partial \hat{Q}}{\partial t} \right\rangle$$
Ma $\hat{H}$ è autoaggiunto, quindi $\langle \hat{H}\Psi|\hat{Q}\Psi\rangle=\langle \Psi|\hat{H}\hat{Q}\Psi\rangle$ e allora
$$\boxed{\frac{d}{dt}\left\langle Q \right\rangle=\frac{i}{\hbar}\left\langle [\hat{H},\hat{Q}] \right\rangle+\left\langle \frac{\partial \hat{Q}}{\partial t} \right\rangle}$$
Nel caso comune[^2] di un operatore $\hat{Q}$ che non dipende dal tempo, $\partial \hat{Q}/\partial t=0$, quindi la derivata temporale di un'osservabile è direttamente proporzionale al suo commutatore con l'Hamiltoniana del sistema. In particolare, *se $Q$ commuta con $H$, allora $Q$ è una [[costante del moto]]*.

Ora consideriamo il principio d'incertezza. Se $Q$ non dipende dal tempo, abbiamo
$$\sigma_{H}^{2}\sigma_{Q}^{2}\geq\left(\frac{1}{2i}\langle[\hat{H},\hat{Q}]\rangle\right)^{2}=\left(\frac{1}{2i} \frac{\hbar}{i} \frac{d}{dt} \left\langle Q \right\rangle\right)^{2}=\left(\frac{\hbar}{2}\right)^{2}\left(\frac{d}{dt} \left\langle Q \right\rangle\right)^{2}$$
e prendendo la radice (dato che entrambi i membri sono garantiti positivi)
$$\sigma_{H}\sigma_{Q}\geq \frac{\hbar}{2} \left| \frac{d}{dt} \left\langle Q \right\rangle \right|$$
La deviazione sull'Hamiltoniana è l'errore sull'energia: $\sigma_{H}\equiv\Delta E$. Definiamo inoltre
$$\Delta t\equiv \frac{\sigma_{Q}}{|d \left\langle Q \right\rangle/dt|}$$
Allora con queste definizioni vale
$$\boxed{\Delta E \Delta t\geq \frac{\hbar}{2}}$$
che è il principio di indeterminazione tempo-energia. La cosa importante qui è il significato della variabile $\Delta t$. Invertendo la sua definizione si vede
$$\sigma_{Q}=\left| \frac{d}{dt}\left\langle Q \right\rangle\right|\Delta t$$
quindi $\Delta t$ rappresenta il lasso di tempo necessario per far si che $\left\langle Q \right\rangle$ cambi di una deviazione standard. Più generalmente, $\Delta t$ è il tempo necessario per causare un cambiamento "sostanziale" nel sistema. $\Delta t$ dipende da dipende dall'osservabile in esame, ma è *sempre* modulata da $\Delta E$: se l'energia è bassa, allora il tempo di cambiamento di *qualunque* variabile sarà lungo, mentre a energie alte il cambiamento avverrà in poco tempo. Vista al contrario, se una variabile cambia molto in poco tempo, l'energia sarà altamente incerta (ossia cambia molto).

Ma si può dire di più: grazie all'equivalenza massa-energia, l'errore sull'energia lo è anche sulla massa, quindi la *massa stessa* di un oggetto quantistico (ossia una particella) che cambia molto rapidamente (ossia ha un tempo di vita molto bassa) è necessariamente molto incerta. Questo è il motivo per cui particelle fondamentali con tempi di vita bassissimi hanno masse molto difficili da misurare con precisione, ergo le distribuzioni di misure di massa molto ampie negli esperimenti con acceleratori.

Questo risultato resiste anche al caso limite di uno stato stazionario, dove l'energia è [[Stato determinato|determinata]]. In questo, chiaramente deve essere $\Delta E =0$, ma allora $\Delta t \rightarrow \infty$. Ma $\Delta t \rightarrow \infty$ significa che le medie delle osservabili impiegano tempo infinito per variare, che è perfettamente sensato dato che in uno stato stazionario sono costanti. Per ottenere una variazione, bisogna combinare linearmente almeno due stati stazionari.

Questa trattazione dell'indeterminazione tempo-energia è detta **formulazione di Mandelstam-Tamm**.

---

Prendo $X=\{x_{i}\}^{d}_{i}$ un insieme di $d$ variabili casuali. Definisco una [[Distribuzione]] $F:X \rightarrow\mathbb{R}$, $x_{i} \rightarrow F(x_{i})$ che agisce sulle $X$. Dato che le $X$ sono determinate casualmente, non è esiste alcun "valore" di $X$. Al meglio, possiamo definire il valore di aspettazione o quantità simili. Ciò significa anche che non possiamo nemmeno determinare $F$, al di là di una media. Calcoliamo allora proprio questa, o meglio i *momenti* della distribuzione $F$ nello [[Stato]] $\pi$
$$\langle F\rangle_{\pi}=\sum\limits_{i=1}^{d}p_{i}F(x_{i})$$
$$\langle F^{2}\rangle_{\pi}=\sum\limits_{i=1}^{d}p_{i}F^{2}(x_{i})$$
$$\Delta_{\pi}F=\langle F^{2}\rangle_{\pi}-\langle F\rangle^{2}_{\pi}$$
In meccanica classica è possibile misurare qualunque cosa, almeno in linea di principio, con precisione arbitraria. In meccanica quantistica, invece, si trova che gli errori su $\hat{p}$ e $\hat{q}$ sono
$$\boxed{\Delta\hat{p}\Delta\hat{q}\geq\frac{\hbar}{2}}$$
che è la **disuguaglianza di Heisenberg**. Per una forma in funzione di due [[Osservabile|osservabili]], vedi [[Misure di osservabili]].
Dunque è impossibile misurare traiettorie per particelle quantistiche, in quanto servirebbe avere misure precise sia per $\hat{p}$ e $\hat{q}$.

Se prendiamo la distribuzione di Gibbs che descrive uno stato misto
$$\rho_{p}(q,p)=\frac{e^{-\beta H(q,p)}}{z_{\beta}}$$
abbiamo il valore di aspettazione
$$\langle F\rangle_{\rho_{\beta}}=\int_{\mathbb{R}^{2}}\rho_{\beta}(q,p)F(q,p)dqdp$$
Possiamo rappresentare un punto nello spazio delle fasi come la distribuzione *[[Delta di Dirac]]*
$$(q,p)\rightarrow\delta(q-q_{0}),\;\delta(p-p_{0})$$
Dunque posso pensare ad un punto come appartenere alla stessa "classe" delle distribuzioni nello [[spazio delle fasi]]. Allora abbiamo
$$\langle F\rangle_{\rho_{\beta}}=\int_{\mathbb{R}^{2}}\rho_{\beta}(q,p)F(q,p)dqdp=F(q_{0},p_{0})$$
Naturalmente la notazione di funzione della delta di Dirac $\delta(x-x_{0})$ è un'approssimazione comoda della notazione rigorosa da distribuzione $\delta_{x_{0}}[f]=f(x_{0})$.

[^1]: L'equivalente finito-dimensionale di questa affermazione è che due [[Matrice hermitiana|matrici autoaggiunte]] che non commutano fra loro ($\mathbf{A}\mathbf{B}\neq \mathbf{B}\mathbf{A}$) non possono essere [[diagonalizzazione|diagonalizzate]] simultaneamente dalla stessa trasformazione simile.
[^2]: Gli operatori che hanno una dipendenza esplicita dal tempo sono piuttosto rari. Un esempio sarebbe un oscillatore armonico la cui costante elastica dipende dal tempo, per qualche ragione.