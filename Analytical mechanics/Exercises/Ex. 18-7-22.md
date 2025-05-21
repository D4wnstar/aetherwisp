Consider a homogeneous disk of [[mass]] $M$ and radius $R$ [[Constraint|constrained]] to the $xy$ plane. The disk rolls without sliding over the $x$ axis. Its center $G$ is linked to the point $(0,R)$ by a spring of elastic constant $k$ and null rest length. A pendulum of length $\ell$ and mass $m$ is hanging from the point $P$. Gravity affects the system. The [[configuration space]] is parameterized by the angles $\theta$ and $\varphi$ as shown. $\varphi$ is defined such that the spring has length zero when $\varphi=\pi$.

![[Diagram Ex. 18-7-22]]

1. Write the [[Lagrangian]] $L$.
2. Write the [[Kinetic energy|kinetic matrix]].
3. Write [[Lagrange equation]] for $\theta$.
4. Setting one parameter ($m,M,k,R,\ell,g$) to zero, the number of constants of motion increases by one. Which?
5. Find the [[Equilibrium point|equilibrium points]] for the system and discuss their stability when $kR/mg>1$ and $2/5\pi<kR/mg<1$.
6. Set $kR/mg=2$, $\ell=R$ and $M=2m/3$, then calculate the frequency of small oscillations, the linearized Lagrangian around the stable equilibrium point and the relative Lagrange equation.

---

We start from the Lagrangian, which means that we need the [[kinetic energy]] and the [[potential energy]]. The kinetic energy of the disk is
$$T_{M}=\frac{M}{2}R^{2}\dot{\varphi}^{2}+ \frac{1}{2}I \dot{ \varphi}^{2}=\frac{M}{2}R^{2}\dot{\varphi}^{2}\left( 1+ \frac{1}{2} \right)=\frac{3}{4}MR^{2} \dot{\varphi}^{2}$$
The pendulums energy is less straightforward. We need to express the coordinates $(x_{Q},y_{Q})$ of $Q$ using coordinates that we know $(\varphi,\theta)$:
$$x_{Q}=x_{G}+R\sin \varphi+\ell \sin \theta,\quad y_{Q}=R-R\cos \varphi -\ell \cos \theta$$
The time derivatives are
$$\dot{x}_{Q}=-R \dot{\varphi}+R \dot{\varphi}\cos \varphi+\ell \dot{\theta}\cos \theta,\quad \dot{y}_{Q}=R \dot{\varphi}\sin \varphi+\ell \dot{\theta}\sin \theta$$
Thus the pendulum kinetic energy is
$$\begin{align}
T_{m}&=\frac{m}{2}(\dot{x}^{2}_{Q}+\dot{y}^{2}_{Q}) \\
&=\frac{m}{2}[R^{2}\dot{\varphi}^{2}+R^{2}\dot{\varphi}^{2}+\ell ^{2}\dot{\theta}^{2}-2R^{2}\dot{\varphi}^{2}\cos \varphi+2R\ell \dot{\varphi}\dot{\theta}(\cos \varphi \cos \theta+\sin \varphi \sin \theta)] \\
&=\frac{m}{2}[2R^{2}(1-\cos \varphi  )\dot{\varphi}^{2}+\ell ^{2}\dot{\theta}^{2}+2R\ell \dot{\varphi}\dot{\theta}(\cos(\theta-\varphi)-\cos \theta)]
\end{align}$$
Of course, the total kinetic energy is just the sum:
$$T=T_{M}+T_{m}$$
The potential energy is a mix of gravity and elastic potential:
$$V=\frac{k}{2}R^{2}(\varphi-\pi)^{2}+mg[R(1-\cos \varphi)-\ell \cos \theta]$$
The Lagrangian is the sum of the two (with some additional grouping in $T$):
$$\begin{align}
L&=\frac{1}{2}R^{2}\dot{\varphi}^{2}\left[ \frac{3}{2}M+(2-2\cos \varphi)m \right]+ \frac{m}{2}\ell ^{2}\dot{\theta}^{2}+ \frac{1}{2}\dot{\varphi}\dot{\theta} \ 2mR\ell[\cos (\theta-\varphi)-\cos \theta] \\
&- \frac{1}{2}kR^{2}(\varphi-\pi)^{2}-mg(R-R\cos \varphi-\ell \cos \theta)
\end{align}$$

---

The kinetic matrix comes from its definition
$$T=\frac{1}{2}\sum_{ij}a_{ij}\dot{q}_{i}\dot{q}_{j}=\frac{1}{2}(a_{11}\dot{\varphi}^{2}+a_{12}\dot{\theta}^{2}+a_{22}\dot{\varphi}\dot{\theta}+a_{21}\dot{\theta}\dot{ \varphi})=\frac{1}{2}(a_{11}\dot{\varphi}^{2}+a_{22}\dot{\varphi}\dot{\theta}+2a_{12}\dot{\varphi}\dot{\theta})$$
so comparing it with our kinetic energy we get
$$a=\begin{pmatrix}
R^{2}\left[ \frac{3}{2}M+(2-2\cos \varphi)m \right] & mR\ell[\cos(\theta-\varphi)-\cos \theta] \\
mR\ell[\cos(\theta-\varphi)-\cos \theta] & m\ell ^{2}
\end{pmatrix}$$

---

Now, to find the Lagrange equation for $\theta$, we just apply the definition
$$\frac{d}{dt} \frac{ \partial L }{ \partial \dot{\theta} } -\frac{ \partial L }{ \partial \theta }=0 $$
So
$$\begin{align}
\frac{d}{dt} \frac{ \partial L }{ \partial \dot{\theta} } &=\frac{d}{dt} (m\ell ^{2}\theta+\dot{\varphi}mR\ell[\cos(\varphi-\theta)-\cos \theta]) \\
&=m\ell ^{2}\ddot{\theta}+\ddot{\varphi}mR\ell[\cos(\theta-\varphi)-\cos \theta]+\dot{\varphi}mR\ell[-(\dot{\theta}-\dot{\varphi})\sin(\theta-\varphi)+\dot{\theta}\sin \theta]
\end{align}$$
and
$$\frac{ \partial L }{ \partial \theta } =\dot{\varphi}\dot{\theta}mR\ell[-\sin (\theta-\varphi)+\sin \theta]-mg\ell \sin \theta$$
Combine the two to get
$$\ell ^{2}\ddot{\theta}+R\ell \ddot{\varphi}[\cos (\theta-\varphi)-\cos \theta]+\dot{\varphi}^{2}R\ell \sin(\theta-\varphi)+mg\ell \sin \theta=0$$
If you want, you could extract $\ddot{ \theta}$ to make it explicit, but this is correct as is.

---

(TODO: Point 4 was skipped in class)

---

To analyze equilibrium points, we look at how the potential behaves by taking its derivatives and seeing where they cancel out:
$$\frac{ \partial V }{ \partial \varphi } =kR^{2}(\varphi-\pi)+mgR\sin \varphi=0,\quad \frac{ \partial V }{ \partial \theta } =mg\ell \sin \theta=0$$
These solve to
$$\sin \varphi=- \frac{kR}{mg}\varphi+ \frac{kR}{mg}\pi,\quad \theta=0,\pi$$

![[Diagram Ex. 18-7-22 Part 5|80%]]

We can use the [[Hessian]] of the potential to determine stability:
$$\partial ^{2}V=\begin{pmatrix}
\frac{ \partial ^{2}V }{ \partial \varphi ^{2} }  & 0 \\
0 & \frac{ \partial ^{2}V }{ \partial \theta ^{2} } 
\end{pmatrix}$$
If both [[Equazione agli autovalori|eigenvalues]] are $>0$, then the point is stable. Then
$$\frac{ \partial V^{2} }{ \partial \theta ^{2} } =mg\ell \cos \theta$$
This is $>0$ when $\theta=0$, so it is a minimum. It is $<0$ when $\theta=\pi$, so it is a maximum. Meanwhile,
$$\frac{ \partial ^{2}V }{ \partial \varphi ^{2} } =kR^{2}+mgR\cos \varphi=mgR\left( \frac{kR}{mg}+\cos \varphi \right)$$
In critical points:
$$\frac{ \partial ^{2}V }{ \partial \varphi ^{2} } (\varphi=\pi)>0\quad\text{when}\quad \frac{kR}{mg}>1$$
Similarly, it is $<0$ in when $2/5\pi<kR/mg<1$.

(TODO: Finish point 5)

---

When $kR/mg=2$, the minimum is in $\varphi=\pi$ and $\theta=0$. To linearize the Lagrangian, we solve the following system:
$$0=\det(B-\lambda A)$$
where
$$A=a|_{\text{min}}=\begin{pmatrix}
5mR^{2} & -2mR^{2} \\
-2mR^{2} & mR^{2}
\end{pmatrix},\quad B=\partial ^{2}V|_\text{min}=\begin{pmatrix}
mgR & 0 \\
0 & mgR
\end{pmatrix}$$
so
$$\begin{align}
0&=\det m\begin{pmatrix}
gR-5R^{2}\lambda & 2R^{2}\lambda \\
2R^{2}\lambda & gR-R^{2}\lambda
\end{pmatrix} \\
&=\det mR^{2}\begin{pmatrix}
\frac{g}{R}-5\lambda & 2\lambda \\
2\lambda & \frac{g}{R}-\lambda
\end{pmatrix} \\
&=\left( \frac{g}{R} \right)^{2}- 6\left( \frac{g}{R} \right)\lambda+5\lambda ^{2}-4\lambda ^{2} \\
&=\frac{g}{R}(3\pm2\sqrt{ 2 })
\end{align}$$
by solving for $\lambda_{1,2}$.

(TODO: Finish point 6)