---
wiki-publish: true
aliases:
  - rest mass energy
---
**Relativistic energy** is a term used to refer to the [[energy]] of a body when taking [[Lorentz transformation|relativistic]] effects into account. It is given by
$$E=\sqrt{ p^{2}c^{2}+m^{2}c^{4} }=\gamma mc^{2}$$
where $p$ is the [[Linear momentum|momentum]] of the body, $m$ is its [[mass]], $c$ is the [[speed of light]] and $\gamma$ is the usual relativistic coefficient. In the special case of an object with zero momentum, we find what is known as the **rest mass energy** of the body:
$$E_{0}=mc^{2}$$
Unlike classical mechanics where, barring [[potential energy]], the energy would be zero for an object with zero speed, in relativity there is always *some* energy for any massive object.
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
Expanding $\gamma$ in series for $\beta\ll1$ and taking the first order, we return to the classical formula for kinetic energy
$$K\sim\left(1+ \frac{\beta^{2}}{2} -1\right)\simeq \frac{mc^{2}\beta^{2}}{2}\simeq \frac{v^{2}}{2c^{2}}mc^{2}=\frac{1}{2}mv^{2}$$
