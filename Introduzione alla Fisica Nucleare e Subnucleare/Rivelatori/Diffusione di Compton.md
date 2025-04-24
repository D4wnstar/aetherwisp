---
aliases:
  - fronte Compton
---
La **diffusione di Compton** è un fenomeno di [[diffusione di particelle]] tra un [[Photon]] ed un [[elettrone]] che è descritta dall'assorbimento e riemissione di un fotone da parte dell'elettrone [[Atomo|atomico]]. È una forma ad energia più alta della [[diffusione di Thompson]].
### Meccanismo
Il processo può essere schematizzato semplicemente:
$$\gamma e^{-} \rightarrow \gamma e^{-}$$

![[Schema Diffusione Compton|center]]

Per energie del fotone molto maggiori dell'[[energia di legame]] dell'elettrone, questo può essere considerato libero e interagire con il fotone in modo elastico, dove l'elettrone assorbe parte dell'energia del fotone e ne varia la frequenza. Si trova che
$$\Delta \lambda=\lambda'-\lambda=\frac{h}{m_{e}c}(1-\cos\theta)=\lambda_{C}(1-\cos\theta)$$
dove $\lambda_{C}$ è la [[lunghezza d'onda di Compton]] del'elettrone. Maggiore è l'angolo di diffusione $\theta$, maggiore è l'energia ceduta.

> [!info] Risultato
> La variazione di frequenza del fotone è maggiore quanto più vicina la frequenza del fotone è alla lunghezza d'onda di Compton $\lambda_{C}$ dell'elettrone. Questo accade quando l'energia del fotone è $E_{\gamma}=h\nu\simeq hc/\lambda_{C}=m_{e}c^{2}=0.51$ MeV. Per valori molto maggiori, la variazione di frequenza è sostanzialmente nulla.

Si distinguono due casi interessanti:
- $\theta=0$: si ha $\Delta \lambda=0$, ossia l'elettrone non ha ceduto energia.
- $\theta=\pi$: si ha la cessione massima di energia.

Ne risulta che l'energia trasferita all'elettrone nell'urto è:
$$E_{e}=E_{\gamma} \frac{\frac{E_{\gamma}}{m_{e}c^{2}}(1-\cos\theta)}{1+\frac{E_{\gamma}}{m_{e}c^{2}}(1-\cos\theta)}$$
che varia tra 0 e un valore massimo quando $\theta=\pi$, che vale
$$E_{e,max}=E_{\gamma} \frac{\frac{2E_{\gamma}}{m_{e}c^{2}}}{1+\frac{2E_{\gamma}}{m_{e}c^{2}}}<E_{\gamma}$$
detto **fronte Compton**. Il fatto che l'energia assorbita debba essere minore dell'energia del fotone differenzia la diffusione Compton dall'[[effetto fotoelettrico]], infatti violerebbe la conservazione della [[Invariant mass]].

Purtroppo, l'angolo di diffusione non può essere predetto in quanto, per quanto ne sappiamo, è interamente casuale. Di conseguenza, anche l'energia dell'elettrone liberato sarà casuale, entro un intervallo noto $0<E_{e}<E_{e,max}<E_{\gamma}$. Dal punto di vista sperimentale, questo significa che la diffusione Compton può al meglio dare un limite inferiore all'energia del fotone incidente, ma non un valore esatto. Il meglio che si può fare è misurare il risultato di un fascio di fotoni monocromatico e ottenere una buona statistica che ci dà il fronte Compton e da lì avere stime più precise.

![[Schema Fronte Compton|90%|center]]
### Meccanismo inverso
È talvolta possibile che lo scambio di energia avvenga al contrario, ossia che sia un elettrone ad alta energia a trasferire energia ad un fotone impattante con energia minore. Questo fenomeno si dice **diffusione di Compton inversa**. È raro nella materia compatta dato che gli elettroni sono confinati negli atomi, ma in condizioni più estreme, come il [[disco di accrescimento]] di un [[buco nero]], è possibile che un elettrone libero relativistico impatti con un fotone ad energia minore, causano quindi diffusione Compton inversa.