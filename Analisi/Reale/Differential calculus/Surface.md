---
wiki-publish: true
---
A **surface**, technically a **parametric surface**, is a continuous function that maps a two-dimensional space to a three-dimensional one: $\Phi : \Omega\subset \mathbb{R}^{2} → \mathbb{R}^{3}$, $\Phi(u,v)=(x(u,v),y(u,v),z(u,v))$, where $u$ and $v$ are called **parameters** of the surface. The image $\Sigma=\Phi(\Omega)$ is called the **support** of the surface.
### Properties
For brevity, we use the notation $\frac{ \partial \Phi }{ \partial u }=\partial_{u}\Phi$ and $\frac{ \partial \Phi }{ \partial v }=\partial_{v}\Phi$. Using $\Phi_{u}$ and $\Phi_{v}$ to denote the same derivatives is also common.
- A surface is said to be **regular** if it is of class $C^1$ and $(\partial_{u}\Phi\times \partial_{v}\Phi)(u,v)\neq(0,0,0),\;\forall(u,v)\in\Omega$ holds.
- Two regular surfaces $\Phi_1:\Omega_1\rightarrow\mathbb{R}^3$ and $\Phi_2:\Omega_2\rightarrow\mathbb{R}^3$ are said to be **equivalent** if they have the same support and there exists a $C^1$-[[diffeomorphism]] $\varphi:\Omega_1\rightarrow \Omega_2$ such that $\Phi_1=\Phi_2\circ\varphi$. The curves have the same orientation if the [[determinant]] of the [[Jacobian]] of $\varphi$ is positive: $\det J_\varphi(u,v)>0\;\forall (u,v)\in \Omega_1$.
- The **reflected set** is defined as the set $\tilde{\Omega}=\{(v,u)|(u,v)\in\Omega\}$. It defines the surface $\Psi:\tilde{\Omega}\subset \mathbb{R}^{2}\rightarrow \mathbb{R}^{3}$ as $\Psi(v,u)=\Phi(u,v)$, where we swapped the variables. The normal vectors are inverted in sign.

The normal vectors to the surface $\hat{n}_\Phi:\Omega\rightarrow \mathbb{R}^3$ are given by
$$\hat{n}_\Phi(u,v)= \frac{\partial_{u}\Phi\times\partial_{v}\Phi}{||\partial_{u}\Phi\times \partial_{v}\Phi||}$$