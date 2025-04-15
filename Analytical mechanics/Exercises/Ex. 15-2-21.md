Two [[point mass|point masses]] of equal [[mass]] $m$ are [[Constraint|constrained]] to move in 2D on a circumference of radius $R$ in the $xy$ plane. The two masses are connected by an elastic spring of elastic constant $k$. A gravitational acceleration $g$ pushes towards $-y$.

![[Diagram Ex. 15-2-21|70%]]

We'll use [[polar coordinates]]:
$$\begin{align}
x_{\theta}&=R\sin \theta \\
y_{\theta}&=-R\cos \theta \\
x_{\varphi}&=R\sin \varphi \\
y_{\varphi}&=-R\cos \varphi
\end{align}$$
To find the [[Lagrangian]], we'll need [[kinetic energy]] and [[potential energy]]. These are
$$T=\frac{1}{2}mR^{2}(\dot{\theta}^{2}+\dot{\varphi}^{2}),\qquad V=mgy_{\theta}+mgy_{\varphi}+ \frac{1}{2}kd(P_{\theta},P_{\varphi})^{2}$$
where $d(P_{\theta},P_{\varphi})^{2}$ is the distance between the origin and the midpoint between the two point masses. It is
$$d=2R\sin\left( \frac{\theta-\varphi}{2} \right)=\sqrt{ (x_{\theta}-x_{\varphi})^{2}+(y_{\theta}-y_{\varphi})^{2} }$$
In polar coordinates, the potential energy becomes
$$\begin{align}
V&=-mgR(\cos \theta+\cos \varphi)+ \frac{1}{2}k\ 4R^{2}\sin ^{2}\left( \frac{\theta-\varphi}{2} \right) \\
&=-mgR(\cos \theta+\cos \varphi)+ kR^{2}(1-\cos (\theta-\varphi)) \\
&=-mgR(\cos \theta+\cos \varphi)- kR^{2}\cos (\theta-\varphi)
\end{align}$$
where we used $\sin ^{2}\left( \theta/2 \right)=(1-\cos\theta)/2$. Our Lagrangian finally is
$$L=T-V=\frac{1}{2}mR^{2}(\dot{\theta}^{2}+\dot{\varphi}^{2})+mgR(\cos \theta+\cos \varphi)+ kR^{2}\cos (\theta-\varphi)$$
We'll solve the [[Lagrange equation]], which means we'll need to solve derivatives for all the coordinates and their velocities.
$$\begin{align}
\frac{ \partial L }{ \partial \theta }&=-mgR\sin \theta-kR^{2}\sin(\theta-\varphi) \\
\frac{ \partial L }{ \partial \varphi } &=-mgR\sin \varphi-kR^{2}\sin(\theta-\varphi) \\
\frac{d}{dt} \left( \frac{ \partial L }{ \partial \dot{\theta} }  \right)&=mR^{2}\ddot{\theta} \\
\frac{d}{dt} \left( \frac{ \partial L }{ \partial \dot{\varphi} }  \right)&=mR^{2}\ddot{\varphi}
\end{align} $$
From the latter two we derive the motion [[Ordinary differential equation|ODEs]]
$$\ddot{\theta}=- \frac{g}{R}\sin \theta- \frac{R}{m}\sin (\theta-\varphi),\qquad \ddot{\varphi}=- \frac{g}{R}\sin \theta + \frac{k}{m}\sin(\theta-\varphi)$$
Now, for [[Equilibrium point|equilibrium points]], we can use minimize the potential energy. First, we need the partial derivatives
$$\begin{align}
\frac{ \partial V }{ \partial \theta } &=mgR\sin \theta+kR^{2}\sin (\theta-\varphi)=0 \\
\frac{ \partial V }{ \partial \varphi } &=mgR\sin \varphi-kR^{2}\sin(\theta-\varphi)=0
\end{align}$$
When solved, these give us $(\theta=0,\varphi=\pi)$, $(\theta=\pi,\varphi=0)$, $(\theta=0,\varphi=0)$ and $(\theta=\pi,\varphi=\pm \pi)$. In order to determine stability, we need the second derivatives of $V$. Since $V:\mathbb{R}^{2}\to \mathbb{R}^{2}$, this means we're dealing with a $2\times 2$ [[Hessian]]:
$$\partial ^{2}V=\begin{pmatrix}
\frac{ \partial ^{2}V }{ \partial \theta ^{2} }  & \frac{ \partial ^{2}V }{ \partial \theta \partial \varphi }  \\
\frac{ \partial ^{2}V }{ \partial \varphi \partial \theta } & \frac{ \partial ^{2}V }{ \partial \varphi ^{2} }
\end{pmatrix}=\begin{pmatrix}
mgR\cos \theta+kR^{2}\cos(\theta-\varphi) & -kR^{2}\cos(\theta-\varphi) \\
-kR^{2}\cos(\theta-\varphi) & mgR\cos \theta+kR^{2}\cos(\theta-\varphi)
\end{pmatrix}$$
With this Hessian, we can attempt to linearize the Lagrangian around the equilibrium points. Our motion matrices are
$$A=\begin{pmatrix}
mR^{2} & 0 \\
0 & mR^{2}
\end{pmatrix}$$
and $B$ is $\partial ^{2}V$ evaluated in the point of equilibrium.