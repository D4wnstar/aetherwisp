The **Gamma function** or **Euler's Gamma function** $\Gamma(z)$ is a complex-valued function defined over the entire complex plane. It is the [[analytic continuation]] of the factorial function and is defined as
$$\Gamma(z)=\int_{0}^{\infty}w^{z-1}e^{-w}dw$$
Some notable values are
$$\Gamma\left( \frac{1}{2} \right)=\sqrt{ \pi },\quad \Gamma(1)=1,\quad \Gamma(z+1)=n\Gamma(z),\quad \Gamma(n)=(n-1)!$$

> [!example] Proof for $\Gamma(z+1)=z\Gamma(z)$
> $$\Gamma(z)=\int_{0}^{\infty}w^{z}e^{-w}dw=-w^{z}e^{-w}|_{0}^{\infty}+\int_{0}^{\infty}zw^{z-1}e^{-w}dw=z\Gamma(z-1)$$
