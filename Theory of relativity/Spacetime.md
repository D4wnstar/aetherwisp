---
aliases:
  - Minkowski space
  - space-like
  - time-like
  - light-like
---
**Spacetime** is a mathematical model to simultaneously describe the three spatial dimensions and one temporal dimension of the Universe, in a single four-dimensional space.

In the absence of [[Gravitational interaction|gravity]], spacetime is described by a **Minkowski space**, which is a [[metric space]] equipped with a [[scalar product]], described by the [[metric tensor]], used to describe the concept of distance in spacetime. In the presence of gravity, it is necessary to use general relativity.

An [[event]] $a$ that occurs at some time $t$ in history and in some location $(x,y,z)$ in space is a point in spacetime, specifically the [[four-vector]] $a=(t,x,y,z)$. All objects move in spacetime, if only because of the inexorable advance of time. The trajectory drawn by an object in spacetime is called a [[world line]].
### Causality
Causality between two events in spacetime can be described by the sign of the metric. Consider two events $a^{\mu}=(t^{1},\mathbf{r}^{1})$ and $a_{\nu}=(t_{2},\mathbf{r}_{2})$. Their scalar product is
$$a^{\mu}a_{\nu}=-(a^{0})^{2}+(a_{1})^{2}+(a^{2})^{2}+(a^{3})^{2}$$
and it can be positive, negative, or zero. The difference is critical to understanding causality and they are given special names:
- positive products are said to be **space-like**;
- negative products are said to be **time-like**;
- null products are said to be **light-like**.

To see why these make any sense, consider the **displacement four-vector**, which is just the *spatial* distance between two events $A=(t_{1},x_{1},y_{1},z_{1})$ and $B=(t_{2},x_{2},y_{2},z_{2})$ in spacetime:
$$\Delta a^{\mu}=a_{A}^{\mu}-x_{B}^{\mu}$$
The product of the displacement of two *different* four vectors is known as the **invariant interval**:
$$I=(\Delta x^{\mu})(\Delta x_{\mu})$$
These intervals inherit the same naming scheme above, but with important meaning:
1. $I>0$: we have $t_{1}=t_{2}$, i.e. the events occur at the same time but are spatially separated. These events are *not* causally linked: two simultaneous events cannot possibly cause one another. Since they are separated in space, but not time, they are called **space-like events**.
2. $I<0$: the events do not occur at the same time (although possibly in the same place) and are causally linked. Since they are separated in time, they are called **time-like events**.
3. $I=0$: the events are causally connected in a very specific way, wherein only something moving at the speed of light can transfer information between the two. Because of this, they are called **light-like events**. Anything slower and they become space-like.
#### The light cone
In abstract, its fair to have a hard time grasping what any of this means. Fortunately, we have a conventional way of drawing these concepts graphically in a figure known as a **light cone**, which you can see below. It is a plot in space and time, drawn using 1D space to make a 2D plot. Any [[curve]] in this graph is a world line.

![[Diagram Light cone|100%|center]]

The cone itself (here drawn in blue), is a two-sided cone, centered in the origin. The origin itself is an event which we consider to be "us", the observers at some time in history and some place in the world. The edges of the cone are given by the world lines $x=\pm ct$, that is, the world lines of an object moving at the speed of light[^1]. Anything *inside* the cone is causally bound to the observer, as the origin can be connected to any event in the cone by a world line that does not require faster-than-light speeds. Once you reach the edge, you need to be going at *exactly* the speed of light for causality to hold. Once we you go outside the cone, any event there is causally detached from the observer: a signal would need to travel at (very unphysical) faster-than-light speeds to convey information from one to the other. As a consequence, the inside and outside regions of the cone are also given special names: the $t>0$ inside part of the cone is called the **future**, the $t<0$ inside part is called the **past** and the outside is simply called **elsewhere**.

We can see the previously mentioned scenarios here too: any event in the future or past is happening at different times. These are time-like events, with the edge case being events exactly on the vertical time axis, which also occur in the same location. Any event on the horizontal space axis is happening simultaneously to the observer, but in a different location. These are space-like events. The edges of the cone instead contain all light-like events.
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

---

Lo **spaziotempo** è un modello matematico per descrivere simultaneamente le tre dimensioni spaziali e l'una temporale dell'Universo, rendendolo quindi uno spazio in quattro dimensioni.

In assenza di [[Interazione gravitazionale|gravitazione]], lo spaziotempo è descritto da uno **spazio di Minkowski**, che è uno [[spazio metrico]] che ammette un [[Scalar product]], detto [[Metric tensor]], usato per descrivere il concetto di distanza nello spaziotempo. In presenza di gravitazione, bisogna fare uso della relatività generale.

Un evento accaduto in qualche momento della storia in qualche luogo dello spazio è semplicemente un punto nello spaziotempo. Tutti gli oggetti si muovono nello spaziotempo, se non altro per l'inesorabile avanzare del tempo. La traiettoria formata da un oggetto nello spaziotempo è detta [[linea di universo]].
### Causalità
La causalità tra due eventi nello spaziotempo può essere descritta mediante il segno della metrica. Allora presi due eventi $E_{1}=(t_{1},\vec{x}_{1})$ e $E_{2}=(t_{2},\vec{x}_{2})$, la loro distanza è
$$S_{12}^{2}=(c\Delta t)^{2}-(\Delta\vec{x})^{2}$$
e si hanno tre casi:
1. $S_{12}^{2}<0$: si ha $t_{1}=t_{2}$, ossia gli eventi avvengono allo stesso tempo e sono spazialmente separati: $S_{12}=\sqrt{-\Delta x^{2}}$. Gli eventi non sono legati causalmente. Si dicono **space-like events**.
2. $S^{2}_{12}>0$: gli eventi non avvengono in contemporanea e sono legati causalmente. Si dicono **time-like events**.
3. $S^{2}_{12}=0$: gli eventi sono connessi solo da un raggio di luce. Si dicono **light-like events**.

È possibile rappresentare questo concetto graficamente mediante un **cono di luce**, ossia il cono prodotto nello spazio tempo un'oggetto che si muove alla velocità della luce e che non è superabile in alcun modo.

![[Diagram Light cone|80%|center]]

### Sistemi di riferimento
In un esperimento, si usano due sistemi di riferimento fondamentali:
1. Il sistema di riferimento del laboratorio è solidale all'osservatore (e ai [[Rivelatore|rivelatori]]). È quello che si usa quando si fa collidere una [[Particella]] con un bersaglio fisso.
2. Il sistema di riferimento del [[centro di massa]] è il sistema tale per cui la somma degli impulsi delle particelle che collidono è nulla: $\sum\vec{p}=0$.

Considerando i [[Four-momentum|quadri-impulsi]] per due particelle (o un bersaglio), si ha per il laboratorio
$$\begin{cases}
p_{1} = (E_{1},\vec{p}_{1})  \\
p_{2} = (M_{2},0)
\end{cases} \quad \Rightarrow \quad p_{tot,lab}=(E_{1}+M_{2},\vec{p}_{1})$$
e per il centro di massa
$$\begin{cases}
p_{1}=(E_{1},\vec{p})  \\
p_{2}=(E_{2},-\vec{p})
\end{cases} \quad \Rightarrow \quad p_{tot,CM}=(E_{1}+E_{2},0)$$
Nel caso di $n$ particelle, si ha $p_{tot,CM}=(\sum E_{i},0)$. In particolare, si ha $p_{tot,CM}=(\sqrt{s},0)$, dove $\sqrt{s}$ è l'[[Center-of-mass energy]].

Applicando le [[Lorentz transformation]] al sistema del laboratorio, possiamo trovare come sono legate energia e impulso. Ad esempio, trasformando lungo $x$ da lab a CM:
$$\begin{pmatrix}\sqrt{s} \\ 0 \\ 0 \\ 0 \end{pmatrix}=g_{\mu\nu}\begin{pmatrix}\sum\limits_{k}E_{k} \\ \sum\limits_{k}p_{k} \\ 0 \\ 0\end{pmatrix} \quad \Rightarrow \quad \beta=\frac{\sum\limits_{k}p_{k}}{\sum\limits_{k}E_{k}}= \frac{p_{tot,lab}}{E_{tot,lab}};\quad \gamma=\frac{E_{tot,lab}}{\sqrt{s}}$$
Se invece applichiamo una trasformazione su $z$ da lab a CM:
$$\begin{pmatrix}E \\ p_{x} \\ p_{y} \\ p_{z}\end{pmatrix}_{LAB}=\begin{pmatrix}E \\ p\sin\theta\cos\varphi \\ p\sin\theta\sin\varphi \\ p\cos\theta\end{pmatrix}_{LAB}=\begin{pmatrix}\gamma & 0 & 0 & \beta\gamma \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ \beta \gamma & 0 & 0 & \gamma\end{pmatrix}\begin{pmatrix}E^{*} \\ p^{*}\sin\theta^{*}\cos\varphi^{*} \\ p^{*}\sin\theta^{*}\sin\varphi^{*} \\ p^{*}\cos\varphi^{*}\end{pmatrix}$$
da cui
$$\begin{pmatrix}E \\ p\sin\theta\cos\varphi \\ p\sin\theta\sin\varphi \\ p\cos\theta\end{pmatrix}_{LAB}=\begin{pmatrix}E^{*}\gamma+\beta\gamma p^{*}\cos\theta^{*} \\ p^{*}\sin\theta^{*}\cos\varphi^{*} \\ p^{*}\sin\theta^{*}\sin\varphi^{*} \\ \beta\gamma E^{*}+\gamma p^{*}\cos\theta^{*}\end{pmatrix}_{CM}$$
da cui si vede $p_{T}=p\sin\theta=p^{*}\sin\varphi^{*}$, ossia si conserva l'*impulso trasverso*, che è quindi un'[[Relativistic invariant]] per una trasformazione lungo $z$, così come $\varphi=\varphi^{*}$ l'*angolo azimutale*.

[^1]: If you want a fancier geometric definition, it is the locus of points on the plane of all light-like events.
