The **free expansion of an ideal gas** is particularly simple system to analyze the thermodynamics of.

Consider an [[ideal gas]] that's contained in a sealed, thermodynamically [[Physical system|isolated]] box by insulating walls. In the real world, this can be approximated by thick walls made of a material with very high [[heat capacity]], such as water (see the figure below).

![[Schema Free expansion of ideal gas|center]]


There are two chambers, separated by a movable stopper. Initially, one chamber contains gas at [[temperature]] $T_{1}$ and volume $V_{1}$, whereas the other is vacuum. The stopper is then removed, letting the gas expand from the first chamber to the second, filling all space. After expansion, the gas has a new temperature $T_{2}$ and volume $V_{2}$. Experimentally, it was found that the temperature went unchanged, so that $T_{1}=T_{2}$. Notably, this implies a few things:
1. Since the temperature was unchanged, no [[heat]] was exchanged: $\Delta Q=0$.
2. Since there is no gas to push against during the expansion, no [[work]] was performed either: $\Delta W=0$.
3. But the [[Laws of thermodynamics|first law of thermodynamics]] therefore gives us $\Delta U=\Delta Q-\Delta W=0$. So the [[internal energy]] of the gas also did not change. Thus, we have $U_{1}(V_{1},T)=U_{2}(V_{2},T)$.

The last point implies that $U$ is independent of volume or, in other words, exclusively dependent on temperature: $U=U(T)$. From the [[heat equations]] we know
$$C_{V}=\left( \frac{ \partial U }{ \partial T }  \right)_{V}=\frac{dU}{dT}$$
where the partial derivative becomes a total derivative since the dependency on $V$ has been lifted. From this we can write
$$U=\int dU=\int C_{V}\ dT=C_{V}T+\text{const}=C_{V}T$$
Note that this is an *indefinite* integral, not a definite one. The leftover constant vanishes by setting $U=0$ at $T=0$. (TODO: Finish writing this)