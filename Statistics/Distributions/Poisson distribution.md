The **Poisson distribution** is a real discrete [[probability distribution]] is the limit of the [[binomial distribution]] where $n\to \infty$ but the number of successes remains constant (that is, $np\to \nu$). It describes rare events: events which have a very low [[probability]] of occurring even over many trials. It has a single parameter $\nu \in[0,1]$. For a [[random variable]] $K$, the [[probability mass function]] is
$$P_{k}=P(k;\nu)=\frac{\nu^{k}e^{-\nu}}{k!}$$

The Poisson distribution tends to the [[Gaussian distribution]] for a large number of events. This is proven by the [[central limit theorem]].

The Poisson distribution is commonly used for event counting. Suppose there are on average $\nu$ independent events per unit time, and thus $\nu\Delta t$ total events in the time interval $\Delta t$. The random variable $K$ is the number of events in $\Delta t$, following the Poisson distribution. To prove this, divide the interval in $n$ sufficiently small, evenly-spaced steps $\delta t=\Delta t/n$ such that the probability of two or more events occurring is zero. Each one of the $n$ intervals has either zero or one event happen in it and the probability of having one event is given by the binomial distribution $p=\nu \delta t$, with [[expected value]] $E[K]=\nu \Delta t$. If we add infinitely many intervals ($n\to \infty$) and send the probability of an event in each to zero ($p\to0$) to keep their product constant, we get the Poisson distribution.
### Moments
The algebraic [[moment-generating function]] is
$$M_{K}^{*}(k)=\sum_{k=1}^{n} e^{tk} \frac{\nu^{k}e^{-\nu}}{k!}=e^{-\nu}\sum_{k=0}^{n} \frac{1}{k!}(\nu e^{t})^{k}=e^{-\nu}e^{\nu e^{t}}=e^{-\nu(1-e^{t})}$$
The central moment-generating function is
$$M_{K}(t)=e^{-t\nu}e^{-\nu(1-e^{t})}=e^{\nu(e^{t}-1-t)}$$

The [[Function moments|moments]] are
0. $\mu_{0}^{*}=1$
1. $\mu^{*}_{1}=\nu$ ([[mean]])

0. $\mu_{0}=1$
1. $\mu_{1}=0$
2. $\mu_{2}=\nu$ ([[variance]])
3. $\mu_{3}=\nu$
4. $\mu_{4}=3\nu ^{2}+\nu$

The coefficients are
1. $\gamma_{1}=1/\sqrt{ n }$ ([[skewness]], tends to become symmetrical when the number of sample events is very high)
2. $\gamma_{2}=1/\nu$ ([[kurtosis]], tends to flatten the tails for a high number of events)
### Properties
- It is [[Normalizzazione|normalized]], with normalization constant $c=1$
### As limit of the binomial distribution
Let's consider the binomial distribution's MGF
$$M_{kB}^{*}(t)=(e^{t}p+q)^{n}=[(e^{t}-1)p+1]^{n}$$
and its expectation value $E[k]=np$. But $np\to \nu$ in the Poisson distribution (so for $n\to \infty$), so we can write $E[k]=\nu$. Thus, $p=\nu/n$. If we plug this in the MGF we get
$$M_{kB}^{*}(t)=\left[ (e^{t}-1) \frac{\nu}{n}+1 \right]^{n}$$
which for $n\to \infty$ tends to the Poisson MGF.