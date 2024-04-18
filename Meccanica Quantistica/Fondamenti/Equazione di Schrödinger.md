L'**equazione di Schrödinger** è un'equazione differenziale di secondo grado che descrive lo [[stato]] di un sistema quantistico in un dato tempo $t$. Si esprime come
$$\boxed{i\hbar \frac{\partial \Psi}{\partial t}=- \frac{\hbar^{2}}{2m} \frac{\partial ^{2}\Psi}{\partial x^{2}}+V\Psi}$$
dove $\hbar$ è la [[costante di Planck]] ridotta, $m$ è la massa della [[particella]], $\Psi(x,t)$ è la [[funzione d'onda]] della particella in esame e $V$ è la funzione energia potenziale della particella. Risolvere l'equazione di Schrödinger, trovando quindi l'equazione d'onda, ci permette di conoscere l'evoluzione temporale del sistema quantistico.

Una forma più generale dell'equazione di Schrödinger è
$$i\hbar \frac{\partial }{\partial t}|\Psi_{t}\rangle=\hat{H}|\Psi_{t}\rangle$$
dove $\hat{H}$ è l'[[operatore]] [[Hamiltoniana|Hamiltoniano]] del sistema e $|\Psi_{t}\rangle$ è lo stato al tempo $t$. Essa è risolta dall'[[evolutore]] e grazie a esso si trova che è *reversibile*. Quindi la dinamica descritta dall'equazione di Schrödinger è reversibile. Questo è un fatto molto importante dato che la dinamica descritta dal collasso di un pacchetto d'onda è *irreversibile*. Come sia possibile che queste due dinamiche coesistano è un problema aperto della fisica.
## Potenziale indipendente dal tempo
Per risolvere l'equazione di Schrödinger bisogna determinare un certo potenziale $V(x,t)$. Possiamo restringere il set di potenziali a quelli indipendenti dal tempo, a modo tale che valga $V(x)$ e non $V(x,t)$.
### Soluzione
Allora, possiamo risolvere l'equazione mediante [[equazioni a variabili separabili|separazione delle variabili]]. Dunque, cerchiamo soluzioni della forma
$$\Psi(x,t)=\psi(x)\varphi(t)$$
Per queste soluzioni vale
$$\frac{\partial \Psi}{\partial t}=\psi \frac{d \varphi}{d t}, \quad \frac{\partial ^{2}\Psi}{\partial x^{2}}=\frac{d^{2}\psi}{dx^{2}}\varphi$$
e l'equazione di Schrödinger diventa dunque
$$i\hbar\psi \frac{d\varphi}{dt}=- \frac{\hbar^{2}}{2m} \frac{d^{2}\psi}{dx^{2}}\varphi+V\psi\varphi$$
che dividendo per $\psi \varphi$ prende la forma
$$\frac{i\hbar}{\varphi(t)} \frac{d\varphi}{dt}(t)=- \frac{\hbar^{2}}{2m} \frac{1}{\psi(x)} \frac{d^{2}\psi}{dx^{2}}(x)+V(x)$$
dove il membro sinistro dipende solo da $t$ e quello destro da $x$. L'unico caso qui possibile che i due membri siano *entrambi costanti*; se non lo fossero, potrei variare $t$ in quello a sinistra e quindi variare quello a destra a causa dell'uguaglianza. Ma il membro a destra è solo dipendente da $x$, non da $t$, quindi non ha senso che cambi variando $t$. Allora segue che devono essere costanti. Chiamiamo allora $E$ la costante a cui sono uguali. Allora risolvendo i due membri si trova
$$\frac{d\varphi}{dt}(t)=- \frac{iE}{\hbar}\varphi(t) \tag{1}$$
$$\boxed{- \frac{\hbar^{2}}{2m} \frac{d^{2}\psi}{dx^{2}}(x) + V(x)\psi(x)=E\psi(x)\tag{2}}$$
che è un sistema di due differenziali ordinarie *non parziali*. La soluzione della $(1)$ si ottiene integrando
$$\int\frac{1}{\varphi}d\varphi=- \frac{iE}{\hbar}\int dt \quad \rightarrow \quad \varphi=Ce^{-iEt/\hbar}$$
La soluzione della $(2)$, detta *equazione di Schrödinger indipendente dal tempo*, si può trovare solo una volta deciso il potenziale.

Se due o più soluzioni distinte (ossia [[lineare indipendenza|linearmente indipendenti]]) della $(2)$ hanno la stessa energia $E$, allora si dicono **degeneri**.
### Proprietà delle soluzioni separabili
Questa forma conferisce alle soluzioni alcune proprietà particolari:
1. sono *stati stazionari*. Ciò significa che il [[valore di aspettazione]] della funzione d'onda, ma anche quello di *qualunque* [[variabile dinamica]], è costante nel tempo. È possibile dunque tralasciare il termine temporale $\varphi$ e usare solo quello spaziale $\psi$. Vale anche che se $\Psi$ è normalizzata, lo è anche $\psi$.
2. L'energia totale è definita e può essere espressa come un'Hamiltoniana della forma $$H(x,p)=\frac{p^{2}}{2m}+V(x)$$con operatore Hamiltoniano associato $$\hat{H}=- \frac{\hbar^{2}}{2m}\frac{\partial ^{2}}{\partial x^{2}}+V(x)$$ottenuto sostituendo $p$ con $\hat{p}$. Allora l'equazione di Schrödinger indipendente dal tempo può essere scritta nella forma estremamente compatta $$\boxed{\hat{H}\psi=E\psi}\tag{3}$$che è un'[[equazione agli autovalori]] per l'Hamiltoniana, di autovalore $E$ e autofunzione $\psi$. Allora, $\psi$ è uno [[stato determinato]] di $\hat{H}$.
3. La soluzione generale dell'equazione di Schrödinger *dipendente* dal tempo è una combinazione lineare delle soluzioni separabili *indipendenti* dal tempo. Ciò significa che una volta risolta l'equazione indipendente, si può costruire la soluzione di quella dipendente.
#### Dimostrazioni e dettagli
*Stati stazionari.* Prendiamo una soluzione $\Psi(x,t)=\psi(x)e^{-iEt/\hbar}$. Ovviamente dipende da $t$, ma la sua densità di probabilità *no*:
$$|\Psi(x,t)|^{2}=\Psi^{*}\Psi=\psi^{*}e^{iEt/\hbar}\psi e^{-iEt/\hbar}=|\psi(x)|^{2}$$
Lo stesso vale per ogni possibile variabile dinamica
$$\left\langle Q(x,p) \right\rangle=\int_{-\infty}^{+\infty}\psi^{*}Q\left(x, \frac{\hbar}{i} \frac{\partial }{\partial x}\right)\psi dx$$
In particolare, la posizione $\left\langle x \right\rangle$ è costante, quindi $\left\langle p \right\rangle=0$. Dunque, (ci si aspetta che) nulla si muove in uno stato stazionario.

*Caratteristiche dell'Hamiltoniana.* Il valore di aspettazione dell'Hamiltoniana $H$ è
$$\left\langle H \right\rangle=\int_{-\infty}^{+\infty}\psi^{*}\hat{H}\psi \;dx=E\int_{-\infty}^{+\infty}|\psi|^{2}dx=E\int_{-\infty}^{+\infty}|\Psi|^{2}=E$$
che è proprio la costante di separazione trovata nella soluzione sopra. Cerchiamo anche la varianza di $H$. Partendo da
$$\hat{H}^{2}\psi=\hat{H}(\hat{H}\psi)=\hat{H}(E\psi)=E(\hat{H}\psi)=E^{2}\psi$$
si ottiene
$$\left\langle H^{2} \right\rangle=\int_{-\infty}^{+\infty}\psi^{*}\hat{H}^{2}\psi\;dx=E^{2}\int_{-\infty}^{+\infty}|\psi|^{2}dx=E^{2}$$
$$\sigma_{H}^{2}=\left\langle H^{2} \right\rangle-\left\langle H \right\rangle^{2}=E^{2}-E^{2}=0$$
Ciò implica che *ogni misura dell'energia totale darà esattamente $E$*, a differenza delle altre [[Osservabile|osservabili]], che sono soggette all'[[indeterminatezza quantistica]]. Questo è un esempio di stato determinato.

*Soluzione generale.* Risolvere l'equazione indipendente di Schrödinger dà un insieme infinito di soluzioni $\psi_{1},\psi_{2},\ldots$, ciascuna con un'energia associata $E_{1},E_{2},\ldots$. Allora è possibile esprimere la soluzione generale a tempo zero come
$$\Psi(x,0)=\sum\limits_{n=1}^{\infty}c_{n}\psi_{n}(x)$$
con $c_{1},c_{2},\ldots$ costanti complesse che esistono *sempre*. È poi possibile generalizzare al caso dipendente dal tempo aggiungendo il termine temporale $\varphi$ per ottenere
$$\boxed{\Psi(x,t)=\sum\limits_{n=1}^{\infty}c_{n}\psi_{n}(x)e^{-iE_{n}t/\hbar}=\sum\limits_{n=1}^{\infty}c_{n}\Psi_{n}(x,t)}$$
dove $\psi_{n}e^{-iEt/\hbar}=\Psi_{n}(x,t)$ sono le soluzioni separabili. È importante notare come sebbene queste siano stati stazionari, la soluzione generale *non lo è*.

Partendo dalla $(3)$, si dimostra che vale
$$\left\langle H \right\rangle=\sum\limits_{n=1}^{\infty}|c_{n}|^{2}E_{n}$$
Questo dimostra un fatto importante: dato che le $|c_{n}|^{2}$ possono essere interpretate come probabilità e che sono indipendenti dal tempo, la probabilità di ottenere un certo $E_{n}$ è essa stessa indipendente dal tempo. Questa è una manifestazione della conservazione dell'energia in meccanica quantistica.
#### Teoremi utili
Per soluzioni normalizzabili, la costante di separazione $E$ è sempre reale.

La funzione d'onda indipendente dal tempo $\psi(x)$ può essere sempre considerata reale, a differenza di $\Psi(x,t)$ che è sempre complessa. Ciò non significa che ogni $\psi_{n}$ deve essere reale, ma è sempre possibile esprimere ogni $\psi_{n}$ complessa come combinazione lineare di $\psi_{n}$ reali con la stessa energia.

Se $V(x)$ è pari, allora $\psi(x)$ è o pari o dispari.

In una dimensione, non esistono [[Stati in meccanica quantistica|stati legati]] degeneri.