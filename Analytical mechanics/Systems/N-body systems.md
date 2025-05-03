(TODO: Maybe move this in  [[Lagrange equation]])

An $N$-body system is a [[Physical system|system]] made up of $N$ components, considered to be [[point mass|point masses]] or similarly idealized objects. Assuming each body is in 3 dimensions (in total, $\mathbb{R}^{3N}$), and with $r$ (possibly zero) [[Constraint|constaints]], the system has $n=3N-r$ [[degrees of freedom]]. We are interested in known how the [[Generalized coordinates|configuration]] $Q$ of the system varies over time, from which we can get how the real coordinates vary in time. We start with only time (and boundary conditions), which resides in $\mathbb{R}^{+}$. From that we move to $Q$, and from that we move to $\mathbb{R}^{3N}$. The chain is as follows:
$$\mathbb{R}^{+}\xrightarrow{q(t)} Q\xrightarrow{\mathbf{w}(q,t)} \mathbb{R}^{3N}$$
where the function $q(t)$ finds configuration from time and the function $\mathbf{w}(q,t)$ finds real coordinates from configuration. If we compose the two, $\mathbf{w}(q,t)\circ q(t)=\mathbf{w}(q(t),t)\equiv \mathbf{w}(t)$, we can jump directly from the time domain $\mathbb{R}^{+}$ to the real coordinate domain $\mathbb{R}^{3N}$. In other words, we're looking for $n$ [[Ordinary differential equation|ODEs]] for the $n$ unknowns $q_{1}(t),\ldots,q_{n}(t)$.

We'll use the constraints to get there. Our constraints state
$$m_{i}\mathbf{a}_{i}-\mathbf{F}_{i}-\Phi_{i}=0$$
There are $N$ equations like this (each with three components), one for each dimension of the system. However, our system only has $n$ degrees of freedom, so we project these like so:
$$\sum_{i=1}^{N} (m_{i}\mathbf{a}_{i}-\mathbf{F}_{i}-\Phi_{i})\cdot \frac{ \partial \mathbf{r}_{i} }{ \partial q_{j} } =0$$
for $j=1,\ldots,n$, which simplifies our equation greatly *if* we claim that our constraints are ideal, for which
$$\Phi_{i}\cdot \frac{ \partial \mathbf{r}_{i} }{ \partial q_{j} } =0\quad\text{(ideal constraints)}$$
Similarly, the middle [[scalar product]] is a [[generalized force]]
$$\sum_{i=1}^{N} \mathbf{F}_{i}\cdot \frac{ \partial \mathbf{r}_{i} }{ \partial q_{j} } =Q_{j}$$
Meanwhile, the first product is
$$m_{i}\mathbf{a}_{i}\cdot \frac{ \partial \mathbf{r}_{i} }{ \partial q_{j} } =m_{i}\frac{d}{dt} \left( \frac{1}{2}\frac{ \partial  }{ \partial \dot{q}_{j} } \lvert \mathbf{v}_{i} \rvert ^{2} \right)- \frac{1}{2}m_{i}\frac{ \partial  }{ \partial q_{j} } \lvert \mathbf{v}_{i} \rvert ^{2}$$
Plugging this back into our sum yields
$$\begin{align}
\sum_{i=1}^{N} m_{i}\mathbf{a}_{i}\frac{ \partial \mathbf{r}_{i} }{ \partial q_{j} } &=\sum_{i=1}^{N} \frac{m}{2}\left( \frac{d}{dt} \frac{ \partial \lvert \mathbf{v}_{i} \rvert ^{2} }{ \partial \dot{q}_{j} } -\frac{ \partial \lvert \mathbf{v}_{i} \rvert ^{2} }{ \partial q_{j} }  \right) \\
&=\frac{d}{dt} \frac{ \partial }{ \partial \dot{q}_{j} } \underbrace{ \left( \frac{1}{2}\sum_{i=1}^{N} m_{i}\lvert \mathbf{v}_{i} \rvert ^{2} \right) }_{ T(q,\dot{q},t) }-\frac{ \partial  }{ \partial q_{j} } \underbrace{ \left( \frac{1}{2}\sum_{i=1}^{N} m_{i}\lvert \mathbf{v}_{i} \rvert ^{2} \right) }_{ T(q,\dot{q},t) }
\end{align}$$
where we find the [[kinetic energy]] $T$. Our functions $q_{j}(t)$ then satisfy the $n$ differential equations
$$\boxed{\frac{d}{dt} \frac{ \partial T }{ \partial \dot{q}_{j} }(q(t),\dot{q}(t),t)- \frac{ \partial T }{ \partial q_{j} } (q(t),\dot{q}(t),t)=Q_{j} }$$
Each of these equations is known as the **[[Lagrange equation]]**, or one form of it at least. The left hand side essentially describes motion. The right hand side is the projection of forces over the direction of motion. Solving this equation means finding $q(t)$ and thus the motion.
### Conservative systems
Say the forces applied onto the system are [[Vector field|conservative]]. In this case, they can be written in terms of a [[potential]]:
$$\mathbf{F}_{i}=-\nabla V\quad\Rightarrow \quad Q_{j}=-\frac{ \partial V }{ \partial q_{j} } (q,t)\quad\text{and}\quad\frac{ \partial V }{ \partial \dot{q}_{j} } =0$$
Knowing this, the generalized force becomes
$$\frac{d}{dt} \frac{ \partial V }{ \partial \dot{q}_{j} } -\frac{ \partial V }{ \partial q_{j} } =Q_{j}$$
We now define the function
$$L(q,\dot{q},t)\equiv T(q,\dot{q},t)-V(q,t)$$
as the difference between kinetic energy and potential. If we plug this definition of $Q_{j}$ into the Lagrange equation and combine the terms using $L$ we get
$$\boxed{\frac{d}{dt} \frac{ \partial L }{ \partial \dot{q}_{j} } (q(t),\dot{q}(t),t)-\frac{ \partial L }{ \partial q_{j} } (q(t),\dot{q}(t),t)=0}$$
This is another form of the Lagrange equation and arguably the more important one, since conservative systems are of great interest. The function $L$ is called the **[[Lagrangian]]**.