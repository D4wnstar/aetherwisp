---
wiki-publish: true
aliases:
  - wavefunction
---
The **wave equation** is a second-order linear [[partial differential equation]] in space and time that describes [[wave]] phenomena. In one spatial dimension $x$, it reads
$$\frac{ \partial ^{2} \psi(x,t) }{ \partial x^{2} }=\frac{1}{v^{2}}\frac{ \partial ^{2}\psi (x,t) }{ \partial t^{2} } \tag{1}$$
$\psi(x,t)$ is the [[scalar field]] solution to the equation and it is called the **wavefunction**, whereas the parameter $v$ is generally interpreted in physics as the **speed of the wave** (although the concept of wave speed is more complicated; see [[phase velocity]] and [[group velocity]]). The value of $\psi$ for any $x$ and $t$ is called the **[[amplitude]]** of the wave in that place and time[^1]. In multiple spatial dimensions, the equation quickly generalizes using the [[Laplacian]]:
$$\nabla ^{2}\psi(\mathbf{x},t)=\frac{1}{v^{2}}\frac{ \partial ^{2} \psi(\mathbf{x},t) }{ \partial t^{2} } \tag{2}$$
It can also be written in an extremely terse manner using the [[d'Alembertian]] operator:
$$\square ^{2} \psi(\mathbf{x},t)=0$$
This form in particular makes it easy to see that, in a way, the wave equation is actually nothing more than a generalized [[Laplace's equation]]. In fact, just like how Laplace's equation is generalized to [[Poisson's equation]], the wave equation can be itself generalized to
$$\square ^{2}\psi(\mathbf{x},t)=f$$
for some real-valued function $f$. This is known as the **inhomogeneous** wave equation, as opposed to the **homogeneous** wave equation when $f=0$.

The wave equation finds numerous applications in physics, such as in the study of [[electromagnetic wave|electromagnetic waves]] in electrodynamics and the study of [[Funzione d'onda|wavefunctions]] of the [[Equazione di Schrödinger|Schrödinger equation]] in quantum mechanics.
### Introduction
Wavefunctions are complicated objects and there are a myriad variations in their behavior in different conditions. This makes them exceptionally useful, as they can model an incredible range of phenomena across many different branches of science, but it also makes them somewhat daunting to approach at first.

Say for simplicity we remain in one dimension, where $\psi(x,t)$ is our wave function. The "shape" of the wave is given by the function evaluated at a specific time. That gets rid of the time dependency and returns the amplitude of the wave over space; "amplitude over all space" is really what we're saying when we talk about shape. In the simplest possible configuration, the wave "holds its shape" as it travels in space. Such a wave is said to be **nondispersive**, and the converse is pretty intuitively said to be **[[dispersion|dispersive]]**. In pleasant nondispersive situations, the shape is found quite easily by evaluating at $t=0$ (or any time really): $\psi(x,0)=f(x)$. We call $f(x)$ the **profile** of the wave. The motion of the wave itself is then just shifting $f(x)$ to the left and right at some known speed.

Given the profile and the claim of nondispersion, we can construct the general form of the wavefunction by hand. After all, since the shape doesn't change (no [[scaling]]) and we are in one dimension (no [[Rotation|rotations]]), the only geometric operation we can do is, as we said, shifting, that is, moving the entire thing left or right. Since $v$ is our speed, the shift after some time $t$ is just what you'd expect it to be, $x'=x\pm vt$. Then, our wavefunction must be:
$$\psi(x,t)=\psi(x\pm vt,0)=f(x\pm vt)\tag{3}$$
This is the essence of a nondispersive waves. If you're mathematically inclined, they are a specific subset of functions that are dependent on both time and space, but *specifically* only as $x\pm vt$. This is how you distinguish a generic function of time and space from a nondispersive wave. In practice, they are functions of a *single* variable $x\pm vt$.

As is often the case in geometry, the signs can be confusing: $-$ is for a wave moving *forward* (towards positive $x$) and $+$ is for a wave moving *backwards* (towards negative $x$). This is just a byproduct of algebra, don't think too much of it. Conveniently, we have proper names for these cases: waves moving forward $\psi(x,t)=f(x-vt)$ are said to be **progressive waves**, whereas those moving backwards $\psi(x,t)=f(x+vt)$ are said to be **regressive waves**.

Of course, we constructed our solution somewhat arbitrarily here. We have no proof that it is a *valid* solution of $(1)$. Thankfully, the proof is just a matter of substituting $(3)$ in $(1)$ and is immediately verified by noticing that $\partial \psi/\partial t=\partial f/\partial t$:
$$\frac{ \partial ^{2}\psi }{ \partial t^{2} }=\pm v\frac{ \partial  }{ \partial x' } \frac{ \partial f }{ \partial t } = \pm v\frac{ \partial  }{ \partial x' } \left( \frac{ \partial \psi }{ \partial t } \right)=\pm v\frac{ \partial  }{ \partial x' } \left( \pm v\frac{ \partial f }{ \partial x' }  \right)=v^{2}\frac{ \partial ^{2}f }{ \partial x^{2} } =v^{2}\frac{ \partial ^{2} \psi }{ \partial ^{2} x} $$
It is of course true for both progressive and regressive waves. But notice how the wave equation is linear: different possible solutions of such an equation can be [[Linear combination|linearly combined]] and the combination is itself a solution. Thus, the *general* solution to the one-dimensional wave equation must be
$$\psi(x,t)=\alpha f(x-vt)+\beta g(x+vt)$$
for some (doubly [[Differential|differentiable]]) functions $f$ and $g$ and some constants $\alpha$ and $\beta$.

[^1]: This is assuming $\psi$ is a real-valued function. It if is complex-valued, as is the case for all quantum mechanical [[Funzione d'onda|wavefunctions]], then the square modulo $\lvert \psi \rvert^{2}$ is the amplitude.