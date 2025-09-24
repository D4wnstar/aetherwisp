---
wiki-publish: true
---
**Euler's method** is a simple but imprecise method for numerical integration. In essence, it consists of following a [[vector field]] in small, discrete steps that can be computed numerically. In one dimension, given a first order autonomous [[Ordinary differential equation|ODE]] $\dot{x}=f(x)$ and a starting condition $x(t_{0})=x_{0}$, Euler's method states that, after a small amount of time $\Delta t$, the point will be in $x(t_{0}+\Delta t)\simeq x_{1}=x_{0}+f(x_{0})\Delta t$. Then, we apply the step again to get $x_{2}$, $x_{3}$, and so on. In general, the update rule is
$$x_{n+1}=x_{n}+f(x_{n})\Delta t\tag{1}$$
The method is quite simple, but also quite imprecise unless $\Delta t$ is extremely small and is therefore not recommended for anything other than examples or introductions.
### Improved Euler's method
It is possible to improve the method by noting that its main source of imprecision is due to evaluating the derivative only at the start of the step (i.e. at $x_{n}$) instead of throughout. Of course, we can't evaluate the derivative everywhere (at that point you might as well just set a smaller $\Delta t$), but we can evaluate it both before and after the step, then pick the average of the two.

Say we do the usual Euler's step $(1)$:
$$\tilde{x}_{n+1}=x_{n}+f(x_{n})\Delta t$$
but now, we don't stop here. We consider $\tilde{x}_{n+1}$ to only be an (imprecise) estimate of where the next point will be. While we won't move there directly, it's "close enough" to the correct location that it's "derivative" $f(\tilde{x}_{n+1})\Delta t$ provides us a precious bit of information on how the system should behave. Thus, we can use this to adapt our update rule to
$$x_{n+1}=x_{n}+ \frac{1}{2}[f(x_{n})+f(\tilde{x}_{n+1})]\Delta t\tag{2}$$
This is the **improved Euler's method**, which relies on information from both before the step and after the step using a trial update, averaging the derivatives to get a better estimate. It's more computation (two steps per update instead of one), but the error per step — defined as $E=\lvert x(t_{n})-x_{n} \rvert$ where $x(t_{n})$ is the exact value and $x_{n}$ is the numerically estimated one — is smaller for a given step size $\Delta t$ than the regular method. More specifically, the Euler method is *first order*, $E\propto \Delta t$, and the improved version is *second order*, $E\propto(\Delta t)^{2}$.