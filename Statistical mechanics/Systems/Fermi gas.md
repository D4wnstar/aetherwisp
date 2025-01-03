A **Fermi gas** is a model for a [[Physical system|system]] of many non-interacting [[Fermion|fermions]], the simplest example of which is a fermionic [[ideal gas]]. The key property is that fermions are subject to the [[Pauli exclusion principle]] and can't simultaneously occupy the same [[stato|state]], which leads to a "pseudo-[[Potenziale|potential]]" that pushes fermions away from each other.
### Equation of state
The [[equation of state]] of a fermion ideal gas can be found through a quantum [[ensemble]], with the [[quantum grand canonical ensemble]] being the most convenient. For a derivation, see [[Ideal gas#Equation of state]]. The equation is
$$\frac{P}{k_{B}T}=\frac{1}{\lambda ^{3}}f_{5/2}(z)$$
where $k_{B}$ is the [[Boltzmann constant]], $T$ is the [[temperature]], $\lambda$ is the [[Formula di de Broglie|de Broglie thermal wavelength]] and $f_{5/2}(z)$ is a [[Fermi and Bose functions|Fermi function]]. This function can be written as a [[serie di potenze|power series]] through a [[Sommerfeld expansion]].
$$\begin{align}
\frac{PV}{Nk_{B}T}&=\frac{Pv}{k_{B}T} \\
&=\frac{v}{\lambda ^{3}_{T}}f_{3/2}(z) \\
&\simeq \frac{v}{\lambda ^{3}_{T}}\left( z- \frac{z^{2}}{2^{3/2}}+\ldots \right) \\
&\simeq \frac{v}{\lambda ^{3}_{T}}\left[ \frac{\lambda ^{3}_{T}}{v}+ \frac{1}{2^{3/2}}\left( \frac{\lambda ^{3}_{T}}{v} \right)-\left(\frac{\lambda ^{3}_{T}}{v} + \frac{1}{2^{3/2}}\left( \frac{\lambda ^{3}_{T}}{v} \right)^{2} \right)^{5/2} \frac{1}{2^{5/2}}+\ldots \right] \\
&=1+ \frac{1}{2^{3/2}} \frac{\lambda_{T}^{3}}{v}- \frac{1}{2^{5/2}}\frac{\lambda ^{3}_{T}}{v} +\ldots
\end{align}$$
Note the consequence here. The classical ideal gas is
$$\frac{PV}{Nk_{B}T}=1$$
Meanwhile, a fermion ideal gas is
$$\boxed{\frac{PV}{Nk_{B}T}=1+ \frac{1}{2^{5/2}} \frac{\lambda_{T}^{3}}{v}+\ldots}$$
We have an expansion with many terms beyond 1. The term beyond one is called the **second virial coefficient**. This normally occurs when you extend an ideal gas to also have internal interactions between particles. But there are no interactions here, it's just fermions. What this is, is the manifestation of the [[Pauli exclusion principle|Pauli exclusion principle]], which can be interpreted as a sort of repulsive interaction between fermions that prevents them from occupying the same [[stato|state]]. It's not *really* a potential, but it behaves like one.
### Behavior
In the low-temperature limit $T\to 0$ and due to the exclusion principle, the [[Fermi-Dirac distribution]] approximately becomes
$$\langle n_{p} \rangle =\frac{1}{e^{\beta(\varepsilon_{p}-\mu)}+1}\to \begin{cases}
0 & \text{ if }\varepsilon_{p}>\mu \\
1 & \text{ if }\varepsilon_{p}<\mu
\end{cases}$$
What this means is that all states with energy lower than $\mu$ will be occupied, and all states with higher energy will be vacant. We can use the [[theta di Heaviside|Heaviside step function]] $\Theta$ to represent this symbolically:
$$\lim_{ T \to 0 } \langle n_{p} \rangle=\Theta(\mu-\varepsilon_{p})$$
The specific energy threshold is known as the [[Fermi energy]] $\varepsilon_{F}$ or $E_{F}$. This energy leads to a momentum called the **Fermi momentum** $p_{F}=\sqrt{ 2m\varepsilon_{F} }$. In [[phase space]], this momentum occupies a spherical region, which contains all the occupied states discussed before. This odd state is known as [[quantum degeneracy]] (not to be confused with state [[Degenerazione|degeneracy]], although the two are closely related).

### Behavior
Consider a fermion [[ideal gas]]. From the [[equation of state]] we get
$$\begin{align}
\frac{PV}{Nk_{B}T}&=\frac{Pv}{k_{B}T} \\
&=\frac{v}{\lambda ^{3}_{T}}f_{3/2}(z) \\
&\simeq \frac{v}{\lambda ^{3}_{T}}\left( z- \frac{z^{2}}{2^{3/2}}+\ldots \right) \\
&\simeq \frac{v}{\lambda ^{3}_{T}}\left[ \frac{\lambda ^{3}_{T}}{v}+ \frac{1}{2^{3/2}}\left( \frac{\lambda ^{3}_{T}}{v} \right)-\left(\frac{\lambda ^{3}_{T}}{v} + \frac{1}{2^{3/2}}\left( \frac{\lambda ^{3}_{T}}{v} \right)^{2} \right)^{5/2} \frac{1}{2^{5/2}}+\ldots \right] \\
&=1+ \frac{1}{2^{3/2}} \frac{\lambda_{T}^{3}}{v}- \frac{1}{2^{5/2}}\frac{\lambda ^{3}_{T}}{v} +\ldots
\end{align}$$
Note the consequence here. The classical ideal gas is
$$\frac{PV}{Nk_{B}T}=1$$
Meanwhile, a fermion ideal gas is
$$\boxed{\frac{PV}{Nk_{B}T}=1+ \frac{1}{2^{5/2}} \frac{\lambda_{T}^{3}}{v}+\ldots}$$
We have an expansion with many terms beyond 1. The term beyond one is called the **second virial coefficient**. This normally occurs when you extend an ideal gas to also have internal interactions between particles. But there are no interactions here, it's just fermions. What this is, is the manifestation of the [[Pauli exclusion principle|Pauli exclusion principle]], which can be interpreted as a sort of repulsive interaction between fermions that prevents them from occupying the same [[stato|state]]. It's not *really* a potential, but it behaves like one.

$$\frac{1}{v}\lambda ^{3}_{T}=\frac{1}{v}\left( \frac{2\pi \hbar^{2}}{mk_{B}T} \right)^{3/2}= \frac{4}{3\sqrt{ \pi }}(\ln z)^{3/2}$$
The logarithm is
$$\ln z=\frac{3^{2/3}(\sqrt{ \pi })^{2/3}2\pi \hbar^{2}}{4^{2/3}v^{2/3}mk_{B}T}$$
But we also have
$$z\simeq e^{\beta E_{F}}\quad\to \quad \beta E_{F}\simeq \ln z$$
As such, the Fermi energy is
$$E_{F}=k_{B}T\ln z=\frac{\hbar^{2}}{2m}\left( \frac{6\pi^{2}}{v} \right)^{2/3}=\frac{\hbar^{2}}{2m}\left( \frac{6\pi^{2}N}{V} \right)^{2/3}$$
The average [[occupation number]] is
$$\langle n_{\mathbf{p}} \rangle \simeq \frac{1}{e^{\beta(\varepsilon_{\mathbf{p}}-E_{F})}+1}$$
If $\varepsilon_{\mathbf{p}}<E_{F}$ we get $\langle n_{\mathbf{p}} \rangle=1$, otherwise $\langle n_{\mathbf{p}} \rangle=0$.

Up until now, we've ignored the presence of [[spin]]. If we call the spin $s$, the [[Degenerazione|degeneracy]] is going to be
$$g=2s+1$$
and the following condition must hold:
$$g\sum_{\mathbf{p}} \langle n_{\mathbf{p}} \rangle_{T=0} =N$$
A $g$-degenerate gas of $N$ fermions behaves like $g$ independent ideal gases stacked on top of each other. In this case, the Fermi energy is
$$\frac{g}{2\pi \hbar} \frac{4\pi}{3}p_{F}^{3}=\frac{N}{V}\quad\to \quad E_{F}=\frac{\hbar^{2}K_{F}^{2}}{2m}=\frac{\hbar^{2}}{2m}\left( \frac{6\pi ^{2}}{gv} \right)^{2/3}$$
$$\frac{\lambda ^{3}_{T}}{v}=f_{3/2}(z)=\frac{4}{3\sqrt{ \pi }}\left[ (\ln z)^{3/2}+ \frac{\pi^{2}}{8}(\ln z)^{-1/2}+\ldots \right]$$
$$(\ln z)^{3/2}+ \frac{\pi^{2}}{8}(\ln z)^{-1/2}\simeq \frac{3\sqrt{ \pi }\lambda_{T}^{3}}{4v}$$
Higher degeneracy reduces the Fermi energy. For $T=0$, we have $\mu=E_{F}$. However, for non-zero temperature we must take some terms from the expansion:
$$\boxed{\mu=E_{F}\left[ 1- \frac{\pi^{2}}{12}\left( \frac{k_{B}T}{E_{F}} \right)^{2}+\ldots \right]=E_{F}\left[ 1- \frac{\pi^{2}}{12}\left( \frac{T}{T_{F}} \right)^{2}+\ldots \right]}$$
where $T_{F}=E_{F}/k_{B}$ is the so-called Fermi temperature. The impact of these corrections is dependent on the ratio between temperature and Fermi temperature, which means that "high" or "low" temperature here is entirely define with respect to the Fermi temperature. The latter is found on a material-by-material basis. For instance, in metals it is $T_{F}\sim 10^{4}\text{ K}$, which means that for room temperature metals ($T\sim 300\text{ K}$), all corrections are tiny expect at most the first. In [[Stella di neutroni|neutron stars]], $T_{F}> 10^{7}\text{ K}$.

More generally, when $T\ll T_{F}$, every particle moves to the lowest energy levels, so we get degeneration. Because of this, $T_{F}$ is also known as the **degeneracy temperature**, which is particularly important in later stages of [[Evoluzione stellare|stellar evolution]].
#### Internal energy
The [[internal energy]] $U$ of the gas could be derived by direct integration:
$$\begin{align}
U&=\sum_{\mathbf{p}}\varepsilon_{\mathbf{p}}\langle n_{\mathbf{p}} \rangle  \\
&=\frac{V}{h^{3}} \frac{4\pi}{2m}\int_{0}^{\infty} p^{4}\langle n_{\mathbf{p}} \rangle dp \\
&=\frac{V}{4\pi ^{2}m\hbar ^{3}}\int_{0}^{\infty} \frac{p^{5}}{5}\left( -\frac{ \partial  }{ \partial p } \langle n_{\mathbf{p}} \rangle  \right) \\
&=\frac{\beta V}{20\pi ^{2}m^{2}\hbar ^{2}}\int_{0}^{\infty} \frac{p^{6}e^{\beta \varepsilon_{\mathbf{p}}-v}}{(e^{\beta \varepsilon_{\mathbf{p}}+1})^{2}}
\end{align}$$
That said, this integral is a mess. It's much easier to use something like a [[quantum grand canonical ensemble]] and use its [[partition function]]:
$$\frac{PV}{k_{B}T}=\ln \mathcal{Z}$$
and use the relation
$$U=-\left( \frac{ \partial  }{ \partial \beta } \ln \mathcal{Z} \right)_{Z,V}=-V\frac{ \partial  }{ \partial \beta } \frac{1}{V}\ln \mathcal{Z}=-V\frac{ \partial  }{ \partial \beta }  \frac{P}{k_{B}T}=-V\left( \frac{ \partial  }{ \partial \beta } \frac{f_{5/2}(z)}{\lambda ^{3}_{T}} \right)_{Z,V}$$
The $f_{5/2}(z)$ function is independent from $\beta$, so we only need
$$\frac{ \partial  }{ \partial \beta } \frac{1}{\lambda ^{3}_{T}}=\frac{ \partial  }{ \partial \beta } \left( 2\pi \hbar ^{2} \frac{\beta}{m} \right)^{-3/2}=- \frac{3}{2\beta}\left( 2\pi \hbar ^{2} \frac{\beta}{m} \right)^{-3/2}=- \frac{3}{2}k_{B}T \frac{1}{\lambda ^{3}_{T}}$$
We can finally write
$$U=\frac{3}{2}Nk_{B}T \frac{f_{5/2}(z)}{f_{3/2}(z)}$$
This is essentially an extended [[equipartition theorem]]. Unfortunately, actually calculating the two $f$ function is complicated or straight-up impossible. We can however use a [[Sommerfeld expansion]] for both of them at $z\gg 1$. The $f_{3/2}$ expansion is above. The $f_{5/2}$ expansion is
$$z\gg 1\qquad f_{5/2}(z)=\frac{8}{15\sqrt{ \pi }}(\ln z)^{5/2}\left[ 1+ \frac{5\pi^{2}}{8} \frac{1}{(\ln z)^{2}}+\ldots \right]$$
Substituting them with only the first term, we get
$$U=\frac{3}{2}Nk_{B}T\left[  \frac{\frac{8}{15\sqrt{ \pi }}(\ln z)^{5/2}}{\frac{4}{3\sqrt{ \pi }}(\ln z)^{3/2}} \right]=\frac{3}{2}Nk_{B}T \frac{2}{5}\ln z$$
For $T=0$ we can see $k_{B}T\ln z=\mu=E_{F}$ and we have
$$\boxed{U=\frac{3}{5} NE_{F}}$$
If we add more terms we get
$$\begin{align}
U&=\frac{3}{2}Nk_{B}T \frac{2}{5}\ln z \left[ \frac{1+ \frac{5\pi ^{2}}{8} \frac{1}{(\ln z)^{2}}}{1+ \frac{\pi ^{2}}{8} \frac{1}{(\ln z)^{2}}} \right] \\
&\simeq\frac{3}{2}Nk_{B}T \frac{2}{5}\ln z\left( 1+ \frac{5\pi ^{2}}{8} \frac{1}{(\log z)^{2}} \right)\left( 1- \frac{\pi ^{2}}{8} \frac{1}{(\ln z)^{2}} \right) \\
&\simeq \frac{3}{2}Nk_{B}T\ln z\left( 1- \frac{\pi ^{2}}{2} \frac{1}{(\ln z)^{2}} \right)
\end{align}$$
From this, we can find other thermodynamic quantities.

[^1]: See Kerson Huang's Introduction to Statistical Physics (*not* Statistical Mechanics). For something more general, see Pathria-Beale Statistical Physics.