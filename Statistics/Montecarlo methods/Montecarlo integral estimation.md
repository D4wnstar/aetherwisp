Consider the integral of some univariate function $g(x)$ of a continuous [[random variable]] $X$ in the interval $[a,b]$:
$$I=\int _{a}^{b}g(x) \ dx $$
The trick is to multiply and divide by a function $f(x)$ like so:
$$I=\int _{a}^{b} \frac{g(x)}{f(x)}f(x) \ dx =E\left[ \frac{g(X)}{f(X)} \right]$$
using the [[expected value]]. $f(x)$ must be [[Normalizzazione|normalized]] over $[a,b]$, so that $\int_{a}^{b}f(x)\ dx=1$, and non-negative, which essentially makes it a [[probability density function]].

We know how to estimate an expectation by sampling a large [[sample]] of $N$ numbers $x_{1},\ldots,x_{N}$ from $f(x)$. Therefore our estimate $\hat{I}$ of $I$ is
$$\hat{I}=\frac{1}{N}\sum_{i=1}^{N} \frac{g(x_{i})}{f(x_{i})}$$
with [[variance]]
$$\sigma ^{2}_{\hat{I}}=\frac{\sigma ^{2}_{g/f}}{N},\qquad \sigma ^{2}_{g/f}=\frac{1}{N-1}\left\{  \sum_{i=1}^{N} \left[ \left( \frac{g(x)/f(x)}{N} \right)^{2} \right] - \hat{I}^{2}  \right\}$$
and so our final result is
$$I=\hat{I}\pm \sigma_{\hat{I}}$$

If we $f(x)$ is a multiple of $g(x)$, so that $g(x)/f(x)=c$ for some constant $c$, we have $g(x)=cf(x)$, so
$$\int_{a}^{b}g(x)\ dx=c\int _{a}^{b}f(x) \ dx =c$$
In this case $\sigma ^{2}_{g/f}=0$. This gives a selection criterion to pick $f(x)$: it's whatever distribution is closest to the distribution of $g(x)$, i.e. the one that minimizes $\sigma ^{2}$.
### Examples
> [!example] Standard normal integral
> Say to test the method we want to calculate the integral of a [[Gaussian distribution|standard normal distribution]] between $[-1,1]$. We have
> $$\begin{align}
> I&=\int_{-1}^{1} \frac{e^{-x^{2}/2}}{\sqrt{ 2\pi }}\ dx= 0.68268\ldots \\
> &=\int_{0}^{1} \underbrace{ \frac{2e^{-x^{2}/2}}{\sqrt{ 2\pi }} }_{ g(x) } \ dx=\int_{0}^{1}g(x)\ dx
> \end{align}
> $$
> by using symmetry arguments. The above numerical result is the correct number we want to aim for. Now that we have a $g(x)$ to work with, let's pick a distribution $f(x)$ to use. Of course, using a standard normal distribution would be the best choice here, since they would be a multiple of each other, but for the sake of argument, let's try with a [[uniform distribution]] and an [[exponential distribution]]. Numerically, we get
> $$\begin{matrix}
 \text{Distribution} & N=100 & N=1000 \\
> \hat{I}_\text{unif} & 0.682\pm 0.010 & 0.6820\pm 0.0010 \\
> \hat{I}_\text{exp} & 0.6855\pm 0.0024 & 0.6828\pm 0.0003
> \end{matrix}$$
> These are all compatible with the [[true value]], but the exponential distribution provides better results (lower variance at equal sample sizes).
