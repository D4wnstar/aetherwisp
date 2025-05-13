---
wiki-publish: true
---
Consideriamo due [[Particella|particelle]] quantistiche. Per una singola particella (trascurando lo [[spin]]), il suo [[stato]] è descritto dalla sua [[funzione d'onda]] $\Psi(\vec{r},t)$. Per due particelle, si ha una funzione d'onda per entrambe: $\Psi(\vec{r}_{1},\vec{r}_{2},t)$, con $\vec{r}_{1}$ le coordinate della particella uno e $\vec{r}_{2}$ le coordinate della particella due. L'evoluzione temporale è descritta come di norma dall'[[equazione di Schrödinger]] con [[Hamiltoniana]]
$$H=- \frac{\hbar^{2}}{2m_{1}}\nabla^{2}_{1}- \frac{\hbar^{2}}{2m_{2}}\nabla^{2}_{2}+V(\vec{r}_{1},\vec{r}_{2},t)$$
con $\nabla^{2}_{i}$ il [[Laplacian]] rispetto alle coordinate della prima o seconda particella.

Una funzione d'onda così definita si comporta come ogni altra: vale l'interpretazione statistica
$$|\Psi(\vec{r}_{1},\vec{r}_{2},t)|^{2}d\tau_{1}d\tau_{2}$$
che rappresenta la probabilità di trovare simultaneamente la particella uno nell'elemento di volume $d\tau_{1}$ e la particella due in $d\tau_{2}$. Deve essere [[Normalization|normalizzata]]:
$$\iint|\Psi(\vec{r}_{1},\vec{r}_{2},t)|^{2}d\tau_{1}d\tau_{2}=1$$
La dipendenza temporale si ottiene sempre per [[separazione di variabili]] e un [[sistema ortonormale completo]] di soluzioni tempo-indipendenti $\psi$:
$$\Psi(\vec{r}_{1},\vec{r}_{2},t)=\psi(\vec{r}_{1},\vec{r}_{2})e^{-i E t/\hbar}$$
dove le $\psi$ si ottengono dall'usuale equazione di Schrödinger indipendente dal tempo
$$- \frac{\hbar^{2}}{2m_{1}}\nabla^{2}_{1}\psi- \frac{\hbar^{2}}{2m_{2}}\nabla^{2}_{2}\psi+ V \psi=E\psi$$
e $E$ è l'energia totale del sistema.
### Particelle interagenti
Nel caso il [[Potential]] di interazione fra le due particelle dipenda solo dalla distanza reciproca $\vec{r}\equiv\vec{r}_{1}-\vec{r}_{2}$, possiamo risolvere l'equazione di Schrödinger per separazione di variabili, compiendo la sostituzione
$$\vec{r}_{1},\quad\vec{r}_{2} \quad \rightarrow \quad \vec{r}\equiv\vec{r}_{1}-\vec{r}_{2},\quad\vec{R}\equiv\frac{m_{1}\vec{r}_{1}+m_{2}\vec{r}_{2}}{m_{1}+m_{2}}$$
dove $\vec{R}$ è il [[centro di massa]]. Con queste sostituzioni, e definendo la massa ridotta come $\mu\equiv\frac{m_{1}m_{2}}{m_{1}+m_{2}}$, si trova che l'equazione indipendente dal tempo diventa
$$- \frac{\hbar^{2}}{2(m_{1}+m_{2})}\nabla^{2}_{R}\psi- \frac{\hbar^{2}}{2\mu}\nabla^{2}_{r}\psi+V(\vec{r})\psi=E\psi$$
che è risolvibile separando $\vec{r}$ e $\vec{R}$. Si trova che $\psi_{R}(\vec{R})$ soddisfa l'equazione di Schrödinger per una particella con massa $m_{1}+m_{2}$, potenziale nullo ed energia $E_{R}$, mentre $\psi_{r}(\vec{r})$ lo fa per una particella con massa ridotta $\mu$, potenziale $V(\vec{r})$ e energia $E_{r}$. L'energia totale è $E=E_{R}+E_{r}$.

In sostanza, questa soluzione ci dice che in una sistema di due particelle accoppiate con potenziale $V\propto\vec{r}$, il centro di massa si muove come una [[Particella libera (quantistica)]] con massa totale e il moto relativo (quello della particella due rispetto alla uno) come una particella con massa ridotta nel potenziale $V$. Questo riduce un sistema a due corpi ad uno equivalente ad un corpo. Lo stesso accade anche in meccanica classica.
### Traslazione rigida
Prendo l'Hamiltoniana di due particelle accoppiate
$$H=H(q_{1},p_{1},q_{2},p_{2})= \frac{p_{1}^{2}}{2m} + \frac{p_{2}^{2}}{2m}+\frac{k}{2}(q_{2}-q_{1})^{2}$$
Il generatore della traslazione (rigida di tutto il sistema) è il momento lineare totale $P=p_{1}+p_{2}$. Allora abbiamo
$$q'_{1}=\frac{dq_{1}}{d\alpha}=\{q_{1},P\}=\{q_{1},p_{1}\}=1$$
$$q'_{2}=\frac{dq_{2}}{d\alpha}=\{q_{2},P\}=\{q_{2},p_{2}\}=1$$
Definendo la posizione relativa $q=q_{2}-q_{1}$, il momento relativo $p= \frac{m_{1}p_{2}-m_{2}p_{1}}{m_{1}+m_{2}}$, la massa ridotta $\mu= \frac{m_{1}m_{2}}{m_{1}+m_{2}}$, il baricentro $Q= \frac{m_{1}q_{1}+m_{2}q_{2}}{m_{1}+m_{2}}$ e la massa totale $M=m_{1}+m_{2}$ sviluppo l'Hamiltoniana
$$H= \frac{P^{2}}{2M}+ \left( \frac{p^{2}}{2\mu} + \frac{k}{2}q^{2} \right)$$
quindi abbiamo disaccoppiato l'interazione reciproca. In meccanica newtoniana la parentesi rappresenta le *forze interne*. In fisica quantistica, possiamo ripetere allo stesso modo il calcolo, usando [[Commutator|commutatori]] e [[operatore|operatori]], e si raggiunge lo stesso identico risultato
$$\hat{H}= \frac{\hat{P}^{2}}{2M}+ \left( \frac{\hat{p}^{2}}{2\mu} + \frac{k}{2}\hat{q}^{2} \right)$$
