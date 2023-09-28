## Primo principio
$$dE = dQ - PdV\quad\quad\mbox{con }dQ = TdS$$
(in forma differenziale). $E$ è l'energia del sistema, $Q$ è il [[calore]], $P$ è la [[pressione]], $V$ è il volume e $S$ è l'[[entropia]]. La forma finita è
$$\Delta E=\Delta Q-\Delta W$$

Si ha che
$$\boxed{S(B) - S(A) = \int_{\gamma_{rev}} \frac{dQ}{T}}$$
con $\gamma_{rev}$ un cammino reversibile da $A$ a $B$. Questo ci dà l'entropia come funzione di stato. Ora prendo la distanza da $A$ a $B$ infinitesima e trovo che 
$$dS = \frac{dQ}{T}$$
da cui si ottiene
$$dE = TdS - PdV$$
ossia l'energia è funzione di entropia e volume: $E(S,V)$.

## Secondo principio

Il secondo principio può essere scritto come
$$\boxed{S(B)-S(A)\geq \int_{A}^{B}\frac{dQ}{T}}$$
In questo caso, il cammino è generico, a differenza del primo principio. L'uguale vale per ogni trasformazione reversibile e si ritrova il primo principio, altrimenti è sempre maggiore.

Nel caso di un sistema isolato vale anche $S(B)-S(A)\geq0$, cioè l'*entropia può solo aumentare*.

### Sistema a temperatura costante

Prendendo $T$ fissa $$\Delta S\geq \frac{1}{T}\int_{A}^{B}dQ \;\Rightarrow\; T\Delta S\geq\Delta Q=\Delta E+ \Delta W$$da cui
$$\boxed{\Delta E- T\Delta S=\Delta(E-TS)= \Delta A \leq - \Delta W}$$
dove la prima uguaglianza vale perché siamo a $T$ costante. Nel caso il sistema sia a $T$ fissato, ma meccanicamente isolato si ha $\Delta W=0$, quindi
$$\Delta A \leq 0$$
### Sistema a pressione costante

Con $P$ costante
$$\boxed{\Delta A + P\Delta V=\Delta(A+PV)=\Delta G\leq0}$$
dove ancora vale perché siamo a pressione costante.