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
### Examples
> [!example] Constrained $N$-body system

The value of generalized forces is mostly found in many-body systems, as they "compress" the information about the bodies themselves inside of them, leaving the final calculation only explicitly dependent on the number of degrees of freedom per body, which is typically small (often 3 or 6). When such a system is subject to one or more [[Constraint|constraints]], we can attempt to simplify the solution by projecting the forces over the configuration space.

[[Newton's laws|Newton's second law]] for such a system states
$$m_{i}\mathbf{a}_{i}+\mathbf{F}_{i}-\Phi_{i}=0$$
These are $N$ equations. If we project these over the configuration space by taking the [[Scalar product|scalar products]] with the 
$$\sum_{i=1}^{N} (m_{i}\mathbf{a}_{i}+\mathbf{F}_{i}-\Phi_{i})\cdot \frac{ \partial \mathbf{r}_{i} }{ \partial q_{j} } =0,\quad j=1,\ldots,n$$
This leads to $n$ equations to solve instead of $N$. Specifically, $n$ [[Ordinary differential equation|ODEs]] for the $n$ unknowns $q_{1}(t),\ldots,q_{n}(t)$. Finding these unknowns is sufficient to fully determine motion.

We start from the acceleration. The acceleration of a body is the time [[Differential|total derivative]] of its velocity:
$$\mathbf{a}_{i}=\frac{d\mathbf{v}_{i}}{dt}$$
from which we can state
$$m \mathbf{a}_{i}\cdot \frac{ \partial \mathbf{r}_{i} }{ \partial q_{j} } =m \frac{d\mathbf{v}_{i}}{dt}\cdot \frac{ \partial \mathbf{r}_{i} }{ \partial q_{j} } =\ldots$$
The trick to move forward is to move the total time derivative from $\mathbf{v}_{i}$ to the whole scalar product. Of course, we can't just *do that*, it's not at all equal. What we can do, is move the derivative while subtracting the difference. That'll end up with an actual equality. With this in mind, we get
$$\ldots=m\frac{d}{dt} \left( \mathbf{v}_{i}\cdot \frac{ \partial \mathbf{r}_{i} }{ \partial q_{j} }  \right)-m\mathbf{v}_{i}\cdot\frac{d}{dt} \frac{ \partial \mathbf{r}_{i} }{ \partial q_{j} } \tag{1}$$
It's worth remembering that $\mathbf{r}_{i}\equiv \mathbf{r}_{i}(q(t),t)$, so its time derivative is given to us by the chain rule:
$$\frac{d}{dt} \frac{ \partial \mathbf{r}_{i} }{ \partial q_{j} } (q(t),t)=\sum_{k=1}^{N} \frac{ \partial ^{2}\mathbf{r}_{i} }{ \partial q_{j}\partial q_{k} } (q(t),t)\dot{q}_{k}(t)+\frac{ \partial ^{2}\mathbf{r}_{i} }{ \partial q_{j}\partial t } (q(t),t)=\ldots\tag{2}$$
Now, let's step off of this equation for a moment and let's consider this other, simpler expression:
$$\sum_{k=1}^{N} \frac{ \partial \mathbf{r}_{i} }{ \partial q_{k} }(q,t)\dot{q}_{k}+\frac{ \partial \mathbf{r}_{i} }{ \partial t }(q,t)  $$
This is some function of $q$. I promise you'll see why this matter in just a second. Since it's a function of $q$, we can take its partial derivative in $q_{j}$. Then we can evaluate it over the motion, $q=q(t)$ and $\dot{q}=\dot{q}(t)$:
$$\left[ \frac{ \partial  }{ \partial q_{j} } \sum_{k=1}^{N} \frac{ \partial \mathbf{r}_{i} }{ \partial q_{k} }(q,t)\dot{q}_{k}+\frac{ \partial \mathbf{r}_{i} }{ \partial t }(q,t)   \right]_{q=q(t),\dot{q}=\dot{q}(t)}$$
But this is just our total derivative from before. You might be wondering why this matters; the answer is that the "some function of $q$" that we "chose" is actually just $\mathbf{v}$. Really, just look at it, it's the total time derivative of $\mathbf{r}_{i}$. So what we have in the end is that $(2)$ is just a partial derivative of velocity *evaluated over the motion*:
$$\ldots=\frac{ \partial \mathbf{v} }{ \partial q_{j} } (q(t),\dot{q}(t),t)$$
If we go back to $(1)$ now we can write
$$m_{i}\mathbf{a}_{i}\cdot \frac{ \partial \mathbf{r}_{i} }{ \partial q_{j} } =m_{i}\frac{d}{dt} \left( \mathbf{v}_{i}\cdot \frac{ \partial \mathbf{r}_{i} }{ \partial q_{j} }  \right)-m_{i}\mathbf{v}_{i}\cdot \frac{ \partial \mathbf{v}_{i} }{ \partial q_{j} } =\ldots$$
If we now take the derivative of $\mathbf{v}_{i}$ with respect to $\dot{q}_{j}$ we get
$$\frac{ \partial \mathbf{v}_{i} }{ \partial \dot{q}_{j} }(q,\dot{q},t) =\frac{ \partial  }{ \partial \dot{q}_{j} } \left[ \sum_{k=1}^{N} \frac{ \partial \mathbf{r}_{i} }{ \partial q_{k} }(q,t)\dot{q}_{k}+\cancel{ \frac{ \partial \mathbf{r}_{i} }{ \partial t }(q,t) } \right]$$
The time derivative is independent of $\dot{q}_{j}$ so it vanishes. Meanwhile, the significant part of the other term is
$$\frac{ \partial \dot{q}_{k} }{ \partial \dot{q}_{j}}=\delta_{jk} $$
It's a [[Kronecker delta]], which leaves us with
$$\frac{ \partial \mathbf{v}_{i} }{ \partial \dot{q}_{j} } (q,\dot{q},t)=\frac{ \partial \mathbf{r}_{i} }{ \partial q_{j} } $$
As such, we can write
$$\ldots=m\frac{d}{dt} \left( \mathbf{v}_{i}\cdot \frac{ \partial \mathbf{v}_{i} }{ \partial \dot{q}_{j} }  \right)-m_{i}\mathbf{v}_{i}\cdot \frac{ \partial \mathbf{v}_{i} }{ \partial q_{j} } =\frac{1}{2}m_{i}\frac{d}{dt} \frac{ \partial \lvert \mathbf{v}_{i} \rvert ^{2} }{ \partial q_{j} } - \frac{1}{2}m_{i}\frac{ \partial \lvert \mathbf{v}_{i} \rvert ^{2} }{ \partial q_{j} } $$
This is *almost* the [[kinetic energy]].