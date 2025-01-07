Entropy
$$S=k_{B}\log W,\qquad \Delta S=\int_{A}^{B} \frac{\delta Q}{T}$$
Useful to change constraints on a quantity (like chemical potential). Number of states in a boolean (occupied/unoccupied) lattice of $n$ sites where $k$ are occupied is the binomial coefficient $\begin{pmatrix}n \\ k\end{pmatrix}$.
### Mathematics
Binomial theorem and Gamma function
$$(x+y)^{n}=\sum_{k=0}^{n}\begin{pmatrix}n \\ k\end{pmatrix}x^{n-k}y^{k}=\sum_{k=0}^{n}\begin{pmatrix}n \\ k\end{pmatrix}x^{k}y^{n-k},\qquad\Gamma(z)=\int_{0}^{\infty}w^{z-1}e^{-w}dw$$
$$\Gamma\left( \frac{1}{2} \right)=\sqrt{ \pi },\quad \Gamma(1)=1,\quad \Gamma(z+1)=n\Gamma(z),\quad \Gamma(n)=(n-1)!$$
Stirling's approximation
$$\ln n! =n\ln n-n+O(\ln n)$$
Partial derivatives under constraints:
$$\left( \frac{ \partial x }{ \partial y }  \right)_{z}\left( \frac{ \partial y }{ \partial z }  \right)_{x}\left( \frac{ \partial z }{ \partial x }  \right)_{y}=-1\quad\to \quad\left( \frac{ \partial x }{ \partial y }  \right)_{z}=-\left( \frac{ \partial z }{ \partial y }  \right)_{x}\left( \frac{ \partial x }{ \partial z }  \right)_{y}$$
### Maxwell relations
$$T=\left( \frac{ \partial U }{ \partial S }  \right)_{V}\qquad P=\left( \frac{ \partial U }{ \partial V }  \right)_{S},\qquad T=\left( \frac{ \partial H }{ \partial S }  \right)_{P}\qquad V=\left( \frac{ \partial H }{ \partial P }  \right)_{S}$$
$$P=-\left( \frac{ \partial A }{ \partial V }  \right)_{T}\qquad S=-\left( \frac{ \partial A }{ \partial T }  \right)_{V},\qquad S=-\left( \frac{ \partial G }{ \partial T }  \right)_{P}\qquad V=\left( \frac{ \partial G }{ \partial P }  \right)_{T}$$
#### Adjacent relations
$$P=T \frac{ \partial S }{ \partial V } ,\qquad\mu=\left( \frac{ \partial E }{ \partial N }  \right)_{S,V}=-T\left( \frac{ \partial S }{ \partial N }  \right)_{E,V}=\left( \frac{ \partial A }{ \partial N }  \right)_{V,T}=\left( \frac{ \partial G }{ \partial N }  \right)_{P,T}$$
### Ensembles
Microcanonical density function
$$\rho(\mathbf{q},\mathbf{p})=\begin{cases}
\text{constant} & E<H(\mathbf{q},\mathbf{p})<E+\Delta \\
0&\text{otherwise}
\end{cases}$$
Canonical density function and partition function
$$\rho(\mathbf{q},\mathbf{p})=\frac{1}{Q_{N}}e^{-\beta H(\mathbf{q},\mathbf{p})},\qquad Q_{N}(V,T)=\int \frac{e^{-\beta H(\mathbf{q},\mathbf{p})}}{h^{3N}N!} \ d^{3N}q\,d^{3N}p$$
Grand canonical density function and partition function
$$\rho(Z,V,T)=Z^{N}Q_{N}(V,T),\qquad\mathcal{Z}(Z,V,T)\equiv \sum_{N=0}^{\infty} Z^{N}Q_{N}(V,T)$$
### Partition function
Internal energy
$$U=-\frac{ \partial  }{ \partial \beta } \ln Z$$
Helmholtz free energy
$$Z=e^{-\beta A}\quad\Rightarrow \quad A=- \frac{1}{\beta} \ln Z$$
## Esercizi
Uno degli esercizi dell'esame è sicuramente "gas di fermioni/bosoni in 1/2/3/4 dimensioni con distribuzione in $p$/$p^{2}$". Sono 16 possibili combinazioni.