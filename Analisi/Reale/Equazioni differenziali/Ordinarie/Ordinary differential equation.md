---
wiki-publish: true
aliases:
  - ODE
---
An **ordinary differential equation**, or **ODE** for short, is an equation where a function and one or more its derivatives appear simultaneously. The highest derivative of the function is said to be the **order** of the ODE. If we denote the function as $f(t)$ and its $i$-th derivative as $f^{(i)}(t)$, a generic ODE written in **normal form** (with the highest derivative isolated) is
$$f^{(n)}(t)=g(f,f^{(1)},\ldots,f^{(n-1)},t)$$
where $g$ is some function.

An ODE is said to be **autonomous** if it has no explicit dependence on $t$ (although all the $f(t)$ still do). In this case, $g$ is not dependent on $t$.
$$f^{(n)}(t)=g(f,f^{(1)},\ldots,f^{(n-1)})$$
If $g$ is a linear function, the ODE can be written as
$$f^{(n)}(t)=c_{0}(t)f(t)+c_{1}(t)f^{(1)}(t)+\ldots+c_{n-1}(t)f^{(n-1)}(t)+k(t)$$
where the $c_{i}$ and $k$ are functions of $t$. In this case, the ODE is said to be **linear**. Moreover, if $k(t)=0$ for all $t$, the equation is said to be **homogeneous**.
### Systems
A high-order ODE can be expressed as a system of first-order ODEs. Consider for instance a generic second-order ODE $\ddot{x}=g(x,\dot{x},t)$, where we used dot notation for derivatives and renamed $f$ to $x$. If we name $\dot{x}=v$, we can express the second-order ODE as a system of two first-order ODEs, one in $x$ and one in $v$:
$$\begin{cases}
\dot{x}=v \\
\dot{v}=f(x,v,t)
\end{cases}$$
In general, the number of first-order ODEs is equal to the order of the original one.

$$\begin{cases}
\dot{x}_{1}=f_{1}(x_{1},\ldots,x_{N}) \\
\dot{x}_{2}=f_{2}(x_{1},\ldots,x_{N}) \\
\vdots \\
\dot{x}_{N}=f_{N}(x_{1},\ldots,x_{N}) \\
\end{cases}$$

The benefit of doing things this way is that first-order ODEs have a large amount of theorems and results that make them far easier to solve and much more reliable to work with. For an example, the following theorem underlies much of the study of these equations.

> [!info] Existence and uniqueness theorem
> Consider a first-order ODE $\dot{x}=f(x)$ and a starting condition $x(t_{0})=x_{0}$. If $f$ and its derivative $f'$ are continuous on an open interval of $x$, and $x_{0}$ is in that interval, then there exists a solution $x(t)$ to the equation in some interval around $t_{0}$ and that solution is unique.

Numerous generalizations are available to include time dependence, multiple coordinates or both.
#### Autonomous systems
A particularly pleasant case of ODE system is an **autonomous system**, which is a system of autonomous first-order ODEs. These usually arise from equations for individual components of a [[Vector field|vector field]]. Given a vector field $f(\mathbf{x})$, they are written as
$$\dot{\mathbf{x}}=f(\mathbf{x})\tag{1}$$
where bold font is used to remark the fact that $\mathbf{x}$ is a [[Vector space|vector]]. For these kinds of systems, the following theorem holds:

> [!info] Time-shift invariance
> Given an autonomous system, if $\mathbf{x}(t)$ is one of its solutions then $\mathbf{x}'(t)\equiv \mathbf{x}(t-t_{0})$ is also a solution.
> 
> **Proof.** Call $\mathbf{x}(t)$ a solution. Since the system is autonomous, $\dot{\mathbf{x}}(t)=f(\mathbf{x}(t))$ (there is no explicit $t$ in $f$). The derivative is
> $$\dot{\mathbf{x}}'(t)=\frac{d}{dt}\mathbf{x}'(t)=\frac{d}{dt} (\mathbf{x}(t-t_{0}))=\dot{\mathbf{x}}(t-t_{0})=f(\mathbf{x}(t-t_{0}))=f(\mathbf{x}'(t))$$

The name comes from the physical interpretation of $t$ as time. Furthermore, we can also make a strong statement on trajectories:

> [!info] Non-intersection
> The solutions of an autonomous system never intersect.
> 
> **Proof.** Assume that there exists two trajectories $\mathbf{x}_{1}(t)$ and $\mathbf{x}_{2}(t)$ that are both solutions of $(1)$ and that they intersect at some point $\mathbf{x}_{0}$. For instance, $\mathbf{x}_{1}(0)=\mathbf{x}_{0}$ and $\mathbf{x}_{2}(t_{0})=\mathbf{x}_{0}$ for some $t_{0}$. If this is true, then there must exist some third trajectory $\mathbf{x}_{3}(t)=\mathbf{x}_{2}(t+t_{0})$ that's also a solution of $(1)$ due to time-shift invariance, for which $\mathbf{x}_{3}(0)=\mathbf{x}_{0}$. But then there would be two distinct solutions $\mathbf{x}_{1}(t)$ and $\mathbf{x}_{3}(t)$ with the same initial condition. But this can't be, as it violates the existence and uniqueness theorem. Therefore $\mathbf{x}_{1}(t)$ and $\mathbf{x}_{2}(t)$ cannot simultaneously exist.

Equation $(1)$ also has the important property that it forces the derivative of the solution $\dot{\mathbf{x}}(t)$ to always be tangent to the solution $\mathbf{x}(t)$. This can, for example, be seen geometrically by using the definition of derivative:
$$\dot{\mathbf{x}}(t)=\lim_{ \delta t \to 0 } \frac{\mathbf{x}(t+\delta t)-\mathbf{x}(t)}{\delta t}$$
If we draw the vectors manually, we see

![[Diagram Derivative of position vector is tangent|100%]]

If we send $\delta t\to0$, the displacement between the white and red vector become minuscule, which leads $\dot{\mathbf{x}}(t)$ to become tangent. A non-visual proof can for instance be found by taking the derivative of the unit vector of $\mathbf{x}(t)$ and proving that it is always perpendicular to the unit vector itself. In fact, the derivative of any unit vector is perpendicular to the original.
##### Flow of a vector field
Now, given some autonomous system like $(1)$, it is legitimate to ask the following questions: since the solution for a given starting condition is unique, what does that solution look like over all $t$? What if instead of selecting a starting condition, we instead select a specific time; what do all of the possible solutions look at that time?

Answering the first question is rather easy. Since $\mathbf{x}(t)$ is a $\mathbb{R}\mapsto \mathbb{R}^{N}$, it represents a [[Curve|curve]] in $\mathbb{R}^{N}$. It's just the definition of a curve of parameter $t$. This makes sense: intuitively, the trajectory of an object is a curve in space that the object follows, so it's not surprising that this is also the case for all possible dimensions.

Answering the second question is harder. Once we set $t$, we are left with an infinite number of solutions, one for all infinite starting conditions. For a given $t$, we can say that this defines a [[linear map]][^1] $\varphi^{t}:\mathbb{R}^{N}\mapsto \mathbb{R}^{N}$ which takes a starting condition and transforms it into its correlated solution, evaluated at our time $t$. We can write this as $\mathbf{x}_{0}\mapsto \varphi^{t}(\mathbf{x}_{0})\equiv \mathbf{x}(t;\mathbf{x}_{0})$. Thus, for any time $t$, we have a linear map. For all $t$, therefore, we have a *family* of maps, which we can write as $\{ \varphi^{t} \}_{t\in \mathbb{R}}$. This [[set]] is known as the **[[flow]] of a vector field**[^2].

Despite the similar name, this is not quite the same as the better known [[flux]], i.e. the [[Integrale su una superficie|surface integral]] of a vector field over some surface. They are named the same because they both embody the idea of "thing moving through a surface", but they describe it in different ways. Namely, the flux in the ODE sense uses the number of trajectory lines passing through a region of space.
## Examples
Well known cases of ODEs appear in physics frequently. The best known example is [[Newton's laws|Newton's second law]], $\mathbf{F}=m\mathbf{a}$. We call the position vector $\mathbf{r}(t)$, the velocity $\mathbf{v}=\dot{\mathbf{r}}$ and the acceleration $\mathbf{a}=\ddot{\mathbf{r}}$, where we used dot notation to represent the derivative in $t$. A typical form of ODE, for a velocity-dependent force (e.g. [[drag]]), is
$$\mathbf{F}(\mathbf{r},\dot{\mathbf{r}},t)=m \ddot{\mathbf{r}}(t)$$
This can take as many forms as [[physical system|physical systems]] you can think of.
### 1D
In one dimension, where $\mathbf{r}\to x$, we have many interesting examples.

> [!example] Free particle
> A [[free particle]] is
> $$\ddot{x}=0$$
> since there is no force. This resolves to $x(t)=at+b$, where $a$ and $b$ are determined by the starting conditions.

> [!example] Harmonic oscillator
> A [[harmonic oscillator]] is
> $$\ddot{x}=-\omega ^{2}x$$
> This resolves to
> $$x(t)=a\cos(\omega t)+b\sin(\omega t)=A\cos(\omega t+\varphi)=Ce^{i\omega t}+C^{*}e^{-i\omega t}$$
> in various equivalent forms.
> 
> It could have also been written in system form as
> $$\begin{pmatrix}
> \dot{x} \\
> \dot{v}
> \end{pmatrix}=\begin{pmatrix}
> v \\
> -\omega ^{2}x
> \end{pmatrix}$$
> Now let's solve for both position $x$ and velocity $v$. Our trajectory is going to be
> $$\mathbf{x}=\begin{pmatrix}
> x \\
> v
> \end{pmatrix}$$
> For simplicity, set $\omega=1$. Our generic solution is going to be described by the matrix
> $$\mathbf{x}(t;x_{0})=\begin{pmatrix}
> x_{0}\cos t+v_{0}\sin t \\
> -x_{0}\sin t+v_{0}\cos t
> \end{pmatrix}=\varphi^{t}(x_{0},v_{0})$$
> where $x_{0}$ and $v_{0}$ are our starting conditions and $\varphi^{t}$ is a function from $\mathbb{R}^{2}$ to $\mathbb{R}^{2}$. The vector field is
> $$f=\begin{pmatrix}
> v \\
> -x
> \end{pmatrix}$$
> 
> Some example trajectories look like this:
> 
> ![[Plot 1D Harmonic oscillator phase space trajectories]]

> [!example] Harmonic repulsor
> A [[harmonic repulsor]] is
> $$\ddot{x}=\omega ^{2}x$$
> which resolves to
> $$x(t)=a\cosh(\omega t)+b\sinh(\omega t)=Ce^{\omega t}+C^{*}e^{-\omega t}$$

> [!example] Generic linear non-homogeneous
> Linear non-homogeneous ODEs sometimes arise with the form
> $$\ddot{x}=-g$$
> where $g$ is some constant. The [[general solution]] is the sum of the [[partial solution]] of the associated homogeneous equation (where $\ddot{x}=0$). The partial is
> $$x_\text{part}=- \frac{1}{2}gt^{2}$$
> The general, homogeneous solution is
> $$x_\text{gen,hom}=at+b$$
> The final result is the sum of the two:
> $$x(t)=- \frac{1}{2}gt^{2}+at+b$$

> [!example] Pendulum
> The [[simple pendulum]] is
> $$\ddot{x}=-\omega ^{2}\sin(x)$$
> This is a non-linear ODE and is therefore very difficult to solve (but can be solved using [[elliptic functions]]). Typically this is solved by noting that for small $x$, $\sin(x)\simeq x$. In this case, it becomes a usual harmonic oscillator and can be solved exactly.

> [!example] Dampened fall
> Falling through a material with nonzero [[viscosity]] leads to
> $$\ddot{x}=-\beta \dot{x}-g$$
> for some $\beta>0$ and $g$ is the (constant) gravitational acceleration. The partial is $x_\text{part}(t)=-gt/\beta$. The associated general solution ($\ddot{x}=0$) is
> $$x_\text{gen}=- \frac{\alpha}{\beta}e^{-\beta t}+b$$
> with derivative
> $$\dot{x}_\text{gen}=\alpha e^{-\beta t}$$
> If we call $-\alpha/\beta=a$ and $-g/\beta=v_{\infty}$, the final solution is
> $$x(t)=v_{\infty}t+ae^{-\beta t}+b$$
> where $v_{\infty}$ represents the terminal velocity, reached asymptotically after an infinite amount of time falling.

> [!example] Oscillator under external constant force
> A harmonic oscillator under a constant external force leading to a constant acceleration $g$ (e.g. [[Interazione gravitazionale|gravity]]) is
> $$\ddot{x}=-\omega ^{2}x-g$$
> The partial is $x_{p}(t)=-g/\omega$. The associated general is $x_\text{gen}=A\cos(\omega t+\varphi)$. The final solution is
> $$x(t)=A\cos(\omega t+\varphi)- \frac{g}{\omega}$$

> [!example] Dampened harmonic oscillator
> A dampened harmonic oscillator is
> $$\ddot{x}=-\omega ^{2}x-2\mu \dot{x}$$
> for some dampening coefficient $\mu>0$. Solving the characteristic polynomial
> $$\lambda ^{2}+2\mu \lambda+\omega ^{2}=0$$
> leads to
> $$\frac{\Delta}{4}=\mu ^{2}-\omega ^{2}$$
> where $\Delta$ is the discriminant. This is not necessarily real. We identify three cases.
> 
> If $\mu>\omega$ (the dampening is very strong), we have
> $$\lambda_{1,2}=-\mu\pm \sqrt{ \mu ^{2}-\omega ^{2} }<0$$
> Our solution is
> $$x(t)=ae^{\lambda_{1}t}+be^{\lambda_{2}t}$$
> 
> If $\mu<\omega$ (the dampening is weak), we have
> $$\lambda_{1,2}=-\mu\pm i\sqrt{ \omega ^{2}-\mu ^{2} }$$
> and the solution is
> $$x(t)=(a\cos (\sigma t)+b\sin(\sigma t))e^{-\mu t}$$
> where $\sigma=\sqrt{ \omega ^{2}-\mu ^{2} }$.
> 
> If $\mu=\omega$, the oscillator is said to be critically dampened, in which case $\sigma=0$ and the solution can be seen from the weak dampening case as
> $$x(t)=(a+bt)e^{-\mu t}$$

[^1]: Specifically an [[automorphism]].

[^2]: More specifically, this is a [[group]]. The identity is $\varphi^{0}$. The inverse of an element $\varphi^{t}$ is found by flipping the sign of $t$, so $\varphi^{-t}$. The composition rule is given by the sum of times: $\varphi^{t}\circ\varphi^{s}=\varphi^{t+s}$.
