Le **equazioni di Friedmann** sono un insieme di equazioni che spiegano l'[[espansione dell'universo]] in un modello cosmologico omogeneo e isotropo.

![[Modello Friedmann|center]]

Consideriamo un oggetto che vediamo allontanarsi da noi: chiamiamolo "galassia", anche se va considerato come un oggetto "tracciante" con massa $m$ trascurabile. In ogni dato istante è a distanza $r$ da noi e si sta allontanando a velocità $v$. Allora
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
che è la **seconda equazione di Friedmann**.