Entropy
$$S=k_{B}\log W,\qquad \Delta S=\int_{A}^{B} \frac{\delta Q}{T}$$
Temperature
$$\frac{1}{T}=\frac{ \partial S }{ \partial E } $$
Pressure
$$P=T \frac{ \partial S }{ \partial V } $$
Chemical potential:
$$\mu=\left( \frac{ \partial E }{ \partial N }  \right)_{S,V}=-T\left( \frac{ \partial S }{ \partial N }  \right)_{E,V}=\left( \frac{ \partial A }{ \partial N }  \right)_{V,T}=\left( \frac{ \partial G }{ \partial N }  \right)_{P,T}$$
Partial derivatives under constraints:
$$\left( \frac{ \partial x }{ \partial y }  \right)_{z}\left( \frac{ \partial y }{ \partial z }  \right)_{x}\left( \frac{ \partial z }{ \partial x }  \right)_{y}=-1\quad\to \quad\left( \frac{ \partial x }{ \partial y }  \right)_{z}=-\left( \frac{ \partial z }{ \partial y }  \right)_{x}\left( \frac{ \partial x }{ \partial z }  \right)_{y}$$
Useful to change constraints on a quantity (like chemical potential).
### Ensembles
Microcanonical density function
$$\rho(\mathbf{q},\mathbf{p})=\begin{cases}
\text{constant} & E<H(\mathbf{q},\mathbf{p})<E+\Delta \\
0&\text{otherwise}
\end{cases}$$
Canonical density function and partition function
$$\rho(\mathbf{q},\mathbf{p})=\frac{1}{Q_{N}}e^{-\beta H(\mathbf{q},\mathbf{p})},\qquad Q_{N}(V,T)=\int \frac{e^{-\beta H(\mathbf{q},\mathbf{p})}}{h^{3N}N!} \ d^{3N}q\,d^{3N}p$$

### Partition function
Internal energy
$$U=-\frac{ \partial  }{ \partial \beta } \ln Z$$
Helmholtz free energy
$$Z=e^{-\beta A}\quad\Rightarrow \quad A=- \frac{1}{\beta} \ln Z$$
