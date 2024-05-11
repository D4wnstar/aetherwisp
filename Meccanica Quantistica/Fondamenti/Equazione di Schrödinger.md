L'**equazione di Schrödinger** è un'equazione differenziale di secondo grado che descrive lo [[Stato]] di un sistema quantistico in un dato tempo $t$. Nel caso unidimensionale, si esprime come
$$i\hbar \frac{\partial \Psi}{\partial t}=- \frac{\hbar^{2}}{2m} \frac{\partial ^{2}\Psi}{\partial x^{2}}+V\Psi\tag{1D}$$
dove $\hbar$ è la [[costante di Planck]] ridotta, $m$ è la massa della [[particella]], $\Psi(x,t)$ è la [[Funzione d'onda]] della particella in esame e $V$ è la funzione energia potenziale della particella. In tre dimensione ha la forma
$$i\hbar \frac{\partial \Psi}{\partial t}=- \frac{\hbar^{2}}{2m}\nabla^{2}\Psi+V\Psi\tag{3D}$$
con $\nabla^{2}$ il [[laplaciano]].

Risolvere l'equazione di Schrödinger, trovando quindi l'equazione d'onda, ci permette di conoscere l'evoluzione temporale del sistema quantistico.

Una forma più generale dell'equazione di Schrödinger è
$$i\hbar \frac{\partial }{\partial t}|\mathcal{S}(t)\rangle=\hat{H}|\mathcal{S}(t)\rangle$$
dove $\hat{H}$ è l'[[operatore]] [[Hamiltoniana|Hamiltoniano]] del sistema e $|\mathcal{S}(t)\rangle$ è lo [[Stato]] al tempo $t$, che può essere rappresentato da una varietà di costrutti matematici, come una funzione d'onda. Essa è risolta dall'[[Evolutore]] e grazie a esso si trova che è *reversibile*. Quindi la dinamica descritta dall'equazione di Schrödinger è reversibile. Questo è un fatto molto importante dato che la dinamica descritta dal collasso di un pacchetto d'onda è *irreversibile*. Come sia possibile che queste due dinamiche coesistano è un problema aperto della fisica.
## Potenziale indipendente dal tempo
Per risolvere l'equazione di Schrödinger bisogna determinare un certo potenziale $V(x,t)$. Possiamo restringere il set di potenziali a quelli indipendenti dal tempo, a modo tale che valga $V(x)$ e non $V(x,t)$.
### Soluzione unidimensionale
Allora, possiamo risolvere l'equazione mediante [[equazioni a variabili separabili|separazione delle variabili]]. Dunque, cerchiamo soluzioni della forma
$$\Psi(x,t)=\psi(x)\varphi(t)$$
Per queste soluzioni vale
$$\frac{\partial \Psi}{\partial t}=\psi \frac{d \varphi}{d t}, \quad \frac{\partial ^{2}\Psi}{\partial x^{2}}=\frac{d^{2}\psi}{dx^{2}}\varphi$$
e l'equazione di Schrödinger diventa dunque
$$i\hbar\psi \frac{d\varphi}{dt}=- \frac{\hbar^{2}}{2m} \frac{d^{2}\psi}{dx^{2}}\varphi+V\psi\varphi$$
che dividendo per $\psi \varphi$ prende la forma
$$\frac{i\hbar}{\varphi(t)} \frac{d\varphi}{dt}(t)=- \frac{\hbar^{2}}{2m} \frac{1}{\psi(x)} \frac{d^{2}\psi}{dx^{2}}(x)+V(x)$$
dove il membro sinistro dipende solo da $t$ e quello destro da $x$. L'unico caso qui possibile che i due membri siano *entrambi costanti*; se non lo fossero, potrei variare $t$ in quello a sinistra e quindi variare quello a destra a causa dell'uguaglianza. Ma il membro a destra è solo dipendente da $x$, non da $t$, quindi non ha senso che cambi variando $t$. Allora segue che devono essere costanti. Chiamiamo allora $E$ la costante (detta *di separazione*) a cui sono uguali. Allora risolvendo i due membri si trova
$$\frac{d\varphi}{dt}(t)=- \frac{iE}{\hbar}\varphi(t) \tag{1}$$
$$\boxed{- \frac{\hbar^{2}}{2m} \frac{d^{2}\psi}{dx^{2}}(x) + V(x)\psi(x)=E\psi(x)\tag{2}}$$
che è un sistema di due differenziali ordinarie *non parziali*. La soluzione della $(1)$ si ottiene integrando
$$\int\frac{1}{\varphi}d\varphi=- \frac{iE}{\hbar}\int dt \quad \rightarrow \quad \varphi=Ce^{-iEt/\hbar}$$
La soluzione della $(2)$, detta *equazione di Schrödinger indipendente dal tempo*, si può trovare solo una volta deciso il potenziale.

Se due o più soluzioni distinte (ossia [[lineare indipendenza|linearmente indipendenti]]) della $(2)$ hanno la stessa energia $E$, allora si dicono **degeneri**.
### Proprietà delle soluzioni separabili
Questa forma conferisce alle soluzioni alcune proprietà particolari:
1. sono *stati stazionari*. Ciò significa che il [[valore di aspettazione]] della funzione d'onda, ma anche quello di *qualunque* [[variabile dinamica]], è costante nel tempo. È possibile dunque tralasciare il termine temporale $\varphi$ e usare solo quello spaziale $\psi$. Vale anche che se $\Psi$ è normalizzata, lo è anche $\psi$.
2. L'energia totale è definita e può essere espressa come un'Hamiltoniana della forma $$H(x,p)=\frac{p^{2}}{2m}+V(x)$$con operatore Hamiltoniano associato $$\hat{H}=- \frac{\hbar^{2}}{2m}\frac{\partial ^{2}}{\partial x^{2}}+V(x)$$ottenuto sostituendo $p$ con $\hat{p}$. Allora l'equazione di Schrödinger indipendente dal tempo può essere scritta nella forma estremamente compatta $$\boxed{\hat{H}\psi=E\psi}\tag{3}$$che è un'[[Equazione agli autovalori]] per l'Hamiltoniana, di autovalore $E$ e autofunzione $\psi$. Allora, $\psi$ è uno [[Stato determinato]] di $\hat{H}$.
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
Ciò implica che *ogni misura dell'energia totale darà esattamente $E$*, a differenza delle altre [[Osservabile|osservabili]], che sono soggette all'[[Indeterminatezza quantistica]]. Questo è un esempio di stato determinato.

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
### Soluzione tridimensionale
Per uno spazio tridimensionale, si giunge ad una simile conclusione. L'equazione indipendente dal tempo in tre dimensioni è
$$\boxed{- \frac{\hbar^{2}}{2m}\nabla^{2}\psi+V\psi=E\psi}$$
e la soluzione all'equazione tempo-dipendente è
$$\boxed{\Psi(\vec{r},t)=\sum\limits_{n=1}^{\infty}c_{n}\psi_{n}(\vec{r})e^{-iE_{n}t/\hbar}=\sum\limits_{n=1}^{\infty}c_{n}\Psi_{n}(\vec{r},t)}$$
#### Separazione delle variabili
A differenza del caso unidimensionale, possiamo ripetere di nuovo la separazione delle variabili per suddividere ancora la funzione d'onda in due componenti: una radiale e una angolare. Allora chiediamo che la funzione d'onda tempo-indipendente abbia soluzioni della forma
$$\psi(r,\theta,\phi)=R(r)Y(\theta,\phi)\tag{4}$$
Esprimo l'equazione di Schrödinger tempo-indipendente in coordinate sferiche, dato che molti sistemi quantistici hanno potenziale a simmetrica sferica (come i modelli di [[atomo]]):
$$- \frac{\hbar^{2}}{2m}\left[\frac{1}{r^{2}}\frac{\partial }{\partial r}\left(r^{2}\frac{\partial \psi}{\partial r}\right)+ \frac{1}{r^{2}\sin\theta}\frac{\partial }{\partial \theta}\left(\sin\theta \frac{\partial \psi}{\partial \theta}\right)+ \frac{1}{r^{2}\sin^{2}\theta}\left(\frac{\partial ^{2}\psi}{\partial \phi^{2}}\right)\right] + V\psi=E\psi$$
e sostituendo la $(4)$ troviamo
$$- \frac{\hbar^{2}}{2m}\left[\frac{Y}{r^{2}}\frac{\partial }{\partial r}\left(r^{2}\frac{\partial R}{\partial r}\right)+ \frac{R}{r^{2}\sin\theta}\frac{\partial }{\partial \theta}\left(\sin\theta \frac{\partial Y}{\partial \theta}\right)+ \frac{R}{r^{2}\sin^{2}\theta}\left(\frac{\partial ^{2}Y}{\partial \phi^{2}}\right)\right] + VRY=ERY$$
Ora possiamo dividere per $RY$ e moltiplicare per $-2mr^{2}/\hbar^{2}$:
$$\left[\frac{1}{R}\frac{\partial }{\partial r}\left(r^{2}\frac{\partial R}{\partial r}\right) - \frac{2mr^{2}}{\hbar^{2}}[V(r)-E]\right]+ \frac{1}{Y}\left[\frac{1}{\sin\theta}\frac{\partial }{\partial \theta}\left(\sin\theta \frac{\partial Y}{\partial \theta}\right)+ \frac{1}{\sin^{2}\theta}\frac{\partial ^{2}Y}{\partial \phi^{2}}\right]= 0$$
dove il primo termine dipende solo da $r$ e il secondo solo da $(\theta,\phi)$. Di conseguenza, entrambe devono pari ad una costante di separazione, proprio come nella soluzione del caso unidimensionale. Decido che questa costante ha la forma $l(l+1)$. Dunque trovo il sistema di due equazioni
$$\frac{1}{R}\frac{\partial }{\partial r}\left(r^{2}\frac{\partial R}{\partial r}\right) - \frac{2mr^{2}}{\hbar^{2}}[V(r)-E]=l(l+1)\tag{5}$$
$$\frac{1}{Y}\left[\frac{1}{\sin\theta}\frac{\partial }{\partial \theta}\left(\sin\theta \frac{\partial Y}{\partial \theta}\right)+ \frac{1}{\sin^{2}\theta}\frac{\partial ^{2}Y}{\partial \phi^{2}}\right]=-l(l+1)\tag{6}$$
Idealmente ora vogliamo determinare la forma di $R$ e $Y$, dette rispettivamente *parte radiale* e *parte angolare*.
#### Parte angolare
Se moltiplichiamo la $(6)$ per $Y\sin^{2}\theta$ otteniamo
$$\sin\theta\frac{\partial }{\partial \theta}\left(\sin\theta \frac{\partial Y}{\partial \theta}\right)+ \frac{\partial ^{2}Y}{\partial \phi^{2}}=-l(l+1)Y\sin^{2}\theta$$
Proviamo ancora con la separazione delle variabili, richiedendo che la soluzione sia del tipo
$$Y(\theta,\phi)=\Theta(\theta)\Phi(\phi)$$
Come da norma, sostituendo e moltiplicando per $\Theta\Phi$ si trova
$$\left\{\frac{1}{\Theta}\left[\sin\theta \frac{d}{d\theta}\left(\sin\theta \frac{d\Theta}{d\theta}\right)\right]+l(l+1)\sin^{2}\theta\right\} + \frac{1}{\Phi} \frac{d^{2}\Phi}{d\phi^{2}}=0$$
Il primo termine (tra le graffe) dipende solo da $\theta$, il secondo solo da $\phi$. Allora chiamo la costante di separazione $m^{2}$ e si ha il sistema
$$\frac{1}{\Theta}\left[\sin\theta \frac{d}{d\theta}\left(\sin\theta \frac{d\Theta}{d\theta}\right)\right]+l(l+1)\sin^{2}\theta=m^{2}$$
$$\frac{1}{\Phi} \frac{d^{2}\Phi}{d\phi^{2}}=-m^{2}$$
L'equazione in $\phi$ è banale. La soluzione è[^1]
$$\frac{d^{2}\Phi}{d\phi^{2}}=-m^{2}\phi \Rightarrow \boxed{\Phi(\phi)=e^{im\phi}}$$
Scegliamo il ramo della funzione esponenziale notando che, ruotando di $2\pi$, torniamo nel punto iniziale, quindi deve valere[^2]
$$\Phi(\phi+2\pi)=\Phi(\phi) \Rightarrow e^{im(\phi+2\pi)}=e^{im\phi} \Rightarrow e^{2\pi im}=1$$
Che non è altro che la formula di Eulero per i numeri complessi. Allora $m$ deve essere un numero intero $0,\pm1,\pm2,\ldots$.

L'equazione in $\theta$ è più complessa. Riscriviamola come
$$\left[\sin\theta \frac{d}{d\theta}\left(\sin\theta \frac{d\Theta}{d\theta}\right)+l(l+1)\sin^{2}\theta-m^{2}\right]\Theta=0$$
Si trova che la soluzione di questa equazione è
$$\boxed{\Theta(\theta)=AP_{l}^{m}(\cos\theta)}$$
dove $A$ è una costante e $P_{l}^{m}$ è la [[Polinomi di Legendre#Polinomi associati di Legendre|funzione di Legendre associata]], definita come
$$P_{l}^{m}(x)\equiv (1-x^{2})^{|m|/2} \left(\frac{d}{dx}\right)^{m}P_{l}(x)$$
dove $P_{l}(x)$ è la [[Polinomi di Legendre|funzione di Legendre]]. Solo valori interi di $l$ e $m$ hanno senso fisico, quindi $P_{l}^{m}$ diventano i polinomi di Legendre associati. Allora la parte angolare è
$$\boxed{Y(\theta,\phi)=AP_{l}^{m}(\cos\theta)e^{im\theta}}$$
#### Parte radiale
La parte radiale è diversa da quella angolare nel fatto che contiene anche il potenziale. Se la parte angolare è indipendente dal potenziale, quella radiale dipende dalla sua forma. Moltiplichiamo la $(5)$ per $R$ e riscriviamo le derivate come totali anziché parziali per ottenere
$$\frac{d}{dr}\left(r^{2}\frac{dR}{dr}\right) - \frac{2mr^{2}}{\hbar^{2}}[V(r)-E]R=l(l+1)R$$
Possiamo compiere un cambio di variabili per semplificare
$$u(r)\equiv rR(r)$$
con cui
$$\boxed{- \frac{\hbar^{2}}{2m} \frac{d^{2}u}{dr^{2}}+\left[V+ \frac{\hbar^{2}}{2m} \frac{l(l+1)}{r^{2}}\right]u=Eu}\tag{7}$$
Questa si chiama **equazione radiale** e va risolta in base al potenziale dato. È molto importante il fatto che sia *esattamente* l'equazione di Schrödinger indipendente dal tempo in una dimensione $(2)$, con un *potenziale effettivo* $V_{\text{eff}}$ pari a
$$V_{\text{eff}}=V+ \frac{\hbar^{2}}{2m} \frac{l(l+1)}{r^{2}}$$
che contiene un termine aggiuntivo detto **termine centrifugale** che tende a "spingere" la particella verso "fuori", proprio come la pseudoforza centrifuga in meccanica classica.
#### Normalizzazione
Ora vogliamo normalizzare le nostre soluzioni. La condizione di normalizzazione in tre dimensioni è
$$\int|\psi|^{2}d\tau=\int|\psi|^{2}r^{2}\sin\theta drd\theta d\phi=\int|R|^{2}r^{2}dr\int|Y|^{2}\sin\theta d\theta d\phi=1$$
Normalizziamo parte radiale e angolare separatamente, cioè
$$\int_{0}^{\infty}|R|^{2}r^{2}dr=1, \quad \int_{0}^{2\pi}\int_{0}^{\pi}|Y|^{2}\sin\theta d\theta d\phi=1$$

La parte angolare normalizzata non è altro che la $l$-$m$-esima [[armoniche sferiche|armonica sferica]] e vale
$$Y_{l}^{m}(\theta,\phi)=\epsilon\sqrt{\frac{2l+1}{4\pi} \frac{(l-|m|)!}{(l+|m|)!}}e^{im\phi}P_{l}^{m}(\cos\theta)$$
dove $\epsilon$ è $(-1)^{m}$ per $m\geq0$ e $1$ per $m\leq0$. Nel contesto della meccanica quantistica, $l$ è detto *numero quantico di momento angolare* e $m$ *numero quantico magnetico*.

La parte radiale normalizzata non ha una forma generale perché dipende dal potenziale.


[^1]: Tecnicamente ci sono due soluzioni: $\exp(im\phi)$ e $\exp(-im\phi)$, ma dato che $m$ può essere negativo, le due coincidono (basta cambiare $m$). Dovrebbe esserci un fattore di scala di fronte, come $C\exp(im\phi)$, ma per convenienza lo assorbiamo nella soluzione di $\Theta$, dato che dovranno inevitabilmente essere moltiplicate l'una per l'altra.
[^2]: Questo ragionamento non è propriamente rigoroso. Ci sono modi più corretti di determinare questa condizione, che in ogni caso è vera.