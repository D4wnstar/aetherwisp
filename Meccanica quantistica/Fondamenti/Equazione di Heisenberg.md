L'**equazione di Heisenberg** è un'[[equazione differenziale ordinaria]] che descrive l'evoluzione temporale delle [[Osservabile|osservabili]] nella [[Rappresentazioni della meccanica quantistica|rappresentazione di Heisenberg]] della meccanica quantistica. Preso un'[[operatore autoaggiunto]] $\hat{A}$ associato ad un osservabile $A$ in un sistema che segue l'[[Hamiltoniana]] $\hat{H}$, l'equazione di Heisenberg è
$$\frac{d}{dt}\hat{A}_{t}=\frac{i}{\hbar}[\hat{H},\hat{A}_{t}]+\frac{\partial }{\partial t}\hat{A}$$
dove $[\cdot,\cdot]$ è il [[commutatore]]. L'operatore $\hat{A}_{t}$ è l'evoluzione temporale di quello a tempo zero:
$$\hat{A}_{t}=\hat{U}_{t}^{+}\hat{A}\hat{U}_{t}$$
dove $\hat{U}_{t}$ è l'[[evolutore]]. Attenzione al fatto che la derivata parziale nel tempo è su $\hat{A}$, non $\hat{A}_{t}$. Infatti, l'operatore iniziale $\hat{A}$ potrebbe dipendere dal tempo ancor prima di essere evoluto ($\hat{U}_{t}$ aggiungerebbe in qual caso una seconda dipendenza da $t$), ma tipicamente non lo è.

Nel caso comune di operatori che non dipendono intrinsecamente dal tempo, l'equazione si riduce al caso molto più pratico
$$\boxed{\frac{d}{dt}\hat{A}(t)=\frac{i}{\hbar}[\hat{H},\hat{A}(t)]=\frac{i}{\hbar}\hat{U}_{t}^{+}[\hat{H},\hat{A}]\hat{U}_{t}}$$
Questo dimostra un risultato universale e molto importante, già scoperto in meccanica analitica. Dato che l'evoluzione temporale (invero, tutte le trasformazioni [[Operatore unitario|unitarie]]) non modificano le parentesi di commutazione, possiamo risolvere l'equazione di Heisenberg senza dover conoscere l'evoluzione temporale. Infatti, dato che l'equazione dipende da $\hat{A}_{t}$, per risolvere l'equazione e trovare la dinamica dovremmo sapere $\hat{A}_{t}$... che *è* la dinamica. Sarebbe un loop infinito e l'equazione sarebbe logicamente irrisolvibile. Ma grazie al fatto che l'evoluzione temporale non modifica le parentesi di commutazione, possiamo risolvere l'equazione con lo stato iniziale a tempo zero e poi riapplicare l'evoluzione, risolvendo il loop.

Casi comuni sono l'operatore di posizione e momento, per i quali l'equazione è
$$\dot{q}_{t}=\frac{i}{\hbar}[\hat{H},q_{t}]\quad; \quad \dot{p}_{t}=\frac{i}{\hbar}[\hat{H},p_{t}]$$
