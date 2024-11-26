Statistical mechanics can be extended to quantum mechanics by applying its [[Postulati della meccanica quantistica|principles]] to the preexisting theory. However, due to the complexity of statistical [[Physical system|systems]] and since thermodynamics in general tries to explain phenomena at a high level, some care needs to be take. Statistical systems are inherently *open systems*, that is, they interact with the environment. Open systems are notoriously complicated to deal with and many quantum systems are approximated as closed for the sake of simplicity. However, we can't do that in statistical mechanics, the entire point of which is to find points of equilibrium with the surrounding environment. In theory, what we need is the [[Hamiltonian]] of the system and the Hamiltonian of the environment, from which we can figure out the coupling. However, the environment Hamiltonian is so complicated, we can't do much of anything with it (and that's assuming we can even find it in the first place). We need a way around that.

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
