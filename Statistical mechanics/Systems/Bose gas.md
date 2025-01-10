A **Bose gas** is a model for a [[Physical system|system]] of many non-interacting [[Boson|bosons]], the simplest example of which is a bosonic [[ideal gas]]. A notable property is that three-dimensional Bose gases exhibit a phenomenon known as [[Bose-Einstein condensation]] at near-zero [[Temperature|temperatures]]. The [[equation of state]] of a Bose gas is
$$\frac{P}{k_{B}T}=\frac{1}{\lambda ^{3}}g_{5/2}(z)- \frac{1}{V}\ln(1-z)$$
where $g_{5/2}(z)$ is a [[Fermi and Bose functions|Bose function]].

Unlike [[Fermion|fermions]], there exist massless bosons on top of [[mass|massive]] ones. A Bose gas of massless bosons has somewhat different properties to a gas of massive bosons, since [[Ensemble|ensembles]] of massless particles always have zero [[chemical potential]]. For an example of a [[photon]] gas, see [[Black body cavity]].
### Critical condensation temperature
Condensation can be illustrated through an gas of $N$ bosons. Assume this gas is enclosed in a cubic volume $V=L^{3}$, where
$$N=\sum_{\mathbf{p}}\langle n_{\mathbf{p}} \rangle =\sum_{\mathbf{p}} \frac{1}{e^{\beta(\varepsilon_{\mathbf{p}}-\mu)}-1}$$
and $\varepsilon_{\mathbf{p}}=\mathbf{p}^{2}/2m$. In the [[Thomas-Fermi approximation]], it becomes
$$N=\int_{0}^{\infty}g(\varepsilon) \frac{1}{e^{\beta(\varepsilon-\mu)}-1}d\varepsilon=\int_{0}^{\infty} \frac{C_{\alpha}\varepsilon^{\alpha-1}}{e^{\beta(\varepsilon-\mu)}-1}$$
We can find an approximate solution for this integral[^1], for instance with the [[Sommerfeld expansion]]. The more interesting question is:  is there a nonzero critical temperature $T_{C}$ where the [[chemical potential]] vanishes, that is $\mu=\min\varepsilon_{p}=0$[^2]? To check this, we try to solve the integral with $\mu=0$ and see where that leads us, if it's even possible.

The original solution is due to Einstein. Since at the condensation point the number of particles in the ground [[stato|state]] blows up, we can split $N$ into $N_\text{exc}$ and $N_\text{ground}=\langle n_{p=0} \rangle$. The sum of these two makes $N$. For most temperatures, $N_\text{ground}\simeq0$ and $\text{N}_\text{exc}\simeq N$, which is why this split makes little sense in most conditions. The integral to solve is
$$N_\text{exc}(T=T_{C},\mu=0)\int_{0}^{\infty} \frac{C_{\alpha}\varepsilon^{\alpha-1}}{e^{\beta_{C} \varepsilon_{p}}-1}d\varepsilon=N$$
where $\beta_{C}=1/k_{B}T_{C}$. If there is a solution to this, then $T_{C}$ exists and is not zero.

To start, we make the substitution $\beta_{C}\varepsilon=x$. This turns the integral into
$$N=k_{B}T_{C}\int_{0}^{\infty} \frac{C_{\alpha}(k_{B}T_{C})^{\alpha-1}x^{\alpha-1}}{e^{x}-1}=(k_{B}T_{C})^{\alpha}\int_{0}^{\infty} \frac{x^{\alpha-1}}{e^{x}-1}\ dx$$
This integral can be solved using the [[Serie geometrica|geometric series]]:
$$\begin{align}
\int_{0}^{\infty} \frac{x^{\alpha-1}}{e^{x}-1}\ dx&=\int_{0}^{\infty} \frac{x^{\alpha-1}}{e^{x}(1-e^{-x})}\ dx \\
\text{(geometric series)}&=\int_{0}^{\infty}x^{\alpha-1}e^{-x}\sum_{j=0}^{\infty}(e^{-x})^{j} \\
&=\sum_{j=0}^{\infty}\int x^{\alpha-1}e^{-x}e^{-jx}\ dx \\
(j+1\to j')&=\sum_{j'=1}^{\infty} \int_{0}^{\infty} e^{-j'x}x^{\alpha-1}\ dx \\
(j'x=y)&=\sum_{j'=1}^{\infty} \int_{0}^{\infty} \frac{1}{j'}e^{-y}\left( \frac{y}{j} \right)^{\alpha-1}= \\
&=\underbrace{ \sum_{j'=1}^{\infty} \frac{1}{(j')^{\alpha}} }_{ \zeta(\alpha) }\underbrace{ \int_{0}^{\infty}e^{-y}y^{\alpha-1}dy }_{ \Gamma(\alpha) } \\
&=\zeta(\alpha)\Gamma(\alpha)
\end{align} $$
using both the [[Riemann Zeta function]] and the [[Gamma function]]. Back to $N$, we have
$$N=(k_{B}T_{C})^{\alpha}\Gamma(\alpha)\zeta(\alpha)$$
Curious selection of functions aside, we can invert the formula to find the critical temperature
$$\boxed{T_{C}=\frac{1}{k_{B}}\left[ \frac{N}{C_{\alpha}\Gamma(\alpha)\zeta(\alpha)} \right]^{1/\alpha}}$$
In the 3D case $d=3\to \alpha=3/2$ we get
$$T_{C}=\frac{1}{k_{B}} \frac{N^{2/3}}{\left[ \frac{Vm^{3/2}}{\sqrt{ 2 }\pi ^{2}\hbar ^{3}}\Gamma\left( \frac{3}{2} \right)\zeta\left( \frac{3}{2} \right) \right]^{2/3}}=\frac{1}{k_{B}}\frac{2\pi}{\left[ \zeta\left( \frac{3}{2} \right) \right]^{2/3}} \frac{\hbar^{2}n^{2/3}}{m}$$
using the density $n=N/V$. This is a finite number, which proves that a free boson gas can condense. With realistic numbers for an [[Atomo|atomic]] gas, we get a value of around $\sim 100$ nanokelvins[^3].

In both the 1D and 2D case, this gives $T_{C}=0$, which shows that bosons cannot condense in those dimensions.

[^1]: Also see Chapter 1 of Feynman's *Statistical Mechanics*.
[^2]: Remember that $\mu <\varepsilon_{p}$ for all $p$, so if $\varepsilon_{p}\to 0$ then $\mu\to 0$.
[^3]: Fun fact: when Einstein first solved this problem, he thought this was mostly a moot answer. Not because it was wrong, but because the temperatures you get are so tiny, he was convinced we would never reach them experimentally. He wasn't completely wrong: most methods of cooling, even modern ones, can't go below $\sim 10$ millikelvins, several order of magnitudes too high. But with the discovery of methods like [[laser cooling]] about 70 years later, it became possible to reach temperatures this low for small systems. What do you know, experiments showed that condensation actually happens. Also, side note: atomic helium gases have a critical temperature of about 3 kelvins and in fact go [[superfluidity|superfluid]] around that point.