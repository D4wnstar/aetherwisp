The **equipartition theorem** is a result in statistical mechanics that equates the [[temperature]] of a [[Physical system|system]] to the average [[energy]] of its components. The name comes from the fact that at [[thermal equilibrium]] and sufficiently high temperatures, total system energy is equally divided among all its components, such as translational, rotational, elastic, etc..

In the most general form, it states the following:

> [!info] Equipartition theorem
> For a physical system with [[Hamiltonian]] $H$ and $N$ [[degree of freedom|degrees of freedom]] $x_{i}$, the following equality holds for all $i,j=1,\ldots,N$:
> $$\left\langle  x_{i}\frac{ \partial H }{ \partial x_{j} }   \right\rangle=\delta_{ij}k_{B}T $$
> where $\delta$ is the [[Delta di Kronecker|Kronecker delta]], $k_{B}$ is the [[Boltzmann constant]] and $T$ is the temperature. The brackets represent an [[ensemble average]]. The degrees of freedom are coordinates in [[phase space]].

For $i=j$ and $x_{i}=p_{i}$ or $x_{i}=q_{i}$ we get
$$\left\langle  p_{i}\frac{ \partial H }{ \partial p_{i} }   \right\rangle =k_{B}T\qquad \left\langle  q_{i}\frac{ \partial H }{ \partial q_{i} }   \right\rangle =k_{B}T$$
Notably this means that, universally, $\langle p^{2} \rangle \propto k_{B}T$.
### Proof
Proof can be found by way of integration over the phase space. It can be found using the formalism of both the [[microcanonical ensemble]] and the [[canonical ensemble]], and both of them revolve around calculating the [[ensemble average]] in different ways.
#### Microcanonical
The following proof uses the microcanonical phase space. Our ensemble average for a quantity $O$ is given by
$$\langle O \rangle =\frac{1}{\Gamma(E)} \int\limits_{E<H<E+\Delta}Od\mathbf{q}d\mathbf{p}$$
$\Gamma(E)$ is the state counting function in a thin spherical shell of radii $E$ and $E+\Delta$, with $\Delta\ll E$. We can therefore state
$$\left\langle  x_{i}\frac{ \partial H }{ \partial x_{j} }   \right\rangle=\frac{1}{\Gamma(E)}\int\limits_{E<H<E+\Delta} x_{i}\frac{ \partial H }{ \partial x_{j} }\,d\mathbf{q}\,d\mathbf{p}=\ldots$$
Since the spherical shell is very thin, $\Gamma(E)$ is well approximated as
$$\Gamma(E)=\Delta \cdot \frac{ \partial \Sigma(E) }{ \partial E } =\Delta\cdot \omega(E)$$
where $\Sigma(E)$ is the function that counts states inside the sphere of radius $E$ and $\omega(E)$ is its derivative. This yields
$$\ldots= \frac{1}{\Gamma(E)}\Delta \frac{ \partial  }{ \partial E } \int\limits_{H<E}x_{i}\frac{ \partial H }{ \partial x_{j} }\,d\mathbf{q}\,d\mathbf{p}=\ldots$$
where we changed our integration bounds from the shell $E<H<E+\Delta$ to the sphere $H<E$. The quantity $\Gamma(E)/\Delta$ is the function $\omega(E)$. Moreover, we can substitute $H$ with $H-E$ in the derivative since $E$ is constant and vanishes either way. Thus
$$\ldots=\frac{1}{\omega(E)}\frac{ \partial  }{ \partial E } \int\limits_{H<E} x_{i}\frac{ \partial (H-E) }{ \partial x_{j} } d\mathbf{q}d\mathbf{p}=\ldots$$
We can now use [[Integrazione per parti|integration by parts]]:
$$\ldots=\frac{1}{\omega(E)}\frac{ \partial  }{ \partial E } \left[ \int\limits_{H<E}\frac{ \partial  }{ \partial x_{j} }(x_{i}(H-E))d\mathbf{q}d\mathbf{p}- \int\limits_{H<E} \delta_{ij}(H-E)d\mathbf{q}d\mathbf{p} \right]=\ldots$$
since $\partial x_{i}/\partial x_{j}=\delta_{ij}$. The first integral vanishes because it can be rewritten as an integral of $H-E$ on the [[hypersurface]] defined by $H=E$. We are now left with
$$\ldots=\frac{\delta_{ij} }{\omega(E)}\frac{ \partial  }{ \partial E } \int\limits_{H<E}(E-H)d\mathbf{q}d\mathbf{p}=\frac{\delta_{ij}}{\omega(E)}\int\limits_{H<E}d\mathbf{q}d\mathbf{p}=\frac{\delta_{ij}}{\omega(E)}\Sigma(E)$$
We have
$$\frac{\Sigma(E)}{\omega(E)}=\left( \frac{1}{\Sigma (E)}\frac{ \partial \Sigma(E) }{ \partial E }  \right)^{-1}=\left( \frac{ \partial \ln \Sigma (E) }{ \partial E }  \right)^{-1}$$
Microcanonical [[entropy]] is given as $S=k_{B}\ln \Sigma(E)$. Its derivative is
$$\frac{1}{T}=\frac{ \partial S }{ \partial E } =k_{B}\frac{ \partial \ln \Sigma(E) }{ \partial E } $$
so
$$\frac{\Sigma(E)}{\omega(E)}=k_{B}T$$
If we substitute this, we get
$$\left\langle  x_{i}\frac{ \partial H }{ \partial x_{j} }   \right\rangle =\delta_{ij}k_{B}T$$
which completes our proof.
### Specific forms
#### Harmonic oscillators
For the specific case of a [[Harmonic oscillator|harmonic oscillator]], the equipartition theorem becomes
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
where $R$ is the [[ideal gas constant]]. This is called the [[Dulong-Petit law]], which is true for temperatures large enough that quantum oscillations are not relevant. Note how the ideal gas constant appears here despite talking about solids. This is actually true for any monatomic metal. For a more detailed understanding of this phenomenon, see [[Harmonic oscillator#Oscillator chains]], where we find a more general, quantum version of this law through the use of [[phonon|phonons]].