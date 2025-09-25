---
wiki-publish: true
---
The **binomial distribution** is a real discrete [[probability distribution]] that describes events that can only take two values: true or false, head or tails, etc.. It is described by one parameter: $p$, which is the [[probability]] of one of the two values occurring. We also define $q=1-p$, which is the probability of the other value occurring.

For a [[random variable]] $K$, the binomial [[probability mass function]] is
$$P_{k}=P(k;n,p)=\begin{pmatrix}n \\ k\end{pmatrix}p^{k}q^{n-k}$$
using the [[Binomial theorem|binomial coefficient]], hence the name. It is the probability that $k$ events will all be the desired value (true, head...) over $n$ total attempts. $k$ must be between $0\leq k\leq n$.

It is useful for studying histograms. Given a data sample, the number of events in each bin is a random variable that approximately follows the binomial distribution. Thus, the expected number of events in each bin is $np$ with $p$ the probability of falling in that bin, and [[standard deviation]] $\sqrt{ npq }$.

> [!example]- Fair coin tosses
> The probability that 6 coin tosses will all result in head is, with probability $p=0.5$ and $q=0.5$:
> $$P_{6}=\begin{pmatrix}n \\ 6\end{pmatrix}0.5^{6}0.5^{n-6}$$
> Unsurprisingly, as the number of attempts $n$ goes up, the probability that it'll occur also goes up.
### Moments
The algebraic [[moment-generating function]] is
$$M_{k}^{*}(t)=E[e^{tK}]=\sum_{k=0}^{n} e^{tk}\begin{pmatrix}n \\ k\end{pmatrix}p^{k}q^{n-k}=\sum_{k=0}^{n} \begin{pmatrix}n \\ k\end{pmatrix}(e^{t}p)^{k}q^{n-k}=(e^{t}p+q)^{n}$$
The central moment-generating function is
$$M_{k}(t)=E[e^{t(K-np)}]=e^{-tnp}M_{k}^{*}(t)=(e^{-tp}e^{t}p+e^{-tp}q)^{n}=(e^{tq}p+e^{-tp}q)^{n}$$

Its [[expected value]] is
$$\text{E}[K]=np$$
and its [[variance]] is
$$\text{var}(K)=npq=np(1-p)$$

The [[Function moments|moments]] are
0. $\mu_{0}^{*}=1$
1. $\mu_{1}^{*}=np$ ([[expected value]])

2. $\mu_{0}=1$
3. $\mu_{1}=0$
4. $\mu_{2}=npq$ ([[Variance]])
5. $\mu_{3}=npq(q-p)$
6. $\mu_{4}=(1-6pq+3npq)npq$

The coefficients are
0. $\gamma_{1}=\frac{q-p}{\sqrt{ npq }}$ ([[skewness]], goes to zero for as $n\to \infty$ or if $p=1/2$)
1. $\gamma_{2}=\frac{1-6pq}{npq}$ ([[kurtosis]], goes to zero for $n\to \infty$)
### Relation to other distributions
When $n=1$, it simplifies to the [[Bernoulli distribution]].