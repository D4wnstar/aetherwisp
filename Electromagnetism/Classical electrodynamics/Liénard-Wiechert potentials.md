The **Liénard-Wiechert potentials** are *retarded* [[Electric potential|electric]] and [[Magnetic vector potential|magnetic vector potentials]] for a [[Electric charge|point charge]] $q$ moving on a specific trajectory. They are
$$V(\mathbf{r},t)=\frac{1}{4\pi \varepsilon_{0}} \frac{qc}{(\mathfrak{r}c-\boldsymbol{\mathfrak{r}}\cdot \mathbf{v})}$$
and
$$\mathbf{A}(\mathbf{r},t)=\frac{\mu_{0}}{4\pi} \frac{qc\mathbf{v}}{(\mathfrak{r}c+\boldsymbol{\mathfrak{r}}\cdot \mathbf{v})}=\frac{\mathbf{v}}{c^{2}}V(\mathbf{r},t)$$
$\mathbf{v}$ is the velocity of the charge at the [[retarded time]] and $\boldsymbol{\mathfrak{r}}$ is the distance between the retarded position (the position at the retarded time) to the field point $\mathbf{r}$.
### Derivation
The proof begins from the general for form of retarded potentials. The electric potential is
$$V(\mathbf{r},t)=\frac{1}{4\pi \varepsilon_{0}}\int \frac{\rho(\mathbf{r}',t_{r})}{\mathfrak{r}}\ d\tau'\tag{1}$$
where, critically, $\rho$ is dependent on the retarded time $t_{r}$. This form is almost identical to the simultaneous case, just with $t_{r}$ added in, which begs the suggestion that the solution might be the same
$$\frac{1}{4\pi \varepsilon_{0}} \frac{q}{\mathfrak{r}}$$
with the caveat that $\mathfrak{r}$ is now the distance from the *retarded* position instead of the current one. But that would be wrong, for the $t_{r}$ dependency in $\rho$ fundamentally changes what $\int \rho(\mathbf{r}',t_{r})d\tau'$ *is*. Whereas without $t_{r}$, $\rho(\mathbf{r}')$ refers to the charge distribution at *one instant*, with $t_{r}$ it is the charge distribution spread not just in space but also throughout time as the retardation, which leads to a distorted charge depending on how far you are from the origin.

It pays to describe this phenomenon with a more easily imagined object: a train. Say you're looking at a train that's coming towards you[^1]. Though you will not notice in the real world because it's so tiny, you will see the train as *longer* that if were standing to the side, or behind it. This is a fundamentally geometric effect due to the finite speed of light. The light from the back of the train was emitted earlier than the one we receive at the same time from the front, since the train is moving towards you. If the train were still, light would from the front and the back would not reach you at the same time, but since it's moving, by the time the light from the back reaches you, the train rolled forward and the light from the front emits from further on, which makes it take *less* time to reach you. This means that, at the same time, you see the *current* front of the train, but the *past* back. The train looks longer by an amount determined by how long it takes for light to get to you and the speed of the train.

![[Figure Retarded train length.png]]
*From Introduction to Electrodynamics, David J. Griffiths, 4ed., page 452*

If the past light from the back needs to travel a distance $L'$ at speed $c$ for it to reach you, in the meantime the train moves by a distance $L'-L$ at speed $v$. Since these two are equal we can state
$$\frac{L'}{c}=\frac{L'-L}{v}\quad\to \quad L'=\frac{L}{1-v/c}$$
The train looks longer by a factor $(1-v/c)^{-1}\geq1$. If the train were going away, it would look shorter by a factor $(1+v/c)^{-1}\leq 1$.

If instead you are at angle $\theta$ from the train, and it is far enough or short enough that the light beams from the front and back can be considered parallel, the past light from the back must instead travel $L'\cos \theta$ (and the train still moves the same distance $L'-L$), which yields
$$\frac{L'\cos\theta}{c}=\frac{L'-L}{v}\quad\to \quad L'=\frac{L}{1-(v\cos \theta)/c}$$
Same as before, the train is shortened, but we can see that only the component coming towards you (more formally, parallel to your line of sight) is significant, as shown by the cosine. The perpendicular component does not matter: if you are watching the train from the side ($\theta \simeq90°$), the distortion factor falls back to $1$ and you see no distortion. We can therefore generalize to from $v\cos \theta$ to $\hat{\boldsymbol{\mathfrak{r}}}\cdot \mathbf{v}$, where $\hat{\boldsymbol{\mathfrak{r}}}$ is the unit vector from the train to the observer. The *volume* of the train $\tau$, then, will be shrunk to a new volume $\tau'$ by a factor
$$\tau'=\frac{\tau}{1-\hat{\boldsymbol{\mathfrak{r}}}\cdot \mathbf{v}/c}\tag{2}$$

Back to electrodynamics, we can just change the object's volume $\tau$ to the total charge in the volume $q$. Thus, our integral $(1)$ then solves *almost* in the original way, but the charge $q$ is now modified by the same factor as seen in $(2)$:
$$V(\mathbf{r},t)=\frac{1}{4\pi \varepsilon_{0}}\int \frac{\rho(\mathbf{r}',t_{r})}{\mathfrak{r}}\ d\tau'=\frac{1}{4\pi \varepsilon_{0}} \frac{q'}{\mathfrak{r}}=\frac{1}{4\pi \varepsilon_{0}} \frac{1}{\mathfrak{r}} \frac{q}{1-\hat{\boldsymbol{\mathfrak{r}}}\cdot \mathbf{v}/c}$$
where $\mathbf{v}$ is now the velocity of the charge. It might be surprising that this correction is significant for a point charge also, since it has no volume, but the correction factor in $(2)$ actually makes no reference to the size of the train/charge/whatever, it only cares about the *velocity relative to the observer*. It is fair to say that anything that's moving must abide to this phenomenon[^2].

The retarded time for a point charge is determined by the equation
$$[\mathbf{r}-\mathbf{w}(t_{r})]=c(t-t_{r})$$
where $\mathbf{w}(t_{r})$ is the location of the charge at time $t_{r}$, the retarded position. The left side is the distance the signal must travel, whereas $t-t_{r}$ on the right is the time it take for it to do so. We can call $\boldsymbol{\mathfrak{r}}=\mathbf{r}-\mathbf{w}(t_{r})$ the distance from the retarded position to the point $\mathbf{r}$. This is important because it allows us to claim that there is only ever *one* point $\mathbf{w}(t_{r})$ in communication with $\mathbf{r}$ at any given time. In fact, if there were two different retarded times $t_{r_{1}}$ and $t_{r_{2}}$ (and associated positions) such that $\mathfrak{r}_{1}=c(t-t_{r_{1}})$ and $\mathfrak{r}_{2}=c(t-t_{r_{2}})$, the then we'd have $\mathfrak{r}_{1}-\mathfrak{r}_{2}=c(t_{r_{2}}-t_{t_{1}})$. But this implies that the average speed of the particle in the direction of $\mathbf{r}$ must be $c$. Even ignoring components in other directions, which could very well set the speed to be greater than $c$ — an impossibility on its own — no charged particle can ever travel at *exactly* $c$, so this is really impossible[^3]. Therefore, there can only every be one retarded time/position for any point $\mathbf{r}$. This is of import to our potential because it guarantees that it is unique everywhere:
$$\boxed{V(\mathbf{r},t)=\frac{1}{4\pi \varepsilon_{0}} \frac{qc}{(\mathfrak{r}c-\boldsymbol{\mathfrak{r}}\cdot \mathbf{v})}}$$
Similarly, since the current density is $\rho \mathbf{v}$, the vector potential is
$$\boxed{\mathbf{A}(\mathbf{r},t)=\frac{\mu_{0}}{4\pi} \frac{qc\mathbf{v}}{(\mathfrak{r}c-\boldsymbol{\mathfrak{r}}\cdot \mathbf{v})}=\frac{\mathbf{v}}{c^{2}}V(\mathbf{r},t)}$$

[^1]: please don't do this

[^2]: Speaking of, the phenomenon might remind you a lot of the [[Doppler effect]] and you'd be right: the principle is more or less the same. It does not however have any connection to special relativity, despite the similarity. It's just a matter of delays due to finite speeds.

[^3]: By contrast, for a wave that does not travel at the speed of light (say, sound), this is perfectly valid. You can absolutely exceed the speed of sound so it is possible to, for example, hear a single something from two places at once so long as the *object moves faster the signal*. For instance, imagine a supersonic jet plane moving near you. You'll hear the sound coming from the sky from *behind* the plane, but also *from* the plane, since the jet is moving faster than the waves can reach you. You cannot, however, *see* the jet in both places because it cannot move faster than light.
