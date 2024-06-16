Il **teorema del viriale** ci dà una relazione tra l'energia cinetica totale e l'energia potenziale totale di un sistema discreto di [[particella|particelle]] legate fra loro da una [[forza conservativa]]. Questo si applica, ad esempio, a sistemi di gas perfetto in equilibrio idrodinamico, orbite Kepleriane e il moto di [[Stella|stelle]] in [[Ammasso stellare|ammassi]] o [[Galassia|galassie]].

Se l'energia potenziale è della forma $V(r)=ar^{n}$, con $r$ la distanza tra le particelle, ha la forma
$$2K+n\Omega=0$$
dove $K$ è l'energia cinetica totale di tutte le particelle e $\Omega$ è l'energia potenziale totale.

Per il [[Interazione gravitazionale|potenziale gravitazionale]], si ha $\Omega\sim r^{-1}$, quindi vale
$$2K+\Omega=0$$
### Derivazione
Consideriamo una sfera composta da un grande numero di particelle sottoposta ad una certa pressione che dipende dal raggio (per esempio, una stella). Partiamo dall'[[Equazioni della struttura stellare#Equilibrio idrostatico|equazione di equilibrio idrostatico]]:
$$dP=-\frac{G\rho(r)M(r)}{r^{2}}{dr}$$
e moltiplichiamola $4\pi r^{3}$:
$$4\pi r^{3}dP=-4\pi rG\rho(r)M(r){dr}$$
e ora integriamola da una parte dalla pressione centrale $P_{c}$ a quella superficiale $P_{s}$, dall'altra da 0 al raggio della sfera $R$:
$$\int_{P_{c}}^{P_{s}}4\pi r^{3}dP=-\int_{0}^{R}4\pi rG\rho(r)M(r)dr$$
Il volume di una sfera è $V(r)=4/3 \pi r^{3}$, quindi al primo membro $4\pi r^{3}=3V(r)$. Al secondo, usiamo l'[[Equazioni della struttura stellare#Equazione di continuità di massa|equazione di continuità di massa]] per una sfera
$$\rho(r)4\pi r^{2}dr=dM(r)$$
da cui
$$3\int_{P_{c}}^{P_{s}}V(r)dP=-\int_{0}^{M_{s}} \frac{GM(r)}{r}dM$$
con $M_{s}$ la massa della stella alla superficie, che non è altro che la massa totale della stella $M_{s}=M$. Il secondo termine ora è il potenziale gravitazionale totale della stella $\Omega$. Il primo termino può essere [[Integrazione per parti|integrato per parti]]:
$$PV|_{c}^{s}-\int_{c}^{s}PdV=-\int_{c}^{s}PdV$$
perché $PV$ si annulla sia al centro (volume nullo) che alla superficie (pressione nulla). Allora usando l'[[equazione di stato dei gas perfetti]] si ha
$$-3\int_{c}^{s}PdV=-2\int_{c}^{s} \frac{3}{2}nk_{B}TdV=-2K$$
con $K$ l'energia cinetica totale delle particelle. Abbiamo trovato quindi
$$2K+\Omega=0$$
