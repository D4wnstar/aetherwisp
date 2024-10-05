The **variance** $\sigma ^{2}$ of a [[random variable]] $X$ is a measure of its [[dispersion]]. It is defined as the [[expected value]] of the square of the deviation from the [[mean]] $E[X]=\mu$:
$$\text{var}(X)\equiv\sigma ^{2}_{X}=E[(X-\mu)^{2}]$$
The variance can also be expressed as
$$\begin{align}
\text{var}(X)&=E[(X-E[X])^{2}] \\
&=E[X^{2}-2XE[X]+E[X]^{2}] \\
&=E[X^{2}]-2E[X]E[X]+E[X]^{2} \\
&=E[X^{2}]-E[X]^{2}
\end{align}$$
### Discrete random variable
Given a discrete random variable $X$ with [[probability mass function]] $p_{X}(x)$ of expected value $\mu$, the variance is
$$\text{var}(X)=\sum_{i=1}^{n} p_{X}(x_{i})(x_{i}-\mu)^{2}$$
