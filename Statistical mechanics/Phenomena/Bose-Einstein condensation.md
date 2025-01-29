**Bose-Einstein condensation** is the tendency of [[Boson|bosons]] to collectively and almost exclusively occupy the ground [[stato|state]] of a [[Physical system|system]] around a specific [[temperature]], known as the condensation temperature or critical temperature. This phenomenon occurs at low temperatures and low energies. Mathematically, it is readily seen from the [[Bose-Einstein distribution]], which gives the average [[occupation number]] of each state:
$$\langle n_{i} \rangle =\frac{1}{e^{\beta(\varepsilon_{i}-\mu)}-1}$$
We can see that the distribution has a [[Singolarità isolata|singularity]] when the exponential is $1$, which means when $\mu=0$ (and so $z=1$) and $\varepsilon_{i}\to 0$. This leads to a massive spike of occupation numbers around zero energy, which occurs at very low temperatures. This means that at these temperatures, bosons collectively end up in the ground state, leaving other states nearly unoccupied.

The asymptotic nature of $\langle n_{i} \rangle$ near the condensation temperature means that it can be seen macroscopically. Also, one- and two-dimensional ideal [[Bose gas|boson gases]] do not exhibit this behavior.  For a discussion on the exact temperature at which it occurs, see [[Bose gas#Critical condensation temperature]].
### Details
The nature of Bose-Einstein condensation lies fundamentally in the [[Stato total-antisimmetrico|antisymmetry]] of boson [[Funzione d'onda|wavefunctions]]. The antisymmetry leads to the $-1$ term seen in the Bose-Einstein distribution above, which as we've seen above causes the singularity at $z=1$. But there's more: the antisymmetry leads to boson systems being well described by [[Fermi and Bose functions|Bose functions]] $g_{k}(z)$. The Bose function of interest is the one that appears in the particle density equation:
$$n=\frac{1}{\lambda ^{3}}g_{3/2}(z)- \frac{1}{V} \frac{z}{1-z}$$
Here $\lambda$ is the [[Formula di de Broglie|de Broglie thermal wavelength]]. For further discussion and origin of this equation, see [[Ideal gas#In the quantum grand canonical ensemble]]. We can split this equation into two:
$$N_{0}=\frac{z}{1-z},\qquad N_\text{exc}=\frac{V}{\lambda^{3}}g_{3/2}(z)$$
Respectively, these are the ground state and excited state particle numbers, obtained from $N=nV$. When $z$ approaches $1$, the ground state number tends to diverge, leading to the condensation phenomenon. But more can be seen in the excited states. Since $z$ is bounded between $0$ and $1$, so too is $g_{3/2}(z)$ bounded between $0$ and $\zeta(3/2)$, using the [[Riemann Zeta function]]. This means that $N_\text{exc}$ is itself bounded:
$$0\leq N_\text{exc}\leq \frac{V}{\lambda ^{3}}\zeta\left( \frac{3}{2} \right)$$
Importantly, there is an upper limit to the number of excited bosons in a Bose gas. Mind you, not the *total* number of bosons, specifically just the *excited* ones. Of course, it is natural that these excited states will host as many bosons as they physically can:
$$N_\text{exc,max}=\frac{V}{\lambda ^{3}}\zeta\left( \frac{3}{2} \right)$$
but any more than these and there just isn't any more room. Any excess will be pushed in its entirety down to the ground state, which due to the singularity has effectively unlimited capacity[^1]. In fact, at a set volume, when $T\to 0$ and hence $\lambda\to \infty$, this limit tends to $0$. All excited bosons are *squeezed* out of the excited states back to the ground state.

These two sets of particles, due to their very different behavior, effectively make up two separate [[phase|phases]]:
1. A *normal phase*, consisting of excited bosons distributed as usual.
2. A *condensed phase*, consisting of a macroscopic amount of bosons all accumulated in the ground state.

At a given volume $V$ and temperature $T$, the onset of the condensation occurs when the number of bosons in the system exceeds the limit for excited bosons:
$$N>N_\text{exc,max}= \frac{V}{\lambda ^{3}}\zeta\left( \frac{3}{2} \right)=T^{3/2} V \frac{(2\pi mk_{B})^{3/2}}{h^{3}}\zeta\left( \frac{3}{2} \right)$$
On the other hand, if hold $N$ constant instead of $T$, we get
$$T<T_{C}=\frac{h^{2}}{2\pi mk_{B}}\left[ \frac{N}{V\zeta\left( \frac{3}{2} \right)} \right]^{2/3}$$
where $T_{C}$ is the critical temperature at which the [[phase transition]] occurs.

[^1]: Unlimited not in the sense of infinite, there's still a finite number $N$ of bosons, rather in the sense that the ground state can accomodate every single boson in the system if it needs to.