The **auxiliary field** $\mathbf{H}$ is a [[Campo vettoriale|vector field]] that combines the effect of both free [[Electric current|currents]] added externally and bound currents induced by [[magnetization]]. It is
$$\mathbf{H}=\frac{1}{\mu_{0}}\mathbf{B}-\mathbf{M}\qquad\left[ \frac{\text{A}}{\text{m}^{2}} \right]$$
where $\mathbf{B}$ is the [[magnetic field]] due to free currents and $\mathbf{M}$ is the magnetization.
### Derivation
Consider any magnetized object upon which is set a free current $\mathbf{J}_{f}$. The total current then is the sum of the free one and the bound one $\mathbf{J}_{b}$:
$$\mathbf{J}=\mathbf{J}_{b}+\mathbf{J}_{f}$$
From [[Ampere's law]] we get
$$\frac{1}{\mu_{0}}(\nabla\times\mathbf{B})=\mathbf{J}=\mathbf{J}_{b}+\mathbf{J}_{f}=\mathbf{J}_{f}+(\nabla\times\mathbf{M})$$
if we collect the [[Curl|curls]] we get
$$\nabla \times\left( \frac{1}{\mu_{0}}\mathbf{B}-\mathbf{M} \right)=\mathbf{J}_{f}$$
The quantity in parenthesis is defined as the auxiliary field $\mathbf{H}$.
### Boundary conditions
The auxiliary field inherits $\mathbf{B}$'s discontinuities over a surface current density. We know from the definition that the [[Divergence]] of $\mathbf{H}$ is $\nabla\cdot\mathbf{H}=-\nabla\cdot\mathbf{M}$, so
$$H_\text{above}^{\perp}-H_\text{below}^{\perp}=-(M_\text{above}^{\perp}-M_\text{below}^{\perp})$$
whereas from the curl of $\mathbf{H}$ derived from [[Ampere's law]], $\nabla\times\mathbf{H}=\mathbf{J}_{f}$, we get
$$\mathbf{H}^{\parallel}_\text{above}-\mathbf{H}^{\parallel}_\text{below}=\mathbf{K}_{f}\times \hat{\mathbf{n}}$$
which may be more useful than the boundary conditions on $\mathbf{B}$ when dealing with magnetized materials.