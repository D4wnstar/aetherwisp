---
wiki-publish: true
aliases:
  - tempo di caduta libera
---
Il **tempo dinamico** $t_{din}$, anche **tempo di caduta libera** o di ***free fall***, di una [[stella]] (o qualunque nube di gas) è il tempo che un elemento di massa fermo alla superficie (a distanza $R$ dal centro della stella) impiega per cadere fino al centro della stella, nel caso ipotetico che la massa $M_{s}$ sia tutta concentrata in un punto al centro:
$$t_{din}=\int_{R}^{0} \frac{dr}{v}=\sqrt{\frac{3\pi}{32G\bar{\rho}}}$$
con $G$ la [[Gravitational constant]] e $\bar{\rho}$ la densità media della stella.

Esistono diverse definizioni del tempo dinamico, ma tutte sono della forma $\text{cost.}/\sqrt{G\bar{\rho}}$. Con questa definizione, il tempo dinamico del Sole è di circa mezz'ora.
### Derivazione
Cominciamo considerando l'energia [[Gravity|potenziale gravitazionale]] $U$ di una stella in forma differenziale:
$$dU=- \frac{GM(r_{0})}{r_{0}}dm$$
dove $M(r_{0})$ è la massa della [[Stella|stella]] entro il raggio $r_{0}$ e $dm$ è l'elemento di massa che compone la stella. In questa formula stiamo implicitamente assumendo che la massa sia contenuta tutta in un punto al centro della stella, che è una buona approssimazione per quanto riguarda la forza gravitazionale.

Dall'equazione sopra si può ricavare
$$\frac{1}{2}\left( \frac{dr}{dt} \right)^{2}= \frac{GM(r_{0})}{r}- \frac{GM(r_{0})}{r_{0}}$$
che scritto in un altro modo è
$$v=\sqrt{2GM_{s} \left(\frac{1}{r} - \frac{1}{R}\right)}$$

Sapendo la velocità di caduta, possiamo determinare il tempo per cadere da $r_{0}$ a 0[^1]:
$$t_{din}=\int_{0}^{t_{din}}dt=\int_{r_{0}}^{0} \frac{dr}{v}=-\int_{r_{0}}^{0}2GM(r_{0})\left( \frac{1}{r}- \frac{1}{r_{0}} \right)^{- \frac{1}{2}}dr=$$
$$=\left( \frac{r_{0}^{3}}{2GM(r_{0})} \right)^{\frac{1}{2}}\underbrace{\int_{0}^{1}\left( \frac{x}{1-x} \right)^{\frac{1}{2}}dx}\limits_{\frac{\pi}{2}}=\sqrt{\frac{3\pi}{32G\rho}}$$

[^1]: Per calcolare l'integrale si può anche porre $\frac{r}{R}=\sin^{2}\theta$ e poi integrare $\theta$ tra 0 e $\pi$.