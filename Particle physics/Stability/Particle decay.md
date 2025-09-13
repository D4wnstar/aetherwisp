---
wiki-publish: true
---
**Particle decay** is the [[random]] process by which an unstable [[particle]] spontaneously splits into one or more particles. It is a process that is first and foremost governed by conservation laws. While a particle may decay in a large number of other particles, the outcome of a decay is heavily restricted by the fact that many intrinsic properties of the particle must be conserved. For instance, [[electric charge]] is conserved, so if the decaying particle has charge $+e$, the total charge across all decay products must also be $+e$.

Particles decay in order to reduce their [[Relativistic energy|rest energy]], which makes them more stable. This is allowed because in relativity, total energy is split between rest energy and [[kinetic energy]]. As such, a decay process involves converting some of the parent particle's rest mass into kinetic energy of the products, leading to a smaller total [[mass]]. Indeed, the condition for decay to be spontaneous is
$$m_\text{parent}>\sum_{i=1}^{N} m_{i\text{-th product}}$$
The energy difference is converted to kinetic energy.

Particle decay is often explained through [[Diagramma di Feynman|Feynman diagrams]], which are standardized schematic representations of particle scattering. Being entire diagrams, they can carry much more information than a simple mathematical representation, which is sorely needed given the complexity of many-particle interactions.

It is similar to, but distinct from, [[nuclear decay]], which occurs in [[Atomic nucleus|nuclei]] and involves different mechanisms.
## Common situations
The exact nature of a particle decay is entirely dependent on the particle itself and its properties. However, the *kinematics* of the process are by-and-large the same for all of them. Most decays happen in one of three situations, which are presented below.
#### Particle at rest
This is the simplest case. An unstable particle $a$ is at rest. At some point, it spontaneously decays into two particles, $b$ and $c$:
$$a\to b+c$$
The emission sends particles away from each other, in opposite directions. This is called **back-to-back decay**.

![[Diagram Particle decay back-to-back|center]]

We'll use [[natural units]]. Conservation of [[energy]] and [[Linear momentum|momentum]] read
$$\begin{cases}
0=\mathbf{p}_{b}+\mathbf{p}_{c} \\
m_{a}=E_{b}+E_{c}
\end{cases}$$
The momenta must go in opposite directions and have the same magnitude:
$$\mathbf{p}_{b}=-\mathbf{p}_{c}\quad\Rightarrow \quad \lvert \mathbf{p}_{b} \rvert =\lvert \mathbf{p}_{c} \rvert $$
In other words, momentum is evenly split between the two. Call $p$ the common magnitude. Then, using the [[relativistic energy]] formula $E=\sqrt{ p^{2}+m^{2} }$,
$$m_{a}=\sqrt{p^{2}+m_{b}^{2}}+\sqrt{p^{2}+m_{c}^{2}}$$
or
$$m_{a} - \sqrt{p^{2}+m_{b}^{2}} = \sqrt{p^{2}+m_{c}^{2}}$$
We want to solve for $p$. Take the square of both sides
$$m_{a}^{2} + p^{2} + m_{b}^{2} - 2m_{a}\sqrt{p^{2}+m_{b}^{2}} = p^{2} + m_{c}^{2}$$
Cancel out $p^{2}$ and rearrange
$$m_{a}^{2} + m_{b}^{2} - m_{c}^{2} = 2m_{a}\sqrt{p^{2}+m_{b}^{2}}$$
Square again to get the final root out of the way
$$(m_{a}^{2} + m_{b}^{2} - m_{c}^{2})^{2} = 4m_{a}^{2}(p^{2} + m_{b}^{2})$$
Now solve for $p$
$$\boxed{p = \frac{1}{2m_{a}} \sqrt{ m_{a}^{4} + (m_{b}^{2} - m_{c}^{2})^{2} - 2m_{a}^{2}(m_{b}^{2} + m_{c}^{2}) }}$$
The interesting result here is that the final momentum of both products is exclusively determined by masses. But since masses are inherent properties of particles, so must be the decay momentum at rest. As such, as long as we have the masses of the particles involved, we can directly predict the momenta of a back-to-back decay at rest.

If you want, you can now also determine the energies. Since $p$ is a function of just mass, then so is all relativistic energy:
$$\begin{cases}
E_{b} = \sqrt{p^{2} + m_{b}^{2}} = \dfrac{ m_{a}^{2} + m_{b}^{2} - m_{c}^{2} }{ 2m_{a} } = \dfrac{ s + m_{b}^{2} - m_{c}^{2} }{ 2\sqrt{s} } \\
E_{c} = \sqrt{p^{2} + m_{c}^{2}} = \dfrac{ m_{a}^{2} - m_{b}^{2} + m_{c}^{2} }{ 2m_{a} } = \dfrac{ s - m_{b}^{2} + m_{c}^{2} }{ 2\sqrt{s} }
\end{cases}$$
where $\sqrt{ s }$ is the [[center-of-mass energy]]. In this case it's equal to $\sqrt{ s }=m_{a}$, since the mass energy of (resting) parent particle is the only energy available to the decay. Once $\sqrt{s}$ is fixed, the energies depend only on the masses.
### Particle in flight
This scenario is similar to the above, in that it's a particle decaying in two bodies, but now the particle is moving. Hence, the center-of-mass energy also includes the [[kinetic energy]] of the parent. Since the particle is moving from our perspective, the choice of [[frame of reference]] becomes important.

In the laboratory frame, at rest with the scientists and [[detector|detectors]], the particle moves at some initial speed. Since momentum is conserved, the decay products will inherit it. This makes them also fly forward, but at an angle, with respect to the original line of motion.

![[Schema Decadimento ad un angolo|80%|center]]

Conservation says
$$\begin{cases}
\mathbf{p}_{a}=\mathbf{p}_{b}+\mathbf{p}_{c} \\
E_{a}=E_{b}+E_{c}
\end{cases}$$
Call $\theta_{1}$ and $\theta_{2}$ the two angles at which the products are emitted and $\theta=\theta_{1}+\theta_{2}$ their sum. The interesting part of this decay is that if you go into the [[Lorentz transformation|center-of-momentum frame]], where $\mathbf{p}_\text{tot}=0$, this goes back to being back-to-back decay. In fact, since $\mathbf{p}_\text{tot}=\mathbf{p}'_{a}=0$, you get
$$\begin{cases}
0=\mathbf{p}'_{b}+\mathbf{p}'_{c} \\
m_{a}=E'_{b}+E'_{c}=\sqrt{ s }
\end{cases}$$
which is back-to-back decay. The primes denote that the we are in a different frame, so the values change.

Now consider the lab frame. The invariant mass is:
$$\begin{align}
\sqrt{s} &= M_{\pi^{0}} = \sqrt{(p_{\gamma,1} + p_{\gamma,2})^2} \\
&= \sqrt{ (E_{\gamma,1} + E_{\gamma,2})^2 - (\mathbf{p}_{\gamma,1} + \mathbf{p}_{\gamma,2})^2 } \\
&= \sqrt{ E_{\gamma,1}^2 + E_{\gamma,2}^2 + 2E_{\gamma,1}E_{\gamma,2} - (p_{\gamma,1}^2 + p_{\gamma,2}^2 + 2|\mathbf{p}_{\gamma,1}||\mathbf{p}_{\gamma,2}|\cos\theta) } \\
&= \sqrt{ 2E_{\gamma,1}E_{\gamma,2}(1 - \cos\theta) } = \sqrt{ 4E_{\gamma,1}E_{\gamma,2} \sin^2\frac{\theta}{2} }
\end{align}$$

(using $E_\gamma = |\mathbf{p}_\gamma|$ and $1 - \cos\theta = 2\sin^2(\theta/2)$). Thus, the [[Invariant mass]] depends on the angle between photons in the lab frame.

Now solve for the minimum angle:
$$\sin\frac{\theta}{2} = \frac{M_{\pi^{0}}}{2\sqrt{E_{1}E_{2}}}$$
If energies are equal, $E_{1}=E_{2}=E_{\pi}/2$, the angle is minimized.

Energy transforms between frames. Perform a [[Lorentz transformation]] along the pion's direction ($x$-axis):
$$\begin{cases}
E_{\gamma,1} = \gamma(E_{\gamma,1}^{*} + \beta p_{\gamma,1}^{*} \cos\theta^{*}) \\
p_{1,x} = \gamma(p_{\gamma,1}^{*} \cos\theta^{*} + \beta E_{\gamma,1}^{*}) \\
p_{1,y} = p_{\gamma,1}^{*} \sin\theta^{*} \\
p_{1,z} = p_{\gamma,1}^{*} \cos\phi^{*} \sin\theta^{*}
\end{cases}$$
where $*$ denotes CM frame quantities.

#### Three-Body Decay

In a three-body decay, momentum conservation does not fully determine the momenta. The system:
$$\begin{cases}
\mathbf{p}_{1} + \mathbf{p}_{2} + \mathbf{p}_{3} = 0 \\
E_{1} + E_{2} + E_{3} = M
\end{cases}$$
has more degrees of freedom than constraints, leading to a continuous spectrum.

A useful trick is to consider the [[Invariant mass]] of two particles as a single entity:
$$s_{12} = (p_1 + p_2)^2 = (M - p_3)^2 = M^2 + m_3^2 - 2ME_3$$
Thus:
$$E_3 = \frac{M^2 + m_3^2 - s_{12}}{2M}$$

$E_3$ varies with $s_{12}$. The minimum $E_3$ occurs when particle 3 is at rest:
$$E_3^{\text{min}} = m_3$$

The maximum $E_3$ occurs when $s_{12}$ is minimized. The minimum invariant mass of the pair is:
$$s_{12}^{\text{min}} = (m_1 + m_2)^2$$
achieved when particles 1 and 2 are collinear and have equal velocities ($\beta_1 = \beta_2$, $\gamma_1 = \gamma_2$).

Then:
$$E_3^{\text{max}} = \frac{M^2 + m_3^2 - (m_1 + m_2)^2}{2M}$$

