---
wiki-publish: true
aliases:
  - velocity field
  - acceleration field
  - generalized Coulomb field
  - radiation field
---
The **Liénard-Wiechert potentials** are the [[retarded potentials]] of a [[Electric charge|point charge]] $q$ moving on a specific trajectory:
$$V(\mathbf{r},t)=\frac{1}{4\pi \varepsilon_{0}} \frac{qc}{(\mathfrak{r}c-\boldsymbol{\mathfrak{r}}\cdot \mathbf{v})}$$
$$\mathbf{A}(\mathbf{r},t)=\frac{\mu_{0}}{4\pi} \frac{qc\mathbf{v}}{(\mathfrak{r}c-\boldsymbol{\mathfrak{r}}\cdot \mathbf{v})}=\frac{\mathbf{v}}{c^{2}}V(\mathbf{r},t)$$
$\mathbf{v}$ is the velocity of the charge at the [[retarded time]] and $\boldsymbol{\mathfrak{r}}$ is the distance between the retarded position (the position at the retarded time) to the field point $\mathbf{r}$.

These potentials lead to the general [[Electric field|electric]] and [[magnetic field]] of a moving point charge:
$$\mathbf{E}(\mathbf{r},t)=\frac{q}{4\pi \varepsilon_{0}} \frac{\mathfrak{r}}{(\boldsymbol{\mathfrak{r}}\cdot \mathbf{u})^{3}}
[(c^{2}-v^{2})\mathbf{u}+\boldsymbol{\mathfrak{r}}\times(\mathbf{u}\times \mathbf{a})]$$
$$\mathbf{B}(\mathbf{r},t)=\frac{1}{c}\hat{\boldsymbol{\mathfrak{r}}}\times \mathbf{E}(\mathbf{r},t)$$
where $\mathbf{u}\equiv c \hat{\mathfrak{r}}-\mathbf{v}$. The first term of the electric field is known as the **velocity field** (or **generalized Coulomb field**) and the second as the **acceleration field** (or **radiation field**).

In case of a point charge moving with constant velocity, these reduce to
$$\mathbf{E}(\mathbf{r},t)=\frac{q}{4\pi \varepsilon_{0}} \frac{1- v^{2}/c^{2}}{(1-(v^{2}/c^{2})\sin ^{2}\theta)^{3/2}} \frac{\hat{\mathbf{R}}}{R^{2}}$$
$$\mathbf{B}(\mathbf{r},t)=\frac{1}{c^{2}}(\mathbf{v}\times \mathbf{E})$$
where $\mathbf{R}\equiv \mathbf{r}-\mathbf{v}t$ is the vector from the *present* location $\mathbf{v}t$ of the charge to $\mathbf{r}$, and $\theta$ is the angle between $\mathbf{R}$ and $\mathbf{v}$.
### Derivation
The proof begins from the general form of retarded potentials. The electric potential is
$$V(\mathbf{r},t)=\frac{1}{4\pi \varepsilon_{0}}\int \frac{\rho(\mathbf{r}',t_{r})}{\mathfrak{r}}\ d\tau'\tag{1}$$
where, critically, $\rho$ is dependent on the retarded time $t_{r}$. This form is almost identical to the simultaneous case, just with $t_{r}$ added in, which begs the suggestion that the solution for a point charge $q$ might be the same
$$\frac{1}{4\pi \varepsilon_{0}} \frac{q}{\mathfrak{r}}$$
with the caveat that $\mathfrak{r}$ is now the distance from the *retarded* position instead of the current one. But that would be wrong, for the $t_{r}$ dependency in $\rho$ fundamentally changes what $\int \rho(\mathbf{r}',t_{r})d\tau'$ *is*. Whereas without $t_{r}$, $\rho(\mathbf{r}')$ refers to the charge distribution at *one instant*, with $t_{r}$ it is the charge distribution spread not just in space but also throughout time, as the retardation leads to a distorted charge depending on how far you are from the origin.

It pays to describe this phenomenon with a more easily imagined object: a train. Say you're looking at a train that's coming right towards you[^1]. Though you will not notice in the real world because it's so tiny, you will see the train as *longer* than if were standing to the side, or behind it. This is a fundamentally geometric effect due to the finite speed of light. The light from the back of the train was emitted earlier than the one we receive at the same time from the front, since the train is moving towards you. If the train were still, the difference in distance covered by light from the front and back would be exactly the length of the train, but since it's moving, the light from the front has to cover less distance because it's moving towards. By the time the light from the back reaches, the train moved forward and the light you receive simultaneously from the front is *after* the motion, since the train covered space that the light would've had to cover itself. This means that you see the *current* front of the train, but the *past* back.

:::image
![[Figure Retarded train length.png]]
From *Introduction to Electrodynamics 4th ed., Griffiths*
:::

The train looks longer by an amount determined by how much space the train covers while the light from the back attempts to reach you. If the light from the back needs to travel a distance $L'$ at speed $c$ for it to reach you, the train moves by a distance $L'-L$ at speed $v$. Since these two take the same amount of time we can state
$$\frac{L'}{c}=\frac{L'-L}{v}\quad\to \quad L'=\frac{L}{1-v/c}$$
The train looks longer by a factor $(1-v/c)^{-1}\geq1$. If the train were going away, it would look shorter by a factor $(1+v/c)^{-1}\leq 1$.

If instead you are at angle $\theta$ from the train, and it is far enough or short enough that the light beams from the front and back can be considered parallel, the past light from the back must instead travel $L'\cos \theta$ (and the train still moves the same distance $L'-L$), which yields
$$\frac{L'\cos\theta}{c}=\frac{L'-L}{v}\quad\to \quad L'=\frac{L}{1-(v\cos \theta)/c}$$
Same as before, but we notice that only the part of velocity coming towards you (more formally, parallel to your line of sight) is significant, as shown by the cosine. The perpendicular component does not matter: if you are watching the train from the side ($\theta \simeq90°$), the distortion factor falls back to $1$ and you see no distortion. We can therefore generalize from $v\cos \theta$ to $\hat{\boldsymbol{\mathfrak{r}}}\cdot \mathbf{v}$, where $\hat{\boldsymbol{\mathfrak{r}}}$ is the unit vector from the train to the observer. The *volume* of the train $\tau$, then, will be shrunk to a new volume $\tau'$ by a factor
$$\tau'=\frac{\tau}{1-\hat{\boldsymbol{\mathfrak{r}}}\cdot \mathbf{v}/c}\tag{2}$$

Back to electrodynamics, we can just change the object's volume $\tau$ to the total charge $q$ within the volume. Thus, our integral $(1)$ then solves *almost* in the original way, but the charge $q$ is now modified by the same factor as seen in $(2)$:
$$V(\mathbf{r},t)=\frac{1}{4\pi \varepsilon_{0}}\int \frac{\rho(\mathbf{r}',t_{r})}{\mathfrak{r}}\ d\tau'=\frac{1}{4\pi \varepsilon_{0}} \frac{q'}{\mathfrak{r}}=\frac{1}{4\pi \varepsilon_{0}} \frac{1}{\mathfrak{r}} \frac{q}{1-\hat{\boldsymbol{\mathfrak{r}}}\cdot \mathbf{v}/c}$$
where $\mathbf{v}$ is now the velocity of the charge. It might be surprising that this correction is significant for a point charge also, since it has no volume, but the correction factor in $(2)$ actually makes no reference to the size of the train/charge/whatever, it only cares about the *velocity relative to the observer*. It is fair to say that anything that's moving must abide to this phenomenon[^2].

The retarded time for a point charge is determined implicitly by the equation
$$\lvert \mathbf{r}-\mathbf{w}(t_{r}) \rvert =c(t-t_{r})$$
where $\mathbf{w}$ is the trajectory of the charge and $\mathbf{w}(t_{r})$ is the location of the charge at time $t_{r}$, the *retarded position* so to speak. The left side is the distance the signal must travel, whereas $t-t_{r}$ on the right is the time it takes to do so. We can call $\boldsymbol{\mathfrak{r}}=\mathbf{r}-\mathbf{w}(t_{r})$ the distance from the retarded position to the point $\mathbf{r}$. This is important because it allows us to claim that there is only ever *one* point $\mathbf{w}(t_{r})$ in communication with $\mathbf{r}$ at any given time. In fact, if there were two different retarded times $t_{r_{1}}$ and $t_{r_{2}}$ (and associated positions) such that $\mathfrak{r}_{1}=c(t-t_{r_{1}})$ and $\mathfrak{r}_{2}=c(t-t_{r_{2}})$, the then we'd have $\mathfrak{r}_{1}-\mathfrak{r}_{2}=c(t_{r_{2}}-t_{t_{1}})$. But this implies that the average speed of the particle in the direction of $\mathbf{r}$ must be $c$. Even ignoring components in other directions, which could very well set the speed to be greater than $c$ — an impossibility on its own — no charged particle can ever travel at *exactly* $c$, so this is really impossible[^3]. Therefore, there can only every be one retarded time/position for any point $\mathbf{r}$. This is important because it guarantees that it is unique everywhere and it is never a superposition of two retarded potentials from the same particle:
$$\boxed{V(\mathbf{r},t)=\frac{1}{4\pi \varepsilon_{0}} \frac{qc}{(\mathfrak{r}c-\boldsymbol{\mathfrak{r}}\cdot \mathbf{v})}}$$
Similarly, since the current density is $\rho \mathbf{v}$ and $\mathbf{v}$ comes out of the volume integral, in practice you get the same result: the vector potential is
$$\boxed{\mathbf{A}(\mathbf{r},t)=\frac{\mu_{0}}{4\pi} \frac{qc\mathbf{v}}{(\mathfrak{r}c-\boldsymbol{\mathfrak{r}}\cdot \mathbf{v})}=\frac{\mathbf{v}}{c^{2}}V(\mathbf{r},t)}$$
#### Fields
Now that we have the potentials, it's possible to calculate the [[electric field]] and [[magnetic field]] of the point charge[^4]. The potential expression of the fields is
$$\mathbf{E}=-\nabla V-\frac{ \partial \mathbf{A} }{ \partial t },\qquad \mathbf{B}=\nabla\times \mathbf{A}$$
Differentiation is greatly complicated by the fact that more than one variable is dependent on retarded time, $\boldsymbol{\mathfrak{r}}=\mathbf{r}-\mathbf{w}(t_{r})$ and $\mathbf{v}=\dot{\mathbf{w}}(t_{r})$, with $t_{r}\equiv t_{r}(\mathbf{r},t)$ itself being dependent on $\mathbf{r}$ and $t$, so the calculation is rather arduous. It is, however, possible.

Let's start from the [[gradient]] of $V$:
$$\nabla V=\frac{qc}{4\pi \varepsilon_{0}} \frac{-1}{(\mathfrak{r}c-\boldsymbol{\mathfrak{r}}\cdot \mathbf{v})^{2}}\nabla(\mathfrak{r}c-\boldsymbol{\mathfrak{r}}\cdot \mathbf{v})$$
We need the gradient at the end. Normally, without retarded time, we'd have $\nabla \mathfrak{r}=\hat{\boldsymbol{\mathfrak{r}}}$. However, with retarded time, we have $\mathfrak{r}=c(t-t_{r})$, which means $\nabla \mathfrak{r}=-c\nabla t_{r}$. The second piece of gradient is
$$\nabla (\boldsymbol{\mathfrak{r}}\cdot \mathbf{v})=(\boldsymbol{\mathfrak{r}}\cdot \nabla)\mathbf{v}+(\mathbf{v}\cdot \nabla)\boldsymbol{\mathfrak{r}}+\boldsymbol{\mathfrak{r}}\times(\nabla\times \mathbf{v})+\mathbf{v}\times(\nabla\times \boldsymbol{\mathfrak{r}})\tag{3}$$
We'll need to calculate all of these one by one, no way around it. Term one:
$$\begin{align}
(\boldsymbol{\mathfrak{r}}\cdot \nabla)\mathbf{v}&=\left( \mathfrak{r}_{x}\frac{ \partial  }{ \partial x } +\mathfrak{r}_{y}\frac{ \partial }{ \partial y } +\mathfrak{r}_{z}\frac{ \partial  }{ \partial z }  \right)\mathbf{v}(t_{r}) \\
&=\mathfrak{r}_{x} \frac{d\mathbf{v}}{dt_{r}} \frac{dt_{r}}{dx}+ \mathfrak{r}_{y} \frac{d\mathbf{v}}{dt_{r}} \frac{dt_{r}}{dy}+ \mathfrak{r}_{z} \frac{d\mathbf{v}}{dt_{r}} \frac{dt_{r}}{dz} \\
&=\mathbf{a}(\boldsymbol{\mathfrak{r}}\cdot \nabla t_{r})
\end{align}\tag{Term 1}$$
where $\mathbf{a}\equiv \dot{\mathbf{v}}$ is the acceleration of the point charge. Term two:
$$(\mathbf{v}\cdot \nabla)\boldsymbol{\mathfrak{r}}=(\mathbf{v}\cdot \nabla)\mathbf{r}-(\mathbf{v}\cdot \nabla)\mathbf{w}$$
The first part is
$$\begin{align}
(\mathbf{v}\cdot \nabla)\mathbf{r}&=\left( v_{x}\frac{ \partial  }{ \partial x } +v_{y}\frac{ \partial  }{ \partial y } +v_{z}\frac{ \partial  }{ \partial z }  \right)(x \hat{\mathbf{x}}+y \hat{\mathbf{y}}+z \hat{\mathbf{z}}) \\
&=v_{x}\hat{\mathbf{x}}+v_{y}\hat{\mathbf{y}}+v_{z}\hat{\mathbf{z}} \\
&=\mathbf{v}
\end{align}$$
The second part is essentially the same process as term one:
$$(\mathbf{v}\cdot \nabla)\mathbf{w}=\mathbf{v}(\mathbf{v}\cdot \nabla t_{r})$$
just instead of getting $\dot{\mathbf{v}}=\mathbf{a}$ we get $\dot{\mathbf{w}}=\mathbf{v}$. Combined we get:
$$(\mathbf{v}\cdot \nabla)\boldsymbol{\mathfrak{r}}=\mathbf{v}-\mathbf{v}(\mathbf{v}\cdot \nabla t_{r})\tag{Term 2}$$
Inside of term three:
$$\begin{align}
\nabla\times \mathbf{v}&=\left( \frac{ \partial v_{z} }{ \partial y } -\frac{ \partial v_{y} }{ \partial z }  \right)\hat{\mathbf{x}}+\left( \frac{ \partial v_{x} }{ \partial z } -\frac{ \partial v_{z} }{ \partial x }  \right)\hat{\mathbf{y}}+\left( \frac{ \partial v_{y} }{ \partial x } -\frac{ \partial v_{x} }{ \partial y }  \right)\hat{\mathbf{z}} \\
&=\left( \frac{ dv_{z} }{ dt_{r} } \frac{ \partial t_{r} }{ \partial y } - \frac{dv_{y}}{dt_{r}} \frac{ \partial t_{r} }{ \partial z }  \right)\hat{\mathbf{x}}+\left( \frac{dv_{x}}{dt_{r}}\frac{ \partial t_{r} }{ \partial z } - \frac{dv_{z}}{dt_{r}} \frac{ \partial t_{r} }{ \partial x } \right)\hat{\mathbf{y}}+\left( \frac{dv_{y}}{dt_{r}}\frac{ \partial t_{r} }{ \partial x } - \frac{dv_{x}}{dt_{r}}\frac{ \partial t_{r} }{ \partial y }  \right)\hat{\mathbf{y}} \\
&=-\mathbf{a}\times \nabla t_{r}
\end{align}$$
Inside of term four:
$$\nabla\times \boldsymbol{\mathfrak{r}}=\cancel{ \nabla \times \mathbf{r} }-\nabla\times \mathbf{w}=-\nabla\times \mathbf{w}=\mathbf{v}\times \nabla t_{r}\tag{4}$$
where we used the same logic as term three, just with $\mathbf{v}=\dot{\mathbf{w}}$ instead of $\mathbf{a}=\dot{\mathbf{v}}$. Put all of this back in $(3)$ and use $\mathbf{A}\times(\mathbf{B}\times \mathbf{C})=\mathbf{B}(\mathbf{A}\cdot \mathbf{C})-\mathbf{C}(\mathbf{A}\cdot \mathbf{B})$ on the triple products to get
$$\begin{align}
\nabla(\boldsymbol{\mathfrak{r}}\cdot \mathbf{v})&=\mathbf{a}(\boldsymbol{\mathfrak{r}}\cdot \nabla t_{r})+\mathbf{v}-\mathbf{v}(\mathbf{v}\cdot \nabla t_{r})-\boldsymbol{\mathfrak{r}}\times(\mathbf{a}\times \nabla t_{r})-\mathbf{v}\times(\mathbf{v}\times \nabla t_{r}) \\
&=\mathbf{a}(\boldsymbol{\mathfrak{r}}\cdot \nabla t_{r})+\mathbf{v}-\mathbf{v}(\mathbf{v}\cdot \nabla t_{r}) \\
&\quad-\mathbf{a}(\boldsymbol{\mathfrak{r}}\cdot \nabla t_{r})+\nabla t_{r}(\boldsymbol{\mathfrak{r}}\cdot \mathbf{a})+\mathbf{v}(\mathbf{v}\cdot \nabla t_{r})-\nabla t_{r}(\mathbf{v}\cdot \mathbf{v}) \\
&=\mathbf{v}+\nabla t_{r}(\boldsymbol{\mathfrak{r}}\cdot \mathbf{a})-\nabla t_{r}v^{2} \\
&=\mathbf{v}+(\boldsymbol{\mathfrak{r}}\cdot \mathbf{a}-v^{2})\nabla t_{r}
\end{align}$$
Put this and $\nabla \mathfrak{r}=-c\nabla t_{r}$ in the $\nabla V$ and you get
$$\nabla V=\frac{qc}{4\pi \varepsilon_{0}} \frac{1}{(\mathfrak{r}c-\boldsymbol{\mathfrak{r}}\cdot v)^{2}}[\mathbf{v}+(c^{2}-v^{2}+\boldsymbol{\mathfrak{r}}\cdot \mathbf{a})\nabla t_{r}]$$
We now need $\nabla t_{r}$. To do so, we'll use a trick to reverse engineer its value in terms. Recall that $\nabla \mathfrak{r}=-c\nabla t_{r}$, but $\mathfrak{r}=\lvert \boldsymbol{\mathfrak{r}} \rvert=\sqrt{ \boldsymbol{\mathfrak{r}}\cdot \boldsymbol{\mathfrak{r}} }$. We can use this to our advantage:
$$-c\nabla t_{r}=\nabla \mathfrak{r}=\nabla(\sqrt{ \boldsymbol{\mathfrak{r}}\cdot \boldsymbol{\mathfrak{r}} })=\frac{1}{2\sqrt{ \boldsymbol{\mathfrak{r}}\cdot \boldsymbol{\mathfrak{r}} }}\nabla(\boldsymbol{\mathfrak{r}}\cdot \boldsymbol{\mathfrak{r}})=\frac{1}{\mathfrak{r}}[(\boldsymbol{\mathfrak{r}}\cdot \nabla)\boldsymbol{\mathfrak{r}}+\boldsymbol{\mathfrak{r}}\times(\nabla\times \boldsymbol{\mathfrak{r}})]$$
Notice how $(\boldsymbol{\mathfrak{r}}\cdot \nabla)\boldsymbol{\mathfrak{r}}$ is something like term two, so it must be
$$(\boldsymbol{\mathfrak{r}}\cdot \nabla)\boldsymbol{\mathfrak{r}}=\boldsymbol{\mathfrak{r}}-\mathbf{v}(\boldsymbol{\mathfrak{r}}\cdot \nabla t_{r})$$
Meanwhile $\nabla\times \boldsymbol{\mathfrak{r}}$ is the inside of term four, which we've already established in $(4)$, so
$$\boldsymbol{\mathfrak{r}}\times(\mathbf{v}\times \nabla t_{r})=\mathbf{v}(\boldsymbol{\mathfrak{r}}\cdot \nabla t_{r})-\nabla t_{r}(\boldsymbol{\mathfrak{r}}\cdot\mathbf{v})$$
Thus
$$-c\nabla t_{r}=\frac{1}{\mathfrak{r}}[\boldsymbol{\mathfrak{r}}-\mathbf{v}(\boldsymbol{\mathfrak{r}}\cdot \nabla t_{r})+\mathbf{v}(\boldsymbol{\mathfrak{r}}\cdot \nabla t_{r})-\nabla t_{r}(\boldsymbol{\mathfrak{r}}\cdot\mathbf{v})]=\frac{1}{\mathfrak{r}}[\boldsymbol{\mathfrak{r}}-\nabla t_{r}(\boldsymbol{\mathfrak{r}}\cdot \mathbf{v})]$$
and so
$$\nabla t_{r}=\frac{-\boldsymbol{\mathfrak{r}}}{\mathfrak{r}c-\boldsymbol{\mathfrak{r}}\cdot \mathbf{v}}$$
Plug this into the gradient of $V$ and we finally get
$$\nabla V=\frac{1}{4\pi \varepsilon_{0}} \frac{qc}{(\mathfrak{r}c-\boldsymbol{\mathfrak{r}}\cdot \mathbf{v})^{3}}[(\mathfrak{r}c-\boldsymbol{\mathfrak{r}}\cdot \mathbf{v})\mathbf{v}-(c^{2}-v^{2}+\boldsymbol{\mathfrak{r}}\cdot \mathbf{a})\boldsymbol{\mathfrak{r}}]$$

A similar calculation leads to
$$\frac{ \partial \mathbf{A} }{ \partial t } =\frac{1}{4\pi \varepsilon_{0}} \frac{qc}{(\mathfrak{r}c-\boldsymbol{\mathfrak{r}}\cdot \mathbf{v})^{3}}\left[ (\mathfrak{r}c-\boldsymbol{\mathfrak{r}}\cdot \mathbf{v})\left( -\mathbf{v}+\frac{\mathfrak{r}\mathbf{a}}{c} \right)+ \frac{\mathfrak{r}}{c}(c^{2}-v^{2}+\boldsymbol{\mathfrak{r}}\cdot \mathbf{a})\mathbf{v} \right]$$
For brevity, we define the vector $\mathbf{u}\equiv c \hat{\boldsymbol{\mathfrak{r}}}-\mathbf{v}$, and combining these two yields the electric field:
$$\boxed{\mathbf{E}(\mathbf{r},t)=\frac{q}{4\pi \varepsilon_{0}} \frac{\mathfrak{r}}{(\boldsymbol{\mathfrak{r}}\cdot \mathbf{u})^{3}}
[(c^{2}-v^{2})\mathbf{u}+\boldsymbol{\mathfrak{r}}\times(\mathbf{u}\times \mathbf{a})]}$$
We are not done yet however, as we still lack the magnetic field. The curl of $\mathbf{A}$ is
$$\nabla\times \mathbf{A}=\frac{1}{c^{2}}\nabla\times(\nabla V\mathbf{v})=\frac{1}{c^{2}}[V(\nabla\times \mathbf{v})-\mathbf{v}\times(\nabla V)]$$
$\nabla\times \mathbf{v}$ is the inside of term three from before, $\nabla\times \mathbf{v}=-\mathbf{a}\times \nabla t_{r}$. Meanwhile, we also know the gradient $\nabla V$. Together:
$$\mathbf{B}=\nabla\times \mathbf{A}=- \frac{1}{c} \frac{q}{4\pi \varepsilon_{0}} \frac{1}{(\mathbf{u}\cdot \boldsymbol{\mathfrak{r}})^{3}}\boldsymbol{\mathfrak{r}}\times[(c^{2}-v^{2})\mathbf{v}+(\boldsymbol{\mathfrak{r}}\cdot \mathbf{a})\mathbf{v}+(\boldsymbol{\mathfrak{r}}\cdot \mathbf{u})\mathbf{a}]$$
Notice how similar the square brackets here are to the ones in the electric field formula. In fact, take the electric field's square brackets and expand the triple product as
$$[(c^{2}-v^{2})\mathbf{u}+(\boldsymbol{\mathfrak{r}}\cdot \mathbf{a})\mathbf{u}-(\boldsymbol{\mathfrak{r}}\cdot \mathbf{u})\mathbf{a}]$$
which is, evidently, *almost* identical; the only difference the usage of $\mathbf{u}$ instead of $\mathbf{v}$. This would be a problem, but recall that $\mathbf{u}=c \hat{\boldsymbol{\mathfrak{r}}}-\mathbf{v}$. When you take the [[vector product]] of this and $\boldsymbol{\mathfrak{r}}$, then the term $c \hat{\boldsymbol{\mathfrak{r}}}$ disappears since the vector product of two parallel vectors is zero, so $\boldsymbol{\mathfrak{r}}\times \mathbf{u}=\boldsymbol{\mathfrak{r}}\times(-\mathbf{v})$. We can use this fact to change all the $\mathbf{v}$ vectors inside of $\nabla\times \mathbf{A}$ into $-\mathbf{u}$ vectors, since they're all going through this vector product anyway. But this makes the square brackets *truly* identical, and so
$$\boxed{\mathbf{B}(\mathbf{r},t)=\frac{1}{c}\hat{\boldsymbol{\mathfrak{r}}}\times \mathbf{E}(\mathbf{r},t)}$$
The magnetic field of a point charge is *entirely* determined by its electric field and is always [[Orthogonality|perpendicular]] to both it and vector to the retarded position.

Let's analyze what we've gotten after all this work. The electric field is now made up of two terms. The second term vanishes is only nonzero if the particle accelerates. If it doesn't, we are left with
$$\mathbf{E}(\mathbf{r},t)=\frac{q}{4\pi \varepsilon_{0}} \frac{\mathfrak{r}}{(\boldsymbol{\mathfrak{r}}\cdot \mathbf{u})^{3}}
(c^{2}-v^{2})\mathbf{u}\qquad(\text{when }\mathbf{a}=0)$$
Furthermore, if the particle also does not accelerate, then $\mathbf{u}=c \hat{\boldsymbol{\mathfrak{r}}}$, so
$$\mathbf{E}(\mathbf{r},t)=\frac{q}{4\pi \varepsilon_{0}} \frac{\mathfrak{r}}{c^{3}(\mathfrak{\boldsymbol{\mathfrak{r}}}\cdot \hat{\boldsymbol{\mathfrak{r}}})^{3}}c^{3}\hat{\boldsymbol{\mathfrak{r}}}=\frac{q}{4\pi \varepsilon_{0}} \frac{\mathfrak{r}}{\mathfrak{r}^{3}}\hat{\boldsymbol{\mathfrak{r}}}=\frac{q}{4\pi \varepsilon_{0}} \frac{\hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}^{2}}\qquad(\text{when }\mathbf{v}=0)$$
but this is just the traditional field of a static point charge! Clearly, our field is here is a true generalization of the classical formula, to which it reduces in the static case. In fact, the first term, the one that appears when $\mathbf{a}=0$, is called the **velocity field** (or sometimes **generalized Coulomb field**). The second term is instead called the **acceleration field** (or sometimes **radiation field**). Analogous terminology is used for the magnetic field. Notably, the velocity field goes like $\sim \mathfrak{r}^{-2}$, but the acceleration field only goes like $\sim \mathfrak{r}^{-1}$, meaning it falls off much slower, but is only present for accelerating charges. This has important consequences, as it is this behavior that causes the acceleration field to generate **[[electromagnetic radiation]]**, hence its alternative name.

Due to its importance, we should calculate the velocity field in a more practical scenario. Imagine a point charge traveling at constant velocity (which implies a straight trajectory $\mathbf{w}=\mathbf{v}t$). We have $\mathbf{a}=0$ and the electric field reduces to the aforementioned
$$\mathbf{E}(\mathbf{r},t)=\frac{q}{4\pi \varepsilon_{0}} \frac{\mathfrak{r}}{(\boldsymbol{\mathfrak{r}}\cdot \mathbf{u})^{3}}
(c^{2}-v^{2})\mathbf{u}$$
We want to get rid of $\mathbf{u}$, so
$$\mathfrak{r}\mathbf{u}=c \boldsymbol{\mathfrak{r}}-\mathfrak{r}\mathbf{v}=c(\mathbf{r}-\mathbf{v}t_{r})-c(t-t_{r})\mathbf{v}=c(\mathbf{r}-\mathbf{v}t)$$

It can be found that%%do Example 10.3 and Problem 10.16 of Griffiths%%
$$\mathfrak{r}c-\boldsymbol{\mathfrak{r}}\cdot \mathbf{v}=\boldsymbol{\mathfrak{r}}\cdot \mathbf{u}=\sqrt{ (c^{2}t-\mathbf{r}\cdot \mathbf{v})^{2}+(c^{2}-v^{2})(r^{2}-c^{2}t^{2}) }$$
Defining $\mathbf{R}\equiv \mathbf{r}-\mathbf{v}t$, the vector from the *present* location $\mathbf{v}t$ of the charge to $\mathbf{r}$, this can be written as
$$\boldsymbol{\mathfrak{r}}\cdot \mathbf{u}=Rc\sqrt{ q-\frac{v^{2}}{c^{2}}\sin ^{2}\theta }$$
where $\theta$ is the angle between $\mathbf{R}$ and $\mathbf{v}$. Thus
$$\boxed{\mathbf{E}(\mathbf{r},t)=\frac{q}{4\pi \varepsilon_{0}} \frac{1- v^{2}/c^{2}}{(1-(v^{2}/c^{2})\sin ^{2}\theta)^{3/2}} \frac{\hat{\mathbf{R}}}{R^{2}}}$$
There's a few of things to notice here. The fields points over $\hat{\mathbf{R}}$, which is vector from the *present* position of the charge. This is curious because the potential here is the retarded one, not the present one. Furthermore, the presence of a $\sin ^{2}\theta$ term means that the intensity of the field depends on the orientation with respect to the charge. It is not spherically uniform any longer, being strongest at 90° angles and suppressed when on the line of motion of the particle.

![[Diagram Moving charge electric field lines]]

The field also depends on the ratio between particle speed and light speed, with faster moving charges being penalized by a factor $(1-v^{2}/c^{2})$ on the axis of motion. At 90° angles, on the other hand, the field is boosted by a factor $1/\sqrt{ 1-v^{2}/c^{2} }$.

As for the magnetic field, we have
$$\hat{\boldsymbol{\mathfrak{r}}}=\frac{\mathbf{r}-\mathbf{v}t_{r}}{\mathfrak{r}}=\frac{(\mathbf{r}-\mathbf{v}t)+(t-t_{r})\mathbf{v}}{\mathfrak{r}}=\frac{\mathbf{R}}{\mathfrak{r}}+ \frac{\mathbf{v}}{c}$$
and so
$$\boxed{\mathbf{B}(\mathbf{r},t)=\frac{1}{c^{2}}(\mathbf{v}\times \mathbf{E})}$$
The magnetic field inherits the orientation dependence from $\mathbf{E}$, being strongest when at a 90° angle from the particle.

When $v^{2}\ll c^{2}$, these approximately reduce to
$$\mathbf{E}(\mathbf{r},t)\simeq \frac{1}{4\pi \varepsilon_{0}} \frac{q}{R^{2}}\hat{\mathbf{R}},\qquad \mathbf{B}(\mathbf{r},t)\simeq \frac{\mu_{0}}{4\pi} \frac{q}{R^{2}}(\mathbf{v}\times \hat{\mathbf{R}})$$
which are the usual point charge electric field and a "point charge [[Biot-Savart law]]".

[^1]: please don't do this

[^2]: Speaking of, the phenomenon might remind you a lot of the [[Doppler effect]] and you'd be right: the principle is more or less the same. It does not however have any connection to special relativity, despite the similarity. It's just a matter of delays due to finite speeds.

[^3]: By contrast, for a wave that does not travel at the speed of light (say, sound), this is perfectly valid. You can absolutely exceed the speed of sound so it is possible to, for example, hear a single sound from two places at once so long as the *object moves faster the signal*. For instance, imagine a supersonic jet plane moving near you. You'll hear the sound coming from the sky from *behind* the plane, but also *from* the plane, since the jet is moving faster than the waves can reach you. You cannot, however, *see* the jet in both places because it cannot move faster than light. Also, yes, it *is* possible for a particle to travel at light speed, but it must be [[mass|massless]], something that was thought to be impossible when this theory was developed.

[^4]: It's also possible to do this starting from [[Jefimenko's equations]], but it's harder.
