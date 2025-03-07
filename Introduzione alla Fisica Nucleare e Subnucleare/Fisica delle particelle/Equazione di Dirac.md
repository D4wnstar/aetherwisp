L'**equazione di Dirac** è un'equazione d'onda relativistica che descrive la dinamica di tutti i [[Fermion|fermioni]] massivi, come [[Elettrone|elettroni]] e [[quark]]. L'equazione è
$$(i\partial_{\mu}\gamma^{\mu}-m)\Psi=0$$
dove $\gamma^{\mu}$ sono le [[matrici gamma]]. La [[funzione d'onda]] $\Psi$ che la risolve è un oggetto a quattro componenti, a differenza della funzione a valori complessi dell'[[equazione di Schrödinger]], e questo viene detto [[bispinore]] o [[spinore di Dirac]].

È una generalizzazione dell'[[equazione di Schrödinger]] che tiene conto della relatività speciale. Essa predice l'esistenza dell'[[antimateria]] e ha portato alla scoperta di numerose particelle, tra cui il [[Elettrone|positrone]].
### Storia e derivazione
Quando si trattano particelle e comunque oggetti molto piccoli, è necessario considerare la meccanica quantistica. Ma queste particelle si muovono alla [[velocità della luce]] (o ad una frazione considerevole di essa), quindi bisogna anche utilizzare la relatività ristretta per descrivere il moto. Come queste due teorie possano essere conciliate è un problema considerevole.

Consideriamo la massa relativistica in [[unità naturali]]
$$E^{2}=p^{2}+m^{2}$$
e l'equazione di Schrödinger
$$E\Psi=H\Psi$$
L'approccio più logico è semplicemente mettere la $E$ relativistica nell'equazione
$$E\Psi=\sqrt{p^{2}+m^{2}}\Psi=H\Psi$$
Allora
$$\sqrt{(-i\nabla)^{2}+m^{2}}\Psi=i \frac{\partial \Psi}{\partial t}$$
Tuttavia, lo spazio e il tempo sono ancora oggetti separati e, per via della radice, non permette di includere l'elettromagnetismo in forma [[Invariante relativistica|invariante]].

Usando l'[[operatore di d'Alembert]] $\Box=\frac{\partial ^{2}}{\partial t^{2}}-\nabla^{2}$ e un po' di algebra, posso riscriverla come
$$(\Box+m^{2})\Psi=0$$
che si chiama [[equazione di Klein-Gordon]]. Ora, grazie al d'Alembertiano, spazio e tempo sono uniti e la radice è svanita, quindi abbiamo risolto entrambi i problemi che avevamo prima.

Purtroppo, questo porta ad un nuovo problema: essendo un'equazione di secondo grado, ci dà due soluzioni: una positiva e una negativa. Ma la soluzione (ad energia) negativa non ha senso, perché implicherebbe probabilità negative, quindi non ha alcun senso fisico. Questa equazione ha comunque utilizzi in qualche ambito della fisica delle particelle, ma non è generale.

Un ragionamento più generale viene da Dirac. Scrivo l'[[Hamiltoniana]] come combinazione lineare di energia e impulso:
$$H=-i\alpha\nabla+\beta m$$
quindi l'equazione di Schrödinger diventa
$$E\Psi=i \frac{\partial \Psi}{\partial t}=(-i\alpha\nabla+\beta m)\Psi$$
$$H=\alpha_{x}p_{x}+\alpha_{y}p_{y}+\alpha_{z}p_{z}+\beta m$$
dove le $\alpha_{i}$ e la $\beta$ devono essere matrici $N\times N$. Se imponiamo che l'energia debba essere uguale all'energia totale relativistica abbiamo
$$E^{2}=p^{2}+m^{2}=(\alpha_{i}p_{i}+m\beta)^{2}$$
Calcolando il quadrato al terzo membro si ha
$$\alpha_{i}p_{i}\alpha_{j}p_{j}+(\alpha_{i}p_{j}m\beta+m\beta \alpha_{j}p_{i})+m^{2}\beta^{2}=\alpha_{i}p_{i}\alpha_{j}p_{j}+(\alpha_{i}\beta+\beta\alpha_{i})mp_{i}+m^{2}\beta^{2}=$$
$$=\alpha_{i}p_{i}\alpha_{j}p_{j}+\{\beta,\alpha_{i}\}mp_{i}+m^{2}\beta^{2}= \frac{1}{2}(\{\alpha_{i},\alpha_{j}\}+[\alpha_{i},\alpha_{j}])p_{i}p_{j}+\{\beta,\alpha_{i}\}mp_{i}+m^{2}\beta^{2}$$
usando il [[Commutatore]] e anticommutatore. Affinché la precedente equazione sia pari a $p^{2}+m^{2}$, devono valere le seguenti condizioni
$$\begin{align}
\{\beta,\alpha_{i}\}&=0 \\
[\alpha_{i},\alpha_{j}]p_{i}p_{j}&=0 \\
\{\alpha_{i},\alpha_{j}\}&=2\delta_{ij} \\
\alpha_{i}^{2}=\beta^{2}&=1
\end{align}$$
con $\delta_{ij}$ la [[Kronecker delta]]. Si trova che le uniche matrici che soddisfano queste condizioni sono
$$\alpha_{i}=\pmatrix{0 & \sigma_{i} \\ -\sigma_{i} & 0},\quad \beta=\pmatrix{\mathbb{1} & 0 \\ 0 & -\mathbb{1}}$$
con $\sigma_{i}$ le [[matrici di Pauli]]. Evidentemente, sono una sorta di loro estensione in spazio $4\times4$.

Dirac introdusse le [[matrici gamma]]:
$$\gamma^{0}=\beta,\quad \gamma^{i}=\gamma^{0}\alpha_{i}$$
e da esse il [[quadrivettore]] $\gamma^{\mu}=(\gamma^{0},\gamma^{1},\gamma^{2},\gamma^{3})$. Con esse posso riscrive l'equazione di Schrödinger come
$$i \frac{\partial \Psi}{\partial t}=(\alpha_{i}p_{i}+\beta m)\Psi$$
moltiplicando per $\beta$
$$i\beta \frac{\partial \Psi}{\partial t}=(\beta\alpha_{i}p_{i}+\beta^{2}m)\Psi$$
ma $\beta=\gamma^{0}$, $\beta\alpha_{i}=\gamma^{i}$, $\beta^{2}=\mathbb{1}$ e sostituendo $p$ con il suo [[operatore]]
$$i\gamma^{0}\frac{\partial \Psi}{\partial t}=\left(-i\gamma^{i}\frac{\partial }{\partial x_{i}}+m\right)\Psi$$
$$i\left(\gamma^{0}\frac{\partial }{\partial t}+\gamma^{i}\frac{\partial }{\partial x_{i}}+m\right)\Psi=0$$
Introduciamo la derivata delle matrici gamma
$$\partial_{\mu}\gamma^{\mu}=\partial_{0}\gamma^{0}+\partial_{i}\gamma^{i}$$
possiamo infine scrivere
$$\boxed{(i\partial_{\mu}\gamma^{\mu}-m)\Psi=0}$$
che è l'**equazione di Dirac** e descrive l'evoluzione temporale di un sistema quantistico tenendo conto dell'energia relativistica. Le soluzioni di questa equazione sono soluzioni anche dell'equazione di Klein-Gordon ed è un [[invariante relativistica]].
### Osservazioni
Come l'equazione di Klein-Gordon, anche quella di Dirac tratta simultaneamente spazio e tempo e permette l'invarianza dell'elettromagnetismo. Inoltre, dato che include implicitamente le matrici di Pauli, tiene automaticamente conto dello [[spin]] semi-intero.

Le uniche probabilità che dà sono tutte positive, che risolve il problema cruciale della Klein-Gordon. Continua a dare soluzioni ad energia negativa, ma non portano a probabilità negative. L'interpretazione di Dirac è che esistesse un elettrone con carica positiva e che gli stati ad energia negativa fossero associati al rilascio di un tale elettrone positivo. In realtà, dato che l'equazione di Dirac vale per tutti i fermioni, ogni fermione doveva avere un antifermione associato. Infatti, secondo Dirac, il [[vuoto quantistico]], l'infinito insieme di possibili stati di energia minima) in realtà non è vuoto, ma è popolato da un numero infinito di [[Particella virtuale|particelle virtuali]] che esistono in stati ad energia negativa e, quando interagiscono con un quanto di energia, possono essere promosse ad energia positiva ed quindi "apparire". Questo concetto, applicato inizialmente solo agli elettroni (le uniche particelle conosciute al tempo), è noto come **mare di Dirac**. Il positrone è inizialmente stato postulato proprio come un buco nel mare di Dirac.

Le soluzioni dell'equazione di Dirac sono anche soluzione dell'equazione di Klein-Gordon.