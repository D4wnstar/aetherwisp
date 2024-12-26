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
#### In the microcanonical ensemble
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
#### In the canonical ensemble
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
It is possible to derive the behavior of an ideal gas using the [[quantum microcanonical ensemble]]. Like all quantum statistical systems, there are two cases: a [[Fermion|fermion]] gas and a [[Boson|boson]] gas (or a third, secret option called a Boltzmann system, where all [[Equazione agli autovalori|eigenfunctions]] are [[Stato totalsimmetrico|symmetric]], like for bosons, but counted using the corrected Boltzmann count. This essentially gives the classical results starting from the quantum description).

Consider a cube of side $L$ and volume $V=L^{3}$ filled with the ideal gas. Since the particles are non-interacting, they are [[Particella libera (quantistica)|free particles]] with non-[[Normalizzazione|normalizable]] [[Funzione d'onda|wavefunctions]] $\psi(\mathbf{r})=e^{-\mathbf{p}\cdot \mathbf{r}/\hbar}$ (a [[plane wave]]). The momentum and energy of each particle are
$$\mathbf{p}=\frac{2\pi \hbar}{L}\hat{\mathbf{n}},\qquad E=\frac{p^{2}}{2m}$$
where $p^{2}=\lvert \mathbf{p} \rvert^{2}$ and $\hat{\mathbf{n}}$ is a direction in space. In one dimension, from the momentum we get
$$p_{x}L=2\pi n_{x}\hbar$$
We need the [[Equazione di Schrödinger|time-independent Schrödinger equation]] $H\ket{\psi}=E\ket{\psi}$, which in [[Rappresentazioni dello stato|position representation]] reads
$$-\hbar ^{2}\frac{ \partial ^{2} }{ \partial x^{2} } \psi(x) =E\psi(x) $$
We can approximately solve this [[equazione differenziale ordinaria|ODE]] by partitioning space into a $\Delta$-sized intervals:
$$\frac{ \partial  }{ \partial x^{2} }\psi\simeq \frac{ \frac{\psi_{i+1}-\psi_{i}}{\Delta}- \frac{\psi_{i}-\psi_{i-1}}{\Delta}}{\Delta}=\frac{\psi_{i+1}+\psi_{i-1}-2\psi_{i}}{\Delta}$$
where $\psi_{i}$ is the value of $\psi$ in the $i$-th interval. The full equation now reads
$$- \frac{\hbar^{2}}{2m\Delta ^{2}}(\psi_{i+1}+\psi_{i-1}-2\psi_{i})=E\psi_{i}$$
We can the wavefunctions to get ??? (TODO: Rewatch lesson from 22/11/2024, about 30-35 minutes in). In order to fully solve the ODE however, we need some boundary conditions. What we can use is set the value on the edges of the cube. Specifically, we can set a [[periodic boundary condition]] so that at the edge, the wavefunction "loops":
$$\psi(x)=\psi(x+L)$$
We can also define **occupation numbers** $\{ n_{\mathbf{p}} \}$, which are the number of particles in the gas that have momentum equal to exactly $\mathbf{p}$. The total number of particles is of course $N=\sum_{\mathbf{p}} n_{\mathbf{p}}$, whereas the energy is $E=\sum_{\mathbf{p}} n_{\mathbf{p}}E_{\mathbf{p}}$ This is where things start to differ for bosons and fermions:
$$n_{\mathbf{p}}=\begin{cases}
0,1&\text{fermions} \\
0,1,2,\ldots&\text{bosons}
\end{cases}$$
This a consequence of the [[Pauli exclusion principle|Pauli exclusion principle]]. The Boltzmann systems behaves like bosons. These numbers are important because they determine the possible [[stato|states]] of the system
$$\frac{N!}{\prod_{\mathbf{p}}(n_{\mathbf{p}}!)}$$
We can divide space in cells identified by an index $i$. Each cell has an average energy $E_{i}$ contains $g_{i}$ energy levels. We can call $n_{i}$ the sum of all occupation numbers $n_{\mathbf{p}}$ present in the cell and $W(\{ n_{i} \})$ the number of system states in that cell. Finally, the state counting function is $\Gamma(E)=\sum_{\{ n_{i} \}}W(\{ n_{i} \})$.

We can use this framework to calculate the [[entropy]] from $S=k_{B}\log \Gamma(E)$. What we want is an expression for $\Gamma(E)$, which means an expression for $W(\{ n_{i} \})$. We'll need to do some combinatorics. Let's call $W_{i}$ the number of possible ways $n_{i}$ particles can be assigned to $g_{i}$ energy levels (in the $i$-th cell). We can therefore express the total number of states $W(\{ n_{i} \})$ as $W(\{ n_{i} \})=\prod_{j}W_{j}$. If we find $W_{j}$, in principle we also have the entropy. These values differ greatly between fermions and bosons.

Starting from bosons, we want to divide ??? in $g_{i}-1$ divisions. So we get
$$W_{i}=\frac{(n_{i}+g_{i}-1)!}{n_{i}!(g_{i}-1)!}\quad\text{(bosons)}$$
Fermions on the other hand are much simpler as it is simply the [[Binomial theorem|binomial coefficient]]:
$$W_{i}=\begin{pmatrix}g_{i} \\ n_{i}\end{pmatrix}=\frac{g_{i}!}{n_{i}!(g_{i}-n_{i})!}\quad\text{(fermions)}$$
In the Boltzmann system, we have
$$W_{i}=\frac{1}{N!} \prod_{i}\frac{N!}{n_{i}!}g_{i}^{n_{i}}=\prod_{i}\frac{g_{i}^{n_{i}}}{n_{i}!}\quad\text{(Boltzmann gas)}$$
$g_{i}^{n_{i}}$ are all the possible ways $n_{i}$ bosons can occupy $g_{i}$ energy levels in the $i$-th cell.

Now that we have $W_{i}$, we can look back at the entropy. Assuming that fluctuations are negligible, we can remember that entropy in the microcanonical ensemble is determined entirely by a single state, so we can turn the sum of states $\sum_{i}W(\{ n_{i} \})$ into just the term that contains that state $W(\{ \bar{n}_{i} \})$ to get $S=k_{B}\log W(\{ \bar{n}_{i} \})$. However, entropy can also be expressed in [[Entropy (information theory)|information-theory]] terms as $S=\sum_{i}p_{i}\log p_{i}$. We can combine these two to solve the logarithm, using the [[Approssimazione di Stirling|Stirling approximation]]. For bosons
$$\log W=\sum_{i}[(n_{i}+g_{i}-1)\log(n_{i}+g_{i}-1)-n_{i}\log n_{i}-(g_{i}-1)\log(g_{i}-1)]$$
We can expand the entropy formula by exploiting [[Lagrange multiplier constraints]]:
$$S\to S_{\text{Lag.}}=-\sum_{x}p(x)\log p(x)+\alpha\left( \sum_{x} p(x)-1 \right)+\beta\left( \sum_{x}p(x)E(x)-E \right)$$
so
$$- \frac{d}{dn_{i}}\log W_{i}=-\sum_{i}[\log(n_{i}+g_{i}-1)+1-\log n_{i}-1]+\alpha \sum_{i}1+\beta \sum_{i}E_{i}$$
...
Finally, we can get the $\bar{n}_{i}$ for all three cases
$$\begin{align}
\bar{n}_{i}&=\frac{g_{i}}{Z^{-1}e^{\beta E_{i}}-1}&\text{(Bose-Einstein)} \\
\bar{n}_{i}&=\frac{g_{i}}{Z^{-1}e^{\beta E_{i}}+1}&\text{(Fermi-Dirac)} \\
\bar{n}_{i}&=g_{i}Ze^{-\beta E_{i}}&\text{(Maxwell-Boltzmann)}
\end{align}$$
where $Z=\sum_{x}e^{-\beta E(x)}$. We now have everything to calculate the entropy. We just need to substitute the correct $\bar{n}_{i}$ in the correct state count $W(\{ \bar{n}_{i} \})$:
$$\frac{S}{k_{B}}=\log W=\begin{align}
&\text{(Bosons) }\sum_{i} \frac{\log(\bar{n}_{i}+g_{i}-1)!}{\bar{n}_{i}(g_{i}-1)!}=\sum_{i}g_{i}\left[ \frac{\beta E_{i}-\log Z}{Z^{-1}e^{\beta E_{i}}-1} - \log(1-Ze^{-\beta E_{i}}) \right] \\
&\text{(Fermions) }\sum_{i} \frac{g_{i}!}{\bar{n}_{i}!(g_{i}-\bar{n}_{i})!} = \sum_{i}g_{i}\left[ \frac{\beta E_{i}-\log Z}{Z^{-1}e^{\beta E_{i}}+1}+ \log(1+Ze^{-\beta E_{i}}) \right]\\
&\text{(Boltzmann) } \sum_{i} \frac{g_{i}^{n_{i}}}{n_{i}!}=Z\sum_{i}g_{i}e^{-\beta E_{i}}(\beta E_{i}-\log Z)+N
\end{align}$$
If $\log g_{i}\gg 1$, the $+N$ term in the Boltzmann system can be safely ignored. It can be found that the $g_{i}$ functions are
$$\begin{align}
\text{(Bosons)}\quad g_{i}&=1 \\
\text{(Fermions)}\quad g_{i}&=1 \\
\text{(Boltzmann)}\quad g_{i}&=\frac{1}{N!} \frac{N!}{\sum_{i}n_{i}!}=\frac{1}{\sum_{i}n_{i}!}
\end{align}$$
#### Boltzmann system
We can calculate the number of particles in the Boltzmann system as
$$\begin{align}
N&=Z\sum_{i}g_{i}e^{-\beta E_{i}}=Z\sum_{\mathbf{p}}e^{-\beta E_{\mathbf{p}}}=\frac{ZV}{h ^{3}}\int e^{-\beta p^{2}/2m}d\mathbf{p}= \\
&=\frac{4\pi ZV}{h ^{3}}\int_{0}^{\infty}p^{2}e^{-\beta p^{2}/2m}dp=\frac{4\pi ZV}{h ^{3}}\int_{0}^{\infty}\sqrt{ \frac{2m}{\beta} } \frac{2m}{\beta}y^{2}e^{-y^{2}}dy= \\
&=\frac{4\pi ZV}{h ^{3}}\left( \frac{2m}{\beta} \right)^{3/2}\underbrace{ \int_{0}^{\infty}y^{2}e^{-y^{2}}dy }_{ \sqrt{ \pi }/4 }
\end{align}$$
This can be expressed in a much simpler form using the [[Formula di de Broglie|de Broglie thermal wavelength]] $\lambda$:
$$N=\frac{ZV}{\lambda ^{3}}$$
The energy ends up being
$$\begin{align}
E&=\sum E_{i}n_{i}=\sum_{i}Zg_{i}E_{i}e^{-\beta E_{i}}=Z\sum_{\mathbf{p}} \frac{\mathbf{p}^{2}}{2m}e^{-\beta p^{2}/2m}=\frac{ZV}{h^{3}}4\pi \int_{0}^{\infty}p^{2} \frac{p^{2}}{2m}e^{-\beta p^{2}/2m}dp \\
&=\frac{3}{2}k_{B}T
\end{align}$$
which is the classical result. The entropy is
$$\frac{S}{k_{B}}=Z\sum_{\mathbf{p}}e^{-\beta E_{\mathbf{p}}}(\beta E_{\mathbf{p}}-\log Z)+N$$
But this is just the [[Sackur-Tetrode equation]], which was the original classical result.
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