---
wiki-publish: true
---
**Length contraction** is the phenomenon where the length of an object decreases if the object moves with respect to the observer. For instance, if a stationary (with respect to the observer) plank of wood is one meter long, a moving plank of wood will be less than a meter long. If $\Delta x_\text{rest}$ is the length of an object at rest and $\Delta x_\text{moving}$ is the length of the same object while moving:
$$\Delta x_\text{moving} = \frac{\Delta x_\text{rest}}{\gamma}$$
where $\gamma$ is the [[Lorentz transformation|relativistic]] gamma. The moving length is contracted by a factor $1/\gamma$. Contraction only occurs on the axis of motion. Lengths perpendicular to the axis of motion are not contracted.
### Thought experiment
Imagine a train cart traveling at some constant speed along a smooth, straight track. On one end, there is a lamp. On the other, a mirror, so that the lamp's light can be reflected back. How long does the light take to make a round trip? For someone on the train, the light takes
$$\Delta t_\text{rest}=2 \frac{\Delta x_\text{rest}}{c}\quad\text{or}\quad \Delta x_\text{rest}=\frac{c\Delta t_\text{rest}}{2}\tag{1}$$
where "rest" denotes that we are in the [[frame of reference]] of the cart and $\Delta x_\text{rest}$ is the rest length of the cart. To someone on the ground, the motion of the train changes the distances that need to be covered.

![[Diagram length contraction thought experiment|100%]]

When the light is emitted, the light must cover the length of the train $\Delta x_\text{moving}$, plus the distance $v\Delta t_{\text{moving},1}$ that the train moves in that time interval $\Delta t_{\text{moving},1}$. When it comes back, it must again travel the length of the train $\Delta x_\text{moving}$ *minus* the distance $v\Delta t_{\text{moving},2}$ the train moves in that time interval $\Delta t_{\text{moving},2}$. So:
$$\Delta t_{\text{moving},1}=\frac{\Delta x_\text{moving}+v\Delta t_{\text{moving},1}}{c},\qquad \Delta t_{\text{moving},2}=\frac{\Delta x_\text{moving}-v\Delta t_{\text{moving},2}}{c}$$
Solving for intervals:
$$\Delta t_{\text{moving},1}=\frac{\Delta x_\text{moving}}{c-v},\qquad \Delta t_{\text{moving},2}=\frac{\Delta x_\text{moving}}{c+v}$$
So the whole round trip takes
$$\Delta t_\text{moving}=\Delta t_{\text{moving},1}+\Delta t_{\text{moving},2}=\frac{2}{c} \Delta x_\text{moving} \frac{1}{1-v^{2}/c^{2}}=\gamma ^{2} \frac{2}{c}\Delta x_\text{moving}$$
Train-time and ground-time are related by [[time dilation]] according to $\Delta t_\text{moving}=\gamma \Delta t_\text{rest}$ so, rearranging to extract $\Delta x_\text{moving}$,
$$\Delta x_\text{moving}=\frac{c}{2\gamma ^{2}}\Delta t_\text{moving}=\frac{c}{2\gamma ^{2}}\gamma \Delta t_\text{rest}=\frac{c\Delta t_\text{rest}}{2\gamma}$$
but this is just $(1)$ so
$$\boxed{\Delta x_\text{moving}=\frac{\Delta x_\text{rest}}{\gamma}}$$
Since $\gamma\geq 1$, we can make we can see that the ground length $\Delta x$ must be *shorter* than the train length by a factor $\gamma$: we call this **length contraction** (or **Lorentz contraction**):

> [!info] Length contraction
> Movement compresses lengths. An object that is a meter long at rest will be less than a meter long when moving from the perspective of a stationary observer.

To clarify, length contraction occurs only on the axis of movement. To recognize why, here's another though experiment. Say we build a wall next to the railroad tracks. One meter above the rails, as measured from the ground, we paint a horizontal blue line. When the train passes, a passenger sticks out the window and paints a horizontal red line on the wall one meter from the ground, as measured from the train. Do the lines overlap or is one above the other? Well, if they didn't overlap, it would depend on the observer. The ground observer would say that the red line is lower, because train distances (and therefore the painted height) contract. Similarly, the train observer would say that the blue line is lower, because ground distances (and therefore the painted height) contract. So who's right? Well, *neither*, because it is not logically possible for the red line to be simultaneously below the blue one. No amount of [[relativity of simultaneity]] can fix this. Thus, we must conclude that the lines *overlap* and therefore height (and distances perpendicular to motion in general) are not contracted.
### From Lorentz transformations
Length contraction can be seen by applying a [[Lorentz transformation]]. Imagine a metal pipe is at rest in some inertial frame $\mathcal{S}'$ and is being observed by an observer in another frame $\mathcal{S}$, who therefore sees it moving at a constant speed $v$ (say, on the $x$ axis). The rest length of the pipe (the length measured in $\mathcal{S}'$) is $\Delta x'=x'_{r}-x_{l}'$, where $x_{r}'$ and $x_{l}'$ denote the left and right ends of the pipe. Measuring the length in $\mathcal{S}$ would require the observer to measure the two ends $x_{r}$ and $x_{l}$ simultaneously at a moment of *his* time $t$, so that we get $\Delta x=x_{r}-x_{l}$. Using applying the Lorentz transformation on $x$ gives
$$\Delta x'=x'_{r}-x'_{l}=\gamma(x_{r}-vt)-\gamma(x_{l}-vt)=\gamma(x_{r}-x_{l})=\gamma \Delta x$$
and hence
$$\Delta x'=\gamma \Delta x$$
which is the length contraction formula.