The **heat equations** or **$dQ$ equations** (not to be confused with the [[heat equation|heat]] [[partial differential equation]]) are a set of equations for the infinitesimal variation of [[heat]] $dQ$ in a [[physical system]]. They are equations of two thermodynamic variable chosen among [[pressure]] $P$, volume $V$ and [[temperature]] $T$, with the third constrained by the system's [[equation of state]].

The equations are
$$\begin{align}
dQ(P,V)&=\left( \frac{ \partial U }{ \partial P }  \right)_{V}dP+\left[ \left( \frac{ \partial U }{ \partial V }  \right)_{P}+P \right]dV \\
dQ(P,T)&=\left[ \left( \frac{ \partial U }{ \partial F }  \right)_{P}+ P\left( \frac{ \partial V }{ \partial T }  \right)_{P} \right]dT+\left[ \left( \frac{ \partial U }{ \partial P }  \right)_{T}+P\left( \frac{ \partial V }{ \partial P }  \right)_{T} \right]dP \\
dQ(V,T)&=\left[ \left( \frac{ \partial U }{ \partial V }  \right)_{T}+P \right]dV+\left( \frac{ \partial U }{ \partial T }  \right)_{V}dT
\end{align}
$$
where $U$ is the [[internal energy]] of the system and $F$ is [[Helmholtz free energy]]. The subscripts mean taking a derivative while holding that variable constant. These derivatives are coefficients that are measured experimentally. Specifically, we have
$$C_{V}=\left( \frac{ \partial U }{ \partial T }  \right)_{V}\qquad C_{P}=\left( \frac{ \partial H }{ \partial T }  \right)_{P}$$
as the [[heat capacity]] for constant-volume and isobaric [[Thermodynamic transformation|transformations]].
### Derivation
The heat equations are directly derived from the [[Laws of thermodynamics|first law of thermodynamics]]. The internal energy must be
$$dU=dQ-dW=dQ-PdV$$
with $dQ$ [[heat]] and $dW=PdV$ [[work]]. The equation of state allows us to lock one the three variables $P$, $V$ or $T$ down, giving us three ways to express $dU$
$$\begin{align}
dU(P,V)&=\left( \frac{ \partial U }{ \partial P }  \right)_{V}dP+ \left( \frac{ \partial U }{ \partial V }  \right)_{P}dV \\
dU(P,T)&=\left( \frac{ \partial U }{ \partial P }  \right)_{T}dP+\left( \frac{ \partial U }{ \partial T }  \right)_{P}dT \\
dU(V,T)&=\left( \frac{ \partial U }{ \partial V }  \right)_{T}dV+\left( \frac{ \partial U }{ \partial T }  \right)_{V}dT
\end{align}$$
for all permutations of the variables. Combining these with the first law $dQ=dU+PdV$ gives us
$$\begin{align}
dQ(P,V)&=\left( \frac{ \partial U }{ \partial P }  \right)_{V}dP+\left[ \left( \frac{ \partial U }{ \partial V }  \right)_{P}+P \right]dV \\
dQ(P,T)&=\left( \frac{ \partial U }{ \partial P }  \right)_{T}dP+\left( \frac{ \partial U }{ \partial T }  \right)_{P}dT+PdV \\
dQ(V,T)&=\left[ \left( \frac{ \partial U }{ \partial V }  \right)_{T}+P \right]dV+\left( \frac{ \partial U }{ \partial T }  \right)_{V}dT
\end{align}$$
The first and third equations are done, but the second equation can't be used as is, because $dV$ is still leftover from the work. We can get rid of it by expressing $V$ in function of the other two:
$$dV=\left( \frac{ \partial V }{ \partial P }  \right)_{T}dP+\left( \frac{ \partial V }{ \partial T }  \right)_{P}dT$$
and so
$$dQ(P,T)=\left[ \left( \frac{ \partial U }{ \partial P }  \right)_{T}+P\left( \frac{ \partial V }{ \partial P }  \right)_{T} \right]dP+\left( \frac{ \partial (U+PV) }{ \partial T }  \right)_{P}dT$$
For convenience, we can use the [[enthalpy]] $H=U+PV$ to simplify things:
$$dQ(P,T)=\left[ \left( \frac{ \partial U }{ \partial P }  \right)_{T}+P\left( \frac{ \partial V }{ \partial P }  \right)_{T} \right]dP+\left( \frac{ \partial H }{ \partial T }  \right)_{P}dT$$
