---
wiki-publish: true
---
[[Electric field|Electric]] and [[Magnetic field|magnetic fields]] transform according to relativity too, although their exact behavior under a [[Lorentz transformation]] is more complicated than your average quantity. The transformation rules for an electromagnetic field are
$$\begin{align}
&E'_{x}=E_{x},&E'_{y}&=\gamma(E_{y}-vB_{z}),&E'_{z}&=\gamma(E_{z}+vB_{y}) \\
&B'_{x}=B_{x},&B'_{y}&=\gamma\left( B_{y}+ \frac{v}{c^{2}}E_{z} \right),&B'_{z}&=\gamma\left( B_{z}- \frac{v}{c^{2}}E_{y} \right)
\end{align}$$
where $v$ is the velocity of the new [[frame of reference]] with respect to the old one.
### Derivation
Within the context of relativity, through the knowledge that the electric field $\mathbf{E}$ and the magnetic field $\mathbf{B}$ are interrelated and of [[magnetism as a relativistic phenomenon]], we want to take the final step and explain $\mathbf{E}$ and $\mathbf{B}$ themselves in terms of relativity. Like most things in relativity, $\mathbf{E}$ and $\mathbf{B}$ are just the spatial parts of their respective [[Four-vector|four-vectors]] — or, that's what you'd hope, as that is *not* the case and the relativistic generalizations of the fields is quite a bit more complex.

To tackle the situation, we are to check how these two transform under a Lorentz transformation. To start, we need to lay the groundwork, which is to say we need to make some assumptions about how this *might* work and then check if it's true (experimentally or theoretically). We need to claim two things:
1. the [[electric charge]] is a [[relativistic invariant]]. It does not change under Lorentz transformation. A charge is a charge everywhere and anywhere.
2. the transformation rules are the same regardless of the origin of the fields. It does not matter how a field was created: stationary charge, straight moving charge, random motion in the core of the Sun, spinning particles in a cyclotron; it makes no difference. All fields should transform the same. If they don't, the field theory formulation must be dispensed with, as the fields are supposed to carry *all* information about electromagnetism on their own, without additional information (such as their origin).

We'll use a [[capacitor]] with surface charge densities $\pm \sigma_{0}$ as a test bench since it makes for rather simple electric fields (we'll assume that it is lying on its side so that its length $l$ lies on the $x$ axis). Assume we are observing the situation while at rest from a frame $\mathcal{S}_{0}$ in which the capacitor is also at rest. In this frame, its electric field is
$$E_{y}=\frac{\sigma_{0}}{\varepsilon_{0}}$$
The Lorentz transformation moves the capacitor to [[frame of reference]] $\mathcal{S}$ moving on the $x$ axis at a constant speed $v_{0}$ (relative to $\mathcal{S}_{0}$).

:::image
![[Diagram Moving capacitor relativity|80%]]
Note how the velocity $v_{0}$ moves the frame of reference to the *left*, which means that the capacitor effectively moves to the *right*.
:::

In fact, in $\mathcal{S}$, it makes a field
$$E_{y}=\frac{\sigma}{\varepsilon_{0}}$$
where $\sigma$ is the surface charge density on the plates of the capacitor. Actually, there's two densities, $\pm \sigma$, depending on whether you're looking at the top or bottom plate. Since $\mathcal{S}$ is moving, the length $l$ will be [[Length contraction|contracted]] by a factor $\gamma_{0}=1/\sqrt{ 1-v_{0}^{2}/c^{2} }$ compared to $\mathcal{S}_{0}$, in which the density (at rest) is $\sigma_{0}$, so $\sigma=\gamma_{0}\sigma_{0}$. Also due to the frame's motion, the charges are moving with speed $v_{0}$, so they'll create a surface [[Electric current|current]] density $\mathbf{K}_{\pm}$ and produce a magnetic field
$$\mathbf{K}_{\pm}=\mp \sigma v_{0}\hat{\mathbf{x}}$$
The field points in the negative $z$ direction (use the right hand rule!) and has magnitude
$$B_{z}=-\mu_{0}\sigma v_{0}$$
as per [[Ampere's law]]. This is the situation in $\mathcal{S}$. In another frame $\mathcal{S}'$, moving at a constant velocity $v$ relative to $\mathcal{S}$, the observed fields will be
$$E_{y}'=\frac{\sigma'}{\varepsilon_{0}},\qquad B_{z}'=-\mu_{0}\sigma'v'$$
where $v'$ is the velocity of $\mathcal{S}'$ relative to $\mathcal{S}_{0}$, as per the [[Postulates of special relativity|Einstein velocity addition rule]]:
$$v'=\frac{v+v_{0}}{1+vv_{0}/c^{2}}$$
The quantity $\sigma'=\gamma'\sigma_{0}$ is weighed by $\gamma'=1/\sqrt{ 1-v'^{2}/c^{2} }$. To find the general transformation rule, we want to express the quantities of $\mathcal{S}'$ in terms of those of $\mathcal{S}$ (i.e. from a general moving system to another general moving system). Using
$$\sigma'=\gamma' \sigma_{0},\quad\sigma=\gamma_{0}\sigma_{0},\quad\Rightarrow \quad \sigma'=\frac{\gamma'}{\gamma_{0}}\sigma$$
we can write
$$E'_{y}=\frac{\gamma'}{\gamma_{0}} \frac{\sigma}{\varepsilon_{0}},\quad B'_{z}=- \frac{\gamma'}{\gamma_{0}}\mu_{0}\sigma v'$$
The ratio of gammas is
$$\frac{\gamma'}{\gamma_{0}}=\frac{\sqrt{ 1-v_{0}^{2}/c^{2} }}{\sqrt{ 1-v'^{2}/c^{2} }}=\frac{1+vv_{0}/c^{2}}{\sqrt{ 1-v^{2}/c^{2} }}=\gamma\left( 1+ \frac{vv_{0}}{c^{2}} \right)$$
where, intuitively, $\gamma=1/\sqrt{ 1-v^{2}/c^{2} }$. Thus, inverting the field relations to express one field in terms of the other:
$$B_{z}=-\mu_{0}\sigma v_{0}=- \frac{\sigma v_{0}}{c^{2}\varepsilon_{0}}\quad\Rightarrow \quad \frac{\sigma}{\varepsilon_{0}}=- \frac{c^{2}B_{z}}{v_{0}}=E_{y}$$
to express the fields in $\mathcal{S}'$ in terms of the fields in $\mathcal{S}$:
$$E'_{y}=\gamma\left( 1+ \frac{vv_{0}}{c^{2}} \right) \frac{\sigma}{\varepsilon_{0}}=\gamma\left( E_{y}- vB_{z} \right)$$
and
$$B'_{z}=-\gamma\left( 1+ \frac{vv_{0}}{c^{2}} \right)\mu_{0}\sigma\left( \frac{v+v_{0}}{1+vv_{0}/c^{2}} \right)=\gamma\left( B_{z}- \frac{v}{c^{2}}E_{y} \right)$$
These are the transformation rules for $E_{y}$ and $B_{z}$. To find the other components, we just align the capacitors on different axes. Say the capacitor is now standing up vertical on the $xy$ plane instead of laying flat on the $xz$ plane like in the image, the fields in $\mathcal{S}$ would be
$$E_{z}=\frac{\sigma}{\varepsilon_{0}},\qquad B_{y}=\mu_{0}\sigma v_{0}$$
(the only practical change is the direction of the magnetic field and that the contracted length is $w$ instead of $l$). The rest of the formulas run the same and we get
$$E_{z}'=\gamma(E_{z}+vB_{y}),\qquad B_{y}'=\gamma\left( B_{y}+ \frac{v}{c^{2}}E_{z} \right)$$
Finally, if we make the capacitor stand up on the $yz$ axis, then little happens. This is because the contracted length here is the distance between plates, but since the electric field doesn't depend on it, nothing changes:
$$E_{x}'=E_{x}$$
In this case, there is no magnetic field, so we can't figure out the transformation of $B_{x}$ from this system. What we can do is use a different electrical component altogether: a long solenoid centered on the $x$ axis at rest in $\mathcal{S}$.

![[Diagram Resting solenoid relativity|80%]]


The field of a resting solenoid with $n$ turns per unit length is
$$B_{x}=\mu_{0}nI$$
When moving at speed $v$ in $\mathcal{S}'$, the turns per unit length become denser as per $n'=\gamma n$. However, we also need to care about [[time dilation]] on the electric current, since it is charge per unit *time*:
$$I'=\frac{I}{\gamma}$$
All in all, these two factors cancel and we get
$$B'_{x}=B_{x}$$
Putting all of these transformations together finally gives us
$$\boxed{\begin{align}
&E'_{x}=E_{x},&E'_{y}&=\gamma(E_{y}-vB_{z}),&E'_{z}&=\gamma(E_{z}+vB_{y}) \\
&B'_{x}=B_{x},&B'_{y}&=\gamma\left( B_{y}+ \frac{v}{c^{2}}E_{z} \right),&B'_{z}&=\gamma\left( B_{z}- \frac{v}{c^{2}}E_{y} \right)
\end{align}}\tag{1}$$
The fields are only transformed in directions [[Orthogonality|perpendicular]] to motion (the opposite of distance contraction).

Interestingly, even we observe *no* fields at a given point in $\mathcal{S}$, $\mathbf{E}=0$ and $\mathbf{B}=0$ in $\mathcal{S}$, we *still* observe something at that same point in $\mathcal{S}'$:
$$\boxed{\mathbf{E}'=\mathbf{v}\times \mathbf{B}',\quad \mathbf{B}'=- \frac{1}{c^{2}}(\mathbf{v}\times \mathbf{E}')}$$
The fields "exist" for one observer but not for another, and in the new system they are related by these [[Vector product|vector products]].