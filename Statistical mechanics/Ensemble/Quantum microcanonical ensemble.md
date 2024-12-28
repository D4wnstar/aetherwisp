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

Let's consider a system of $N$ non-interacting particles. We can define [[occupation number|occupation numbers]] $\{ n_{\mathbf{p}} \}$ for the momentum, which are the number of particles that are in the momentum state $\ket{\mathbf{p}}$. Since the particles are non-interacting, these are equivalent to [[Stato stazionario|energy eigenstates]] $\ket{E}$. The total number of particles is of course $N=\sum_{\mathbf{p}} n_{\mathbf{p}}$, whereas the total system energy is $E=\sum_{\mathbf{p}} n_{\mathbf{p}}\varepsilon_{\mathbf{p}}$. The energy of each state is purely [[kinetic energy|kinetic]]: $\varepsilon_{\mathbf{p}}=\lvert \mathbf{p} \rvert^{2}/2m$.

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
#### Boltzmann gas
Let's start from the unrealistic-but-useful Boltzmann system. Here, particles are neither fermions nor bosons. They are entirely classical particles with no quantum-derived restraints. As such, the method of counting their possible arrangements in the cells in immediate. Since we are trying to find how many ways there are of arranging $N$ objects (particles) into some amount of boxes (cells), the number of [[combination|combinations]] is given by the [[multinomial theorem|multinomial coefficient]]:
$$W(\{ n_{i} \})=\prod_{i}\frac{N!}{n_{i}!}g_{i}^{n_{i}}$$
$g_{i}^{n_{i}}$ is the number of possible ways we can arrange $n_{i}$ particles in $g_{i}$ states. Weighing by this number is necessary because without it, each cell would be a single box (energy state), but we have specifically designed them to contain $g_{i}$ states each, so there are $g_{i}^{n_{i}}$ more "internal" arrangements for every cell.

Unfortunately, this formula leads to a wrong result. The problem is the [[Gibbs paradox]], we would lead us to [[Intensive property|intensive]] entropy due to not considering the [[Identical particles|indistinguishability]] of particles. The solution is to divide by $N!$. As such, the correct state count is
$$W(\{ n_{i} \})=\prod_{i} \frac{g_{i}^{n_{i}}}{n_{i}!}$$
We now want the [[Entropy (information theory)|Boltzmann entropy]] $S=k_{B}\ln W$, so we need the logarithm:
$$\ln W(\{ n_{i} \})=\ln\left( \prod_{i} \frac{g_{i}^{n_{i}}}{n_{i}!}\right)=\sum_{i}[\ln g_{i}^{n_{i}}-\ln n_{j}!]$$
For large $n_{j}$ and $g_{j}$, we can use [[Stirling's approximation]]:
$$\ln W(\{ n_{i} \})\simeq \sum_{i}[\ln g_{i}^{n_{i}}-n_{i}\ln n_{i}+n_{i}]$$
The highest entropy state is found by maximizing this function. To do this, we can use [[Moltiplicatori di Lagrange|Lagrange multipliers]] (for a similar derivation, see [[Entropy from Lagrange multipliers]])[^1]. Our constraints $g_{1}$ and $g_{2}$ arise are the constant particle number and the constant energy:
$$\gamma_{1}=N-\sum_{j}n_{j},\qquad \gamma_{2}=E-\sum_{j}\varepsilon_{j}n_{j}$$
With this information, the [[Lagrangian]] to work on is
$$\begin{align}
\mathcal{L}&=\ln W+\alpha \gamma_{1}+\beta \gamma_{2} \\
&=\sum_{j}[\ln g_{i}^{n_{i}}-n_{j}\ln n_{j}]+\alpha\left(N- \sum_{j} n_{j} \right)+\beta\left( E-\sum_{j}\varepsilon_{j}n_{j} \right)
\end{align}$$
To find the maximum, we look for the stationary point
$$\begin{align}
0&=\nabla \mathcal{L}(n_{i})=\frac{d}{dn_{i}}\mathcal{L}(n_{i}) \\
&=
\end{align}$$
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
$$\gamma_{1}=N-\sum_{j}n_{j},\qquad \gamma_{2}=E-\sum_{j}\varepsilon_{j}n_{j}$$
With this information, the [[Lagrangian]] to work on is
$$\begin{align}
\mathcal{L}&=\ln W+\alpha \gamma_{1}+\beta \gamma_{2} \\
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
$$\bar{n}_{j}=\frac{g_{j}}{e^{\alpha+\beta \varepsilon_{j}}+1}$$
where we wrote $\bar{n}_{j}$ to remember that this is specifically the most likely/highest entropy configuration. If we can figure out what $\alpha$ and $\beta$ are, we can then substitute this back in $\ln W$ and use that to finally find the entropy. Right away, we can see a connection: this just the [[Fermi-Dirac distribution]], multiplied by $g_{j}$ and with $\alpha=-\beta \mu$ and $\beta=\beta$. In fact, if we make this substitution, we get
$$\bar{n}_{j}=\frac{g_{j}}{e^{\beta(\varepsilon_{j}-\mu)}+1}$$
Actually proving this requires quite a few more calculations. For the full derivation, see below.
#### Bosons
Bosons require more attention than fermions because we can't rely on the exclusion principle. To figure out how many possible arrangements each cell can be put in, notice how the presences of $g_{j}$ distinct energy levels creates $g_{j}-1$ partitions in each cell. While we can't modify the energy levels themselves, we can order them however we want to rearrange the partitions, keeping the particles where they are. This is a way of cycling through every possible arrangement of particle numbers. The number of ways to populate the cell with $n_{j}$ bosons is to throw them into the cell in any order (they will distribute themselves in the partitions) and then count the number of possible arrangements obtainable by [[permutazione|permutations]] of $n_{j}$ bosons with $g_{j}-1$ partitions[^2]. These are
$$w_{j}(n_{j})=\frac{(n_{j}+g_{j}-1)!}{n_{j}!(g_{j}-1)!}$$
We need the logarithm
$$\begin{align}
\ln W&=\ln\left[  \prod_{j}\frac{(n_{j}+g_{j}-1)!}{n_{j}!(g_{j}-1)!} \right] \\
&=\sum_{j}\ln\left[ \frac{(n_{j}+g_{j}-1)!}{n_{j}!(g_{j}-1)!} \right] \\
&=\sum_{j}[\ln(n_{j}+g_{j}-1)!-\ln n_{j}!-\ln(g_{j}-1)!] \\
\text{(Stirling's appr.)}&\simeq\sum_{j}[(n_{j}+g_{j}-1 )\ln(n_{j}+g_{j}-1)-n_{j}\ln n_{j}-(g_{j}-1)\ln(g_{j_{1}}-1)] \\
(g_{j}-1\simeq g_{j})&\simeq \sum_{j}[(n_{j}+g_{j})\ln(n_{j}+g_{j})-n_{j}\ln n_{j}-g_{j}\ln g_{j}]
\end{align}$$
We maximize with Lagrange multipliers again under the same constraints.
$$\begin{align}
\mathcal{L}&=\ln W+\alpha \gamma_{1}+\beta \gamma_{2} \\
&=\sum_{j}[(n_{j}+g_{j})\ln(n_{j}+g_{j})-n_{j}\ln n_{j}-g_{j}\ln g_{j}]+\alpha\left( N-\sum_{j}n_{j} \right)+\beta\left( E-\sum_{j}\varepsilon_{j}n_{j} \right)
\end{align}$$
$$\begin{align}
\frac{d\mathcal{L}}{dn_{j}}&=0 \\
&=\sum_{j}\left[ \frac{d}{dn_{j}}(n_{j}+g_{j})\ln(n_{j}+g_{j})- \frac{d}{dn_{j}}n_{j}\ln n_{j} \right]-\alpha \sum_{j} \frac{d}{dn_{j}}n_{j}-\beta \sum_{j}\varepsilon_{j} \frac{d}{dn_{j}}n_{j} \\
&=\sum_{j}[\ln(n_{j}+g_{j})+1-\ln n_{j}-1]-\alpha \sum_{j}1-\beta \sum_{j}\varepsilon_{j} \\
&=\sum_{j}\left[ \ln\left( \frac{n_{j}+g_{j}}{n_{j}} \right)-\alpha-\beta \varepsilon_{j} \right]
\end{align}$$
All terms are independent of each other, so
$$\ln\left( \frac{n_{j}+g_{j}}{n_{j}} \right)-\alpha-\beta \varepsilon_{j}=0$$
Extracting the $n_{j}$ we get
$$\bar{n}_{j}=\frac{g_{j}}{e^{\alpha+\beta \varepsilon_{j}}-1}$$
Similarly to before, this is the [[Bose-Einstein distribution]] with $\alpha=-\beta \mu$ and $\beta=\beta$.
#### Determining the parameters
Now we want to determine what $\alpha$ and $\beta$ are. Since the two distributions differ only by a sign, we can deal with both of them together by writing
$$n_{j}=\frac{g_{j}}{e^{\alpha+\beta \varepsilon_{j}}\pm 1}$$
$+$ is for fermions, $-$ is for bosons. The total number of particles is
$$N=\sum_{j}n_{j}=\sum_{j} \frac{g_{j}}{e^{\alpha+\beta \varepsilon_{j}}\pm 1}$$
Here we finally drop the cell notation. Remember that each cell contains $g_{j}$ states $\ket{\mathbf{p}}$. Thus, as sum over cells weighed by $g_{j}$ is the same as a sum over the states themselves
$$\sum_{j}g_{j}\equiv \sum_{\mathbf{p}}$$
where $\mathbf{p}$ is the momentum that identifies the state. Thus we can say
$$N=\sum_{\mathbf{p}} \frac{1}{e^{\alpha+\beta \varepsilon_{p}}\pm 1}$$
where $p=\lvert \mathbf{p} \rvert$. Remember that we've known $\varepsilon_{\mathbf{p}}$ since the very beginning: $\varepsilon_{\mathbf{p}}=\lvert \mathbf{p} \rvert^{2}/2m$.

To reach $\alpha$ and $\beta$, we can move to the [[thermodynamic limit]], in which we look for the particle density $n=N/V$ and the sum becomes an integral. Since integration changes the dimensions, we add a constant $h$ with the dimensions of an [[angular momentum]] to correct them[^3]:
$$\begin{align}
n&=\int \frac{1}{h^{3}} \frac{1}{e^{\alpha+\beta \varepsilon_{p}}\pm 1} \ d^{3}p \\
\text{(Spherical coords.)}&=\frac{1}{h^{3}}\int _{0}^{2\pi} \ d\theta \int_{0}^{\pi}\sin \phi\ d\phi \int_{0}^{\infty} \frac{1}{e^{\alpha+\beta \varepsilon_{p}}\pm 1} p^{2}\ dp \\
&=\frac{4\pi}{h^{3}}\int_{0}^{\infty} \frac{p^{2}}{e^{\alpha+\beta \varepsilon_{p}}\pm 1} dp
\end{align}$$
To understand the change to [[spherical coordinates]], consider this: the previous sum occurs over all of the momenta in the ensemble. When we change to integration, we integrate over all momenta in the ensemble. But the integral tells us the number of particles (well, density) in a certain range of momenta, so if we integrate over a range that no particle is in, we get zero. So, we can trivially extend the integral from all momenta in the ensemble to all space. Anything that's not present will cancel out anyway. Integration over all space can be easily done with an infinite-radius [[palla|sphere]].

We now make the substitution $\beta \varepsilon_{p}=x^{2}$, which gives us $p=x\sqrt{ 2m/\beta }$. The integral becomes
$$n=\frac{4\pi}{h^{3}}\left( \frac{2m}{\beta} \right)^{3/2} \int_{0}^{\infty} \frac{x^{2}}{e^{\alpha+x^{2}}\pm 1}dx$$
To make physical sense, the density needs to remain finite even when $\beta\to 0$, despite $\beta$ being at the denominator. For that to be true, the integral needs to go to zero, which means the denominator needs to go to infinity:
$$\lim_{ \beta \to 0 } e^{\alpha+x^{2}}=\lim_{ \beta \to 0 } e^{\alpha}=\infty$$
where we omitted the $\pm 1$ since it makes no difference. The second term is because $\lim_{ \beta \to 0 }x^{2}=\lim_{ \beta \to 0 }\beta \varepsilon_{p}=0$. In this limit we have
$$\lim_{ \beta \to 0 } n_{\mathbf{p}}=\frac{1}{e^{\alpha+x^{2}}}=\frac{1}{e^{\beta \varepsilon_{p}+\alpha}}$$
But this is precisely the [[Maxwell-Boltzmann statistic]]. So we found that our system (this time the whole system, not just an imaginary cell) is correctly described by the classical statistic for state occupation. Thus, we can definitively state that $\alpha=-\beta \mu$ and $\beta=\beta=1/k_{B}T$, with $\mu$ the [[chemical potential]], $k_{B}$ the [[Boltzmann constant]] and $T$ the [[temperature]]. We can also define the [[fugacity]] as $z=e^{-\alpha}=e^{\beta \mu}$. With this, we can write the final distribution
$$\boxed{n_{\mathbf{p}}=\frac{1}{z^{-1}e^{\beta \varepsilon_{p}}+c}\quad\text{where}\quad c=\begin{cases}
+1\quad&\text{fermions} \\
-1\quad&\text{bosons} \\
0\quad&\text{classical/high temperature}
\end{cases}}$$

Notice how both quantum distributions converge to the same classical distribution at low $\beta$/high temperatures. This is because the higher the temperature gets, the more excited states become available, but the particle number remains the same. This means that the average occupation of the states becomes progressively lower and lower until it is so low that the [[Pauli exclusion principle]] does not even need to apply (there are so many available states compared to fermions that they don't need to compete on which occupies a state). With the principle gone, bosons and fermions end up behaving the same, which is why we get the same distribution for both.
#### Entropy
Now that we have the distributions, we can use them to find the $\ln W$ and then $S=k_{B}\ln W$ for both fermions and bosons. For brevity, we call $z^{-1}e^{\beta \varepsilon_{p}}=\xi$, which makes the distributions into
$$n_{\mathbf{p}}=\frac{1}{\xi\pm 1}$$
The fermion $\ln W$ is
$$\ln W(\{ n_{i} \})\simeq \sum_{j}[g_{j}\ln g_{j}-n_{j}\ln n_{j}-(g_{j}-n_{j})\ln(g_{j}-n_{j})]$$
We are now working with the states themselves instead of the cells, so we can swap the sum over cells to a sum over states, in which $g_{j}=1$:
$$\begin{align}
\ln W(\{ n_{\mathbf{p}} \})&=\sum_{\mathbf{p}}[-n_{\mathbf{p}}\ln n_{\mathbf{p}}-(1-n_{\mathbf{p}})\ln(1-n_{\mathbf{p}})] \\
&=\sum_{\mathbf{p}}\left[ \frac{1}{\xi+1}\ln(\xi+1)- \frac{\xi}{\xi+1}\ln\left( \frac{\xi}{\xi+1} \right) \right]
\end{align}$$
For bosons we have
$$\ln W(\{ n_{i} \})=\sum_{j}[(n_{j}+g_{j})\ln(n_{j}+g_{j})-n_{j}\ln n_{j}-g_{j}\ln g_{j}]$$
which becomes
$$\begin{align}
\ln W(\{ n_{i} \})&=\sum_{\mathbf{p}}[(n_{j}+1)\ln(n_{j}+1)-n_{j}\ln n_{j}] \\
&=\sum_{\mathbf{p}}\left[ \frac{1}{\xi-1}\ln(\xi-1)+ \frac{\xi}{\xi-1}\ln\left( \frac{\xi}{\xi-1} \right) \right]
\end{align}$$
We can combine them to write
$$\ln W(\{ n_{i} \})=\sum_{\mathbf{p}}\left[ \frac{1}{\xi\pm 1}\ln(\xi\pm 1)\mp \frac{\xi}{\xi\pm 1}\ln\left( \frac{\xi}{\xi \pm 1} \right) \right]$$
Our entropy therefore is
$$\boxed{S=k_{B}\sum_{\mathbf{p}}\left[ \frac{1}{\xi\pm 1}\ln(\xi\pm 1)\mp \frac{\xi}{\xi\pm 1}\ln\left( \frac{\xi}{\xi \pm 1} \right) \right]}$$
#### Boltzmann gas properties
Despite being inaccurate at a quantum level, a Boltzmann gas can still give us useful results at high temperatures. We can do a similar thing as we did when determining the parameters. We can calculate the number of particles in the Boltzmann system as
$$N=\sum_{\mathbf{p}}n_{p}$$
Boltzmann gases use the classical [[Maxwell-Boltzmann statistic]] that we found in the high temperature limit, so
$$N=\sum_{\mathbf{p}} \frac{1}{z^{-1}e^{\beta \varepsilon_{p}}}=\sum_{\mathbf{p}}ze^{-\beta \varepsilon_{p}}$$
The deceptively important part here is the second step. Since there is no $\pm 1$, we can bring everything up to the numerator. When we jump into the thermodynamic limit to get the particle density, the integral can now be solved pretty easily:
$$\begin{align}
n&=\frac{z}{h ^{3}}\int e^{-\beta \varepsilon_{p}}d^{3}p \\
\text{(spherical coords.)}&=\frac{4\pi z}{h ^{3}}\int_{0}^{\infty}p^{2}e^{-\beta \varepsilon_{p}}dp \\
(\beta \varepsilon_{p}=x^{2})&=\frac{4\pi z}{h ^{3}}\int_{0}^{\infty}\sqrt{ \frac{2m}{\beta} } \frac{2m}{\beta}x^{2}e^{-x^{2}}dx \\
&=\frac{4\pi z}{h ^{3}}\left( \frac{2m}{\beta} \right)^{3/2} \int_{0}^{\infty}x^{2}e^{-x^{2}}dx \\
\end{align}$$
The remaining integral is (half of) a [[Gaussian integral]], the solution of which is $\sqrt{ \pi }/4$, so we get
$$n=\frac{4\pi z}{h^{3}}\left( \frac{2m}{\beta} \right)^{3/2} \frac{\sqrt{ \pi }}{4}$$
This can be expressed in a much simpler form using the [[Formula di de Broglie|de Broglie thermal wavelength]] $\lambda$:
$$n=\frac{z}{\lambda ^{3}}$$
Notice that in the boson/fermion cases, we never actually solved the integral. Here on the other hand, it ended up being pretty straight-forward and because of that, finding the particle density (and maybe the number of particles, if the volume is known) for a classical gas is just a matter of putting in the numbers.

In a similar fashion, we can find the energy:
$$U=\sum_{\mathbf{p}}\varepsilon_{p}n_{p}=\sum_{\mathbf{p}}\varepsilon_{p}ze^{-\beta\varepsilon_{p}}$$
In the thermodynamic limit, we temporarily use the volume $V$ to find the energy:
$$\begin{align}
U&=\frac{Vz}{h^{3}}\int \varepsilon_{p}e^{-\beta \varepsilon_{p}}\ d^{3}p \\
\text{(sperhical coords.)}&=\frac{4\pi Vz}{h^{3}}\int_{0}^{\infty}p^{2}\varepsilon_{p}e^{-\beta \varepsilon_{p}}\ dp \\
&= \frac{4\pi Vz}{2mh^{3}}\int_{0}^{\infty}p^{4}e^{-\beta p^{2}/2m}\ dp \\
\text{(Gaussian integral)}&=\frac{4\pi Vz}{2mh^{3}} \frac{1}{2}\left( \frac{\beta}{2m} \right)^{5/2}\Gamma\left( \frac{5}{2} \right)\\
&=\frac{\pi Vz}{mh^{3}}\left( \frac{2m}{\beta} \right)^{5/2} \frac{3\sqrt{ \pi }}{4} \\
&=\frac{3Vz}{\cancelto{ 2 }{ 4m }} \underbrace{ \frac{\pi^{3/2}}{h^{3}}\left( \frac{2m}{\beta} \right)^{3/2} }_{ 1/\lambda^{3} } \frac{\cancel{2 m }}{\beta} \\
&=\frac{3Vz}{2\lambda ^{3}\beta} \\
\left( N=nV=\frac{zV}{\lambda ^{3}} \right)&=\frac{3N}{2\beta}
\end{align}$$
Since $1/\beta=k_{B}T$, this returns the well-known result regarding the average energy of a particle in a three dimensional ideal gas, as given by the [[equipartition theorem]]:
$$\boxed{u=\frac{U}{N}=\frac{3}{2}k_{B}T}$$

The entropy is
$$\frac{S}{k_{B}}=Z\sum_{\mathbf{p}}e^{-\beta E_{\mathbf{p}}}(\beta E_{\mathbf{p}}-\log Z)+N$$
But this is just the [[Sackur-Tetrode equation]], which was the original classical result.

:::hidden
In the Boltzmann system, we have
$$W_{i}=\frac{1}{N!} \prod_{i}\frac{N!}{n_{i}!}g_{i}^{n_{i}}=\prod_{i}\frac{g_{i}^{n_{i}}}{n_{i}!}\quad\text{(Boltzmann gas)}$$
$g_{i}^{n_{i}}$ are all the possible ways $n_{i}$ bosons can occupy $g_{i}$ energy levels in the $i$-th cell.

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
:::

[^1]: Note that we are technically maximizing $\ln W$ here, not $S$. However, since $S=k_{B}\ln W$, they share maxima, so the result is the same.

[^2]: Think of it like this. Imagine you have four buckets and some marbles. You throw the marbles in the buckets randomly. Now each bucket contains some number of marbles, say $n_{1}$, $n_{2}$, $n_{3}$ and $n_{4}$. You want to know how many other outcomes you could have had if those same marbles counts ended up in different buckets. Like for example, if instead of $(n_{1},n_{2},n_{3},n_{4})$ you ended up with $(n_{2},n_{1},n_{3},n_{4})$. The amounts in the buckets are the same, they're just ordered differently. This time, the amounts in bucket 1 and 2 are reversed. (Crucially, the $n$'s themselves are the same. You didn't throw them in again, you just moved the already existing amounts from one bucket to another.) There's two ways you can go about counting these possibilities. One way is to empty out two buckets and fill them back, just with reversed amounts. But here's a simpler way: just move the buckets. Instead of emptying and refilling them, just swap the actual buckets. The result is the same. Now go ahead and count in how many distinct ways you can reorder those buckets. And this is all just for one outcome of randomly throwing the marbles in, $n_{1},n_{2},n_{3},n_{4}$. You can repeat this reordering count for every single possible set of $n_{1},n_{2},n_{3},n_{4}$. But what you're doing here is finding every possible [[permutazione|permutation]] of marbles in four buckets. Now just call them bosons instead of marbles and cell partitions instead of buckets and you're good.

[^3]: $n$ has dimensions of inverse cubic length ($1/L^{3}$). The integral gives a cubic momentum. So $h$, if used at the denominator, has to be length times momentum, which is angular momentum.