---
wiki-publish: true
---
The **Lie derivative** is a derivative [[Operatore|operator]] defined on a [[dynamical variable]] $G:\mathbb{R}^{N}\mapsto \mathbb{R}$ and a [[vector field]] $f(\mathbf{x})$ as
$$\begin{align}
&\mathcal{L}_{f}G:\mathbb{R}^{N}\mapsto \mathbb{R} \\
&\mathbf{x}\mapsto \sum_{i=1}^{N} \frac{ \partial G }{ \partial x_{i} } (\mathbf{x})f_{i}(\mathbf{x})=\nabla G\cdot f=dG[f]
\end{align}$$
where $\nabla G$ is the [[gradient]] of $G$ and $dG[f]$ is the [[exact differential]] of $G$.

The importance of Lie derivatives comes from their ability to detect [[Constant of motion|constants of motion]], thanks to the following result:

> [!info] Lie derivatives and constants
> Let $G:\mathbb{R}^{N}\to \mathbb{R}$ be dynamical variable for some system of [[Ordinary differential equation|ODEs]] $\dot{\mathbf{x}}(t)=f(\mathbf{x}(t))$. $G$ is a constant of motion if and only if its Lie derivative is zero:
> $$G\text{ is a constant of motion}\quad\Leftrightarrow\quad \mathcal{L}_{f}G=0$$
> 
> **Proof.**
> - $(\Leftarrow)$ If the Lie derivative is zero, then $G$ is obviously a constant.
> - $(\Rightarrow)$ If $G$ is a constant, then let $\mathbf{x}_{0}\in \mathbb{R}^{N}$ be some point. Then, $\mathcal{L}_{f}G(\mathbf{x}_{0})=\mathcal{L}_{f}G(\mathbf{x}(t_{0}))=0$, which is true since $G$ is a constant of motion. This is true for any $\mathbf{x}_{0}\in \mathbb{R}^{N}$, so $\mathcal{L}_{f}G=0$ everywhere.

### Relation with homogeneous functions[^1]
Lie derivatives have some interesting connections to [[homogeneous function]] that, while not particularly useful in practice, help to make some connections between different areas of mathematics. Assume that our dynamical variable $G(\mathbf{x})$ is now homogeneous of degree $\alpha$. By Euler's theorem for homogeneous functions we can state
$$\alpha G(\mathbf{x})=\sum_{i=1}^{N} \frac{ \partial G }{ \partial x_{i} } x_{i}$$
You might notice a staggering similarity with the definition of the Lie derivative. In fact, the sum on the right hand side *is* a Lie derivative, but very specifically over the identity vector field $I(\mathbf{x})=\mathbf{x}$, which allows us to state the following:
$$\mathcal{L}_{I}G=\sum_{i=1}^{N} \frac{ \partial G }{ \partial x_{i} } I(x_{i})=\sum_{i=1}^{N} \frac{ \partial G }{ \partial x_{i} } x_{i}=\alpha G(\mathbf{x})$$
Evidently, if the dynamical variable is homogeneous, its Lie derivative with respect to the identity vector field is just an integer scaling of the function, specifically by the homogeneity degree. There are a few observations we can make from this. If $G$ is homogeneous of degree zero, then $\alpha=0$ and quite simply
$$\mathcal{L}_{I}G=0$$
But by the theorem above, this implies that $G$ is a constant of motion within the context of the [[dynamical system]] of dynamics defined by $\dot{\mathbf{x}}(t)=I(\mathbf{x}(t))=\mathbf{x}(t)$. But $G$ is somewhat generic; we can make the following proposition:

> [!info] Homogeneous constants of motion
> Let $G:\mathbb{R}^{N}\to \mathbb{R}$ be a dynamical variable that is homogeneous of degree zero. Let $G$ be subject to the dynamical system $\dot{\mathbf{x}}=\mathbf{x}$. Then, $G$ is a constant of motion.
> 
> **Proof.** The Lie derivative of $G$ in this system is
> $$\mathcal{L}_{I}G=\sum_{i=1}^{N} \frac{ \partial G }{ \partial x_{i} } I(x_{i})=\sum_{i=1}^{N} \frac{ \partial G }{ \partial x_{i} } x_{i}$$
> According to Euler's theorem for homogeneous functions
> $$\sum_{i=1}^{N} \frac{ \partial G }{ \partial x_{i} }x_{i} =\alpha G=0$$
> where $\alpha$ is the degree of homogeneity, which is $\alpha=0$ for $G$. Comparing the two we get
> $$\mathcal{L}_{I}G=0$$
> Using the theorem above, we conclude our proof.

We can see this in another light by solving the system $\dot{\mathbf{x}}=\mathbf{x}$ manually. This is a pretty trivial system that solves to $\mathbf{x}(t)=e^{t}\mathbf{x}_{0}$, for some starting condition $\mathbf{x}_{0}\in \mathbb{R}^{N}$. If we calculate $G$ over the motion as $G(\mathbf{x}(t))$, we can use degree zero homogeneity to see that $G(e^{t}\mathbf{x}_{0})=G(\mathbf{x}_{0})$, which is by definition a constant of motion over the trajectory imposed by the identity vector field. In fact, a degree zero homogeneous function essentially "ignores" scaling, and since the dynamics of the identity vector field are really just scaling by $e^{t}$, it's not surprising that $G$ does not change at all.

Another interesting fact is that the equation we derived for the Lie derivative
$$\mathcal{L}_{I}G=\alpha G$$
is actually an [[Equazione agli autovalori|eigenvalue equation]]. It's an equation for the Lie derivative operator in the identity vector field, where the homogeneity degree is the eigenvalue and the dynamical variable is the eigenfunction. As before, we can see how the dynamics of $I$ are scalings.

[^1]: This section is my own independent research. Take it with a grain of salt.
