Statistical mechanics can be extended to quantum mechanics by applying its [[Postulati della meccanica quantistica|principles]] to the preexisting theory. However, due to the complexity of statistical [[Physical system|systems]] and since thermodynamics in general tries to explain phenomena at a high level, some care needs to be take. Statistical systems are inherently *open systems*, that is, they interact with the environment. Open systems are notoriously complicated to deal with and many quantum systems are approximated as closed for the sake of simplicity. However, we can't do that in statistical mechanics, the entire point of which is to find points of equilibrium with the surrounding environment. In theory, what we need is the [[Hamiltonian]] of the system and the Hamiltonian of the environment, from which we can figure out the coupling. However, the environment Hamiltonian is so complicated, we can't do much of anything with it (and that's assuming we can even find it in the first place). We need a way around that.
### Quantum regime
First things first, let's define when we should use quantum mechanics in the first place. We know that the [[kinetic energy]] $K$ of a [[Particella|particle]] in a gas depends on the [[temperature]] of the system. For an [[ideal gas]] we have
$$K=\frac{p_{0}^{2}}{2m}=\frac{3}{2}k_{B}T$$
and more generally $K\propto T$. Using the [[Formula di de Broglie|de Broglie wavelength]] we get
$$\lambda_{0}=\frac{h}{\sqrt{ 3mk_{B}T }}$$
which gives us a measure of the spatial extension of a particle. Due to the [[Disuguaglianza di Heisenberg|uncertainty principle]], the uncertainty on spatial extension $\Delta x$ and momentum spread $\Delta p$ are related by $\Delta x\Delta p\sim \hbar$[^1]. The wavelength $\lambda_{0}$ serves as an order-of-magnitude estimate of the spatial extension. A more convenient metric of spatial extent is the [[Formula di de Broglie|de Broglie thermal wavelength]], defined as
$$\lambda=\sqrt{ \frac{2\pi \hbar^{2}}{mk_{B}T} }$$
which is really just a rescaled form of the previous one (it makes for nicer-looking equations, that's all). Quantum effects begin to occur when the [[Funzione d'onda|wavefunction]] superposition starts to crop up. For two wavefunctions to superimpose, they must more or less occupy the same space, and for that to happen, the particles must close enough that their spatial extend is less than their distance. As such, if take particle density $n$ to be a measure of average interparticle distance (which is proportional to $n^{1/3}$), we can state that quantum effects begin to be relevant when
$$n\lambda ^{3}\simeq 1\quad\text{(onset of quantum effects)}$$
Much more than this, and quantum effects are negligible. Note that $\lambda$ is dependent on temperature. This means that we can rewrite the previous equation to find a specific temperature at which a gas starts to behave like a quantum system. If we use the full equality $n\lambda ^{3}=1$ and extract $T$ out of $\lambda$ we find
$$T_{0}=\left( \frac{2\pi \hbar^{2}}{k_{B}m} \right)n^{2/3}$$
We call $T_{0}$ the [[degeneracy temperature]]. Anything below this value and we must take quantum physics into account. What this value actually is changes extensively across several orders of magnitude depending on which system we are talking about. For instance, atomic hydrogen ($H_{2}$) gas at particle density of $2\times 10^{19}\text{ particles/cm}^{3}$ has a degeneracy temperature of $T_{0}=5\times 10^{-2}\text{ K}$. However, if we express free [[Elettrone|electrons]] in metal as a particle gas of density $10^{22}\text{ particles/cm}^{3}$ we get a temperature of $T_{0}=10^{4}\text{ K}$. A difference of six orders of magnitude.


One of the basic [[Postulati della meccanica quantistica|principles of quantum mechanics]] is that a [[stato|state]] $\psi$ can be expressed as a [[Serie di Fourier|Fourier series]] of [[Equazione agli autovalori|eigenfunctions]] $\phi_{n}$ as
$$\psi=\sum_{n}c_{n}\phi_{n} $$
where $c_{n}$ are coefficients. Each component of the system has its own state described by its own eigenfunction. The [[Stato|macrostate]] of the system as a whole is a [[Stato|mixed state]] of all of these [[Stato|microstates]]. In time, $c_{n}(t)$ can be considered [[Funzione d'onda|wavefunctions]] just like $\phi_{n}$. The [[mean]] of a quantity $O$ in a state $\psi$ is
$$\langle O \rangle =\frac{\braket{ \psi | O |\psi }}{\braket{ \psi | \psi } }$$
If we expand $\psi$ in series we get
$$\langle O \rangle =\frac{\sum_{n,m}\braket{ c_{n} | c_{m} } \braket{ \phi_{n} | O |\phi_{m} }}{\sum_{n}\braket{ c_{n} | c_{n} }}  $$
But we want to describe the equilibrium state of the system, so we want to remove time dependence. To do that, we use the time average of the coefficients
$$\langle O \rangle =\frac{\sum_{n,m}\overline{\braket{ c_{n} | c_{m} }} \braket{ \phi_{n} | O |\phi_{m} }}{\sum_{n}\braket{ c_{n} | c_{n} }}  $$
where the overline is the time average, not the complex conjugate.

In order to fix the complexity, we need to make a hypothesis, or assumption about how the system works. For this, let's say that the time it takes for the microscopic processes to complete is far smaller than macroscopic time. In this assumption, microscopic oscillations vanish when looking at a time average as they change so frequently and the [[energy]] $E$ of the macroscopic system is *mostly* constant, specifically it lies in some interval $[E,E+\Delta]$, where $\Delta\ll E$ quantifies the small oscillations. The valid energy levels are determined by the [[Equazione di Schrödinger|Schrödinger equation]] as
$$H\ket{\phi_{n}}=E_{n}\ket{\phi_{n}}  $$
where $\ket{\phi_{n}}$ are the eigenstates of the system. Like in classical statistical mechanics, we apply the [[equal a priori probability hypothesis]], where we state that all [[macrostate|macrostates]] are equally likely. However, in quantum statistical mechanics, we apply a second statement, which is the [[random phase hypothesis]], which states that the phases of individual states are random and therefore on average they cancel out when taking time averages. In other words, only diagonal components matter. This means
$$\overline{\braket{ c_{n} | c_{m} } }=0\quad\text{for}\quad n\neq m$$
This makes the set of all coefficients [[Ortogonalità|orthogonal]] (but not necessarily [[Normalizzazione|normalized]]!). However, we can also enforce normalization within the energy eigenstates of our systems (i.e. within $[E,E+\Delta]$), so that
$$\overline{\braket{ c_{n} | c_{m} } }=\begin{cases}
1&E<E_{n}<E+\Delta \\
0&\text{elsewhere}
\end{cases}$$
If we call $\overline{\braket{ c_{n} | c_{m} } }=\lvert b_{n} \rvert^{2}$ we get
$$\boxed{\langle O \rangle =\frac{\sum_{n,m}\lvert b_{n} \rvert ^{2} \braket{ \phi_{n} | O |\phi_{m} }}{\sum_{n}\lvert b_{n} \rvert ^{2}}  }$$
The eigenstates of a system can be packaged in a [[Matrice di densità|density matrix]] $\rho$, through which we can write
$$\langle O \rangle =\frac{\sum_{n}\braket{ \phi_{n} | O\rho | \phi_{n} } }{\sum_{n}\braket{ \phi_{n} | \rho | \phi_{n} } }=\frac{\sum_{n,m}\braket{ \phi_{n} | O | \phi_{m} }\braket{ \phi_{m} | \rho | \phi_{n} }  }{\sum_{n}\braket{ \phi_{n} | \rho | \phi_{n} } }=\frac{\text{Tr}(O\rho)}{\text{Tr}(\rho)}$$
The density matrix in the $b_{n}$ [[base|basis]] is
$$\boxed{\rho=\sum_{n}\ket{\phi_{n}}\lvert b_{n} \rvert ^{2}\bra{\phi_{n}}  }$$

[^1]: Of course, the product of the uncertainties can go up to infinity, but we care systems with realistically low uncertainty (although not necessarily lowest-uncertainty states).