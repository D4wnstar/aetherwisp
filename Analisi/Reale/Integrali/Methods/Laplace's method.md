---
wiki-publish: true
aliases:
  - saddle point method
---
**Laplace's method** is a technique used to approximate integrals of the form
$$\int_{a}^{b}e^{Mf(x)}\ dx$$
where $M$ is a large constant and $f(x)$ is a twice-[[Differential|differentiable]] function with a unique global maximum. $a$ and $b$ may be infinite.

Laplace's method can be generalized to work on [[Integrale su una curva|path integrals]] over the complex plane. This generalization is known as the **saddle point method**.
### Theory
Call $x_{0}$ the global maximum of $f(x)$. We can [[Taylor series|Taylor expand]] $f(x)$ around that point and stop at the second order
$$f(x)\simeq f(x_{0})+f'(x_{0})(x-x_{0})+ \frac{1}{2}f''(x_{0})(x-x_{0})^{2}$$
but since $x_{0}$ is a [[Punto critico|stationary point]], $f'(x_{0})=0$, so we get
$$f(x)\simeq f(x_{0})+ \frac{1}{2}f''(x_{0})(x-x_{0})^{2}$$
Since $x_{0}$ is a maximum, in that point we have $f''(x_{0})\leq 0$. For points in the neighborhood of $x_{0}$, we can approximately state
$$f(x)\simeq f(x_{0})- \frac{1}{2}|f''(x_{0})|(x-x_{0})^{2}$$
If we plug this in the integral we get
$$\int_{a}^{b}e^{Mf(x)}\ dx\simeq e^{Mf(x_{0})}\int_{a}^{b}e^{- \frac{1}{2}M|f''(x_{0})|(x-x_{0})^{2}}\ dx$$
If we replace $a$ and $b$ with $-\infty$ and $+\infty$ (if they weren't already) as if $M$ is large, the integral far from $x_{0}$ is almost zero, so there is little difference. Doing so makes it into a [[Gaussian integral]] (an integral of a function like $e^{-x^{2}}$), which can be solved as
$$\boxed{\int_{a}^{b}e^{Mf(x)}\ dx\simeq \sqrt{ \frac{2\pi}{M|f''(x_{0})|} }e^{Mf(x_{0})}}$$
which becomes more and more precise as $M\to \infty$.