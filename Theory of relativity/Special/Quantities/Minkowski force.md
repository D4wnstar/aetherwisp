---
wiki-publish: true
---

### Dynamics and derivation
Relativistic dynamics are essentially just a question of how many of [[Newton's laws]] survive the pilgrimage to relativity. The first law is built into the [[postulates of special relativity]], so that's easy enough. The second also survives as long as we use the relativistic momentum:
$$\mathbf{F}=\frac{d\mathbf{p}}{dt}$$
The behavior of forces in relativity (or rather, the trajectories they make) is a little weird however, but consistent.

> [!example]- Constant force
> Consider some particle of mass $m$. It is perpetually affected by a force $F$ over an axis of your preference. Assume it starts at the origin at time $t=0$. The force is
> $$F=\frac{dp}{dt}\quad\Rightarrow \quad p=Ft+p_{0}$$
> by simple integration. Since $p(t=0)=0$ then $p_{0}=0$. Thus we must have
> $$p=\frac{mv}{\sqrt{ 1-v^{2}/c^{2} }}=Ft$$
> Solving for $v$ gives us
> $$v=\frac{(F/m)t}{\sqrt{ 1+(Ft/mc)^{2} }}$$
> The numerator is what we'd get in classical physics. The denominator is essentially a different flavor of the relativistic gamma which prevents the velocity from exceeding the [[speed of light]]. Unsurprisingly, as time $t\to \infty$, then $v\to c$, as we'd imagine. To find the trajectory, we must integrate
> $$\begin{align}
> x(t)&=\frac{F}{m}\int_{0}^{t} \frac{t'}{\sqrt{ 1+(Ft'/mc)^{2} }}dt' \\
> &=\frac{mc^{2}}{F}\left.{\sqrt{ 1+(Ft'/mc)^{2} }}\right|_{0}^{t} \\
> &=\frac{mc^{2}}{F}\left(\sqrt{ 1-(Ft/mc)^{2} }-1\right)
> \end{align}$$
> In classical physics, we would've gotten a [[parabola]]. Here we get a [[hyperbola]] and the motion in general is often called **hyperbolic motion**. It happens in some situations of interest, such as when a [[Electric charge|point charge]] is set in a uniform [[electric field]].

[[Work]] is defined as usual
$$W=\int \mathbf{F}\cdot d\mathbf{r}$$
and the [[work-energy theorem]] still holds as long as you use the ordinary velocity $\mathbf{v}$:
$$W=\int \frac{d\mathbf{p}}{dt}\cdot d\mathbf{r}=\int \frac{d\mathbf{p}}{dt}\cdot \frac{d\mathbf{r}}{dt}dt=\int \frac{d\mathbf{p}}{dt}\cdot \mathbf{v}\ dt $$
Also
$$\frac{d\mathbf{p}}{dt}\cdot \mathbf{v}=\left( \frac{d}{dt} \frac{m\mathbf{v}}{\sqrt{ 1-v^{2}/c^{2} }} \right)\cdot \mathbf{v}=\frac{m\mathbf{v}}{(1-v^{2}/c^{2} )^{3/2}}\cdot \frac{d\mathbf{v}}{dt}=\frac{d}{dt} \left( \frac{mc^{2}}{\sqrt{ 1-v^{2}/c^{2} }} \right)=\frac{dE}{dt}$$
and so
$$W=\int \frac{dE}{dt}dt=E_\text{final}-E_\text{start}$$
So all is good with the second law.

The third law is... not doing great. Say some thing $A$ applies a force $\mathbf{F}(t)$ on another thing $B$, which responds with an equal and opposite reaction $-\mathbf{F}(t)$. The issue here is, as always, time. What is $t$? It's time as measured by a rest clock in $A$'s [[frame of reference]]. That's great for $A$, but if some observer in a different frame looks a this, they'll see broken physics: the reaction of $B$ occurs at a different time than the action of $A$. Why? Because [[Relativity of simultaneity|simultaneity is relative]], but the third law hinges on a unique definition of simultaneity. Thus, the third law is relativistically broken, only resisting in contact interactions, where no time is needed to carry the information, and constant forces that don't depend on time.

But not all is lost. Ordinary velocity is also "broken" in a similar manner, in that everything changes as soon as you change point of view. In fact, looking at a component off the axis $x$ of a [[Lorentz transformation]]
$$\bar{F}_{y}=\frac{d\bar{p}_{y}}{dt}=\frac{dp_{y}}{\gamma dt- \frac{\gamma \beta}{c}dx}=\frac{dp_{y}}{dt} \frac{1}{\gamma- \frac{\gamma \beta}{c} \frac{dx}{dt}}=\frac{F_{y}}{\gamma(1-\beta v_{x}/c)}$$
since, remember, $\gamma$ and $\beta$ are determined by the relative motion of the frames of reference (not the particle) and are therefore constant in time. Similarly for the $z$ component:
$$\bar{F}_{z}=\frac{F_{z}}{\gamma(1-\beta v_{x}/c)}$$
The component *on* the axis of transformation is that much worse:
$$\bar{F}_{x}=\frac{d\bar{p}_{x}}{dt}=\ldots=\frac{F_{x}- \frac{\beta}{c} \frac{dE}{dt}}{1-\beta v_{x}/c}$$
You can do the math yourself if you want proof. We do have the time derivative of $E$ thought, as we found it in the work-energy theorem above.
$$\bar{F}_{x}=\frac{F_{x}-\beta(\mathbf{v}\cdot \mathbf{F})/c}{1-\beta v_{x}/c}$$
These equations are ugly. There is *one* case in which this are sort of okay, and that's when the particle is (instantaneously) at rest from the point of view of the observer (i.e. in frame $\mathcal{S}$ instead of its own frame $\bar{\mathcal{S}}$). In this case, $\mathbf{v}=0$ and
$$\bar{\mathbf{F}}_{\perp}=\frac{\mathbf{F}_{\perp}}{\gamma},\qquad \bar{F}_{\parallel}=F_{\parallel}$$
which is to say that the component of $F$ parallel to the motion of $\bar{\mathcal{S}}$ is unchanged and the [[Orthogonality|perpendicular]] component just suffers a reduction by a factor $\gamma$. Either way, the relativistic force is not easy to deal with.

The mention of similarity to the ordinary velocity before was not random. In fact, just like how we "fixed" ordinary velocity by introducing proper velocity, we can do the same thing by defining a "proper force":
$$\boxed{K^{\mu}\equiv \frac{dp^{\mu}}{d\tau}}$$
This is called a **Minkowski force**. It is related to the ordinary force in the spatial part by
$$\mathbf{K}=\frac{d\mathbf{p}}{d\tau}=\frac{dt}{d\tau} \frac{d\mathbf{p}}{dt}=\frac{\mathbf{F}}{\gamma}$$
The zeroth component is
$$K^{0}=\frac{dp^{0}}{dt}=\frac{1}{c} \frac{dE}{d\tau}$$
with $dE/d\tau$ being a sort of "proper [[power]]" applied onto the force. Relativistic dynamics can be developed with both kinds of forces, each with their own benefits. The Minkowski force leads to much nicer calculations, but the ordinary force is what we actually control and what we want to end up with in our equations. As such, the ordinary force is often preferred despite the challenge.