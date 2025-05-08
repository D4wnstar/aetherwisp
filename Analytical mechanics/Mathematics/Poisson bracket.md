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
- $\{f,f\}=0$ (due to antisymmetry).
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
As a side note, the Hamiltonian itself is a constant if
$$\{ H,H \}+\frac{ \partial H }{ \partial t } =\frac{ \partial H }{ \partial t } =0$$
In other words, it's always constant unless it explicitly changes over time.
### Examples
> [!example] Point mass moving in 3D
> Consider some point in [[Cartesian coordinates]] $\mathbf{q}$, with $\mathbf{p}$ the momentum. The [[angular momentum]] is $\mathbf{L}=\mathbf{q}\times \mathbf{p}$, also written in terms of the [[Tensore di Levi-Civita]] as $L_{i}=\sum_{j,k=1}^{3}\varepsilon_{ijk}q_{j}p_{k}$. The Poisson brackets between linear and angular momentum are
> $$\begin{align}
> \{ p_{l},L_{i} \}&=-\frac{ \partial L_{i} }{ \partial q_{l} } =-\sum_{j,k=1}^{3}\varepsilon_{ijk}\delta_{jl}p_{k} \\
> &=\ldots \\
> &=-\sum_{k=1}^{3} \varepsilon_{ilk}p_{k} \\
> &=\sum_{k=1}^{3} \varepsilon_{lik}p_{k}
> \end{align} $$
> Between position and angular momentum they are essentially the same:
> $$\{ q_{l},L_{i} \}=\sum_{k=1}^{3} \varepsilon_{lik}q_{k}$$
> The Poisson brackets between components of the angular momentum are among the most relevant in physics (and later on, quantum mechanics):
> $$\begin{align}
> \{ L_{i},L_{j} \}&=\left\{  \sum_{m,s=1}^{3} \varepsilon_{ims}q_{m}p_{s}, L_{j}  \right\} \\
> \text{(bilinear)}&=\sum_{m,s=1}^{3} \varepsilon_{ims}\{ q_{m}p_{s},L_{j} \} \\
> \text{(commutative)}&=\sum_{m,s=1}^{3} \varepsilon_{ims}(q_{m}\{ p_{s},L_{j} \}+\{ q_{m},L_{j} \}p_{j}) \\
> &=\sum_{m,s=1}^{3} \varepsilon_{ims}\left( \sum_{r=1}^{3} q_{m}\varepsilon_{sjr}p_{r}+\sum_{r=1}^{3} \varepsilon_{mjr}q_{r}p_{s} \right) \\
> &=\sum_{m,r=1}^{3} q_{m}p_{r}\underbrace{ \sum_{s=1}^{3} \varepsilon_{ims}\varepsilon_{jrs} }_{ \delta_{ij}\delta_{mr}-\delta_{ir}\delta_{mj} }-\sum_{r,s=1}^{3} q_{r}p_{s}\underbrace{ \sum_{m=1}^{3} \varepsilon_{mis}\varepsilon_{mjr} }_{ \delta_{ij}\delta_{sr}-\delta_{ir}\delta_{sj} } \\
> &=-q_{j}q_{i}+q_{i}q_{j} \\
> &=???
> \end{align}$$
> (TODO: Fix this, 08/05/2025) So, the Poisson brackets on angular momentum component is
> $$\boxed{\{ L_{i},L_{j} \}=\sum_{k=1}^{3} \varepsilon_{ijk}L_{k}}$$
> Specializing to specific indexes, we see the following fundamental relations:
> $$\boxed{\{ L_{1},L_{2} \}=L_{3},\quad \{ L_{2},L_{3} \}=L_{1},\quad \{ L_{3},L_{1} \}=L_{2}}$$
> Another important set of brackets is between the square [[norm]] of the angular momentum and any of its components (for brevity, $\lvert \mathbf{L} \rvert^{2}\equiv L^{2}$):
> $$\begin{align}
> \{ L^{2},L_{i} \}&=\sum_{r=1}^{3} \{ L_{r}^{2},L_{i} \} \\
> \text{(commutative)}&=\sum_{r=1}^{3} (L_{r}\{ L_{r},_{Li} \}+\{ L_{r},L_{i} \}L_{r}) \\
> &=2\sum_{r=1}^{3} L_{r}\{ L_{r},L_{i} \} \\
> &=2\sum_{r=1}^{3} L_{r}\sum_{s=1}^{3} \varepsilon_{ris}L_{s} \\
> &=-2\sum_{r,s=1}^{3} \varepsilon_{irs}L_{r}L_{s} \\
> &=\ldots
> \end{align}$$
> We'll use a useful property of tensors. Consider two [[tensor|tensors]], an antisymmetric tensor $a_{lk}$ and a symmetric one $s_{lk}$. The *compression* of their sum is zero: $\sum_{n,m}a_{nm}s_{nm}=0$. This is because due to antisymmetry, as $\sum_{n,m}a_{nm}b_{nm}=-\sum_{nm}a_{mn}b_{mn}$ and the only number that is equal to its negative is zero. In our case, $\varepsilon_{irs}$ is antisymmetric, and the product $L_{r}L_{s}$ is a symmetric tensor. So, we can use this little trick to simply state:
> $$\boxed{\{ L^{2},L_{i} \}=0}$$
