---
wiki-publish: true
aliases:
  - conic section
---
A **conic**, or more correctly **conic section**, is a geometric shape, specifically a [[curve]], derived from the intersection of a [[plane]] and a [[cone]]. It is defined as the locus of points of the plane in which the ratio $r/h$ is constant, where $r$ is the distance from a point called the **focus** and $h$ is the distance from a [[line]] called the **directrix**. The ratio is written $e\equiv r/h$ and called the **eccentricity** of the conic, which is a measure of how "squished" the shape is.

There are three kinds of conics: the [[hyperbola]], the [[parabola]] and the [[ellipse]]; the "fourth" type, the [[circle]], is a special case of the ellipse. The eccentricity of a circle is $e=0$. For an ellipse, it is $0<e<1$. For a parabola, $e=1$. For a hyperbola, $e>1$. The actual equations for these shapes are derived from analyzing the ratio $e=r/h$.
### Cartesian coordinates
In [[Cartesian coordinates]] $(x,y)$ one gets
$$\frac{\tilde{x}^{2}}{\left( \frac{ed}{1-e^{2}} \right)^{2}}+ \frac{y^{2}}{\frac{(ed)^{2}}{1-e^{2}}}=1$$
where
$$\tilde{x}=x+ \frac{d}{1-e^{2}}$$
and $d$ is the distance between the focus and the origin. If we call the denominators $a^{2}$ and $b^{2}$, we get the familiar formulas for ellipses ($e<1$) 
$$\text{(parabola)}\quad\frac{x^{2}}{a^{2}}+ \frac{y^{2}}{b^{2}}=1$$
and hyperbolas ($e>1$)
$$\text{(hyperbola)}\quad\frac{x^{2}}{a^{2}}- \frac{y^{2}}{b^{2}}=1$$
### Polar coordinates
In [[polar coordinates]] $(r,\theta)$, the ratio becomes
$$\frac{r}{h}=e\quad\to \quad \frac{r}{e}=d-r\cos \theta$$
Extracting $r$ we get
$$r\left( \frac{1}{e}+\cos \theta \right)=\frac{\eta}{e}\quad\to \quad r=\frac{\eta}{e\left( \frac{1}{e}+\cos \theta \right)}$$
so
$$r(\theta)=\frac{\eta}{1+e\cos \theta}$$
