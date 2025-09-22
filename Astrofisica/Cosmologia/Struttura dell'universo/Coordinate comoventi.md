---
wiki-publish: true
aliases:
  - distanza comovente
  - distanza di luminosità
  - distanza di diametro
---
Le **coordinate comoventi** sono un sistema di riferimento che annulla l'effetto dell'[[Espansione dell'universo]]. In altre parole, due oggetti misurati in coordinate comoventi restano fermi rispetto l'un l'altro se l'unico loro moto è quello del trascinamento di Hubble. In queste coordinate, gli unici movimenti misurati sono i *moti peculiari*.

Consideriamo una sorgente cosmologica a [[Redshift]] $z$. Un [[Photon]] che arriva a noi da essa è in ritardo per via della limitatezza della [[velocità della luce]]. Nel frattempo, la sorgente si è allontanata per l'espansione dell'universo. Senza le coordinate comoventi la velocità della sorgente è data dalla [[Legge di Hubble]]:
$$cz=H_{0}d+v_{0}$$
con $v_{0}$ la velocità peculiare e $d$ la distanza.

Definiamo $r(z)$ la coordinata radiale della sorgente. Per un [[Curvatura dell'universo|universo piatto]], si può porre $r(z)$ come uguale alla distanza fisica tra noi e la sorgente misurata ad un tempo $t_{0}$, detta **distanza comovente** $d_{C}$. Nessuna delle due è misurabile in pratica.

Possiamo definire la **distanza di luminosità** $d_{L}$ usando il [[Flusso energetico|flusso]] che osserviamo:
$$f=\frac{L}{4\pi d_{L}^{2}}$$
Dato che l'espansione sia rallenta l'arrivo dei fotoni che ne diminuisce l'energia, il flusso risulta inferiore a quello in mancanza di espansione di un fattore $(1+z)^{2}$. Allora
$$d_{L}=(1+z)r(z)$$
Delle distanze, questa è la più comoda.

Si definisce **distanza di diametro** la distanza per la quale vale la relazione $\Delta \theta=D_{0}/d_{D}$, derivata dal fatto che l'espansione causi l'allontanamento della sorgente di $a(t_{0})/a(t)=(1+z)$ e dal fatto che l'espansione lasci gli angoli invariati. Si trova
$$d_{D}=\frac{r(z)}{1+z}$$
### Espansione della distanza di luminosità
Possiamo espandere in [[Taylor series|serie di Taylor]] la funzione $d_{L}(z)$. Al primo termine ritroviamo la legge di Hubble-Lemaitre. Dal secondo in poi abbiamo i termini non lineari, che diventano rilevanti per redshift molto alto ($z>1$). Infatti, per [[Candela standard|candele standard]] molto lontane, il diagramma di Hubble comincia a pendere. Al secondo termine troviamo
$$d_{L}=\frac{1}{H_{0}}c\left(z- \frac{1-q_{0}}{2}z^{2}+\ldots\right)$$
dove $q_{0}$ è un parametro detto **parametro di decelerazione**. È legato alla derivata seconda del fattore di scala come
$$q_{0}=- \frac{d^{2}a}{dt^{2}}(t_{0})\left[\frac{da}{dt}(t_{0})\right]^{-2}$$
Nei modelli di Friedmann-Robertson-Walker si trova
$$q_{0}=\frac{\Omega_{m}}{2}$$
teoricamente, allora, misurando la distanza di oggetti molto lontani è possibile trovare la percentuale di materia dell'universo.

---

Nelle coordinate comoventi il termine $H_{0}d$ deve svanire. Dunque la distanza comovente può essere calcolata con
$$D_{C}(z)=\frac{c}{H_{0}} \int_{0}^{z} \frac{dz'}{E(z')}$$
con
$$E(z')=\frac{H(z)}{H_{0}}=\sqrt{\Omega_{m}(1+z)^{3}+\Omega_{\kappa}(1+z)^{2}+\Omega_{\Lambda}}$$
Le coordinate comoventi sono dipendenti dalla cosmologia che si usa. In particolare, la cosmologia serve per fare il passaggio da redshift a distanza. Avere una cosmologia significa definire alcuni parametri cosmologici: $H_{0}$, $\Omega_{m}$, $\Omega_{\Lambda}$ e $\Omega_{\kappa}$, con il vincolo che $\Omega_{m}+\Omega_{\Lambda}+\Omega_{\kappa}=1$.