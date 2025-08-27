---
wiki-publish: true
---
The **angular momentum** $\mathbf{L}$ of an object at position $\mathbf{r}$ moving about a point $O$ with [[linear momentum]] $\mathbf{p}$ is the [[Vector product|cross product]]
$$\mathbf{L}=\mathbf{r}\times \mathbf{p}$$
$\mathbf{r}$ is the vector connecting $O$ with the object.

A [[moment of force]] $\mathbf{N}$ applied onto the object changes the angular momentum of the object according to:
$$\mathbf{N}=\frac{d\mathbf{L}}{dt}=\dot{\mathbf{L}}$$
also using dot notation for the derivative. From this we can immediately see the very important theorem of angular momentum conservation.

> [!info] Conservation of angular momentum
> If the total moment of force $\mathbf{N}$ is zero, then $\dot{\mathbf{L}}=0$ and the angular momentum is conserved. Each components conserves independently, so for example if $N_{z}=0$ then $\dot{L}_{z}=0$.

An equivalent theorem also holds for a system of [[Particle|particles]]:

> [!info] Conservation of the angular momentum of a system of particles
> If the total *external* moment of force $\mathbf{N}$ is zero, and all of the internal forces (if present) are applied on the lines connecting each particle, the total angular momentum is conserved.

The clause about the direction of the internal forces is necessary to cancel out the internal moments of force, as they read $\mathbf{r}_{ij}\times \mathbf{F}_{ij}$, with $i$ and $j$ the indexes of individual particles. If $\mathbf{r}_{ij}$ and $\mathbf{F}_{ij}$ are not parallel, these do not cancel and the theorem does not hold. External moments of force are those applied to the particles by external sources and not other particles.