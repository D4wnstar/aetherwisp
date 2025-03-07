**Mirtich's algorithm** is a mathematical method to calculate the mass and [[Moment of inertia|inertia tensor]] for a solid polyhedron of constant mass density. It uses the [[Teorema della divergenza|divergence theorem]] to reduce a volume integrals into a [[Superficie|surface]] integrals and then again [[Teorema del rotore|Green's theorem]] to reduce the surface integrals into [[Curva|line]] integrals. Some important things to note are:
1. The polyhedron is composed of flat faces, which means that the surface integrals are just two-dimensional integrals on a plane. The same can be said for the line integrals at the edges of the faces.
2. Consequently, the faces can and should be projected onto a plane in order to avoid numerical problems.
3. The reduction to line integrals returns known integrals, which can be manually calculated for a considerable improvement in speed.

Point 2. is necessary to give precise number to point 3., and point 3. is necessary in order to handle polyhedra with arbitrary face polygons, such as squares or hexagons. In case the face polygons are triangles (which is always the case for computer meshes), then points 2. and 3. are redundant and the algorithm can be greatly simplified.
### Algorithm
#### Reduction of volume integrals
Calculation of the mass, [[Center of mass]] and [[Moment of inertia|inertia tensor]] all require a volume integral of the form
$$\int_{V}P(x,y,z)\ dV$$
where $V$ is the volume of the polyhedron and $P$ is a polynomial among: 1, $x$, $y$, $z$, $x^{2}$, $y^{2}$, $z^{2}$, $xy$, $xz$ and $yz$. This integral may be converted to a [[Integrale su una superficie|surface integral]] by use of the divergence theorem:
$$\int_{V}P(x,y,z)\ dV=\int_{V}\nabla\cdot\vec{F}\ dV=\int_{S}\vec{N}\cdot\vec{F}\ dS$$
where $S$ the boundary [[Superficie|surface]] of the polyhedron, a union of triangular surfaces and $\vec{F}:\mathbb{R}^{3} \rightarrow\mathbb{R}^{3}$ is chosen so that $\vec{N}\cdot\vec{F}=P$. $\vec{N}$ is outgoing normal vector from the surface. There is only one possible choice for $\vec{F}$ for any one polynomial. The full list is:

| $P$   | $\vec{F}$      |
| ----- | -------------- |
| 1     | $(x,0,0)$      |
| $x$   | $(x^2/2,0,0)$  |
| $y$   | $(0,y^2/2,0)$  |
| $z$   | $(0,0,z^2/2)$  |
| $x^2$ | $(x^3/3,0,0)$  |
| $y^2$ | $(0,y^3/3,0)$  |
| $z^2$ | $(0,0,z^3/3)$  |
| $xy$  | $(x^2y/2,0,0)$ |
| $xz$  | $(0,0,z^2x/2)$ |
| $yz$  | $(0,y^2z/2,0)$ |

Let's call the generic polyhedron face $\mathcal{F}$. Then, $S=\bigcup\mathcal{F}$. We can therefore express the surface integral as a sum of integral over the faces:
$$\int_{S}\vec{N}\cdot\vec{F}\ dS=\sum\limits_{\mathcal{F}\in S}\int_{\mathcal{F}}\vec{N}_{\mathcal{F}}\cdot\vec{F}\ dS$$
where $\vec{N}_{\mathcal{F}}=(\hat{\eta}_{x},\hat{\eta}_{y},\hat{\eta}_{z})$ is the normal vector over the face $\mathcal{F}$.
The integrals to be computed are now reduced to
$$\begin{align*}
\int_{V}dV=\sum\limits_{\mathcal{F}\in S}\hat{\eta}_{x}
\int_{\mathcal{F}}x\ dS \quad\quad &\int_{V}y^{2}\,dV=\frac{1}{3}\sum\limits_{\mathcal{F}\in S}\hat{\eta}_{y}
\int_{\mathcal{F}}y^{3}\,dS \\
\int_{V}x\,dV=\frac{1}{2}\sum\limits_{\mathcal{F}\in S}\hat{\eta}_{x}
\int_{\mathcal{F}}x^{2}\,dS \quad\quad & \int_{V}z^{2}\,dV=\frac{1}{3}\sum\limits_{\mathcal{F}\in S}\hat{\eta}_{z}\int_{\mathcal{F}}z^{3}\,dS \\
\int_{V}y\,dV=\frac{1}{2}\sum\limits_{\mathcal{F}\in S}\hat{\eta}_{y}\int_{\mathcal{F}}y^{2}\,dS \quad\quad &  \int_{V}xy\,dV=\frac{1}{2}\sum\limits_{\mathcal{F}\in S}\hat{\eta}_{x}\int_{\mathcal{F}} x^{2}y\,dS \\
\int_{V}z\,d V={\frac{1}{2}}\sum\limits_{\mathcal{F}\in S}{\hat{\eta}}_{z}\int_{\mathcal{F}}z^{2}\,d S \qquad & \int_{V}y z\,d V={\frac{1}{2}}\sum\limits_{\mathcal{F}\in S}{\hat{\eta}}_{y}\int_{\mathcal{F}}y^{2}z\,d S \\ \int_{V}x^{2}\,d V={\frac{1}{3}}\sum\limits_{\mathcal{F}\in S}{\hat{\eta}}_{x}\int_{\mathcal{F}}x^{3}\,d S \qquad  & \int_{V}x z\,d V={\frac{1}{2}}\sum\limits_{\mathcal{F}\in S}{\hat{\eta}}_{z}\int_{\mathcal{F}}z^{2}x\,d S
\end{align*}$$
which means something of the form
$$\hat{\eta}_{i}\int_{\mathcal{F}}Q(x,y,z)\ dS\tag{1}$$
where $i$ is any of $x$, $y$ or $z$ and $Q$ is a polynomial among $x$, $x^{2}$, $y^{2}$, $z^{2}$, $x^{3}$, $y^{3}$, $z^{3}$, $x^{2}y$, $y^{2}z$ or $z^{2}y$.
#### Reduction of surface integrals
The integrals can be further simplified by transforming them into a [[Integrale su una curva|line integral]]. For an example, consider the simplest possible case $Q=1$. Here, $\int_{\mathcal{F}}dS$ is just the [[misura|measure]] of the face, that is, its area. The surface is in 3D space, so we must compute it as a 3D quantity:
$$A=\int_{\mathcal{F}}dS=\frac{1}{2}\vec{N}_{\mathcal{F}}\cdot\sum\limits_{i=0}^{N-1}\vec{P}_{i}\times\vec{P}_{i+1}$$
where $N$ is the number of vertices of the face and $\vec{P}_{i}=(x_{i},y_{i},z_{i})$ are their coordinates. The vertices are ordered counterclockwise relative to the normal vector. This form is derive from [[Teorema del rotore|Stokes' theorem]]. Unfortunately, this is not a very efficient way of doing the calculations.

A more efficient way is to project the polygon onto a coordinate plane, compute the area in two dimensions and adjust the result based on the projection. The plane the polygon face sits on is $\hat{\eta}_{x}+\hat{\eta}_{y}+\hat{\eta}_{z}+w=0$, where $w=-\vec{N}_{\mathcal{F}}\cdot\vec{P_{0}}$. As long as $\hat{\eta}_{z}\neq0$, we may just project on the $xy$-plane, which in this case is defined by
$$z=f(x,y)=-(w+\hat{\eta}_{x}x+\hat{\eta}_{y}y)/\hat{\eta}_{z}$$
The surface element $dS$ can be expressed as
$$\begin{align*}
dS&=\left|\frac{\partial f}{\partial x}\times\frac{\partial f}{\partial y}\right|dxdy\\
&=\sqrt{1+\left(\frac{\partial f}{\partial x}\right)^{2}+\left(\frac{\partial f}{\partial y}\right)^{2}}dxdy\\
&=\sqrt{1+\left(\frac{-\hat{\eta}_{x}}{\hat{\eta}_{z}}\right)^{2}+\left(\frac{-\hat{\eta}_{y}}{\hat{\eta}_{z}}\right)^{2}}dxdy\\
&=\frac{1}{|\hat{\eta}_{z}|}dxdy
\end{align*}$$
since $|\vec{N}_{\mathcal{F}}|=1$. We therefore have
$$A=\int_{\mathcal{F}}dS=\frac{1}{|\hat{\eta}_{z}|}\int_{R}dxdy$$
where $R$ is the region bounded by the projected polygon. Call this polygon's vertices $\vec{Q}_{i}=(x_{i},y_{i})$. This integral may be converted to a line integral by [[Teorema del rotore|Green's theorem]]:
$$\int_{R}P(x,y)dxdy=\int_{R}\nabla\cdot\vec{G}\ dxdy=\int_{L}\vec{M}\cdot\vec{G}\ ds$$
where $L$ is the 1D boundary of $R$, $ds$ is the arc length element $\vec{G}$ is a function such that $\nabla\cdot\vec{G}=P$ and $\vec{M}$ is the outgoing curve normal vector. In this example, $P=1$ and $L$ is a polygon. As in the previous section, there a several choices for $\vec{G}$, one of which is $\vec{G}=(x,0)$. Let's describe $L$ as the union of polygon edges $\mathcal{E}$: $L=\bigcup\mathcal{E}$. Each edge has its own curve normal $\vec{M}_{\mathcal{E}}$. Thus, the integral decomposes to
$$\int_{L}\vec{M}\cdot\vec{G}\ ds=\sum\limits_{\mathcal{E}\in L}\int_{\mathcal{E}}\vec{M}_{\mathcal{E}}\cdot\vec{G}\ ds$$
This is fundamentally the same process form the previous section, just going from surface to edges instead of volume to surfaces. We can parameterize the edges: the generic edge $\mathcal{E}$ is the segment between points $\vec{Q}_{i}$ and $\vec{Q}_{i+1}$ and has a length equal to $\ell_{i}=|\vec{Q}_{i}-\vec{Q}_{i}|$. Then, the edge can be parameterized as
$$(x(s),y(s))=\left(1- \frac{s}{\ell_{i}}\right)\vec{Q}_{i}+\left(\frac{s}{\ell_{i}}\right)\vec{Q}_{i+1}$$
for $s\in[0,\ell_{i}]$. The general form of the edge normal is
$$\vec{M}_{i}=\text{Sign}(\hat{\eta}_{z}) \frac{(y_{i+1}-y_{i},\ \ x_{i}-x_{i+1})}{\ell_{i}}$$
where the sign function makes the formula independent of the orientation. It is 1 if the orientation is counterclockwise, -1 otherwise. We can finally rewrite our integral as
$$\begin{align*}
\int_{L}\vec{M}\cdot\vec{G}&=\sum\limits_{i=0}^{n-1}\vec{M}_{i}\cdot(x(s),0)\ ds\\
&=\text{Sign}(\hat{\eta}_{z})\sum\limits_{i=0}^{n-1} \frac{y_{i+1}-y_{i}}{\ell_{i}}\int_{0}^{\ell_{i}}\left(1- \frac{s}{\ell_{i}}\right)x_{i}+\left(\frac{s}{\ell_{i}}\right)x_{i+1}\ ds\\
&=\text{Sign}(\hat{\eta}_{z})\sum\limits_{i=0}^{n-1} \frac{y_{i+1}-y_{i}}{\ell_{i}}\int_{0}^{1}(1-t)x_{i}+tx_{i+1}\ dt \qquad \text{with }t=\frac{s}{\ell_{i}}\\
&=\frac{1}{2}\text{Sign}(\hat{\eta}_{z})\sum\limits_{i=0}^{n-1}(y_{i+1}-y_{i})(x_{i+1}+x_{i})\\
&=\frac{1}{2}\text{Sign}(\hat{\eta}_{z})\sum\limits_{i=0}^{n-1}(y_{i+1}-y_{i-1})x_{i}
\end{align*}$$
The last equality exploits modular indexing where $y_{0}=y_{n}=y_{2n}=\ldots$ and $y_{-1}=y_{n-1}$. This reduces the number of arithmetic operations by a third.

One potential source of numerical error is when $|\hat{\eta}_{z}|\sim0$, as we need to divide by it. In this case, we can project onto a different plane and use $\hat{\eta}_{x}$ or $\hat{\eta}_{y}$ instead. The magnitude of $\vec{M}$ is 1, so at least one of its components must be large enough to reach this value (and therefore not $\sim0$), so this is guaranteed to remove the problem. The formulae for these cases are derive in an identical manner as above, just with different coordinates. The full list is for all three planes is
$$A=\left\{\begin{align}
\frac{1}{|\hat{\eta}_{z}|}\int_{R_{xy}}dxdy=\frac{1}{2}\text{Sign}(\hat{\eta}_{z})\sum\limits_{i=0}^{n-1}(y_{i+1}-y_{i-1})x_{i} \qquad &|\hat{\eta}_{z}|=\max\{|\hat{\eta}_{x}|,|\hat{\eta}_{y}|,|\hat{\eta}_{z}|\} \\
\frac{1}{|\hat{\eta}_{x}|}\int_{R_{yz}}dydz=\frac{1}{2}\text{Sign}(\hat{\eta}_{x})\sum\limits_{i=0}^{n-1}(z_{i+1}-z_{i-1})y_{i} \qquad &|\hat{\eta}_{x}|=\max\{|\hat{\eta}_{x}|,|\hat{\eta}_{y}|,|\hat{\eta}_{z}|\} \\
\frac{1}{|\hat{\eta}_{y}|}\int_{R_{zx}}dzdx=\frac{1}{2}\text{Sign}(\hat{\eta}_{y})\sum\limits_{i=0}^{n-1}(x_{i+1}-x_{i-1})z_{i} \qquad &|\hat{\eta}_{y}|=\max\{|\hat{\eta}_{x}|,|\hat{\eta}_{y}|,|\hat{\eta}_{z}|\}
\end{align}\right.$$
where $R_{xy}$, $R_{yz}$ and $R_{zx}$ are the projected polygons' region.

Now, recall that the above was for the specific case $P=1$. The general case is for any of the listed polynomials. The result can be obtained for each of them in the same manner. We get, for $A=\int_{S}Q(x,y,z)\ dS$:
$$A=\left\{\begin{align}
\frac{1}{|\hat{\eta}_{z}|}\int_{R_{xy}}Q\left(x,y,-\frac{w+\hat{\eta}_{x}x+\hat{\eta}_{y}y}{\hat{\eta}_{z}}\right)dxdy\qquad&|\hat{\eta}_{z}|=\max\{|\hat{\eta}_{x}|,|\hat{\eta}_{y}|,|\hat{\eta}_{z}|\} \\
\frac{1}{|\hat{\eta}_{x}|}\int_{R_{yz}}Q\left(-\frac{w+\hat{\eta}_{y}y+\hat{\eta}_{z}z}{\hat{\eta}_{x}},y,z\right)dydz\qquad &|\hat{\eta}_{x}|=\max\{|\hat{\eta}_{x}|,|\hat{\eta}_{y}|,|\hat{\eta}_{z}|\} \\
\frac{1}{|\hat{\eta}_{y}|}\int_{R_{zx}}Q\left(x,-\frac{w+\hat{\eta}_{x}x+\hat{\eta}_{z}z}{\hat{\eta}_{y}},z\right)dzdx\qquad &|\hat{\eta}_{y}|=\max\{|\hat{\eta}_{x}|,|\hat{\eta}_{y}|,|\hat{\eta}_{z}|\}
\end{align}\right.$$
where the polynomials include the respective plane equation of the projection. The polynomials are functions of two independent variables. We can solve the integral as we did before, just using a generically parameterized function $\vec{G}(x(s),y(x))$:
$$\begin{align*}
\int_{S}Q\,dS &=\frac{1}{|\hat{\eta}_{z}|}\sum\limits_{i=0}^{n-1}\int_{0}^{\ell_{i}}\vec{M}_{i}\cdot\vec{G}(x(s),y(s))\,ds\\
&=\frac{\text{Sign}(\hat{\eta}_{z})}{|\hat{\eta}_{z}|}\sum\limits_{i=0}^{n-1}\frac{(y_{i+1}-y_{i},x_{i}-x_{i+1})}{\ell_{i}}\cdot\int_{0}^{\ell_{i}}G\left(\left(1-\frac{s}{\ell_{i}}\right)\vec{Q}_{i}+\left(\frac{s}{\ell_{i}}\right)\vec{Q}_{i+1}\right)\,ds \\
&=\frac{1}{\hat{\eta}_{z}}\sum\limits_{i=0}^{n-1}(y_{i+1}-y_{i},x_{i}-x_{i+1})\cdot\int_{0}^{1}G((1-t)\vec{Q}_{i}+t\vec{Q}_{i+1})\ dt
\end{align*}$$
At this point, the formula can only be advanced by picking a form for $\vec{G}$. Unfortunately, there is no silver bullet: the solution must be found for each function individually. Below is the list of all possible solutions. The notations uses $(\alpha,\beta,\gamma)$ to represent any [[permutazione|permutation]] of the coordinates $(x,y,z)$. The projection integrals are denoted $\pi_{f}=\int_{R}f\ d\alpha d\beta$, where $R$ is the projected region onto the $\alpha\beta$-plane and $f$ is the polynomial function. We have
$$\begin{align}
\int_{\mathcal{F}}\alpha\,d S&=|\hat{\eta}_{\gamma}|^{-1}\pi_{\alpha}\\
\int_{\mathcal{F}}\beta\,d S&=|\hat{\eta}_{\gamma}|^{-1}\pi_{\beta}\\
\int_{\mathcal{F}}\gamma\,d S&=-|\hat{\eta}_{\gamma}|^{-1}\hat{\eta}_{\gamma}^{-1}(\hat{\eta}_{\alpha}\pi_{\alpha}+\hat{\eta}_{\beta}\pi_{\beta}+w\pi_{1})\\
\int_{\mathcal{F}}\alpha^{2}\,d S&=|\hat{\eta}_{\gamma}|^{-1}\pi_{\alpha^{2}} \\
\int_{\mathcal{F}}\beta^{2}\,d S&=|\hat{\eta}_{\gamma}|^{-1}\pi_{\beta^{2}}\\ \int_{\mathcal{F}}\gamma^{2}\,dS&=|\hat{\eta}_{\gamma}|^{-1}\hat{\eta}_{\gamma}^{-2}(\hat{\eta}_{\alpha}^{2}\pi_{\alpha^{2}}+2\hat{\eta}_{\alpha}\hat{\eta}_{\beta}\pi_{\alpha\beta}+\hat{\eta}_{\beta}^{2}\pi_{\beta^{2}})\\ &\quad+2w(\hat{\eta}_{\alpha}\pi_{\alpha}+\hat{\eta}_{\beta}\pi_{\beta})+w^{2}\pi_{1})\\
\int_{\mathcal{F}}\alpha^{3}\,dS&=|\hat{\eta}_{\gamma}|^{-1}\pi_{\alpha^{3}}\\
	\int_{\mathcal{F}}\beta^{3}\,d S&=|\hat{\eta}_{\gamma}|^{-1}\pi_{\beta^{3}}\\
\int_{\mathcal{F}}\gamma^{3}\,d S&=-|\hat{\eta}_{\gamma}\,|^{-1}\hat{\eta}_{\gamma}^{-3}(\hat{\eta}_{\alpha}^{3}\pi_{\alpha^{3}}+3\hat{\eta}_{\alpha}^{2}\hat{\eta}_{\beta}\pi_{\alpha^{2}\beta}+3\hat{\eta}_{\alpha}\hat{\eta}_{\beta}^{2}\pi_{\alpha\beta^{2}}+\hat{\eta}_{\beta}^{3}\pi_{\beta^{3}}\\ &\quad+3w(\hat{\eta}_{\alpha}^{2}\pi_{\alpha^{2}}+2\hat{\eta}_{\alpha}\hat{\eta}_{\beta}\pi_{\alpha\beta}+\hat{\eta}_{\beta}^{2}\pi_{\beta^{2}})\\
&\quad+3w^{2}(\hat{\eta}_{\alpha}\pi_{\alpha}+\hat{\eta}_{\beta}\pi_{\beta})+w^{3}\pi_{1})\\
\int_{\mathcal{F}}\alpha^{2}\beta\,dS&=|\hat{\eta}_{\gamma}|^{-1}\pi_{\alpha^{2}\beta} \\
\int_{\mathcal{F}}\beta^{2}\gamma\,d S&=-|\hat{\eta}_{\gamma}|^{-1}\hat{\eta}_{\gamma}^{-1}(\hat{\eta}_{\alpha}\pi_{\alpha\beta^{2}}+\hat{\eta}_{\beta}\pi_{\beta^{3}}+w\pi_{\beta^{2}})\\
\int_{\mathcal{F}}\gamma^{2}\alpha\,dS&=|\hat{\eta}_{\gamma}|^{-1}\hat{\eta}_{\gamma}^{-2}(\hat{\eta}_{\alpha}^{2}\pi_{\alpha^{3}}+2\hat{\eta}_{\alpha}\hat{\eta}_{\beta}\pi_{\alpha^{2}\beta}+\hat{\eta}_{\beta}^{2}\pi_{\alpha\beta^{2}}\\
&\quad+2w(\hat{\eta}_{\alpha}\pi_{\alpha^{2}}+\hat{\eta}_{\beta}\pi_{\alpha\beta})+w^{2}\pi_{\alpha})
\end{align}$$
For the projection integrals
$$\begin{align*}
\pi_{1}&={\frac{\operatorname{Sign}({\hat{\eta}}_{\gamma})}{2}}\sum_{i=0}^{n-1}(\beta_{i+1}-\beta_{i})(\alpha_{i+1}+\alpha_{i})\\
\pi_{\alpha}&={\frac{\operatorname{Sign}({\hat{\eta}}_{\gamma})}{6}}\sum_{i=0}^{n-1}(\beta_{i+1}-\beta_{i})\big{(}\alpha_{i+1}^{2}+\alpha_{i+1}\alpha_{i}+\alpha_{i}^{2}\big{)}\\
\pi_{\beta}&=-{\frac{\operatorname{Sign}({\hat{\eta}}_{\gamma})}{6}}\sum_{i=0}^{n-1}(\alpha_{i+1}-\alpha_{i})\left(\beta_{i+1}^{2}+\beta_{i+1}\beta_{i}+\beta_{i}^{2}\right)\\
\pi_{\alpha^{2}}&=\frac{\text{Sign}(\hat{\eta}_{\gamma})}{12}\sum_{i=0}^{n-1}(\beta_{i+1}-\beta_{i})\big{(}\alpha_{i+1}^{3}+\alpha_{i+1}^{2}\alpha_{i}+\alpha_{i+1}\alpha_{i}^{2}+\alpha_{i}^{3}\big{)}\\
\pi_{\alpha\beta}&=\frac{\text{Sign}(\hat{\eta}_{\gamma})}{24}\sum_{i=0}^{n-1}(\beta_{i+1}-\beta_{i})\big{(}\beta_{i+1}\left(3\alpha_{i+1}^{2}+2\alpha_{i+1}\alpha_{i}+\alpha_{i}^{2}\right)\\
&\qquad\qquad\qquad\quad+\beta_{i}\left(\alpha_{i+1}^{2}+2\alpha_{i+1}\alpha_{i}+3\alpha_{i}^{2}\right))\\
\pi_{\beta^{2}}&=-\frac{\text{Sign}(\hat{\eta}_{\gamma})}{12}\sum_{i=0}^{n-1}(\alpha_{i+1}-\alpha_{i})\bigl(\beta_{i+1}^{3}+\beta_{i+1}^{2}\beta_{i}+\beta_{i+1}\beta_{i}^{2}+\beta_{i}^{3}\bigr)\\
\pi_{\alpha^{3}}&=\frac{\text{Sign}(\hat{\eta}_{\gamma^{\prime}})}{20}\sum_{i=0}^{n-1}(\beta_{i+1}-\beta_{i})\big{(}\alpha_{i+1}^{4}+\alpha_{i+1}^{3}\alpha_{i}+\alpha_{i+1}^{2}\alpha_{i}^{2}+\alpha_{i+1}\alpha_{i}^{3}+\alpha_{i}^{4}\big{)}\\
\pi_{\alpha^{2}\beta}&=\frac{\text{Sign}(\hat{\eta}_{\gamma^{\prime}})}{60}\sum_{i=0}^{n-1}(\beta_{i+1}-\beta_{i})\big{(}\beta_{i+1}\left(4\alpha_{i+1}^{3}+3\alpha_{i+1}^{2}\alpha_{i}+2\alpha_{i+1}\alpha_{i}^{2}+\alpha_{i}^{3}\right)\\
&\qquad\qquad\qquad\quad+\beta_{i}\left(\alpha_{i+1}^{3}+2\alpha_{i+1}^{2}\alpha_{i}+3\alpha_{i+1}\alpha_{i}^{2}+4\alpha_{i}^{3}\right)\big{)}\\
\pi_{\alpha\beta^{2}}&=-\frac{\text{Sign}(\hat{\eta}_{\gamma})}{60}\sum_{i=0}^{n-1}(\alpha_{i+1}-\alpha_{i})\big{(}\alpha_{i+1}\big{(}4\beta_{i+1}^{3}+3\beta_{i+1}^{2}\beta_{i}+2\beta_{i+1}\beta_{i}^{2}+\beta_{i}^{3}\big{)}\\
&\qquad\qquad\qquad\quad+\alpha_{i}\big{(}\beta_{i+1}^{3}+2\beta_{i+1}^{2}\beta_{i}+3\beta_{i+1}\beta_{i}^{2}+4\beta_{i}^{3}\big{)}\big{)}\\
\pi_{\beta^{3}}&=-\frac{\text{Sign}(\hat{\eta}_{\gamma})}{20}\sum_{i=0}^{n-1}(\alpha_{i+1}-\alpha_{i})\big{(}\beta_{i+1}^{4}+\beta_{i+1}^{3}\beta_{i}+\beta_{i+1}^{2}\beta_{i}^{2}+\beta_{i+1}\beta_{i}^{3}+\beta_{i}^{4})
\end{align*}$$
Notice that the $\pi_{1}$ formula is just what we derive for the $P=1$ case.
#### Reduction of triangular faces
If the face polygon is a triangle, we can greatly simplify the formulas. Assume the face is ordered counterclockwise and has vertices $\vec{P}=(x_{i},y_{i},z_{i})$ for $i=0,1,2$. Two edges are
$$\vec{E}_{i}=\vec{P}_{i}-\vec{P}_{0}=(x_{i}-x_{0},y_{i}-y_{0},z_{i}-z_{0})=(\alpha_{i},\beta_{i},\gamma_{i})$$
for $i=1,2$. The face can be parameterized as
$$\begin{align*}
\vec{P}(u,v)&=\vec{P}_{0}+u\vec{E}_{1}+v\vec{E}_{2}\\
&=(x_{0}+\alpha_{1}u+\alpha_{2}v,y_{0}+\beta_{1}u+\beta_{2}v,z_{0}+\gamma_{1}u+\gamma_{2}v)\\
&=(x(u,v),y(u,v),z(u,v))
\end{align*}$$
where $u\geq0$, $v\geq0$ and $u+v\leq1$. The surface element is
$$dS=\left|\frac{\partial \vec{P}}{\partial u}\times\frac{\partial \vec{P}}{\partial v}\right|dudv=|\vec{E}_{1}\times\vec{E}_{2}|dudv$$
and the outgoing normal vector for the face is
$$\vec{N}_{\mathcal{F}}=\frac{\vec{E}_{1}\times\vec{E}_{2}}{|\vec{E}_{1}\times\vec{E}_{2}|}=\frac{(\beta_{1}\gamma_{2}-\beta_{2}\gamma_{1},\alpha_{2}\gamma_{1}-\alpha_{1}\gamma_{2},\alpha_{1}\beta_{2}-\alpha_{2}\beta_{1})}{|\vec{E}_{1}\times\vec{E}_{2}|}=\frac{(\delta_{0},\delta_{1},\delta_{2})}{|\vec{E}_{1}\times\vec{E}_{2}|}$$
where we defined
$$\boxed{\begin{cases}
\delta_{0}&=\beta_{1}\gamma_{2}-\beta_{2}\gamma_{1}=(y_{1}-y_{0})(z_{2}-z_{0})-(y_{2}-y_{0})(z_{1}-z_{0}) \\
\delta_{1}&=\alpha_{2}\gamma_{1}-\alpha_{1}\gamma_{2}=(x_{2}-x_{0})(z_{1}-z_{0})-(x_{1}-x_{0})(z_{2}-z_{0}) \\
\delta_{2}&=\alpha_{1}\beta_{2}-\alpha_{2}\beta_{1}=(x_{1}-x_{0})(y_{2}-y_{0})-(x_{2}-x_{0})(y_{1}-y_{0})
\end{cases}}$$
This means the integrals from $(1)$ simplify to
$$\begin{align*}\\
(\vec{N}_{\mathcal{F}}\cdot\vec{\ell})\int_{\mathcal{F}}Q(x,y,z)\,d S&=(\vec{E}_{1}\times\vec{E}_{2}\cdot\vec{\ell})\int_{0}^{1}\int_{0}^{1-v}Q(x(u,v),y(u,v),z(u,v))\,d u\,d v \\
&=(\vec{E}_{1}\times\vec{E}_{2}\cdot\vec{\ell})\int_{0}^{1}\int_{0}^{1-v}Q(\vec{P}(u,v))\,d u\,d v
\end{align*}$$
These integrals can be solved analytically. Define the values
$$\boxed{\begin{align*}
s_{n}(w)&=\sum_{i=0}^{n}w_{0}^{n-i}w_{1}^{i}\\
f_{0}(w)&=1\\
f_{n}(w)&=s_{n}(w)+w_{2}f_{n-1}(w)\quad\text{for }n\geq1\\
g_{i}(w)&=f_{2}(w)+w_{i}f_{1}(w)+w_{i}^{2}
\end{align*}}$$
With these, the solutions are
$$\boxed{\begin{align}(\vec{N}_{\mathcal{F}}\cdot\vec{i})\int_{\mathcal{F}}x\,d S=\frac{\delta_{0}}{6}f_{1}(x)\qquad&(\vec{N}_{\mathcal{F}}\cdot\vec{j})\int_{\mathcal{F}}y^{3}\,d S=\frac{\delta_{1}}{20}f_{3}(y)\\ (\vec{N}_{\mathcal{F}}\cdot\vec{i})\int_{\mathcal{F}}x^{2}\,d S=\frac{\delta_{0}}{12}f_{2}(x)\qquad&(\vec{N}_{\mathcal{F}}\cdot\vec{k})\int_{\mathcal{F}}z^{3}\,d S=\frac{\delta_{2}}{20}f_{3}(z)\\
(\vec{N}_{\mathcal{F}}\cdot\vec{j})\int_{\mathcal{F}}y^{2}\,d S=\frac{\delta_{1}}{12}f_{2}(y)\qquad&(\vec{N}_{\mathcal{F}}\cdot\vec{i})\int_{\mathcal{F}}x^{2}y\,d S=\frac{\delta_{0}}{60}(y_{0}g_{0}(x)+y_{1}g_{1}(x)) \\ (\vec{N}_{\mathcal{F}}\cdot\vec{k})\int_{\mathcal{F}}z^{2}\,d S=\frac{\delta_{2}}{12}f_{2}(z)\qquad&(\vec{N}_{\mathcal{F}}\cdot\vec{j})\int_{\mathcal{F}}y^{2}z\,d S=\frac{\delta_{1}}{60}(z_{0}g_{0}(y)+z_{1}g_{1}(y))+z_{2}g_{2}(y))\\
(\vec{N}_{\mathcal{F}}\cdot\vec{i})\int_{{\mathcal{F}}}x^{3}\,d S={\frac{\delta_{0}}{20}}{\hat{f}}_{3}(x)\qquad&(\vec{N}_{\mathcal{F}}\cdot\vec{k})\int_{{\mathcal{F}}}z^{2}x\,d S={\frac{\delta_{2}}{60}}(x_{0}g_{0}(z)+x_{1}g_{1}(z)+x_{2}g_{2}(z))
\end{align}}$$
Just for comparison, let's see how the formula for $x$ looks like
$$Q_{x}=\frac{\delta_{0}}{6}f_{1}(x)=\frac{\delta_{0}}{6}(x_{0}+x_{1}+x_{2})$$
whereas Mirtich's formula would be
$$Q_{x}={\frac{\delta_{0}}{6}}{\frac{(y_{1}-y_{0})(x_{1}^{2}+x_{0}x_{1}+x_{0}^{2})+(y_{2}-y_{1})(x_{2}^{2}+x_{1}x_{2}+x_{1}^{2})+(y_{0}-y_{2})(x_{0}^{2}+x_{0}x_{2}+x_{2}^{2}))}{(x_{1}-x_{0})(y_{2}-y_{0})-(x_{2}-x_{0})(y_{1}-y_{0})}}$$
which is massively more complicated and computationally expensive. In fact, the numerator divides perfectly by the denominator and ends up giving $(x_{0}+x_{1}+x_{2})$, just like the simpler formula above.