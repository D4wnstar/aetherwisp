The **Poisson distribution** is a real univariate discrete [[probability distribution]] is the limit of the [[binomial distribution]] where $n\to \infty$ but the number of successes remains constant (that is, $np\to \nu$). It describes rare events: events which have a very low probability of occurring even over many trials. It has a single parameter $\nu \in[0,1]$ and its [[probability mass function]] is
$$P_{k}=P(k;\nu)=\frac{\nu^{k}e^{-\nu}}{k!}$$
### Moments
The algebraic [[moment-generating function]] is
$$M_{k}^{*}(k)=\sum_{k=1}^{n} e^{tk} \frac{\nu^{k}e^{-\nu}}{k!}=e^{-\nu}\sum_{k=0}^{n} \frac{1}{k!}(\nu e^{t})^{k}=e^{-\nu}e^{\nu e^{t}}=e^{-\nu(1-e^{t})}$$
The central moment-generating function is
$$M_{k}(t)=e^{-t\nu}e^{-\nu(1-e^{t})}=e^{\nu(e^{t}-1-t)}$$
The algebraic moments are
$$\mu^{*}_{1}=\nu$$
The central moments are
$$\mu_{2}=\nu,\quad \mu_{3}=\nu,\quad \mu_{4}=3\nu ^{2}+\nu$$
The [[asymmetry coefficient]] is
$$\gamma_{1}=\frac{\mu_{3}}{\mu_{2}^{3/2}}=\frac{1}{\sqrt{ n }}$$
which means that it tends to become symmetrical only when the number of sample events is very high. The [[kurtosis]] is
$$\gamma_{2}=\frac{\mu_{4}}{\mu_{2}^{2}}-3=\frac{\nu}{\nu ^{2}}=\frac{1}{\nu}$$
which also tends to flatten the tails for a high number of events. In fact, the Poisson distribution tends to the [[Gaussian distribution]] for a large number of events by way of the [[central limit theorem]].
### As limit of the binomial distribution
Let's consider the binomial distribution's MGF
$$M_{kB}^{*}(t)=(e^{t}p+q)^{n}=[(e^{t}-1)p+1]^{n}$$
and its expectation value $E[k]=np$. But $np\to \nu$ in the Poisson distribution (so for $n\to \infty$), so we can write $E[k]=\nu$. Thus, $p=\nu/n$. If we plug this in the MGF we get
$$M_{kB}^{*}(t)=\left[ (e^{t}-1) \frac{\nu}{n}+1 \right]^{n}$$
which for $n\to \infty$ tends to the Poisson MGF.