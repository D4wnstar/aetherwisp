Le **equazioni di Friedmann** sono un insieme di equazioni che spiegano l'[[espansione dell'universo]] in un modello cosmologico che obbedisce al [[principio cosmologico]]. Derivano da una soluzione dipendente dal tempo dell'[[equazione di Einstein]].
## Derivazione dalle leggi di Newton
Sebbene non sia un modo efficace di studiare l'universo, è possibile derivare le equazioni di Friedmann dalle [[leggi di Newton]]. È necessario tuttavia usare un risultato della relatività generale: il [[teorema di Birkhoff]], che è una generalizzazione [[Lorentz transformation|relativistica]] del [[teorema di Gauss]]. In sostanza, dice che in una sfera di distribuzione di massa omogenea e isotropa, l'evoluzione all'interno della sfera non è influenzato da quella all'esterno della sfera.
### Seconda equazione
Consideriamo una sfera di raggio $r$ e densità di massa $\rho$ in espansione secondo la [[legge di Hubble]] e un oggetto "tracciante"[^1] con massa $m$ piccola che si allontana da noi. Lo osserviamo al tempo $t_{0}$ a distanza $r$ e si sta allontanando a velocità $v$. Allora vale
$$v=Hr$$
con $H$ un numero, non necessariamente costante.

![[Schema Modello Friedmann|center]]


Per conservazione dell'energia, l'energia del tracciante è
$$E=\frac{1}{2}mv^{2}- \frac{GmM}{r}=\text{cost.}$$
dato da energia cinetica e potenziale gravitazionale della massa tra noi e l'oggetto. Ci sono due casi fondamentali: se $E<0$, l'oggetto è in un sistema gravitazionale [[Stati in meccanica quantistica|legato]] e prima o poi torna a cadere verso di noi: nel caso della massa di tutto l'universo questo evento si chiama *Big Crunch*; se $E>0$, si allontana all'infinito.

Consideriamo il caso limite $E=0$, chiamata *energia critica*. Deve essere
$$\frac{1}{2}mv^{2}- \frac{GmM}{r}=0$$
La massa nella sfera è
$$M=\frac{4}{3}\pi r^{3}\rho$$
che non dipende da $r$. Sostituendo $v$ ed $M$:
$$\frac{1}{2}H^{2}r^{2}=\frac{G}{r} \frac{4\pi}{3}r^{3}\rho \quad\rightarrow\quad \frac{1}{2}H^{2}=\frac{4\pi}{3}G \rho \quad \rightarrow \quad \rho=\frac{3H^{2}}{8\pi G}$$
da cui definiamo la *densità critica* come la densità a cui vale $E=0$:
$$\rho_{c}=\frac{3H^{2}}{8\pi G}$$
se $\rho>\rho_{c}$, l'energia è positiva, mentre se $\rho<\rho_{c}$, l'energia è negativa.

Utilizzando $H^{-1}=9.78\times10^{9}\ h^{-1}yr$ troviamo che la densità critica è $\rho_{C}=1.88\times10^{-29}\ h^{2}g\;cm^{-3}$, che è la densità di un universo *critico*. Se l'universo ha più densità di così (e quindi più massa), è destinato a collassare in un Big Crunch. Se è più basso, si espande all'infinito. Con misure approssimate si trova che, considerando tutte le [[stella|stelle]] stimate dell'universo, la densità dell'Universo è circa il 31% di quella critica. Possiamo esprimere la densità critica anche in altre unità, come $\rho_{C}=2.78\times10^{11}\ h^{2}M_{\odot}Mpc^{-3}$. Sappiamo per esempio che l'ammasso di Andromeda ha una densità media circa 10 volte più alta.

Avendo una densità di riferimento, possiamo definire
$$\Omega_{m}=\frac{\rho}{\rho_{c}}=\frac{8\pi G}{3H^{2}}\rho$$
il **parametro di densità di materia**. La $m$ sta per [[materia]] e si legge *omega matter*.

Consideriamo $t=\frac{1}{\sqrt{G\rho}}$, ossia il [[tempo dinamico]] di un sistema autogravitante. Quindi abbiamo che $H^{-1}$ ha le dimensioni di un tempo dinamico.

Definiamo cos'è $H$. Le misure umane dell'universo possono essere assunte come tutte fatte nello stesso istante rispetto all'età dell'universo: chiamiamolo $t_{0}$. Prendiamo una distanza $r_{0}$ (ad esempio, quella della sfera di prima) e chiamiamo la quantità $a(t)=r/r_{0}$ **fattore di scala**. Per definizione, $a(t_{0})=1$.

Riprendiamo $v=Hr$, da cui $H=v/r$. Usando che $v=dr/dt$, quindi
$$H=\frac{v}{r}=\frac{1}{r} \frac{dr}{dt}=\frac{r_{0}}{r} \frac{da}{dt}=\frac{1}{a} \frac{da}{dt}$$
Ma allora anche $H$ deve essere dipendente dal tempo: chiamiamo $H(t)$ il **parametro di Hubble**, che vale
$$\boxed{H(t)=\frac{1}{a} \frac{da}{dt}}$$
e abbiamo che $H(t_{0})=H_{0}$, ossia la [[Legge di Hubble|costante di Hubble]] non è altro che il valore del parametro di Hubble oggi. Dato che $H$ dipende dal tempo, lo fa anche $\rho_{c}$. Definiamo allora la densità critica *attuale* e il parametro di densità *attuale*
$$\rho_{C,0}=\frac{3H_{0}^{2}}{8\pi G}, \quad \Omega_{m}=\frac{\rho(t_{0})}{\rho_{C,0}}$$

Proviamo a calcolare l'energia del tracciante a $t_{0}$ :
$$E=\frac{1}{2}mH_{0}^{2}r_{0}^{2}- \frac{Gm}{r_{0}} \frac{4\pi}{3}r_{0}^{3}\rho(t_{0})=\frac{1}{2}mH_{0}^{2}r_{0}^{2}- \frac{1}{2}mH_{0}^{2}r_{0}^{2}\left(\frac{2}{mH_{0}^{2}r_{0}^{2}} \frac{Gm}{r_{0}} \frac{4\pi}{3}r_{0}^{3}\rho_{0}\right)=$$
$$=\frac{1}{2}mH_{0}^{2}r_{0}^{2}(1-\Omega_{m})$$
Allora
$$\frac{1}{2}mH^{2}r^{2}- \frac{Gm}{r}\rho \frac{4\pi}{3}r^{3}=\frac{1}{2}mH_{0}^{2}r_{0}^{2}(1-\Omega_{m})$$
$$\frac{H^{2}}{H_{0}^{2}}=\frac{\rho}{\rho_{C,0}}=\frac{1}{a^{2}}(1-\Omega_{m})$$
Da cui si evince che la densità va come
$$\rho\propto r^{-3}\propto a^{-3}$$
e quindi
$$\rho=\rho_{0}a^{-3}$$
Allora possiamo riscrivere l'ultima equazione come
$$\boxed{\frac{H^{2}}{H_{0}^{2}}=\frac{\Omega_{m}}{a^{3}}+ \frac{1-\Omega_{m}}{a^{2}}}$$
che è la **seconda equazione di Friedmann**, che proviene dalla componente spaziale delle equazioni di Einstein. È valida nel caso l'universo sia dominato dalla materia.

Questa equazione è risolvibile analiticamente e si ottiene un'equazione simile ad un cicloide. Si hanno tre diverse soluzioni
1. $\Omega_{m}<1$: l'universo non è legato e si espande in eterno, seguendo una legge simile ad un cicloide ma con trigonometria iperbolica.
2. $\Omega_{m}=1$: l'universo è critico, detto [[universo di Einstein-de Sitter]]. In questo caso, $a(t)=(t/t_{0})^{2/3}$ e l'espansione è ancora eterna.
3. $\Omega_{m}>1$: la soluzione è un cicloide, l'universo è legato e eventualmente collassa su sé stesso.

Questo ci dice dunque che, in presenza di sola materia, $\Omega_{m}$ decide da solo il destino dell'universo. Questo ci permette di calcolare l'età dell'universo con maggiore precisione: se la gravità rallenta l'espansione dell'universo, le [[galassia|galassie]] passate recedevano più velocemente che oggi. In questo caso, il tempo di Hubble $t_{0}=t_{H}=H_{0}^{-1}$, che è valido nell'ipotesi di velocità di espansione costante, sovrastima di molto l'età misurata dell'Universo. Questa sovrastima diventa più grave maggiore è il rallentamento, ossia maggiore è la densità dell'universo, ossia maggiore è $\Omega_{m}$.

Per $\Omega_{m}\ll1$, quindi piccoli, $t_{0}$ si avvicina a $t_{H}$, mentre per $\Omega_m=1$ si ha $a(t)=(t/t_{0})^{2/3}$ e allora
$$H(t)=\frac{1}{a} \frac{da}{dt}=\frac{2}{3t} \quad \Rightarrow \quad t_{0} = \frac{2t_{H}}{3}$$
#### Universo di radiazione
È possibile ripercorrere i passaggi per riottenere al seconda equazione per un universo dominato da [[radiazione]]. Basta notare che la massa $M$ nella sfera è la massa energia dei [[Photon|fotoni]] $M=\rho_{\gamma}V$, con $\rho_{\gamma}$ la densità di massa dei fotoni[^2]. Dato che questa va come $a(t)^{-4}$ e $V\propto a(t)^{3}$, la massa "diminuisce" col tempo per via dell'espansione come
$$M= \frac{M_{1}}{a}$$
dove 1 e 2 sono due tempi qualunque. Da qui si può ottenere
$$\frac{H^{2}}{H_{1}^{2}}=\frac{\Omega_{r}}{a^{4}}+ \frac{1-\Omega_{r}}{a^{2}}$$
dove abbiamo definito $\Omega_{r}$ il **parametro di densità di radiazione** al tempo $t_{1}$. Se $a\ll1$, il secondo termine è trascurabile e rimane
$$\frac{H^{2}}{H_{1}^{2}}\simeq\frac{1}{a^{4}}$$
quindi l'universo è circa piatto ($\Omega\sim1$). La soluzione di questa equazione dà
$$a(t)=\left(\frac{t}{t_{1}}\right)^{1/2} \quad \Rightarrow \quad \rho_{\gamma}\propto a(t)^{-2}$$
Se i fotoni sono in equilibrio termico e hanno lo [[Spettro (astrofisica)|spettro]] di un [[corpo nero]], allora $\rho_{\gamma}c^{2}=\sigma T_{\gamma}^{4}$ con $\sigma$ [[Stefan-Boltzmann constant]], quindi $T_{\gamma}\propto t^{-1/2}$ e $T_{\gamma}\propto a(t)^{-1}$:
### Terza equazione
Torniamo all'inizio, con l'osservazione di una galassia tracciante. Deve valere il [[Principi della termodinamica#Primo principio|primo principio della termodinamica]]:
$$dU+PdV=dE$$
Supponiamo che l'universo sia permeato di una componente di densità di energia pari a $\rho c^{2}$ e pressione $P$. Per un sistema adiabatico, si ha $dE=0$ e quindi $dU+PdV=0$. Considerato che il volume dell'universo si espande con il fattore di scala $V\propto a(t)^{3}$ e ponendo
$$U=\rho c^{2}V=\rho c^{2}a^{3}r_{0}^{3} \quad \Rightarrow \quad dU=\rho c^{2}dV$$
Ma $r_{0}^{3}$ della $\rho$ si semplifica con quello del volume $dV$, quindi possiamo già toglierlo per semplicità $U=\rho c^{2}a^{3}$. Allora vale anche $V=a^{3}$. Notando le derivate temporale con il punto, abbiamo
$$\dot{U}+P\dot{V}=0$$
$$\dot{\rho}c^{2}a^{3}+3\rho c^{2}a^{2}\dot{a}+P3a^{2}\dot{a}=0$$
$$\dot{\rho}+3H\rho+3H \frac{P}{c^{2}}=0$$
Raccogliendo
$$\boxed{\dot{\rho}+3H\left(\rho+\frac{P}{c^{2}}\right)=0}$$
che è la **terza equazione di Friedmann**, che proviene dalla conservazione dell'energia.
Nel caso della materia di $P=0$, che vale in casi non relativistiche, vale
$$\frac{\dot{\rho}}{\rho}+3 \frac{\dot{a}}{a}=0$$
$$\frac{d\ln\rho}{dt}=\frac{d\ln a^{-3}}{dt} \quad\Rightarrow \quad \rho_{m}\propto a^{-3}$$
Nel caso della radiazione di $P=\frac{1}{3}\rho c^{2}$, che è la [[pressione di radiazione]], abbiamo
$$\dot{\rho}_{\gamma}+4 \frac{\dot{a}}{a}=0 \quad\Rightarrow\quad \rho_{\gamma}\propto a^{-4}$$

Va notato che l'energia della radiazione *diminuisce* mentre viaggia perché la sua lunghezza d'onda diminuisce come $a^{-1}$. Ciò giustifica il fatto che, nel caso della pressione di radiazione, la densità di energia diminuisce come $a^{-4}$ e non $a^{-3}$. Un modo vago ma intuitivo per pensarci è che è come un gas in espansione: più il gas si espande, più diminuisce la temperatura.
### Prima equazione
Prendiamo la densità di materia
$$\frac{\Omega_{0}}{a^{3}}=\frac{\rho_{0}a^{-3}}{\frac{3H_{0}^{2}}{8\pi G}}=\frac{8\pi G}{3} \frac{1}{H_{0}^{2}}\rho$$
$$\left(\frac{\dot{a}}{a}\right)^{2}=\frac{8\pi G}{3}\rho+ H_{0}^{2}\frac{1-\Omega_{0}}{e^{2}}$$
$$\dot{a}^{2}=\frac{8\pi G}{3}\rho a^{2}+H_{0}^{2}(1-\Omega_{0})$$
$$2\dot{a}\ddot{a}=\frac{8\pi G}{3}(\dot{\rho}a^{2}+2a\dot{a}\rho)$$
$$\boxed{\frac{\ddot{a}}{a}=- \frac{4\pi G}{3}\left(\rho+3 \frac{P}{c^{2}}\right)}$$
che è la **prima equazione di Friedmann**, che viene dalla componente temporale delle equazioni di Friedmann. Ci dice che la derivata seconda del fattore di scala è sempre negativa, ossia l'universo è in costante decelerazione o, in altre parole, sta cadendo su se stesso.

[^1]: Possiamo immaginare questo oggetto come una [[galassia]], ma è un qualcosa di astratto.
[^2]: La densità di energia è equivalente alla densità di massa per l'[[equivalenza massa-energia]]. Se $u$ è la densità di energia, quella di massa è $\rho=u/c^{2}$, che quindi ha senso anche per [[Particella|particelle]] prive di massa.