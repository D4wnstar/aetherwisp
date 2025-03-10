The **divergence theorem** states that the integral of the [[divergence]] of a three-dimensional [[vector field]] in a volume is equal to the integral of the field itself projected over the bounding [[surface]] of the volume. For a generic vector field $\mathbf{F}$ in a volume $V$ of bounding surface $S$, the theorem states:
$$\int_{V}\nabla\cdot\mathbf{F}=\oint_{S}\mathbf{F}\cdot d\mathbf{a}$$
where $d\mathbf{a}=\hat{\mathbf{n}}\ da$ is the area element projected with the normal unit vector $\hat{\mathbf{n}}$.
### Mathematical treatment
Let $F : U ⊂ \mathbb{R}^{3} → \mathbb{R}^{3}$ be a vector field. Let's consider a closed domain $D ⊂ U$ of boundary $∂^+D = \Sigma$, which is the support of a closed and oriented surface with an outward normal field $\hat{\nu}$.  Then
$$\iiint_{D}(\nabla\cdot F)(x,y,z)\ dxdydz=\iint_{\partial^+D}F\cdot\hat{\nu}\;dS$$
A similar, more general result holds in other dimensions too, where the integral goes from an $N$-dimensional integral to an $(N-1)$-dimensional integral. For instance, in the plane it goes from a surface to the bounding [[curve]]. In one-dimension, it becomes [[integrazione per parti|integration by parts]].

Despite the name, similar results also hold for the [[curl]]
$$\iiint_{D}(\nabla\times F)(x,y,z)dxdydz=-\iint_{\partial^+D}F\times\hat{\nu}\;dS$$
and the [[gradient]] of a [[scalar field]] $\phi:U\subset \mathbb{R}^{3}\rightarrow \mathbb{R}$
$$\iiint_{D}(\nabla\phi)(x,y,z)dxdydz=\iint_{\partial^+D}\phi\hat{\nu}\;dS$$
