---
wiki-publish: true
---
**Kepler's laws** are a set of three laws that describe the motion of the Earth around the Sun in terms of classical [[Gravity|gravitation]]:
$$\mathbf{F}=- \frac{GMm}{r^{2}}\hat{R}$$
Using [[Newton's laws]] $\mathbf{F}=m\mathbf{a}$:
$$\mathbf{a}=- \frac{GM}{r^{3}}\mathbf{r}$$
Note that we went from $\hat{R}$ as a unit vector to $\mathbf{r}=r\hat{R}$ as a proper vector. Consider
$$\frac{d}{dt}(\mathbf{r}\times\mathbf{v})=\mathbf{r}\times\dot{\mathbf{v}}+\dot{\mathbf{r}}\times\mathbf{v}=\mathbf{r}\times\left(- \frac{GM}{r^{3}}\mathbf{r}\right)+\mathbf{v}\times\mathbf{v}=0$$
because a [[Vector product|cross product]] of a vector with itself is always zero. This means the angular velocity $\mathbf{r}\times\mathbf{v}=\mathbf{w}$ is some constant vector $\mathbf{C}$, and by extension the angular momentum $\mathbf{r}\times m\mathbf{v}$ is also constant. Also, $\mathbf{r}\cdot\mathbf{w}=\mathbf{r}\cdot\mathbf{C}=0$, which implies that the motion occurs on the plane determined by $\mathbf{r}\cdot\mathbf{C}=0$, which contains the position of the Sun and has a normal vector $\mathbf{C}$.
### First law
> Equal areas in the plane of motion are swept out in equal time intervals.

The rate of change for the area swept in a given time is
$$\dot{A}=\frac{1}{2}|\mathbf{r}\times\dot{\mathbf{r}}|=\frac{1}{2}|\mathbf{r}\times\mathbf{v}|=\frac{1}{2}|\mathbf{C}|$$
which is constant, therefore independent of time, therefore equal for any time interval.
### Second law
> The orbit of the Earth is an ellipse with the Sun as one of the focal points.

Consider
$$\begin{align*}
\frac{d}{dt}(\mathbf{v}\times\mathbf{C})&=\dot{\mathbf{v}}\times\mathbf{C}=- \frac{GM}{r^{3}}\mathbf{r}\times\mathbf{C}=- \frac{GM}{r^{3}}\mathbf{r}\times(\mathbf{r}\times\mathbf{v})=- \frac{GM}{r^{3}}\mathbf{r}\times(\mathbf{r}\times(r\dot{\hat{R}}+\dot{r}\hat{R}))=\\
&=- \frac{GM}{r^{3}}\mathbf{r}\times(r\mathbf{r}\times\dot{\hat{R}})=-GM\hat{R}\times(\hat{R}\times\dot{\hat{R}})=-GM((\hat{R}\cdot\dot{\hat{R}})\hat{R}-(\hat{R}\cdot\hat{R})\hat{R})=\\
&=GM\dot{\hat{R}}
\end{align*}$$
where we used the expression for velocity in [[Polar coordinates]]. We can now integrate this easily to get $\mathbf{v}\times\mathbf{C}=GM\hat{R}+\mathbf{K}$ with $\mathbf{K}$ some other constant vector. We can see
$$|\mathbf{C}|^{2}=\mathbf{r}\times\mathbf{v}\cdot\mathbf{C}=\mathbf{r}\cdot\mathbf{v}\times\mathbf{C}=\mathbf{r}\cdot(GM\hat{R}+\mathbf{K})=GMr+\mathbf{r}\cdot\mathbf{K}=GMr+r|\mathbf{K}|\cos\theta$$
with $\theta$ the angle between $\mathbf{r}$ and $\mathbf{K}$. In polar coordinates, then, the equation can be solved for $r$ as a function of $\theta$:
$$r(\theta)=\frac{|\mathbf{C}|^{2}}{GM+|\mathbf{K}|\cos\theta}=\frac{e\rho}{1+e\cos\theta}$$
where $e=|\mathbf{K}|/GM$ is the eccentricity of the ellipse and $\rho=|\mathbf{C}|^{2}/|\mathbf{K}|$. The major axis length is $2a=r(0)+r(\pi)=2\rho e/(1-e^{2})$ and the minor axis length is $2b=2a\sqrt{1-e^{2}}$. The area is $A=\pi ab$.
### Third law
> The square of the period of the motion is proportional to the cube of the major axis length.

We know the areal rate of change from the first law, so we can integrate it over a period of time $t\in[0,T]$, which yields the total area of the ellipse $A=|\mathbf{C}|T/2$. But we also know the area from the second law, so if we equate the two we get
$$T=\frac{2A}{|\mathbf{C}|}=\frac{2\pi a^{2}\sqrt{1-e^{2}}}{\sqrt{GMa(1-e^{2})}}=\frac{2\pi}{\sqrt{GM}}a^{3/2}$$
thus
$$T^{2}\propto a^{3}$$
### Angular speed
We can also explicitly find the angular speed $\dot{\theta}$ as
$$\dot{\theta}=\frac{\alpha}{G^{2}M^{3}}\left(c_{0}\sin\theta +c_{1}\cos\theta - \frac{G^{2}M^{4}}{\alpha^{2}}\right)^{2}$$
which is a first order, non-linear differential equation with a starting condition of $\theta(0)=\theta_{0}$. It can be solved numerically. $\alpha$ is the angular momentum (which is conserved) and $c_{0}$ and $c_{1}$ are constants to be determined.