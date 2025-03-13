The **wave equation** is a second order linear [[partial differential equation]] in space and time. In one spatial dimension $x$, it reads
$$\frac{ \partial ^{2} \psi(x,t) }{ \partial x^{2} }=\frac{1}{v^{2}}\frac{ \partial ^{2}\psi (x,t) }{ \partial t^{2} } \tag{1}$$
$\psi(x,t)$ is the [[scalar field]] solution to the equation and it is called the **wavefunction**, whereas the parameter $v$ is generally interpreted in physics as the **speed of the wave** (although the concept of wave speed is more complicated). The value of $\psi$ for any $x$ and $t$ is called the **amplitude** of the wave in that place and time[^1]. In multiple spatial dimensions, the equation quickly generalizes using the [[Laplacian]]:
$$\nabla ^{2}\psi(\mathbf{x},t)=\frac{1}{v^{2}}\frac{ \partial ^{2} \psi(\mathbf{x},t) }{ \partial t^{2} } \tag{2}$$
The wave equation finds numerous applications in physics, primarily in the study of [[electromagnetic wave|electromagnetic waves]] in electrodynamics and the study of [[Funzione d'onda|wavefunctions]] of the [[Equazione di Schrödinger|Schrödinger equation]] in quantum mechanics.
### Properties
Wavefunctions are complicated objects and there myriad variations in their behavior in different conditions. Say for simplicity we remain in one dimension, where $\psi(x,t)$ is our wave function.

The "shape" of the wave is given by the function evaluated at a specific time. That gets rid of the time dependency and returns the amplitude of the wave over space; "amplitude over space" is really  what we're saying when we talk about shape. In the simplest possible configuration, the wave "holds its shape" as it travels in space. Such a wave is said to be **nondispersive**, and the converse is pretty intuitively said to be **dispersive**. In these pleasant situations, the shape is given by evaluating at $t=0$ (or any time really): $\psi(x,0)=f(x)$. We call $f(x)$ the **profile** of the wave.

Given the profile and the claim that it remains identical over time, we can construct the general form of the wavefunction by hand. After all, since the shape doesn't change (no [[scaling]]) and we are in one dimension (no [[Rotation|rotations]]), the only geometric operation we can do is shifting, that is, moving the entire thing left or right. Since $v$ is our speed, the shift is just what you'd expect it to be, $x'=x\pm vt$. Then, our wavefunction must be:
$$\psi(x,t)=\psi(x\pm vt,0)=f(x\pm vt)\tag{3}$$
As usual for geometry, the signs can be confusing: $-$ is for a wave moving *forward* (towards positive $x$) and $+$ is for a wave moving *backwards* (towards negative $x$). This is just a byproduct of algebra, don't think too much of it. Conveniently, we have proper names for these cases: waves moving forward $\psi(x,t)=f(x-vt)$ are said to be **progressive waves**, whereas those moving backwards $\psi(x,t)=f(x+vt)$ are said to be **regressive waves**.

Of course, we constructed our solution arbitrarily here. We have no proof that it is a *valid* solution of $(1)$. Thankfully, by just substituting $(3)$ in $(1)$ it is immediately verified by noticing that $\frac{ \partial \psi }{ \partial t }=\frac{ \partial f }{ \partial t }$:
$$\frac{ \partial ^{2}\psi }{ \partial t^{2} }=\pm v\frac{ \partial  }{ \partial x' } \frac{ \partial f }{ \partial t } = \pm v\frac{ \partial  }{ \partial x' } \left( \frac{ \partial \psi }{ \partial t } \right)=\pm v\frac{ \partial  }{ \partial x' } \left( \pm v\frac{ \partial f }{ \partial x' }  \right)=v^{2}\frac{ \partial ^{2}f }{ \partial x^{2} } =v^{2}\frac{ \partial ^{2} \psi }{ \partial ^{2} x} $$
### Harmonic waves
An incredibly useful set of wavefunctions are the **harmonic waves**, or just **harmonics**. They are purely sinusoidal nondispersive waves:
$$\psi(x,t)=A\sin(k(x\pm vt))$$
for some constant $A>0$ representing the maximum amplitude of the wave and $k>0$, called the **wave number** (the modulo of a vector quantity called **[[wave vector]]**) , representing the spatial frequency of the wave (if you prefer, how many peaks there are per unit space at a fixed time). The true benefit of these waves isn't that they are common in nature (in fact, these are extremely theoretical objects), but that by way of a [[Serie di Fourier|Fourier series]], *any wave can be decomposed into a sum of harmonics*. Take literally any phenomenon you can describe as a wave and that phenomenon can be described as an infinite sum of harmonics. This works for truly anything: a complex quantum system is solved, at least in principle, in the same way as the waves of an ocean or a chord played of a piano.

Common examples of ways harmonics may be written are
$$\begin{align}
&\psi(x,t)=A\sin(k(x\pm vt))&\psi(x,t)=A\sin\left( 2\pi\left( \frac{x}{\lambda}\pm \frac{t}{\tau} \right) \right) \\
&\psi(x,t)=A\sin(2\pi(hx\pm \nu t))&\psi(x,t)=A\sin(kx\pm \omega t)
\end{align}$$
We've already seen the wavenumber $k$, which is also called the **angular spatial frequency**. $\lambda$ is the **[[wavelength]]** of the wave, $\tau$ is the **oscillation period**, $h$ is the **spatial frequency**, $\nu$ is the **[[frequency]]** (in time) and $\omega$ is the **[[Frequency|angular frequency]]**. These are all interconnected and the choice of parameters is just a matter of convenience; the most typical is the last one, with $k$ and $\omega$. The formulas for these are
$$\lambda=\frac{2\pi}{k},\quad h=\frac{k}{2\pi}=\frac{1}{\lambda},\quad \nu=\frac{1}{\tau}=\frac{\omega}{2\pi},\quad \omega=\frac{2\pi}{\tau}=2\pi \nu$$

[^1]: This is assuming $\psi$ is a real-valued function. It if is complex-valued, as is the case for all quantum mechanical [[Funzione d'onda|wavefunctions]], then the square modulo $\lvert \psi \rvert^{2}$ is the amplitude.
