---
wiki-publish: true
aliases:
  - conservative field
  - conservative force
  - irrotational
  - solenoidal
---
A **vector field** is a function $\mathbf{F} : S \subseteq \mathbb{R}^N → \mathbb{R}^N$ defined in a [[vector space]] $S$ that assigns a vector to each point in space.
### Properties
Vector fields find many applications in vector calculus through their derivatives. Being multivariate functions, vector fields admit three kinds of derivatives: the [[gradient]], the [[divergence]] and the [[curl]]. If the curl is zero, the field is said to be **irrotational**. If the divergence is zero, the field is said to be **solenoidal**.

A vector field is said to be **conservative** if it admits a [[potential]] $V$ that states that $\mathbf{F}=-\nabla V$. If $\mathbf{F}$ is continuous, [[Differential|differentiable]] and conservative then it is also irrotational. The converse also applies: if a field is irrotational, then it admits a potential.

Alternatively, it can admit a [[vector potential]] $\mathbf{A}$ such that $\mathbf{F}=\nabla\times \mathbf{A}$. If $\mathbf{F}$ is continuous, differentiable and admits a vector potential then it is also solenoidal. The converse also applies: if a field is solenoidal, then it admits a vector potential.