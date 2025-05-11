---
wiki-publish: true
aliases:
  - Stokes theorem
  - Gauss-Green theorem
---
The **curl theorem** or **Stokes-Kelvin theorem** states that the integral of the [[curl]] of a three-dimensional [[vector field]] in a [[surface]] is equal to the integral of the field itself projected over the bounding [[curve]] of the surface. For a generic vector field $\mathbf{F}$ on a surface $S$ of bounding curve $\gamma$, the theorem states:
$$\int_{S}(\nabla\times\mathbf{F})\cdot d\mathbf{a}=\oint_{\gamma}\mathbf{F}\cdot d\mathbf{s}$$
where $d\mathbf{a}=\hat{\mathbf{n}}\ da$ is the area element projected with the normal unit vector $\hat{\mathbf{n}}$ and $d\mathbf{s}=\hat{\boldsymbol{\tau}}\ ds$ is the line element projected with the tangent unit vector $\hat{\boldsymbol{\tau}}$.
### Mathematical treatment
Let $F : U ⊂ \mathbb{R}^{3} → \mathbb{R}^{3}$ be a vector field. Consider a regular surface $\Sigma\subset U$ oriented with a field of normal unit vectors $ν̂$. We orient its boundary $∂^+\Sigma$ positively and assume that it is the support of a closed (piecewise) regular curve. Then
$$\iint_{\Sigma}(\nabla\times F)\cdot\hat{\nu}\;dS=\oint_{\partial^+\Sigma}F\times\hat{\tau}\;ds$$

In the two-dimensional case, it is called **Gauss-Green theorem** and states: given a vector field $F = (F_{1} , F_{2}) : U ⊆ \mathbb{R}^{2} → \mathbb{R}^{2}$ and a closed domain $D ⊂ U$, then the following holds:
$$\iint_{D}\left(\frac{\partial F_2}{\partial x}- \frac{\partial F_{1}}{\partial y}\right)\ dxdy=\oint_{\partial^+D}F\times\hat{\tau}\;ds=\oint_{\partial^{+}D}(F_{2}dx+F_{1}dy)$$
