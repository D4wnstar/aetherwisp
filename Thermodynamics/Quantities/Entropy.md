**Entropy** $S$ is a measurement of uniformity and disorder of a system. In Clausius' words, it is the "amount of transformation of a system". In differential form it is defined as
$$dS=\frac{\delta Q_{\text{rev}}}{T}=k_{B}\ dS_\text{it}$$
where $Q_\text{rev}$ is the [[heat]] exchanged by a reversible [[thermodynamic transformation]] and $T$ is [[temperature]]. $S_\text{it}$ is the [[entropy (information theory)|information theory entropy]], which becomes thermodynamic entropy when weighed by the [[Costante di Boltzmann|Boltzmann constant]] $k_{B}$. Notably, $dS$ is an [[exact differential]], unlike $\delta Q$, which usually isn't.

Entropy is defined up to an additive constant and the difference between two [[stato|states]] $A$ and $B$ connected by a reversible transformation is
$$\Delta S=S(B)-S(A)\equiv \int_{A}^{B} \frac{\delta Q}{T}$$
By [[Clausius' theorem]], $\Delta S$ is independent of path, so long it is reversible.
### Irreversible transformations
To understand the effects of an irreversible transformation, let's define two paths, $P$ and $R$, between the same end states. $P$ is not reversible, $R$ is. The combined process $P-R$ forms an irreversible cycle. Invoking Clausius' theorem again, we know that $\int_{P-R}dQ/T\leq 0$, which in turn means
$$\int_{P} \frac{dQ}{T}\leq \int_{R} \frac{dQ}{T}=\Delta S$$
since the right-hand integral is the entropy variation defined above. In other words, for an irreversible path $P$ between $A$ and $B$, we have
$$\Delta S=S(B)-S(A)\geq \int_{A}^{B} \frac{dQ}{T}$$
If we are working in an [[Physical system|isolated system]], $dQ=0$ and so we get
$$\Delta S\geq 0$$
which means that the entropy of an isolated system can only increase or, at most, remain constant if all transformations are reversible. Since the [[Universo|Universe]] is considered and isolated system, that means that the global entropy of the Universe can only increase.
### Etymology
The word "entropy" was coined by Clausius starting from the Greek work $\tau \rho o\pi \eta$ (tropi) which means "transformation". The "en" comes from "energy". It was added as a prefix to make the word as similar as possible to energy due to them being intrinsically linked.