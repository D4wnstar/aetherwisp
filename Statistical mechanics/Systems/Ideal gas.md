---
aliases:
  - ideal gas law
---
An **ideal gas** is an approximate model of the behavior of a gas that holds for low density gases. It is sparse and has weak internal interactions that limit [[information]] exchange. The dynamics are determined by the **ideal gas law**:
$$PV=Nk_{B}T=nRT$$
where $P$ is the [[pressure]], $V$ is the volume occupied by the gas, $N$ is the number of [[particella|particles]] composing the gas, $k_{B}$ is the [[Boltzmann constant]], $T$ is the [[temperature]], $n$ is the number of [[mole|moles]] and $R$ is the [[ideal gas constant]]. The latter form exists because, besides being of practical convenience, thermodynamics was historically developed at a time where the existence of the [[atomo|atom]] had yet to be proven and with it, the [[Particella|particle]] division of matter. In fact, classical thermodynamics as a whole does not strictly require the existence of particles like atoms.

![[Schema Ideal Gas state|center]]
### Properties
The [[heat capacity]] by volume of a monatomic ideal gas is
$$C_{V}=\frac{3}{2}Nk_{B}$$
### Entropy
The [[entropy]] of an ideal gas can calculated as a function of volume $V$ and temperature $T$ by explicitly integrating $dS=dQ/T$. Let's consider a [[stato|state]] $A$, which we approach from two different states: one using an constant-volume transformation (path 1), the other using a isothermal one (path 2).

Along path 1, $V$ is constant, so
$$\int \frac{dQ}{T}=C_{V}\int \frac{dT}{T}$$
and thus if we start the transformation at temperature $T_{0}$ we get
$$S(V,T)=S(V,T_{0})+C_{V}\int_{T_{0}}^{T} \frac{dT}{T}=S(V,T_{0})+C_{V}\ln \frac{T}{T_{0}}$$

Along path 2, $T$ is constant, so
$$dU=0$$
and thus, using the [[Laws of thermodynamics|first law of thermodynamics]] and the ideal gas law, we get
$$dQ=dW=PdV=Nk_{B}T \frac{dV}{V}$$
which gives us, starting from $V_{0}$,
$$S(V,T)=S(V_{0},T)+Nk_{B}\int_{V_{0}}^{V} \frac{dV}{V}=S(V_{0},T)+Nk_{B}\ln \frac{V}{V_{0}}$$

The entropy for the two paths must be equal, so comparing the two expressions for $S(V,T)$ we get (TODO: Figure out how this even works)
$$S(V,T_{0})=C_{0}+Nk_{B}\ln V$$
 where $C_{0}$ is an arbitrary constant. Absorbing $V_{0}$ into $C_{0}$ we can write
 $$S(V,T)=C_{0}+Nk_{B}\ln V+C_{V}\ln T$$
 This depends on the nature of the gas itself, because of $C_{V}$. For a monatomic ideal gas, we have
$$S(V,T)=C_{0}+Nk_{B}\ln(VT^{3/2})$$
#### In the classical microcanonical ensemble
The entropy can also be calculated by modeling an ideal gas as a [[microcanonical ensemble]] of [[Hamiltonian]]
$$H=\sum_{i=1}^{N} \frac{\mathbf{p}^{2}_{i}}{2m}$$
We use the entropy given by the sigma function $S=k_{B}\log \Sigma(E)$ where
$$\Sigma(E)=\frac{1}{h^{3N}}\int\limits_{H(\mathbf{q},\mathbf{p})<E}d^{3}q_{1}\ldots d^{3}q_{N}\,d^{3}p_{1}\ldots d^{3}p_{N}$$
and $h$ is a dimensionally appropriate constant, specifically $\text{impulse}\times\text{length}$, which gives $\text{energy}\times\text{seconds}$. We can develop this as
$$\Sigma(E)=\left( \frac{V}{h^{3}} \right)^{N}\int\limits_{H(\mathbf{q},\mathbf{p})<E}d^{3}p_{1}\ldots d^{3}p_{N}$$
Since the energy of a particle under no potential is $E=p^{2}/2m$, the momentum is $p=\sqrt{ 2mE }$. This momentum describes a $n$-[[palla|ball]] of radius $R=p=\sqrt{ 2mE }$ in the momentum-only [[phase space]], but the integral finds the volume of that ball in phase space (by finding the representative points contained therein), so we can rename the integral as a function $\Omega_{3N}(R)$ which finds the volume of a $3N$-dimensional ball of radius $R$:
$$\Sigma(R)=\left( \frac{V}{h^{3}} \right)^{N}\Omega_{3N}(R)$$
In general, $\Omega_{3N}$ is
$$\Omega_{3N}(R)=\int\limits_{x_{1}^{2}+x_{2}^{2}+\ldots+x_{n}^{2}<R^{2}}dx_{1}\ldots dx_{n}$$
(in our case, $x\equiv p$). We know both $V$ and $h$ ($h$ just needs to have the correct dimensions, so might as well be $h=1 \text{ Js}$ in this case), so in order to find $\Sigma$ and therefore $S$, we just need to solve $\Omega$ in $3N$ dimensions. Thankfully, $\Omega$ can be solved generally for any integer $N$ (see [[Volume of an n-ball]]), which gives
$$\Omega_{3N}=\frac{\pi^{3N/2}}{\Gamma\left( \frac{3N}{2}+1 \right)}R^{3N}$$
where $\Gamma$ is the [[Gamma function]]. Thus, we have
$$\Sigma(R)=\left( \frac{V}{h^{3}} \right)^{N} \underbrace{ \frac{\pi^{3N/2}}{\Gamma\left( \frac{3N}{2}+1 \right)} }_{ c_{n} }R^{3N}=\left( \frac{V}{h^{3}} \right)^{N}c_{3N} (2mE)^{3N/2}$$
and entropy
$$S=k_{B}\log \Sigma(R)$$
We can use the fact that $\Gamma(n+1)=n!$ and [[Stirling's approximation]] $\log n!=n\log n-n+O(\log n)$ to get [[Steps Entropy microcanonical ideal gas]].
#### In the classical canonical ensemble
An ideal gas can also be derived from the [[canonical ensemble]]. Using the Hamiltonian
$$H=\sum_{i=1}^{N} \frac{\mathbf{p}^{2}_{i}}{2m}$$
the [[partition function]] is
$$\begin{align}
Q_{N}&=\int \frac{e^{-\beta(\mathbf{p}_{1}^{2}+\ldots+\mathbf{p}_{N}^{2})/2m}}{h^{3N}N!} \ d^{3N}q\ d^{3N}p \\ \\
&= \frac{1}{N!} \int d^{3N}q\int \frac{e^{-\beta(\mathbf{p}_{1}^{2}+\ldots+\mathbf{p}_{N}^{2})/2m}}{h^{3N}}d^{3N}p \\
&= \frac{V^{N}}{N!}\left( \int_{-\infty}^{\infty} \frac{e^{-\beta p^{2}/2m}}{h} \ dp  \right)^{3N}
\end{align} $$
Solving the [[Gaussian integral]] and using the [[Formula di de Broglie|de Broglie thermal wavelength]] $\lambda$, we write
$$Q_{N}=\frac{1}{N!}\left( \frac{V}{\lambda ^{3}} \right)^{N}$$
and its logarithm is
$$\ln Q_{N}=-\ln N!+N\ln \frac{V}{\lambda ^{3}}\simeq N-N\ln N+N\ln \frac{V}{\lambda ^{3}}=N(1-\ln n\lambda ^{3})$$
where we defined the particle density $n=N/V$. Now that we have the partition function, thermodynamics follows suit naturally. The Helmholtz free energy is
$$A=- \frac{1}{\beta}\ln Q_{N}\simeq- \frac{1}{\beta}N(1-\ln (n\lambda ^{3}))=k_{B}TN[\ln(n\lambda ^{3})-1]$$
and the entropy
$$\begin{align}
S&=-\left( \frac{ \partial A }{ \partial T }  \right)_{V} \\
&=-k_{B}N\frac{ \partial  }{ \partial T } [T(\ln(n\lambda ^{3})-1)] \\
&=-k_{B}N\left[ \ln(n\lambda ^{3})-1 + T\frac{ \partial  }{ \partial T } \ln(n\lambda ^{3}) \right] \\
&=-k_{B}N\left[ \ln(n\lambda ^{3})-1- T\frac{3}{2T} \right] \\
&=k_{B}N\left[ \frac{5}{2}-\ln(n\lambda ^{3}) \right]
\end{align}$$
which is the [[Sackur-Tetrode equation]], as expected.
### In the quantum microcanonical ensemble
It is possible to derive the behavior of an ideal gas using the [[quantum microcanonical ensemble]]. Consider a cube of side $L$ and volume $V=L^{3}$ filled with the ideal gas.
### In the quantum grand canonical ensemble
The [[equation of state]] can be expressed with the grand [[partition function]] $\mathcal{Z}$ as
$$\frac{PV}{k_{B}T}=\log \mathcal{Z}(Z,V,T)=\left\{\begin{align}
\text{(Bosons)}\quad &-\sum_{\bar{p}} \log (1-Ze^{-\beta \varepsilon_{\bar{p}}}) \\
\text{(Fermions)}\quad &\sum_{\bar{p}} \log(1+Ze^{-\beta \varepsilon_{\bar{p}}})
\end{align}\right.$$
The number of particle is
$$\sum_{\bar{p}}\langle n_{\bar{p}} \rangle =N=Ze\frac{ \partial  }{ \partial Z } \mathcal{Z}(Z,V,T)=\left\{\begin{align}
\text{(Bosons)}\quad &\sum_{\bar{p}} \frac{Ze^{-\beta \varepsilon_{\bar{p}}}}{1-Ze^{-\beta \varepsilon_{\bar{p}}}}  \\
\text{(Fermions)}\quad &\sum_{\bar{p}} \frac{Ze^{-\beta \varepsilon_{\bar{p}}}}{1+Ze^{-\beta \varepsilon_{\bar{p}}}}
\end{align}\right.$$
The particle density is
$$\frac{1}{v}=\frac{N}{V}=\frac{4\pi}{h^{3}}\int_{0}^{\infty}p^{2} \frac{1}{Z^{-1}e^{\beta p^{2}/2m}}dp$$
#### Fermions
For fermions, the average occupation number is
$$\langle n_{\bar{p}} \rangle =\frac{1}{Z^{-1}e^{\beta \varepsilon_{\bar{p}}}+1}=\frac{1}{e^{\beta(\varepsilon_{\bar{p}}-\mu)}+1}$$
We get
$$\frac{PV}{k_{B}T}=\log \mathcal{Z}=\sum_{\bar{p}}\log(1+Ze^{-\beta \varepsilon_{\bar{p}}})=\frac{V}{(2\pi h)^{3}}4\pi \int_{0}^{\infty}p^{2}\log(1+Ze^{-\beta p^{2}/2m})\ dp=\ldots$$
Introducing the function
$$f_{5/2}(Z)=\frac{4}{\sqrt{ \pi }}\int_{0}^{\infty}x^{2}\log(1+Ze^{-x^{2}})\ dx=\frac{4}{\sqrt{ \pi }}\sum_{j=1}^{\infty}\int_{0}^{\infty}x^{2}Z^{j}e^{-jx^{2}}=\sum_{j=1}^{\infty} \frac{(-1)^{j+1}Z^{j}}{j^{5/2}}$$
(This is the Riemann zeta function calculated in 5/2???) and using the substitution $\beta p^{2}/2m=y^{2}$, we can state
$$\begin{align}
\ldots&=\frac{4\pi}{h^{3}}\int_{0}^{\infty}\sqrt{ \frac{2m}{\beta} }y^{2} \frac{2m}{\beta}\log(1+Ze^{-y^{2}})\ dy \\
&=\left( \frac{4\pi}{h^{3}} \right)\left( \frac{2m}{\beta} \right)^{3/2}\int_{0}^{\infty}y^{2}\log(1+Ze^{-y^{2}})\ dy \\
&=\frac{1}{\lambda^{3}}f_{5/2}(Z)
\end{align}$$
using the thermal wavelength. The particle density is
$$\frac{1}{v}=\frac{4\pi}{h^{3}}\left( \frac{2m}{\beta} \right)^{3/2}\int_{0}^{\infty} \frac{y^{2}}{Z^{-1}e^{y^{2}}+1}=\frac{1}{\lambda ^{3}}Z\frac{ \partial  }{ \partial Z } f_{5/2}(Z)$$
If we introduce another function
$$f_{3/2}(Z)=\sum_{j=1}^{\infty} \frac{(-1)^{j+1}Z^{j}}{j^{3/2}}$$
we can finally get
$$\boxed{\left\{ \begin{align}
\frac{PV}{k_{B}T}&=\frac{1}{\lambda ^{3}}f_{5/2}(Z)\\
\frac{1}{v}&=\frac{1}{\lambda ^{3}}f_{3/2}(Z)
\end{align} \right.}$$
##### Bosons
For bosons we have
$$\frac{PV}{k_{B}T}=-\sum_{\bar{p}}\log(1-Ze^{-\beta \varepsilon_{\bar{p}}})$$
The average occupation number is
$$\langle n_{\bar{p}} \rangle =\frac{1}{Z^{-1}e^{\beta \varepsilon_{\bar{p}}}-1}=\frac{1}{e^{\beta(\varepsilon_{\bar{p}}-\mu)}-1}$$
Note that this function diverges if $e^{\beta(\varepsilon_{\bar{p}}-\mu)}=1$, which is to say $\mu=0$ and $\bar{p}\to 0$. In this state, the ground state's occupation number blows up to infinity and all other states becomes unoccupied, which means that all bosons "collapsed" into the ground state. This is called [[Bose-Einstein condensation]] and it only occurs in bosons due to the $-1$ term at the denominator. Fermions have a $+1$, which means that the function never diverges.

Similarly to fermions, we can find
$$\left\{ \begin{align}
\frac{P}{k_{B}T}&=\frac{4\pi}{h^{3}}\int_{0}^{\infty}p^{2}\log(1-Ze^{\beta p^{2}/2m})\ dp- \frac{1}{V}\log(1-Z) \\
\frac{1}{v}&=\frac{4\pi}{h^{3}}\int p^{2} \frac{1}{Z^{-1}e^{\beta p^{2}/2m}} + \frac{1}{V} \frac{Z}{1-Z}
\end{align} \right.$$
Defining
$$g_{5/2}(Z)=\sum_{j=1}^{\infty} \frac{Z^{j}}{j^{5/2}},\qquad g_{3/2}(Z)=\sum_{j=1}^{\infty} \frac{Z^{j}}{j^{3/2}}$$
we get
$$\boxed{\left\{ \begin{align}
\frac{P}{k_{B}T}&=\frac{1}{\lambda ^{3}}g_{5/2}(Z)- \frac{1}{V}\log(1-Z) \\
\frac{1}{v}&=\frac{1}{\lambda ^{3}}g_{3/2}(Z)+ \frac{1}{V} \frac{Z}{1-Z}
\end{align} \right.}$$
##### Internal energy
The grand canonical [[internal energy]] $U$ is
$$U(Z,V,T)=-\left( \frac{ \partial  }{ \partial \beta } \log \mathcal{Z} \right)_{P,V}=-\frac{ \partial  }{ \partial \beta }  \frac{PV}{k_{B}T}$$
For fermions we have
$$U=-\frac{ \partial  }{ \partial \beta } \frac{1}{\lambda ^{3}}f_{5/2}(Z)$$
$$\frac{ \partial P }{ \partial \beta } =\frac{ \partial  }{ \partial \beta } \left( k_{B}+ \frac{1}{\lambda ^{3}}f_{5/2}(Z) \right)$$
$$\frac{U}{V}=\frac{3}{2}k_{B}+ \frac{1}{\lambda ^{3}}f_{5/2}(Z)$$
For bosons we get the same
$$\frac{U}{V}=\frac{3}{2}k_{B}+ \frac{1}{\lambda ^{3}}g_{5/2}(Z)$$
In the [[Thermodynamic limit]], these simplify down to
$$U=\frac{3}{2}k_{B}T$$
which is the classical result, satisfying the correspondence principle.
##### Free boson gas
Consider a gas of $N$ [[Particella libera (quantistica)|free]] bosons in a cubic volume $V=L^{3}$, where
$$N=\sum_{\mathbf{p}}\langle n_{\mathbf{p}} \rangle =\sum_{\mathbf{p}}= \frac{1}{e^{\beta(\varepsilon_{\mathbf{p}}-\mu)}-1}$$
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
We want to solve this integral[^1]. In fact, we mostly want to see if there is a critical temperature $T_{C}\neq 0$ such that ???. To solve the integral, we define
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


[^1]: Also see Chapter 1 of Feynman's *Statistical Mechanics*.