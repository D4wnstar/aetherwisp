---
wiki-publish: true
---
The **law of large number** is a law that states that the [[arithmetic mean]] of an [[iid]] random [[sample]] is guaranteed to converge to the [[expected value]] as the sample size becomes infinite.

More formally, the law actually has two statements: the **strong law of large numbers** and the **weak law of large numbers**.

> [!info] Weak law of large numbers
> Given a sample of $n$ iid random variables $X_{1},\ldots,X_{n}$ with finite [[expected value]] $\mathrm{E}[X]= \mu$, the sample mean [[convergence in probability|converges in probability]] to the true mean as the sample size $n$ approaches infinity:
> $$\bar{X}_{n}\xrightarrow{P}\mu$$
> In other terms, given an arbitrarily small $\varepsilon$:
> $$\lim_{ n \to \infty } P(\lvert \bar{X}-\mu \rvert \geq \varepsilon)=0$$
> where $P$ is a [[measure]] of probability.

> [!info] Strong law of large numbers
> Given a sample of $n$ iid random variables $X_{1},\ldots,X_{n}$ with finite expected value $\mathrm{E}[X]=\mu$, the sample mean [[almost sure convergence|converges almost surely]] to the true mean as the sample size $n$ approaches infinity:
> $$\bar{X}_{n}\xrightarrow{\text{a.s.}}\mu$$
> In other terms,
> $$P(\lim_{ n \to \infty } \bar{X}_{n}=\mu)=1$$
> where $P$ is a measure of probability.
