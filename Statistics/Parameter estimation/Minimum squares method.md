---
wiki-publish: true
---
The **minimum squares method** is a [[parameter estimation]] method. It assumes that the outputs $y$ are related to the inputs $x$ according to a function $y=f(x;\mathbf{p})$ for some set parameters $\mathbf{p}$. The method returns an [[estimator]] of $\mathbf{p}$. It is commonly employed in [[linear regression]], where $\mathbf{p}=(m,q)$ are the linear parameters of $y=mx+q$.

Given a set of $N$ samples $\{ x_{1},\ldots,x_{N} \}$ and related values $\{ y_{1},\ldots,y_{N} \}$, we call
$$\chi ^{2}=\sum_{i=1}^{N} \left[ \frac{y_{i}-f(x_{i};\mathbf{p})}{\sigma} \right]^{2}$$
where $\sigma$ is the [[standard deviation]] of the output sample set $\{ y_{1},\ldots,y_{N} \}$. This is the deviation of the assumed function $f(x_{i};\mathbf{p})$ from the measured values $y_{i}$ for the $i$-th pair $(x_{i},y_{i})$, normalized by the deviation, squared and then summed over all pairs. The idea of the method is to minimize the variation of this quantity with respect to all the parameters $\mathbf{p}=(p_{1},\ldots,p_{M})$, meaning
$$\boxed{\frac{ \partial \chi ^{2} }{ \partial p_{i} } =0\quad\forall\ p_{i}}$$
This will reduce the difference between the measured $y$ and the estimated $f(x;\mathbf{p})$ to a minimum.
### Linear minimum squares
In linear regression, the relation is $f(x;\mathbf{p})=mx+q$ we are trying to estimate $\mathbf{p}=(m,q)$. $\chi ^{2}$ becomes
$$\chi ^{2}=\sum_{i=1}^{N} \left( \frac{y_{i}-mx_{i}-q}{\sigma} \right)^{2}$$
We need to minimize two derivatives:
$$\begin{align}
\frac{ \partial \chi ^{2} }{ \partial m } =0\quad&\Rightarrow \quad \sum_{i=1}^{N} \frac{ \partial  }{ \partial m } (y_{i}-mx_{i}-q)^{2}=0 \\
\frac{ \partial \chi ^{2} }{ \partial q } =0\quad&\Rightarrow \quad \sum_{i=1}^{N} \frac{ \partial  }{ \partial q } (y_{i}-mx_{i}-q)^{2}=0
\end{align}$$
This system can be solved to find
$$\boxed{m=\frac{NS_{xy}-S_{x}S_{y}}{D},\qquad q=\frac{S_{x}^{2}S_{y}-S_{x}S_{xy}}{D}}$$
where
$$S_{xy}=\sum_{i=1}^{N} x_{i}y_{i},\quad S_{xx}=\sum_{i=1}^{N} x_{i}^{2},\quad S_{x}=\sum_{i=1}^{N}x_{i},\quad S_{y}=\sum_{i=1}^{N}y_{i},\quad D=NS_{xx}-S_{x}^{2}  $$
These equations can be further handled using [[Variance#Propagation of variance]] to read
$$m=\frac{1}{N}\sum_{i=1}^{N} \frac{x_{i}-\mu_{x}}{\mu_{x^{2}}-\mu_{x}^{2}}y_{i}\quad\Rightarrow \quad \sigma_{m}^{2}=\sum_{i=1}^{N} \left(\frac{1}{N} \frac{x_{i}-\mu_{x}}{\mu_{x^{2}}-\mu_{x}^{2}}\right)^{2}\sigma ^{2}$$
and more
$$\boxed{\sigma_{q}=\sqrt{ \frac{\sigma ^{2}S_{xx}}{D} },\qquad \sigma_{m}=\sqrt{ \frac{N\sigma ^{2}}{D} }}$$
### Nonlinear minimum squares
In case of a nonlinear $f(x;\mathbf{p})$, using minimum squares is more involved. The easiest way is to linearize the equation.

Take for example the freefall equation
$$s=\frac{1}{2}gt^{2}$$
where $g$ is [[gravitational acceleration]] and $t$ is time. Of course, this is a quadratic relation in time, so $s=f(t;g)$ won't be linear. Let's do some algebra to make it linear. Invert to get $t$:
$$t=\sqrt{ \frac{2s}{g} }$$
This is of course also not linear, since the square root of $\sqrt{ s }$ isn't linear. However, we don't *have* to use $s$ as our input. We can just $\sqrt{ s }$ directly! In this case we could write
$$\underbrace{ t }_{ y }=\underbrace{ \sqrt{ \frac{2}{g} } }_{ m }\underbrace{ \sqrt{ s } }_{ x }+\underbrace{ t_{0} }_{ q }$$
and we get a linear relation again, which can be solved using the method above. ($t_{0}$ was added manually since it's possible there might be some bias in our measurements. Ideally we get $t_{0}=0$ and it disappears.) Just be careful of taking the square roots of your values of $s$ before using them. Once we're done with the estimation, we get $g$ out of $m$ with
$$m=\sqrt{ \frac{2}{g} }\quad\Rightarrow \quad g=\frac{2}{m^{2}}$$
The variance of $m$ is known from the linear minimum squares. The variance of $g$ is hence given by the propagation of variance
$$\sigma_{g}^{2}=\left( \frac{ \partial g }{ \partial m }  \right)^{2}\sigma_{m}^{2}$$
