Consider two bodies of [[mass|masses]] $m_{1}$ and $m_{2}$ moving in $\mathbb{R}^{3}$, for a total of $n=6$ [[degrees of freedom]]. Each position vector is $\mathbf{r}_{i}=(x_{i},y_{i},z_{i})$ for $i=1,2$. The [[kinetic energy]] is
$$T=\frac{1}{2}m_{1} \dot{\mathbf{r}}_{1}^{2}+ \frac{1}{2}m_{2}\dot{\mathbf{r}}_{2}^{2}$$
The [[potential energy]] is dependent on the distance between the bodies, $V\equiv V(\mathbf{r}_{1}-\mathbf{r}_{2})=V(\mathbf{r})$, where we defined $\mathbf{r}\equiv \mathbf{r}_{1}-\mathbf{r}_{2}$ for the sake of brevity. Like in most $N$-body systems, we can use the [[center of mass]] frame to simplify our treatment. Call $M\equiv m_{1}+m_{2}$ the total mass. The center of mass is located by
$$\mathbf{R}=\frac{m_{1}\mathbf{r}_{1}+m_{2}\mathbf{r}_{2}}{M}$$
We can retroactively get the positions of the two bodies from the center of mass as
$$\mathbf{r}_{1}=\mathbf{R}+ \frac{m_{2}\mathbf{r}}{M},\qquad \mathbf{r}_{2}=\mathbf{R}- \frac{m_{1}\mathbf{r}}{M}$$
With these new coordinates, we can rewrite the expression of kinetic energy in this frame:
$$\begin{align}
T&=\frac{1}{2}m_{1}\left( \dot{\mathbf{R}}^{2}+ \cancel{ \frac{2m_{2}}{M}\dot{\mathbf{R}}\cdot\dot{\mathbf{r}} }+ \frac{m_{2}^{2}}{M}\dot{\mathbf{r}}^{2} \right)+ \frac{1}{2}m_{2}\left( \dot{\mathbf{R}}^{2}- \cancel{ \frac{2m_{1}}{M}\dot{\mathbf{R}}\cdot \dot{\mathbf{r}} }+ \frac{m_{1}^{2}}{M}\dot{\mathbf{r}}^{2} \right) \\
&=\frac{1}{2}M \dot{\mathbf{R}}^{2}+ \frac{1}{2} \frac{m_{1}m_{2}^{2}+m_{2}m_{1}^{2}}{M^{2}}\dot{\mathbf{r}}^{2}
\end{align}$$
We now defined the reduced mass $\mu\equiv m_{1}m_{2}/M$, with which we can comfortably write
$$T=\frac{1}{2}M \dot{\mathbf{R}}^{2}+ \frac{1}{2}\mu \dot{\mathbf{r}}^{2}$$
The kinetic energy has gone from the sums if kinetic energy of the bodies to the sums of kinetic energy of the "center of mass" and of another terms that evidently takes up "everything else". With the kinetic energy known, we are ready to write the [[Lagrangian]] of this system:
$$L=\frac{1}{2}M \dot{\mathbf{R}}^{2}+ \frac{1}{2}\mu \dot{\mathbf{r}}^{2}- V(\mathbf{r})$$
for some potential energy $V$. Note that this does not depend on *where* the center of mass is, as there is no mention of $\mathbf{R}$ (only its derivative $\dot{\mathbf{R}}$).

We can interpret this equation as the sum of a free particle of mass $M$ and a particle of mass $\mu$ subject to a potential $V(\mathbf{r})$. In this light, we'll split the Lagrangian in two. Specifically, the latter part is
$$L(\mathbf{r},\dot{\mathbf{r}})=\frac{1}{2}\mu \lvert \dot{\mathbf{r}} \rvert ^{2}-V(\lvert \mathbf{r} \rvert )$$
As with all Lagrangians, our priority should be sniff out [[Constant of motion|constants of motion]], as each and every one we find makes our problem easier. This Lagrangian of $\mathbf{r}$, for instance, is invariant to [[Rotation|rotations]] (in $SO(3)$). Invoking [[Nöther's theorem]], this means that the [[angular momentum]] $\mathbf{A}$[^1] is a constant of motion (all three components actually, so $A_{x}$, $A_{y}$ and $A_{z}$). Let's analyze what this invariance implies. The momentum is $\mathbf{A}=\mu \mathbf{r}\times \dot{\mathbf{r}}$. If it's constant over $\mathbf{r}(t)$, then $\mu \mathbf{r}(t)\times \dot{\mathbf{r}}(t)=\mathbf{A}_\text{const}$, but for a [[vector product]] to give an angle-independent constant we must have both $\mathbf{r}(t)$ and $\dot{\mathbf{r}}(t)$ lying [[Orthogonality|orthogonal]] to $\mathbf{A}_\text{const}$. In other words, both $\mathbf{r}(t)$ and $\dot{\mathbf{r}}(t)$ (and by extension the whole motion) lie on a plane perpendicular to $\mathbf{A}_\text{const}$.

This bit of geometry gives us the information that we need to simplify our coordinates. We'll then pick a [[frame of reference]] in which $(A_\text{const})_{x}=(A_\text{const})_{y}=0$[^2]. In this frame, we can pick the canonical [[basis]] $\{ \mathbf{e}_{x} ,\mathbf{e}_{y}\}$ and express $\mathbf{r}$ and $\dot{\mathbf{r}}$ as a [[linear combination]] of these:
$$\mathbf{r}=x\mathbf{e}_{x}+y\mathbf{e}_{y},\qquad \dot{\mathbf{r}}=\dot{x}\mathbf{e}_{x}+\dot{y}\mathbf{e}_{y}$$
In here, the Lagrangian becomes
$$L=\frac{1}{2}\mu(\dot{x}^{2}+\dot{y}^{2})- V(\sqrt{ x^{2}+y^{2} })$$
Since we're on a plane, we might as well move to [[polar coordinates]]. The appropriate [[coordinate transformation]] is
$$x=r\cos \theta,\qquad y=r\sin \theta$$
for which
$$L=\frac{1}{2}\mu(\dot{r}^{2}+r^{2}\dot{\theta}^{2})-V(r)$$
You might be wondering why the switch: the answer is that our "$\mu$" particle is moving in a straight line. Of course: there's no angular momentum, it can't be rotating! So our angular coordinate must be *[[Lagrangian|cyclical]]* and, as such, its [[Conjugate momenta|conjugate momentum]] is another constant of motion:
$$p_{\theta}=\frac{ \partial L }{ \partial \theta } =mr^{2}\dot{\theta}\equiv l=\text{constant}$$
As usual, this leads to an easy first order [[Ordinary differential equation|ODE]]:
$$\dot{ \theta}=\frac{l}{mr^{2}}$$
We can look for an effective Lagrangian
$$\begin{align}
L_\text{eff}&=L-\left.{\dot{\theta}l}\right|_{\dot{ \theta}=l/mr^{2}} \\
&=\frac{1}{2}m \dot{ r}^{2}+ \frac{m}{2}r^{2} \frac{l^{2}}{(mr^{2})^{2}}-V(r)- \frac{l^{2}}{mr^{2}} \\
&=\frac{1}{2}m \dot{r}^{2}- V(r)- \frac{l^{2}}{2mr^{2}} \\
&=\frac{1}{2}m \dot{r}^{2}-V_\text{eff}(r)
\end{align}$$


[^1]: Unfortunately, both common letters for angular momentum, $L$ and $M$, are taken here so we'll use the less orthodox $\mathbf{A}$ here (it stands for "angular").

[^2]: Mathematically, this defines a [[level set]] of codimension $2$.
