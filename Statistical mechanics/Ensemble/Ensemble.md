An **ensemble** or **statistical ensemble** is a collection of identical copies of a mechanical [[Physical system|system]] characterized by a **density function** $\rho(\mathbf{q},\mathbf{p},t)$ defined in the [[phase space]] of the system.

The most common ensembles are the [[microcanonical ensemble]], the [[canonical ensemble]]and the [[grand canonical ensemble]]. They differ in the following points:
- The **microcanonical** is [[Physical system|isolated]] from the environment.
- The **canonical** is not isolated and is subject to [[energy]] fluctuations. It is linked to a [[heat reservoir]] so that those fluctuations are temporary.
- The **grand canonical** is not isolated and is subject to both energy fluctuations and number of particles fluctuations. It is connected to both a heat reservoir and particle reservoir.

Notably, all ensembles are equivalent to each other in the [[thermodynamic limit]] and lead to the same physics. The choice of which to use is fundamentally just a matter of which of the above conditions are met by the studied system.
### Fundamental concept
Ensembles are fundamentally based on respecting conservation laws at a large scale. Different ensembles are derived by changing what quantities are conserved. In the microcanonical ensemble, the system is isolated and energy is conserved. In the canonical ensemble, energy is allowed to be exchanged with reservoir, but [[temperature]] is conserved. In the grand canonical ensemble, the particle number is also allowed to vary, but the chemical potential is conserved alongside the temperature. It is very much possible to do follow the same idea with other quantities to make a new ensemble. For instance, we could allow [[electric charge]] to vary and instead conserve [[electric potential]]. We can even stack multiple conservation laws on top of each other to permit different kinds of fluctuations, like in the grand canonical. For example, we could invent an ensemble where temperature and electric potential are conserved.
### Detailed description
Consider a gas of $N$ [[particella|particles]], each with position $\mathbf{q}$ and momentum $\mathbf{p}$. In three dimensions, each particles has six variables, so for a system of $N$ particles, we are working with a $6N$-dimensional [[Phase space|phase space]] $\Gamma$. This is, of course, impossible to solve analytically.

The system as a whole, when subject to known macroscopic conditions, is set in a measurable **[[Stato|macrostate]]** (the broad state of the system, like temperature and [[pressure]], as we know from thermodynamics), but internally it is correctly described by its massively more complicated **[[Stato|microstate]]** (the set of all $6N$ positions and momenta of all particles, as we know from atomic or particle physics). The set of all possible microstates is said to be an **ensemble**, which can be thought of as "variants" of the internal state that are equivalent to each other and lead to the same macroscopic state in equilibrium. In other words, an ensemble is really just a long list of all possible arrangements that a system's internal components can take. If you are familiar with [[probability]] theory, you can think of the microstate as a [[random variable]] whose [[sample space]] is the ensemble.

Each ensemble is characterized by a **density function** $\rho(\mathbf{q},\mathbf{p},t)$, with $\mathbf{q}=(q_{1},\ldots,q_{3N})$ and $\mathbf{p}=(p_{1},\ldots,p_{3N})$. Integration of this function over a region of the [[phase space]] (i.e. over $d^{3N}q\,d^{3N}p$) returns the number of [[Phase space|representative points]] (i.e. microstates) found in that region at a time $t$. In the probability theory description, $\rho$ is the [[probability density function]] associated with the microstate random variable.

Finding this density function fully determines all the properties of the ensemble. In the simplest case, it is the [[uniform distribution]], which is the case of the [[microcanonical ensemble]]. The [[Normalizzazione|normalizing]] factor of the density function is known as the [[partition function]].
### Properties
The total number of microstates in an ensemble is conserved (as is the number of representative points).

The [[probability]] per unit phase space of finding the system in $dp\,dq$ at time $t$ is
$$\text{Prob}=\frac{\rho(\mathbf{q},\mathbf{p},t)}{\int \rho(\mathbf{q},\mathbf{p},t)\,d^{3N}p\,d^{3N}q}=\frac{\rho(\mathbf{q},\mathbf{p},t)}{Z}$$
where $Z$ is the aforementioned partition function.