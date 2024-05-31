L'**equazione di Heisenberg** è un'[[equazione differenziale ordinaria]] che descrive l'evoluzione temporale delle [[Osservabile|osservabili]] nella [[Rappresentazioni della meccanica quantistica|rappresentazione di Heisenberg]] della meccanica quantistica. Preso un'[[operatore autoaggiunto]] $\hat{A}$ associato ad un osservabile $A$ in un sistema che segue l'[[Hamiltoniana]] $\hat{H}$, l'equazione di Heisenberg è
$$\frac{d}{dt}\hat{A}_{H}(t)=\frac{i}{\hbar}[\hat{H},\hat{A}_{H}(t)]+\left(\frac{\partial }{\partial t}\hat{A}_{S}(t)\right)_{H}$$
dove $[\cdot,\cdot]$ è il [[commutatore]]. I pedici H e S denotano l'operatore nella rappresentazione di Heisenberg e Schrödinger. L'operatore in H è l'evoluzione temporale di quello in S:
$$\hat{A}_{H}(t)=\hat{U}_{t}^{+}\hat{A}_{S}\hat{U}_{t}$$
dove $\hat{U}_{t}$ è l'[[evolutore]]. È importante notare che l'operatore in H è sempre dipendente dal tempo (perché lo si pesa per l'evolutore), mentre quello in S può essere costante nel tempo.

Nel caso comune di operatori in S che non dipendono dal tempo, l'equazione si riduce a
$$\frac{d}{dt}\hat{A}_{H}(t)=\frac{i}{\hbar}[\hat{H},\hat{A}_{H}(t)]$$
Casi comuni sono l'operatore di posizione e momento, per i quali l'equazione è
$$\dot{q}_{t}=\frac{i}{\hbar}[\hat{H},q_{t}]\quad; \quad \dot{p}_{t}=\frac{i}{\hbar}[\hat{H},p_{t}]$$