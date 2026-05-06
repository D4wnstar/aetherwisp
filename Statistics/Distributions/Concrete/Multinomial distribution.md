---
hl-publish: true
---
The **multinomial distribution** is a discrete multivariate [[Probability distribution]] that acts as the many-outcome extension to the [[binomial distribution]]. Whereas the binomial distribution models events with two outcomes (e.g., true or false), the multinomial distribution models events with an arbitrary number of outcomes.

For $M$ [[Random variable|random variables]] $K_{1},\ldots,K_{M}$, the [[joint distribution function]] of having $n$ total outcomes, divided exactly in $k_{i}$ occurrences per type, each with probability $p_{i}$ of occurring, is
$$P(k_{1},\ldots,k_{M};n,p_{1},\ldots,p_{M})= \frac{n!}{k_{1}!\ldots k_{M}!}p_{1}^{k_{1}}\ldots p_{M}^{k_{M}}$$
For a more compact notation, define $\mathbf{k}=(k_{1},\ldots,k_{M})$ and $\mathbf{p}=(p_{1},\ldots,p_{M})$ and rewrite as
$$P(\mathbf{k};n,\mathbf{p})=\frac{n!}{\prod_{i=1}^{M} k_{i}!}\prod_{i=1}^{M} p_{i}^{k_{i}}$$
If the binomial distribution can be seen as modeling coin flips, the multinomial distribution can be seen as modelling a fair $M$-sided die rolls.
### Moments
The [[Expected value]] and [[Variance]] of the $i$-th random variable are
$$E[K_{i}]=np_{i},\qquad \text{var}(K_{i})=np_{i}(1-p_{i})$$
Both are the same as the binomial distribution for that variable. The [[Covariance]] between two random variables is
$$\text{cov}(K_{i},K_{j})=-np_{i}p_{j}$$
and the correlation coefficient is
$$\rho=-\sqrt{ \frac{p_{i}p_{j}}{(1-p_{i})(1-p_{j})} }$$
Notice the negative sign. All outcomes are anticorrelated: this is because if one event occurs, the others don't, and viceversa. This means that if one outcome count goes up, the others must go down (or technically, not increase).
### Variable $n$
The above results hold if $n$ is a constant. It is possible to extend the description by treating $n$ as variable. As an illustrative example, say you have 2 hours of time to take measurements of a random event (e.g., [[Particle decay|particle decay]], lightning sightings, etc.), the amount of measurements you'll take, which is $n$, is of course not known in advance (it's random). Instead, as long as the events are mutually independent, they are [[Poisson distribution|Poisson distributed]] and the phenomenon is a [[Poisson process]], with expected value $\nu$ as
$$P(n)=\frac{e^{-\nu}}{n!}\nu^{n}$$
We can use the multinomial to find the distribution of $n$ such that there are $k_{1}$ events of type 1, $k_{2}$ events of type 2, etc. The probability distribution is the product the above Poisson distribution and the multinomial:
$$\begin{align}
P(n,\mathbf{k};\mathbf{p})&=\frac{e^{-\nu}}{\cancel{ n! }}\nu^{n} \frac{\cancel{ n! }}{k_{1}!\ldots k_{M}!}p_{1}^{k_{1}}\ldots p_{M}^{k_{M}} \\
&=\frac{1}{k_{1}!\ldots k_{M}!}e^{-\nu}(\nu p_{1})^{k_{1}}\ldots(\nu p_{n})^{k_{M}} \\
&=\frac{e^{-\nu p_{1}}}{k_{1}!}(\nu p_{1})^{k_{1}}\ldots \frac{e^{-\nu p_{n}}}{k_{M}!}(\nu p_{M})^{k_{M}}
\end{align}$$
achieved by using $\sum_{i=1}^{M}p_{i}=1$ and $\sum_{i=1}^{M}k_{i}=n$. Combining the last line in product notation yields
$$P(n,\mathbf{k};\mathbf{p})=\prod_{i=1}^{M} \frac{e^{-\nu p_{i}}}{k_{i}!}(\nu p_{i})^{k_{i}}$$
