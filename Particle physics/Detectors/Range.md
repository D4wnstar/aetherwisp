---
wiki-publish: true
aliases:
  - range straggling
---
In particle physics, the **range** of a [[Particle|particle]] in the distance it can travel in a medium before losing all its [[kinetic energy]] due to the medium's [[stopping power]]. It is defined as
$$R(K)=\int_{0}^{K_{0}} \frac{dK}{S(K)}$$
where $R$ is the mean range, $K_{0}$ is the initial energy of the particle, and $S(K)$ is the stopping power. It is typically measured in $\text{g}/\text{cm}^{2}$.

Provided different particles are given the same starting kinetic energy $K_{0}$, the range measured from their collisions onto a material is strongly representative of their [[mass]]. As such, range is a powerful tool for determining the mass of particle when we know its kinetic energy.

The definition follows from expressing the range as an [[integral]] and playing with the [[Differential|differentials]] to turn it into an energy integral:
$$R(K)=\int_{0}^{R}dx=\int_{K_{0}}^{0} \frac{dK}{dK} dx=-\int_{K_{0}}^{0} \frac{dK}{S(K)}=\int_{0}^{K_{0}} \frac{dK}{S(K)}$$

Since the amount of energy lost in the material is [[random]] ([[Stopping power|energy straggling]]), the range is also random and described by a [[probability distribution]] parameterized by kinetic energy. This phenomenon is called **range straggling**.
### Nonrelativistic behavior
For a particle of [[Electric charge|charge]] $z$, mass $M$, and nonrelativistic kinetic energy $K_{0}$, we can approximate the stopping power using the [[Stopping power|Bethe-Bloch formula]]. In nonrelativistic range, the logarithm is essentially constant. Then, the only functional dependence in $dK/dx$ is $z^{2}/\beta ^{2}$ and everything else is a constant. Then, we can state
$$\frac{dK}{dx} \simeq C \frac{z^{2}}{\beta^{2}}=C\frac{z^{2}c^{2}(M/2)}{v^{2}(M/2)} = C'\frac{Mz^{2}}{K}$$
where $M$ is the [[mass]] of the particle and $C,C'$ are some common constant to group up all the other constants. Then range becomes
$$R(K)=\int_{K_{0}}^{0} \frac{dK}{dK}dx\simeq \frac{C'}{Mz^{2}}\int_{K_{0}}^{0}KdK=\frac{C''}{Mz^{2}}K_{0}^{2}$$
(where $C''=-C'$). Given an initial kinetic energy $K_{0}$, the range varies with mass according to $1/M$. The heavier the particle, the smaller the range and greater the energy loss. Just like the Bethe-Bloch curve, this fact is very useful for measuring particle mass, as the path covered by a particle before decaying or stopping is often relatively easy to measure by, say, analyzing tracks in a [[cloud chamber]] or having a layered set of [[Detector|detectors]] that count the passage of particles.

:::image
![[Diagram Layered range measurement|80%]]
Experimental setup to measure range. A layer of detectors that absorb energy is setup, each with some length $l$. If a particle is absorbed is some detector, it will be recorded. Each detector will therefore count the number of particles that stop in it. This provides a [[histogram]] of distances covered and thus an estimate of the range distribution. If the range is bigger then the total length, $R(K_\text{in})>L$, then we'll see few measurements and no peak. If the range is less, $R(K_\text{in})<L$, then we'll see the full range distribution with a peak in one of the detectors and very few $N_\text{out}$.
:::
