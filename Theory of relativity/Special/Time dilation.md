---
wiki-publish: true
---
**Time dilation** is the phenomenon where the duration of a phenomenon increases if it occurs while moving relative to the observer. In other words, time passes slower for things that move (compared to the observer). For instance, if a stationary (with respect to the observer) kettle takes one minute to boil water, a moving kettle will take more than a minute to boil the water. If $\Delta t_\text{rest}$ is a duration measured by a clock at rest and $\Delta t_\text{moving}$ is the same duration measured by a moving clock
$$\Delta t_\text{moving}=\gamma\Delta t_\text{rest}$$
where $\gamma$ is the [[Lorentz transformation|relativistic]] gamma. The moving time is dilated by a factor $\gamma$.
### Thought experiment
Imagine a train cart traveling at some constant speed along a smooth, straight track. In the center of the cart, a light bulb is attached to the ceiling, initially off. Imagine someone turns on the bulb. The light takes some time to reach the floor of the cart. What is this time? For someone on the train, everything is at rest, so the time is exactly the amount of time $\Delta t_{\text{rest}}$ it takes for the light, traveling at the [[speed of light]] $c$, to traverse the height $h$ of the cart,
$$\Delta t_{\text{rest}}=\frac{h}{c}$$
where "rest" denotes that we are in the [[frame of reference]] of the cart and the light is at rest with respect to the observer. On the other hand, for someone on the ground, the space to travel is greater, as it is the diagonal between the location of the bulb when the light is emitted and the location of the floor after the light has traveled.

![[Diagram Time dilation thought experiment|100%]]

The train, which assume moves at speed $v$, travels some distance $v\Delta t$ while the light reaches the ground. Thus, the actual distance covered is given by the [[Law of cosines|Pythagorean theorem]], $\sqrt{ h^{2}+(v\Delta t_\text{moving})^{2} }$, and so
$$\Delta t_\text{moving}=\frac{\sqrt{ h^{2}+(v\Delta t_\text{moving})^{2} }}{c}$$
Extracting $\Delta t_\text{moving}$ yields
$$\Delta t_\text{moving}=\frac{h}{c} \frac{1}{\sqrt{ 1-v^{2}/c^{2} }}$$
By defining the parameter
$$\gamma\equiv \frac{1}{\sqrt{ 1-v^{2}/c^{2} }}$$
and substituting $\Delta t_\text{rest}$, the ground-observed (moving) time is related to train-observed (rest) time by
$$\boxed{\Delta t_\text{moving}=\gamma \Delta t_\text{rest}}$$
Seeing how $\gamma\geq 1$, we can make we can see that the ground time $\Delta t_\text{moving}$ must be *longer* than the train time by a factor $\gamma$: we call this **time dilation**.

> [!info] Time dilation
> Movement stretches durations of time. An event that lasts a minute at rest will last more than a minute when moving from the perspective of a stationary observer.
### From Lorentz transformations
Time dilation can be seen by applying a [[Lorentz transformation]]. Say an observer in a frame of reference $\mathcal{S}$ at time $t=0$ reads several clocks moving in a different frame of reference $\mathcal{S}'$. The observer finds that the clocks all read different times, depending on their location. The Lorentz transformation in time is
$$t'=-\gamma \frac{v}{c^{2}}x$$
Evidently, the clocks at positive $x$ will be behind, whereas those at negative $x$ will be ahead. Only the clock at $x=0$ (and so $t'=0$) matches the time of the stationary clocks in $\mathcal{S}$. Thus, moving clocks becomes desynchronized from each other and only stationary clocks can be trusted to share correctness. You can do the same exact argument in the reverse direction by doing the inversion transformation
$$t=\gamma \frac{v}{c^{2}}x'$$
only now the time discrepancy works in reverse due to the change in sign.

Say now the observer in $\mathcal{S}$ looks only at a clock that is at rest in $\mathcal{S}'$ at some position $x'=a$ and watches it over a time interval $\Delta t=t_\text{end}-t_\text{start}$. Since $x'$ is fixed (the clock is at rest within its frame, and thus moving at $v$ in $\mathcal{S}$), then the time transformation
$$t=\gamma\left( t'+ \frac{v}{c^{2}}a \right)$$
gives
$$\Delta t=t_\text{end}-t_\text{start}=\gamma\left( t'_\text{end}- \frac{v}{c^{2}}a \right)- \gamma\left( t'_\text{start}- \frac{v}{c^{2}}a \right)=\gamma(t'_\text{end}-t'_\text{start})=\gamma \Delta t'$$
or
$$\Delta t'=\frac{\Delta t}{\gamma}$$
which is the time dilation formula, where $\Delta t\equiv \Delta t_\text{moving}$ (since the clock is moving in $\mathcal{S}$) and $\Delta t'\equiv \Delta t_\text{rest}$ (since the clock is at rest in $\mathcal{S}'$).