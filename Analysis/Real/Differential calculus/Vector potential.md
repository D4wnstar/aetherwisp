---
hl-publish: true
---
A **vector potential** is a [[Vector field]] $\mathbf{A}:S\subseteq \mathbb{R}^{N}\to \mathbb{R}^{N}$ associated with another vector field $\mathbf{F}:S\subseteq \mathbb{R}^{N}\to \mathbb{R}^{N}$  such that its [[Curl]] is the vector field:
$$\nabla\times\mathbf{A}=\mathbf{F}$$
The vector potential is defined up to the gradient of a [[Scalar field]], which means that given any scalar field $S$, the function $\tilde{\mathbf{A}}=\mathbf{A}+\nabla S$ is itself the vector potential of the same field. This is because the curl of a [[Gradient]] is always zero:
$$\mathbf{F}=\nabla\times \tilde{\mathbf{A}}=\nabla \times(\mathbf{A}+\nabla S)=\nabla\times\mathbf{A}+\underbrace{ \nabla \times(\nabla S) }_{ 0 }=\nabla\times\mathbf{A}$$