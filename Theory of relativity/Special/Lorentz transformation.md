---
wiki-publish: true
aliases:
  - relativistic
  - ultrarelativistic
---
A **Lorentz transformation** is a [[coordinate transformation]] between [[Frame of reference|inertial frames]] in [[spacetime]]. A transformation between a [[frame of reference]] $(x,y,z,t)$ to $(x',y',z',t')$ states
$$\left\{\begin{align}
&x'=\gamma(x-\beta ct) \\
&y'=y \\
&z'=z \\
&t'=\gamma\left( t- \frac{\beta}{c}x \right)
\end{align}\right.$$
with parameters
$$\gamma\equiv \frac{1}{\sqrt{ 1-\beta ^{2} }},\qquad \beta\equiv\frac{v}{c}$$
In the language of [[proper velocity]], $v$ would be the *ordinary* velocity. Alternatively, in common [[four-vector]] notation $(ct,x,y,z)\equiv(x^{0},x^{1},x^{2},x^{3})$:
$$\left\{\begin{align}
&\bar{x}^{0}=\gamma(x^{0}-\beta x^{1}) \\
&\bar{x}^{1}=\gamma\left(x^{1}- \beta x^{0} \right) \\
&\bar{x}^{2}=x^{2} \\
&\bar{x}^{3}=x^{3}
\end{align}\right.$$
where the overbar now denotes the new frame. Here, time is expressed in units of $ct$ instead of $t$, meaning that it is measured in meters and interpreted as the time it takes for light to travel that many meters. In matrix notation we have
$$\bar{x}=\Lambda x$$
where
$$\Lambda=\begin{pmatrix}\gamma & -\beta \gamma & 0 & 0 \\ -\beta \gamma & \gamma & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1\end{pmatrix},\qquad x=\begin{pmatrix}
x^{0} \\ x^{1} \\ x^{2} \\ x^{3}
\end{pmatrix},\qquad \bar{x}=\begin{pmatrix}
\bar{x}^{0} \\ \bar{x}^{1} \\ \bar{x}^{2} \\ \bar{x}^{3}
\end{pmatrix}$$
$\Lambda$ is known as the **Lorentz transformation matrix**. The convenience of this form lies in that, besides being more compact, it also makes it easier to handle transformations that are not on a common $x,\bar{x}$ axis, as you'd just change the matrix accordingly. Each individual component is then written
$$\bar{x}^{\mu}=\sum_{\nu=0}^{3} \Lambda_{\nu}^{\mu}x^{\nu}\equiv \Lambda_{\nu}^{\mu}x^{\nu}$$
where the second equality is using [[Einstein notation]] for implicit summation.
### Derivation
Say we have an [[event]] $E$ at coordinates $(x,y,z,t)$ in some inertial system $\mathcal{S}$. We want to express this event in another inertial frame $\mathcal{S}'$, where it'll have coordinates $(x',y',z',t')$. We are looking for the coordinate transformation that will convert between the two. This space is four dimensional, so a complete visualization is not possible. However, think of it like this: since we have inertial frames, the origins can move at some constant velocity. Let's say that at time $t=0$, both $\mathcal{S}$ and $\mathcal{S}'$ coincide. As time goes on, the two systems will in general move away from each other, at some constant velocity $\mathbf{v}$. Say this velocity is on the $x$ axis (if it's not, rotate everything until it is). Then, over some time $t$, the origin of $\mathcal{S}'$ will move a distance $vt$ away from the origin of $\mathcal{S}$ on the $x$ axis (the other coordinates don't change). The event coordinates will *of course* be connected by
$$x=x'+vt$$
and so the coordinate transformation is
$$\begin{cases}
x'=x-vt \\
y'=y \\
z'=z \\
t'=t
\end{cases}$$
These are the old [[Galilean transformation|Galilean transformations]] that applied to [[Galilean relativity]]. As you may guess from this nomenclature, these start to collapse when introducing special relativity and a finite [[speed of light|top speed]] in the universe and the cause is due to the consequences of the [[postulates of special relativity]]. [[Relativity of simultaneity]] and [[time dilation]] must have some sort of effect on $t'=t$ and [[distance contraction]] certainly invalidates the snarky "*of course*" regarding $x=x'+vt$. On the other hand, $y'=y$ and $z'=z$ are safe since distance contraction occurs only on the axis of motion.

The issue in the previous derivation is in being a little too sure that $x=x'+vt$. More generally, say we have $x=d+vt$, where $d$ is the distance measured between the origin of $\mathcal{S}'$ and the $x$-component of $E$. If distance contraction weren't a thing, $d$ would certainly be $x'$ and our results above would hold. But distance contraction is indeed a thing, so we must take it into account:
$$d=\frac{x'}{\gamma}\quad\Rightarrow \quad x=d+vt=\frac{x'}{\gamma}+vt\quad\Rightarrow \quad x'=\gamma(x-vt)$$
The same argument could be done in reverse to go from $\mathcal{S}'$ to $\mathcal{S}$, just this time we'll have $x'=d'-vt'$, where $d'$ is the distance between the origin of $\mathcal{S}$ and the $x$ component of $E$. In classical physics, this is again $d'=x$, but in relativity, we must consider contraction, so
$$d'=\frac{x}{\gamma}\quad\Rightarrow \quad x'=d'-vt=\frac{x}{\gamma}-vt\quad\Rightarrow \quad x=\gamma(x'+vt)$$
which shouldn't be surprising, since relativistic effects are symmetrical between observer. We can now substitute these results into the Galilean transformations and solve for $t'$ to obtain
$$\boxed{\left\{\begin{align}
&x'=\gamma(x-vt) \\
&y'=y \\
&z'=z \\
&t'=\gamma\left( t- \frac{v}{c^{2}}x \right)
\end{align}\right.}$$
These are the **Lorentz transformations** for spacetime coordinates (or a singular Lorentz transformation if you are talking the change as a whole). The reverse transformation is just a matter of changing the primes and inverting the minuses into pluses:
$$\left\{\begin{align}
&x=\gamma(x'+vt') \\
&y=y' \\
&z=z' \\
&t=\gamma\left( t'+ \frac{v}{c^{2}}x' \right)
\end{align}\right.$$
Defining $\beta\equiv v/c$, they can also be written as
$$\left\{\begin{align}
&x'=\gamma(x-\beta ct) \\
&y'=y \\
&z'=z \\
&t'=\gamma\left( t- \frac{\beta}{c}x \right)
\end{align}\right.$$
Note how when $v\ll c$, then $\gamma\to 1$ and $\beta\to 0$ and these go back to being the usual Galilean transformations.
### Limite relativistico
Gli effetti relativistici diventano importanti solo quando la velocità di un oggetto si avvicina a quella della luce. Si dice **limite relativistico** il limite oltre il quale bisogna usare la relatività per evitare errori grandi. Matematicamente, il limite equivale ad avere $\beta\sim1$ e $\gamma>1$. Si dice **regime ultrarelativistico** le condizioni $\beta\sim1$ e $\gamma\gg1$.
### As a hyperbolic rotation
A Lorentz transformation is a hyperbolic [[rotation]] in spacetime, the angle of which is called the [[rapidity]] $y$:
$$\pmatrix{ct' \\ x' \\ y' \\ z'}=\pmatrix{\cosh y & -\sinh y & 0 & 0 \\ -\sinh y & \cosh y & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1}\pmatrix{ct \\ x \\ y \\ z}$$
