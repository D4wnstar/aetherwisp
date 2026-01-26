---
wiki-publish: true
---
A **moment-generating function** (**MGF**) of a [[Random variable]] $X$ is a real-valued function whose derivatives are the [[Function moments|moments]] of that variable's [[Probability distribution]]. There exists both **raw** (or **algebraic**) and **central** moment-generating functions. They are respectively defined as
$$M_{X}^{*}(t)=\text{E}[e^{tX}]=\int_{\Omega}e^{tx}f_{X}(x)\ dx\qquad\text{(raw)}$$
$$M_{X}(t)=\text{E}[e^{t(X-\mu_{X})}]=\int_{\Omega}e^{t(x-\mu_{X})}f_{X}(x)\ dx\qquad\text{(central)}$$
where $\text{E}[\cdot]$ is the [[Expected value|expectation operator]], $\mu_{X}$ is the [[mean]] of $X$, $f_{X}(x)$ is the [[Probability density function]] and integration occurs over the [[sample space]] $\Omega$. A continuous variable is assumed here; for discrete variables, just change the definition of $\text{E}[\cdot]$ accordingly and use a [[Probability mass function]] instead. The two are bound by the following equality:
$$M_{X}(t)=e^{-t\mu_{X}}M_{X}^{*}(t)$$
Proof is trivial: notice that $e^{t(x-\mu_{X})}=e^{tx}e^{-t\mu_{X}}$ and extract the second term from the integral of $M_{X}(t)$.

To understand the connection to moments, we can express them in a [[serie di potenze|power series]] by expanding the [[exponential series]]:
$$M_{X}^{*}(t)=\int_{\Omega}e^{tx}f_{X}(x)\ dx=\sum_{n=0}^{\infty} \frac{t^{n}}{n!}\int_{\Omega}x^{n}f_{X}(x)\ dx=\sum_{n=0}^{\infty} \frac{t^{n}}{n!}\mu_{n}^{*} $$
where $\mu_{n}^{*}$ is the $n$-th order raw moment. The same applies to $M_{X}(t)$. We can extract $\mu$ by just taking $n$-th derivative for $t^{n}$ and evaluating in $t=0$:
$$\mu^{*}_{n}=\left.\frac{ \partial ^{n}M^{*}_{X} }{ \partial t^{n} } \right|_{t=0},\qquad \mu_{n}=\left.\frac{ \partial ^{n}M_{X} }{ \partial t^{n} } \right|_{t=0}$$
### Properties
- Since the set of all moments fully determines the probability distribution, and the MGF allows one to find all moments, the MGF determines the distribution completely.
- If two random variables $X$ and $Y$ have MGFs $M_{X}(t)$ and $M_{Y}(t)$ that are equal in at least a small interval around $t=0$, then $X=Y$.
- If $X$ and $Y$ are [[Independent variables|independent]], then $M_{X+Y}(t)=M_{X}(t)M_{Y}(t)$.
- A random variable may not have an MGF. This is, for instance, the case for variables following the [[Cauchy distribution]]. In these cases, it's always possible to use the [[Characteristic function|characteristic function]] instead.