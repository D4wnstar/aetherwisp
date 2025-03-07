---
aliases:
  - ODE
---
An **ordinary differential equation**, or **ODE** for short, is an equation where a function and one or more its derivatives appear simultaneously. The highest derivative of the function is said to be the **order** of the ODE. If we denote the function as $f(t)$ and its $i$-th derivative as $f^{(i)}(t)$, a generic ODE written in **normal form** (with the highest derivative isolated) is
$$f^{(n)}(t)=g(f,f^{(1)},\ldots,f^{(n-1)},t)$$
where $g$ is some function.

An ODE is said to be **autonomous** if the ODE has no explicit dependence on $t$ (although all the $f(t)$ still do). In this case, $g$ is not dependent on $t$.
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

The benefit of doing things this way is that first-order ODEs have a large amount of theorems and results that make them far easier to solve and much more reliable to work with. For an example, the following theorem underlies much of the study of these equations.

> [!info] Existence and uniqueness theorem
> Given a first-order ODE $\dot{x}=f(x,t)$ and a starting condition $x(t_{0})=x_{0}$, there exists a solution $x(t)$ and that solution is unique.
#### Autonomous systems
A particularly pleasant case of ODE system is an **autonomous system**, which is a system of first-order ODEs, one for each component of a [[Campo vettoriale|vector field]]. Given a vector field $f(\mathbf{x})$, they are written as
$$\dot{\mathbf{x}}=f(\mathbf{x})\tag{1}$$
If a system is autonomous, the following theorem holds:

> [!info] Time-shift invariance
> Given an autonomous system, if $x(t)$ is a solution of $(1)$ then $x'(t)\equiv x(t-t_{0})$ is also a solution.
> 
> **Proof.** Call $x(t)$ a solution. Since the system is autonomous, $\dot{x}(t)=f(x(t))$ (there is no explicit $t$ in $f$). The derivative is
> $$\dot{x}'(t)=\frac{d}{dx}x'(t)=\dot{x}(t-t_{0})=f(x(t-t_{0}))=f(x'(t))$$

The name comes from the physical interpretation of $t$ as time. Furthermore, we can also make a strong statement on trajectories:

> [!info] Non-intersection
> The solutions of an autonomous system never intersect.
> 
> **Proof.** Assume that there exists two trajectories $\mathbf{x}_{1}(t)$ and $\mathbf{x}_{2}(t)$ that are both solutions of $(1)$ such that they intersect at some point $\mathbf{x}_{0}$. For instance, $\mathbf{x}_{1}(0)=\mathbf{x}_{0}$ and $\mathbf{x}_{2}(t_{0})=\mathbf{x}_{0}$. If this is true, then there must exist some third trajectory $\mathbf{x}_{3}(t)=\mathbf{x}_{2}(t+t_{0})$ that's also a solution of $(1)$ due to time-shift invariance. But then there would be two distinct solutions $\mathbf{x}_{1}(t)$ and $\mathbf{x}_{2}(t)$ such that $\mathbf{x}_{1}(0)=\mathbf{x}_{0}$ and $\mathbf{x_{3}}(0)=\mathbf{x}_{0}$. But this can't be, as it violates the theorem of existence and uniqueness. Therefore $\mathbf{x}_{1}(t)$ and $\mathbf{x}_{2}(t)$ cannot simultaneously exist.

> [!info] Flux of the vector field
> Given some point $\mathbf{x}_{0}\in \mathbb{R}^{N}$, there exists one and only one solution $\mathbf{x}(t;\mathbf{x}_{0})$ such that $\mathbf{x}(0;\mathbf{x_{0}})=\mathbf{x}_{0}$.

Given some $\mathbf{x_{0}}$, the solution of $(1)$ traces a [[Curva|curve]] in $\mathbb{R}^{N}$ parameterized by $t$. Meanwhile, given some $t$, $\mathbf{x}(t;\mathbf{x}_{0})$ is a function of $\mathbf{x}_{0}$ and it describes a map $\varphi^{t}:\mathbb{R}^{N}\to \mathbb{R}^{N},\ \mathbf{x}_{0}\to \varphi^{t}(\mathbf{x}_{0})=\mathbf{x}(t;\mathbf{x}_{0})$. Such a map exists for any $t$. In fact, the set of all $\varphi^{t}$ for all $t$ is known in mathematics as a **family** of maps $\{ \varphi^{t} \}_{t\in \mathbb{R}}$ from $\mathbb{R}^{N}$ to $\mathbb{R}^{N}$. This specific family is known as the **flux of the vector field**. This is not quite the same as the more typical flux, i.e. the [[Integrale su una superficie|surface integral]] of the vector field over some surface. They are named the same because they both embody the idea of "thing moving through surface", but they describe in different ways. Namely, this flux-as-a-family uses the number of trajectory lines passing through a region of space.

The equation $(1)$ also has the important property that it forces the derivative of the solution $\dot{\mathbf{x}}(t)$ to always be tangent to the solution $\mathbf{x}(t)$.
## Examples
Well known cases of ODEs appear in physics frequently. The best known example is [[Newton's laws|Newton's second law]], $\mathbf{F}=m\mathbf{a}$. We call the position vector $\mathbf{r}(t)$, the velocity $\mathbf{v}=\dot{\mathbf{r}}$ and the acceleration $\mathbf{a}=\ddot{\mathbf{r}}$, where we used dot notation to represent the derivative in $t$. A typical form of ODE, for a velocity-dependent force (e.g. [[drag]]), is
$$\mathbf{F}(\mathbf{r},\dot{\mathbf{r}},t)=m \ddot{\mathbf{r}}(t)$$
This can take as many forms as [[physical system|physical systems]] you can think of.
### 1D
In one dimension, where $\mathbf{r}\to x$, we have many interesting examples.
#### Free particle
A [[free particle]] is
$$\ddot{x}=0$$
since there is no force. This resolves to $x(t)=at+b$, where $a$ and $b$ are determined by the starting conditions.
#### Harmonic oscillator
A [[harmonic oscillator]] is
$$\ddot{x}=-\omega ^{2}x$$
This resolves to
$$x(t)=a\cos(\omega t)+b\sin(\omega t)=A\cos(\omega t+\varphi)=Ce^{i\omega t}+C^{*}e^{-i\omega t}$$
in various equivalent forms.

It could have also been written in system form as
$$\begin{pmatrix}
\dot{x} \\
\dot{v}
\end{pmatrix}=\begin{pmatrix}
v \\
-\omega ^{2}x
\end{pmatrix}$$

Now let's solve for both position $x$ and velocity $v$. Our trajectory is going to be
$$\mathbf{x}=\begin{pmatrix}
x \\
v
\end{pmatrix}$$
For simplicity, set $\omega=1$. Our generic solution is going to be described by the matrix
$$\mathbf{x}(t;x_{0})=\begin{pmatrix}
x_{0}\cos t+v_{0}\sin t \\
-x_{0}\sin t+v_{0}\cos t
\end{pmatrix}=\varphi^{t}((x_{0},v_{0}))$$
where $x_{0}$ and $v_{0}$ are our starting conditions and $\varphi^{t}$ is a function from $\mathbb{R}^{2}$ to $\mathbb{R}^{2}$. The vector field is
$$f=\begin{pmatrix}
v \\
-x
\end{pmatrix}$$

Some example trajectories look like this:

![[Plot 1D Harmonic oscillator phase space trajectories]]
#### Harmonic repulsor
A [[harmonic repulsor]] is
$$\ddot{x}=\omega ^{2}t$$
which resolves to
$$x(t)=a\cosh(\omega t)+b\sinh(\omega t)=Ce^{\omega t}+C^{*}e^{-\omega t}$$
#### Generic linear non-homogeneous
Linear non-homogeneous ODEs sometimes arise with the form
$$\ddot{x}=-g(x)$$
The [[general solution]] is the sum of the [[partial solution]] of the associated homogeneous equation (where $\ddot{x}=0$). The partials are
$$x_\text{part}=- \frac{1}{2}gt^{2}$$
The general, homogeneous solution is
$$x_\text{general,hom}=at+b$$
The final result is
$$x(t)=- \frac{1}{2}gt^{2}+at+b$$
#### Pendulum
The [[simple pendulum]] is
$$\ddot{x}=-\omega ^{2}\sin(x)$$
This is a non-linear ODE and is therefore very difficult (if possible) to solve. Typically this is solved by noting that for small $x$, $\sin(x)\simeq x$. In this case, it becomes linear and can be solved exactly.
#### Dampened fall
Falling through a material with nonzero [[viscosity]] leads to
$$\ddot{x}=-\beta \dot{x}-g$$
for some $\beta>0$. The partial is $x_\text{part}(t)=-gt/\beta$. The associated general solution ($\ddot{x}=0$) is
$$x_\text{gen}=- \frac{\alpha}{\beta}e^{-\beta t}+b$$
with derivative
$$\dot{x}_\text{gen}=\alpha e^{-\beta t}$$
If we call $-\alpha/\beta=a$ and $-g/\beta=v_{\infty}$, the final solution is
$$x(t)=v_{\infty}t+ae^{-\beta t}+b$$
where $v_{\infty}$ represents the terminal velocity, reached asymptotically after an infinite amount of time falling.
#### Oscillator under external force
A harmonic oscillator under an external force $g$ is
$$\ddot{x}=-\omega ^{2}x-g$$
The partial is $x_{p}(t)=-g/\omega$. The associated general is $x_\text{gen}=A\cos(\omega t+\varphi)$. The final solution is
$$x(t)=A\cos(\omega t+\varphi)- \frac{g}{\omega}$$
#### Dampened harmonic oscillator
A dampened harmonic oscillator is
$$\ddot{x}=-\omega ^{2}x-2\mu \dot{x}$$
for some dampening coefficient $\mu>0$. Solving the characteristic polynomial
$$\lambda ^{2}+2\mu \lambda+\omega ^{2}=0$$
leads to
$$\frac{\Delta}{4}=\mu ^{2}-\omega ^{2}$$
where $\Delta$ is the discriminant. This is not necessarily real. We identify three cases.

If $\mu>\omega$ (i.e. the dampening is very strong), we have
$$\lambda_{1,2}=-\mu\pm \sqrt{ \mu ^{2}-\omega ^{2} }<0$$
Our solution is
$$x(t)=ae^{\lambda_{1}t}+be^{\lambda_{2}t}$$

If $\mu<\omega$ (i.e. the dampening is weak), we have
$$\lambda_{1,2}=-\mu\pm i\sqrt{ \omega ^{2}-\mu ^{2} }$$
and the solution is
$$x(t)=(a\cos (\sigma t)+b\sin(\sigma t))e^{-\mu t}$$
where $\sigma=\sqrt{ \omega ^{2}-\mu ^{2} }$.

If $\mu=\omega$, the oscillator is said to be critically dampened, in which case $\sigma=0$ and the solution can be seen from the weak dampening case as
$$x(t)=(a+bt)e^{-\mu t}$$
