There is a [[point mass]] of [[mass]] $m$ [[Constraint|constrained]] to the $xy$ plane. The mass is attached with an inextensible rope to a weight of mass $M$ hanging off the origin $\mathcal{O}$. [[Interazione gravitazionale|Gravity]] $g$ affects the whole system, pulling the weight down.

![[Diagram Ex. 18-3-18]]

We have a few constraints here. $m$ is locked to the $xy$ plane, so $z_{1}=0$. We'll use [[polar coordinates]] $r$ and $\theta$ for $m$, so $x_{1}=r\cos \theta$ and $y_{1}=r\sin \theta$. The weight hangs off the origin, so $x_{2}=0$ and $y_{2}=0$. $z_{2}$ must be determined by the length of the rope, $L=r-z_{2}$, from which $z_{2}=r-L$. In total we get
$$\begin{align}
x_{1}&=r\sin \theta \\
y_{1}&=r\cos \theta \\
z_{1}&=0 \\
x_{2}&=0 \\
y_{2}&=0 \\
z_{2}&=r-L
\end{align}$$
We'll use a [[Lagrangian]], so we need both the [[kinetic energy]] and the [[potential energy]]. For kinetic energy, we need velocities, which we get by derivation:
$$\begin{align}
\dot{x}_{1}&=\dot{r}\cos \theta-r \dot{\theta}\sin \theta \\
\dot{y}_{1}&=\dot{r}\sin \theta+r \dot{\theta}\cos \theta \\
\dot{z}_{2}&=\dot{r}
\end{align}$$
Everything else is zero. Our kinetic energy then is
$$\begin{align}
T&=\frac{1}{2}m(\dot{x}_{1}^{2}+\dot{y}_{1}^{2})+ \frac{1}{2}M \dot{z}_{2}^{2} \\
&=\frac{1}{2}m(\dot{r}^{2}\cos ^{2}\theta-2r \dot{r}\dot{\theta}\sin \theta \cos \theta+r^{2}\theta ^{2}\sin ^{2}+\dot{r}^{2})\ldots \\
&=\frac{1}{2}(m+M)\dot{r}^{2}+ \frac{1}{2}mr^{2}\dot{\theta}^{2}
\end{align}$$
The potential energy is just standard gravitational potential
$$V=Mgz_{2}=Mgr-MgL$$
Our Lagrangian then is
$$\boxed{\mathcal{L}=T-V=\frac{1}{2}(m+M)\dot{r}^{2}+ \frac{1}{2}mr^{2}\dot{\theta}^{2}-Mgr+mgL}$$
We now need to solve the [[Lagrange-Euler equation]]
$$\frac{ \partial \mathcal{L} }{ \partial q } -\frac{d}{dt} \left( \frac{ \partial \mathcal{L} }{ \partial \dot{q} }  \right)=0$$
We'll do the derivatives for each coordinate:
$$\begin{align}
\frac{ \partial \mathcal{L} }{ \partial r } &=-Mg+mr \dot{\theta}^{2} \\
\frac{ \partial \mathcal{L} }{ \partial \theta } &=0 \\
\frac{d}{dt} \frac{ \partial \mathcal{L} }{ \partial \dot{r} } &=\frac{d}{dt} [(m+M)\dot{r}]=(m+M)\ddot{r} \\
\frac{d}{dt} \frac{ \partial \mathcal{L} }{ \partial \dot{\theta} } &=\frac{d}{dt} (mr^{2}\dot{\theta})=mr^{2}\ddot{\theta}+2mr \dot{r}\dot{\theta}
\end{align}$$
The Lagrange equations for $q=r$ and $q=\theta$ are
$$\begin{align}
&(q=r)\qquad-Mg+mr \dot{ \theta}^{2}=(m+M)\ddot{r}\quad\to \quad \ddot{r}=\frac{m}{m+M}r \dot{\theta}^{2}- \frac{M}{m+M}g \\
&(q=\theta)\qquad mr^{2}\ddot{\theta}+2mr \dot{r}\dot{\theta}=0\quad\to \quad \ddot{\theta}=- \frac{2\dot{r}\dot{\theta}}{r}
\end{align}$$
$\ddot{r}$ and $\ddot{\theta}$ are our motion [[Ordinary differential equation|ODEs]]. We don't really need to solve one of them however; $\theta$ is a [[Lagrangian|cyclical coordinate]]. In fact, imagine the motion of the point mass. Once it's let free, the weight will be pulled down by gravity and the point mass will be dragged along with it until it stops at the origin. It does not rotate: it goes straight for the origin. As such, the [[Conjugate momenta|conjugate momentum]] $P_{\theta}$ of $\theta$ must be a [[constant of motion]] and we can use this to reduce the number of ODEs we need to solve by one. In fact, the whole system really only has one effective [[Degrees of freedom|degree of freedom]]. First, we find $P_{\theta}$:
$$P_{\theta}=\frac{ \partial \mathcal{L} }{ \partial \dot{\theta} } =mr^{2}\dot{\theta}\quad\to \quad\dot{\theta}=\frac{P_{\theta}}{mr^{2}}$$
Our *effective* Lagrangian is
$$\begin{align}
\mathcal{L}^{*}&=\left.{(\mathcal{L}-\dot{ \theta}P_{\theta})}\right|_{\dot{\theta}(P_{\theta})} \\
&=\frac{1}{2}(M+m)\dot{r}^{2}+ \frac{1}{2}mr^{2}\left( \frac{P_{\theta}^{2}}{m^{2}r^{4}} \right)-Mgr \\
&=\frac{1}{2}(M+m)\dot{r}^{2}+ \frac{1}{2} \frac{P_{\theta}^{2}}{mr^{2}}-Mgr \\
&=\frac{1}{2}(M+m)\dot{r}^{2}+\frac{P_{\theta}^{2}}{mr^{2}}\underbrace{\ - \frac{1}{2} \frac{P_{\theta}^{2}}{mr^{2}}-Mgr }_{ V_\text{eff} }
\end{align}$$
Our *effective* potential is
$$V_\text{eff}=Mgr+ \frac{1}{2} \frac{P_{\theta}^{2}}{mr^{2}}$$
with derivative
$$V'_\text{eff}=Mg- \frac{P_{\theta}^{2}}{mr^{3}}$$
and second derivative
$$V''_\text{eff}=\frac{3P_{\theta}^{2}}{mr^{4}}>0\quad\forall r>0$$
The second derivative is always positive, so there is a global minimum, and that minimum is the only point $r_{\star}$ where $V'_\text{eff}=0$. This is
$$\frac{P_{\theta}^{2}}{mr^{3}_{\star}}=Mg\quad\to \quad r_{\star}^{3}=\frac{P_{\theta}^{2}}{mMg}\quad\to \quad r_{\star}=\left( \frac{P_{\theta}^{2}}{mMg} \right)^{1/3}$$
This is an [[equilibrium point]] for the *effective Lagrangian* (but not for the complete one!). We'll now study some small oscillations around this point, and to do so we'll try to change the Lagrangian until it is in the form of a [[harmonic oscillator]]. The linearized Lagrangian must be of some form
$$\mathcal{L}_\text{lin}=\frac{1}{2}A \dot{r}^{2}-B(r-r_{\star})^{2}$$
$A$ and $B$ would normally be matrices, but since we only have one degree of freedom, they are $1\times1$, so just [[scalar|scalars]]. We'll want to [[diagonalization|diagonalize]] the motion "matrices" by solving
$$\det(B-\lambda A)=0$$
Again, since $A$ and $B$ are scalars, this is just
$$B=\lambda A\quad\to \quad \lambda=\frac{B}{A}=???=\frac{V''(r_{\star})}{M+m}=\frac{3P^{2}_{\theta}}{mr_{\star}^{4}} \frac{1}{M+m}$$
