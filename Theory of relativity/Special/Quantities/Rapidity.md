---
wiki-publish: true
---
The **rapidity** $y$ is an alternative quantity to represent the speed of a [[particle]], typically in the context of relativity. Given the relativistic speed coefficient $\beta=v/c$, where $c$ is the [[speed of light]], the rapidity is defined as its hyperbolic arctangent:
$$y=\text{arctanh } \beta$$
Rapidity, by construction, is a [[relativistic invariant]].

The benefit of rapidity is that, since it is defined from a hyperbolic arctangent, it goes from $-\infty$ to $+\infty$ as $v\to \pm c$. Moreover, rapidities add like in classical physics ($y_{1}+y_{2}=y_\text{total}$) instead of having to follow the [[Postulates of special relativity|Einstein velocity addition rule]]. These facts combined make rapidity quite similar to how velocity works in classical physics, which can make it a more intuitive way of describing movement.
### Derivation
The rapidity is the value for which the following relations hold:
$$\begin{cases}
e^{y}=\gamma(1+\beta)=\gamma\left(1+ \frac{v}{c}\right)=\sqrt{\frac{1+ \frac{v}{c}}{1- \frac{v}{c}}}=\sqrt{\frac{1+\beta}{1-\beta}} \\
e^{-y}=\ldots=\sqrt{\frac{1-\beta}{1+\beta}}
\end{cases}$$
Then $y=\ln(\gamma(1+\beta))$ and
$$\begin{cases}
ct-x=e^{-y}(ct'-x') \\
ct+x=e^{y}(ct'+x')
\end{cases}$$
$$\frac{e^{y}+e^{-y}}{2}=\gamma\quad;\quad \frac{e^{y}-e^{-y}}{2}=\beta\gamma$$
from which we find
$$\begin{cases}
\gamma=\cosh(y) \\
\beta\gamma=\sinh(y)
\end{cases}$$
and putting them together
$$\beta=\tanh(y)$$
### As a hyperbolic rotation
Then we can interpret a [[Lorentz transformation]] as a hyperbolic [[rotation]] in [[spacetime]], with rapidity representing the angle of rotation:
$$\pmatrix{ct' \\ x' \\ y' \\ z'}=\pmatrix{\cosh y & -\sinh y & 0 & 0 \\ -\sinh y & \cosh y & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1}\pmatrix{ct \\ x \\ y \\ z}$$
