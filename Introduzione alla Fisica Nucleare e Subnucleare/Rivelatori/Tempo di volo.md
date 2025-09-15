---
wiki-publish: true
aliases:
  - time of flight
  - TOF
---
Il **tempo di volo** (**time of flight**, o **TOF**) è il tempo impiegato da una [[Particle]] per spostarsi da un [[Detector]] ad un altro. Si tratta di una misura utile per determinare la vita media di una particella, il tempo che ci impiega per coprire la distanza (e dunque la velocità), o anche per discriminare tra due particelle di masse diverse ma pari impulso (che hanno diversa velocità e quindi diverso TOF).

I due contatori (partenza e arrivo) devono essere posti ad una distanza $L$ tale da rendere l'errore di misura temporale piccolo. Se $TOF=t_{2}-t_{1}$, allora
$$\frac{\sigma _\text{TOF}}{TOF}=\sigma _\text{TOF} \frac{v}{L}\quad\Rightarrow \quad \frac{\sigma_{v}}{v}=\frac{\sigma _\text{TOF}}{TOF}$$
Se i due rivelatori sono identici si ha $\sigma_{t_{1}}=\sigma_{t_{2}}=\sigma_{t}$, da cui
$$\sigma _\text{TOF}=\sqrt{ 2 }\sigma_{t}\quad\Rightarrow \quad \frac{\sigma _\text{TOF}}{TOF}=\sqrt{ 2 } \frac{v}{L}\sigma _{t}$$
La velocità $v$ è fuori dal nostro controllo e $\sigma_{t}$ dipende dall'architettura dei rivelatori. La distanza $L$ è la più semplice da variare: qui distanti sono i rivelatori, migliore è la misura.