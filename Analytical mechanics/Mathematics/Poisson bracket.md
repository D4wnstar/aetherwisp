The **Poisson brackets** map a pair of functions in [[phase space]] to another function in phase space:
$$f(q,p,t),\ g(q,p,t)\quad\to \quad \{ f,g \}(q,p,t)=\sum_{i=1}^{n} \left( \frac{ \partial f }{ \partial q_{i} } \frac{ \partial g }{ \partial p_{i} } - \frac{ \partial f }{ \partial p_{i} } \frac{ \partial g }{ \partial q_{i} }  \right)$$
They can be written in a more compact form as follows:
$$\{ f,g \}(\mathbf{x},t)=\sum_{i,j=1}^{2n} \frac{ \partial f }{ \partial x_{i} } E_{ij}\frac{ \partial g }{ \partial x_{j} } =\nabla_{x}f\cdot \mathrm{E}\nabla_{x}g$$
where $\mathbf{x}=(\mathbf{q},\mathbf{p})=(q_{1},\ldots,q_{n},p_{1},\ldots,p_{n})$ and $\mathrm{E}$ is the [[block matrix]]
$$\mathrm{E}=\begin{pmatrix}
0 & -\mathrm{I}_{n} \\
\mathrm{I}_{n} & 0
\end{pmatrix}$$
using the $n$-dimensional [[identity matrix]] $\mathrm{I}$.
### Properties
- The brackets are **bilinear**: $\{ f,\alpha g+\beta h \}=\alpha \{ f,g \}+\beta \{ f,h \}$.
- They are **antisymmetric**: $\{ f,g \}=-\{ g,f \}$.
- They obey the **Jacobi identity**: $\{ f,\{ g,h \} \}+\{ g, \{ h,f \} \}+\{ h, \{ f,g \} \}=0$
- $\{ f,g\cdot h \}=g\{ f,h \}+\{ f,g \}h$.
- $\{f,f\}=0$.
- $\{f(x),x\}=0$.

The first three are the most important, as a [[vector space]] equipped with an operation that satisfies them is a [[Lie algebra]].
### Fundamental Poisson brackets
Some instances of Poisson brackets are particularly important, specifically the brackets on the [[generalized coordinates]] and momenta of the phase space:
$$\{ q_{i},q_{j} \}=\sum_{k=1}^{n} \frac{ \partial q_{i} }{ \partial q_{k} } \underbrace{ \frac{ \partial q_{j} }{ \partial p_{k} } }_{ 0 } - \underbrace{ \frac{ \partial q_{i} }{ \partial p_{k} } }_{ 0 } \frac{ \partial q_{j} }{ \partial q_{k} }=0$$
$$\{ p_{i},p_{j} \}=\sum_{k=1}^{n} \underbrace{ \frac{ \partial p_{i} }{ \partial q_{k} } }_{ 0 } \frac{ \partial p_{j} }{ \partial p_{k} } - \frac{ \partial p_{i} }{ \partial p_{k} } \underbrace{ \frac{ \partial p_{j} }{ \partial q_{k} } }_{ 0 }=0 $$
$$\{ q_{i},p_{j} \}=\sum_{k=1}^{n} \left( \underbrace{ \frac{ \partial q_{i} }{ \partial q_{k} } }_{ \delta_{ik} } \underbrace{ \frac{ \partial p_{j} }{ \partial p_{k} } }_{ \delta_{jk} } - \cancel{ \frac{ \partial q_{i} }{ \partial p_{k} } \frac{ \partial p_{j} }{ \partial q_{k} } }  \right)=\sum_{k=1}^{n} \delta_{ik}\delta_{jk}=\delta_{ij}$$
Also using compact formalism:
$$\{ x_{i},x_{j} \}=\sum_{k,l=1}^{2n} \underbrace{ \frac{ \partial x_{i} }{ \partial x_{k} } }_{ \delta_{ik} } \mathrm{E}_{kl}\underbrace{ \frac{ \partial x_{j} }{ \partial x_{l} } }_{ \delta_{jl} } =\sum_{k,l=1}^{2n} \delta_{ik}\delta_{jl}\mathrm{E}_{kl}=\mathrm{E}_{ij}$$
$$\{ x_{i},g \}(\mathbf{x},t)=\sum_{j,k=1}^{2n} \underbrace{ \frac{ \partial x_{i} }{ \partial x_{j} } }_{ \delta_{ij} } \mathrm{E}_{jk}\frac{ \partial g }{ \partial x_{k} } =\sum_{k=1}^{2n} \mathrm{E}_{ik}\frac{ \partial g }{ \partial x_{k} } $$
$$\{ \mathbf{x},g \}=\mathrm{E}\nabla_{x}g$$
The last case is notable, as we know that the [[Hamilton equation]] can be written as $\dot{\mathbf{x}}=\mathrm{E}\nabla_{x}H$, for some [[Hamiltonian]] $H$. Because of this, we can rewrite the Hamilton equation as a Poisson bracket as
$$\boxed{\dot{\mathbf{x}}=\{ \mathbf{x},H \}}$$
### Regarding constants of motion
Poisson brackets have some interesting behavior with respect to [[Constant of motion|constants of motion]]. Say now $f(q,p,t)$ is a constant of motion over the motion $q(t)$ and $p(t)$, so
$$\frac{d}{dt} f(q(t),p(t),t)=0$$
for $q(t)$ and $p(t)$ that describe motion (i.e. they solve the Hamilton equations of the system). If we calculate the [[Differential|total derivative]] explicitly and apply the Hamilton equations $\dot{p}_{i}=-\frac{ \partial H }{ \partial q_{i} }$ and $\dot{q}_{i}=\frac{ \partial H }{ \partial p_{i} }$, we get
$$\begin{align}
\frac{d}{dt} f(q(t),p(t),t)&=\sum_{i=1}^{n} \left( \frac{ \partial f }{ \partial p_{i} } \dot{p}_{i}+ \frac{ \partial f }{ \partial q_{i} } \dot{q}_{i} \right)+\frac{ \partial f }{ \partial t }  \\
&=\sum_{i=1}^{n} \left( -\frac{ \partial f }{ \partial p_{i} } \frac{ \partial H }{ \partial q_{i} } +\frac{ \partial f }{ \partial q_{i} } \frac{ \partial H }{ \partial p_{i} }  \right)+\frac{ \partial f }{ \partial t }  \\
&=\{ f,H \}(q(t),p(t),t)+\frac{ \partial f }{ \partial t } 
\end{align}$$
This lets us say that $f$ is a constant of motion if and only if
$$\{ f,H \}+\frac{ \partial f }{ \partial t } =0$$
In the special (but common) case where $f$ does not explicitly depend on $t$, we get
$$\boxed{f\text{ is a constant of motion}\quad\Leftrightarrow\quad \{ f,H \}=0}$$
