The **quantum microcanonical ensemble** is the quantum extension of the [[microcanonical ensemble]]. Its [[Matrice di densità|density matrix]] is
$$\hat{\rho}=\sum_{E<E_{n}<E+\Delta}\ket{\phi_{n}} \bra{\phi_{n}} $$
where $E$ is the [[energy]] of the system, $\Delta\ll E$ is a small energy amount to account for small fluctuations, $\ket{\phi_{n}}$ are the [[Equazione agli autovalori|eigenstates]] of the [[Physical system|system]] and $E_{n}$ are the energy eigenvalues.
### Properties
The [[entropy]] is the same as the classical case
$$S=k_{B}\log \Gamma(E)$$
where $k_{B}$ is the [[Boltzmann constant]].
### Energy levels
The energy level discussion is a bit more complicated than in the classical case. Since energy levels are discrete due to being eigenstates, there is no longer an energy continuum. However, since there are so many particles, each with their own energy, the actual global energy states are incredibly numerous and only differ from one another by tiny amounts. This has two consequences. For one, the energy states are essentially a continuum even though we are dealing with quantum eigenstates. Secondly, $\Delta$ is taken to be small with respect to $E$, but large with respect to the separation of energy levels. As such, the interval $[E,E+\Delta]$ actually contains a number of energy states, from $E_{n}$ to $E_{n+m}$ for some integers $n$ and $m$.

Compared to the general case (see [[Quantum statistical mechanics]]), the $\lvert b_{n} \rvert^{2}$ coefficients are all [[Normalizzazione|normalized]]. The counting function $\Gamma(E)$ is
$$\Gamma(E)=\sum_{n}\rho_{nn}=\text{Tr}(\hat{\rho})$$
where $\text{Tr}$ is the [[Traccia|trace]]. Notably, it does not suffer from the [[Gibbs paradox]], unlike its classical sibling.
### Derivation
Like all quantum statistical systems, there are two cases: a [[Fermion|fermion]] gas and a [[Boson|boson]] gas (or a third, secret option called a Boltzmann gas, where all [[Equazione agli autovalori|eigenfunctions]] are [[Stato totalsimmetrico|symmetric]], like for bosons, but counted using the correct Boltzmann counting. This essentially gives the classical results starting from the quantum description).

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