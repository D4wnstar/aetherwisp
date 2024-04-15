La **delta di Dirac** $\delta(x)$ è una [[distribuzione temperata]]. Ha le dimensione dell'inverso dell'argomento. È definita come
$$\delta(x)=\begin{cases}
0 & \text{se }x\neq0 \\
\infty & \text{se }x=0
\end{cases}$$
e vale anche
$$\int_{-\infty}^{+\infty}\delta(x)dx=1$$
e soprattutto
$$\int_{-\infty}^{+\infty}\delta(x)f(x)=f(0)$$

La notazione $\delta(x)$ è leggermente impropria, dato che è la notazione di una funzione, mentre questa è una funzione generalizzata. Più correttamente, andrebbe scritta in forma [[operatore|operatoriale]] $\delta_{0}$, con 0 a rappresentare il punto in cui va a infinito. Così facendo, si può scrivere in modo conciso $\delta_{0}f(x)=f(0)$.

È possibile definire una delta di Dirac che va a infinito in un punto diverso da zero semplicemente traslando di una costante reale $a$:
$$\delta(x-a)=\begin{cases}
0 & \text{se }x\neq a \\
\infty & \text{se }x=a
\end{cases}$$
e anche
$$\delta_{a}f(x)=\int_{-\infty}^{+\infty}\delta(x-a)f(x)=f(a)$$
### Risultati utili
È la derivata (nel senso delle distribuzioni) della [[theta di Heaviside]]:
$$D\theta(x)=\delta(x)$$
Preso un [[operatore]] $T$, l'equazione $xT=0$ è risolta da $T=c\delta(x)$, con $c$ una constate arbitraria.

Analogamente, $xT=aT$ è risolta da $T=c\delta(x-a)$. Questa può essere vista come una sorta di "forma debole" di un'equazione agli autovalori, dove sebbene $x$ non abbia autofunzioni, ha delle "autodistribuzioni" $\delta(x-a)$.

In generale, se $u(x)$ è continua e in un punto $x_{0}$ si ha $u(x_{0})=0$, allora $u(x)\delta(x-x_{0})$.

L'equazione $xT=1$ ha come soluzione generale $T=\mathscr{P} \frac{1}{x}+c\delta(x)$, con $\mathscr{P} \frac{1}{x}$ la [[distribuzione parte principale]].