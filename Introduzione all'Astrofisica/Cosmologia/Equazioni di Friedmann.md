Le **equazioni di Friedmann** sono un insieme di equazioni che spiegano l'[[espansione dell'universo]] in un modello cosmologico omogeneo e isotropo.

![[Modello Friedmann|center]]

Consideriamo un oggetto che vediamo allontanarsi da noi: chiamiamolo "galassia", anche se va considerato come un oggetto "tracciante" con massa $m$ piccola. In ogni dato istante è a distanza $r$ da noi e si sta allontanando a velocità $v$. Allora
$$v=Hr$$
con $H$ un numero, non necessariamente costante.
Consideriamo una densità di massa $\rho$ tra noi e l'oggetto: allora la massa in quella sfera è
$$M=\frac{4}{3}\pi r^{3}\rho$$
L'energia del tracciante è
$$E=\frac{1}{2}mv^{2}- \frac{GmM}{r}=\text{cost.}$$
dato da energia cinetica e potenziale gravitazionale della massa tra noi e l'oggetto. Ci sono due casi fondamentali: se l'energia totale è negativa, l'oggetto è in un sistema gravitazionale legato e prima o poi torna a cadere verso di noi: nel caso della massa di tutto l'universo questo evento si chiama *Big Crunch*; se è maggiore di zero, va avanti all'infinito. Consideriamo il caso limite $E=0$, chiamata *energia critica*. Deve essere
$$\frac{1}{2}mv^{2}- \frac{GmM}{r}=0$$
Sostituendo $v$ ed $M$ 
$$\frac{1}{2}H^{2}r^{2}=\frac{G}{r} \frac{4\pi}{3}r^{3}\rho \rightarrow \frac{1}{2}H^{2}=\frac{4\pi}{3}G \rho$$
Definiamo la *densità critica* come
$$\rho_{C}=\frac{3H^{2}}{8\pi G}$$
Consideriamo $t=\frac{1}{\sqrt{G\rho}}$, ossia il *tempo dinamico* di un sistema autogravitante, ossia il tempo che il sistema ci mette a collassare su se stesso in mancanza di equilibrio idrostatico. Quindi abbiamo che $H^{-1}$ ha le dimensioni di un tempo dinamico. Utilizzando $H^{-1}=9.78\times10^{9}h^{-1}yr$ troviamo che la densità critica è $\rho_{C}=1.88\times10^{-29}h^{2}g\;cm^{-3}$, che è la densità di un universo *critico*. Se l'universo ha più densità di così (e quindi più massa), è destinato a collassare in un Big Crunch. Se è più basso, si espande all'infinito. Con misure approssimate, si trova che considerando tutte le stelle stimate dell'universo, questo avrebbe densità nell'ordine delle $10^{-31}$, ossia un centesimo della soglia critica.

Possiamo esprimere la densità critica in altre unità, come $\rho_{C}=2.78\times10^{11}h^{2}M_{\odot}Mpc^{-3}$. Sappiamo che l'ammasso di Andromeda ha una densità media circa 10 volte più alta.

Definiamo cos'è $H$. Le misure umane dell'universo possono essere assunte come tutte fatte nello stesso istante rispetto all'età dell'universo: chiamiamolo $t_{0}$. Prendiamo una distanza $r_{0}$ e chiamiamo la quantità $a(t)=\frac{r}{r_{0}}$ *fattore di scala*. Abbiamo che $a(t_{0})=1$. Riprendiamo $v=Hr$, ma è anche vero che $v=\frac{dr}{dt}$, quindi
$$v=\frac{dr}{dt}=r_{0} \frac{da}{dt}=Hr_{0}a(t)$$
usando che $r=r_{0}a(t)$. La velocità può quindi essere espresso in funzione del fattore di scala. Ma allora anche $H$ deve essere dipendente dal tempo: chiamiamo $H(t)$ il **parametro di Hubble**, che vale
$$H(t)=\frac{1}{a} \frac{da}{dt}$$
e abbiamo che $H(t_{0})=H_{0}$, ossia la [[costante di Hubble]] non è altro che il valore del parametro di Hubble oggi. Definiamo
$$\rho_{C,0}=\frac{3H_{0}^{2}}{8\pi G}$$
Allora posso definire
$$\Omega_{m}=\frac{\rho(t_{0})}{\rho_{C,0}}$$
che chiamo **parametro di densità**, dove la $m$ al pedice sta per materia.

Proviamo a calcolare l'energia dell'universo a $t_{0}$ 
$$E=\frac{1}{2}mH_{0}^{2}r_{0}^{2}- \frac{Gm}{r_{0}} \frac{4\pi}{3}r_{0}^{2}\rho(t_{0})=\frac{1}{2}mH_{0}^{2}r_{0}^{2}- \frac{1}{2}mH_{0}^{2}r_{0}^{2}\left(\frac{2}{mH_{0}^{2}r_{0}^{2}} \frac{Gm}{r_{0}} \frac{4\pi}{3}r_{0}^{3}\rho_{0}\right)=$$
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
che è la **seconda equazione di Friedmann**, che proviene dalla componente spaziale delle equazioni di Einstein.

---

Torniamo all'inizio, con l'osservazione di una galassia tracciante. Deve essere
$$dU+PdV=0$$
Il potenziale va espresso in termini della relatività generale
$$U=\rho c^{2}a^{3}r_{0}^{3}$$
con $\rho$ densità di energia nel senso della relatività generale (dove massa = energia). Ma $r_{0}^{3}$ si semplifica con quello del volume $dV$, quindi possiamo già toglierlo per semplicità $U=\rho c^{2}a^{3}$. Allora vale anche $V=a^{3}$. Notando le derivate temporale con il punto, abbiamo
$$\dot{U}+P\dot{V}=0$$
$$\dot{\rho}c^{2}a^{3}+3\rho c^{2}a^{2}\dot{a}+P3a^{2}\dot{a}=0$$
$$\dot{\rho}+3H\rho+3H \frac{P}{c^{2}}=0$$
Raccogliendo
$$\boxed{\dot{\rho}+3H\left(\rho+\frac{P}{c^{2}}\right)=0}$$
che è la **terza equazione di Friedmann**, che proviene dalla conservazione dell'energia.
Nel caso di $P=0$, che vale approssimativamente per particelle non relativistiche (cioè con velocità termiche molto minori a quelle della luce), vale
$$\frac{\dot{\rho}}{\rho}+3 \frac{\dot{a}}{a}=0$$
$$\frac{d\ln\rho}{dt}=\frac{d\ln a^{-3}}{dt} \rightarrow \rho_{m}=\rho_{m,0}a^{-3}$$
Prendendo il caso $P=\frac{1}{3}\rho c^{2}$, che la pressione di radiazione, abbiamo
$$\dot{\rho}_{\gamma}+4 \frac{\dot{a}}{a}=0 \rightarrow \rho_{\gamma}=\rho_{\gamma,0}a^{-4}$$
Consideriamo l'energia di un elettrone $e=h\nu=\frac{hc}{\lambda}$. Esprimiamo la lunghezza d'onda in base al fattore di scala dell'universo
$$\frac{\lambda_{oss}}{a(t_{oss})}=\frac{\lambda_{em}}{a(t_{em})}$$
ossia la lunghezza d'onda osservata differisce da quella emessa in funzione del fattore di scala ai tempi di osservazione e di emissione. Se consideriamo il [[Redshift]], abbiamo
$$\boxed{1+Z= \frac{1}{a(t_{em})}}$$
ossia possiamo calcolare il fattore scala dal redshift, che è misurabile. Dunque il fattore di scala è un [[Osservabile]].

Va notato che l'energia degli elettroni *diminuisce* mentre viaggia perché la sua lunghezza d'onda diminuisce come $a^{-1}$. Ciò giustifica il fatto che, nel caso della pressione di radiazione, la densità di energia diminuisce come $a^{-4}$ e non $a^{-3}$. Un modo vago ma intuitivo per pensarci è che è come un gas in espansione: più il gas si espande, più diminuisce la temperatura.

---

Prendiamo la densità di materia
$$\frac{\Omega_{0}}{a^{3}}=\frac{\rho_{0}a^{-3}}{\frac{3H_{0}^{2}}{8\pi G}}=\frac{8\pi G}{3} \frac{1}{H_{0}^{2}}\rho$$
$$\left(\frac{\dot{a}}{a}\right)^{2}=\frac{8\pi G}{3}\rho+ H_{0}^{2}\frac{1-\Omega_{0}}{e^{2}}$$
$$\dot{a}^{2}=\frac{8\pi G}{3}\rho a^{2}+H_{0}^{2}(1-\Omega_{0})$$
$$2\dot{a}\ddot{a}=\frac{8\pi G}{3}(\dot{\rho}a^{2}+2a\dot{a}\rho)$$
$$\boxed{\frac{\ddot{a}}{a}=- \frac{4\pi G}{3}\left(\rho+3 \frac{P}{c^{2}}\right)}$$
che è la **prima equazione di Friedmann**, che viene dalla componente temporale delle equazioni di Friedmann. Ci dice che la derivata seconda del fattore di scala è sempre negativa, ossia l'universo è in costante decelerazione o, in altre parole, sta cadendo su se stesso.