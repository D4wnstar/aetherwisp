---
wiki-publish: true
---
A **potential** is a [[scalar field]] $V:A\subseteq \mathbb{R}\to \mathbb{R}^{N}$ associated with a [[Vector field]] $\mathbf{F}:A\subseteq \mathbb{R}^{N}\to \mathbb{R}^{N}$ such that its [[gradient]] is the vector field with the sign changed:
$$\mathbf{F}=-\nabla V$$
The sign change is a convention and is designed to make equations nicer to work with, since many potentials are dependent on an inverse power of their argument (typically $\sim 1/r$, e.g. [[electric potential]]) which lead to a minus sign when derived. The additional minus in the definition cancel the other one out.

A potential is defined up to a constant, which means that given any constant $C$, the function $\tilde{V}=V+C$ is itself a potential of the same vector field. This is because the derivative of a constant is always zero:
$$\mathbf{F}=-\nabla \tilde{V}=-\nabla(V+C)=-\nabla V-\underbrace{ \nabla C }_{ 0 }=-\nabla V$$
