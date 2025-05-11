---
wiki-publish: true
---
The **Lie derivative** is a derivative [[Operatore|operatore]] defined on a [[Dynamical variable|dynamical variables]] $G:\mathbb{R}^{N}\to \mathbb{R}$ and a [[vector field]] $f(\mathbf{x})$ as
$$\begin{align}
&\mathcal{L}_{f}G:\mathbb{R}^{N}\to \mathbb{R} \\
&\mathbf{x}\to \sum_{i=1}^{N} \frac{ \partial G }{ \partial x_{i} } (\mathbf{x})f_{i}(\mathbf{x})=\nabla G\cdot f=dG[f]
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
