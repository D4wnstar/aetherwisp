---
wiki-publish: true
---
The **Runge-Kutta methods** (**RK** for short) are a family of numerical integration methods of a variety of orders, the most popular of which is the **fourth-order Runge-Kutta method**. They are essentially evolutions of [[Euler's method]], using specifically chosen quantities and points to estimate to increase the order of the method (and thus the precision) in some instances at the cost of more computation.

Despite their age, RK methods are very commonly used thanks to their strong versatility, good enough precision and ease of implementation. More modern methods, like [[predictor-corrector method|predictor-corrector methods]] or [[Bulirsch-Stoer method|Bulirsch-Stoer methods]], can be more efficient and precise in some instances, but require more effort to implement and aren't always the best choice.
### Fourth-order Runge-Kutta
The fourth-order Runge-Kutta method is a very popular variant of the RK methods due to ease of implementation and excellent results. As the name suggests, it is a fourth order method and requires four evaluations per physics step. For a one-dimensional autonomous [[Ordinary differential equation|ODE]] $\dot{x}=f(x)$ and a timestep $\Delta t$, the update rule from point $x_{n}$ to $x_{n+1}$ is given by
$$\begin{align}
k_{1}&=f(x_{n})\Delta t \\
k_{2}&=f\left( x_{n}+ \frac{1}{2}k_{1} \right)\Delta t \\
k_{3}&=f\left( x_{n}+ \frac{1}{2}k_{2} \right)\Delta t \\
k_{4}&=f(x_{n}+k_{3})\Delta t \\
x_{n+1}&=x_{n}+ \frac{1}{6}(k_{1}+2k_{2}+2k_{3}+k_{4})
\end{align}$$
