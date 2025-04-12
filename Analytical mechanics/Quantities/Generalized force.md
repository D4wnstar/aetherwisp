The **generalized forces** $Q_{i}$ acting on a systems are coefficients that, when multiplied with [[virtual displacement|virtual displacements]] $\delta q_{i}$ over the axes of the [[configuration space]], give the [[virtual work]] of a [[Physical system|system]]:
$$\delta W=\sum_{i=1}^{n} Q_{i}\delta q_{i}$$
$n$ is the number of [[degrees of freedom]] of the system. If the system is made up of $N$ [[point mass|point masses]], each of which has a [[force]] $\mathbf{F}_{i}$ applied onto it, they are given by
$$Q_{j}=\sum_{i=1}^{N} \mathbf{F}_{i}\cdot \frac{ \partial \mathbf{r}_{i} }{ \partial q_{j} } $$
### Definition
We'll start by considering a system of $N$ point masses, each of which has a classical force $\mathbf{F}_{i}$ applied to it. The virtual work that these forces would do over virtual displacements $\delta \mathbf{r}_{i}$ is
$$\delta W=\sum_{i=1}^{N} \mathbf{F}_{i}\cdot \delta\mathbf{r}_{i}$$
If the position vectors $\mathbf{r}_{i}$ of the particles are functions of the [[generalized coordinates]] $q_{1},\ldots,q_{N}$, we express $\delta \mathbf{r}_{i}$ as a [[linear combination]] using the [[chain rule]]:
$$\delta W=\sum_{i=1}^{N} \mathbf{F}_{i}\cdot\left( \sum_{j=1}^{n} \frac{ \partial \mathbf{r}_{i} }{ \partial q_{j} } \delta q_{j} \right)=\sum_{j=1}^{n} \underbrace{ \left( \sum_{i=1}^{N} \mathbf{F}_{i}\cdot \frac{ \partial \mathbf{r}_{i} }{ \partial q_{j} }  \right) }_{ Q_{j} }\delta q_{j}=\sum_{j=1}^{n} Q_{j}\delta q_{j}$$
The quantity $Q_{j}$ is a coefficient that, when multiplied with a displacement, gives a work. It must, then, be some kind of force: we call these **generalized forces**.
### Conservative forces
If the forces $\mathbf{F}_{i}$ are [[Vector field|conservative]], and thus permit a [[potential]] $\tilde{V}(\mathbf{r}_{1},\ldots,\mathbf{r}_{N},t)$ such that $\mathbf{F}_{i}=-\nabla_{i}\tilde{V}$, we can derive $Q_{j}$ just from the $\tilde{V}$:
$$\begin{align}
Q_{j}&=\sum_{i=1}^{N} \mathbf{F}_{i}\cdot \frac{ \partial \mathbf{r}_{i} }{ \partial q_{j} }  \\
&=-\sum_{i=1}^{N} \nabla_{i}\tilde{V}\cdot \frac{ \partial \mathbf{r}_{i} }{ \partial q_{j} } \\
&=-\sum_{i=1}^{N} \left( \frac{ \partial \tilde{V} }{ \partial x_{i} } \frac{ \partial x_{i} }{ \partial q_{j} } +\frac{ \partial \tilde{V} }{ \partial y } \frac{ \partial y }{ \partial q_{j} } +\frac{ \partial \tilde{V} }{ \partial z } \frac{ \partial z }{ \partial q_{j} }  \right) \\
&=-\frac{ \partial }{ \partial q_{j} } \tilde{V}(\mathbf{r}_{1}(q,t),\ldots,\mathbf{r}_{N}(q,t),t)
\end{align}$$
where we used the fact that the sum was just the derivative of a composite function using the [[chain rule]]. In fact, if we call $V(q,t)\equiv \tilde{V}(\mathbf{r}_{1}(q,t),\ldots,\mathbf{r}_{N}(q,t),t)$ the composition of $\tilde{V}$ with all the $\mathbf{r}_{i}$, we can express the generalized force itself as the derivative of a potential
$$\boxed{Q_{j}=- \frac{ \partial V }{ \partial q_{j} } }$$
