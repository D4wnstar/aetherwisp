---
wiki-publish: true
---
A **moment-generating function** (**MGF**) of a [[random variable]] $X$ is a real-valued function whose derivatives are the [[Function moments|moments]] of that variable's [[probability distribution]]. There exists both algebraic (raw) and central moment-generating functions. They are respectively defined as
$$M_{X}^{*}(t)=E[e^{tX}]=\int_{\Omega}e^{tx}f_{X}(x)\ dx\qquad\text{(algebraic)}$$
$$M_{X}(t)=E[e^{t(X-\mu_{X})}]=\int_{\Omega}e^{t(x-\mu_{X})}f_{X}(x)\ dx\qquad\text{(central)}$$
where $E[\cdot]$ is the [[Expected value|expectation operator]], $\mu_{X}$ is the [[mean]] of $X$ and $f_{X}(x)$ is the [[probability density function]]. Here a continuous variable is assumed; for discrete variables, just change the definition of $E[\cdot]$ and use a [[probability mass function]] instead. The two are bound by the following equality:
$$M_{X}(t)=e^{-t\mu_{X}}M_{X}^{*}(t)$$

To see the connection to moments, we can expand them in a [[serie di potenze|power series]] by expanding the exponential inside of the integral:
$$M_{X}^{*}(t)=E[e^{tX}]=\int_{\Omega}e^{tx}f_{X}(x)\ dx=\sum_{k=0}^{\infty} \frac{t^{k}}{k!}\int_{\Omega}x^{k}f_{X}(x)\ dx=\sum_{k=0}^{\infty} \frac{t^{k}}{k!}\mu_{k}^{*} $$
where $\mu_{k}^{*}$ is the $k$-th order algebraic moment. The same applies to $M_{X}(t)$. We can extract $\mu$ by just taking $k$-th derivative for $t^{k}$ and evaluating in $t=0$:
$$\mu^{*}_{k}=\left.\frac{ \partial ^{k}M^{*}_{X} }{ \partial t^{k} } \right|_{t=0},\qquad \mu_{k}=\left.\frac{ \partial ^{k}M_{X} }{ \partial t^{k} } \right|_{t=0}$$

It is occasionally possible that a random variable has no MGF. This is, for instance, the case for the [[Cauchy distribution]]. In these cases, we can fall back to the [[characteristic function (probability theory)|characteristic function]].