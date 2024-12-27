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

%%Consider a cube of side $L$ and volume $V=L^{3}$ filled with the ideal gas. Since the particles are non-interacting, they are [[Particella libera (quantistica)|free particles]] with non-[[Normalizzazione|normalizable]] [[Funzione d'onda|wavefunctions]] $\psi(\mathbf{r})=e^{-\mathbf{p}\cdot \mathbf{r}/\hbar}$ (a [[plane wave]]). The momentum and energy of each particle are
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
%%

Let's consider a system of $N$ non-interacting particles. We can define [[occupation number|occupation numbers]] $\{ n_{\mathbf{p}} \}$ for the momentum, which are the number of particles that are in the momentum state $\ket{\mathbf{p}}$. Since the particles are non-interacting, these are equivalent to [[Stato stazionario|energy eigenstates]] $\ket{E}$. The total number of particles is of course $N=\sum_{\mathbf{p}} n_{\mathbf{p}}$, whereas the total system energy is $E=\sum_{\mathbf{p}} n_{\mathbf{p}}E_{\mathbf{p}}$.

The number of possible states is reliant on the energy/momentum [[Spettro|spectrum]] of the system (which is assumed to be discrete). However, for a large number of particles (and in the [[thermodynamic limit]]), the number of states is so high and dense that it is approximately continuous. As such, to aid the counting of the states, we can divide the quasi-continuous spectrum in clearly discrete cells identified by an index $i$. Each cell contains a large number $g_{i}$ of states. $g_{i}$ should be large, but still small enough that each cell remains unresolved at a macroscopic scale. We call $\varepsilon_{i}$ the energy of the cell and $g_{i}$ the cell [[Degenerazione|degeneracy]]. The addition of these values is a purely mathematical tool meant to make derivation easier. They do not contain any physical meaning and should not appear in the end result.

![[Spectrum_cell_division.png]]

We can call $n_{i}$ the sum of all occupation numbers present in cell $i$, which is just the sum of all single-state occupation number $n_{\mathbf{p}}$ in the cell: $n_{i}=\sum_{\text{in cell}} n_{\mathbf{p}}$. As usual, these satisfy the constraints $N=\sum_{i}n_{i}$ and $E=\sum_{i}\varepsilon_{i}n_{i}$.

We call $\{ n_{i} \}$ the cell occupation, which is the set of all cell occupation numbers. Cell occupation describes how the system's microstate is distributed based on the cells, instead of on each individual state (which would've been $\{ n_{\mathbf{p}} \}$). It gives us information on which cells contain the most particles and which contain the fewest. As usual, there is a huge number of ways $\{ n_{i} \}$ can be arranged and, similarly to the classical microcanonical, there should be a most likely set $\{ \bar{n}_{i} \}$ which describes [[thermal equilibrium]]. This most likely set associated with a most likely [[entropy]], which according to the [[Laws of thermodynamics|second law of thermodynamics]] is the highest possible one.

Let's call $W(\{ n_{i} \})$ the number of possible combinations of $\{ n_{i} \}$. Cells are fictitious objects, so what cell each particle resides into does not mean anything, physically speaking. Thus, all cells are independent of each other and the number of total combinations is just the product of each individual cell's combinations:
$$W(\{ n_{i} \})=\prod_{j}w_{j}(n_{_{j}})$$
where $w_{j}(n_{j})$ represents the possible state arrangements of the $n_{j}$ particles of the $j$-th cell. Finally, the state counting function for a certain system energy $E$ is
$$\Gamma(E)=\sum_{\{ n_{i} \}}W(\{ n_{i} \})$$
What we need to solve the ensemble is to find all the $W(\{ n_{i} \})$, which in turn means find out all the possible $w_{j}(n_{j})$.

Realistically though, we only care about the highest-entropy state $\{ \bar{n}_{i} \}$, so
$$\Gamma=\sum_{\{ n_{i} \}}W(\{ n_{i} \})\quad\to \quad \Gamma=W(\{ \bar{n}_{i} \})$$
so what we actually need is just $W(\{ n_{i} \})$.
#### Fermions
A system of [[Fermion|fermions]] is solved by exploiting the fact that $n_{j}\in \{ 0,1 \}$. To place $n_{j}$ fermions in $g_{j}$ states, we choose $n_{j}$ elements out of a set of $g_{j}$ elements. What we are looking for is the number of [[combination|combinations]], which is given directly by the [[Binomial theorem|binomial coefficient]]:
$$w_{j}(n_{j})=\begin{pmatrix} g_{j} \\ n_{j}\end{pmatrix}=\frac{g_{j}!}{n_{j}!(g_{j}-n_{j})!}$$
and so
$$W(\{ n_{i} \})=\prod_{j} \frac{g_{j}!}{n_{j}!(g_{j}-n_{j})!}$$
We now want the [[Entropy (information theory)|Boltzmann entropy]] $S=k_{B}\ln W$, so we need the logarithm:
$$\ln W(\{ n_{i} \})=\sum_{j}\ln\left( \frac{g_{j}!}{n_{j}!(g_{j}-n_{j})!} \right)=\sum_{j}[\ln g_{j}!-\ln n_{j}!-\ln(g_{j}-n_{j})!]$$
For large $n_{j}$ and $g_{j}$, we can use [[Stirling's approximation]]:
$$\ln W(\{ n_{i} \})\simeq \sum_{j}[g_{j}\ln g_{j}-n_{j}\ln n_{j}-(g_{j}-n_{j})\ln(g_{j}-n_{j})]$$
The highest entropy state is found by maximizing this function. To do this, we can use [[Moltiplicatori di Lagrange|Lagrange multipliers]] (for a similar derivation, see [[Entropy from Lagrange multipliers]])[^1]. Our constraints $g_{1}$ and $g_{2}$ arise are the constant particle number and the constant energy:
$$g_{1}=N-\sum_{j}n_{j},\qquad g_{2}=E-\sum_{j}\varepsilon_{j}n_{j}$$
With this information, the [[Lagrangian]] to work on is
$$\begin{align}
\mathcal{L}&=\ln W+\alpha g_{1}+\beta g_{2} \\
&=\sum_{j}[g_{j}\ln g_{j}-n_{j}\ln n_{j}-(g_{j}-n_{j})\ln(g_{j}-n_{j})]+\alpha\left(N- \sum_{j} n_{j} \right)+\beta\left( E-\sum_{j}\varepsilon_{j}n_{j} \right)
\end{align}$$
To find the maximum, we look for the stationary point
$$\begin{align}
0&=\nabla \mathcal{L}(n_{j})=\frac{d}{dn_{j}}\mathcal{L}(n_{j}) \\
&=-\sum_{j} \frac{d}{dn_{j}}(n_{j}\ln n_{j})-\sum_{j} \frac{d}{dn_{j}}[(g_{j}-n_{j})\ln(g_{j}-n_{j})]-\alpha \sum_{j} \frac{d}{dn_{j}}n_{j}-\beta \sum_{j}\varepsilon_{j} \frac{d}{dn_{j}}n_{j} \\
&=-\sum_{j}(\ln n_{j}+1)+\sum_{j}[\ln(g_{j}-n_{j})+1]-\alpha \sum_{j}1-\beta \sum_{j}\varepsilon_{j} \\
&=\sum_{j}[-\ln n_{j}-1+\ln(g_{j}-n_{j})+1-\alpha-\beta \varepsilon_{j}]
\end{align}
$$
From this we get
$$-\ln n_{j}+\ln(g_{j}-n_{j})-\alpha-\beta \varepsilon_{j}=0$$
which we can rearrange to extract $n_{j}$:
$$n_{j}=\frac{g_{j}}{e^{\alpha+\beta \varepsilon_{j}}+1}$$
If we can figure out what $\alpha$ and $\beta$ are, we can then substitute this back in $\ln W$ and use that to finally find the entropy. Right away, we can see a connection: this just the [[Fermi-Dirac distribution]], multiplied by $g_{j}$ and with $\alpha=-\beta \mu$ and $\beta=\beta$. In fact, if we make this substitution, we get
$$n_{j}=\frac{g_{j}}{e^{\beta(\varepsilon_{j}-\mu)}+1}$$
Actually proving this requires quite a few more calculations. For the full derivation, see below.
#### Bosons
Bosons require more attention than fermions because we can't rely on the exclusion principle. To figure out how many possible arrangements each cell can be put in, notice how the presences of $g_{j}$ distinct energy levels creates $g_{j}-1$ partitions in each cell. While we can't modify the energy levels themselves, we can order them however we want to rearrange the partitions, keeping the particles where they are. This is a way of cycling through every possible arrangement of particle numbers. The number of ways to populate the cell with $n_{j}$ bosons is to throw them into the cell in any order (they will distribute themselves in the partitions) and then count the number of possible arrangements obtainable by [[permutazione|permutations]] of $n_{j}$ bosons with $g_{j}-1$ partitions[^2]. These are
$$w_{j}(n_{j})=\frac{(n_{j}+g_{j}-1)!}{n_{j}!(g_{j}-1)!}$$


---

Starting from bosons, we want to divide ??? in $g_{i}-1$ divisions. So we get
$$W_{i}=\frac{(n_{i}+g_{i}-1)!}{n_{i}!(g_{i}-1)!}\quad\text{(bosons)}$$
Fermions on the other hand are much simpler as it is simply the [[Binomial theorem|binomial coefficient]]:
$$W_{i}=\begin{pmatrix}g_{i} \\ n_{i}\end{pmatrix}=\frac{g_{i}!}{n_{i}!(g_{i}-n_{i})!}\quad\text{(fermions)}$$
In the Boltzmann system, we have
$$W_{i}=\frac{1}{N!} \prod_{i}\frac{N!}{n_{i}!}g_{i}^{n_{i}}=\prod_{i}\frac{g_{i}^{n_{i}}}{n_{i}!}\quad\text{(Boltzmann gas)}$$
$g_{i}^{n_{i}}$ are all the possible ways $n_{i}$ bosons can occupy $g_{i}$ energy levels in the $i$-th cell.

Now that we have $W_{i}$, we can look back at the entropy. Assuming that fluctuations are negligible, we can remember that entropy in the microcanonical ensemble is determined entirely by a single state, so we can turn the sum of states $\sum_{i}W(\{ n_{i} \})$ into just the term that contains that state $W(\{ \bar{n}_{i} \})$ to get $S=k_{B}\log W(\{ \bar{n}_{i} \})$. However, entropy can also be expressed in [[Entropy (information theory)|information-theory]] terms as $S=\sum_{i}p_{i}\log p_{i}$. We can combine these two to solve the logarithm, using the [[Approssimazione di Stirling|Stirling approximation]]. For bosons
$$\log W=\sum_{i}[(n_{i}+g_{i}-1)\log(n_{i}+g_{i}-1)-n_{i}\log n_{i}-(g_{i}-1)\log(g_{i}-1)]$$
We can expand the entropy formula by exploiting [[Entropy from Lagrange multipliers]]:
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

[^1]: Note that we are technically maximizing $\ln W$ here, not $S$. However, since $S=k_{B}\ln W$, they share maxima, so the result is the same.
[^2]: Think of it like this. Imagine you have four buckets and some marbles. You throw the marbles in the buckets randomly. Now each bucket contains some number of marbles, say $n_{1}$, $n_{2}$, $n_{3}$ and $n_{4}$. You want to know how many other outcomes you could have had if those same marbles counts ended up in different buckets. Like for example, if instead of $(n_{1},n_{2},n_{3},n_{4})$ you ended up with $(n_{2},n_{1},n_{3},n_{4})$. The amounts in the buckets are the same, they're just ordered differently. This time, the amounts in bucket 1 and 2 are reversed. (Crucially, the $n$'s themselves are the same. You didn't throw them in again, you just moved the already existing amounts from one bucket to another.) There's two ways you can go about counting these possibilities. One way is to empty out two buckets and fill them back, just with reversed amounts. But here's a simpler way: just move the buckets. Instead of emptying and refilling them, just swap the actual buckets. The result is the same. Now go ahead and count in how many distinct ways you can reorder those buckets. And this is all just for one outcome of randomly throwing the marbles in, $n_{1},n_{2},n_{3},n_{4}$. You can repeat this reordering count for every single possible set of $n_{1},n_{2},n_{3},n_{4}$. But what you're doing here is finding every possible [[permutazione|permutation]] of marbles in four buckets. Now just call them bosons instead of marbles and cell partitions instead of buckets and you're good.