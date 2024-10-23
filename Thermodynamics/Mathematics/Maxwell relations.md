The **Maxwell relations** are a set of four equations in thermodynamics regarding a system's energy when subject to a reversible [[thermodynamic transformation]]. They exist for several [[Equation of state|equations of state]]: [[internal energy]] $U$, [[enthalpy]] $H$, [[Helmholtz free energy]] $A$ and [[Gibbs free energy]] $G$. These shouldn't be confused with [[Maxwell's equations]], which are the description of electromagnetism. There are many forms for Maxwell relations, depending on which system energy is chosen.

$$\begin{align}
U(S,V)&:& dU=TdS-PdV \\
H(S,P)&:& dH=TdS-VdP \\
A(V,T)&:& dA=-SdT-PdV \\
G(P,T)&:& dG=-SdT+VdP
\end{align}$$

Here $T$ is [[temperature]], $S$ is [[entropy]], $P$ is [[pressure]] and $V$ is volume.
### Mnemonic
Maxwell relations can be rendered graphically in a square diagram:

![[Diagram Maxwell Relations|50%|center]]

The system energy is at the center of the sides and can be expressed in function of the two variables at its sides. The arrows refer to what the constant quantities are: starting at one of the variables, follow the arrow to find the constant. If you go in the direction of the arrow, it's a positive term, else it's negative. For instance, $U$ is between $S$ and $V$ so it will be $U(S,V)$. An arrow connects $V$ to $P$ and we go against the arrow, so one term will be $-PdV$. The other arrow points from $S$ to $T$ and we go alongside it, so the other term will be $TdS$. In total, we have $U(S,V)=TdS-PdV$.
### Derivations
The difference between exact differentials ($d$) and inexact differentials ($\delta$) here is somewhat important. This assumes reversible transformations and therefore exact differentials.

For all of these, we use $dW=PdV$ and $dS=dQ/T$.
#### Enthalpy
From $H$ we get
$$dH=dU+d(PV)=dQ-\cancel{ dW }+\cancel{ PdV }+VdP=TdS+VdP$$
We get
$$T=\left( \frac{ \partial H }{ \partial S }  \right)_{P}\qquad V=\left( \frac{ \partial H }{ \partial P }  \right)_{S}$$
#### Helmholtz free energy
From $A$ we get
$$dA=dU-d(TS)=\cancel{ dQ }-dW-\cancel{ TdS }-SdT$$
so
$$dA=-PdV-SdT$$
Since $A=A(V,T)$, we get
$$P=-\left( \frac{ \partial A }{ \partial V }  \right)_{T}\qquad S=-\left( \frac{ \partial A }{ \partial T }  \right)_{V}$$
#### Gibbs free energy
From $G$ we get
$$dG=dA+d(PV)=-SdT-\cancel{ PdV }+\cancel{ PdV }+VdP$$
and so
$$dG=VdP-SdT$$
We get
$$S=-\left( \frac{ \partial G }{ \partial T }  \right)_{P}\qquad V=\left( \frac{ \partial G }{ \partial P }  \right)_{T}$$
