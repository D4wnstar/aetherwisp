---
wiki-publish: true
aliases:
  - range straggling
  - Bragg peak
---
In particle physics, the **range** of a [[Particle|particle]] in the distance it can travel in a medium before losing all its [[kinetic energy]] due to the medium's [[stopping power]]. It is defined as
$$R(K)=\int_{0}^{K_{0}} \frac{dK}{S(K)}$$
where $R$ is the mean range, $K_{0}$ is the initial energy of the particle, and $S(K)$ is the stopping power. It is typically measured in $\text{g}/\text{cm}^{2}$.

Provided different particles are given the same starting kinetic energy $K_{0}$, the range measured from their collisions onto a material is strongly dependent on their [[mass]]. As such, range is a powerful tool for determining the mass of particle when we know its kinetic energy.

The definition follows from expressing the range as an [[integral]] and playing with the [[Differential|differentials]] to turn it into an energy integral:
$$R(K)=\int_{0}^{R}dx=\int_{K_{0}}^{0} \frac{dK}{dK} dx=-\int_{K_{0}}^{0} \frac{dK}{S(K)}=\int_{0}^{K_{0}} \frac{dK}{S(K)}$$

Since the amount of energy lost in the material is [[random]] ([[Stopping power|energy straggling]]), the range is also random. As in the energy case, this phenomenon is called **range straggling**.

For heavy particles, the energy loss scales as $\sim 1/v^{2} \sim 1/K$. Because of this, the majority of energy lost occurs where the particle is slowest, which means at the end of its travel distance right before it stops. A plot of energy loss versus depth shows a sharp peak around the mean range, a shape known as a **Bragg peak**.
### Nonrelativistic behavior
For a particle of [[Electric charge|charge]] $z$, mass $M$, and nonrelativistic kinetic energy $K_{0}$, we can approximate the stopping power using the [[Stopping power|Bethe-Bloch formula]]. In nonrelativistic range, the logarithm is essentially constant. Then, we can state
$$\frac{dK}{dx} \sim \frac{z^{2}}{\beta^{2}}=\frac{z^{2}c^{2}(M/2)}{v^{2}(M/2)} = C\frac{Mz^{2}}{K}$$
where $C$ is some common constant that groups up all the other constants. Then range becomes
$$R(K)=\int_{K_{0}}^{0} \frac{dK}{dK}dx\simeq \frac{C}{Mz^{2}}\int_{K_{0}}^{0}KdK=\frac{C'}{Mz^{2}}K_{0}^{2}$$
(where $C'=-C$). Given an initial kinetic energy, the range varies with mass according to $1/M$. The heavier the particle, the smaller the range and greater the energy loss. Just like the Bethe-Bloch curve, this fact is very useful for measuring particle mass.