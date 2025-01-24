The **microcanonical ensemble** is an [[ensemble]] whose [[probability density function]] is
$$\rho(\mathbf{q},\mathbf{p})=\begin{cases}
\text{constant} & E<H(\mathbf{q},\mathbf{p})<E+\Delta \\
0&\text{otherwise}
\end{cases}$$
where $H$ is the [[Hamiltoniana|Hamiltonian]] of the [[Physical system|system]] and $E$ is its total [[energy]]. It represents an [[Physical system|isolated system]] in [[thermal equilibrium]] whose energy $E$ is precisely defined and conserved. Given this definition, the [[equal a priori probability hypothesis]] applies to it directly, hence the constant density function.

In practice, we instead consider the system energy to be in an interval $[E,E+\Delta]$ to account for practical uncertainties in measurement, since our understanding of energy is never going to be without error. Nevertheless, $\Delta$ is to be seen as a tiny constant with respect to the energy ($\Delta\ll E$) and likewise $[E,E+\Delta]$ is a tiny interval.

It differs from the [[Canonical ensemble|canonical]] and [[Grand canonical ensemble|grand canonical ensembles]], both of which are not isolated and have energy fluctuations.
### Expectation values
Given some [[variabile dinamica|dynamical variable]] $f(\mathbf{q},\mathbf{p})$, its most likely value (the [[mode]]) is the one that $f$ takes in the largest number of systems. The [[mean]] on the other hand is the usual [[ensemble average]]:
$$\langle f \rangle = \frac{\int f(\mathbf{q},\mathbf{p})\rho(\mathbf{q},\mathbf{p})\,d^{3N}q\,d^{3N}p}{\int \rho(\mathbf{q},\mathbf{p})\,d^{3N}q\,d^{3N}p}$$
The mean and mode tend to coincide if the [[mean squared error]] of $f$ tends to zero. Empirically, the MSE is inversely proportional to the number of [[Particella|particles]] in the system $N$: $\text{MSE}\propto 1/N$. So for large $N$, the mean and the mode coincide.
### Entropy
To find the [[entropy]] function for the ensemble, let's introduce a function $\Gamma(E)$ which counts the number of states whose energy is between $E$ and $E+\Delta$:
$$\Gamma(E)=\int\limits_{E<H(\mathbf{q},\mathbf{p})<E+\Delta}d^{3N}q\,d^{3N}p$$
This function explicitly depends on $E$, but also on the number of particles $N$ (the integration variables) and the volume $V$ (in the integration limits due to $\mathbf{q}$). $\Gamma$ returns a volume in [[phase space]], which is a finite spherical shell bounded by two hypersurfaces of energies $E$ and $E+\Delta$.

Let's introduce another function $\Sigma(E)$ that counts all states with energy below $E$:
$$\Sigma(E)=\int\limits_{H(\mathbf{q},\mathbf{p})<E}d^{3N}q\,d^{3N}p$$
This is the volume of a sphere of radius $E$. Of course, a spherical shell is just the difference between two spheres of different radii, and so the two functions are related by
$$\Gamma(E)=\Sigma(E+\Delta)-\Sigma(E)$$

Since the thickness $\Delta$ of the shell is small compared to the radius ($\Delta\ll E$), the volume of the shell can be well approximated as
$$\Gamma(E)=\Delta \cdot\omega(E)=\Delta\cdot\frac{ \partial \Sigma(E) }{ \partial E }$$

Since $\Gamma$ is a number of states, we can reasonably assume the entropy comes from [[Entropy (information theory)#Boltzmann's entropy|Boltzmann's definition of entropy]]:
$$S(E,V)=k\log \Gamma(E,V)$$
where $k$ is some constant (presumably the [[Boltzmann constant]]). However, in order to definitively prove this is entropy we need to prove that
1. $S$ is [[Extensive property|extensive]];
2. $S$ obeys the [[Laws of thermodynamics|second law of thermodynamics]].

Let's start from the first. Consider some chamber divided in two volumes $V_{1}$ and $V_{2}$, respectively containing $N_{1}$ and $N_{2}$ particles.

![[Schema Microcanonical entropy proof|center]]

If entropy is extensive, then the total entropy of the system must be the sum of the entropies of the subsystems. The entropy measures disorder, so if the two systems heavily interact with each other, that'll increase entropy by a lot. For this proof, let's assume that the energy of interaction $E_\text{int}$ between the two systems is much smaller than the energy of each system, $E_\text{int}<E_{1}$ and $E_\text{int}<E_{2}$. This removes the interaction-entropy term and leaves us with just the internal entropies. For the interaction to be negligible we need two things:
1. the range of interaction between particles must be finite (we'll send the volume to infinity later so any finite value is fine). This excludes long-range interactions like [[Interazione gravitazionale|gravity]] from this proof;
2. the contact-surface-to-volume ratio must be negligible as the volume goes infinite. This excludes weird contact surface from this proof.

If these are true, then the Hamiltonian is extensive: $H(\mathbf{q},\mathbf{p})=H_{1}(\mathbf{q}_{1},\mathbf{p}_{1})+H(\mathbf{q}_{2},\mathbf{p}_{2})$. To continue, let's define the entropies separately as $S_{1}=k\log \Gamma_{1}(E_{1})$ and $S_{2}=k\log \Gamma_{2}(E_{2})$. $\Gamma_{1}$ and $\Gamma_{2}$ are volumes in the phase spaces $(\mathbf{q}_{1},\mathbf{p}_{1})$ and $(\mathbf{q}_{2},\mathbf{p}_{2})$. Now back to the collective system, the total energy must be between $E$ and $E+2\Delta$, but it must also be equal to the sum of the subsystems, so
$$E<E_{1}+E_{2}<E+2\Delta$$
Meanwhile, the product $\Gamma_{1}(E_{1})\Gamma_{2}(E_{2})$ is the number of total states whose energy is between $E_{1}+E_{2}$ and $E_{1}+E_{2}+2\Delta$ (it's a product and not a sum because we want all possible combinations of states of 1 and 2). To join these two clearly related quantities we divide $E_{1}$ and $E_{2}$ into infinitesimal intervals of width $\Delta$, starting from zero. This division requires there to be an energy minimum. Then, we can sum the number of states from each interval like so:
$$\Gamma(E)=\sum_{i=1}^{E/\Delta} \Gamma_{1}(E_{i})\Gamma_{2}(E-E_{i})$$
If we plug this back in the Boltzmann entropy we get
$$\boxed{S=k\log \sum_{i=1}^{E/\Delta} \Gamma_{1}(E_{i})\Gamma_{2}(E-E_{i})}$$

Now, let $\Gamma_{1}(\bar{E}_{1})\Gamma_{2}(\bar{E}_{2})$ with $\bar{E}_{1}+\bar{E}_{2}=E$ be the largest contribution in the sum for $S$. We want to see what happens at different $N$. We have
$$\Gamma_{1}(\bar{E}_{1})\Gamma_{2}(\bar{E}_{2})\leq \Gamma(E)\leq \frac{E}{\Delta}\Gamma_{1}(\bar{E}_{1})\Gamma_{2}(\bar{E}_{2})$$
The first inequality is true because $\Gamma_{1}(\bar{E}_{1})\Gamma_{2}(\bar{E}_{2})$ is just a term in the sum for $\Gamma(E)$. The second is true because $E/\Delta$ is arbitrarily large (since $\Delta$ is small). If we transition to entropies we get
$$k\log [\Gamma_{1}(\bar{E}_{1})\Gamma_{2}(\bar{E}_{2})]\leq S(E,V)\leq k\log[\Gamma_{1}(\bar{E}_{1})\Gamma_{2}(\bar{E}_{2})]+k\log \frac{E}{\Delta}$$
Since the number of states is proportional to the number of particles, we have $\log\Gamma_{1}\propto N_{1}$, $\log\Gamma_{2}\propto N_{2}$. Also $E\propto N_{1}+N_{2}=N$, which means $\log E/\Delta \sim \log N$. But see how the only difference in between the sides of the inequality is given by $k\log E/\Delta$, so if we were to remove this corrective term, then the entropy $S(E,V)$ would exactly be $k\log[\Gamma_{1}(\bar{E}_{1})\Gamma_{2}(\bar{E}_{2})]$. But this is the entropy of the largest contribution alone, which means that outside of the $\sim \log N$ correction, the only term that matters is the largest one. So in the case of $\log N=0$ we are left with
$$S(E,V)=k\log[\Gamma_{1}(\bar{E}_{1})\Gamma_{2}(\bar{E}_{2})]=k\log \Gamma_{1}(\bar{E}_{1})+k\log \Gamma_{2}(\bar{E}_{2})=S_{1}+S_{2}$$
and so we proved that $S$ is additive over subsystems, i.e. it is extensive.

In other words, there is a single state with energies $(\bar{E}_{1},\bar{E}_{2})$ with an entropy so large it overwhelms all other terms. So the values $\bar{E}_{1}$ and $\bar{E}_{2}$ are such that they maximize $\Gamma_{1}(E_{1})\Gamma_{2}(E_{2})$ under the constraint $E_{1}+E_{2}=E$. Being a maximum, $(\bar{E}_{1},\bar{E}_{2})$ is a [[Punto critico|stationary point]], for which
$$\delta(\Gamma_{1}(E_{1})\Gamma_{2}(E_{2}))=0,\qquad \delta E_{1}+\delta E_{2}=0$$
From this we have
$$\left.\frac{ \partial  }{ \partial E_{1} } \log \Gamma_{1}(E_{1})\right|_{\bar{E}_{1}}-\left.\frac{ \partial  }{ \partial E_{2} } \log \Gamma_{2}(E_{2})\right|_{\bar{E}_{2}}=0$$
and so
$$\left.\frac{ \partial S_{1}(E_{1}) }{ \partial E_{1} }\right|_{E_{1}=\bar{E}_{1}}=\left.\frac{ \partial S_{2}(E_{2}) }{ \partial E_{2} }\right|_{E_{2}=\bar{E}_{2}}$$
If we introduce the [[temperature]] through the [[Maxwell relations]] like
$$T=\left( \frac{ \partial U }{ \partial S }  \right)_{V}$$
we can define the inverse buy inverting the above relation (and calling $U\to E$)
$$\frac{1}{T}=\frac{ \partial S(E,V) }{ \partial E } $$
and substituting it above we get
$$T_{1}=T_{2}$$
which is exactly what we should expect as we are studying the system in the context of [[thermal equilibrium]]. But the definition of temperature we used comes from [[absolute temperature]], which inherently relies on the Boltzmann constant. Therefore, $k$ has to be precisely the Boltzmann constant $k_{B}$, else the definition of $T$ would no longer hold.

As a side note, $T_{1}=T_{2}$ holds for any two subsystems, which means that the global temperature of a [[Physical system|isolated system]] described by the microcanonical ensemble also regulates the temperature (and therefore thermal equilibrium) of all of its components.

It can be proven that the entropy can be calculated from any of $\Gamma$, $\omega$ and $\Sigma$, and that they are all equal up to an additive constant:
$$\boxed{S=k_{B}\log \Gamma(E)\qquad S=k_{B}\log \omega(E)\qquad S=k_{B}\log \Sigma(E)}$$

The only thing left to prove is that $S$ obeys the second law of thermodynamics. Thankfully this is straight-forward: the second law says that when a thermodynamic systems goes from one state to another through a [[Thermodynamic transformation|transformation]], the entropy does not decrease. In a microcanonical ensemble, entropy is a function of $E$, $N$ and $V$. But $E$ and $N$ are constant, so the only thing we can change to vary the state is $V$. But if $V$ is increased, then $\Sigma(E)$ must also increase as we are integrating over more states (recall that the integration bounds are affected by $V$). But since $S=k_{B}\log \Sigma(E)$, and $\Sigma(E)$ can only increase, then $S$ can also only increase. Thus, the second law is preserved, and with that we proved that $S$ is formally entropy.
#### Connection to information theory
Consider the definition of entropy in function of [[Entropy (information theory)|information-theoretical entropy]], $S=k_{B}S_\text{inf}$. Note that this has the same form as the above three, just with $S_\text{inf}$ instead of the $\log$ of $\Gamma$, $\omega$ or $\Sigma$. This suggests that all three of these are formally types of information-theoretical entropy, which then gets converted into physical entropy by the Boltzmann constant.
### Examples
> [!example] Two state system
> Consider a system of $N$ particles. $n_{0}$ are at energy $0$ and $n_{1}$ are at energy $E>0$. Find the entropy and temperature of the system.
> 
> The total energy of the system must be $U=n_{1}E$ (all $n_{0}$ particles have no energy). We can write $n_{0}$ as
> $$n_{0}=N-n_{1}=N- \frac{U}{E}$$
> With some combinatorics, the number of state combinations due to $n_{1}$ is
> $$W=\begin{pmatrix}N \\ n_{1}\end{pmatrix}=\frac{N!}{n_{1}!(N-n_{1})!}$$
> using the [[Binomial theorem|binomial coefficient]]. The entropy therefore is
> $$S=k_{B}\log \left( \frac{N!}{n_{1}!(N-n_{1})!} \right)$$
> Dividing entropy by the Boltzmann constant we get
> $$\frac{S}{k_{B}}=\log N!-\log n_{1}!-\log[(N-n_{1})!]\simeq N\log N- \frac{U}{E}\log \frac{U}{E}- \left( N- \frac{U}{E} \right)\log\left( N- \frac{U}{E} \right)$$
> using [[Stirling's approximation]] and $n_{1}=U/E$.
> 
> As for the temperature, we have from the [[Maxwell relations]]:
> $$T=\frac{ \partial U }{ \partial S } \quad\to \quad \frac{1}{T}=\frac{ \partial S }{ \partial U } $$
> We use the inverse just because it's easier, as we already have $S$ anyway. So
> $$\frac{1}{T}=\frac{k_{B}}{E} \log\left( \frac{NE-U}{U} \right)$$
> So
> $$T=\frac{E}{k_{B}\log\left( \frac{NE-U}{U} \right)}$$
> Note that this temperature could very well be negative. This, of course, is non-physical, but it's happening here regardless. The reason why it happens is that the system is being bounded in energy from above, that is, there is a maximum energy that the system cannot cross. The unphysical nature of negative temperature implies that systems with an energy maximum cannot exist, or at most exist as approximation of unbounded systems. This is the case for [[Sistema a due livelli|two-level systems]], which in practice do exist, but only within a short period of time. For instance, a [[qubit]] is a two-level system during the short period of its measurement, but if we were to observe one over long periods of time, it would not remain so as that would imply the possibility of negative temperature.
> 
> We can also invert the last equation to find the internal energy of the system:
> $$U=\frac{NE}{e^{\beta E}+1}$$
> or alternatively, using $n_{1}=U/E$, the fraction of particles in the $n_{1}$ state:
> $$\frac{n_{1}}{N}=\frac{1}{e^{\beta E}+1}$$
> This is the [[Fermi-Dirac distribution]] for a system with no [[chemical potential]]. It is interesting to see how we managed to find a strictly quantum property from a purely classical treatment. The reason is that a two state system is inherently a quantum idea as it requires the discretization of energy.
> 
> We can also derive the [[heat capacity]] from its definition:
> $$C(T)=\frac{\partial U}{\partial T}=\frac{NE^{2}}{k_{B}T^{2}} \frac{e^{\beta E}}{e^{\beta E}+1}$$
