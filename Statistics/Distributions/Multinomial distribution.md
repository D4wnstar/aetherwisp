The **multinomial distribution** is a real, multivariate [[probability distribution]] which describes the probability of an event occurring in different ways, such as a $n$-sided dice landing on each of its face. It is the multivariate extension of the [[binomial distribution]], which only handles events with boolean outcomes, like a coin toss. For $m$ [[random variable|random variables]] $K_{1},\ldots,K_{n}$, the [[probability mass function]] of having $n$ total outcomes, divided exactly in $k_{i}$ occurrences per type (such as a specific dice roll), each with probability $p_{i}$ of occurring, is
$$P(k_{1},\ldots,k_{n})= \frac{n!}{k_{1}!\ldots k_{m}!}p_{1}^{k_{1}}\ldots p_{m}^{k_{m}}=\frac{n!}{\prod_{i=1}^{m} k_{i}!}\prod_{i=1}^{m} p_{m}^{k_{m}}$$
### Moments
The [[expected value]] for the $i$-th random variable is
$$E[K_{i}]=np_{i}$$
and the [[variance]] is
$$\text{var}(K_{i})=np_{i}(1-p_{i})$$
The [[covariance]] between two random variables is
$$\text{cov}(K_{i},K_{j})=-np_{i}p_{j}$$
and the correlation coefficient is
$$\rho=- \frac{np_{i}p_{j}}{\sqrt{ np_{i}(1-p_{i})np_{j}(1-p_{j}) }}=-\sqrt{ \frac{p_{i}p_{j}}{(1-p_{i})(1-p_{j})} }$$
### Variable $n$
The above results hold if $n$ is a predefined constant. This is not always true, however: say you have 2 hours of time to take measurements of a random event (i.e. [[Decadimento di particelle|particle decay]], the amount of measurements you'll take, that is $n$, is not defined. Instead, it is [[Poisson distribution|Poisson distributed]], with expected value $\nu$ as
$$P(n)=\frac{e^{-\nu}}{n!}\nu^{n}$$
We can use the multinomial to find the distribution of the value of $n$ such that there are $k_{1}$ events of type 1, $k_{2}$ events of type 2, etc. The probability distribution is
$$\begin{align}
P(n,k_{1},\ldots,k_{n})&=\frac{e^{-\nu}}{\cancel{ n! }}\nu^{n} \frac{\cancel{ n! }}{k_{1}!\ldots k_{m}!}p_{1}^{k_{1}}\ldots p_{m}^{k_{m}} \\
&=\frac{1}{k_{1}!\ldots k_{n}!}e^{-\nu}(\nu p_{1})^{k_{1}}\ldots(\nu p_{n})^{k_{m}} \\
&=\frac{e^{-\nu p_{1}}}{k_{1}!}(\nu p_{1})^{k_{1}}\ldots \frac{e^{-\nu p_{n}}}{k_{m}!}(\nu p_{m})^{k_{m}} \\
&=\prod_{i=1}^{m} \frac{e^{-\nu p_{i}}}{k_{i}!}(\nu p_{i})^{k_{i}}
\end{align}$$
using $\sum_{i=1}^{m}p_{i}=1$ and $\sum_{i=1}^{m}k_{i}=n$.