---
wiki-publish: true
---
Uno **spettrometro magnetico** è uno strumento utilizzato per misurare la quantità di moto di una [[Particle]] [[Electric charge|carica]] mediante la curvatura indotta da un [[Magnetic field|campo magnetico]]. Consiste tipicamente in un magnete ed una serie di [[Rivelatore|rivelatori]] per tracciare il moto della particella.

Il moto è determinato dalla [[Lorentz force|forza di Lorentz]] e dalla [[Newton's laws|seconda legge di Newton]] nel caso del [[Rotation#Circular motion|moto circolare uniforme]]:
$$|\vec{F}|=q|\vec{v}\times \vec{B}|=\frac{mv^{2}}{\rho}$$
con $\rho$ il raggio di curvatura della particella. Invertendo
$$p=q\rho B=0.3\rho B$$
Avendo nota la carica della particella da misurare e sapendo il campo magnetico per costruzione, basta misurare il raggio di curvatura per estrarre il momento.

Per misurare il raggio di curvatura, la geometria ci obbliga a rivelare le coordinate di almeno tre punti dove passa la particella (in rosso nella figura). Per piccole deflessioni, questo è sufficiente. 

![[Schema Metodo della sagitta|80%|center]]

Misuriamo quindi la sagitta $s$:
$$s=\rho-\rho \cos \frac{\theta}{2}=\rho\left( 1-\cos \frac{\theta}{2} \right)=\rho\left[ 1-\left( \cos ^{2} \frac{\theta}{4} -\sin ^{2} \frac{\theta}{4}\right) \right]=$$
$$=\rho\left[ 1-\left( 1-2\sin ^{2} \frac{\theta}{4} \right) \right]=2\rho \sin ^{2} \frac{\theta}{4}$$
Per angoli piccoli si ha $\sin\theta \simeq \theta \simeq L/\rho$, da cui
$$s\simeq 2\rho\left( \frac{L}{4\rho} \right)^{2}=\frac{L^{2}}{8\rho}$$
e sostituendo $\rho$ abbiamo
$$s=\frac{0.3}{8} \frac{BL^{2}}{p}\quad \to \quad p=\frac{0.3}{8} \frac{BL^{2}}{s}$$
La propagazione degli errori dà
$$\sigma_{p}=\frac{0.3}{8} \frac{BL^{2}}{s^{2}}\sigma_{s}\quad\text{e}\quad \frac{\sigma_{p}}{p}=\frac{\sigma_{s}}{s}=\frac{8}{0.3} \frac{p}{BL^{2}}\sigma_{s}$$
quindi il potere risolutivo dello spettrometro magnetico è proporzionale alla risoluzione spaziale e dipende direttamente da $BL^{2}$, che sono i parametri che caratterizzano lo spettrometro. La risoluzione peggiora linearmente con l'aumentare del momento da misurare. La lunghezza $L$ dello strumento è più importante del campo magnetico $B$ per migliorare la risoluzione per via della dipendenza quadratica.

Se misuriamo la sagitta a partire dai tre punti $x_{1}$, $x_{2}$ e $x_{3}$ in rosso, abbiamo
$$s=x_{2} - \frac{x_{1}+x_{3}}{2}\quad\Rightarrow \quad \sigma_{s}=\sqrt{ \frac{3}{2} }\sigma_{x}$$
da cui
$$\frac{\sigma_{p}}{p}=\sqrt{ \frac{3}{2} } \frac{8}{0.3} \frac{p}{BL^{2}}\sigma_{x}$$
assumendo che i tre rivelatori abbiamo la stessa incertezza $\sigma_{x}=\sigma_{x1}=\sigma_{x2}=\sigma_{x3}$.