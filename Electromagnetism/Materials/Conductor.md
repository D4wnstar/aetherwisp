---
wiki-publish: true
---
A **conductor** is a material that contains a large (ideally infinite) number of free [[electric charge|electric charges]], typically [[Elettrone|electrons]] or [[ione|ions]].
### Properties
Conductors have special characteristic properties:
1. The [[electric field]] $\mathbf{E}$ is zero inside the conductor.
2. The volume charge density $\rho$ is zero inside the conductor.
3. Any net charge resides on the surface[^1].
4. A conductor is an equipotential volume, meaning the [[electric potential]] is the same for any two points inside or on the surface of the conductor.
5. The electric field is perpendicular to the surface at any point on the surface.
#### Explanation
When an external electric field $\mathbf{E}_{0}$ is applied to the conductor, the positive and negative charges that comprise it move towards or away from the field. This means there is a surplus of positive charges on one side of the material and a surplus of negative ones on the other. These excesses then produce what's called an **induced charge**, making the two sides of the material positively and negatively charged overall. These charges cause an electric field $\mathbf{E}_{1}$ to occur whose direction is exactly opposite that of $\mathbf{E}_{0}$. The magnitude of both is also identical, as $\mathbf{E}_{1}$ depends on the displacement of the charges, which itself depends on $\mathbf{E}_{0}$. This means that $\mathbf{E}_{0}$ and $\mathbf{E}_{1}$ cancel each other out within the material, leading to a net neutral zone inside (property 1). Outside, however, the field is nonzero. This adaptive nature of conductors applies for any field almost instantly, leading to a "response" field $\mathbf{E}_{1}$ that follows $\mathbf{E}_{0}$ perfectly.

Using [[Gauss' law]], we have $\nabla\cdot\mathbf{E}=\rho/\varepsilon_{0}$, so if $\mathbf{E}$ is zero inside, so is $\rho$ (property 2). Since charges cannot be created or destroyed and cannot stay on the inside, they must "migrate" to the surface, leading to a surface charge distribution (property 3). In fact, this can be seen as a consequence of the [[least action principle]], as the energy of the system needs to be at its lowest for the system to come to rest. As it happens the electrostatic energy of a solid is always lowest when all charge is distributed at the boundary surface, when keeping charge and shape constant.

The electric field is given by $\mathbf{E}=-\nabla V$, so if $\mathbf{E}=0$ then $V$ must be a constant (property 4).

Any component $\mathbf{E}$ not perpendicular to the surface would cause a shift in the underlying charges for the same reasons an outside field does, meaning that charges reassess constantly in such a way that any tangential component $\mathbf{E}$ is removed (property 5).
### Cavity and internal charges
Say you have a solid conductor with a hollow cavity dug out in it. Say, then, you place a charge within the cavity. The electric field within the cavity will not be zero, but outside of the cavity it will be entirely nullified, similarly to an external field. This implies that the internal charge is completely isolated from the outside world and viceversa.

That said, the charge still has an effect on the interior surface of the cavity, as it forces the charges of the solid to be aligned in such a way that they nullify the internal field. This has a repercussions on the outer surface too, which will be charged in the opposite manner as the inner one for balance and thus communicate the presence of an internal charge to an outside observer. The charge on the inner surface is equal and opposite to the cavity charge, as a consequence of Gauss' law. The charge on the outer surface must be equal and opposite to the inner surface charge, which means equal to the cavity charge. So for a charge $q$ it goes
$$+q_\text{cavity} \to -q_\text{inner surface} \to +q_\text{outer surface}$$
### Surface force and pressure
We can find the force applied to a charge on the surface by taking the average of the internal and external fields. In a conductor, the internal field is always zero, so the result is very simple:
$$\mathbf{E}_\text{avg}=\frac{\mathbf{E}_\text{above}}{2}$$
so the force per unit area is
$$\mathbf{f}=\frac{\sigma}{2}\mathbf{E}_\text{above}=\frac{\sigma^{2}}{2\varepsilon_{0}}\hat{\mathbf{n}}$$
where we used the fact that the discontinuity of the field over a surface is always $(\sigma/\varepsilon_{0})\hat{\mathbf{n}}$. This amounts to an outwards [[electrostatic pressure]] on the surface, tending to draw the conductor into the field, regardless of the sign of $\sigma$. Just outside the surface, the pressure is
$$P=\frac{\varepsilon_{0}}{2}E^{2}$$
### Modelling dispersion
The near-infinite free charges in conductors cause them to exhibit very special behavior when subject to [[electromagnetic wave|electromagnetic waves]]. A discussion on the reflection and transmission behavior can be found in [[Electromagnetic wave#In conductors]]. There, it is found that conductors suppress incoming waves within a very short distance, a phenomenon called the [[skin effect]], and that conductors universally cause [[dispersion]] in the wave. 

[^1]: It's important to stress that this property only applies to a 3D volume. A 2D conductor such as a disk does not have all its charges on the perimeter circle and a 1D line conductor does not have its charges only at its ends.