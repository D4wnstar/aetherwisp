The **equipartition theorem** is a result in statistical mechanics that equates the [[temperature]] of a [[Physical system|system]] to the average [[energy]] of its components. The name comes from the fact that at [[thermal equilibrium]], total system energy is equally divided among all its components, such as translational, rotational, elastic, etc..

In the most general form, it states the following:

> [!info] Equipartition theorem
> For a physical system with [[Hamiltonian]] $H$ and $N$ [[degree of freedom|degrees of freedom]] $x_{i}$, the following equality holds for all $i,j=1,\ldots,N$:
> $$\left\langle  x_{i}\frac{ \partial H }{ \partial x_{j} }   \right\rangle=\delta_{ij}k_{B}T $$
> where $\delta$ is the [[Delta di Kronecker|Kronecker delta]], $k_{B}$ is the [[Boltzmann constant]] and $T$ is the temperature. The brackets represent an [[ensemble average]]. The degrees of freedom are coordinates in [[phase space]].

For $i=j$ and $x_{i}=p_{i}$ or $x_{i}=q_{i}$ we get
$$\left\langle  p_{i}\frac{ \partial H }{ \partial p_{i} }   \right\rangle =k_{B}T\quad,\quad \left\langle  q_{i}\frac{ \partial H }{ \partial q_{i} }   \right\rangle =k_{B}T$$
Notably this means that, universally, $\langle p^{2} \rangle \propto k_{B}T$.
### Proof
Proof can be found by way of integration over the phase space. It can be found using the formalism of both the [[microcanonical ensemble]] and the [[canonical ensemble]]. The following proof uses the microcanonical phase space with the $\Gamma(E)$ state counting function:
$$\left\langle  x_{i}\frac{ \partial H }{ \partial x_{j} }   \right\rangle=\frac{1}{\Gamma(E)}\int\limits_{E<H<E+\Delta} x_{j}\frac{ \partial H }{ \partial x_{j} }\,dp\,dq= \frac{1}{\Gamma(E)}\Delta \frac{ \partial  }{ \partial E } \int\limits_{H<E}x_{j}\frac{ \partial H }{ \partial E }\,dp\,dq=$$
$$\frac{\Delta}{\Gamma(E)}\frac{ \partial  }{ \partial E } \int\limits_{E<H}x_{i}\frac{ \partial  }{ \partial x_{j} } (H-E)=\frac{\Delta}{\Gamma(E)}\frac{ \partial  }{ \partial E } \left\{ \int\limits_{H<E} \frac{ \partial  }{ \partial x_{j} } [x_{i}(H-E)]\,dp\,dq-\delta _{ij}\int H-E\,dp\,dq \right\}$$
The first integral in the curly brackets cancels out because it is the integral of a derivative (?). and defining $\Gamma(E)=\omega(E)\cdot\Delta$ and $\omega(E)=\frac{ \partial \Sigma(E) }{ \partial E }$.
$$\left\langle  x_{i}, \frac{ \partial H }{ \partial x_{j} }   \right\rangle = \frac{1}{\omega(E)}\delta_{ij}\frac{ \partial  }{ \partial E } \int\limits_{H<E}(E-H)\,dp\,dq=\frac{\delta_{ij}}{\omega(E)}\int\limits_{H<E}dp\,dq=\frac{\delta_{ij}}{\omega(E)}\Sigma(E)=$$
$$=\frac{\delta_{ij}}{\frac{ \partial \Sigma(E) }{ \partial E } }\Sigma(E)=\delta_{ij} \frac{1}{\frac{ \partial  }{ \partial E } \log \Sigma(E)}$$
Since the [[entropy]] is $S=k_{B}\log \Sigma(E)$ and $\frac{1}{T}=\frac{ \partial S }{ \partial E }$ we get
$$\left\langle  x_{i}\frac{ \partial H }{ \partial x_{j} }   \right\rangle=\delta_{ij}k_{B}T $$



$$\frac{ \partial E }{ \partial x_{j} } =0$$
### Specific forms
#### Harmonic oscillators
For the specific case of a [[Oscillatore armonico|harmonic oscillator]], the equipartition theorem becomes
$$\langle H \rangle =\frac{f}{2}k_{B}T$$
where $f$ is the number of oscillators. Each harmonic term contributes $\frac{k_{B}T}{2}$ to the total.
#### Ideal gas
This can be applied to an [[ideal gas]]. A homogeneous, ideal gas in three dimensions obeys by
$$\langle H \rangle =\frac{3N}{2}k_{B}T$$
and has constant-volume [[heat capacity]]
$$C_{V}=\frac{3}{2}Nk_{B}$$
and [[specific heat]] by [[Atomo|atom]]
$$c_{N}=\frac{C_{V}}{N}=\frac{3}{2}k_{B}$$

If the ideal gas is subject to a harmonic [[Potenziale|potential]], the equations become
$$\langle H \rangle =3Nk_{B}T,\qquad C_{V}=3Nk_{B},\qquad c_{N}=3k_{B}$$
Twice as much as in the no-potential case.
#### Crystalline solids
Crystalline solids are subject to elastic potential between atoms. In this case we get
$$U=3Nk_{B}T,\qquad C_{V}=3Nk_{B}=3R$$
where $R$ is the [[ideal gas constant]]. This is called the [[Dulong-Petit law]], which is true for temperatures large enough that quantum oscillations are not relevant. Note how the ideal gas constant appears here despite talking about solids. This is actually true for any monatomic metal. For a more detailed understanding of this phenomenon, see [[Oscillatore armonico#Oscillator chains]], where we find a more general, quantum version of this law through the use of [[phonon|phonons]].