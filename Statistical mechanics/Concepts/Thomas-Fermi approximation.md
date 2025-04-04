The **Thomas-Fermi approximation** is an approximation used to express the [[Degenerazione|degeneracy]] of [[Stato|states]] of a nonrelativistic quantum [[ideal gas]] as a [[Differential|differential]] instead of a discrete sequence. This transforms sums into integrals and allows for analytical computation using, for instance, the [[partition function]] of a quantum [[ensemble]].

The approximation holds for a large number of [[Particella|particles]] and high volume, which means that it automatically applies in the [[thermodynamic limit]].
### Description
A quantum ideal gas is composed of [[Particella libera (quantistica)|free particles]] inside of a perfect enclosure of sides $L$, which can be seen as an [[Buca infinita quantistica|infinite square well]] in some number of dimensions. Since the particles are free, their [[Equazione agli autovalori|eigenfunctions]] are [[Plane wave|plane waves]]: $\psi\propto e^{i\mathbf{p}\cdot \mathbf{r}/\hbar}$. Calling $\mathbf{n}=(n_{x},n_{y},n_{z})$ the direction of the momentum $\mathbf{p}$, we get (using periodic boundary conditions, they are necessary for this proof!)
$$\mathbf{p}=\frac{2\pi \hbar}{L} \mathbf{n}$$
where $\hbar$ is the [[Planck constant|reduced Planck constant]]. This is like saying that there is one possible state of $\mathbf{p}$ for every "volume" $\left( \frac{2\pi \hbar}{L} \right)^{3}$ (the volume is in momentum [[phase space]]). There is only a discrete number of possible states, enumerated by the components of the direction (in this sense, it is not really a direction as it is not [[Normalization|normalized]]. It's more like a [[Numero quantico|quantum number]] position vector in phase space). We can use this fact to count quantum states. Call $G(\varepsilon)$ the number of states up to an [[energy]] $\varepsilon=p^{2}/2m$ where $p=\lvert \mathbf{p} \rvert$ for simplicity. If the number of particles is very large ($N\gg 1$), the number of states is itself going to be very large. More importantly, the separation between states is going to be so tiny with respect to the [[internal energy]] of the system that we can think of $G(\varepsilon)$ as approximately continuous. Because of this, we can allow ourselves to take its derivative
$$g(\varepsilon)=\frac{ \partial G(\varepsilon) }{ \partial \varepsilon } $$
This is known as the **density of states (DOS)** function, and it can be used to turn integrals in three momentum dimensions into integrals of one energy dimension.

A set value of $\varepsilon$ defines a [[Palla|sphere]] in momentum space (it is the locus of all points for which $p^{2}/2m\leq\varepsilon$). All momentum values contained in the sphere are $\varepsilon_{p}<\varepsilon$. We want to count these. Thankfully, we know both the volume of a sphere and the volume of each state, so the number of states is the ratio of these (i.e. how many state volumes fit inside the sphere volume):
$$G(\varepsilon)=\frac{\frac{4\pi}{3}p^{3}}{\left( \frac{2\pi \hbar}{L} \right)^{3}}=\frac{\frac{4\pi}{3}(2m\varepsilon)^{3/2}}{(2\pi \hbar)^{3}}V= \frac{\sqrt{ 2 }}{3\pi ^{2}} \frac{(m\varepsilon)^{3/2}}{\hbar ^{3}}V$$
If we take the derivative of $\varepsilon$ we get
$$\boxed{g(\varepsilon)=\frac{Vm^{3/2}}{\sqrt{ 2 }\pi ^{2}\hbar ^{3}}\sqrt{ \varepsilon }}$$
This leads to the conclusion that the density of states in three dimensions is proportional to the square root of energy. This is a fact that is seen in several [[Physical system|systems]], from [[Atomo|atoms]] to [[Stella|stars]].
#### $N$ dimensions
More generally, an $N$ dimensional ideal gas behaves like
$$G(\varepsilon)\propto p^{d}\propto (\sqrt{ \varepsilon })^{d}\propto \varepsilon^{d/2},\qquad g(\varepsilon)\propto \varepsilon^{d/2-1}$$
This leads to some weird behavior in lower dimensions, where $d=2$ implies that state density is completely independent of energy and in $d=1$, it is inversely proportional to it.

In general, the DOS function has the form
$$\boxed{g(\varepsilon)=C_{\alpha}\varepsilon^{\alpha-1}}$$
where $\alpha=d/2$ is a real number that is half the dimension of the system. For instance, in the 3D gas above we have $\alpha=3/2$.
### Consequences
The intended use case for this approximation is turning sums over quantum states to integrals over energy. For instance, in a [[Fermi gas|Fermi]] or [[Bose gas]], the number of particles is
$$N=\sum_{\varepsilon} \frac{1}{z^{-1}e^{\beta \varepsilon}\pm 1}$$
In the Thomas-Fermi approximation, this becomes
$$N=\int_{0}^{\infty} \frac{g(\varepsilon)}{z^{-1}e^{\beta \varepsilon}\pm 1}d\varepsilon=C_{\alpha}\int_{0}^{\infty} \frac{\varepsilon^{\alpha-1}}{z^{-1}e^{\beta \varepsilon}\pm 1}d\varepsilon$$
This integral can't be solved, but the [[Sommerfeld expansion]] provides a strong approximation for high $z$. They can be analytically written using [[Fermi and Bose functions]]. A more general notation could be
$$\sum_{\varepsilon} \langle n_{\varepsilon} \rangle \to \int_{0}^{\infty}g(\varepsilon)\langle n_{\varepsilon} \rangle d\varepsilon $$

> [!warning] Integration variable
> When you make the approximation above, make sure that the integration variable is the same one that you're using to label the states! If you use a different variable, your integral will be wrong by the constant $a$ such that $d\varepsilon=a\ dx$, where $x$ is the variable you were supposed to use ($k$, $p$, $\omega$,...). For instance, if your sum is over [[wave vector]] $k$, you must integrate over $dk$. If you integrate over $d\varepsilon$, you'll be wrong by $\hbar c$ since you'll need to substitute $d\varepsilon=\hbar c\ dk$.
