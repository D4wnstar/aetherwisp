The **Gibbs paradox** is a paradox regarding a non-quantum derivation of [[entropy]] that does not consider the indistinguishability of [[Particella|particles]]. The paradox notes how this non-quantum entropy is [[Intensive property|intensive]], despite entropy needing to be [[Extensive property|extensive]].
### Description
Consider two [[ideal gas|ideal gases]], with $N_{1}$ and $N_{2}$ [[Particella|particles]] and $V_{1}$ and $V_{2}$ volumes, initially separated from each other. They have the same [[temperature]] $T$ and density. Let's call the total occupied volume $V=V_{1}+V_{2}$. From the [[entropy]] of an ideal gas, we can figure out the **mixing entropy**:
$$\frac{\Delta S}{k_{B}}=N_{1}\ln \frac{V}{V_{1}}+N_{2}\ln \frac{V}{V_{2}}>0$$
and the total entropy:
$$S=Nk_{B}\ln(V\mu^{3/2})+NS_{0}$$
where $k_{B}$ is the [[Boltzmann constant]], $\mu=\frac{U}{N}$ and $U$ is [[internal energy]] and $S_{0}$ is the initial entropy.

The mixing entropy is equal for something i guess so it's wrong?
### Correction
The paradox was corrected by using **Boltzmann's corrected count** $\Sigma(E)/N!$. Using this new way of counting microstates, we get the **Salkur-Tetrode equation**:
$$S=Nk_{B}\ln\left( \frac{V}{N}\mu^{3/2} \right)+ \frac{3}{2}Nk_{B}\left( \frac{5}{3}+\ln \frac{4\pi m}{3h^{2}} \right)$$
where $h$ is the [[Costante di Planck|Planck constant]] and $m$ is ???. This equation was proven correct experimentally.

The reason why the microstate count was corrected by dividing by $N!$ comes from quantum mechanics. A high-level overview goes as follows: consider two 