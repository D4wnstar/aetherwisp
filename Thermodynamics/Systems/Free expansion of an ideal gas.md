The **free expansion of an ideal gas** is particularly simple [[physical system]] to analyze the thermodynamics of.
### Mechanics
Consider an [[Ideal gas]] that's contained in a sealed, thermodynamically [[Physical system|isolated]] box by insulating walls. In the real world, this can be approximated by thick walls made of a material with very high [[heat capacity]], such as water (see the figure below).

![[Schema Free expansion of ideal gas|center]]


There are two chambers, separated by a movable stopper. Initially, one chamber contains gas at [[temperature]] $T_{1}$ and volume $V_{1}$, whereas the other is vacuum. The stopper is then removed, letting the gas expand from the first chamber to the second, filling all space. After expansion, the gas has a new temperature $T_{2}$ and volume $V_{2}$. Experimentally, it was found that the temperature went unchanged, so that $T_{1}=T_{2}$. Notably, this implies a few things:
1. Since the temperature was unchanged, no [[heat]] was exchanged: $\Delta Q=0$.
2. Since there is no gas to push against during the expansion, no [[work]] was performed either: $\Delta W=0$.
3. But the [[Laws of thermodynamics|first law of thermodynamics]] therefore gives us $\Delta U=\Delta Q-\Delta W=0$. So the [[internal energy]] of the gas also did not change. Thus, we have $U_{1}(V_{1},T)=U_{2}(V_{2},T)$.

The last point implies that $U$ is independent of volume or, in other words, exclusively dependent on temperature: $U=U(T)$. From the [[heat equations]] we know
$$C_{V}=\left( \frac{ \partial U }{ \partial T }  \right)_{V}=\frac{dU}{dT}$$
where the partial derivative becomes a total derivative since the dependency on $V$ has been lifted. If $C_{V}$ is constant, we can write
$$U=\int dU=\int C_{V}\ dT=C_{V}T+\text{const}$$
Note that this is an *indefinite* integral, not a definite one. The leftover constant vanishes by setting $U=0$ at $T=0$, leaving us with
$$\boxed{U=C_{V}T}$$
Also from the heat equations, we can find the isobaric heat capacity as
$$C_{P}=\left( \frac{ \partial H }{ \partial T }  \right)_{P}=\left( \frac{ \partial (U+PV) }{ \partial T }  \right)_{P}=\frac{dU}{dT}+ \frac{ \partial (Nk_{B}T) }{ \partial T } =C_{V}+Nk_{B}$$
where $N$ is the number of [[particella|particles]] in the gas and $k_{B}$ is the [[Boltzmann constant|Boltzmann constant]]. So the difference between constant-volume and isobaric heat capacities for an ideal gas is
$$C_{P}-C_{V}=Nk_{B}$$
#### Transformations
We can work out the equation governing a [[Thermodynamic transformation|reversible, adiabatic transformation]]. Since for an adiabatic transformation $dQ=0$ and work is $dW=PdV$, the [[Laws of thermodynamics|first law of thermodynamics]] gives us $dU=-PdV$, but since $dU=C_{V}dT$ is also true, we get
$$C_{V}dT+PdV=0$$
We can use the ideal gas law $PV=Nk_{B}T$ to state the infinitesimal form
$$dT=\frac{d(PV)}{Nk_{B}}=\frac{VdP+PdV}{Nk_{B}}$$
so we get
$$\begin{align}
0&=C_{V}dT+PdV \\
&=C_{V} \frac{VdP+PdV}{Nk_{B}} + PdV \\
&=C_{V}(VdP+PdV)+Nk_{B}PdV \\
&=C_{V}VdP+(C_{V}+Nk_{B})PdV \\
&=C_{V}VdP+C_{P}PdV \\
&=\frac{dP}{P}+ \gamma\frac{dV}{V}
\end{align}$$
where $\gamma\equiv C_{P}/C_{V}$. If $\gamma$ is constant, we can integrate the former equation to get
$$0=\int \frac{dP}{P}+ \gamma \int \frac{dV}{V}=\ln P+\gamma \ln V+K$$
for some constant $K$. From this we get
$$\ln P=-\gamma \ln V+K\quad\Rightarrow \quad P=e^{-\gamma \ln V+K}=e^{K}e^{\ln (V^{-\gamma})}=CV^{-\gamma}$$
where $C$ is some other constant. Therefore
$$\boxed{PV^{\gamma}=\text{constant}}$$
Using the [[equation of state]] $PV=Nk_{B}T$, we get the equivalent form
$$\boxed{TV^{\gamma-1}=\text{constant}}$$
Since $PV=\text{constant}$ determines an isotherm (because $PV\propto T$ in the ideal gas law), $PV^{\gamma}=\text{constant}$ has a similar shape to an isotherm, but since $\gamma>1$ as $C_{P}=C_{V}+Nk_{B}>C_{V}$, it has a steeper slope in a $PV$ graph. Thus, for an ideal gas, adiabatic transformations have a steeper $PV$ slope.

![[Graph Transformation of ideal gas|center]]

