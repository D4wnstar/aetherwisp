---
wiki-publish: true
---
The **divergence** $\nabla\cdot\mathbf{F}$ of a [[Differential|differentiable]] vector function $\mathbf{F}$ is a [[scalar field]] that represents the volume density of the outgoing [[flux]] of $\mathbf{F}$ from an infinitesimal volume around a given point. In simpler terms, it represents how $\mathbf{F}$ "emanates" from a point. Positive divergence means the function emanates outwards from a source, negative divergence means the function compresses inwards towards a sink.

It is linked to the flux by the [[Divergence theorem|divergence theorem]].

In [[Cartesian coordinates]], the divergence can be written as
$$\nabla\cdot\mathbf{F}=\left( \frac{ \partial  }{ \partial x } +\frac{ \partial  }{ \partial y } + \frac{ \partial  }{ \partial z }  \right)\cdot(F_{x},F_{y},F_{z})=\frac{ \partial F_{x} }{ \partial x } +\frac{ \partial F_{y} }{ \partial y } +\frac{ \partial F_{z} }{ \partial z }=\sum_{i=1}^{3} \frac{ \partial  F_{i} }{ \partial i }$$
where $i=x,y,z$ denotes the axis in the last expression.
### Useful results
Given a generic position vector $\mathbf{r}=r \hat{\mathbf{r}}$, the following useful results hold:
$$\nabla\cdot\mathbf{r}=3,\quad \nabla\cdot\left( \frac{\mathbf{r}}{r} \right)=\frac{2}{r},\quad \nabla\cdot\left( \frac{\mathbf{r}}{r^{2}} \right)=\frac{1}{r^{2}},\quad \nabla\cdot\left( \frac{\mathbf{r}}{r^{3}} \right)=4\pi \delta^{3}(\mathbf{r}),\quad \nabla\cdot\left( \frac{\mathbf{r}}{r^{4}} \right)=- \frac{1}{r^{4}}$$
where $\delta ^{3}(\mathbf{r})$ is the three-dimensional [[Delta di Dirac|Dirac delta]]. For proof of $\nabla\cdot(\mathbf{r}/r^{3})=4\pi \delta^{3}(\mathbf{r})$ see [[Electric field#Divergence of $ hat{r}/r {2}$]].
### In curvilinear coordinates
Say the function $\mathbf{F}$ has the generic form
$$\mathbf{F}=F_{u}\mathbf{\hat{u}}+F_{v}\mathbf{\hat{v}}+F_{w}\mathbf{\hat{w}}$$
We want to evaluate the flux
$$\oint_{S} \mathbf{F}\cdot d\mathbf{a}$$
where $S$ is the [[Surface|surface]] bounding an infinitesimal volume created by moving in each direction by an amount $(du,dv,dw)$ respectively. Since $(\hat{\mathbf{u}},\hat{\mathbf{v}},\mathbf{\hat{w}})$ is a [[Orthonormality|orthonormal]] [[base|basis]], the volume formed is a rectangular solid (in the infinitesimal limit), and the sides have lengths $(dl_{u},dl_{v},dl_{w})=(f\ du,g\ dv,h\ dw)$, with $f$, $g$ and $h$ some functions that depend on the coordinate system of choice (see [[Curvilinear coordinates functions]]). Since we are working with a rectangular solid, we can break the surface down into rectangular faces [[Incollamento|glued]] onto each other.

The "front" surface i
$$d\mathbf{a}=-(gh)\ dvdw\mathbf{\hat{u}}$$
so that
$$\mathbf{F}\cdot d\mathbf{a}=-(ghF_{u})\ dvdw$$
The "back" surface is identical, but with the sign flipped and evaluated on $u+du$ instead of $du$. For any differentiable function, we have
$$F(u+du)-F(u)=\frac{dF}{du}du$$
the front and back surface are in total
$$\left[ \frac{ \partial  }{ \partial u } (ghF_{u}) \right]\ dudvdw=\frac{1}{fgh}\frac{ \partial  }{ \partial u } (ghF_{u})\ d\tau$$
since $d\tau=dl_{u}dl_{v}dl_{w}$. The "left" and "right" surfaces, using the same logic, give
$$\frac{1}{fgh}\frac{ \partial  }{ \partial v } (fhF_{v})\ d\tau$$
and the "top" and "bottom" give
$$\frac{1}{fgh}\frac{ \partial  }{ \partial w } (fgF_{w})\ d\tau$$
Thus, the whole integral gives
$$\oint_{S}\mathbf{F}\cdot d\mathbf{a}=\frac{1}{fgh}\left[ \frac{ \partial  }{ \partial u } (ghF_{u})+\frac{ \partial  }{ \partial v } (fhF_{v})+\frac{ \partial  }{ \partial w } (fgF_{w}) \right]\ d\tau$$
The coefficient of $d\tau$ defines the divergence in curvilinear coordinates:
$$\nabla\cdot\mathbf{F}=\frac{1}{fgh}\left[ \frac{ \partial  }{ \partial u } (ghF_{u})+\frac{ \partial  }{ \partial v } (fhF_{v})+\frac{ \partial  }{ \partial w } (fgF_{w}) \right]$$
and therefore we get
$$\oint_{S}\mathbf{F}\cdot d\mathbf{a}=(\nabla\cdot\mathbf{F})\ d\tau$$
which is *almost* the [[Divergence theorem|divergence theorem]]. The key difference is that this has only been applied onto an infinitesimal volume, not an arbitrary one. But the extension is easy: any (finite) volume can be broken down into infinitesimals, but the issue that needs to be fixed is that simply summing all the contributions may not give the correct results. Of course, the divergence theorem integrates over the external bounding surface, whereas a simple sum integrates over the surfaces of all infinitesimal chunks, including internal ones. Fortunately, each internal surface occurs at the boundary of another adjacent surface (they are all back-to-back), and since $d\mathbf{a}$ always points outwards, the normal vector is mirrored for adjacent pairs, which means that they cancel out. This occurs everywhere surfaces touch, which is to say everywhere except on the outside where there are no more surfaces. Thus, the only surfaces that don't cancel are though outside, which when summed over produce the total bounding are of a volume. Thus, we can write
$$\oint_{S}\mathbf{F}\cdot d\mathbf{a}=\int_{V}(\nabla\cdot\mathbf{F})\ d\tau$$
which is the actual divergence theorem.