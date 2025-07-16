---
wiki-publish: true
aliases:
  - Einstein's first postulate
  - Einstein's second postulate
  - Einstein velocity addition rule
---
The theory of special relativity is based on two fundamentals claims, known as the **postulates of special relativity**:
1. The laws of physics are the same in all inertial [[frame of reference|frames of reference]].
2. Light moves in the vacuum at a constant [[Speed of light|speed]] in all inertial frames of reference, and it is the maximum speed at which [[energy]] can propagate.

Compared to [[Galilean relativity]], special relativity extends the equivalence of inertial frames to *all* of physics instead of only classical mechanics, essentially stating that there is no such thing as a "universal rest frame". The second postulates adds an ulterior constraint, denying the existence of an "ether frame" that the speed of light is relative to.

These postulates lead to all the other phenomena that special relativity explains, namely [[relativity of simultaneity]], [[time dilation]] and [[Length contraction]].
### Relativistic velocity addition rule
The second postulate essentially generalizes the old velocity addition rule of Galileo:
$$v_{AC}=v_{AB}+v_{BC}$$
where $A$, $B$ and $C$ represent three objects in motion relative to each other; for instance, a person $A$ walking in a train $B$ traveling over the ground $C$. The speed of the person with respect to the train $v_{AB}$ is whatever speed it's walking at (say, $5\text{ km/h}$). The speed of the train with respect to the ground $v_{BC}$ is whatever speed it's traveling at (say, $100\text{ km/h}$). Then, the speed of the person with respect to the ground $v_{AC}$ must be the simple sum of the two ($105\text{ km/h}$). This method cannot possibly work when there exists a maximum speed in the universe, for if one were to, say, shine a flashlight on the train, the total speed of the light would be
$$v_{\text{light}}=c+\text{100 km/h}$$
which is of course greater than $c$. The new special relativistic velocity addition rule is
$$\boxed{v_{AC}=\frac{v_{AB}+v_{BC}}{1+v_{AB}v_{BC}/c^{2}}}$$
which is the same as the previous one, but weighed by a factor $(1+v_{AB}v_{BC}/c^{2})^{-1}$. The benefit is that this satisfies the universality of the speed of light, for if $v_{AB}=c$, then
$$v_{AC}=\frac{c+v_{BC}}{1+cv_{BC}/c^{2}}=c \frac{1+v_{BC}/c}{1+v_{BC}/c}=c$$
This rule is found by applying a [[Lorentz transformation]] on a moving object. Say this object moves some small distance $dx$ on the $x$ axis of an inertial frame of reference $\mathcal{S}$. Its velocity in that frame will be
$$u=\frac{dx}{dt}$$
In another inertial frame $\mathcal{S}'$, it will have moved a distance determined by the Lorentz transformation on $x'$
$$dx'=\gamma(dx-vdt)$$
in time also determined by the transformation on $t'$:
$$dt'=\gamma\left( dt- \frac{v}{c^{2}}dx \right)$$
The velocity in $\mathcal{S}'$ will therefore be
$$u'=\frac{dx'}{dt'}=\frac{\gamma (dx-vdt)}{\gamma(dt-v/c^{2}dx)}=\frac{dx/dt-v}{1-(v/c^{2}) dx/dt}=\frac{u-v}{1-uv/c^{2}}$$
This is Einstein's velocity addition rule. It matches the previous statement when $A$ is the object, $B$ is $\mathcal{S}$ and $C$ is $\mathcal{S}'$. In that case, $u=v_{AB}$, $u'=v_{AC}$ and $v=v_{CB}=-v_{BC}$.