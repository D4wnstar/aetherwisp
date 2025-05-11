---
wiki-publish: true
---
[]()The **binomial distribution** is a real discrete [[probability distribution]] that describes events that can only take two values: true or false, head or tails, etc.. It is described by two parameters: $p$ and $q=1-p$, such that $p+q=1$. For a [[random variable]] $K$, its [[probability mass function]] is
$$P_{k}=P(k;n,p)=\begin{pmatrix}n \\ k\end{pmatrix}p^{k}q^{n-k}$$
using the [[Binomial theorem|binomial coefficient]], hence the name. $k$ must be between $0\leq k\leq n$. $P_{k}$ is the probability that $k$ events will all be true (or head, or anything else), each with probability $p$ of occurring, over $n$ total attempts. For instance, the probability that 6 coin tosses will all result in head is, with probability $p=0.5$ and $q=0.5$:
$$P_{6}=\begin{pmatrix}n \\ 6\end{pmatrix}0.5^{6}0.5^{n-6}$$
Unsurprisingly, as the number of attempts $n$ goes up, the probability that it'll occur also goes up.

It is useful for studying histograms. Given a data sample, the number of events in each bin is a random variable that approximately follows the binomial distribution. Thus, the expected number of events in each bin is $np$ with $p$ the probability of falling in that bin, and [[standard deviation]] $\sqrt{ npq }$.
### Moments
The algebraic [[moment-generating function]] is
$$M_{k}^{*}(t)=E[e^{tK}]=\sum_{k=0}^{n} e^{tk}\begin{pmatrix}n \\ k\end{pmatrix}p^{k}q^{n-k}=\sum_{k=0}^{n} \begin{pmatrix}n \\ k\end{pmatrix}(e^{t}p)^{k}q^{n-k}=(e^{t}p+q)^{n}$$
The central moment-generating function is
$$M_{k}(t)=E[e^{t(K-np)}]=e^{-tnp}M_{k}^{*}(t)=(e^{-tp}e^{t}p+e^{-tp}q)^{n}=(e^{tq}p+e^{-tp}q)^{n}$$

Its [[expected value]] is
$$E[K]=np$$
and its [[variance]] is
$$\text{var}(K)=npq=np(1-p)$$

The [[Function moments|moments]] are
0. $\mu_{0}^{*}=1$
1. $\mu_{1}^{*}=np$ ([[mean]])

0. $\mu_{0}=1$
1. $\mu_{1}=0$
2. $\mu_{2}=npq$ ([[variance]])
3. $\mu_{3}=npq(q-p)$
4. $\mu_{4}=(1-6pq+3npq)npq$

The coefficients are
0. $\gamma_{1}=\frac{q-p}{\sqrt{ npq }}$ ([[skewness]], goes to zero for as $n\to \infty$ or if $p=1/2$)
1. $\gamma_{2}=\frac{1-6pq}{npq}$ ([[kurtosis]], goes to zero for $n\to \infty$)
