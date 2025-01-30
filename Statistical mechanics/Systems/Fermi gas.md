A **Fermi gas** is a model for a [[Physical system|system]] of many non-interacting [[Fermion|fermions]], the simplest example of which is a fermionic [[ideal gas]]. The key property is that fermions are subject to the [[Pauli exclusion principle]] and can't simultaneously occupy the same [[stato|state]], which leads to a "pseudo-[[Potenziale|potential]]" that pushes fermions away from each other.
### Zero temperature and Fermi energy
In the low-temperature limit $T\to 0$ and due to the exclusion principle, the [[Fermi-Dirac distribution]] approximately becomes
$$\langle n_{p} \rangle =\frac{1}{e^{\beta(\varepsilon_{p}-\mu)}+1}\to \begin{cases}
0 & \text{ if }\varepsilon_{p}>\mu \\
1 & \text{ if }\varepsilon_{p}<\mu
\end{cases}$$
What this means is that all states with energy lower than $\mu$ will be occupied, and all states with higher energy will be vacant. We can use the [[theta di Heaviside|Heaviside step function]] $\Theta$ to represent this symbolically:
$$\lim_{ T \to 0 } \langle n_{p} \rangle=\Theta(\mu-\varepsilon_{p})$$
The specific energy threshold is known as the [[Fermi energy]] $E_{F}$. This energy leads to a momentum called the Fermi momentum $p_{F}=\sqrt{ 2mE_{F} }$. In [[phase space]], this momentum occupies a spherical region, which contains all the occupied states discussed before. The [[Superficie|surface]] of this sphere is known as the [[Fermi surface]]. This odd state is known as [[quantum degeneracy]] (not to be confused with state [[Degenerazione|degeneracy]], although the two are closely related). Despite being under no potential, fermions in this state are subject to an effective [[pressure]], known as [[degenerate pressure]], which prevents them for compacting further. This pressure is a considerable factor for fermionic systems in extreme environments, such as [[Nana bianca|white dwarfs]], which rely on [[Elettrone|electron]] degeneracy pressure, and [[Stella di neutroni|neutron stars]], which rely on [[neutrone|neutron]] degeneracy pressure.

Fermi energy can be calculated purely from knowledge of the exclusion principle, that fermions are non-interacting and by choosing some appropriate boundary conditions.
#### 1D
Consider a one dimensional [[Physical system|system]] composed in a length $L$ of space.
##### Open boundary conditions
Starting from the [[Equazione di Schrödinger|time-independent Schrödinger equation]], we have
$$H\psi_{n}=E\psi_{n}$$
The solution depends on the boundary. If we set open boundary conditions (that is, the edges of the system are impassable, so $\psi(x=0)=\psi(x=L)=0$), our system turns into a [[Buca infinita quantistica|infinite square well]], so the solution is $\psi_{n}\propto \sin kx$. We also have $kL=n\pi$, which means
$$\psi_{n}(x)\propto \sin \frac{n\pi x}{L},\qquad E_{n}=\frac{\hbar^{2}k^{2}_{n}}{2m}=\frac{\hbar^{2}n^{2}\pi ^{2}}{2mL^{2}}=\frac{h^{2}}{2m} \left( \frac{n}{2L} \right)^{2}$$
The [[Hamiltonian]] is the usual [[Particella libera (quantistica)|free particle]] one:
$$\hat{H}=- \frac{\hbar^{2}}{2m}\frac{ \partial ^{2} }{ \partial x^{2} } $$
If our $N$ fermions have two possible [[spin]] eigenvalues, $N/2$ will be spin up and $N/2$ will be spin down due to the exclusion principle. (For the rest of the article, we'll only consider fermions with two possible spins, which are by far the most common, but it is possible to generalize to $\ell$ spins by multiplying all formulas directly dependent on spin count by $\ell$.) Since each state has precisely one fermion in it, the highest occupied state must be $N/2$. Thus the Fermi energy is found at $n=N/2$:
$$\boxed{E_{F}=\frac{h^{2}}{2m}\left( \frac{N}{4L} \right)^{2}}$$
##### Periodic boundary conditions
With periodic boundary conditions, our system becomes a looping ring defined by $\psi(x=0)=\psi(x=L)$. Since fermions are free, their [[Equazione agli autovalori|eigenfunctions]] are [[plane wave|plane waves]] $\propto e^{ikx}$, so this is like saying $e^{ikx}=e^{ik(x+L)}$ and therefore $e^{ikL}=1$. This is true when $2\pi n=kL$, where $n=0,\pm 1, \pm 2,\ldots$. Since the energy is given by the wave vector, we get
$$k=\frac{2\pi}{L}n\quad\to \quad E_{k}=\frac{\hbar^{2}k^{2}}{2m}$$
The Fermi energy is
$$E_{F}=\frac{\hbar^{2}}{2m}k^{2}_\text{last occupied}=\frac{\hbar^{2}}{2m} \left( \frac{2\pi}{L} \frac{N}{2\cdot 2} \right)^{2}=\boxed{\frac{h^{2}}{2m}\left( \frac{N}{4L} \right)^{2}}$$
since $n_\text{last occupied}=N/4$, unlike in the open boundary case. This is because, beyond spin [[Degenerazione|degeneracy]], here we have to consider both signs of $n$, whereas in the square well we drop the negative $n$'s. This is balanced out by the additional $2$ in the periodic condition (before it was $\pi n=kL$, now it is $2\pi n=kL$).
##### Density of states
We can also use a density of state (DOS) function through the [[Thomas-Fermi approximation]]. The state counting function for momentum is
$$G(E)=\frac{\frac{4\pi}{3}p^{3}}{\left( \frac{2\pi \hbar}{L} \right)^{3}}=\frac{\frac{4\pi}{3}(2mE)^{3/2}}{\left( \frac{2\pi \hbar}{L} \right)^{3}}$$
This counts the number of states up to an energy $E$. In one dimension, this becomes
$$G(E)=\frac{2p}{\left( \frac{2\pi \hbar}{L} \right)}=\frac{2L\sqrt{ 2mE }}{h}$$
since the [[measure]] in 1D is the length of the interval, which in our case is the diameter of the sphere, i.e. $2p$. The state count at Fermi energy *for each spin* is given as before by the number of particles, divided by $2$:
$$\boxed{G(E_{F})=\frac{N}{2}}$$
The single spin Fermi energy returns the previous result:
$$\boxed{E_{F}=\frac{h^{2}}{2m}\left( \frac{N}{4L} \right)^{2}}$$
The DOS for both spins is
$$\boxed{g(E)=2\frac{ \partial G }{ \partial E } =\frac{4L}{h}\sqrt{ \frac{m}{2E} }}$$
where the $2$ is due to considering both spins. Due to the one state = one particle clause, we can find the Fermi energy exclusively from the DOS, if we somehow have access to it directly:
$$N=\int_{0}^{E_{F}}g(E)\ dE=\int_{0}^{E_{F}} \frac{4L}{h}\sqrt{ \frac{m}{2} }\frac{1}{\sqrt{ E }}\ dE=\frac{8L}{h}\sqrt{ \frac{m}{2} }\sqrt{ E_{F} }$$
Reversing the formula gives the familiar result
$$E_{F}=\frac{h^{2}}{2m}\left( \frac{N}{4L} \right)^{2}$$
##### Zero temperature internal energy
The total [[internal energy]] of a Fermi gas at zero temperature, denoted $E_{0}$, can be found from the Fermi energy. The internal energy is just the sum of the energies of each occupied state. For doubly-degenerate spins in open boundary conditions, that is
$$E_{0}=2\sum_{n=1}^{N/2} \frac{h^{2}n^{2}}{2m(2L)^{2}}=2 \frac{h^{2}}{2m(2L)^{2}}\sum_{i=1}^{N/2} n^{2}$$
We know the sum
$$\sum_{n=1}^{s} n=\frac{s(s+1)}{2}$$
The square is
$$\sum_{n=1}^{s} n^{2}=\frac{s(2s^{2}+3s+1)}{6}\simeq \frac{s^{3}}{3}$$
where the approximation holds at large $s$ (proven by taking an integral instead of a sum, which are essentially the same for large enough numbers). Back to the energy, we have
$$\boxed{E_{0}\simeq \frac{2h^{2}}{2m(2L)^{2}} \frac{1}{3}\left( \frac{N}{2} \right)^{2}=\frac{1}{3}NE_{F}}$$
The $1/3$ factor depends on the dimension, but $N$ and $E_{F}$ are always the same.

The same result can be found from the DOS by energy:
$$E_{0}=\int_{0}^{E_{F}}E\ g(E)\ dE=\frac{N}{3}E_{F}$$
#### 3D
We now move on to 3D, in a volume $V=L^{3}$.
##### Open boundary conditions
Using open boundary conditions in 3D is more challenging. The [[Hamiltonian]] is
$$\hat{H}=- \frac{\hbar^{2}}{2m}\nabla ^{2}$$
and we're still in an infinite square well, just a 3D one (an infinite square box?). Our position [[Equazione agli autovalori|eigenfunctions]] are
$$\psi_{n}\propto \sin \frac{\pi n_{x}}{L}\sin \frac{\pi n_{y}}{L}\sin \frac{\pi n_{z}}{L}$$
where $n_{x,y,z}=1,2,3,\ldots$. Our energy eigenvalues are
$$E_{n_{x},n_{y},n_{z}}=\frac{\hbar^{2}}{2m} \frac{\pi^{2}}{L^{2}}(n_{x}^{2}+n_{y}^{2}+n_{z}^{2})$$
Reasonable enough so far. The issue is now finding what the last occupied value is. In 1D it was easy: the number of particles divided by $2$. But here it's complicated, as there are three separate degrees of freedom. For instance, a singly-excited state can be any of $(1,0,0)$, $(0,1,0)$ or $(0,0,1)$. At higher excitations, there are more and more [[combination|combinations]]. In fact, this is a combinatorics problem that we'd need to solve. It's easier to just pick another set of boundary conditions in which this does not happen.
##### Periodic boundary conditions
Using periodic boundary conditions and with wavefunctions $\psi_{\mathbf{k}}(\mathbf{r})=\frac{1}{\sqrt{ V }}e^{i\mathbf{k}\cdot \mathbf{r}}$ for a direction $\mathbf{k}=\frac{2\pi}{L}\hat{\mathbf{n}}$, the Schrödinger equation
$$\hat{H}\psi_{\mathbf{k}}=E_{\mathbf{k}}\psi_{\mathbf{k}}$$
is solved by
$$E_{\mathbf{k}}=\frac{\hbar^{2}}{2m}(k_{x}^{2}+k_{y}^{2}+k_{z}^{2})$$
Again, now we need to figure out what the last occupied $\mathbf{k}$ is, which is the same problem as before since $k\propto n$. Our best bet is to just go with density of states directly.
##### Density of states
The state function is given by the usual [[Thomas-Fermi approximation]] method. For each spin, we have:
$$\boxed{G(E)=\frac{\frac{4\pi}{3}p^{3}}{\left( \frac{2\pi \hbar}{L} \right)^{3}}=\frac{\sqrt{ 2 }V(mE)^{3/2}}{3\pi^{2}\hbar^{3}}}$$
At Fermi energy, the state count *per spin* is still
$$G(E_{F})=\frac{N}{2}$$
This is the saving grace. The Pauli exclusion principle doesn't care about dimensionality and will give the same number of states regardless. The only thing that matters is the number of states for each energy level, i.e. the degeneracy, i.e. the number of spin states. If we compare the two equations, we find
$$\boxed{E_{F}=\frac{\hbar^{2}k_{F}^{2}}{2m}}$$
where we defined the Fermi wave vector as
$$\boxed{k_{F}\equiv\left( 3\pi ^{2} \frac{N}{V} \right)^{1/3}}$$
The DOS function for both spins can be found to be
$$\boxed{g(E)=\frac{2Vm^{3/2}\sqrt{ E }}{\sqrt{ 2 }\pi^{2}\hbar ^{3}}}$$
We can find the number of particles from the DOS:
$$N=G_\text{both spins}(E)=\int_{0}^{E_{F}}g(E)\ dE=\frac{2\sqrt{ 2 }Vm^{3/2}E_{F}^{3/2}}{3\pi ^{2}\hbar^{3}}$$
##### Zero temperature internal energy
The zero temperature internal energy is
$$E_{0}=\int_{0}^{E_{F}}E\ g(E)\ dE=2 \frac{Vm^{3/2}}{\sqrt{ 2 }\pi ^{2}\hbar ^{3}}\int_{0}^{E_{F}}E^{3/2}dE=2 \frac{Vm^{3/2}}{\sqrt{ 2 }\pi ^{2}\hbar ^{3}} \frac{2}{5}E^{5/2}_{F}$$
By using $E_{F}^{5/2}=E_{F}^{3/2}+E_{F}$ and substituting the previous formula for $E_{F}$ in $E_{F}^{3/2}$ we get
$$\boxed{E_{0}=\frac{3}{5}NE_{F}}$$
As we can see, only the numerical factor changed from the 1D version.
### Nonzero temperature
#### Virial expansion of the equation of state
The [[equation of state]] of a fermion ideal gas can be found through a quantum [[ensemble]], with the [[quantum grand canonical ensemble]] being the most convenient. For a derivation, see [[Ideal gas#Equation of state]]. The equation is
$$\frac{P}{k_{B}T}=\frac{1}{\lambda ^{3}}f_{5/2}(z)$$
where $k_{B}$ is the [[Boltzmann constant]], $T$ is the [[temperature]], $\lambda$ is the [[Formula di de Broglie|de Broglie thermal wavelength]] and $f_{5/2}(z)$ is a [[Fermi and Bose functions|Fermi function]]. We can approximate it by using its series representation:
$$\begin{align}
\frac{PV}{Nk_{B}T}&=\frac{Pv}{k_{B}T} \\
&=\frac{v}{\lambda ^{3}_{T}}f_{5/2}(z) \\
&\simeq \frac{v}{\lambda ^{3}_{T}}\left( z- \frac{z^{2}}{2^{5/2}}+\ldots \right) \\
&=\ldots
\end{align}$$
($v=V/N$ is the volume per particle). We know that
$$\frac{\lambda ^{3}_{T}}{v}=f_{3/2}(z)=z- \frac{z^{2}}{2^{3/2}}+\ldots\quad\Rightarrow \quad z=\frac{\lambda ^{3}_{T}}{v}+ \frac{z^{2}}{2^{3/2}}-\ldots$$
If we substitute $z$ with its first order approximation $\lambda ^{3}_{T}/v$ (???) we get
$$z=\frac{\lambda ^{3}}{v}+ \frac{1}{2^{3/2}} \left( \frac{\lambda ^{3}}{v} \right)^{2}-\ldots$$
and if we put this back in the equation of state we get
$$\begin{align}
\ldots&\simeq \frac{v}{\lambda ^{3}_{T}}\left[ \frac{\lambda ^{3}_{T}}{v}+ \frac{1}{2^{3/2}}\left( \frac{\lambda ^{3}_{T}}{v} \right)^{2}-\ldots +\left(\frac{\lambda ^{3}_{T}}{v} + \frac{1}{2^{3/2}}\left( \frac{\lambda ^{3}_{T}}{v} \right)^{2}-\ldots \right)^{2} \frac{1}{2^{5/2}}+\ldots \right] \\
&=1+ \frac{1}{2^{3/2}} \frac{\lambda_{T}^{3}}{v}- \frac{1}{2^{5/2}}\frac{\lambda ^{3}_{T}}{v} +\ldots \\
&=1+ \frac{1}{2^{5/2}} \frac{\lambda ^{3}_{T}}{v}+\ldots
\end{align}$$
Note the consequence here. The classical ideal gas is
$$\frac{PV}{Nk_{B}T}=1$$
Meanwhile, a fermion ideal gas is
$$\boxed{\frac{PV}{Nk_{B}T}=1+ \frac{1}{2^{5/2}} \frac{\lambda_{T}^{3}}{v}+\ldots}$$
This expansion is a form of the [[virial expansion]] and the terms are called **virial coefficients**. Specifically, the term after $1$ is the **second virial coefficient** and is usually  the most relevant one. This series isn't a new thing in statistical mechanics: the virial expansion normally occurs when you generalize an ideal gas to an [[interacting gas]], which also includes internal interactions. But there are no interactions here, it's just inert fermions. The pseudo-interaction is the manifestation of the [[Pauli exclusion principle|Pauli exclusion principle]], which can be interpreted as a sort of repulsive force between fermions that prevents them from occupying the same [[stato|state]]. It's not *really* a potential, but it certainly behaves like one.
#### Fermi energy
All virial coefficients except the first are only relevant at temperatures that are low compared to the [[Fermi energy|Fermi temperature]]. Far above and the Fermi-Dirac distribution converges to the [[Maxwell-Boltzmann statistic]], which gives the classical results. But since we are at low temperature anyway, we might as well use the [[Sommerfeld expansion]]. This lets us explore the behavior of the Fermi energy at low-but-not-zero temperatures.

Starting from the density equation and using only the first term of the expansion
$$n\lambda ^{3}_{T}=\frac{1}{v}\lambda ^{3}_{T}=f_{3/2}(z)\quad \to \quad\frac{1}{v}\left( \frac{2\pi \hbar^{2}}{mk_{B}T} \right)^{3/2}\simeq \frac{4}{3\sqrt{ \pi }}(\ln z)^{3/2}$$
The logarithm is
$$\ln z=\left( \frac{3\sqrt{ \pi }}{4v} \right)^{2/3} \frac{2\pi \hbar^{2}}{mk_{B}T}$$
But we also have
$$z\simeq e^{\beta E_{F}}\quad\to \quad \beta E_{F}\simeq \ln z$$
As such, the Fermi energy is
$$E_{F}=k_{B}T\ln z\simeq\frac{\hbar^{2}}{2m}\left( \frac{6\pi^{2}}{v} \right)^{2/3}=\frac{\hbar^{2}}{2m}\left( \frac{6\pi^{2}N}{V} \right)^{2/3}$$
The average [[occupation number]] is
$$\langle n_{\mathbf{p}} \rangle \simeq \frac{1}{e^{\beta(\varepsilon_{\mathbf{p}}-E_{F})}+1}$$
If $\varepsilon_{\mathbf{p}}<E_{F}$ we get $\langle n_{\mathbf{p}} \rangle\simeq1$, otherwise $\langle n_{\mathbf{p}} \rangle\simeq0$.

Up until now, we've ignored the presence of [[spin]]. If we call the spin $s$, the spin [[Degenerazione|degeneracy]] is going to be
$$g=2s+1$$
and the following condition must hold:
$$g\sum_{\mathbf{p}} \langle n_{\mathbf{p}} \rangle_{T=0} =N$$
A $g$-degenerate gas of $N$ fermions behaves like $g$ independent Fermi gases stacked on top of each other. In this case, the Fermi energy is
$$\frac{g}{2\pi \hbar} \frac{4\pi}{3}p_{F}^{3}=\frac{N}{V}\quad\to \quad E_{F}=\frac{\hbar^{2}k_{F}^{2}}{2m}=\frac{\hbar^{2}}{2m}\left( \frac{6\pi ^{2}}{gv} \right)^{2/3}$$
$$\frac{\lambda ^{3}_{T}}{v}=f_{3/2}(z)=\frac{4}{3\sqrt{ \pi }}\left[ (\ln z)^{3/2}+ \frac{\pi^{2}}{8}(\ln z)^{-1/2}+\ldots \right]$$
$$(\ln z)^{3/2}+ \frac{\pi^{2}}{8}(\ln z)^{-1/2}\simeq \frac{3\sqrt{ \pi }}{4v}\lambda_{T}^{3}$$
Higher degeneracy reduces the Fermi energy. For $T=0$, we still have $\mu=E_{F}$. However, for non-zero temperature we must take some terms from the expansion:
$$\boxed{\mu=E_{F}\left[ 1- \frac{\pi^{2}}{12}\left( \frac{k_{B}T}{E_{F}} \right)^{2}+\ldots \right]=E_{F}\left[ 1- \frac{\pi^{2}}{12}\left( \frac{T}{T_{F}} \right)^{2}+\ldots \right]}$$
where $T_{F}=E_{F}/k_{B}$ is the Fermi temperature. The impact of these corrections is dependent on the ratio between temperature and Fermi temperature, which means that "high" or "low" temperature here is entirely define with respect to the Fermi temperature. The latter is found on a material-by-material basis. For instance, in metals it is $T_{F}\sim 10^{4}\text{ K}$, which means that for room temperature metals ($T\sim 300\text{ K}$), all corrections are tiny expect at most the first. In [[Stella di neutroni|neutron stars]], $T_{F}> 10^{7}\text{ K}$.
#### Internal energy
The [[internal energy]] $U$ of the gas could be derived by direct integration:
$$\begin{align}
U&=\sum_{\mathbf{p}}\varepsilon_{\mathbf{p}}\langle n_{\mathbf{p}} \rangle  \\
&=\frac{V}{h^{3}} \frac{4\pi}{2m}\int_{0}^{\infty} p^{4}\langle n_{\mathbf{p}} \rangle dp \\
&=\frac{V}{4\pi ^{2}m\hbar ^{3}}\int_{0}^{\infty} \frac{p^{5}}{5}\left( -\frac{ \partial  }{ \partial p } \langle n_{\mathbf{p}} \rangle  \right) \\
&=\frac{\beta V}{20\pi ^{2}m^{2}\hbar ^{2}}\int_{0}^{\infty} \frac{p^{6}e^{\beta \varepsilon_{\mathbf{p}}-v}}{(e^{\beta \varepsilon_{\mathbf{p}}}+1)^{2}}
\end{align}$$
That said, this integral is a mess. It's much easier to use something like a [[quantum grand canonical ensemble]] and use its [[partition function]]:
$$\frac{PV}{k_{B}T}=\ln \mathcal{Z}$$
and use the relation
$$U=-\left( \frac{ \partial  }{ \partial \beta } \ln \mathcal{Z} \right)_{Z,V}=-V\frac{ \partial  }{ \partial \beta }  \frac{P}{k_{B}T}=-V\left( \frac{ \partial  }{ \partial \beta } \frac{f_{5/2}(z)}{\lambda ^{3}_{T}} \right)_{Z,V}$$
The $f_{5/2}(z)$ function is independent from $\beta$, so we only need
$$\frac{ \partial  }{ \partial \beta } \frac{1}{\lambda ^{3}_{T}}=\frac{ \partial  }{ \partial \beta } \left( 2\pi \hbar ^{2} \frac{\beta}{m} \right)^{-3/2}=- \frac{3}{2\beta}\left( 2\pi \hbar ^{2} \frac{\beta}{m} \right)^{-3/2}=- \frac{3}{2}k_{B}T \frac{1}{\lambda ^{3}_{T}}$$
We can finally write
$$\boxed{U=\frac{3}{2}Nk_{B}T \frac{f_{5/2}(z)}{f_{3/2}(z)}}$$
This is essentially an extended [[equipartition theorem]]. Unfortunately, actually calculating the two $f$ function is complicated or straight-up impossible. We can however use a [[Sommerfeld expansion]] for both of them at $z\gg 1$. The $f_{3/2}$ expansion is above. The $f_{5/2}$ expansion is
$$f_{5/2}(z)=\frac{8}{15\sqrt{ \pi }}(\ln z)^{5/2}\left[ 1+ \frac{5\pi^{2}}{8} \frac{1}{(\ln z)^{2}}+\ldots \right]$$
Using the first term of each we get
$$U=\frac{3}{2}Nk_{B}T\left[  \frac{\frac{8}{15\sqrt{ \pi }}(\ln z)^{5/2}}{\frac{4}{3\sqrt{ \pi }}(\ln z)^{3/2}} \right]=\frac{3}{2}Nk_{B}T \frac{2}{5}\ln z$$
For $T=0$ we can see $k_{B}T\ln z=\mu=E_{F}$ and we have
$$\boxed{U=\frac{3}{5} NE_{F}}$$
which proves that this is a self-consistent description. If we add more terms we get
$$\begin{align}
U&=\frac{3}{2}Nk_{B}T \frac{2}{5}\ln z \left[ \frac{1+ \frac{5\pi ^{2}}{8} \frac{1}{(\ln z)^{2}}}{1+ \frac{\pi ^{2}}{8} \frac{1}{(\ln z)^{2}}} \right] \\
&\simeq\frac{3}{2}Nk_{B}T \frac{2}{5}\ln z\left( 1+ \frac{5\pi ^{2}}{8} \frac{1}{(\log z)^{2}} \right)\left( 1- \frac{\pi ^{2}}{8} \frac{1}{(\ln z)^{2}} \right) \\
&\simeq \frac{3}{5}Nk_{B}T\ln z\left( 1- \frac{\pi ^{2}}{2} \frac{1}{(\ln z)^{2}} \right)
\end{align}$$
and so
$$\boxed{U=\frac{3}{5}NE_{F}\left( 1- \frac{\pi ^{2}}{2} \frac{1}{(\ln z)}^{2} \right)}$$
From this, we can find other thermodynamic quantities.