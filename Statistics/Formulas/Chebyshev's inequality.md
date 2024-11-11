**Chebyshev's inequality** is an inequality that puts an upper limit to the [[probability]] of a [[random variable]] $X$ taking on a certain value or range of values, depending on its (finite) [[variance]]. It reads
$$P(\lvert X-\mu \rvert \geq \lambda \sigma_{X})\leq \frac{1}{\lambda ^{2}}$$
where $\lambda$ is some positive real number, $\mu$ is the [[expected value]] of $X$ and $\sigma_{X}$ is the [[standard deviation]] of $X$. $\lambda$ is taken to be greater than 1 as cases where $\lambda<1$ are trivial (all probabilities are $<1$ anyway). This result is independent of $X$'s [[probability distribution]].

It is useful to determine the minimum percentage of values that will be found within a given range from the mean; for instance, the inequality states that at least 75% must be within two standard deviation and at least 88.89% of values must be within three standard deviations. The inequality only states the minimum: probability distributions may very well have different (and less uncertain) results. The [[Gaussian distribution]], for example, has 95% of values withing $2\sigma$ and 99.7% of values within $3\sigma$.

> [!example] Proof
> Call $f_{X}(x)$ the [[probability density function]] of $X$. Let's consider another function $h(x)\geq 0$ defined on the [[sample space]] $\Omega$ where $X$ is defined. Let's call $k\geq 0$ some value between the minimum and maximum of $h(x)$ and $R\subset \Omega$ the subset where $h(x)\geq k$. We have
> $$E[h(x)]=\int_{\Omega}h(x)f_{X}(x)\ dx\geq \int_{R}h(x)f_{X}(x)\ dx\geq k\int_{R}f_{X}(x)\ dx=kP(h(x)\geq k)$$
> and thus
> $$P(h(x)\geq k)=\frac{E[h(x)]}{k}$$
> If we call $k=\lambda ^{2}\sigma ^{2}$ and $h(x)=(x-\mu)^{2}$, we get the inequality.
