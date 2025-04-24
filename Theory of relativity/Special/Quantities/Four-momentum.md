---
aliases:
  - energy-momentum four-vector
---
The **four-momentum**, or **energy-momentum four-vector**, of an object of [[mass]] $m$ is the [[four-vector]]
$$p^{\mu}=m\eta^{\mu}=\left(\frac{E}{c},\;\mathbf{p}\right)$$
where $\eta^{\mu}$ is the [[proper velocity]]. If we use the relativistic energy $E=\gamma mc^{2}$ and relativistic momentum $\mathbf{p}=\gamma m\mathbf{v}$, we can state
$$p^{\mu}=(\gamma mc,\;\gamma m\mathbf{v})$$
### Relativistic energy
In the same way as classical [[Linear momentum|momentum]] correlates quite directly with energy, so too does the four-momentum correlate with relativistic. Inspired by the fact that to get the classical energy we need to take the square [[norm]] of momentum (since $E=\lvert \mathbf{p} \rvert^{2}/2m$), we just need to take the norm of the four-vector (we'll use $\lvert \mathbf{p} \rvert\equiv p$ for simplicity):
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
### $N$-body system
The four-momentum and relativistic energy of a [[Physical system|system]] of $N$ bodies is just the sum of individual momenta and energy:
$$p_{\text{total}}^{\mu}=\sum_{i=1}^{N} p_{i}^{\mu},\qquad E_{\text{total}}=\sum_{i=1}^{N} E_{i}$$
The norm of the total momentum is
$$p_{\text{total}}^{\mu}p_{\mu}^{\text{total}}=-m_{I}^{2}c^{2}$$
Here, $m_{I}$ is not the mass of any particular object, it is known as the [[invariant mass]] of the system.
### Under Lorentz transformations
Let's take a particle $p$ in a reference frame in spherical coordinates.

![[Coordinate Sferiche Particella|center]]

Then
$$\pmatrix{\frac{E'}{c} \\ p_{x}' \\ p_{y}' \\ p_{z}'}=\pmatrix{\gamma & 0 & 0 & \beta\gamma \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ \beta\gamma & 0 & 0 & \gamma}\pmatrix{\frac{E}{c} \\ p_{x} \\ p_{y} \\ p_{z}}$$
with
$$\begin{cases}
p_{x}=p\sin\theta\cos\phi \\
p_{y}=p\sin\theta\sin\phi \\
p_{z}=p\cos\theta
\end{cases}$$
Then
$$\begin{cases}
E'=\gamma E+\beta\gamma p\cos\theta \\
p'\cos\theta'\cos\phi'=p\sin\theta\cos\phi \\
p'\sin\theta'\sin\phi'=p\sin\theta\sin\phi \\
p'\cos\theta=\gamma p\cos\theta+\beta\gamma E
\end{cases}$$
$$p^{2}\sin^{2}\theta'(\cos^{2}\phi'+\sin^{2}\phi')=p^{2}\sin^{2}\theta(\cos^{2}\phi+\sin^{2}\phi)$$
From which it is obtained
$$p'\sin\theta=p\sin\theta$$
which is called **transverse momentum** and holds
$$p'_{T}=p_{T}$$
and is a [[Relativistic invariant]]. From the same equation, we also find $\phi'=\phi$, therefore also the azimuthal angle is a relativistic invariant.
### Examples
> [!example] Inelastic collision
> An interesting and useful example is the [[inelastic collision]] of two [[particle|particles]] moving at relativistic speeds. This is essentially the central behavior of particle colliders such as the LHC at CERN: smash particles together, see what happens[^1]. Assume both particles are moving at $\beta=\frac{3}{5}c$, in opposite directions, aimed perfectly at each other. Both have the same mass $m$. The total three-momentum (not four-momentum!) before the collision is zero: after all, the individual momenta cancel out in a vector sum. Since momentum is conserved, it must be zero even after the collision: $\mathbf{p}_{\text{bef}}=\mathbf{p}_{\text{aft}}=0$. Energy on the other hand is
> $$E_\text{bef}=2 \frac{mc^{2}}{\sqrt{ 1- \left( \frac{3}{5} \right)^{2} }}=2 \frac{5}{4}mc^{2}=\frac{5}{2}mc^{2}$$
> Of course, energy is conserved, so $E_\text{bef}=E_\text{aft}$. But remember that the collision is inelastic: the particles get "stuck" together, they don't bounce[^2]. You'd expect the total mass $M$ of this object to be the the sum of individual masses, so $M=2m$, but it's not! Since the velocity of this object is *zero* (momenta cancel, leading to standstill), the only energy it has left is rest mass energy $E_{0}=Mc^{2}$, which means
> $$E_\text{bef}=E_\text{end}=E_{0}=Mc^{2}=\frac{5}{2}mc^{2}\quad\Rightarrow \quad M=\frac{5}{2}m>2m$$
> Evidently, we just "created" mass by transferring kinetic energy to mass energy. This is how we can make heavier particles for smaller, more stable ones like [[Elettrone|electrons]] and [[protone|protons]]: we just need high enough kinetic energies and a strong enough collision.

> [!example] Massless particles
> Some particles like [[photon|photons]] have no mass, yet they still possess some energy when moving. This is an inherently quantum phenomenon due to particle-wave duality (see for instance [[Formula di de Broglie]]), although that's not the point of this example. We just want to see what happens when $m=0$. Of course, the most intuitive thing to say is that $p^{\mu}=0$. After all, how can a massless particle have momentum? Well, you'd be *wrong*, for massless particles *do* have momentum, and as de Broglie showed it depends on the wavelength of the particle. So what now? de Broglie "says" that $p>0$ but Einstein "says" $p=0$. The issue here is that we haven't talked about the speed of the particle. Mathematically speaking, it is possible for $p$ to be nonzero even when $m=0$: we just need some term that goes to infinity just as fast as $m$ goes to zero, so that their asymptotic behaviors cancel out and leave us with a finite value. We don't have much to play with, really. The only other non-constant in $\mathbf{p}$ is the speed of the particle:
> $$\mathbf{p}=\frac{m\mathbf{v}}{\sqrt{ 1- \frac{v^{2}}{c^{2}} }}$$
> For $p>0$, we must simultaneously have $m\to0$ and $v\to c$. In this case — and only this case — does $p$ come out to be nonzero and finite. In other words, *all* massless particles *must* move at the speed of light. This is why "light moves at the speed of light", so to speak. Light is a photon beam, photons are massless, and so photons move at $c$. In truth, it would be more correct to call $c$ the "speed of massless particles", of which light happens to be made of, but scientists did not know this when they first coined the term.

[^1]: The actual experiments are obviously more complicated, usually testing the validity of numerous conservation laws for [[Numero quantico|quantum numbers]]. See for instance, [[Diffusione di particelle]].

[^2]: In practice, what happens is that a fundamentally random particle process occurs, reassigning quantum numbers around while respecting conservation laws. Either way, the system ends with a different set of objects compared to what it started with.
