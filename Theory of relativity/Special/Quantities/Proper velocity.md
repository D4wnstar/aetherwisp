---
wiki-publish: true
aliases:
  - ordinary velocity
---
**Proper velocity** or **4-velocity** $\eta$ of a moving object is the derivative [[spacetime]] [[displacement four-vector|displacement]] $x$ measured by the observer in the [[proper time]] $d\tau$ measured by the object:
$$\eta^{\mu}=\frac{dx^{\mu}}{d\tau}=(\eta^{0},\boldsymbol{\eta})$$
where $\gamma$ is the [[Lorentz transformation|relativistic]] gamma. This is opposed to the **ordinary velocity** $\mathbf{v}$ (only defined in space, not spacetime) which is the derivative of displacement measured by the observer in time *also* measured by the observer, $\mathbf{v}=d\mathbf{x}/dt$. The two are related by
$$\boldsymbol{\eta}=\gamma \mathbf{v}$$

| Quantity          | Symbol       | Space          | Time                       |
| ----------------- | ------------ | -------------- | -------------------------- |
| Ordinary velocity | $\mathbf{v}$ | Observer frame | Observer frame             |
| Proper velocity   | $\eta$       | Observer frame | Object frame (proper time) |

From the perspective of a traveler, the ordinary velocity is what *others* see you moving at, whereas the proper velocity is a bit of a mixed bag, since it's the space that *others* will see you cover, in your *own* time. The benefit of a quantity of this sort is that it interacts pleasantly with [[Lorentz transformation|Lorentz transformations]]. The time component is given by the [[speed of light]] $c$ as
$$\eta^{0}=\frac{dx^{0}}{d\tau}=c \frac{dt}{d\tau}=\frac{c}{\sqrt{ 1- v^{2}/c^{2} }}=\gamma c$$
and the space components are
$$\boldsymbol{\eta}=\frac{\mathbf{v}}{\sqrt{ 1-v^{2}/c^{2} }}=\gamma \mathbf{v}$$
When placed under Lorentz transformation, we get
$$\bar{\eta}^{\mu}=\Lambda_{\nu}^{\mu}\eta^{\nu}$$
By comparison, ordinary velocity must transform according to the [[Postulates of special relativity|Einstein velocity addition rule]], which are much more verbose.