---
wiki-publish: true
aliases:
  - rest mass energy
---
**Relativistic energy** is a term used to refer to the [[energy]] of a body when taking [[Lorentz transformation|relativistic]] effects into account. It is given by
$$E=\sqrt{ p^{2}c^{2}+m^{2}c^{4} }=\gamma mc^{2}$$
where $p$ is the [[Linear momentum|momentum]] of the body, $m$ is its [[mass]], $c$ is the [[speed of light]] and $\gamma$ is the relativistic gamma. In the special case of an object with zero momentum, we find what is known as the **rest (mass) energy** of the body:
$$E_{0}=mc^{2}$$
Unlike classical mechanics where, barring [[potential energy]], the energy would always be zero for an object with zero speed, in relativity there is always *some* energy for any massive object. As such, this rest energy must be of a special nature and we are thus left with *three*, not two, pieces of energy: potential energy, [[kinetic energy]] and rest mass energy. The relativistic energy is the sum of the last two. In fact, the kinetic energy of a body is
$$K=E-E_{0}=E-mc^{2}$$
The total relativistic energy of a [[Physical system|system]] is a conserved quantity. This does not mean it is a [[relativistic invariant]]; conservation has nothing to do with [[Frame of reference|frames of reference]], it just means that the quantity remains the same before and after a process. Notably, this means that mass is *not* conserved, as it can "flow" into kinetic energy and viceversa so long the total relativistic energy is conserved.
### From four-momentum
In the same way as classical [[Linear momentum|momentum]] correlates quite directly with kinetic energy, so too does the [[four-momentum]] correlate with relativistic energy. Inspired by the fact that to get the classical energy we need to take the square [[norm]] of momentum (since $E=\lvert \mathbf{p} \rvert^{2}/2m$), we'll take the norm of the four-vector (we'll use $\lvert \mathbf{p} \rvert\equiv p$ for simplicity):
$$\begin{align}
p^{\mu}p_{\mu}&=p^{0}p_{0}+\mathbf{p}\cdot \mathbf{p}=-(p^{0})^{2}+p^{2}=- \left( \frac{E}{c} \right)^{2}+ \frac{m^{2}v^{2}}{(1-v^{2}/c^{2})}= \\
&=- \frac{m^{2}c^{2}}{(1- v^{2}/c^{2})}+ \frac{m^{2}v^{2}}{(1-v^{2}/c^{2})}=-m^{2}c^{2}
\end{align}$$
We can match intermediate steps to state
$$p^{\mu}p_{\mu}= \frac{E^{2}}{c^{2}}+p^{2}=-m^{2}c^{2}$$
which gives
$$E^{2}-p^{2}c^{2}=m^{2}c^{4}$$
When reordered, we find what's known as the **relativistic energy** of a body:
$$\boxed{E^{2}=p^{2}c^{2}+m^{2}c^{4}}$$
In the simplest case of an object with no momentum, $p^{2}=0$, we find the well-known formula due to Einstein for **rest mass energy**:
$$\boxed{E_{0}=mc^{2}}$$
This is the energy an object holds exclusively due to its mass. This stands in contrast with [[kinetic energy]] $K$, which is given by the motion. With this in mind, the relativistic energy is
$$E^{2}=E_{0}^{2}+K^{2}$$
We can also rewrite $\beta$ and $\gamma$ as
$$\gamma=\frac{E}{mc^{2}},\qquad\beta=\frac{|\mathbf{p}|c}{E}$$
#### Connection to classical energy
We can see how the relativistic energy falls back to classical energy in the low velocity limit. If we extract the kinetic part of the energy
$$K=E-mc^{2}=\gamma mc^{2} -mc^{2}=mc^{2}(\gamma-1)$$
Expressing $\gamma$ in [[Binomial theorem|binomial expansion]] for $\beta\ll1$ and taking the first order, we find
$$K\simeq\left(1+ \frac{\beta^{2}}{2} -1\right)=\frac{mc^{2}\beta^{2}}{2}=\frac{v^{2}}{2c^{2}}mc^{2}=\frac{1}{2}mv^{2}$$
which is the classical formula for kinetic energy.