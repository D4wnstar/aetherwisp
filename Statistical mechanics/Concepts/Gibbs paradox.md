The **Gibbs paradox** is a paradox regarding a non-quantum derivation of [[entropy]] that does not consider the [[Identical particles|indistinguishability]] of [[Particella|particles]]. The paradox revolves around how the entropy as derived from classical [[Ensemble|ensembles]] is [[Intensive property|intensive]], despite entropy by definition needing to be [[Extensive property|extensive]]. It is resolved by taking the indistinguishability of particles into account when counting the number of states.
### Description
Stating that entropy is intensive is, in a way, the same as saying that the entropy of a system is not equal to the sum of its parts, which makes little sense. Gibbs sought to describe this phenomenon by taking two [[Ideal gas|ideal gases]], mixing them and seeing the results.

Consider two ideal gases, with $N_{1}$ and $N_{2}$ [[Particella|particles]] and $V_{1}$ and $V_{2}$ volumes, initially separated from each other. They have the same [[temperature]] $T$. Let's call the total occupied volume $V=V_{1}+V_{2}$. From the [[entropy]] of a classical ideal gas
$$S_{i}=k_{B}N_{i}\left[ \frac{3}{2}\ln\left( \frac{2\pi m_{i}k_{B}T}{h^{2}} \right)+\ln V_{i}+ \frac{3}{2} \right]$$
we can figure out the **entropy of mixing** as the difference between the total final entropy
$$S_{T}=\sum_{i=1}^{2} k_{B}N_{i}\left[ \frac{3}{2}\ln\left( \frac{2\pi m_{i}k_{B}T}{h^{2}} \right)+\ln V+ \frac{3}{2} \right]$$
(note that here we use $V=V_{1}+V_{2}$ as opposed to $V_{i}$) and the sum of individual entropies:
$$\Delta S=S_{T}-\sum_{i=1}^{2} S_{i}>0\tag{1}$$
If the gas density is the same for both gases, this simplifies greatly to
$$\frac{\Delta S}{k_{B}}=N_{1}\ln \frac{V}{V_{1}}+N_{2}\ln \frac{V}{V_{2}}>0\tag{2}$$
So far so... good, actually. This isn't illogical. The issues start to arise when we mix a gas with *itself* (i.e. the gases are the same). In this case, $m_{1}=m_{2}=m$ and the total entropy is
$$S_{T}=k_{B}N\left[ \frac{3}{2}\ln\left( \frac{2\pi mk_{B}T}{h^{2}} \right)+\ln V+ \frac{3}{2} \right]$$
The only difference from the previous formula is that, everything else being equal, the sum just amounts to $N_{1}+N_{2}=N$, hence why $N$ lost the subscript. It is otherwise identical to before. Because of this, the entropy of mixing will be given by $(1)$ and $(2)$. However, *this* is nonsense, and the reason for that is that mixing a gas with itself is perfectly reversible, so long as the original temperature and density are the same: removing the partitioning wall keeping the gases separate effectively does nothing because the gases are already in the same starting condition. Thus, putting the wall back fully reverses the process. And yet the entropy increases, despite nothing happening? Reversible [[Thermodynamic transformation|transformations]] are supposed to have $\Delta S=0$, so this can't be. This is the essence of the paradox.

Let's be more precise: something obviously does happen when you remove the partitioning wall. Atoms of gas 1 move into the volume of gas 2 and viceversa. But we know for a fact that entropy can't increase in this process, so by necessity this exchanging of atoms must do nothing with respect to entropy. In fact, this is the crux of the matter: we cannot distinguish between atoms, and not for lack of trying. It is simply an innate property of quantum particles that we need to accept and play around. This [[Identical particles|indistinguishability]], as it is known, is the true culprit of the paradox. If we accept that we cannot distinguish particles from each other (and also not track their motion, see [[Disuguaglianza di Heisenberg|Uncertainty principle]]), the start state and end state of mixing two gases made of the same particles are *identical*, and so how could entropy change?
### Correction
The paradox is corrected by removing the overcounting of indistinguishable states. This is done by using so called **correct Boltzmann counting**, which simply involves dividing the number of states by $N!$. Using this new way of counting, the entropy of an ideal gas comes out to be
$$\frac{S}{k_{B}N}=\ln\left[ \frac{V}{N}\left( \frac{4\pi m}{3h^{2}} \frac{U}{N} \right)^{3/2} \right]+ \frac{5}{2}$$
This is known as the [[Sackur-Tetrode equation]] and it was proven correct experimentally.

For a derivation of why specifically $N!$, see [[Identical particles#Correct Boltzmann counting]].