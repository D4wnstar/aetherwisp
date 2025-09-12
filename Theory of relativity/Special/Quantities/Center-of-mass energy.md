---
wiki-publish: true
---
The **center-of-mass energy** of a relativistic [[Physical system|system]] is the [[norm]] of the total [[four-momentum]]:
$$\lvert p_{\text{tot}} \rvert=\sqrt{s} =\sqrt{\left(\sum\limits_{i}E_{i}\right)^{2}-\left(\sum\limits_{i}\mathbf{p}_{i}\right)^{2}}$$
It is a [[relativistic invariant]].

The center-of-mass energy is most commonly used to determine the amount of [[energy]] that is available to a [[particle scattering]] or [[particle decay]] process.
### Examples
> [!example]- Particle on a fixed target
> Consider a fixed target of mass $m_{2}$. We'll use [[natural units]]. Its four-momentum is $p_{2}=(m_{2},0)$. It is hit perpendicularly by a projectile of four-momentum $p_{1}=(E_{1},\mathbf{p}_{1})$. The center-of-mass energy of the impact is
> $$\begin{align}
> \sqrt{s}&=\lvert p_{1}+p_{2} \rvert  \\
> &=\sqrt{(E_{1}+m_{2})^{2}-|\mathbf{p}_{1}|^{2}} \\
> &=\sqrt{E_{1}^{2}+m_{2}^{2}+2E_{1}m_{2}-|\mathbf{p}_{1}|^{2}} \\
> &=\sqrt{m_{1}^{2}+|\mathbf{p}_{1}|^{2}+m_{2}^{2}+2E_{1}m_{2}-|\mathbf{p}_{1}|^{2}} \\
> &=\sqrt{m_{1}^{2}+m_{2}^{2}+2E_{1}m_{2}}
> \end{align}$$
> In the special case of a particle with much more [[kinetic energy]] than [[Relativistic energy|rest energy]], we can say $E_{1}\gg m_{1}$ and so
> $$\sqrt{ s }\simeq \sqrt{2E_{1}m_{2}}$$

> [!example]- Two particles at an angle
> Consider two particles of four-momenta $(E_{1},\mathbf{p}_{1})$ and $(E_{2},\mathbf{p}_{2})$. We'll use [[natural units]]. If they collide at an angle $\theta$, the center-of-mass energy of the impact is
> $$\begin{align}
> \sqrt{s}&=\sqrt{(E_{1}+E_{2})^{2}-(\mathbf{p}_{1}+\mathbf{p}_{2})^{2}} \\
> &=\sqrt{E_{1}^{2}+E_{2}^{2}+2E_{1}E_{2}-(|\mathbf{p}_{1}|^{2}+|\mathbf{p}_{2}|^{2}+2\mathbf{p}_{1}\cdot\mathbf{p}_{2})} \\
> &=\sqrt{E_{1}^{2}+E_{2}^{2}+2E_{1}E_{2}-(|\mathbf{p}_{1}|^{2}+|\mathbf{p}_{2}|^{2}+2p_{1}p_{2}\cos\theta)}
> \end{align}$$
> If the special case of particles with much more kinetic energy than rest energy, we have $E_{1}\simeq p_{1}$ and $E_{2}\simeq p_{2}$, therefore
> $$\sqrt{s}\simeq\sqrt{2E_{1}E_{2}-2E_{1}E_{2}\cos\theta}=\sqrt{2E_{1}E_{2}(1-\cos\theta)}$$
> If the collision is head-on ($\theta\simeq0$), then we have $\sqrt{s}\simeq\sqrt{2E_{1}E_{2}}$.
