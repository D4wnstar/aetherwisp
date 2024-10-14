La **delta di Dirac** $\delta(x)$ è una [[Distribuzione temperata]]. Ha le dimensione dell'inverso dell'argomento. È definita come
$$\delta(x)=\begin{cases}
0 & \text{se }x\neq0 \\
\infty & \text{se }x=0
\end{cases}$$
e vale anche
$$\int_{-\infty}^{+\infty}\delta(x)dx=1$$
e soprattutto
$$\int_{-\infty}^{+\infty}\delta(x)f(x)=f(0)$$

La notazione $\delta(x)$ è leggermente impropria, dato che è la notazione di una funzione, mentre questa è una funzione generalizzata. Più correttamente, andrebbe scritta in forma [[Operatore|operatoriale]] $\delta_{0}$, con 0 a rappresentare il punto in cui va a infinito. Così facendo, si può scrivere in modo conciso $\delta_{0}f(x)=f(0)$.

È possibile definire una delta di Dirac che va a infinito in un punto diverso da zero semplicemente traslando di una costante reale $a$:
$$\delta(x-a)=\begin{cases}
0 & \text{se }x\neq a \\
\infty & \text{se }x=a
\end{cases}$$
e anche
$$\delta_{a}f(x)=\int_{-\infty}^{+\infty}\delta(x-a)f(x)=f(a)$$
### Come limite di successione
In generale, la delta di Dirac può essere rappresentata come
$$\delta(x-x_{0})=\int_{-\infty}^{\infty} \frac{e^{ip(x-x_{0})/\hbar}}{2\pi \hbar} \ dp $$
che è particolarmente utile in meccanica quantistica. Per dimostrarlo, consideriamo l'integrale
$$\int_{-\infty}^{\infty} f(x) \ dx =1$$
Consideriamo la successione delle funzioni di prova $f_{n}(x)=nf(nx)$ e definiamo per ciascuna di esse il [[funzionale]] lineare
$$\hat{f}_{n}[g]=\int_{-\infty}^{\infty} f_{n}(nx)g(x) \ dx $$
ossia le applichiamo come una distribuzione. Ora consideriamo il limite
$$\lim_{ n \to \infty } \hat{f}_{n}[g]=\lim_{ n \to \infty } \int_{-\infty}^{\infty} f_{n}(\underbrace{ nx }_{ y })g(x) \ dx =\lim_{ n \to \infty } \int_{-\infty}^{\infty} f(y)g\left( \frac{y}{n} \right) \ dy= $$
$$=\left[ \int_{-\infty}^{\infty} f(y) \ dy  \right]g(0)=g(0)=\int_{-\infty}^{\infty} \delta(x)g(x) \ dx $$
quindi la $\delta(x)$ è il limite (nel senso delle distribuzioni) della successione di funzione $f_{n}(nx)$.

Ci sono diverse scelte per queste $f_{n}$. La più semplice è una successione di funzioni gradino
$$f_{n}(x)=\frac{n}{2}\chi_{[-1,1]}(nx)=\frac{n}{2}\chi_{\left[ - \frac{1}{n}, \frac{1}{n} \right]}(x)$$
dove
$$\chi_{[-1,1]}(x)=\begin{cases}
1 & -1\leq x\leq 1 \\
0 & x>1,\ x<1
\end{cases}$$
ma anche una successione di approssimanti [[Gaussian distribution|Gaussiane]]:
$$f_{n}(x)=n\frac{e^{-n^{2}x^{2}}}{\sqrt{ \pi }}$$
Per dimostrare il punto originale, dobbiamo quindi trovare se c'è una successione di $f_{n}$ il cui limite sia la delta di Dirac. In particolare, vogliamo dimostrare che vale
$$\lim_{ n \to \infty } \underbrace{ \int_{-n}^{n} \frac{e^{-ipx/\hbar}}{2\pi \hbar}\ dx }_{ f_{n}(p) }=\delta(p)$$
Partiamo da $n=1$:
$$\int_{-1}^{1} \frac{e^{-ixp/\hbar}}{2\pi \hbar} \ dx =\frac{i\hbar}{p} \left.\frac{e^{-ixp/\hbar}}{2\pi \hbar}\right|_{-1}^{1}=\text{da finire}$$
da cui
$$f(p)=\sqrt{ \frac{2\hbar}{\pi} } \frac{\sin(p/\hbar)}{p}$$
Più in generale, un'altra possibile successione di funzioni utile è
$$f_{n}(x)=\frac{\sin(nx)}{\pi x}$$
### Risultati utili
È la derivata (nel senso delle distribuzioni) della [[theta di Heaviside]]:
$$D\theta(x)=\delta(x)$$
Preso un [[Operatore]] $T$, l'equazione $xT=0$ è risolta da $T=c\delta(x)$, con $c$ una constate arbitraria.

Analogamente, $xT=aT$ è risolta da $T=c\delta(x-a)$. Questa può essere vista come una sorta di "forma debole" di un'equazione agli autovalori, dove sebbene $x$ non abbia autofunzioni, ha delle "autodistribuzioni" $\delta(x-a)$.

In generale, se $u(x)$ è continua e in un punto $x_{0}$ si ha $u(x_{0})=0$, allora $u(x)\delta(x-x_{0})$.

L'equazione $xT=1$ ha come soluzione generale $T=\mathscr{P} \frac{1}{x}+c\delta(x)$, con $\mathscr{P} \frac{1}{x}$ la [[Distribuzione parte principale]].