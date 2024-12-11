Un **fermione** è una [[Particella]] fondamentale con [[spin]] pari a mezzo intero ($\frac{1}{2}$, $\frac{3}{2}$, ...) descritta da una [[Funzione d'onda]] [[Stato total-antisimmetrico|total-antisimmetrica]]. Gli [[Elettrone|elettroni]] sono fermioni e hanno spin $\frac{1}{2}$.
### Fermi surface
The common property of all fermions is the existence of the **Fermi surface**, which is the surface that divides occupied [[stato|states]] from unoccupied states at zero [[temperature]].
#### 1D
To study it, we start with a one dimensional [[Physical system|system]] composed of a length $L$ of space. There are several methods for solving the system.
##### Open boundary conditions
Using open boundary conditions (that is, $\psi(x=0)=\psi(x=L)=0$) and starting from the [[Equazione di Schrödinger|time-independent Schrödinger equation]], we have
$$H\psi_{n}=E\psi_{n}$$
The boundary conditions make our system into a [[Buca infinita quantistica|infinite square well]], so the solution is $\psi_{n}\propto \sin kx$. We also have $kL=n\pi$, which means
$$\psi_{n}(x)\propto \sin \frac{n\pi x}{L},\qquad E_{n}=\frac{\hbar^{2}k^{2}}{2m}=\frac{h^{2}}{2m} \left( \frac{n\pi}{L} \right)^{2}=- \frac{h^{2}}{2m} \left( \frac{n}{2L} \right)^{2}$$
$$H=- \frac{h^{2}}{2m}\frac{ \partial ^{2} }{ \partial x^{2} } $$
By the [[principio di esclusione di Pauli|Pauli exclusion principle]], fermions will be coupled in spin pairs. If we have $N$ fermions in the space, $N/2$ will be spin up and $N/2$ will be spin down. The highest occupied state is therefore $N/2$. Thus our **Fermi energy** (the energy of the last occupied state) is
$$E_{F}=\frac{h^{2}}{2m}\left( \frac{N}{4L} \right)^{2}$$
##### Periodic boundary conditions
If we use periodic boundary conditions, we have $\psi(x=0)=\psi(x=L)$, or $e^{ikx}=e^{ik(x+L)}$ and $e^{ikL}=1$. Our periodic condition is $2\pi n=kL$, where $n=0,\pm 1, \pm 2,\ldots$, so
$$k=\frac{2\pi}{L}n\quad\to \quad E_{k}=\frac{\hbar^{2}k^{2}}{2m}$$
The Fermi energy is
$$E_{F}=\frac{\hbar^{2}}{2m}K^{2}_\text{last occupied}=\frac{\hbar^{2}}{2m} \left( \frac{2\pi}{L} \frac{N}{2\cdot2} \right)^{2}=\frac{h^{2}}{2m}\left( \frac{N}{4L} \right)^{2}$$
The twos at the denominator are due to spin [[Degenerazione|degeneracy]].
##### Density of states
We can also use a density of state (DOS) function. Consider the [[phase space]]. We'll define the state counting function as
$$G(E)=\frac{\frac{4\pi}{3}p^{3}(E)}{\left( \frac{2\pi \hbar}{L} \right)^{2}}=\frac{\frac{4\pi}{3}\sqrt{ 2mE }}{\left( \frac{2\pi \hbar}{L} \right)^{2}}$$
This counts the number of states up to the Fermi energy. Due to Pauli exclusion, this is the same as counting the number of particles, as no more than one fermion can occupy the same state. If we consider only one spin, we get
$$G(E)=\frac{2p}{\left( \frac{2\pi \hbar}{L} \right)}=\frac{2L\sqrt{ 2mE }}{h}$$
At Fermi energy, this is
$$G(E_{F})=\frac{N}{l}$$
where $l$ is the degeneracy of spin states. From this we can derive
$$E_{F}=\frac{h^{2}}{2m}\left( \frac{N}{4L} \right)^{2}$$
The DOS for both spins is
$$g(E)=2\frac{ \partial G }{ \partial E } =\frac{4L}{h}\sqrt{ \frac{m}{2E} }$$
Since one state is one particle, we can find the particle number exclusively from the DOS, if we have access to it:
$$N=\int_{0}^{E_{F}}g(E)\ dE=\int_{0}^{E_{F}} \frac{4L}{h}\sqrt{ \frac{m}{2} }\frac{1}{\sqrt{ E }}\ dE=\frac{8L}{h}\sqrt{ \frac{m}{2} }\sqrt{ E_{F} }$$
By reversing the formula we get
$$E_{F}=\frac{h^{2}}{2m}\left( \frac{N}{4L} \right)^{2}$$
This way, we can also find the ground state per-particle energy:
$$E_{0}=2\sum_{n=1}^{N/2} \frac{h^{2}n^{2}}{2m(2L)^{2}}=2 \frac{h^{2}}{2m(2L)^{2}}\sum_{i=1}^{N/2} n^{2}$$
$$E_{0}\simeq???=\frac{N}{3}E_{F}$$
The $N/3$ factor depends on the dimension. The same result can also be derived from the DOS function directly:
$$E_{0}=\int_{0}^{E_{F}}Eg(E)dE=???=\frac{N}{3}E_{F}$$
#### 3D
The fermi surface can be derive in higher dimensions with more general methods.
(TODO: Check how much of this actually refers to 3D and not other dimensions. 11/12 at about 1:10-1:20 in)
##### Open boundary conditions
Using open boundary conditions in 3D is more challenging, but still doable. The [[Hamiltonian]] is
$$\hat{H}=- \frac{\hbar^{2}}{2m}\nabla ^{2}$$
Our position [[Equazione agli autovalori|eigenfunctions]] are
$$\psi_{n}\propto \sin \frac{\pi n_{x}}{L}\sin \frac{\pi n_{y}}{L}\sin \frac{\pi n_{z}}{L}$$
where $n_{x,y,z}=1,2,3,\ldots$. Our energy eigenvalues are
$$E_{n_{x},n_{y},n_{z}}=\frac{\hbar^{2}}{2m} \frac{\pi^{2}}{L^{2}}(n_{x}^{2}+n_{y}^{2}+n_{z}^{2})$$
##### Periodic boundary conditions
Using periodic boundary conditions and using the [[Funzione d'onda|wavefunction]] $\psi_{\mathbf{k}}(\mathbf{r})=\frac{1}{\sqrt{ V }}e^{i\mathbf{k}\cdot \mathbf{r}}$ on a direction $\mathbf{k}=\frac{2\pi}{L}\hat{\mathbf{n}}$, our equation is
$$\hat{H}\psi_{\mathbf{k}}=E_{\mathbf{k}}\psi_{\mathbf{k}}$$
Its solution is
$$E_{\mathbf{k}}=\frac{\hbar^{2}}{2m}(k_{x}^{2}+k_{y}^{2}+k_{z}^{2})$$
???
##### Density of states
If we start with the state counting function for each spin state
$$G(E)=\frac{\frac{4\pi}{3}p^{3}(E)}{\left( \frac{2\pi \hbar}{L} \right)^{3}}=\frac{\sqrt{ 2 }V(mE)^{3/2}}{3\pi^{2}\hbar^{3}}$$
At the Fermi energy, it becomes
$$G(E=E_{F})=\frac{N}{2}=2 \frac{4\pi V 2\sqrt{ 2 }m^{3/2}E_{F}^{3/2}}{3\cdot 8\pi^{3}\hbar ^{3}}$$
The Fermi energy itself is
$$E_{F}=\frac{\hbar^{2}k_{F}^{2}}{2m}$$
where we defined the **Fermi wavevector**
$$k_{F}\equiv3\pi ^{2} \frac{N}{V}$$
Since it is a wavevector, we can also find the **Fermi velocity** $v_{F}=\hbar k_{F}/m$ and the **Fermi momentum** $p_{F}=\hbar k_{F}$. The DOS function for both spins can be found to be
$$g(E)=\frac{2Vm^{3/2}\sqrt{ E }}{\sqrt{ 2 }\pi^{2}\hbar ^{3}}$$
We can find the number of particles from the DOS:
$$N=G_\text{both spins}(E)=\int_{0}^{E_{F}}g(E)\ dE=\frac{2\sqrt{ 2 }Vm^{3/2}E_{F}^{3/2}}{3\pi ^{2}\hbar^{3}}$$
