Quando si trattano [[Particella|particelle]] e comunque oggetti molto piccoli, è necessario considerare la meccanica quantistica. Ma queste particelle si muovono alla [[velocità della luce]] (o ad una frazione considerevole di essa), quindi bisogna anche utilizzare la relatività ristretta per descrivere il moto. Come queste due teorie possano essere conciliate è un problema considerevole.

Consideriamo la massa relativistica in [[unità naturali]]
$$E^{2}=p^{2}+m^{2}$$
e l'[[equazione di Schrödinger]]
$$E\Psi=H\Psi$$
L'approccio più logico è mettere la $E$ relativistica nell'equazione
$$E\Psi=\sqrt{p^{2}+m^{2}}\Psi=H\Psi$$
Allora
$$\sqrt{(-i\nabla)^{2}+m^{2}}\Psi=i \frac{\partial \Psi}{\partial t}$$
...

Usando l'[[operatore di d'Alembert]] $\Box=\frac{\partial ^{2}}{\partial t^{2}}-\nabla^{2}$ posso scrivere
$$(\Box+m^{2})\Psi=0$$
che si chiama **equazione di Klein-Gordon**. Il problema con questa equazione è che, essendo un'equazione di secondo grado, ci dà due soluzioni: una positiva e una negativa. Ma la soluzione (ad energia) negativa non ha senso, perché implicherebbe probabilità negative, quindi non ha alcun senso fisico. Questa equazione ha comunque utilizzi in qualche ambito della fisica delle particelle, ma non è generale.

Un ragionamento più generale viene da Dirac. Scrivo l'[[Hamiltoniana]] come
$$H=\alpha_{i}p_{i}+m\beta$$
quindi l'equazione di Schrödinger diventa
$$E\Psi=i \frac{\partial \Psi}{\partial t}=(-i\alpha\nabla+\beta m)\Psi$$
$$(\alpha_{i}p_{i}+m\beta)^{2}=E^{2}=p^{2}+m^{2}$$
Calcolando il quadrato al primo membro si ha
$$\alpha_{i}p_{i}\alpha_{j}p_{j}+(\alpha_{i}p_{j}m\beta+m\beta \alpha_{j}p_{i})+m^{2}\beta^{2}=\alpha_{i}p_{i}\alpha_{j}p_{j}+(\alpha_{i}\beta+\beta\alpha_{i})mp_{i}+m^{2}\beta^{2}=$$
$$=\alpha_{i}p_{i}\alpha_{j}p_{j}+\{\beta,\alpha_{i}\}mp_{i}+m^{2}\beta^{2}= \frac{1}{2}(\{\alpha_{i},\alpha_{j}\}+[\alpha_{i},\alpha_{j}])p_{i}p_{j}+\{\beta,\alpha_{i}\}mp_{i}+m^{2}\beta^{2}$$
usando il [[commutatore]] e anticommutatore. Affinché la precedente equazione sia pari a $p^{2}+m^{2}$, devono valere le seguenti condizioni
$$\begin{align}
\{\beta,\alpha_{i}\}&=0 \\
[\alpha_{i},\alpha_{j}]p_{i}p_{j}&=0 \\
\{\alpha_{i},\alpha_{j}\}&=2\delta_{ij} \\
\alpha_{i}^{2}=\beta^{2}&=1
\end{align}$$
con $\delta_{ij}$ la [[delta di Kronecker]]. Si trova che le uniche matrici che soddisfano queste condizioni sono
$$\alpha_{i}=\pmatrix{0 & \sigma_{i} \\ -\sigma_{i} & 0},\quad \beta=\pmatrix{1 & 0 \\ 0 & -1}$$
con $\sigma_{i}$ le [[matrici di Pauli]].

Introduciamo le nuove matrici
$$\gamma^{0}=\beta,\quad \gamma^{i}=\gamma^{0}\alpha_{i}$$
e da esse il [[quadrivettore]] $\gamma^{\mu}=(\gamma^{0},\gamma^{1},\gamma^{2},\gamma^{3})$. Allora posso scrivere
$$i \frac{\partial \Psi}{\partial t}=(\alpha_{i}p_{i}+\beta m)\Psi$$
$$i\beta \frac{\partial \Psi}{\partial t}=(\beta\alpha_{i}p_{i}+\beta^{2}m)\Psi$$
$$i\gamma^{0}\frac{\partial \Psi}{\partial t}=\left(-i\gamma^{i}\frac{\partial }{\partial x_{i}}+m\right)\Psi$$
$$i\left(\gamma^{0}\frac{\partial }{\partial t}+\gamma^{i}\frac{\partial }{\partial x_{i}}\right)\Psi=m\Psi$$
$$\partial_{\mu}\gamma^{\mu}=\partial_{0}\gamma^{0}+\partial_{i}\gamma^{i}$$
$$\boxed{(i\partial_{\mu}\gamma^{\mu}-m)\Psi=0}$$
che si chiama **equazione di Dirac** e descrive l'evoluzione temporale di un sistema quantistico tenendo conto dell'energia relativistica. Le soluzioni di questa equazione sono soluzioni anche dell'equazione di Klein-Gordon ed è un [[invariante relativistica]].

Questa equazione continua a dare soluzioni ad energia negativa, ma l'interpretazione di Dirac è che esistesse un [[elettrone]] con carica positiva e che gli stati ad energia negativa fossero associati al rilascio di un tale elettrone positivo. In realtà, dato che l'equazione di Dirac vale per tutti i [[Fermione|fermioni]], ogni fermione doveva avere un antifermione associato. Lo spazio di infiniti stati ad energia negativa prende il nome di **mare di Dirac**.