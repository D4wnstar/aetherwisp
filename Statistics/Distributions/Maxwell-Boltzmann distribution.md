The **Maxwell-Boltzmann distribution** is a real, continuous [[probability distribution]]. For a [[random variable]] $X$, the [[probability density function]] is
$$f(x)=\sqrt{ \frac{2}{\pi} } \frac{x^{2}}{a^{3}} e^{-x^{2}/2a^{2}}$$
where $a>0\in \mathbb{R}$ is a parameter. It is commonly employed in physics to model the velocity distribution of [[Particella|particles]] in an [[ideal gas]].
### 3D monoatomic ideal gas
In a 3D monoatomic ideal gas, the distribution measures the speed of the particles $v^{2}=v_{x}^{2}+v_{y}^{2}+v_{z}^{2}$. In this case, $a=\sqrt{ k_{B}T/m }$ and the PDF is
$$f(v)=\sqrt{ \frac{2}{\pi} } \left( \frac{m}{k_{B}T} \right)^{3/2} v^{2}e^{- mv^{2}/2k_{B}T}$$
where $k_{B}$ is the [[Boltzmann constant]], $T$ is the [[temperature]] and $m$ is the [[mass]] of the particles.
### 2D monoatomic ideal gas
A similar distribution can be derived in a 2D gas as well:
$$f(v)=\frac{m}{k_{B}T} ve^{-mv^{2}/2k_{B}T}$$
### $N$-dimensional generalization
The distribution can be generalized to an arbitrary number of dimensions as
$$f(v)=A\left( \frac{m}{2\pi k_{B}T} \right)^{N/2}v^{N-1}e^{-m\lvert v \rvert ^{2}/2k_{B}T}$$
where $A$ is a [[Normalizzazione|normalization]] constant.
### Relation to other distributions
It is a specific case of the [[chi-square distribution]], with 3 degrees of freedom (representing the components of the velocity vector).