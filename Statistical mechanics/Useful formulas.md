### Mathematics
Binomial theorem and Gamma function
$$(x+y)^{n}=\sum_{k=0}^{n}\begin{pmatrix}n \\ k\end{pmatrix}x^{n-k}y^{k}=\sum_{k=0}^{n}\begin{pmatrix}n \\ k\end{pmatrix}x^{k}y^{n-k},\qquad\Gamma(z)=\int_{0}^{\infty}w^{z-1}e^{-w}dw$$
$$\Gamma\left( \frac{1}{2} \right)=\sqrt{ \pi },\quad \Gamma(1)=1,\quad \Gamma(z+1)=n\Gamma(z),\quad \Gamma(n)=(n-1)!$$
Stirling's approximation
$$\ln n! =n\ln n-n+O(\ln n)$$
Partial derivatives under constraints:
$$\left( \frac{ \partial x }{ \partial y }  \right)_{z}\left( \frac{ \partial y }{ \partial z }  \right)_{x}\left( \frac{ \partial z }{ \partial x }  \right)_{y}=-1\quad\to \quad\left( \frac{ \partial x }{ \partial y }  \right)_{z}=-\left( \frac{ \partial z }{ \partial y }  \right)_{x}\left( \frac{ \partial x }{ \partial z }  \right)_{y}$$
Useful to change constraints on a quantity (like chemical potential). Number of states in a boolean (occupied/unoccupied) lattice of $n$ sites where $k$ are occupied is the binomial coefficient $\begin{pmatrix}n \\ k\end{pmatrix}$. Gaussian integrals:
$$\int_{-\infty}^{\infty} e^{-ax^{2}} \ dx=\sqrt{ \frac{\pi}{a} } ,\qquad\int_{-\infty}^{\infty} x^{2}e^{-ax^{2}} \ dx=\frac{\sqrt{ \pi }}{2a^{3/2}}$$
### Constants
$$k_{B}=1.38\cdot10^{-23}\text{ J/K}$$
### Entropy
$$S_\text{inf}=-\sum_{x}p(x)\log p(x),\qquad W\text{ equiprobable events} \to S=\log W$$
Equilibrium state is highest entropy state. In the microcanonical
$$S=k_{B}\log \Gamma(E)$$
From thermodynamics
$$S=\int_{0}^{T} \frac{C_{V}}{T}dT$$
### Common quantities
$$A=U-TS,\qquad G=A+PV,\qquad C_{V}=\frac{ \partial U }{ \partial T },\qquad \frac{1}{\lambda ^{3}}=\left( \frac{2\pi m}{\beta h^{2}} \right)^{3/2} $$
### Maxwell relations
$$T=\left( \frac{ \partial U }{ \partial S }  \right)_{V}\qquad P=\left( \frac{ \partial U }{ \partial V }  \right)_{S},\qquad T=\left( \frac{ \partial H }{ \partial S }  \right)_{P}\qquad V=\left( \frac{ \partial H }{ \partial P }  \right)_{S}$$
$$P=-\left( \frac{ \partial A }{ \partial V }  \right)_{T}\qquad S=-\left( \frac{ \partial A }{ \partial T }  \right)_{V},\qquad S=-\left( \frac{ \partial G }{ \partial T }  \right)_{P}\qquad V=\left( \frac{ \partial G }{ \partial P }  \right)_{T}$$
#### Adjacent relations
$$P=T \frac{ \partial S }{ \partial V } ,\qquad\mu=\left( \frac{ \partial U }{ \partial N }  \right)_{S,V}=-T\left( \frac{ \partial S }{ \partial N }  \right)_{E,V}=\left( \frac{ \partial A }{ \partial N }  \right)_{V,T}=\left( \frac{ \partial G }{ \partial N }  \right)_{P,T}$$
### Ensemble density/partition functions
Microcanonical density function
$$\rho(\mathbf{q},\mathbf{p})=\begin{cases}
\text{constant} & E<H(\mathbf{q},\mathbf{p})<E+\Delta \\
0&\text{otherwise}
\end{cases}$$
Canonical density function and partition function
$$\rho(\mathbf{q},\mathbf{p})=e^{-\beta H(\mathbf{q},\mathbf{p})},\qquad Q_{N}(V,T)\equiv\int \frac{e^{-\beta H(\mathbf{q},\mathbf{p})}}{h^{3N}N!} \ d^{3N}q\,d^{3N}p$$
$$U=-\frac{ \partial  }{ \partial \beta } \ln Q_{N},\qquad A=- \frac{1}{\beta}\ln Q_{N}$$
Grand canonical density function and partition function
$$\rho(z,V,T)=z^{N}Q_{N}(V,T),\qquad\mathcal{Z}(z,V,T)\equiv \sum_{N=0}^{\infty} z^{N}Q_{N}(V,T)$$
$$U=-\left( \frac{ \partial  }{ \partial \beta } \ln \mathcal{Z} \right)_{N,V},\qquad \frac{PV}{k_{B}T}=\ln \mathcal{Z}\text{ (ideal gas)}$$
### Particle statistics
$$\langle n_{\varepsilon} \rangle =\frac{1}{e^{\beta(\varepsilon-\mu)}\pm 1}=\frac{1}{z^{-1}e^{\beta \varepsilon}\pm 1}$$
$+$ for Fermi-Dirac, $-$ for Bose-Einstein. Condensation happens when $\mu= 0$ and $\varepsilon\to 0$. Classical particles (Maxwell-Boltzmann) remove $\pm 1$.
## Esercizi
Uno degli esercizi dell'esame è sicuramente "gas di fermioni/bosoni in 1/2/3/4 dimensioni con distribuzione in $p$/$p^{2}$". Sono 16 possibili combinazioni.