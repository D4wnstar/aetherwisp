The **Fermi-Dirac distribution** is a [[probability distribution]] that describes the behavior of a [[Physical system|system]] of $N$ [[Fermion|fermions]] in [[thermal equilibrium]]. Its [[probability density function]] is
$$\langle n_{i} \rangle =\frac{1}{e^{\beta(\varepsilon_{i}-\mu)}+1}$$
$\langle n_{i} \rangle$ is the average number of fermions in the $i$-th single-[[Particella|particle]] [[stato|state]] of energy $\varepsilon_{i}$, $\mu$ is the system [[chemical potential]] and $\beta=1/k_{B}T$ is the inverse temperature, with $k_{B}$ the [[Boltzmann constant]] and $T$ the [[temperature]]. The [[Normalizzazione|normalization]] constant is
$$\sum_{i}n_{i}=N$$
Since we are working with fermions, the [[Pauli exclusion principle|Pauli exclusion principle]] must hold, which is to say that $\langle n_{i} \rangle< 1$.
### ?
$$f_{3/2}(z)=\sum_{l=1}^{\infty} \frac{(-1)^{l+1}z^{l}}{l^{3/2}}=z\frac{ \partial  }{ \partial z }f_{5/2}(z)=\frac{4}{\sqrt{ \pi }}\int_{0}^{\infty} \frac{x^{2}}{z^{-1}e^{x^{2}}+1}\ dx$$
The first few terms are
$$f_{3/2}(z)=z- \frac{z^{2}}{2^{3/2}}+ \frac{z^{3}}{z^{3/2}}-\ldots$$
### Sommerfeld expansions
The $f_{3/2}(z)$ can be expanded in terms of $\ln z$, which is useful for large $z$. That said, the derivation is somewhat convoluted[^1].

Let's start from
$$\nu=\beta \mu=\frac{\mu}{k_{B}T}=\ln z$$
We can write
$$f_{3/2}(z)=\frac{4}{\sqrt{ \pi }}\int_{0}^{\infty} \frac{x^{2}}{e^{x^{2}-\nu}+1}\ dx=\frac{4}{2\sqrt{ \pi }}\int_{0}^{\infty} \frac{\sqrt{ y }}{e^{y-\nu}+1}\ dy=\frac{4}{3\sqrt{ \pi }}\int_{0}^{\infty} \frac{y^{3/2}e^{y-\nu}}{(e^{y-\nu}+1)^{2}}\ dy=\ldots$$
using the $x^{2}=y$ substitution. The last step is from [[Integrazione per parti|integration by parts]] on
$$f=\frac{1}{e^{y-\nu}+1}$$
and $g=\sqrt{ y }$. The integrand is peaked around $\nu$. Making the further substitution $y=\nu+t$, we get
$$\ldots=\frac{4\nu^{3/2}}{3\sqrt{ \pi }}\int_{-\nu}^{\infty} \left( 1+ \frac{t}{\nu} \right)^{3/2} \frac{e^{t}}{(e^{t}+1)^{2}}=\ldots$$
Since the integral peaks around $\nu$, we might as well extend the lower bound to $-\infty$
$$\ldots\simeq \frac{4\nu^{3/2}}{3\sqrt{ \pi }}\int_{-\infty}^{\infty}\left( 1 + \frac{t}{\nu} \right)^{3/2} \frac{e^{t}}{(e^{t}+1)^{2}}\ dt=\ldots$$
Now, using the expansion
$$\left( 1+ \frac{t}{\nu} \right)^{3/2}\simeq 1+ \frac{3}{2} \frac{t}{\nu}+ \frac{3}{8} \frac{t^{2}}{\nu ^{2}}+\ldots$$
we can write
$$\ldots= \frac{4\nu^{3/2}}{3\sqrt{ \pi }}\int_{-\infty}^{\infty}\left( 1+ \frac{3}{2} \frac{t}{\nu} + \frac{3}{8} \frac{t^{2}}{\nu ^{2}}+ \ldots \right) \frac{e^{t}}{(e^{t}+1)^{2}}=\frac{4\nu^{3/2}}{3\sqrt{ \pi }} \left( I_{0}+ \frac{3}{\sqrt{ \pi }}I_{1}+\ldots \right)$$
The $I_{n}$ are the expansion coefficients (TODO: The previous equation is probably somewhat wrong). From this, we can state
$$\begin{align}
z\ll 1\qquad&f_{3/2}(z)=z- \frac{z^{2}}{2^{3/2}}+ \frac{z^{3}}{3^{3/2}}-\ldots \\
z\gg 1\qquad& f_{3/2}(z)=\frac{4}{3\sqrt{ \pi }}\left[ (\ln z)^{3/2}+ \frac{\pi ^{2}}{8} \frac{1}{(\ln z)^{3/2}}+\ldots \right]
\end{align}$$
...

The $f_{3/2}(z)$ connects specific volume to the thermal wavelength:
$$\frac{1}{v}=\frac{N}{V}=\frac{1}{\lambda ^{3}_{T}}f_{3/2}(z)$$
Interparticle distance is on the order of $\sim v^{1/3}$. For high temperature, the de Broglie thermal wavelength is tiny, way smaller than $v^{1/3}$, (in symbols, $v^{1/3}\gg \lambda_{T}$) so the wave nature of matter becomes irrelevant and we see classical physics. Having low density (and so high $v$ compared to $\lambda_{T}$) is one way of ignoring quantum effects.
### Ideal gas
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