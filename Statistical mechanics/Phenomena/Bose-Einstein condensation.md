**Bose-Einstein condensation** is the tendency of [[Boson|bosons]] to collectively and almost exclusively occupy the ground [[stato|state]] of a [[Physical system|system]] around a specific [[temperature]], known as the condensation temperature or critical temperature. This phenomenon occurs at low temperatures and low energies. Mathematically, it is readily seen from the [[Bose-Einstein distribution]], which gives the average [[occupation number]] of each state:
$$\langle n_{i} \rangle =\frac{1}{e^{\beta(\varepsilon_{i}-\mu)}-1}$$
We can see that the distribution has a [[Singolarità isolata|singularity]] when the exponential is $1$, which means when $\mu=0$ and $\varepsilon_{i}\to 0$. This leads to a massive spike of occupation numbers around zero energy, which occurs at very low temperatures. This means that at these temperatures, bosons collectively end up in the ground state, leaving other states nearly unoccupied.
### Boson ideal gas
Condensation can be illustrated through an [[ideal gas]] of $N$ bosons. Assume this gas is enclosed in a cubic volume $V=L^{3}$, where
$$N=\sum_{\mathbf{p}}\langle n_{\mathbf{p}} \rangle =\sum_{\mathbf{p}} \frac{1}{e^{\beta(\varepsilon_{\mathbf{p}}-\mu)}-1}$$
and $\varepsilon_{\mathbf{p}}=\mathbf{p}^{2}/2m$ Since the bosons are free, their [[Equazione agli autovalori|eigenfunctions]] are [[plane wave|plane waves]]: $\propto e^{i\mathbf{p}\cdot \mathbf{r}/\hbar}$. The momentum in the in the direction $\hat{\mathbf{n}}=(n_{x},n_{y},n_{z})$ is
$$\mathbf{p}=\frac{2\pi}{L}\hbar \hat{\mathbf{n}}$$
There is a possible state for every direction. We want to find the number of states $G(\varepsilon)$ up to a certain energy $\varepsilon$:
$$g(\varepsilon)=???$$
The density of states (DOS) $g(\varepsilon)$ is
$$g(\varepsilon)=\frac{ \partial G}{ \partial \varepsilon } =\frac{Vm^{3/2}}{\sqrt{ 2 }\pi ^{2}\hbar ^{3}}\sqrt{ \varepsilon }$$
More generally, the DOS is a function like
$$g(\varepsilon)=C_{\alpha}\varepsilon^{\alpha-1}$$
As it happens, in three dimension $d=3$ and for $\alpha=d/2=3/2$ we have
$$C_{3/2}=V \frac{\sqrt{ 2 }}{3\pi ^{2}\hbar ^{3}}$$
The number of particles can be expressed through the DOS
$$N=\sum_{\mathbf{p}} \frac{1}{e^{\beta(\varepsilon _{\mathbf{p}}-\mu)}-1}=\int_{0}^{\infty}g(\varepsilon) \frac{1}{e^{\beta(\varepsilon-\mu)}-1}d\varepsilon=\int_{0}^{\infty} \frac{C_{\alpha}\varepsilon^{\alpha-1}}{e^{\beta(\varepsilon-1)}-1}$$
We want to solve this integral[^2]. In fact, we mostly want to see if there is a critical temperature $T_{C}\neq 0$ such that ???. To solve the integral, we define
$$\frac{\varepsilon}{k_{B}T_{C}}=x$$
This turns the integral into
$$N=k_{B}T_{C}\int_{0}^{\infty} \frac{C_{\alpha}(k_{B}T_{C})^{\alpha-1}x^{\alpha-1}}{e^{x}-1}=(k_{B}T_{C})^{\alpha}\int_{0}^{\infty} \frac{x^{\alpha-1}}{e^{x}-1}\ dx$$
We can instead solve
$$\begin{align}
\mathcal{I}&=\int_{0}^{\infty} \frac{x^{\alpha-1}}{e^{x}(1-e^{-x})}\ dx=\int_{0}^{\infty}x^{\alpha-1}e^{-x}\sum_{j=0}^{\infty}(e^{-x})^{j}= \\
&=\sum_{j=0}^{\infty}\int x^{\alpha-1}e^{-x}e^{-jx}\ dx=\sum_{j'=1}^{\infty} \int_{0}^{\infty} e^{-j'x}x^{\alpha-1}\ dx= \\
(j'x=y)\quad&=\sum_{j'=1}^{\infty} \int_{0}^{\infty} \frac{1}{j'}e^{-y}\left( \frac{y}{j} \right)^{\alpha-1}=\ldots \\
\end{align} $$
using the Riemann [[Zeta function]]
$$\zeta(\alpha)=\sum_{n=1}^{\infty} \frac{1}{n^{\alpha}}$$
and the [[Gamma function]]. So back to $N$ we have
$$N=(k_{B}T_{C})^{\alpha}\Gamma(\alpha)\zeta(\alpha)$$
We can invert the formula to find the critical temperature
$$T_{C}=\frac{1}{k_{B}}\left[ \frac{N}{C_{\alpha}\Gamma(\alpha)\zeta(\alpha)} \right]^{1/\alpha}$$
In the case $d=3\to \alpha=3/2$ we get, since $\Gamma\left( 3/2 \right)=\sqrt{ \pi }/2$,
$$T_{C}=\frac{1}{k_{B}} \frac{N^{2/3}}{\left[ \frac{Vm^{3/2}}{\sqrt{ 2 }\pi ^{2}\hbar ^{3}}\Gamma\left( \frac{3}{2} \right)\zeta\left( \frac{3}{2} \right) \right]^{2/3}}=\frac{1}{k_{B}}\frac{2\pi}{\left[ \zeta\left( \frac{3}{2} \right) \right]^{2/3}} \frac{\hbar^{2}n^{2/3}}{m}$$
using the density $n=N/V$. This is a finite number, which proves that a free boson gas can condense. With realistic numbers, we get a value of around $\sim 100\text{ nanokelvins}$.