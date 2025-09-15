---
wiki-publish: true
aliases:
  - particella libera
---
La **particella libera** è un sistema quantistico costituito da una singola [[Particle]] in assenza di [[Potential]], ovvero $V(x)=0$ ovunque. Nel caso classico, questo sistema è banale e ha soluzioni immediate, dato che la particella compie un semplice moto rettilineo a velocità costante, ma nel caso quantistico compaiono problemi non trascurabili e diventa più complesso dell'[[Oscillatore armonico quantistico]].
### Soluzione
Partiamo come al solito dall'[[Equazione di Schrödinger#Potenziale indipendente dal tempo|equazione di Schrödinger indipendente dal tempo]]
$$- \frac{\hbar^{2}}{2m} \frac{d^{2}\psi}{dx^{2}}=E\psi$$
che ha potenziale nullo. Come per la [[Buca infinita quantistica|buca infinita]], scriviamola in una forma più compatta
$$\frac{d^{2}\psi}{dx^{2}}=-k^{2}\psi,\quad\text{con }k\equiv \frac{\sqrt{2mE}}{\hbar}$$
Ma questo non è altro che un [[Harmonic oscillator]] classico, la cui soluzione generale è
$$\psi(x)=Ae^{ikx}+Be^{-ikx}$$
qui scritta in forma esponenziale complessa.

A differenza della buca infinita, non ci sono condizioni al contorno a limitare le energie che la particella può ottenere, a patto che siano positive. Aggiungendo la dipendenza temporale standard, la soluzione tempo-dipendente diventa
$$\Psi(x,t)=Ae^{ik[x- (\hbar k/2m)t]}+Be^{-ik[x+ (\hbar k/2m)t]}$$
Ciò significa che *ogni* funzione di $x$ e $t$ dipendente da queste variabili nella forma $x\pm vt$ con $v=\hbar k/2m$ costante, rappresenta un'onda di profilo costante che viaggia nella direzione $\mp x$ a velocità $v$. Un punto fisso sulla forma d'onda è associato ad un valore fisso di $x\pm vt$, cioè $x=\mp vt+C$ con $C$ una costante (di fase). Con profilo costante s'intende che, dato che ogni punto dell'onda si muove alla stessa velocità, la *forma* dell'onda non cambia nella propagazione. Così, il termine $Ae^{ikx}$ rappresenta un'onda che si propaga verso $+x$ e $Be^{-ikx}$ un'onda che si propaga verso $-x$, come si trova nel caso classico delle onde. Possiamo semplificare la forma combinando i due termini, dato che differiscono solo per un segno all'esponente
$$\Psi_{k}(x,t)=Ae^{i[kx- (\hbar k^{2}/2m)t]}$$
Se lasciamo che $k$ sia anche negativo, questa equazione è equivalente alla precedente. Allora, si ha
$$k\equiv \pm \frac{\sqrt{2mE}}{\hbar}$$
Se $k>0$, l'onda va a $+x$ e se $k<0$, l'onda va a $-x$.

Ricordiamo però che queste *non* sono onde a priori, ma sono gli *stati stazionari* di una particella libera. Evidentemente, questi stati sono onde progressive con lunghezza d'onda pari a $\lambda=2\pi/|k|$ e hanno una quantità di moto associata $p=\hbar k$[^1]. Dunque la velocità dell'onda non può che essere
$$v_{\text{quantistica}}=\frac{\hbar|k|}{2m}=\sqrt{\frac{E}{2m}}$$
dividendo il coefficiente di $x$ ($k$) per il coefficiente di $t$ ($\hbar k^{2}/2m$). D'altro canto, la velocità di una particella *classica* di energia $E$ (che è solo cinetica dato che il potenziale è nullo per costruzione) è data da $E=(1/2)mv^{2}$, cioè
$$v_{\text{classica}}=\sqrt{\frac{2E}{m}}=2v_{\text{quantistica}}$$
Allora la particella quantistica viaggia a metà della particella classica? Non ha senso, dato che rappresentano la stessa cosa. Una delle due deve essere sbagliata. Ma c'è un altro problema: $\Psi(x,t)$ *non è normalizzabile* o, in altre parole, *non ha senso fisico*. Infatti
$$\int_{-\infty}^{+\infty}\Psi_{k}^{*}\Psi_{k}dx=|A|^{2}\int_{-\infty}^{+\infty}dx=|A|^{2}\cdot \infty$$
Cosa implica tutto questo?

> [!success] Risultato
> Una particella libera non può esistere in uno stato stazionario. Detta in altri termini, non esistono particelle libere con un'energia ben definita.

Dunque, le soluzioni separabili di cui sopra non hanno alcun significato fisico, ma ne hanno uno matematico. Di fatto, la soluzione generale non è più una *somma* su degli stati *numerabili* determinati dall'indice $n$, bensì un *integrale* su infiniti stati *non numerabili* determinati dalla variabile continua $k$. La [[Funzione d'onda]] definitiva, allora, è
$$\boxed{\Psi(x,t)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^{+\infty}\phi(k)e^{ik[x-(\hbar k^{2}/2m)t]}dk}$$
In questa forma, $\phi(k)/\sqrt{2\pi}$ prende il ruolo dei coefficienti $c_{n}$ della forma discreta. Questa funzione d'onda può essere normalizzata per appropriati $\phi(k)$ e quindi ha significato fisico. Ciascun $\phi(k)$ però porta necessariamente con sé un intervallo di $k$, non un singolo $k$, e quindi un intervallo di energie e velocità. Questo si chiama *pacchetto d'onda*.

A tempo zero, la funzione d'onda iniziale ha la forma
$$\Psi(x,0)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^{+\infty}\phi(k)e^{ixk}dk=F[\phi(k)](x)$$
Ma questa non è altro che la [[Trasformata di Fourier]] dal dominio delle frequenze spaziali $k$ a quello delle posizioni $x$. Per estrarre $\phi(k)$, basta applicare l'antitrasformata:
$$\boxed{\phi(k)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^{+\infty}\Psi(x,0)e^{-ikx}dx=F^{-1}[\Psi(x,0)](k)}$$
È giusto menzionare che gli integrali per $\phi(k)$ e soprattutto per $\Psi(x,t)$ sono raramente risolvibili analiticamente.
#### Paradosso della velocità
Nella ricerca della funzione d'onda per la particella libera, ci si è imbattuti in un paradosso: la velocità data dalla teoria classica è il doppio di quella data dalla teoria quantistica, anche se rappresentano la stessa identica particella. Il problema di fatto non sussiste, dato che la soluzione che porta a questo problema non ha significato fisico, ma è comunque interessante studiare il perché di questo paradosso.

Definiamo a grandi linee un pacchetto d'onda: un pacchetto d'onda è una sovrapposizione di funzioni sinusoidali modulate dalla funzione $\phi(k)$. Si tratta di un'onda contenuta in un battimento e come in tutti questi casi, si hanno due tipi di velocità, non una: la **velocità di fase** è la velocità che ha un punto sull'onda, mentre la **velocità di gruppo** è la velocità del battimento. Queste possono, ma non devono, essere uguali.

Ciò che importa è che per un'onda quantistica, la velocità di gruppo è il doppio della velocità di fase. Ciò riconcilia le due teorie, ma va dimostrato. La [[relazione di dispersione]] dell'onda della particella libera è $\omega(k)=\hbar k^{2}/2m$. Assumiamo che $\phi(k)$ abbia un picco piuttosto localizzato attorno ad un $k_{0}$[^2]. Allora, possiamo espandere in [[Taylor series|serie di Taylor]] la $\omega(k)$ attorno a $k_{0}$ senza grandi errori:
$$\omega(k)\simeq \omega(k_{0})+ \frac{d\omega}{dk}(k_{0})(k-k_{0})\equiv \omega_{0}+\omega_{0}'(k-k_{0})$$
Compiendo il cambio di variabile $s\equiv k-k_{0}$, l'integrale della funzione d'onda diventa
$$\Psi(x,t)\simeq \frac{1}{\sqrt{2\pi}}\int_{-\infty}^{+\infty}\phi(k_{0}+s)e^{i[(k_{0}+s)x-(\omega_{0}+\omega_{0}'s)t]}ds$$
e a $t=0$
$$\Psi(x,0)\simeq \frac{1}{\sqrt{2\pi}}\int_{-\infty}^{+\infty}\phi(k_{0}+s)e^{i(k_{0}+s)x}ds$$
e a tempi successivi
$$\Psi(x,t)\simeq \frac{1}{\sqrt{2\pi}}e^{i(-\omega_{0}t+k_{0}\omega_{0}'t)}\int_{-\infty}^{+\infty}\phi(k_{0}+s)e^{i(k_{0}+s)(x-\omega_{0}'t)}ds$$
L'unica differenza che c'è con l'integrale per $\Psi(x,0)$ è la traslazione da $x$ a $x-\omega_{0}'t$. Dunque, possiamo scrivere
$$\Psi(x,t)\simeq \Psi(x-\omega_{0}'t,0)e^{-i(\omega_{0}-k_{0}\omega_{0}')t}$$
Al di là della fase $e^{-i(\omega_{0}-k_{0}\omega_{0}')t}$, il pacchetto d'onda si muove a velocità
$$v_{\text{gruppo}}=\frac{d\omega}{dk}$$
in $k=k_{0}$. La velocità di fase è invece
$$v_{\text{fase}}=\frac{\omega}{k}$$
Nel nostro caso, valgono
$$v_{\text{fase}}=\frac{\omega}{k}=\frac{\hbar k}{2m},\quad v_{\text{gruppo}}=\frac{d\omega}{dk}=\frac{\hbar k}{m}=2v_{\text{fase}}$$
che il paradosso: la teoria classica ci dà la velocità di gruppo dell'onda quantistica, non la velocità degli stati stazionari.
### Soluzione nel tempo
L'[[Hamiltonian]] di un particella libera è
$$\hat{H}=\frac{\hat{p}^{2}}{2m}$$
Usiamo l'equazione di Schrödinger generale
$$i\hbar \partial_{t} \ket{\psi_{t}} =\hat{H}\ket{\psi_{t}}$$
Usiamo la [[Rappresentazioni dello stato|rappresentazione della posizione]], nella quale sappiamo che forma ha l'operatore $\hat{p}=-i\hbar \partial_{x}$:
$$i\hbar \partial_{t} \psi _{t}(x)=- \frac{\hbar^{2}}{2m}\partial_{x} ^{2}\psi_{t}(x)$$
Questa è un'equazione differenziale parziale sia in tempo che in posizione. La derivata in tempo è qui per definizione dell'equazione di Schrödinger, ma la derivata in posizione è arrivata dalla scelta di usare la rappresentazione in posizione. Se usassimo la rappresentazione in momento? In quel caso, avremmo
$$\braket{ p | (i\hbar \partial_{t} \psi_{t}) } =i\hbar \partial_{t} \psi_{t}(p)=\braket{ p | \frac{\hat{p}^{2}}{2m}\psi_{t} }=\frac{p^{2}}{2m}\psi_{t}(p) $$
dove la terza uguaglianza è derivata dall'equazione di Schrödinger e la quarta sviluppando la terza dato che $\hat{p}$ è [[Operatore autoaggiunto|hermitiano]] e vale
$$\braket{ p | \frac{\hat{p}^{2}}{2m}\psi_{t} } =\frac{1}{2m}\braket{ \hat{p}^{2}p | \psi_{t} } =\frac{p^{2}}{2m}\braket{ p | \psi _{t} } =\frac{p^{2}}{2m}\psi_{t}(p)$$
dato che $\hat{p}\ket{p}=p\ket{p}$. Ma quindi ora abbiamo
$$i\hbar \partial_{t} \psi_{t}(p)=\frac{p^{2}}{2m}\psi_{t}(p)$$
che è un'equazione differenziale di gran lunga più semplice. La soluzione è un esponenziale.
$$\psi_{t}(p)=e^{-(i/\hbar)(p^{2}/2m)t}\psi(p)$$
Per gli scopi fisici però abbiamo più bisogno della soluzione nelle posizioni. Per convertire basta sfruttare la [[Proiettore|relazione di completezza]]:
$$\psi_{t}(x)=\braket{ x | \psi_{t} } =\bra{x} \int_{-\infty}^{\infty} \ket{p} \bra{p}  \ dp \ket{\psi_{t}} =\int_{-\infty}^{\infty} \braket{ x | p } \braket{ p | \psi_{t} }  \ dp=  $$
$$=\int_{-\infty}^{\infty} \frac{e^{ipx/\hbar}}{\sqrt{ 2\pi \hbar }} e^{-(i/\hbar)(p^{2}/2m)t}\psi(p) \ dp$$
che è un'[[Trasformata di Fourier|antitrasformata di Fourier]]. Purtroppo lo stato iniziale $\psi(p)$ noi lo conosciamo in posizione come $\psi(x)$, quindi dovremmo compiere un'altra antitrasformata per convertirla (o usare la completezza di nuovo):
$$\psi(p)=\braket{ p | \psi } =\int_{-\infty}^{\infty} \braket{ p | y } \braket{ y | \psi }  \ dy=\frac{1}{\sqrt{ 2\pi \hbar }} \int_{-\infty}^{\infty} e^{-ipy/\hbar}\psi(y) \ dy $$
Ora che abbiamo convertito tutto, il problema sta nel risolvere gli integrali in sé.
$$\begin{align}
\psi_{t}(x)&=\int_{-\infty}^{\infty} \frac{e^{ipx/\hbar}}{\sqrt{ 2\pi \hbar }} e^{-(i/\hbar)(p^{2}/2m)t}\left(\frac{1}{\sqrt{ 2\pi \hbar }} \int_{-\infty}^{\infty} e^{-ipy/\hbar}\psi(y) \ dy\right) \ dp \\
&=\frac{1}{ 2\pi \hbar }\int_{-\infty}^{\infty}\int_{-\infty}^{\infty} e^{(i/\hbar)p(x-y)-(i/\hbar)(p^{2}/2m)t}\ \psi(y) \ dy \ dp
\end{align}$$
Quello che possiamo fare è raggruppare gli integrali in questo modo
$$\begin{align}
\psi_{t}(x)=\int_{-\infty}^{\infty} \left( \int_{-\infty}^{\infty} \frac{e^{ip(x-y)/\hbar-(i/\hbar)(p^{2}/2m)t}}{2\pi \hbar} \ dp  \right)\psi(y) \ dy 
\end{align}$$
L'integrale centrale è la rappresentazione dell'evolutore libero in una dimensione, che prende i contributi dello stato iniziale noto $\psi(y)$ e li porta al tempo $t$ alla posizione $x$. Si tratta di una [[Green's function|funzione di Green]]. Infatti, si può dimostrare che questo integrale non è altro che $\bra{x}\hat{U}_{t}\ket{y}$, con $\hat{U}_{t}$ l'[[evolutore]].

> [!example] Dimostrazione
> $$\begin{align}
> \psi_{t}(x)&=\braket{ x | \psi_{t} } =\braket{ x | \hat{U}_{t}\psi } =\bra{x} \left( \int_{-\infty}^{\infty} \ket{y} \bra{y}  \ dy \right)\ \ket{\hat{U}_{t}\psi}=\int_{-\infty}^{\infty} \braket{ x | y } \braket{ y | \hat{U}_{t}\psi }  \ dy  \\
> &=\int_{-\infty}^{\infty} \braket{ x | y }\ \hat{U}_{t}\psi(y) \ dy =\int_{-\infty}^{\infty} \bra{x} \hat{U}_{t}\ket{y}\ \psi(y) \ dy
> \end{align}$$
> usando la relazione di completezza e
> $$\psi_{t}(y)=\hat{U}_{t}\psi(y),\qquad\psi_{t}(y)=\braket{ y | \psi_{t} } =\braket{ y | \hat{U}_{t}\psi } \quad\Rightarrow \quad\braket{ y | \hat{U}_{t}\psi } =\hat{U}_{t}\psi(y) $$
> e
> $$\hat{U}_{t}\braket{ x | y } =\bra{x} \hat{U}_{t}\ket{y} \quad\text{(unitarietà?)}$$

Ci rimane quindi
$$\psi_{t}(x)=\int_{-\infty}^{\infty} \bra{x}\hat{U}_{t}\ket{y} \psi(y) \ dy $$
$\bra{x}\hat{U}_{t}\ket{y}$ è abbastanza importante da avere un nome tutto suo: [[propagatore]]. Chiaramente la forma astratta ci è utile a livello teorico, ma qui vogliamo trovare la forma specifica alla particella libera. Dobbiamo quindi calcolare l'integrale. Possiamo completare il quadrato all'esponente:
$$\int_{-\infty}^{\infty} \frac{e^{ip(x-y)/\hbar-(i/\hbar)(p^{2}/2m)t}}{2\pi \hbar} \ dp=\frac{1}{2\pi \hbar}\int_{-\infty}^{\infty} e^{-(i/t\hbar)(t/m)p^{2}-2p(m/t)(x-y)+ (m^{2}/p^{2})(x-y)^{2}} \ dp= $$
$$=\frac{1}{2\pi \hbar}\int_{-\infty}^{\infty} e^{(it/\hbar) (1/2m)(m^{2}/p^{2})(x-y)^{2}} \ dp =\frac{e^{(im/2\hbar)t(x-y)}}{2\pi \hbar}\int_{-\infty}^{\infty} e^{-(it/2m\hbar)\underbrace{ (p-m(x-y)/t)^{2} }_{ =u }} \ dp =$$
$$=\frac{e^{(im/2\hbar)t(x-y)}}{2\pi \hbar}\int_{-\infty}^{\infty} e^{-(it/2m\hbar)u^{2}} \ du =\ldots$$
Dobbiamo risolvere questo integrale, quindi
$$\int_{-\infty}^{\infty} e^{-(it/2m\hbar)u^{2}} \ du=\sqrt{ \frac{2m\hbar}{t} }\int_{-\infty}^{\infty} e^{-iv^{2}} \ dv $$
usando $\frac{t}{2m\hbar}u^{2}=v^{2}$ e quindi $v=\sqrt{ \frac{t}{2m\hbar} }u$. Chiamando il propagatore $G(y-x)$, esso è
$$G(y-x)=e^{im(x-y)^{2}/2\hbar t}\sqrt{ \frac{2m\hbar}{t} } \frac{1}{2\pi \hbar}\int_{-\infty}^{\infty} e^{-iv^{2}} \ dv $$
Con la sostituzione $iv^{2}=w^{2}$ ho $w=\sqrt{ iv^{2} }=\sqrt{ i }v$. Allora
$$\int_{-\infty}^{\infty} e^{-iv^{2}} \ dv =\int_{-\infty}^{\infty} \frac{e^{-w^{2}}}{\sqrt{ i }} \ dw= \sqrt{ \frac{\pi}{i} }$$
e quindi mi aspetto che il propagatore sia
$$G(y-x)=e^{im(x-y)^{2}/2\hbar t}\sqrt{ \frac{m}{2it\pi \hbar} }$$
Ora possiamo introdurre il propagatore nell'espressione originale per $\psi_{t}(x)$:
$$\boxed{\psi_{t}(x)=\sqrt{ \frac{m}{2it\pi \hbar} }\int_{-\infty}^{\infty} e^{im(x-y)^{2}/2\hbar t}\psi(y) \ dy }$$
che è l'[[ampiezza di probabilità]] di trovare la particella in un intervallo centrato in $x$ a partire da un intervallo centrato in $y$. La probabilità in sé è $\lvert \psi_{t}(x) \rvert^{2}$.

È notevole il fatto che questa probabilità sia in generale non nulla per qualunque intervallo spaziale. Dal punto di vista fisico, questo è una chiara violazione della relatività, dato che c'è una probabilità che una particella viaggi in un luogo [[Spacetime|spaziotemporalmente]] disconnesso, nel senso che la luce non viaggia a sufficiente velocità per connettere i due punti nell'intervallo di tempo dato. In altre parole, c'è una possibilità che una particella si ritrovi in un punto al di fuori del [[cono di luce]] costruito attorno ad esso. La ragione è dovuta al fatto che l'equazione di Schrödinger dipenda da $\frac{ \partial  }{ \partial t }$ e non da $\frac{ \partial  }{ \partial t^{2} }$ come dovrebbe una [[equazione d'onda]]. La teoria quantistica dei campi e l'utilizzo dell'[[Dirac equation]] anziché di quella di Schrödinger risolvono il problema.

[^1]: Questa relazione è particolarmente utile, dato che se conosciamo $k$, conosciamo anche $p$. È doppiamente importante perché questo legame fa sì che $k$ si comporti come $p$ ai fini del [[Disuguaglianza di Heisenberg|principio di indeterminazione]], quindi se l'errore su $x$ è basso, l'errore su $k$ è alto.
[^2]: È certamente sensato avere una $\phi(k)$ più generica e diffusa, ma la nozione di gruppo — e quindi di velocità di gruppo — perde senso quando la $\phi(k)$ diventa così "diluita", dato che il gruppo cambia forma di continuo a causa delle diverse velocità interne.