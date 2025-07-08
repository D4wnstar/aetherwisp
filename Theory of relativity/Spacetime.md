---
wiki-publish: true
aliases:
  - Minkowski space
  - spacelike
  - timelike
  - lightlike
  - light cone
---
**Spacetime** is a mathematical model to simultaneously describe the three spatial dimensions and one temporal dimension of the Universe, in a single four-dimensional space.

In the absence of [[Gravitational interaction|gravity]], spacetime is described by a **Minkowski space**, which is a [[metric space]] equipped with a [[scalar product]], described by the [[metric tensor]], used to describe the concept of distance in spacetime. In the presence of gravity, it is necessary to use general relativity.

An [[event]] $a$ that occurs at some time $t$ in history and in some location $(x,y,z)$ in space is a point in spacetime, specifically the [[four-vector]] $a=(t,x,y,z)$. All objects move in spacetime, if only because of the inexorable advance of time. The trajectory drawn by an object in spacetime is called a [[world line]].
### Causality
Causality between two events in spacetime can be described by the sign of the metric. Consider a four-vector $a$. Its [[norm]] is
$$a^{\mu}a_{\nu}=-(a^{0})^{2}+(a_{1})^{2}+(a^{2})^{2}+(a^{3})^{2}$$
and unlike the usual norm, it can be positive, negative, or zero. This is most important when the four-vector represents the spacetime difference between two events, as we'll see below. The difference between positive, negative and null cases is critical to understanding [[causality]] and how any two events are related to each other. The three cases are given special names:
- positive norms are said to be **spacelike**;
- negative norms are said to be **timelike**;
- null norms are said to be **lightlike**.

To see why these names make sense, consider the **[[displacement four-vector]]**, which is the spacetime distance between two events $A=(x^{0}_{A},x_{A}^{1},x_{A}^{2},x_{A}^{3})$ and $B=(x_{B}^{0},x_{B}^{1},x_{B}^{2},x_{B}^{3})$ in spacetime:
$$\Delta x^{\mu}=x_{A}^{\mu}-x_{B}^{\mu}$$
Its norm is called the **invariant interval**:
$$I=\Delta x^{\mu}\Delta x_{\mu}=-c^{2}t^{2}+d^{2}$$
where $t$ is the temporal difference between events (how far apart in history they happen) and $d$ is the spatial distance (how distance the places they happen in are). Since norms are [[relativistic invariant|relativistic invariants]], when you change between different [[Frame of reference|inertial frames]] through a [[Lorentz transformation]] the invariant interval does not change. In other words, the time of occurrence might change, the spatial location might change, but their combined interval does *not*. Its in this invariant interval that the naming scheme shows its worth:
1. **Spacelike** ($I>0$): the events in different places but possibly at the same time. There is no valid Lorentz transformation to a frame in which these occur in the same place, as the condition for $I>0$ to be true requires the speed required to go from one another before they both happen to be higher than light ($d/t>c$). These events are *not causally linked*, since a single observer would need to exceed the speed of light to experience them both as they happen. There is however a transformation to have them happen at the same time.
2. **Timelike** ($I<0$): the events do not occur at the same time but may occur in the same place. There is always a valid Lorentz transformation to a frame in which they occur in the same place, for one can just travel from one to the other at speed $d/t<c$ to be there in time. As such, the events are *causally linked*, since a single observer can experience them in sequence. There is however *no* transformation to have them happen at the same time.
3. **Lightlike** ($I=0$): the events are technically causally linked (timelike) but only by something moving at the speed of light. Anything slower and they become spacelike.
#### The light cone
In abstract, its fair to have a hard time grasping what any of this means. Fortunately, we have a conventional way of drawing these concepts graphically in a figure known as a **Minkowski diagram**, which you can see below. It is a plot in space and time, drawn using 1D space to make a 2D plot. Any [[curve]] in this graph is a world line.

![[Diagram Light cone|100%|center]]

The [[cone]] drawn in blue and centered in the origin and is called a **light cone**. The origin itself is an event which we consider to be "us", the observers at some time in history and some place in the world. The edges of the cone are given by the world lines $x=\pm ct$, that is, the world lines of an object moving at the speed of light[^1]. Anything *inside* the cone is causally linked to the observer, as the origin can be connected to any event in the cone by a world line that does not require faster-than-light speeds. Once you reach the edge, you need to be going at *exactly* the speed of light for causality to hold. Once we you go outside the cone, any event there is causally detached from the observer: a signal would need to travel at a (very unphysical) faster-than-light speed to convey information from one to the other. As a consequence, the inside and outside regions of the cone are also given special names: the $t>0$ part inside the cone is called the **future**, the locus of all points you can access from that point on; the $t<0$ part inside the cone is called the **past**, the locus of all points you could've come from; the $t=0$ line is called the **present**, the slice of spacetime of all things that are happening alongside you; and the outside of the cone doesn't really have a name; here I called it **elsewhere**.
#### Geometry
This geometric explanation of how motion in spacetime works goes much deeper, but compared to regular space, it is *weird*. The root cause is the presence of an odd minus sign associated with the time coordinate in spacetime. This single sign fundamentally alters the geometry of spacetime to be *hyperbolic* instead of *circular* as we're used to. Whenever a constant value is set to be [[Rotation|rotated]] in usual space, it draws a [[circle]] of radius equal to that value. Whenever a constant value (say, the invariant interval) is set to be Lorentz transformed in spacetime, it draws a *[[hyperbola]]*. More generally, when another space axis is included, it draws a *[[hyperboloid]] of revolution*. When the value is negative (timelike), it is a hyperboloid of two sheets, when positive (spacelike) it is a hyperboloid of one sheet, and when zero (lightlike) it is a double cone (reminds you of something?). In fact, what a Lorentz transformation does is essentially just change the coordinates on the surface of the hyperboloid, but it cannot move something on or off that hyperboloid (or from one sheet to the other). This is why a Lorentz transformation is, geometrically speaking, "just" a hyperbolic rotation. The angle of this rotation is the **[[rapidity]]**.
### Reference frames
In an experiment, two fundamental reference frames are used:
1. The laboratory reference frame is fixed to the observer (and to the [[Detector|detectors]]). It is the one used when a [[Particle]] collides with a fixed target.
2. The [[center of mass]] reference frame is the frame for which the sum of the momenta of the colliding particles is zero: $\sum\vec{p}=0$.

Considering the [[four-momentum|four-momenta]] for two particles (or a target), we have for the laboratory
$$\begin{cases}
p_{1} = (E_{1},\vec{p}_{1})  \\
p_{2} = (M_{2},0)
\end{cases} \quad \Rightarrow \quad p_{tot,lab}=(E_{1}+M_{2},\vec{p}_{1})$$
and for the center of mass
$$\begin{cases}
p_{1}=(E_{1},\vec{p})  \\
p_{2}=(E_{2},-\vec{p})
\end{cases} \quad \Rightarrow \quad p_{tot,CM}=(E_{1}+E_{2},0)$$
In the case of $n$ particles, we have $p_{tot,CM}=(\sum E_{i},0)$. In particular, we have $p_{tot,CM}=(\sqrt{s},0)$, where $\sqrt{s}$ is the [[center-of-mass energy]].

By applying the [[Lorentz transformation|Lorentz transformations]] to the laboratory system, we can find how energy and momentum are related. For example, transforming along $x$ from lab to CM:
$$\begin{pmatrix}\sqrt{s} \\ 0 \\ 0 \\ 0 \end{pmatrix}=g_{\mu\nu}\begin{pmatrix}\sum\limits_{k}E_{k} \\ \sum\limits_{k}p_{k} \\ 0 \\ 0\end{pmatrix} \quad \Rightarrow \quad \beta=\frac{\sum\limits_{k}p_{k}}{\sum\limits_{k}E_{k}}= \frac{p_{tot,lab}}{E_{tot,lab}};\quad \gamma=\frac{E_{tot,lab}}{\sqrt{s}}$$
If instead we apply a transformation on $z$ from lab to CM:
$$\begin{pmatrix}E \\ p_{x} \\ p_{y} \\ p_{z}\end{pmatrix}_{LAB}=\begin{pmatrix}E \\ p\sin\theta\cos\varphi \\ p\sin\theta\sin\varphi \\ p\cos\theta\end{pmatrix}_{LAB}=\begin{pmatrix}\gamma & 0 & 0 & \beta\gamma \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ \beta \gamma & 0 & 0 & \gamma\end{pmatrix}\begin{pmatrix}E^{*} \\ p^{*}\sin\theta^{*}\cos\varphi^{*} \\ p^{*}\sin\theta^{*}\sin\varphi^{*} \\ p^{*}\cos\varphi^{*}\end{pmatrix}$$
from which
$$\begin{pmatrix}E \\ p\sin\theta\cos\varphi \\ p\sin\theta\sin\varphi \\ p\cos\theta\end{pmatrix}_{LAB}=\begin{pmatrix}E^{*}\gamma+\beta\gamma p^{*}\cos\theta^{*} \\ p^{*}\sin\theta^{*}\cos\varphi^{*} \\ p^{*}\sin\theta^{*}\sin\varphi^{*} \\ \beta\gamma E^{*}+\gamma p^{*}\cos\theta^{*}\end{pmatrix}_{CM}$$
from which it is seen $p_{T}=p\sin\theta=p^{*}\sin\varphi^{*}$, i.e., the *transverse momentum* is conserved, which is therefore a [[relativistic invariant]] for a transformation along $z$, as well as $\varphi=\varphi^{*}$ the *azimuthal angle*.

[^1]: If you want a fancier geometric definition, it is the locus of points on the plane of all light-like events.
