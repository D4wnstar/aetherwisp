---
aliases:
  - indistinguishable
  - distinguishable
---
Two [[Particella|particles]] are said to be **identical** if all their characteristic properties (like [[Numero quantico|quantum numbers]]) are the same. Identical particles are **distinguishable** in classical mechanics, and **indistinguishable** in quantum mechanics.
### Fermions and bosons
In classical mechanics, two particles may be identical, but can always be distinguished. For instance, consider two pool balls tagged as 1 and 2. They strike each other and scatter, bouncing off. Let's call the balls after the scattering 3 and 4. Of course, these are still the same balls, with $1\to 3$ and $2\to 4$. If 1 and 2 are differently colored, it's trivial to tell which is which after the scattering. If they are colored the same, it's harder but still possible, as we can follow the motion instant-by-instant to check where each one goes, but tracing their trajectories.

Not so in quantum physics. Say the pool balls are now quantum objects. After the scattering they end up in some joint [[stato|state]] $\ket{\psi}=\ket{x_{1}=a,x_{2}=b}=\ket{ab}$. Classically, the states $\ket{ab}$ and $\ket{ba}$ would be different, as we'd be switching the positions and since the balls are distinguishable, this makes for a different end state. But due to the [[Disuguaglianza di Heisenberg|indeterminacy principle]], we can't follow trajectories in quantum physics (hell, the very *concept* of trajectory makes no sense), so our previous method of tracking movement to distinguish what happens fails. Thus, we have no proof that $\ket{ab}$ and $\ket{ba}$ are any different. What we can do is say that the two states are proportional to each other (they still arise from the same source, after all). In symbols, this means $\ket{ab}=\alpha \ket{ba}$, where $\alpha \in \mathbb{C}$. The end state is some linear combination of the two
$$\ket{\psi} =\beta \ket{ab} +\gamma \ket{ba} =\alpha[\beta \ket{ba} +\gamma \ket{ab} ]$$
We have $\beta=\alpha \gamma$ and $\gamma=\alpha \beta$, so $\alpha=\beta/\gamma=\gamma/\beta$. This implies $\alpha^{2}=1$ or $\alpha=\pm 1$. So, there are only two possible states
$$\ket{ab} =\pm \ket{ba} $$
This shows that there is a [[Parità|parity]] phenomenon going on. Sometimes, inverting the position causes the state to flip sign, other times nothing happens. This suggests the presence of two types of particles, one which undergoes parity flipping, and another which does not. These two types of particles are respectively called [[Fermion|fermions]] and [[Boson|bosons]]. Fermions flip signs and make for odd wavefunctions, bosons do not and make for even wavefunctions.

This has the remarkable outcome that fermions just can't occupy the same state as another fermion in the same system simultaneously, whereas bosons can. In fact, if $a=b$, the fermion mixed state would be
$$\ket{\psi} =\ket{aa} -\ket{aa} =0$$
Meaning, there is no such state. The two fermions *must* end up in different states $\ket{a}$ and $\ket{b}$. It doesn't matter which goes where, but it is necessary for the two to differ. Meanwhile for bosons, we get
$$\ket{\psi} =\ket{aa} +\ket{aa} =2\ket{aa} $$
so not only does the state exists, it is simply a rescaling of the original. As such, it is perfectly fine for two bosons to end up in the same state. This odd property is called the [[Pauli exclusion principle]].

> [!example] $N$ particles
> This can be readily generalized to any number of particles. Consider $N$ of them. The position [[Funzione d'onda|wavefunction]] of the system is $\psi(\mathbf{r}_{1},\mathbf{r}_{2},\ldots,\mathbf{r}_{N})$, where $\mathbf{r}_{i}$ is the position of the $i$-th particle. We can define the particle [[Operatore di scambio|switch operator]] $P$ as
>$$P\psi(\mathbf{r}_{1},\ldots,\mathbf{r}_{i},\ldots,\mathbf{r}_{j},\ldots,\mathbf{r}_{N})=\psi(\mathbf{r}_{1},\ldots,\mathbf{r}_{j},\ldots,\mathbf{r}_{i},\ldots,\mathbf{r}_{N})$$
> Of course, switching particles gets us back to the original wavefunction, so $P$ is [[Operatore unitario|unitary]] ($PP=P^{2}=1$). As with all unitary operators, applying them to a state won't change the [[Equazione agli autovalori|eigenvalues]]:
> $$H\psi=E\psi \quad\to \quad H(P\psi)=E(P\psi)$$
> If the eigenvalue is not [[Degenerazione|degenerate]], $\psi$ and $P\psi$ must describe the same state and thus be proportional to each other: $P\psi=\alpha \psi$, where $\alpha \in \mathbb{C}$. However, since $P$ is unitary, $\alpha$ must be $\pm 1$. As such, we get
> $$P\psi=\pm \psi$$
> Again, we see that switching two particles can only have two effects. Either it flips the sign of the state, or it doesn't.
### Correct Boltzmann counting
The indistinguishability of particles affects the number of unique states that are possible in a quantum system. Since particles positions can't be determined precisely, states where the only difference is how the particles are ordered all combine into a single mixed state made up of a superposition of all of these pure states. For instance, if you have two particles at positions $a$ and $b$ and you measure them, their mixed state would be
$$\ket{\psi} =\ket{ab} \pm \ket{ba} $$
(with some omitted [[Normalizzazione|normalization]] constant). This is because it is not possible to distinguish between $\ket{ab}$ and $\ket{ba}$. The sign of $\pm$ is determined by whether we are working with fermions (-) or bosons (+). Thus, when passing from classical to quantum physics, the number of states is reduced from two to one.

This can be extend to a system of $N$ particles, in which the number of identical configurations (i.e. coordinate [[permutazione|permutations]]) becomes $N!$ and so the number of distinguishable states is reduced to $1/N!$ of the classical version. This is the origin of the so called **correct Boltzmann counting**, which was needed in classical [[Ensemble|ensembles]] to solve the [[Gibbs paradox]]. The reason it is necessary even in classical statistical mechanics is because even classical ensembles deal with quantum objects such as [[Atomo|atoms]] and [[molecule|molecules]] as basic elements.