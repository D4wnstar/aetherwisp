---
aliases:
  - formula di Bethe-Bloch
---
Lo **stopping power** $S$ è la capacità di un materiale di rallentare una [[particella]] che ci passa attraverso mediante l'interazione con la materia, diminuendo la sua energia cinetica. Matematicamente, è la media della diminuzione di energia $E$ della particella per unità di spazio $x$, inteso come lo spazio occupato da materia entro il quale passa la particella:
$$S(E)=- \left\langle\frac{dE}{dx}\right\rangle$$
per un sistema del tipo
![[Schema Rivelatore generico|40%|center]]
L'esatto valore della diminuzione di energia fluttua con una distribuzione gaussiana, come si trova anche sperimentalmente. L'esatta distribuzione in realtà non è perfettamente gaussiana (si sono osservate anche distribuzione poissoniane), ma per il [[teorema del limite centrale]], avendo una statistica sufficientemente ampia, converge ad una gaussiana.

In fisica nucleare e delle particelle, si può misurare lo stopping power di un materiale usando la **formula di Bethe-Bloch**:
$$S(E)=- \frac{dE}{dx}=0.15 \frac{Z}{A}\rho \frac{z^{2}}{\beta^{2}}\left[\ln\left(\frac{2\beta^{2}\gamma^{2}mc^{2}E_{M}}{I^{2}}\right)-2\beta^{2}-\delta(\gamma)\right]$$
o la sua forma più semplice che trascura alcune correzioni
$$S(E)=- \frac{dE}{dx}=\underbrace{4\pi r^{2}_{e}mc^{2}}\limits_{1} \underbrace{\frac{N_{a}Z\rho}{A} \frac{z^{2}}{\beta^{2}}}\limits_{2}\underbrace{\ln\left(\frac{mc^{2}\beta^{2}\gamma^{2}}{lv}\right)}\limits_{3}$$
dove
- $Z$ è il [[Atomo|numero atomico]].
- $A$ è il [[Atomo|numero di massa atomica]].
- $\beta$ e $\gamma$ rappresentano il [[limite relativistico]].
- $\rho$ è la densità del materiale.
- $z$ è la carica della particella.
- $E_{M}$ è l'energia a riposo dell'[[elettrone]].
- $I$ è il *potenziale di eccitazione*.

Il $0.15$ proviene dal termine di *perdita di energia per ionizzazione* $4\pi mc^{2}N_{A}r_{e}^{2}=0.3$ [[Elettronvolt|MeV]] cm$^{2}$/g diviso per due, con $N_{A}$ il [[numero di Avogadro]]. Il termine logaritmico, che cresce lentamente, diventa grande solo per $\gamma$ molto grandi, ossia in regimi ultrarelativistici.

Dato che $\rho$ è il parametro più semplice da manipolare, è comune usare la formula di Bethe-Bloch in una forma alternativa che porta fuori il termine di densità. Definendo $X=\rho x$, vale
$$- \frac{dE}{dX}=\frac{1}{\rho} \frac{dE}{dx}$$
dove $[X]=g/cm^2$. Questa forma non rappresenta più la perdita di energia per distanza oltrepassata nel materiale, bensì una distanza pesata per la densità.

Le uniche due proprietà intrinseche della particella da cui la formula dipende sono $z$ e $m$, il che significa che il comportamento in termini di *stopping power* di un materiale non distingue tra particelle con stessa massa e carica. La massa è anche presente solo nel termine logaritmico, il che vuol dire che è rilevante solo in casi ultrarelativistici. Per velocità minori, è importante solo la carica, dato che la variazione del logaritmo può essere trascurata[^1]. Nel caso $z=1$, la decaduta di energia ha una forma del genere:

![[Schema Stopping power per z=1|80%|center]]
*L'asse $x$ è in scala log10*

Lo stopping power ha un minimo, per poi risalire nuovamente per effetti relativistici. Una particella con diminuzione di energia minima viene detta *minimum ionizing particle* (o *MIP*) e per tutte le MIP vale che $\beta\gamma\simeq3$.

[^1]: Dato che si tratta di un prodotto, il logaritmo in sé non può essere trascurato (bisognerebbe avere una somma). È però possibile trascurare la variazione del logaritmo e quindi rimanere con una costante.