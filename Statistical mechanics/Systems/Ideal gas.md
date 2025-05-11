---
wiki-publish: true
aliases:
  - ideal gas law
---
An **ideal gas** is an approximate model of the behavior of a gas that holds for low density gases. It is sparse and has weak internal interactions. The dynamics are determined by the **ideal gas law**:
$$PV=Nk_{B}T=nRT=\frac{2}{3}U$$
where $P$ is the [[pressure]], $V$ is the volume occupied by the gas, $N$ is the number of [[particella|particles]] composing the gas, $k_{B}$ is the [[Boltzmann constant]], $T$ is the [[temperature]], $n$ is the number of [[mole|moles]], $R$ is the [[ideal gas constant]] and $U$ is the [[internal energy]][^1]. The first and second forms apply only to classical gases, whereas the third is also valid for quantum gases (if the particles have [[mass]]).

An ideal gas is a [[Physical system|system]] of free particles enclosed in a finite enclosure with rigid, perfectly elastic walls. The system [[Hamiltonian]] is
$$H=\sum_{i=1}^{N} \frac{\mathbf{p}^{2}_{i}}{2m}$$
### Classical thermodynamics
Many properties of the ideal gas were already derived with classical thermodynamics.
#### Heat capacity
The [[heat capacity]] by volume of a monatomic ideal gas is
$$C_{V}=\frac{3}{2}Nk_{B}$$
#### Entropy
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
#### Pressure
The pressure of an ideal gas is the average force per unit area that it exerts on the wall of its container. By calculating the energy transferred from each particle collision on the walls per unit time, we can derive the pressure directly from particle mechanics.

Take the wall to be normal to the $x$ axis and assume the wall is perfectly reflecting. When a particle of velocity $v_{x}$ hits the wall, it transfers $2p_{x}=2mv_{x}$ momentum to the wall. The total force on the wall is given by this momentum transfer multiplied by the amount of particles hitting a unit area of the wall, i.e. the particle [[flux]].

The flux is the number of particles crossing a unit area per second. If the particles are moving over $x$, this is equal to a cylinder of unit cross-section and length $v_{x}\Delta t\equiv v_{x}$, since $\Delta t=1\text{ second}$. Thus, the flux is given by
$$\Phi=v_{x}f(\mathbf{p})d\mathbf{p}$$
where $f(\mathbf{p})$ is the [[Maxwell-Boltzmann distribution]] for momentum
$$f(\mathbf{p})=n\left( \frac{\beta}{2\pi m} \right)^{3/2}e^{-\beta \lvert \mathbf{p} \rvert ^{2}/2m}$$
which is weighted by the particle density $n=N/V$. The pressure is therefore
$$P=\int_{v_{x}>0}2mv_{x}\ v_{x}f(\mathbf{p})d\mathbf{p}=m\int_{v_{x}>0}v_{x}^{2}f(\mathbf{p})d\mathbf{p}$$
Since motion in an ideal gas is isotropic, we can make the substitution
$$v_{x}^{2}=\frac{1}{3}(v_{x}^{2}+v_{y}^{2}+v_{z}^{2})=\frac{1}{3}\lvert \mathbf{v} \rvert^{2}=\frac{1}{3} \frac{\lvert\mathbf{p}\rvert^{2}}{m^{2}} $$
and so
$$P=\frac{1}{3m}\int _{v_{x}} \lvert \mathbf{p} \rvert ^{2}f(\mathbf{p})d\mathbf{p}=\frac{2}{3} \frac{U}{V}$$
which is solved with a [[Gaussian integral]]. $U$ is the [[internal energy]].
### In the classical microcanonical ensemble
The ideal gas is a simple enough system that it can be solved exactly using as the [[microcanonical ensemble]].
#### Entropy
We use the entropy given by the sigma function $S=k_{B}\log \Sigma(E)$ where
$$\Sigma(E)=\frac{1}{h^{3N}}\int\limits_{H(\mathbf{q},\mathbf{p})<E}d^{3}q_{1}\ldots d^{3}q_{N}\,d^{3}p_{1}\ldots d^{3}p_{N}$$
and $h$ is a dimensionally appropriate constant, specifically $\text{impulse}\times\text{length}$, which gives $\text{energy}\times\text{seconds}$. We put no restrictions on position, so all those integrals just amount to $V^{N}$:
$$\Sigma(E)=\left( \frac{V}{h^{3}} \right)^{N}\int\limits_{H(\mathbf{q},\mathbf{p})<E}d^{3}p_{1}\ldots d^{3}p_{N}$$
Since the energy of a free particle is $E=p^{2}/2m$, the momentum is $p=\sqrt{ 2mE }$. This momentum describes a $n$-[[Palla|ball]] of radius $R=p=\sqrt{ 2mE }$ in the momentum-only [[phase space]], but the integral finds the volume of that ball in phase space (by finding the representative points contained therein), so we can rename the integral as a function $\Omega_{3N}(R)$ which finds the volume of a $3N$-dimensional ball of radius $R$:
$$\Sigma(R)=\left( \frac{V}{h^{3}} \right)^{N}\Omega_{3N}(R)$$
In general, $\Omega_{3N}$ is
$$\Omega_{3N}(R)=\int\limits_{x_{1}^{2}+x_{2}^{2}+\ldots+x_{n}^{2}<R^{2}}dx_{1}\ldots dx_{n}$$
(in our case, $x\equiv p$). We know both $V$ and $h$ ($h$ just needs to have the correct dimensions, so might as well be $h=1 \text{ Js}$ in this case), so in order to find $\Sigma$ and therefore $S$, we just need to solve $\Omega$ in $3N$ dimensions. Thankfully, $\Omega$ can be solved generally for any integer $N$ (see [[Volume of an n-ball]]), which gives
$$\Omega_{3N}=\frac{\pi^{3N/2}}{\Gamma\left( \frac{3N}{2}+1 \right)}R^{3N}$$
where $\Gamma$ is the [[Gamma function]]. Thus, we have
$$\Sigma(R)=\left( \frac{V}{h^{3}} \right)^{N} \frac{\pi^{3N/2}}{\Gamma\left( \frac{3N}{2}+1 \right)}R^{3N}$$
and entropy
$$S=k_{B}\log \Sigma(R)$$
We can use the fact that $\Gamma(n+1)=n!$ and [[Stirling's approximation]] $\log n!=n\log n-n$ to get ([[Steps Entropy microcanonical ideal gas]])
$$\boxed{S=k_{B}N\left[ \frac{3}{2}\ln\left( \frac{4\pi m}{3h^{2}} \frac{E}{N}\right)+\ln V+ \frac{3}{2} \right]}$$
This equation is simultaneously two things: the entropy of a classical gas, and also profoundly *wrong*. Alas, this is not the entropy we were hoping for, and not because the math or the ensemble are wrong. It is wrong because the term $\ln V$ causes this entropy to not be [[Extensive property|extensive]], despite by definition needing to be so. The culprit is to be found in quantum effects, namely the [[Identical particles|indistinguishability]] of particles, which makes many (most) states equivalent to each other and therefore not appear in the entropy. In other words, our $\Sigma(E)$ function greatly overcounts states by not taking this into account. But we're working with a classical ensemble, why do quantum effects matter? See, the issue is that despite working with a classical framework, the components here are [[Atomo|atoms]], [[molecule|molecules]], subatomic particles, you name it, whatever makes up the gas, and as it happens, these *are* quantum objects by themselves and *are* subject to quantum effects. Their individual quantum quirks end up being seen at a macroscopic level too because while the whole gas isn't quantum, it's made of quantum particles. Problems like these are in the nature of statistical mechanics: if we are to derive the macroscopic from the microscopic, we cannot ignore the quirks of the microscopic world. By the way, this wrong result is generally referred to as the [[Gibbs paradox]].
### In the classical canonical ensemble
As usual, the [[canonical ensemble]] is a simpler way to obtain the same results as the microcanonical above.
#### Partition function
Let's find the [[partition function]]:
$$Q_{N}=\int \frac{e^{-\beta(\mathbf{p}_{1}^{2}+\ldots+\mathbf{p}_{N}^{2})/2m}}{h^{3N}N!} \ d^{3N}q\ d^{3N}p=\ldots$$
The [[Hamiltonian]] of the ideal gas is separable ($H=\sum_{i=1}^{N}H_{i}$), which allows us to solve the split the integral into $2N$ integrals, each in three dimensions.
$$\begin{align}
\ldots&= \frac{1}{h^{3N}N!} \int d^{3N}q\int e^{-\beta(\mathbf{p}_{1}^{2}+\ldots+\mathbf{p}_{N}^{2})/2m}d^{3N}p \\
&= \frac{1}{N!} \left( \int_{V} d^{3}q \right)^{N}\left( \int e^{-\beta \mathbf{p}^{2}/2m}d^{3}p \right)^{N}=\ldots
\end{align}$$
The first integral is just the volume $V$. The second integral can be rewritten in [[Spherical coordinates]] by noticing that there is no angular dependency, and so the two angle integrals just evaluate to $4\pi$:
$$\ldots= \frac{V^{N}}{h^{3N}N!}\left( 4\pi\int_{0}^{\infty} p^{2}e^{-\beta p^{2}/2m} \ dp  \right)^{N}=\ldots$$
This is a [[Gaussian integral]], which solves to
$$\ldots=\frac{V^{N}}{h^{3N}N!} \left( \frac{2m\pi}{\beta} \right)^{3N/2}$$
Using the [[Formula di de Broglie|de Broglie thermal wavelength]] $\lambda$, we can simplify to
$$\boxed{Q_{N}=\frac{1}{N!}\left( \frac{V}{\lambda ^{3}} \right)^{N}}$$
#### Helmholtz free energy
The partition function's logarithm is
$$\ln Q_{N}=-\ln N!+N\ln \frac{V}{\lambda ^{3}}\simeq N-N\ln N+N\ln \frac{V}{\lambda ^{3}}=N(1-\ln n\lambda ^{3})$$
where we used [[Stirling's approximation]] and the particle density $n=N/V$. The [[Helmholtz free energy]] is
$$A=- \frac{1}{\beta}\ln Q_{N}\simeq- \frac{1}{\beta}N(1-\ln (n\lambda ^{3}))=k_{B}TN[\ln(n\lambda ^{3})-1]$$
#### Entropy
The entropy comes from the [[Maxwell relations]] connecting it to the Helmholtz free energy:
$$\begin{align}
S&=-\left( \frac{ \partial A }{ \partial T }  \right)_{V} \\
&=-k_{B}N\frac{ \partial  }{ \partial T } [T(\ln(n\lambda ^{3})-1)] \\
&=-k_{B}N\left[ \ln(n\lambda ^{3})-1 + T\frac{ \partial  }{ \partial T } \ln(n\lambda ^{3}) \right] \\
&=-k_{B}N\left[ \ln(n\lambda ^{3})-1- T\frac{3}{2T} \right] \\
&=k_{B}N\left[ \frac{5}{2}-\ln(n\lambda ^{3}) \right]
\end{align}$$
which is the [[Sackur-Tetrode equation]], as expected.
### In the quantum microcanonical ensemble
It is possible to derive the behavior of an ideal gas using the [[quantum microcanonical ensemble]]. Consider a cube of side $L$ and volume $V=L^{3}$ filled with the ideal gas. Like all quantum statistical systems, there are two cases: a [[Fermion|fermion]] gas and a [[Boson|boson]] gas (actually, there's third, secret option called a Boltzmann gas, where all [[Equazione agli autovalori|eigenfunctions]] are [[Stato totalsimmetrico|symmetric]], like for bosons, but counted using correct Boltzmann counting. This essentially gives the classical results starting from the quantum description).
#### Occupation numbers
Let's consider $N$ non-interacting particles. We wish to know the [[occupation number|occupation numbers]] $\{ n_{\mathbf{p}} \}$ of the momentum states, which are the number of particles in the momentum state $\ket{\mathbf{p}}$ at a given time. Since the particles are non-interacting, these are equivalent to [[Stato stazionario|energy eigenstates]] $\ket{E}$. The total number of particles is of course $N=\sum_{\mathbf{p}} n_{\mathbf{p}}$, whereas the total system energy is $E=\sum_{\mathbf{p}} n_{\mathbf{p}}\varepsilon_{\mathbf{p}}$. The energy of each state is purely [[kinetic energy|kinetic]]: $\varepsilon_{\mathbf{p}}=\lvert \mathbf{p} \rvert^{2}/2m$.

The number of possible states is reliant on the energy/momentum [[Spettro|spectrum]] of the system (which is assumed to be discrete). However, for a large number of particles (and in the [[thermodynamic limit]]), the number of states is so high and dense that it is approximately continuous. As such, to aid the counting of the states, we can divide the quasi-continuous spectrum in clearly discrete cells identified by an index $i$. Each cell contains a large number $g_{i}$ of states. $g_{i}$ should be large, but still small enough that each cell remains unresolved at a macroscopic scale. This is because these cells are just a mental construct to make the counting easier, and should in theory disappear by the time we are done with the derivation. We name these temporary values $\varepsilon_{i}$ the energy of the cell and $g_{i}$ the cell [[Degenerazione|degeneracy]].

![[Spectrum_cell_division.png]]

We call $n_{i}$ the sum of all occupation numbers present in cell $i$, which is just the sum of all single-state occupation number $n_{\mathbf{p}}$ in the cell: $n_{i}=\sum_{\text{in cell}} n_{\mathbf{p}}$. Since this is just a regrouping of the same states, these also satisfy the constraints $N=\sum_{i}n_{i}$ and $E=\sum_{i}\varepsilon_{i}n_{i}$.

We call $\{ n_{i} \}$ the cell occupation, which is the set of all cell occupation numbers. Cell occupation describes how the system's microstate is distributed based on the cells, instead of on each individual state (which would've been $\{ n_{\mathbf{p}} \}$). It gives us information on which cells contain the most particles and which contain the fewest. As usual, there is a huge number of ways $\{ n_{i} \}$ can be arranged and, similarly to the classical microcanonical ensemble, we should expect there to be a most probable set $\{ \bar{n}_{i} \}$ which describes [[thermal equilibrium]]. The highest probability set should be the highest [[entropy]] set, as per the [[Laws of thermodynamics|second law of thermodynamics]].

Let's call $W(\{ n_{i} \})$ the number of possible combinations of $\{ n_{i} \}$. Cells are fictitious objects, so what cell each particle resides in has no real physical meaning. Thus, all cells are independent of each other and the number of total combinations is just the product of each individual cell's combinations:
$$W(\{ n_{i} \})=\prod_{j}w_{j}(n_{_{j}})$$
where $w_{j}(n_{j})$ represents the possible state arrangements of the $n_{j}$ particles of the $j$-th cell. Finally, the state counting function for a certain system energy $E$ is
$$\Gamma(E)=\sum_{\{ n_{i} \}}W(\{ n_{i} \})$$
What we need to solve the ensemble is to find all the $W(\{ n_{i} \})$, and for that we need to find all the possible $w_{j}(n_{j})$.

Realistically though, we only care about the highest-entropy state $\{ \bar{n}_{i} \}$, so
$$\Gamma=\sum_{\{ n_{i} \}}W(\{ n_{i} \})\quad\to \quad \Gamma=W(\{ \bar{n}_{i} \})$$
so what we actually need is just $W(\{ \bar{n}_{i} \})$.
##### Boltzmann gas
Let's start from the unrealistic-but-useful Boltzmann system. Here, particles are neither fermions nor bosons. They are entirely classical particles with no quantum-derived constraints on their wavefunction. As such, the method of counting their possible arrangements in the cells in immediate. Since we are trying to find how many ways there are of arranging $N$ objects (particles) into some amount of boxes (cells), the number of [[combination|combinations]] is given by the [[multinomial theorem|multinomial coefficient]]:
$$W(\{ n_{j} \})=\frac{N!}{n_{1}!n_{2}!\ldots}g_{1}^{n_{1}}g_{2}^{n_{2}}\ldots=\prod_{j}\frac{N!}{n_{j}!}g_{j}^{n_{j}}$$
$g_{j}^{n_{j}}$ is the number of possible ways we can arrange $n_{j}$ particles in $g_{j}$ states. This number is here because we are counting combinations of *cells*, but each cell internally has its own number of combinations of *particles* therein. Since we have $n_{j}$ particles in the cell and we need to be distribute them over $g_{j}$ states, this yields $w_{j}(n_{j})=g_{j}^{n_{j}}$.

Unfortunately, this formula leads to a wrong result. The problem is the classical [[Gibbs paradox]], we would lead us to [[Intensive property|intensive]] entropy due to us failing to consider the [[Identical particles|indistinguishability]] of particles. The solution, as proven in [[Identical particles#Correct Boltzmann counting]], is to divide by $N!$. As such, the correct state count is
$$W(\{ n_{j} \})=\prod_{j} \frac{g_{j}^{n_{j}}}{n_{j}!}$$
We now want the [[Entropy (information theory)|Boltzmann entropy]] $S=k_{B}\ln W$, so we need the logarithm:
$$\ln W(\{ n_{j} \})=\ln\left( \prod_{j} \frac{g_{j}^{n_{j}}}{n_{j}!}\right)=\sum_{j}[\ln g_{j}^{n_{j}}-\ln n_{j}!]=\sum_{j}[n_{j}\ln g_{j}-\ln n_{j}!]$$
For large $n_{j}$ and $g_{j}$, we can use [[Stirling's approximation]]:
$$\ln W(\{ n_{j} \})\simeq \sum_{j}[n_{j}\ln g_{j}-n_{j}\ln n_{j}+n_{j}]$$
The highest entropy state is found by maximizing this function. To do this, we can use [[Moltiplicatori di Lagrange|Lagrange multipliers]] (for a similar derivation, see [[Entropy from Lagrange multipliers]])[^2]. Our constraints $\gamma_{1}$ and $\gamma_{2}$ are particle number conservation and the energy conservation:
$$\gamma_{1}=N-\sum_{j}n_{j},\qquad \gamma_{2}=E-\sum_{j}\varepsilon_{j}n_{j}$$
With this information, the [[Lagrangian]] to work on is
$$\begin{align}
\mathcal{L}&=\ln W+\alpha \gamma_{1}+\beta \gamma_{2} \\
&=\sum_{i}[n_{i}\ln g_{i}-n_{i}\ln n_{i}+n_{i}]+\alpha\left(N- \sum_{i} n_{i} \right)+\beta\left( E-\sum_{i}\varepsilon_{i}n_{i} \right)
\end{align}$$
To find the maximum, we look for the stationary point
$$\begin{align}
0&=\nabla \mathcal{L}(n_{i})=\frac{d}{dn_{i}}\mathcal{L}(n_{i}) \\
&=\sum_{i}\left[ \frac{d}{dn_{i}}n_{i}\ln g_{i}- \frac{d}{dn_{i}}n_{i}\ln n_{i}+ \frac{d}{dn_{i}}n_{i} \right]-\alpha \sum_{i} \frac{d}{dn_{i}}n_{i}-\beta \sum_{i} \varepsilon_{i} \frac{d}{dn_{i}}n_{i} \\
&=\sum_{i}[\ln g_{i}-\ln n_{i}-1+1]-\alpha \sum_{i}1-\beta \sum_{i}\varepsilon_{i} \\
&=\sum_{i}\left[ \ln \frac{g_{i}}{n_{i}}-\alpha-\beta \varepsilon_{i} \right]
\end{align}$$
Terms are independent from each other, so the only way the sum can be zero is if each terms is individually zero:
$$\ln \frac{g_{i}}{n_{i}}-\alpha-\beta \varepsilon_{i}=0$$
which we can rearrange to get $n_{i}$:
$$\bar{n}_{i}=\frac{g_{i}}{e^{\alpha+\beta \varepsilon_{i}}}$$
where the bar over $n_{i}$ was added to remember that this is specifically the most likely/highest entropy $n_{i}$. If we can figure out what $\alpha$ and $\beta$ are, we can then substitute this back in $\ln W$ and use that to finally find the entropy. Right away, we can see a connection: this just the [[Maxwell-Boltzmann statistic]], multiplied by $g_{i}$ and with $\alpha=-\beta \mu$ and $\beta=\beta$. In fact, if we make this substitution, we get
$$\bar{n}_{i}=\frac{g_{i}}{e^{\beta(\varepsilon_{i}-\mu)}}$$
More evidence of this can be found below.
##### Fermions
A system of [[Fermion|fermions]] is solved by exploiting the fact that $n_{j}\in \{ 0,1 \}$. Inside of a given cell $j$, to place $n_{j}$ fermions in $g_{j}$ states, we choose $n_{j}$ elements out of a set of $g_{j}$ elements. What we are looking for is the number of [[combination|combinations]], which is given by the [[Binomial theorem|binomial coefficient]]:
$$w_{j}(n_{j})=\begin{pmatrix} g_{j} \\ n_{j}\end{pmatrix}=\frac{g_{j}!}{n_{j}!(g_{j}-n_{j})!}$$
Compared to the Boltzmann system, there are far fewer states, by a factor of $(g_{j}-n_{j})!$. This is the consequence of constraining the wavefunction to be [[Stato total-antisimmetrico|antisymmetric]]. Then
$$W(\{ n_{i} \})=\prod_{j} \frac{g_{j}!}{n_{j}!(g_{j}-n_{j})!}$$
We now want the [[Entropy (information theory)|Boltzmann entropy]] $S=k_{B}\ln W$, so we need the logarithm:
$$\begin{align}
\ln W(\{ n_{i} \})&=\sum_{j}\ln\left( \frac{g_{j}!}{n_{j}!(g_{j}-n_{j})!} \right) \\
&=\sum_{j}[\ln g_{j}!-\ln n_{j}!-\ln(g_{j}-n_{j})!] \\
\text{(Stirling's appr.)}&\simeq \sum_{j}[g_{j}\ln g_{j}-n_{j}\ln n_{j}-(g_{j}-n_{j})\ln(g_{j}-n_{j})]
\end{align}$$
We define our Lagrangian in the same way as before.
$$\begin{align}
\mathcal{L}&=\ln W+\alpha \gamma_{1}+\beta \gamma_{2} \\
&=\sum_{j}[g_{j}\ln g_{j}-n_{j}\ln n_{j}-(g_{j}-n_{j})\ln(g_{j}-n_{j})]+\alpha\left(N- \sum_{j} n_{j} \right)+\beta\left( E-\sum_{j}\varepsilon_{j}n_{j} \right)
\end{align}$$
Then we look for the stationary point
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
Similarly to before, this is the [[Fermi-Dirac distribution]] with $\alpha=-\beta \mu$ and $\beta=\beta$.
##### Bosons
Bosons require more attention than fermions because we can't rely on the exclusion principle. To figure out how many possible arrangements each cell can be put in, notice how the presences of $g_{j}$ distinct energy levels creates $g_{j}-1$ partitions in each cell. While we can't modify the energy levels themselves, we can order them however we want to rearrange the partitions, keeping the particles where they are. This is a way of cycling through every possible arrangement of particle numbers. The number of ways to populate the cell with $n_{j}$ bosons is to throw them into the cell in any order (they will distribute themselves in the partitions) and then count the number of possible arrangements obtainable by [[permutazione|permutations]] of $n_{j}$ bosons with $g_{j}-1$ partitions[^3]. These are
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
Now we want to determine what $\alpha$ and $\beta$ are. Since the two quantum distributions differ only by a sign, we can deal with both of them together by writing
$$n_{j}=\frac{g_{j}}{e^{\alpha+\beta \varepsilon_{j}}\pm 1}$$
$+$ is for fermions, $-$ is for bosons. The total number of particles is
$$N=\sum_{j}n_{j}=\sum_{j} \frac{g_{j}}{e^{\alpha+\beta \varepsilon_{j}}\pm 1}$$
Here we finally drop the cell notation. Remember that each cell contains $g_{j}$ states $\ket{\mathbf{p}}$. Thus, a sum over cells weighed by $g_{j}$ is the same as a sum over the states themselves
$$\sum_{j}g_{j}\equiv \sum_{\mathbf{p}}$$
where $\mathbf{p}$ is the momentum that identifies the state. Thus we can say
$$N=\sum_{\mathbf{p}} \frac{1}{e^{\alpha+\beta \varepsilon_{p}}\pm 1}$$
where $p=\lvert \mathbf{p} \rvert$. Remember that we've known $\varepsilon_{\mathbf{p}}$ since the very beginning: $\varepsilon_{\mathbf{p}}=\lvert \mathbf{p} \rvert^{2}/2m$.

To determine $\alpha$ and $\beta$, we can move to the [[thermodynamic limit]], in which we look for the particle density $n=N/V$ and the sum becomes an integral. Since integration changes the dimensions, we add a constant $h$ with the dimensions of an [[angular momentum]] to correct them[^4]:
$$\begin{align}
n&=\int \frac{1}{h^{3}} \frac{1}{e^{\alpha+\beta \varepsilon_{p}}\pm 1} \ d^{3}p \\
\text{(Spherical coords.)}&=\frac{1}{h^{3}}\int _{0}^{2\pi} \ d\theta \int_{0}^{\pi}\sin \phi\ d\phi \int_{0}^{\infty} \frac{1}{e^{\alpha+\beta \varepsilon_{p}}\pm 1} p^{2}\ dp \\
&=\frac{4\pi}{h^{3}}\int_{0}^{\infty} \frac{p^{2}}{e^{\alpha+\beta \varepsilon_{p}}\pm 1} dp
\end{align}$$
To understand the change to [[Spherical coordinates]], consider this: the previous sum occurs over all of the momenta in the ensemble. When we change to integration, we integrate over all momenta in the ensemble. But the integral tells us the number of particles (well, density) in a certain range of momenta, so if we integrate over a range that no particle is in, we get zero. So, we can trivially extend the integral from all momenta in the ensemble to all space. Anything that's not present will cancel out anyway. Integration over all space can be easily done with an infinite-radius [[Palla|sphere]].

We now make the substitution $\beta \varepsilon_{p}=x^{2}$, which gives us $p=x\sqrt{ 2m/\beta }$. The integral becomes
$$n=\frac{4\pi}{h^{3}}\left( \frac{2m}{\beta} \right)^{3/2} \int_{0}^{\infty} \frac{x^{2}}{e^{\alpha+x^{2}}\pm 1}dx$$
To make physical sense, the density needs to remain finite even when $\beta\to 0$, despite $\beta$ being at the denominator. For that to be true, the integral needs to go to zero, which means the denominator needs to go to infinity:
$$\lim_{ \beta \to 0 } e^{\alpha+x^{2}}=\lim_{ \beta \to 0 } e^{\alpha}=\infty$$
where we omitted the $\pm 1$ since it makes no difference. The second term is because $\lim_{ \beta \to 0 }x^{2}=\lim_{ \beta \to 0 }\beta \varepsilon_{p}=0$. In this limit we have
$$\lim_{ \beta \to 0 } n_{\mathbf{p}}=\frac{1}{e^{\alpha+x^{2}}}=\frac{1}{e^{\alpha+\beta \varepsilon_{p}}}$$
But this is precisely the [[Maxwell-Boltzmann statistic]]. So we found that our system (this time the whole system, not just an imaginary cell) is correctly described by the classical statistic for state occupation. Thus, we can definitively state that $\alpha=-\beta \mu$ and $\beta=1/k_{B}T$, with $\mu$ the [[chemical potential]], $k_{B}$ the [[Boltzmann constant]] and $T$ the [[temperature]]. We can also define the [[fugacity]] as $z=e^{-\alpha}=e^{\beta \mu}$. With this, we can write the final distribution
$$\boxed{n_{\mathbf{p}}=\frac{1}{z^{-1}e^{\beta \varepsilon_{p}}+c}\quad\text{where}\quad c=\begin{cases}
+1\quad&\text{fermions} \\
-1\quad&\text{bosons} \\
0\quad&\text{classical/high temperature}
\end{cases}}$$

Notice how both quantum distributions converge to the same classical distribution at low $\beta$/high temperatures. This is because the higher the temperature gets, the more excited states become available, but the particle number remains the same. This means that the average occupation of the states becomes progressively lower and lower until it is so low that the [[Pauli exclusion principle]] does not even need to apply (there are so many available states compared to fermions that they don't need to compete on which occupies a state). With the principle gone, bosons and fermions end up behaving the same, which is why we get the same distribution for both.
#### Pressure
For pressure, we can use a similar discussion as in the classical ideal gas (see [[Ideal gas#Pressure]]). The pressure is given the momentum transferred by a collision between a particle and a wall, times the [[flux]] of those particles on the wall. We found that to be
$$P=\int_{v_{x}>0}2mv_{x}\ v_{x}f(\mathbf{p})d\mathbf{p}=m\int_{v_{x}>0}v_{x}^{2}f(\mathbf{p})d\mathbf{p}$$
where $f(\mathbf{p})$ is the [[Maxwell-Boltzmann distribution]] for momentum, scaled by the particle density. We can instead express this distribution through the appropriate statistics by stating
$$f(\mathbf{p})=\frac{n_{\mathbf{p}}}{h^{3}}$$
If motion is isotropic, we can say
$$v_{x}^{2}=\frac{1}{3}(v_{x}^{2}+v_{y}^{2}+v_{z}^{2})=\frac{1}{3}\lvert \mathbf{v} \rvert^{2} $$
which means
$$P=\frac{2}{3}\int \frac{1}{h^{3}} \frac{\varepsilon_{\mathbf{p}}}{z^{-1}e^{\beta \varepsilon_{\mathbf{p}}}\pm 1} \ d\mathbf{p}=\frac{8\pi}{3h^{3}}\int_{0}^{\infty} \frac{p^{2}\varepsilon_{\mathbf{p}}}{z^{-1}e^{\beta \varepsilon_{p}}\pm 1}dp$$
using spherical coordinates. With the substitution $\beta \varepsilon_{p}=x^{2}$ we get $p=x\sqrt{ 2m/\beta }$ and $dp=\sqrt{ 2m/\beta }\ dx$. Plugging this in we see
$$P=\frac{8\pi}{3h^{3}}\left( \frac{2m\pi}{\beta} \right)^{3/2} \frac{1}{\beta}\int_{0}^{\infty} \frac{x^{4}}{z^{-1}e^{x^{2}}\pm 1}dx=\frac{8}{3\sqrt{ \pi }} \frac{1}{\lambda ^{3}\beta}\int_{0}^{\infty} \frac{x^{4}}{z^{-1}e^{x^{2}}\pm 1}dx$$
Unfortunately, this cannot be solved analytically, but this expression is still useful in some instances.
#### Internal energy
The internal energy is given by
$$U=\sum_{\mathbf{p}}\varepsilon_{p}n_{p}=\sum_{\mathbf{p}} \frac{\varepsilon_{p}}{z^{-1}e^{\beta\varepsilon_{p}}\pm 1}\quad \to \quad \frac{V}{h^{3}}\int \frac{\varepsilon_{p}}{z^{-1}e^{\beta \varepsilon_{p}}\pm 1} \ d\mathbf{p} $$
We also cannot solve this, but we can do the usual spherical-coordinates-into-$\beta \varepsilon_{p}=x^{2}$-substitution procedure to end up with an integral that we can directly compare to the pressure above. Doing so leads us this remarkable result:
$$\boxed{PV=\frac{2}{3}U}$$
This is the ideal gas law, the classical one. It might be in a somewhat unfamiliar form, but if we use the classical [[equipartition theorem]] (or the Boltzmann gas, see below) we can state $U=3N/2\beta$, which when put in returns $PV=N/\beta=Nk_{B}T$. Of course, *this* form does not apply in the quantum case, as the equipartition theorem is for classical gases only, but the more generic, internal-energy-based one *does* apply. This is a fascinating result because it's one of the few cases where a quantum system directly inherits classical behavior. The reason it remains the same is that the only physical dependency behind this law is for 3D motion to satisfy $\varepsilon_{p}\propto \mathbf{p}^{2}$, which is true for all free particles, regardless of them being classical or quantum.
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
$$S=k_{B}\sum_{\mathbf{p}}\left[ \frac{1}{\xi\pm 1}\ln(\xi\pm 1)\mp \frac{\xi}{\xi\pm 1}\ln\left( \frac{\xi}{\xi \pm 1} \right) \right]$$
This can be proven to lead to the following results:
$$\boxed{\frac{S}{k_{B}}=\log W=\begin{align}
&\text{(Boson) }\sum_{i} \frac{\log(\bar{n}_{i}+g_{i}-1)!}{\bar{n}_{i}(g_{i}-1)!}=\sum_{i}g_{i}\left[ \frac{\beta E_{i}-\log z}{z^{-1}e^{\beta E_{i}}-1} - \log(1-ze^{-\beta E_{i}}) \right] \\
&\text{(Fermion) }\sum_{i} \frac{g_{i}!}{\bar{n}_{i}!(g_{i}-\bar{n}_{i})!} = \sum_{i}g_{i}\left[ \frac{\beta E_{i}-\log z}{Z^{-1}e^{\beta E_{i}}+1}+ \log(1+ze^{-\beta E_{i}}) \right]\\
&\text{(Boltzmann) } \sum_{i} \frac{g_{i}^{n_{i}}}{n_{i}!}=z\sum_{i}g_{i}e^{-\beta E_{i}}(\beta E_{i}-\log z)+N
\end{align}}$$
If $\log g_{i}\gg 1$, the $+N$ term in the Boltzmann system can be safely ignored. It can be found that the $g_{i}$ functions are
$$\begin{align}
\text{(Boson)}\quad g_{i}&=1 \\
\text{(Fermion)}\quad g_{i}&=1 \\
\text{(Boltzmann)}\quad g_{i}&=\frac{1}{N!} \frac{N!}{\sum_{i}n_{i}!}=\frac{1}{\sum_{i}n_{i}!}
\end{align}$$
#### Boltzmann gas properties
Despite being inaccurate at a quantum level, a Boltzmann gas can still give us useful results at high temperatures. We can follow a similar procedure as we did when determining the parameters.
##### Particle density
We can calculate the number of particles in the Boltzmann system as
$$N=\sum_{\mathbf{p}}n_{p}$$
Using the Maxwell-Boltzmann statistic that we found yields
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
$$\boxed{n=\frac{z}{\lambda ^{3}}}$$
Notice that in the boson/fermion cases, we never actually solved the integral. Here on the other hand, it ended up being pretty straight-forward. Using the quantum grand canonical ensemble (see [[Ideal gas#In the quantum grand canonical ensemble|below]]), one can prove that this is actually the leading order approximation of the quantum ideal gas density for both fermions and bosons.
##### Internal energy
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
##### Entropy
Using the Boltzmann gas $\ln W$, the entropy is
$$\begin{align}
S&=k_{B}\ln W \\
&=k_{B}\sum_{i}[n_{i}\ln g_{i}-n_{i}\ln n_{i}+n_{i}] \\
&=k_{B}\sum_{i}n_{i}[\ln g_{i}-\ln n_{i}+1]
\end{align}$$
The distribution is
$$n_{i}=g_{i}ze^{-\beta \varepsilon_{i}}=g_{i}\varphi$$
where $\varphi=ze^{-\beta \varepsilon_{i}}$ for convenience. We get
$$\begin{align}
S&=k_{B}\sum_{i}g_{i}\varphi[\ln g_{i}-\ln(g_{i}\varphi)+1] \\
&=k_{B}\sum_{i}g_{i}\varphi[\cancel{ \ln g_{i} }-\cancel{ \ln g_{i} }-\ln \varphi+1] \\
\left( \sum_{i}g_{i}\equiv \sum_{\mathbf{p}} \right)&=k_{B}\sum_{\mathbf{p}}\varphi[1-\ln \varphi] \\
&=k_{B}\sum_{\mathbf{p}}ze^{-\beta \varepsilon_{p}}[1-\ln z+\beta \varepsilon_{p}] \\
&=k_{B}\sum_{\mathbf{p}}ze^{-\beta \varepsilon_{p}}[\beta \varepsilon_{p}-\ln z]+k_{B}\sum_{\mathbf{p}}\underbrace{ ze^{-\beta \varepsilon_{p}} }_{ n_{p} } \\
&=k_{B}z\sum_{\mathbf{p}}e^{-\beta \varepsilon_{p}}[\beta \varepsilon_{p}-\ln z]+k_{B}N
\end{align}$$
This isn't very meaningful in the current form, but we can divide by $k_{B}N$ to find an old acquaintance:
$$\begin{align}
\frac{S}{k_{B}N}&=\frac{z}{N}\sum_{\mathbf{p}}e^{-\beta \varepsilon_{p}}[\beta \varepsilon_{p}-\ln z]+1 \\
(z=n\lambda ^{3})&=\frac{z}{N}\sum_{\mathbf{p}}\beta \varepsilon_{p}e^{-\beta \varepsilon_{p}}- \frac{z}{N}\sum_{\mathbf{p}}\ln (n\lambda ^{3})e^{-\beta \varepsilon_{p}}+1 \\
&=\frac{\beta}{N}\sum_{\mathbf{p}}\varepsilon_{p}\underbrace{ ze^{-\beta \varepsilon_{p}} }_{ n_{p} }- \frac{\ln(n\lambda ^{3})}{N}\sum_{\mathbf{p}}\underbrace{ ze^{-\beta \varepsilon_{p}} }_{ n_{p} }+1 \\
&=\frac{\beta}{N}U- \frac{\ln(n\lambda ^{3})}{N}N+1 \\
\left( U=\frac{3N}{2\beta} \right)&=\frac{\beta}{N} \frac{3N}{2\beta}-\ln(n\lambda ^{3})+1 \\
&=-\ln(n\lambda ^{3})+ \frac{5}{2}
\end{align}$$
This is the [[Sackur-Tetrode equation]], just as we should expect from a classical ideal gas.
### In the quantum canonical ensemble
In the [[quantum canonical ensemble]], analytic calculation is actually often not possible. The reason is that the summation in the quantum canonical partition function $Q_{N}$ is tough to solve. In fact, given the sets of [[Occupation number|occupation numbers]] $\{ n \}$ identified by some quantity (say, momentum $\mathbf{p}$), we have
$$Q_{N}(V,T)=\text{Tr}\hat{\rho}=\sum_{\substack{\{ n \} \\ \sum_{p}n_{p}=N}}e^{-\beta E(\{ n \})}$$
where the sum happens over all sets $\{ n \}$ constrained by $\sum_{\mathbf{p}}n_{\mathbf{p}}=N$. It is this constraint that makes the sum so hard to manage, along with all thermodynamic quantities. That said, it is possible in some cases where the states are cleanly ordered and labeled, such as in a [[Oscillatore armonico quantistico|quantum harmonic oscillator]]. In that case, one must make sure to abide by the wavefunction constraints and their effects on state counting. More discussion on this in the [[Partition function#Properties]] page.
### In the quantum grand canonical ensemble
The [[quantum grand canonical ensemble]] works just fine however. The quantum grand partition function is
$$\mathcal{Z}(z,V,T)=\sum_{N=0}^{\infty} z^{N}Q_{N}(V,T)=\sum_{N=0}^{\infty} \sum_{\substack{\{ n \} \\ \sum_{p}n_{p}=N}}z^{N}e^{-\beta E(\{ n \})}$$
where the inner sum satisfies $\sum_{\mathbf{p}}n_{\mathbf{p}}=N$ (see quantum canonical ensemble above). The important part in this equation is that the two sums can be merged, removing the inner sum's constraint:
$$\sum_{N=0}^{\infty}\ \sum_{\substack{\{ n \} \\ \sum_{p}n_{p}=N}}\equiv \sum_{\{ n \}}$$
This is because constraining to a specific $N$ no longer matters when you are summing over all possible $N$'s, leaving us with the same sum as the canonical ensemble, but over every possible set, not just ones whose total is $N$. As such, representing the sums as separate or single is just a matter of preference over how you group the terms, just like how $a+b+c+d$ is the same as $(a+b)+(c+d)$. Thus
$$\mathcal{Z}(z,V,T)=\sum_{\{ n \}}z^{N}e^{-\beta E(\{ n \})}=\ldots$$
with no constraint. We can use the property $e^{\sum n}=\prod_{n}e^{n}$ to rewrite both terms, since both $N$ and $E(\{ n \})$ are sums:
$$\begin{align}
\ldots&=\sum_{\{ n \}}\prod_{\mathbf{p}}z^{n_{\mathbf{p}}}\prod_{\mathbf{p}}e^{-\beta \varepsilon_{\mathbf{p}}n_{\mathbf{p}}} \\
&=\sum_{\{ n \}}\prod_{\mathbf{p}}(ze^{-\beta \varepsilon_{\mathbf{p}}})^{n_{\mathbf{p}}} \\
&=\sum_{\{ n \}}(ze^{-\beta \varepsilon_{0}})^{n_{0}}(ze^{-\beta \varepsilon_{1}})^{n_{1}}\ldots \\
&=\sum_{n_{0}=0}^{1\text{ or }\infty} (ze^{-\beta \varepsilon_{0}})^{n_{0}}\sum_{n_{1}=0}^{1\text{ or }\infty} (ze^{-\beta \varepsilon_{1}})^{n_{1}}\ldots \\
&=\prod_{\mathbf{p}}\sum_{n_{\mathbf{p}}=0}^{1\text{ or }\infty} (ze^{-\beta \varepsilon_{\mathbf{p}}})^{n_{\mathbf{p}}}
\end{align}$$
where we momentarily expanded the product by labeling each momentum state with a number. The sum now has two possibilities, depending on whether we are dealing with fermions or bosons:
$$\boxed{\mathcal{Z}(z,V,T)=\left\{\begin{align}
\prod_{\mathbf{p}} (1+ze^{-\beta \varepsilon_{p}})&\quad\text{(Fermions)} \\
\prod_{\mathbf{p}} \frac{1}{1-ze^{-\beta \varepsilon_{p}}}&\quad\text{(Bosons)}
\end{align}\right.}$$
where the first is directly obtained and the second is from the [[Serie geometrica|geometric series]]. Now that we have the grand partition function, we can derive everything else.
#### Particle number
The average particle number is
$$\langle N \rangle =z\frac{ \partial  }{ \partial z } \mathcal{Z}(z,V,T)=\left\{\begin{align}
\left( \prod_{\mathbf{p}}(1+ze^{-\beta \varepsilon_{\mathbf{p}}}) \right)\sum_{\mathbf{p}} \frac{1}{z^{-1}e^{\beta \varepsilon_{\mathbf{p}}}+1} &\quad \text{(Fermions)} \\
\left( \prod_{\mathbf{p}} \frac{1}{1-ze^{-\beta \varepsilon_{\mathbf{p}}}} \right)\sum_{\mathbf{p}} \frac{1}{z^{-1}e^{\beta \varepsilon_{\mathbf{p}}}-1} & \quad\text{(Bosons)}
\end{align}\right\}=\mathcal{Z}\sum_{\mathbf{p}}\langle n_{\mathbf{p}} \rangle $$
found using the generalized [[Product rule]] and $e^{\sum n}=\prod_{n}e^{n}$.
#### Equation of state
The [[equation of state]] can be expressed with the grand [[partition function]] $\mathcal{Z}$ as
$$\frac{PV}{k_{B}T}=\ln \mathcal{Z}(z,V,T)=\pm\sum_{\mathbf{p}} \ln(1\pm ze^{-\beta \varepsilon_{\mathbf{p}}})$$
where $+$ is for fermions, $-$ is for bosons. Calculating the actual value is, unfortunately, not possible analytically. However, we can check the [[thermodynamic limit]] and find an approximate quantum solution.
##### Fermions
We start from
$$\frac{PV}{k_{B}T}=\ln \mathcal{Z}=\sum_{\mathbf{p}}\ln(1+ze^{-\beta \varepsilon_{\mathbf{p}}})$$
In the thermodynamic limit, we move to density (divide by $V$) and get
$$\begin{align}
\frac{P}{k_{B}T}&=\frac{1}{V}\ln \mathcal{Z}\\
&\to \frac{1}{h^{3}}\int \ln(1+ze^{-\beta p^{2}/2m})d^{3}p \\
&=\frac{4\pi}{h^{3}}\int_{0}^{\infty}p^{2}\ln(1+ze^{-\beta p^{2}/2m})\ dp \\
&=\ldots
\end{align}$$
where we used [[Spherical coordinates]] (see [[Ideal gas#Determining the parameters]] for more info). We can't solve this integral directly, but we can introduce a class of functions $f_{k}(z)$ called [[Fermi and Bose functions|Fermi functions]]. Expanding $\ln(1+x)$ in [[Serie di Taylor|Taylor series]] we find
$$\begin{align}
\ldots&=\frac{4\pi}{h^{3}}\int_{0}^{\infty}p^{2}\sum_{j=1}^{\infty} \frac{(-1)^{j+1}z^{j}e^{-j\beta\varepsilon_{p}}}{j} \\
&=\frac{4\pi}{h^{3}}\sum_{j=1}^{\infty} \frac{(-1)^{j+1}z^{j}}{j}\int_{0}^{\infty}p^{2}e^{-j\beta p^{2}/2m} \\
&=\frac{4\pi}{h^{3}}\sum_{j=1}^{\infty} \frac{(-1)^{j+1}z^{j}}{j} \frac{\sqrt{ \pi }}{4(j\beta/2m)^{3/2}} \\
&=\left( \frac{2\pi m}{\beta h^{2}} \right)^{3/2} \sum_{j=1}^{\infty} \frac{(-1)^{j+1}z^{j}}{j^{5/2}}  \\
&=\frac{1}{\lambda ^{3}}f_{5/2}(z)
\end{align}$$
where we used the [[Formula di de Broglie|de Broglie thermal wavelength]]. This gives us the equation of state of a fermion ideal gas
$$\boxed{\frac{P\lambda ^{3}}{k_{B}T}=f_{5/2}(z)}$$
This equation substitutes (and extends) the well-known classical $PV=Nk_{B}T$. Notice that volume does not make an appearance here, instead substituted by the cube of the thermal wavelength. Clearly then, a quantum gas depends not on the size of its enclosure (actually it does, just not directly), but rather on the wave properties of its components.

From the previous steps we can retroactively state
$$\int_{0}^{\infty}p^{2}\ln(1+ze^{-\beta \varepsilon_{p}})dp=\frac{\sqrt{ \pi }}{4} \left( \frac{2m}{\beta} \right)^{3/2} f_{5/2}(z)$$

The particle density is
$$\begin{align}
n&=\frac{1}{V}\sum_{\mathbf{p}}\langle n_{\mathbf{p}} \rangle  \\
&\to \frac{1}{h^{3}}\int \frac{1}{z^{-1}e^{\beta \varepsilon_{\mathbf{p}}}+ 1}d^{3}p \\
&=\frac{4\pi}{h^{3}}\int_{0}^{\infty} \frac{p^{2}}{z^{-1}e^{\beta \varepsilon_{p}}+ 1}dp \\
\text{(pull }z^{-1}e^{\beta \varepsilon_{p}}\text{ out)}&=\frac{4\pi}{h^{3}}\int_{0}^{\infty} \frac{ze^{-\beta \varepsilon_{p}}p^{2}}{ze^{-\beta \varepsilon_{p}}+1}dp \\
&=\ldots
\end{align}$$
We ideally want to reuse the previous integral. However, the integral does not look the same at all. The trick is to reverse engineer a logarithm into existence by remembering that the derivative of a logarithm is a fraction of the argument. Conveniently, the denominator here is just the argument we need:
$$\frac{ \partial  }{ \partial z } \ln(1+ze^{-\beta \varepsilon_{p}})=\frac{1}{ze^{-\beta \varepsilon_{p}}+1}e^{-\beta \varepsilon_{p}}\quad\rightarrow \quad \frac{1}{ze^{-\beta \varepsilon_{p}}+1}=e^{\beta \varepsilon_{p}}\frac{ \partial  }{ \partial z } \ln(1+ze^{-\beta \varepsilon_{p}})$$
Substituting this in the integral gives us
$$\begin{align}
\ldots&=\frac{4\pi}{h^{3}}z\int_{0}^{\infty} p^{2}e^{-\beta \varepsilon_{p}}e^{\beta \varepsilon_{p}}\frac{ \partial  }{ \partial z } \ln(1+ze^{-\beta \varepsilon_{p}}) dp\\
&=\frac{4\pi}{h^{3}}z\frac{ \partial  }{ \partial z } \int_{0}^{\infty}p^{2}\ln(1+ze^{-\beta \varepsilon_{p}})dp \\
&=\frac{4\pi}{h^{3}} \frac{\sqrt{ \pi }}{4}\left( \frac{2m}{\beta} \right)^{3/2}z\frac{ \partial  }{ \partial z } f_{5/2}(z) \\
&=\frac{1}{\lambda ^{3}}z\frac{ \partial  }{ \partial z } f_{5/2}(z)
\end{align}$$
This is pleasantly compact, but the derivative is an eyesore. Thankfully, now that we know that we are working with $f_{5/2}$, we can compute its derivative:
$$\begin{align}
\frac{ \partial  }{ \partial z } f_{5/2}(z)&=\frac{ \partial  }{ \partial z } \sum_{j=1}^{\infty} \frac{(-1)^{j+1}z^{j}}{j^{5/2}} \\
&=\sum_{j=1}^{\infty} \frac{(-1)^{j+1}}{j^{5/2}}\frac{ \partial  }{ \partial z } z^{j} \\
&=\sum_{j=1}^{\infty} \frac{(-1)^{j+1}}{j^{5/2}}jz^{j-1} \\
&=\frac{1}{z}\sum_{j=1}^{\infty} \frac{(-1)^{j+1}z^{j}}{j^{3/2}}=\frac{1}{z}f_{3/2}(z)
\end{align}$$
This result is actually a specific case of a more general recurrence relation among Fermi (and Bose) functions. It inverts to $f_{3/2}(z)=z\frac{ \partial  }{ \partial z }f_{5/2}(z)$, which very nicely exists in our previous result as-is. As such, our final formula is
$$\boxed{n=\frac{1}{\lambda ^{3}}f_{3/2}(z)}$$
##### Bosons
We start from
$$\frac{PV}{k_{B}T}=\ln \mathcal{Z}=-\sum_{\mathbf{p}}\ln(1-ze^{-\beta \varepsilon_{\mathbf{p}}})$$
The process is the same as with fermions, except we use [[Fermi and Bose functions|Bose functions]] $g_{k}$ instead. We can find
$$\frac{P}{k_{B}T}=\frac{4\pi}{h^{3}}\int_{0}^{\infty}p^{2}\ln(1-ze^{-\beta \varepsilon_{p}})\ dp$$
which resolves to
$$\boxed{\frac{P}{k_{B}T}=\frac{1}{\lambda ^{3}}g_{5/2}(z)}$$
Similarly, the particle density is
$$n=\frac{4\pi}{h^{3}}\int_{0}^{\infty} p^{2} \frac{1}{z^{-1}e^{\beta \varepsilon_{p}}}dp$$
which yields
$$\boxed{n=\frac{1}{\lambda ^{3}}g_{3/2}(z)}$$

A more precise result can be reached by taking [[Bose-Einstein condensation]] into consideration. Condensation occurs at minimal temperatures, which in turn implies minimal particle energies, $\varepsilon_{p}\to 0$. In this state, the occupation number blows up and causes a [[Singolarità isolata|singularity]], making it technically impossible to calculate the integral at the lower bound $p=0$. Because of this, we can extract the term $p=\varepsilon_{p}=0$ from the equation of state sum *before* going to integral notation, which leaves us with
$$\boxed{\frac{P}{k_{B}T}=\frac{1}{\lambda ^{3}}g_{5/2}(z)- \frac{1}{V}\ln(1-z)}$$
Similarly, the particle density is
$$\boxed{n=\frac{1}{\lambda ^{3}}g_{3/2}(z)+ \frac{1}{V} \frac{z}{1-z}}$$
Both of these terms behave like $\sim N$ when $z\ll 1$, so in the classical limit they spontaneously disappear. That said, only the additional density term is relevant. When $z$ rises towards its limiting value of $1$, the additional density term tends to blow up. At first glance, the equation of state term appears to do so too. However, notice how the number of particles in the ground state can be expressed in terms of $z$:
$$N_{0}=\langle n_{p=0} \rangle =n_{0}V=\frac{z}{1-z}$$
This is because $\lambda\to \infty$ when $p=0$[^5], so we only keep the latter term. Conversely, the other term is excited boson number
$$N_\text{exc}=\langle n_{p>0} \rangle =\frac{1}{\lambda ^{3}}g_{3/2}(z)$$
Typically, $N_\text{exc}\gg N_{0}$, but near condensation temperature, this no longer holds true. Invert the ground state number and we get
$$z=\frac{N_{0}}{N_{0}+1}$$
Among other things, this shows how closely tied ground state particle number and fugacity are in a boson gas. If we substitute this in the additional equation of state term we see
$$-\frac{1}{V}\ln\left( 1- \frac{N_{0}}{N_{0}+1} \right)=\frac{1}{V}\ln(N_{0}+1)$$
Since $V\propto N$, this entire term is $\sim \frac{1}{N}\ln N$, which disappears for large $N$.
#### Internal energy
The grand canonical [[internal energy]] $U$ is given by
$$U(z,V,T)=-\left( \frac{ \partial  }{ \partial \beta } \ln \mathcal{Z} \right)_{P,V}=-\frac{ \partial  }{ \partial \beta }  \frac{PV}{k_{B}T}$$
In the thermodynamic limit, we can use the equations of state above.
##### Fermions
For fermions we have
$$\frac{U}{V}=-\frac{ \partial  }{ \partial \beta } \frac{P}{k_{B}T}=-\frac{ \partial  }{ \partial \beta } \frac{1}{\lambda ^{3}}f_{5/2}(z)=-\left( \frac{ \partial  }{ \partial \beta } \frac{1}{\lambda ^{3}} \right)f_{5/2}(z)- \frac{1}{\lambda ^{3}}\left( \frac{ \partial  }{ \partial \beta } f_{5/2}(z) \right)$$
Computing the derivatives separately
$$\frac{ \partial  }{ \partial \beta } \frac{1}{\lambda ^{3}}=-\frac{1}{\lambda ^{3}} \frac{3}{2\beta},\qquad \frac{ \partial  }{ \partial \beta } f_{5/2}(z)=\sum_{j=1}^{\infty} \frac{(-1)^{j+1}}{j^{5/2}}\frac{ \partial  }{ \partial \beta } z^{j}=\mu\sum_{j=1}^{\infty} \frac{(-1)^{j+1}}{j^{3/2}}z^{j}=\mu f_{3/2}(z)$$
and so
$$\frac{U}{V}=\frac{3}{2\beta} \frac{f_{5/2}(z)}{\lambda ^{3}}-\mu \frac{f_{3/2}(z)}{\lambda ^{3}}=\frac{3}{2\beta}\beta P-\mu n$$
If we move $V$ over to the right side, we get
$$\boxed{U=\frac{3}{2}PV-\mu N}$$
This is identical to the classical result, which is what we want.
##### Bosons
Since the equation of state of bosons is identical to that of fermions, but with Bose functions instead of Fermi functions, the internal energy is itself identical, derived in the same way as above. It should be noted that the additional term due to condensation in the equation of state does not make a difference.

[^1]: The form $PV=nRT$ exists because, besides being convenient in a laboratory setting, thermodynamics was historically developed at a time where the existence of the [[atomo|atom]] had yet to be proven and with it, the [[Particella|particle]] division of matter. In fact, classical thermodynamics as a whole does not strictly require the existence of particles like atoms.
[^2]: Note that we are technically maximizing $\ln W$ here, not $S$. However, since $S=k_{B}\ln W$, they share maxima, so the result is the same.

[^3]: Think of it like this. Imagine you have four buckets and some marbles. You throw the marbles in the buckets randomly. Now each bucket contains some number of marbles, say $n_{1}$, $n_{2}$, $n_{3}$ and $n_{4}$. You want to know how many other outcomes you could have had if those same marbles counts ended up in different buckets. Like for example, if instead of $(n_{1},n_{2},n_{3},n_{4})$ you ended up with $(n_{2},n_{1},n_{3},n_{4})$. The amounts in the buckets are the same, they're just ordered differently. This time, the amounts in bucket 1 and 2 are reversed. (Crucially, the $n$'s themselves are the same. You didn't throw them in again, you just moved the already existing amounts from one bucket to another.) There's two ways you can go about counting these possibilities. One way is to empty out two buckets and fill them back, just with reversed amounts. But here's a simpler way: just move the buckets. Instead of emptying and refilling them, just swap the actual buckets. The result is the same. Now go ahead and count in how many distinct ways you can reorder those buckets. And this is all just for one outcome of randomly throwing the marbles in, $n_{1},n_{2},n_{3},n_{4}$. You can repeat this reordering count for every single possible set of $n_{1},n_{2},n_{3},n_{4}$. But what you're doing here is finding every possible [[permutazione|permutation]] of marbles in four buckets. Now just call them bosons instead of marbles and cell partitions instead of buckets and you're good.

[^4]: $n$ has dimensions of inverse cubic length ($1/L^{3}$). The integral gives a cubic momentum. So $h$, if used at the denominator, has to be length times momentum, which is angular momentum.
[^5]: If you are not convinced, remember that temperature is tied to kinetic energy. If you remove the momentum, and so the kinetic energy, you remove the temperature too. Since $\lambda\propto T^{-1/2}$, if $T\to0$ then $\lambda\to \infty$. In other words, ground state bosons (and particles in general, really) are "stuck" at zero temperature.