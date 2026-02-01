---
wiki-publish: true
---
The **binomial distribution** is a real discrete [[Probability distribution]] that describes events that can only take two values: true or false, head or tails, etc.. It is described by one parameter: $p$, which is the [[Probability]] of one of the two values occurring. We also define $q=1-p$, which is the probability of the other value occurring.

For a [[Random variable]] $K$, the binomial [[Probability mass function]] is
$$P_{k}=P(k;n,p)=\begin{pmatrix}n \\ k\end{pmatrix}p^{k}q^{n-k}$$
using the [[Binomial theorem|binomial coefficient]], hence the name. It is the probability that $k$ events will all be the desired value (true, head...) over $n$ total attempts. $k$ must be between $0\leq k\leq n$.
### Moments
The raw [[moment-generating function]] is
$$M_{K}^{*}(t)=E[e^{tK}]=\sum_{k=0}^{n} e^{tk}\begin{pmatrix}n \\ k\end{pmatrix}p^{k}q^{n-k}=\sum_{k=0}^{n} \begin{pmatrix}n \\ k\end{pmatrix}(e^{t}p)^{k}q^{n-k}=(e^{t}p+q)^{n}$$
The central moment-generating function is
$$M_{K}(t)=E[e^{t(K-np)}]=e^{-tnp}M_{k}^{*}(t)=(e^{-tp}e^{t}p+e^{-tp}q)^{n}=(e^{tq}p+e^{-tp}q)^{n}$$
Some [[Function moments|moments]] are:
- Raw
	0. $\mu_{0}^{*}=1$
	1. $\mu_{1}^{*}=np$ ([[Expected value]])
- Central
	0. $\mu_{0}=1$
	1. $\mu_{1}=0$
	2. $\mu_{2}=npq$ ([[Variance]])
	3. $\mu_{3}=npq(q-p)$
	4. $\mu_{4}=(1-6pq+3npq)npq$
- Coefficients
	0. $\gamma_{1}=\frac{q-p}{\sqrt{ npq }}$ ([[skewness]], goes to zero for as $n\to \infty$ or if $p=1/2$)
	1. $\gamma_{2}=\frac{1-6pq}{npq}$ ([[kurtosis]], goes to zero for $n\to \infty$)
### Relation to other distributions
- For $n=1$, we get a [[Bernoulli distribution]], $\text{Bernoulli}(x;p)$.
- When the sample size becomes large ($n\to \infty$) but the number of successes doesn't increase ($np\to \nu$), it becomes a [[Poisson distribution]], $\text{Pois}(x;np)$.
### Histograms
The binomial distribution has a special connection to histograms. Given a data [[sample]], the number of events in each bin is a random variable that approximately follows the binomial distribution. Thus, the expected number of events in each bin is $np$ where $p$ is the probability of falling in that bin, and [[standard deviation]] $\sqrt{ npq }$. It is possible to find $p$ through the [[cumulative distribution function]] $F(x)$ as $p=F(x_{i+1})-F(x_{i})$, where $x_{i}$ and $x_{i+1}$ are the left and right edges of the $i$-th bin.

This property is useful to analyze the dispersion of a histogram and how far it is from the intended distribution. This method is used in the Pearson goodness-of-fit [[chi-square test]].

If the sample is very large and the bins are small (as in, low width), it's also possible to use the [[Poisson distribution]].
### Examples
> [!example]- Fair coin tosses
> The probability that 6 coin tosses will all result in head is, with probability $p=0.5$ and $q=0.5$:
> $$P_{6}=\begin{pmatrix}n \\ 6\end{pmatrix}0.5^{6}0.5^{n-6}$$
> Unsurprisingly, as the number of attempts $n$ goes up, the probability that it'll occur also goes up.
