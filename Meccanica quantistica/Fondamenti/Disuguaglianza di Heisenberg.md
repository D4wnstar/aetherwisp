---
wiki-publish: true
aliases:
  - principio di indeterminazione
  - osservabili compatibili
  - osservabili incompatibili
---
La **disuguaglianza di Heisenberg**, o **principio di indeterminazione**, è una disuguaglianza che mostra come il prodotto tra l'errore sulla posizione $q$ e quello sulla quantità di moto $p$ di una [[Particle]] quantistica ha un minimo costante. Ciò implica che le due quantità non possono essere determinate con precisione arbitraria allo stesso tempo e che misurare con precisione una rende la seconda molto imprecisa. Matematicamente, in una dimensione
$$\Delta q\Delta p\geq\frac{\hbar}{2}$$
e in tre dimensioni
$$\Delta x \Delta p_{x}\geq \frac{\hbar}{2}, \quad \Delta y \Delta p_{y}\geq \frac{\hbar}{2}, \quad \Delta z \Delta p_{z}\geq \frac{\hbar}{2}$$
mentre in coordinate diverse non c'è una particolare relazione (ad esempio, $\Delta x \Delta p_{y}\geq0$).

L'errore qui definito non è quello della strumentazione, ma quello intrinseco dovuto alla [[funzione d'onda]] della particella, dato che misure uguali su sistemi preparati allo stesso modo *non* danno lo stesso risultato. È una manifestazione dell'[[indeterminatezza quantistica]].
## Forma generale
Consideriamo un'[[osservabile]] $A$ e il suo [[operatore autoaggiunto]] $\hat{A}$ per una funzione d'onda $\psi$. Allora la sua [[Variance|varianza]] è
$$\sigma_{A}^{2}=\langle (\hat{A}-\left\langle A \right\rangle)\psi\;|\; (\hat{A}-\left\langle A \right\rangle)\psi\rangle=\langle f|f\rangle$$
con $f=(\hat{A}-\left\langle A \right\rangle)\psi$ e $\langle \cdot \rangle=\bra{\psi}\cdot \ket{\psi}$ la media nello stato $\psi$. Per un'altra osservabile $B$ si ha
$$\sigma_{B}^{2}=\langle g|g\rangle$$
con $g=(\hat{B}-\left\langle B \right\rangle)\psi$. Usando la [[Disuguaglianza di Cauchy-Schwarz]] vale
$$\sigma_{A}^{2}\sigma_{B}^{2}=\langle f|f\rangle \langle g|g\rangle\geq |\langle f|g\rangle|^{2}\tag{1}$$
Per ogni numero complesso $z$ vale
$$|z|^{2}=|\text{Re}(z)^{2}|+|\text{Im}(z)|^{2}\geq |\text{Im}(z)|^{2}=\left[\frac{1}{2i}(z-z^{*})\right]^{2}\tag{2}$$
Dunque dato che $\langle f|g\rangle$ è un valore complesso $z$, si ha
$$\sigma_{A}^{2}\sigma_{B}^{2}=\left(\frac{1}{2i}[\langle f|g\rangle-\langle g|f\rangle]\right)^{2}$$
Compiendo esplicitamente i calcoli per $\langle f|g\rangle$ troviamo
$$\langle f|g\rangle=\langle (\hat{A}-\left\langle A \right\rangle)\psi| (\hat{B}-\left\langle B \right\rangle)\psi\rangle=\langle \psi|(\hat{A}-\left\langle A \right\rangle)(\hat{B}-\left\langle B \right\rangle)\psi\rangle=$$
$$=\langle \psi|(\hat{A}\hat{B}-\hat{A}\left\langle B \right\rangle-\hat{B}\left\langle A \right\rangle+\left\langle A \right\rangle \left\langle B \right\rangle \psi\rangle=$$
$$=\langle \psi|\hat{A}\hat{B}\psi\rangle-\left\langle B \right\rangle \langle \psi|\hat{A}\psi\rangle-\left\langle A \right\rangle \langle \psi|\hat{B}\psi\rangle+\left\langle A \right\rangle \left\langle B \right\rangle \langle \psi|\psi\rangle=$$
$$=\langle \hat{A}\hat{B} \rangle + \left\langle B \right\rangle \left\langle A \right\rangle - \left\langle A \right\rangle \left\langle B \right\rangle + \left\langle A \right\rangle \left\langle B \right\rangle= \langle \hat{A}\hat{B} \rangle - \left\langle A \right\rangle \left\langle B \right\rangle$$
usando la normalizzazione della funzione d'onda $\langle \psi|\psi\rangle=1$. Con lo stesso procedimento
$$\langle g|f\rangle=\langle \hat{B}\hat{A}\rangle - \left\langle A \right\rangle \left\langle B \right\rangle$$
quindi
$$\langle f|g\rangle-\langle g|f\rangle=\langle [\hat{A},\hat{B}] \rangle$$
che è il valor medio del [[Commutator]] delle due osservabili. Allora, scrivendo la media in forma estesa e notando $(1/2i)^{2}=-1/4$, possiamo scrivere la disuguaglianza di Heisenberg in uno stato $\psi$ come
$$\boxed{\sigma_{A}^{2}\sigma_{B}^{2}\geq -\frac{1}{4} \left(\bra{\psi} [\hat{A},\hat{B}]\ket{\psi} \right)^{2}}\tag{3}$$
Il commutatore di due operatori autoaggiunti ha valore di aspettazione immaginario, quindi la $i$ al denominatore si semplifica e il valore è reale e positivo, come ci si aspetta. Allora il principio di indeterminazione è un concetto più generale che si applica a *tutte le coppie di osservabili che hanno commutatore non nullo*. Queste coppie si dicono **osservabili incompatibili**. Se invece il commutatore è nullo, non si applica il principio di indeterminazione e si dicono **osservabili compatibili**. Osservabili compatibili ammettono un [[Sistema completo]] di [[Equazione agli autovalori|autofunzioni]] condivise, mentre quelle incompatibili no.[^1]

Se decidiamo $A=q$ e $B=p$ si ha che il commutatore fra le due è $[\hat{q},\hat{p}]=i\hbar$ e quindi la $(3)$ diventa
$$\sigma_{p}^{2}\sigma_{q}^{2}\geq \frac{\hbar^{2}}{4}$$
che è il quadrato della disuguaglianza di Heisenberg.
### Minima incertezza
Si può cercare il caso generale in cui la disuguaglianza diventa un'uguaglianza e quindi l'incertezza è minima. Sappiamo che la disuguaglianza di Cauchy-Schwarz è saturata nel caso $f=cg$ con $g$ una costante complessa. Allora, cerchiamo quando la $(1)$ e la $(2)$ sono uguaglianze. Per la $(2)$, deve essere $\text{Re}(z)=0$. Ciò vale a dire $\text{Re}(\langle f|g\rangle)=\text{Re}(c \langle f|f\rangle)=0$. Dato che $\langle f|f\rangle$ è sempre reale, deve essere che $c$ è immaginaria, quindi $c=i\mu$, con $\mu$ una costante reale. Allora la condizione per avere minima incertezza è $g(x)=i\mu f(x)$. In forma estesa, vale a dire
$$\lvert \braket{ (\hat{A}-\langle A \rangle )\psi | (\hat{B}-\langle B \rangle )\psi }  \rvert ^{2}=||(\hat{A}-\langle A \rangle \psi)||^{2}\,||(\hat{B}-\langle B \rangle )\psi||^{2}$$
da cui
$$\boxed{(\hat{B}-\langle B \rangle )\ket{\psi} =i\mu(\hat{A}-\langle A \rangle )\ket{\psi} }\tag{4}$$
con $\mu \in \mathbb{R}$.

Nel caso posizione-momento unidimensionale, vale
$$\left(\hat{p} - \left\langle \hat{p} \right\rangle\right)\ket{\psi} =i\mu(\hat{q}- \left\langle \hat{q} \right\rangle)\ket{\psi} $$
che è un'equazione differenziale di $\psi$ in $q$, la cui soluzione rispetto alla posizione è
$$\boxed{\psi(x)=Ae^{-\mu(x-\left\langle x \right\rangle)^{2}/2\hbar}e^{i\left\langle p \right\rangle x/\hbar}}$$
che è una gaussiana. Allora *il pacchetto d'onda di minima incertezza ha sempre una forma Gaussiana*.

In [[Rappresentazioni dello stato|rappresentazione della posizione]] (cioè proiettando su $\bra{x}$), i calcoli completi sono
$$\braket{ x | \hat{p}\psi } -\langle \hat{p} \rangle _{\psi}\braket{ x | \psi } =i\mu \braket{ x | \hat{q}\psi } -i\mu \langle \hat{q} \rangle _{\psi}\braket{ x | \psi } $$
$$-i\hbar \partial_{x} \psi(x)-\langle \hat{p} \rangle _{\psi}\psi(x)=i\mu x\psi(x)-i\mu \langle \hat{q} \rangle _{\psi}\psi(x)$$
$$\psi'(x)=\partial_{x} \psi(x)=\frac{i}{\hbar}\langle \hat{p} \rangle _{\psi}\psi(x)- \frac{\mu}{\hbar}x\psi(x)+ \frac{\mu}{\hbar}\langle \hat{q} \rangle _{\psi}\psi(x)$$
$$\frac{d}{dx}\log \psi(x)=\frac{\psi'(x)}{\psi(x)}=\frac{i}{\hbar}\langle \hat{p} \rangle _{\psi}- \frac{\mu}{\hbar}x+ \frac{\mu}{\hbar}\langle \hat{q} \rangle _{\psi}$$
$$\log \psi(x)+A=\frac{i}{\hbar}\langle \hat{p} \rangle _{\psi}x- \frac{\mu}{2\hbar}x^{2}+ \frac{\mu}{\hbar}x\langle \hat{q} \rangle _{\psi}$$
$$\psi(x)=ce^{- \mu x^{2}/2\hbar}e^{i\langle \hat{p} \rangle _{\psi}x/\hbar}e^{\mu x\langle \hat{q} \rangle _{\psi}/\hbar}$$
che possiamo riscrivere come
$$\psi(x)=\tilde{c}e^{-\mu(x-\langle \hat{q} \rangle _{\psi})^{2}/2\hbar}e^{i\langle \hat{p} \rangle _{\psi}x/\hbar}$$
che è una forma Gaussiana.

In [[Rappresentazioni dello stato|rappresentazione del momento]], i calcoli sono simili, ma si proietta su $\bra{p}$:
$$\braket{ p | \hat{p}\psi } -\langle \hat{p} \rangle _{\psi}\braket{ p | \psi } =i\mu \braket{ p | \hat{q}\psi } -i\mu \langle \hat{q} \rangle _{\psi}\braket{ p | \psi } $$
$$p\psi(p)-\langle \hat{p} \rangle _{\psi}\psi(p)=i\mu \braket{ p | \hat{q}\psi } -i\mu \langle \hat{q} \rangle _{\psi}\psi(p)$$
Bisogna risolvere $\braket{ p | \hat{q}\psi }$. Possiamo sfruttare la [[Proiettore|relazione di completezza]]:
$$\begin{align}
\braket{ p | \hat{q}\psi } &=\bra{p}\left( \int_{-\infty}^{\infty} \ket{x} \bra{x}  \ dx  \right)\ket{\hat{q}\psi}  =\int_{-\infty}^{\infty} \braket{ p | x } \braket{ x | \hat{q}\psi }  \ dx =\int_{-\infty}^{\infty} \frac{e^{-ipx/\hbar}}{\sqrt{ 2\pi \hbar }}x\psi(x) \ dx = \\
&=\int_{-\infty}^{\infty} (i\hbar \partial_{p}) \left( \frac{e^{-ipx/\hbar}}{\sqrt{ 2\pi \hbar }} \right)\psi(x) \ dx =i\hbar \partial_{p} \underbrace{ \left( \int_{-\infty}^{\infty} \frac{e^{-ipx/\hbar}}{\sqrt{ 2\pi \hbar }}\psi(x) \ dx  \right) }_{ \psi(p) }=i\hbar \partial_{p}\psi(p)
\end{align}$$
Quindi sostituendo questo nell'equazione precedente troviamo
$$p\psi(p)-\langle \hat{p} \rangle _{\psi}\psi(p)=-\mu \hbar \partial_{p}\psi(p)-i\mu \langle \hat{p} \rangle _{\psi}$$
Questa si può risolvere allo stesso modo della posizione. Le due funzioni $\psi(p)$ e $\psi(x)$ sono come al solito legate dalla [[Trasformata di Fourier]] come $\mathcal{F}[\psi(p)]=\psi(x)$.
### Disuguaglianza tempo-energia
Dalla forma generale del principio di indeterminazione possiamo ottenere la legge per la coppia tempo-energia, che ha un significato fisico particolare. Allora partiamo cercando una misura di quanto in fretta un sistema stia cambiano calcolando la derivata temporale del valor medio di un'osservabile $Q(x,p,t)$:
$$\frac{d}{dt}\left\langle Q \right\rangle=\frac{d}{dt}\langle \psi|\hat{Q}\psi\rangle=\left\langle \frac{\partial \psi}{\partial t}|\hat{Q}\psi\right\rangle+\left\langle \psi| \frac{\partial \left\langle Q \right\rangle}{\partial t}\psi\right\rangle + \left\langle \psi|\hat{Q}\frac{\partial \psi}{\partial t}\right\rangle$$
L'[[Equazione di Schrödinger]] ha la forma
$$i\hbar \frac{\partial \psi}{\partial t}=\hat{H}\psi$$
dove l'[[Hamiltonian]] è $H=p^{2}/2m+V$. Allora
$$\frac{d}{dt}\left\langle Q \right\rangle=- \frac{1}{i\hbar}\langle \hat{H}\psi|\hat{Q}\psi\rangle+ \frac{1}{i\hbar}\langle \psi|\hat{Q}\hat{H}\psi\rangle+\left\langle \frac{\partial \hat{Q}}{\partial t} \right\rangle$$
Ma $\hat{H}$ è autoaggiunto, quindi $\langle \hat{H}\psi|\hat{Q}\psi\rangle=\langle \psi|\hat{H}\hat{Q}\psi\rangle$ e allora
$$\boxed{\frac{d}{dt}\left\langle Q \right\rangle=\frac{i}{\hbar}\left\langle [\hat{H},\hat{Q}] \right\rangle+\left\langle \frac{\partial \hat{Q}}{\partial t} \right\rangle}$$
Questa equazione, detta [[equazione di Heisenberg]], forma la base della [[Rappresentazioni della meccanica quantistica|rappresentazione di Heisenberg]], dove l'evoluzione temporale è data agli operatori.

Nel caso comune[^2] di un operatore $\hat{Q}$ che non dipende dal tempo, $\partial \hat{Q}/\partial t=0$, quindi la derivata temporale di un'osservabile è direttamente proporzionale al suo commutatore con l'Hamiltoniana del sistema.

> [!success] Commutazione = costante del moto
> Se un'osservabile $\hat{Q}$ commuta con $\hat{H}$, ossia $[\hat{Q},\hat{H}]=0$, allora $Q$ è una [[constant of motion|costante del moto]].

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

Ma si può dire di più: grazie all'equivalenza massa-energia, l'errore sull'energia lo è anche sulla massa, quindi la *massa stessa* di un oggetto quantistico (ossia una particella) che cambia molto rapidamente (ossia ha un tempo di vita molto bassa) è necessariamente molto incerta. Questo è il motivo per cui particelle elementari con tempi di vita bassissimi hanno masse molto difficili da misurare con precisione, ergo le distribuzioni di misure di massa molto ampie negli esperimenti con acceleratori.

Questo risultato resiste anche al caso limite di uno stato stazionario, dove l'energia è [[Stato determinato|determinata]]. In questo, chiaramente deve essere $\Delta E =0$, ma allora $\Delta t \rightarrow \infty$. Ma $\Delta t \rightarrow \infty$ significa che le medie delle osservabili impiegano tempo infinito per variare, che è perfettamente sensato dato che in uno stato stazionario sono costanti. Per ottenere una variazione, bisogna combinare linearmente almeno due stati stazionari.

Questa trattazione dell'indeterminazione tempo-energia è detta **formulazione di Mandelstam-Tamm**.

[^1]: L'equivalente finito-dimensionale di questa affermazione è che due [[Matrice hermitiana|matrici autoaggiunte]] che non commutano fra loro ($\mathbf{A}\mathbf{B}\neq \mathbf{B}\mathbf{A}$) non possono essere [[Diagonalization|diagonalizzate]] simultaneamente dalla stessa trasformazione simile.
[^2]: Gli operatori che hanno una dipendenza esplicita dal tempo sono piuttosto rari. Un esempio sarebbe un oscillatore armonico la cui costante elastica dipende dal tempo, per qualche ragione.