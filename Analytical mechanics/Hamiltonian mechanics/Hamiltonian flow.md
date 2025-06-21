---
wiki-publish: true
---
The **Hamiltonian flow** is the [[flow]] of the [[Hamiltonian]] [[vector field]] $\mathrm{E}\nabla_{\mathbf{x}}H(\mathbf{x},t)$.

The [[Hamilton equations]] can be written in compact form as
$$\dot{\mathbf{x}}=\mathrm{E}\nabla_{\mathbf{x}}H(\mathbf{x},t)$$
which is a first order [[ordinary differential equation]]. As with other differential equations, we can look for the flow. We'll denote it $\Phi^{t}:T^{*}Q\mapsto T^{*}Q$ and its application is $\mathbf{x}_{0}\mapsto \Phi^{t}(\mathbf{x}_{0})\equiv \mathbf{x}(t;\mathbf{x}_{0})$. As usual, this isn't a single map, but rather a family of maps parameterized by $t$. We call this the Hamiltonian flow.
### As a canonical transformation
Given $n$ [[degrees of freedom]], the Hamiltonian flow is an invertible function with domains $\mathbb{R}^{2n}\to \mathbb{R}^{2n}$. This qualifies it as a [[coordinate transformation]], so we can use $\Phi^{t}$ to change coordinates. We'll define the transformation as $\mathbf{x}\equiv \mathbf{w}(\tilde{\mathbf{x}},t)=\Phi^{t}(\tilde{\mathbf{x}})$, and it isn't just a generic transformation.

> [!info] Proposition
> The Hamiltonian flow is a [[Canonical transformation|univalent canonical transformation]].

> [!quote]- Proof
> To prove this, we'll use the first canonicity criterion. Specifically, we will prove that the [[Jacobian]] of the flow is [[Symplectic matrix|symplectic]]. The Jacobian is
> $$J_{ij}=\frac{ \partial \Phi_{i}^{t} }{ \partial \tilde{x}_{j} }=\frac{ \partial w_{i} }{ \partial \tilde{x}_{j} }$$
> The symplectic condition is $J^{T}\mathrm{E}J=\mathrm{E}$ for all $t$. Starting from $t=0$,
> $$w_{i}(\tilde{\mathbf{x}},0)=\Phi_{i}^{0}(\tilde{\mathbf{x}})=\tilde{x}_{i}\quad\Rightarrow \quad J_{ij}=\frac{ \partial w_{i} }{ \partial \tilde{x}_{j} } =\frac{ \partial \tilde{x}_{i} }{ \partial \tilde{x}_{j} } =\delta_{ij}$$
> But remember that the [[Kronecker delta]] defines the components of the [[identity matrix]] $\mathrm{I}$, so $J=\mathrm{I}$ for $t=0$, and $\mathrm{I}$ is symplectic since $\mathrm{I}\mathrm{E}\mathrm{I}=\mathrm{E}$.
> 
> We now want to extend this to any $t$. We'll do so by proving that $J_{t}^{T}\mathrm{E}J_{t}$ does not actually depend on $t$. To do so, we'll check if the time derivative is zero:
> $$\frac{ \partial  }{ \partial t } J_{t}^{T}\mathrm{E}J_{t}=0\quad(?)$$
> If this is true, then $J_{t}$ is always equal to $J_{0}$, which we already proved is symplectic. As such, the Jacobian would be symplectic for all $t$ and that would prove our point.
>  
> The derivative of the $ih$ element is
> $$\begin{align}
> \frac{ \partial  }{ \partial t } (J^{T}\mathrm{E}J)_{ih}&=\frac{ \partial  }{ \partial t } \left( \sum_{j,k}J_{ij}^{T}\mathrm{E}_{jk}J_{kh} \right) \\
> &=\frac{ \partial  }{ \partial t } \left( \sum_{j,k}J_{ji}\mathrm{E}_{jk}J_{kh} \right) \\
> &=\frac{ \partial  }{ \partial t } \left( \sum_{j,k}\frac{ \partial \Phi_{j}^{t} }{ \partial \tilde{x}_{i} } \mathrm{E}_{jk}\frac{ \partial \Phi_{k}^{t} }{ \partial \tilde{x}_{h} }  \right) \\
> &=\sum_{j,k}\left[ \frac{ \partial  }{ \partial \tilde{x}_{i} } \left( \frac{ \partial \Phi^{t}_{j}(\tilde{\mathbf{x}}) }{ \partial t }  \right)\mathrm{E}_{jk}\frac{ \partial \Phi_{k}^{t} }{ \partial \tilde{x}_{h} } +\frac{ \partial \Phi_{j}^{t} }{ \partial \tilde{x}_{i} } \mathrm{E}_{jk}\frac{ \partial  }{ \partial \tilde{x}_{h} } \left( \frac{ \partial \Phi^{t}(\tilde{\mathbf{x}}) }{ \partial t }  \right) \right]=\ldots
> \end{align}$$
> Now, we need the time derivative of $\Phi^{t}$. Recall that $\Phi^{t}\equiv \mathbf{w}$, so
> $$\frac{ \partial  }{ \partial t } \mathbf{w}(\tilde{\mathbf{x}},t)=\frac{ \partial \Phi^{t} }{ \partial t } (\mathbf{x}_{0})=\frac{ \partial }{ \partial t } \mathbf{x}(t;\mathbf{x}_{0})=\dot{\mathbf{x}}(t)=\mathrm{E}\nabla_{\mathbf{x}}H(\mathbf{x}(t),t)$$
> The last step is allowed because this is not a generic $\dot{\mathbf{x}}$, but rather specifically the one that solves motion, $\dot{\mathbf{x}}(t)$, which means it is equal to the compact-form Hamilton equations. Moving on, we'll develop the first term in the square brackets above by writing the matrix multiplication between $\mathrm{E}$ and $\nabla_{\mathbf{x}}H(\mathbf{x}(t),t)$ element by element for $\Phi_{j}^{t}$:
> $$\begin{align}
> \sum_{j,k}\frac{ \partial  }{ \partial \tilde{x}_{i} } \left( \sum_{l}E_{jl}\frac{ \partial H }{ \partial x_{l} }  \right)E_{jk}\frac{ \partial \Phi_{k}^{t} }{ \partial \tilde{x}_{h} } = \sum_{j,k,l}\underbrace{ \mathrm{E}_{jl} }_{ -\mathrm{E}_{lj} }\underbrace{ \frac{ \partial }{ \partial \tilde{x}_{i} } \left( \frac{ \partial H }{ \partial x_{l} }  \right) }_{ (*) }\mathrm{E}_{jk}\underbrace{ \frac{ \partial \Phi_{k}^{t} }{ \partial \tilde{x}_{h} } }_{ J_{kh} }
> \end{align}$$
> Remember that $H\equiv H(\mathbf{x}(t),t)\equiv H(\mathbf{w}(\tilde{\mathbf{x}},t),t)\equiv H(\Phi^{t}(\tilde{\mathbf{x}},t),t)$, so by the chain rule
> $$(*)\equiv\sum_{a}\frac{ \partial ^{2}H }{ \partial \tilde{x}_{i}\partial x_{l}}\frac{ \partial \Phi_{a}^{t} }{ \partial x_{a} }=\sum_{a}\frac{ \partial ^{2}H }{ \partial x_{l}\partial x_{a}}\frac{ \partial \Phi_{a}^{t} }{ \partial \tilde{x}_{i} } =\sum_{a}\frac{ \partial ^{2}H }{ \partial x_{a}\partial x_{l}}J_{ai}=\sum_{a}\frac{ \partial ^{2}H }{ \partial x_{a}\partial x_{l}}J_{ia}^{T} $$
> The other half is the same, but with different indexes ($j\to m$ and $a\to b$), so with some rearrangement
> $$\begin{align}
> \ldots&=-\sum_{j,k,l,a}J_{ia}^{T}(\partial^{2}H)_{al}\mathrm{E}_{jl}\mathrm{E}_{jk}J_{kh}+\sum_{j,k,m,b}J_{ij}^{T}\mathrm{E}_{jk}\mathrm{E}_{km}(\partial ^{2}H)_{mb}J_{bh} \\
> &=-J^{T}(\partial ^{2}H)\mathrm{E}^{2}J+J^{T}\mathrm{E}^{2}(\partial ^{2}H)J \\
> &=-J^{T}(\partial ^{2}H)J+J^{T}(\partial ^{2}H)J \\
> &=0
> \end{align}$$
> This completes our proof.

The Hamiltonian flow defines a set of coordinates that we can use to describe motion. But what even are these coordinates? Let's look at them for a moment: $\mathbf{x}$ and $\tilde{\mathbf{x}}$ are points in [[phase space]]. We have $\mathbf{x}=\Phi^{t}(\tilde{\mathbf{x}})$. Then $\mathbf{x}$ must be the time evolution of $\tilde{\mathbf{x}}$ at time $t$. We can hence interpret the $\Phi^{t}$ in two ways:
1. In the active way, it is the time evolution of $\tilde{\mathbf{x}}$.
2. In the passive way, it is the backwards time evolution of the axes.

Moreover, it's fair to ask what the conjugate Hamiltonian is here. Using the canonicity lemma
$$\begin{align}
\mathrm{E}\nabla_{\tilde{\mathbf{x}}}K&=\tilde{J}\mathrm{E}\nabla_{\mathbf{x}}H+\frac{ \partial \tilde{w} }{ \partial t }  \\
&=\tilde{J}\mathrm{E}\nabla_{\mathbf{x}}H-\tilde{J}\frac{ \partial w }{ \partial t }  \\
&=\tilde{J}\mathrm{E}\nabla_{\mathbf{x}}H-\tilde{J}\mathrm{E}\nabla_{x}H \\
&=0
\end{align}$$
This implies $\nabla_{\tilde{\mathbf{x}}}K=0$ and so $K$ is constant. But a constant doesn't matter since motion is exclusively determined by the gradient of the Hamiltonian, so we might as well say $K=0$. Thus, the effect of the Hamiltonian flux is to conjugate the starting Hamiltonian $H$ into $0$.