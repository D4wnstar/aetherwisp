---
wiki-publish: true
aliases:
  - cyclical coordinates
---
The **Lagrangian** $L$ is the difference between the [[Kinetic energy|kinetic]] $T$ and [[potential]] $V$ energy of a [[conservative system]]:
$$L(q,\dot{q},t)=T(q,\dot{q},t)-V(q,t)$$
$q$ are the [[generalized coordinates]].
### Cyclical coordinates
Consider the case of a Lagrangian in $n$ dimensions that does not explicitly depend on some coordinates $q_{m+1},\ldots,q_{n}$, such that $L\equiv L(q_{1},\ldots,q_{m},\dot{q}_{1},\ldots,\dot{q}_{m},t)$. These are known as **cyclical coordinates** (the remaining ones are **free coordinates**). These have special properties that make them useful to study. For one, $L$ is invariant over translations of cyclical coordinates. If we send $q_{l}$ to $q_{l}+c$ for some constant $c$ and $l=m+1,\ldots,n$, the Lagrangian does not change[^1].  Also, $\partial L/ \partial q_{l} =0$ and therefore
$$\frac{d}{dt}\frac{ \partial L }{ \partial \dot{q}_{l} }=0$$
This means that all [[conjugate momenta]] $P_{l}$ of cyclical coordinates are [[Constant of motion|constants of motion]]. This is very useful, as it means we can knock out $n-m$ variables and just solve the remaining $m$; the rest will follow suit.

For the sake of brevity, for the rest of this article we'll use $q_\text{free}\equiv(q_{1},\ldots,q_{m})$ to refer to the free coordinates alone. Similarly, $\dot{q}_\text{free}\equiv(\dot{q}_{1},\ldots,\dot{q}_{m})$ is the free velocities alone.
#### Effective Lagrangians
The Lagrangian does not depend on cyclical coordinates. This means that, in theory, we can rewrite the Lagrangian in a form that explicitly does not include them. Such a Lagrangian is known as the **effective Lagrangian** of the system: it describes the same system, but with only variables that actually matter (i.e. have an *effect*).

To do so, consider the [[level set]] given by the conjugate momenta
$$P_{l}(q_\text{free},\dot{q}_{\text{free}},t,\underbrace{ \dot{q}_{m+1},\ldots,\dot{q}_{n} }_{ n-m\text{ cyclical unknowns} })=\tilde{P}_{l}=\text{constant}\tag{*}$$
This inverts to another level set
$$\dot{q}_{l}=u_{l}(q_\text{free},\dot{q}_\text{free},t,\tilde{P}_{m+1},\ldots,\tilde{P}_{n})\tag{**}$$
where $u_{l}$ is some function that inverts the $\tilde{P}_{l}$ relation above.

We can determine the effective Lagrangian over this level set as
$$\begin{align}
&L_\text{eff}(q_\text{free},\dot{q}_\text{free},t,\tilde{P}_{m+1},\ldots,\tilde{P}_{n}) \\
&\equiv L(q_\text{free},\dot{q}_\text{free},t,u_{m+1}(q_\text{free},\dot{q}_\text{free},t,\tilde{P}),\ldots,u_{n}(q_\text{free},\dot{q}_\text{free},t,\tilde{P}))-\sum_{l=m+1}^{n} \tilde{P}_{l}u_{l}(q_\text{free},\dot{q}_\text{free},t,\tilde{P})
\end{align}$$
Without all of the dependencies it reads
$$\boxed{L_\text{eff}=\left.{\left( L-\sum_{l=m+1}^{n} \tilde{P}_{l}\dot{q}_{l} \right)}\right|_{\dot{q}_{l}=u_{l}(q_\text{free},\dot{q}_\text{free},t,\tilde{P})}}$$
This is great and all, but nowhere does it say that this is a valid solution to the system. We now look for the derivatives of $L_\text{eff}$ in order to prove this:
$$\frac{ \partial L_\text{eff} }{ \partial q_{h} } =\frac{ \partial L }{ \partial q_{h} } +\sum_{k=m+1}^{n} \underbrace{ \frac{ \partial L }{ \partial \dot{q}_{k} } }_{ P_{k} } \frac{ \partial u_{k} }{ \partial q_{h} } -\sum_{l=m+1}^{n} \tilde{P}_{l}\frac{ \partial u_{l} }{ \partial q_{h} } $$
and now the time derivatives:
$$\frac{d}{dt} \frac{ \partial L_\text{eff} }{ \partial \dot{q}_{h} } =\frac{d}{dt} \left[ \frac{ \partial L }{ \partial \dot{q}_{h} }  +\sum_{k=m+1}^{n} \underbrace{ \frac{ \partial L }{ \partial \dot{q}_{k} } }_{ P_{k} } \frac{ \partial u_{k} }{ \partial \dot{q}_{h} } -\sum_{l=m+1}^{n} \tilde{P}_{l}\frac{ \partial u_{l} }{ \partial \dot{q}_{h} } \right]$$
If we subtract one from we get
$$E=\frac{d}{dt} \frac{ \partial L_\text{eff} }{ \partial \dot{q}_{h} } -\frac{ \partial L_\text{eff} }{ \partial q_{h} } \quad\text{(on the level set *)}$$
(???)

This takes care of the $m$ non-cyclical coordinates $q_{1},\ldots,q_{m}$. We now need to figure out the remaining $q_{l}$ cyclical coordinates from these ones. To do so, we put the $q_{h}$ found from $E$ in the level set $(**)$. This yields $\dot{q}_{l}(t)=F_{l}(t)$, from which we can find $q_{l}(t)$ by integration.
#### Examples
> [!example] Harmonic oscillator under gravitational pull
 > Consider the Lagrangian
> $$L=\frac{m}{2}(\dot{x}^{2}+\dot{y}^{2}+\dot{z}^{2})-mgz$$
> which is a [[harmonic oscillator]] under a constant force $mg$, interpreted as [[Interazione gravitazionale|gravity]]. $L$ does not depend explicitly on neither $x$ nor $y$, which makes both cyclical coordinates. We should therefore be able to solve the system with just $z$. We find the conjugate momenta of $x$ and $y$ as
> $$\tilde{P}_{x}=\frac{ \partial L }{ \partial \dot{x} } =m \dot{x}\quad\to \quad \dot{x}=\frac{\tilde{P}_{x}}{m}$$
> $$\tilde{P}_{y}=\frac{ \partial L }{ \partial \dot{y} } =m \dot{y}\quad\to \quad \dot{y}=\frac{\tilde{P}_{y}}{m}$$
> The conjugate momenta are constants of motion. We rewrite the Lagrangian as the effective one by substituting $\dot{x}$ and $\dot{y}$ with $\tilde{P}_{x}$ and $\tilde{P}_{y}$:
> $$\begin{align}
> L_\text{eff}(z,\dot{z},\tilde{P}_{x},\tilde{P}_{y})&=\frac{m}{2}\left( \left( \frac{\tilde{P}_{x}}{m} \right)^{2}+\left( \frac{\tilde{P}_{y}}{m} \right)^{2}+\dot{z}^{2} \right)-mgz- \frac{\tilde{P}_{x}^{2}}{m}- \frac{\tilde{P}_{z}^{2}}{m} \\
> &=\frac{m}{2}\dot{z}^{2}-mgz+\text{const.}
> \end{align}$$
> Take a time derivative and we get
> $$\ddot{z}=-g$$
> which is trivial to solve:
> $$z(t)=- \frac{1}{2}gt^{2}+at+z_{0}$$
> where $z_{0}$ is a constant. We have fully solved the system: $x$ and $y$ are determined by constants alone. In fact,
> $$\dot{x}=\frac{\tilde{P}_{x}}{m}\quad\to \quad x(t)=\frac{\tilde{P}_{x}t}{m}+x_{0}$$
> $$\dot{y}=\frac{\tilde{P}_{y}}{m}\quad\to \quad y(t)=\frac{\tilde{P}_{y}t}{m}+y_{0}$$

> [!example] Charge in a constant magnetic field $\mathbf{B}$
> A rather useful problem is figuring out how charges move in a uniform [[magnetic field]], which are common in laboratory settings. The Lagrangian is here given in [[cylindrical coordinates]] as
> $$L=\frac{m}{2}(\dot{r}^{2}+r^{2}\dot{\varphi}^{2}+\dot{z}^{2})+ \frac{eB}{2}r^{2}\dot{\varphi}$$
> Both $\varphi$ and $z$ are cyclical coordinates. The conjugate momentum of $\varphi$ is
> $$\frac{ \partial L }{ \partial \dot{\varphi} } =mr^{2}\dot{\varphi}+ \frac{eB}{2}r^{2}=l\quad\to \quad \dot{\varphi}=\frac{l- \frac{eB}{2}r^{2}}{mr^{2}}=\frac{l}{mr^{2}}- \frac{eB}{2m}$$
> The effective Lagrangian is
> $$L_\text{eff}=\frac{m}{2}\dot{r}^{2}+ \frac{m}{2}\dot{z}^{2}+ \frac{mr^{2}}{2}\left( \frac{l}{mr^{2}}- \frac{eB}{2m} \right)^{2}+ \frac{eB}{2}r^{2}\left( \frac{l}{mr^{2}}- \frac{eB}{2m} \right)-l\left( \frac{l}{mr^{2}}- \frac{eB}{2m} \right)$$
> The last two terms becomes
> $$\frac{eB}{2}r^{2}\left( \frac{l}{mr^{2}}- \frac{eB}{2m} \right)-l\left( \frac{l}{mr^{2}}- \frac{eB}{2m} \right)=-mr^{2}\left( \frac{l}{mr^{2}}- \frac{eB}{2m} \right)^{2}$$
> The whole equation Lagrangian then is
> $$L_\text{eff}=\underbrace{ \frac{m}{2}\dot{r}^{2}+ \frac{m}{2}\dot{z}^{2} }_{ T_\text{eff} }-\underbrace{ mr^{2}\left( \frac{l}{mr^{2}}- \frac{eB}{2m} \right)^{2} }_{ V_\text{eff} }$$
> (TODO: Finish this; end of lesson 27/03/2025)

### Angular momentum
There is a strong connection between [[rotation|rotations]] and [[Constant of motion|constants of motion]]. If $L$ is [[Transformation invariance|invariant under a rotation]] about an axis, then the [[angular momentum]] component on that axis is a constant of motion. This is true because of [[Nöther's theorem]]. Also see [[Rotation#Conservation of angular momentum]].

[^1]: This is rather obvious: if $L$ is not dependent on $q_{l}$, of course it wouldn't change when $q_{l}$ changes. It is however a useful property and worth stressing.
