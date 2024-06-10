---
aliases:
  - particella quantistica libera
---
La **particella libera** è un sistema quantistico costituito da una singola [[Particella]] in assenza di [[Potenziale]], ovvero $V(x)=0$ ovunque. Nel caso classico, questo sistema è banale e ha soluzioni immediate, dato che la particella compie un semplice moto rettilineo a velocità costante, ma nel caso quantistico compaiono problemi non trascurabili e diventa più complesso dell'[[Oscillatore armonico quantistico]].
## Soluzione
Partiamo come al solito dall'[[Equazione di Schrödinger#Potenziale indipendente dal tempo|equazione di Schrödinger indipendente dal tempo]]
$$- \frac{\hbar^{2}}{2m} \frac{d^{2}\psi}{dx^{2}}=E\psi$$
che ha potenziale nullo. Come per la [[Buca infinita quantistica|buca infinita]], scriviamola in una forma più compatta
$$\frac{d^{2}\psi}{dx^{2}}=-k^{2}\psi,\quad\text{con }k\equiv \frac{\sqrt{2mE}}{\hbar}$$
la cui soluzione generale è
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

> **Risultato.** Una particella libera non può esistere in uno stato stazionario. Detta in altri termini, non esistono particelle libere con un'energia ben definita.

Dunque, le soluzioni separabili di cui sopra non hanno alcun significato fisico, ma ne hanno uno matematico. Di fatto, la soluzione generale non è più una *somma* su degli stati *numerabili* determinati dall'indice $n$, bensì un *integrale* su infiniti stati *non numerabili* determinati dalla variabile continua $k$. La [[Funzione d'onda]] definitiva, allora, è
$$\boxed{\Psi(x,t)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^{+\infty}\phi(k)e^{ik[x-(\hbar k/2m)t]}dk}$$
In questa forma, $\phi(k)/\sqrt{2\pi}$ prende il ruolo dei coefficienti $c_{n}$ della forma discreta. Questa funzione d'onda può essere normalizzata per appropriati $\phi(k)$ e quindi ha significato fisico. Ciascun $\phi(k)$ però porta necessariamente con sé un intervallo di $k$, non un singolo $k$, e quindi un intervallo di energie e velocità. Questo si chiama *pacchetto d'onda*.

A tempo zero, la funzione d'onda iniziale ha la forma
$$\Psi(x,0)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^{+\infty}\phi(k)e^{ixk}dk=F[\phi(k)](x)$$
Ma questa non è altro che la [[Trasformata di Fourier]] dal dominio delle frequenze spaziali $k$ a quello delle posizioni $x$. Per estrarre $\phi(k)$, basta applicare l'antitrasformata:
$$\boxed{\phi(k)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^{+\infty}\Psi(x,0)e^{-ikx}dx=F^{-1}[\Psi(x,0)](k)}$$
È giusto menzionare che gli integrali per $\phi(k)$ e soprattutto per $\Psi(x,t)$ sono raramente risolvibili analiticamente.
### Paradosso della velocità
Nella ricerca della funzione d'onda per la particella libera, ci si è imbattuti in un paradosso: la velocità data dalla teoria classica è il doppio di quella data dalla teoria quantistica, anche se rappresentano la stessa identica particella. Il problema di fatto non sussiste, dato che la soluzione che porta a questo problema non ha significato fisico, ma è comunque interessante studiare il perché di questo paradosso.

Definiamo a grandi linee un pacchetto d'onda: un pacchetto d'onda è una sovrapposizione di funzioni sinusoidali modulate dalla funzione $\phi(k)$. Si tratta di un'onda contenuta in un battimento e come in tutti questi casi, si hanno due tipi di velocità, non una: la **velocità di fase** è la velocità che ha un punto sull'onda, mentre la **velocità di gruppo** è la velocità del battimento. Queste possono, ma non devono, essere uguali.

Ciò che importa è che per un'onda quantistica, la velocità di gruppo è il doppio della velocità di fase. Ciò riconcilia le due teorie, ma va dimostrato. La [[relazione di dispersione]] dell'onda della particella libera è $\omega(k)=\hbar k^{2}/2m$. Assumiamo che $\phi(k)$ abbia un picco piuttosto localizzato attorno ad un $k_{0}$[^2]. Allora, possiamo espandere in [[Polinomio di Taylor|serie di Taylor]] la $\omega(k)$ attorno a $k_{0}$ senza grandi errori:
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

[^1]: Questa relazione è particolarmente utile, dato che se conosciamo $k$, conosciamo anche $p$. È doppiamente importante perché questo legame fa sì che $k$ si comporti come $p$ ai fini del [[Disuguaglianza di Heisenberg|principio di indeterminazione]], quindi se l'errore su $x$ è basso, l'errore su $k$ è alto.
[^2]: È certamente sensato avere una $\phi(k)$ più generica e diffusa, ma la nozione di gruppo - e quindi di velocità di gruppo - perde senso quando la $\phi(k)$ diventa così "diluita", dato che il gruppo cambia forma di continuo a causa delle diverse velocità interne.