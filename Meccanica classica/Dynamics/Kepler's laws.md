**Kepler's laws** are a set of three laws that describe the motion of the Earth around the Sun in terms of classical [[Interazione gravitazionale|gravitation]]:
$$\vec{F}=- \frac{GMm}{r^{2}}\hat{R}$$
Using [[Newton's laws]] $\vec{F}=m\vec{a}$:
$$\vec{a}=- \frac{GM}{r^{3}}\vec{r}$$
Note that we went from $\hat{R}$ as a unit vector to $\vec{r}=r\hat{R}$ as a proper vector. Consider
$$\frac{d}{dt}(\vec{r}\times\vec{v})=\vec{r}\times\dot{\vec{v}}+\dot{\vec{r}}\times\vec{v}=\vec{r}\times\left(- \frac{GM}{r^{3}}\vec{r}\right)+\vec{v}\times\vec{v}=0$$
because a [[Prodotto vettoriale|cross product]] of a vector with itself is always zero. This means the angular velocity $\vec{r}\times\vec{v}=\vec{w}$ is some constant vector $\vec{C}$, and by extension the angular momentum $\vec{r}\times m\vec{v}$ is also constant. Also, $\vec{r}\cdot\vec{w}=\vec{r}\cdot\vec{C}=0$, which implies that the motion occurs on the plane determined by $\vec{r}\cdot\vec{C}=0$, which contains the position of the Sun and has a normal vector $\vec{C}$.
### First law
> Equal areas in the plane of motion are swept out in equal time intervals.

The rate of change for the area swept in a given time is
$$\dot{A}=\frac{1}{2}|\vec{r}\times\dot{\vec{r}}|=\frac{1}{2}|\vec{r}\times\vec{v}|=\frac{1}{2}|\vec{C}|$$
which is constant, therefore independent of time, therefore equal for any time interval.
### Second law
> The orbit of the Earth is an ellipse with the Sun as one of the focal points.

Consider
$$\begin{align*}
\frac{d}{dt}(\vec{v}\times\vec{C})&=\dot{\vec{v}}\times\vec{C}=- \frac{GM}{r^{3}}\vec{r}\times\vec{C}=- \frac{GM}{r^{3}}\vec{r}\times(\vec{r}\times\vec{v})=- \frac{GM}{r^{3}}\vec{r}\times(\vec{r}\times(r\dot{\hat{R}}+\dot{r}\hat{R}))=\\
&=- \frac{GM}{r^{3}}\vec{r}\times(r\vec{r}\times\dot{\hat{R}})=-GM\hat{R}\times(\hat{R}\times\dot{\hat{R}})=-GM((\hat{R}\cdot\dot{\hat{R}})\hat{R}-(\hat{R}\cdot\hat{R})\hat{R})=\\
&=GM\dot{\hat{R}}
\end{align*}$$
where we used the expression for velocity in [[polar coordinates]]. We can now integrate this easily to get $\vec{v}\times\vec{C}=GM\hat{R}+\vec{K}$ with $\vec{K}$ some other constant vector. We can see
$$|\vec{C}|^{2}=\vec{r}\times\vec{v}\cdot\vec{C}=\vec{r}\cdot\vec{v}\times\vec{C}=\vec{r}\cdot(GM\hat{R}+\vec{K})=GMr+\vec{r}\cdot\vec{K}=GMr+r|\vec{K}|\cos\theta$$
with $\theta$ the angle between $\vec{r}$ and $\vec{K}$. In polar coordinates, then, the equation can be solved for $r$ as a function of $\theta$:
$$r(\theta)=\frac{|\vec{C}|^{2}}{GM+|\vec{K}|\cos\theta}=\frac{e\rho}{1+e\cos\theta}$$
where $e=|\vec{K}|/GM$ is the eccentricity of the ellipse and $\rho=|\vec{C}|^{2}/|\vec{K}|$. The major axis length is $2a=r(0)+r(\pi)=2\rho e/(1-e^{2})$ and the minor axis length is $2b=2a\sqrt{1-e^{2}}$. The area is $A=\pi ab$.
### Third law
> The square of the period of the motion is proportional to the cube of the major axis length.

We know the areal rate of change from the first law, so we can integrate it over a period of time $t\in[0,T]$, which yields the total area of the ellipse $A=|\vec{C}|T/2$. But we also know the area from the second law, so if we equate the two we get
$$T=\frac{2A}{|\vec{C}|}=\frac{2\pi a^{2}\sqrt{1-e^{2}}}{\sqrt{GMa(1-e^{2})}}=\frac{2\pi}{\sqrt{GM}}a^{3/2}$$
thus
$$T^{2}\propto a^{3}$$
