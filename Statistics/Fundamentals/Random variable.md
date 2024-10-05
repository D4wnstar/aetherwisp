A **random variable** is a physical quantity whose value cannot be known before measurement due to a dependency on random events. What can be known is the [[probability distribution]] that the variable follows, which gives us no information on what the value *is*, but does gives us information on what the value *is likely to be*.

Generally speaking, it is assumed that a random variable is associated with a "true value", that is, the actual, errorless physical quantity that an object or phenomenon possesses and that we then take measurements of. Our measurements are realizations of the random variable associated with the true value, with an error being introduced by our measurement process. It is also possible that no true value even exists and that a quantity is fundamentally statistical even on a physical level. This is paramount in quantum physics, where systems are described by intrinsically probabilistic [[Funzione d'onda|wave functions]], but it may also be something as simple as a die roll.

More formally, a random variable is a function $X:\Omega\to E$ whose domain (called the [[sample space]] $\Omega$) may be either discrete or continuous and includes all possible values that the variable can take, and its image is a [[measure|measurable]] set of numbers $E$. For instance, a coin flip may be describe as the random variable $\text{Coin}:\Omega\equiv\{\text{Head},\text{Tails}\}\to\{1,-1\}$.

Random variables are typically written with a capital letter like $X$, whereas specific values that the variable can take a written in lowercase like $x$.
### Discrete random variables
A discrete random variable $X$ in defined over a discrete sample space $\Omega=\{ x_{1},\ldots,x_{n} \}$ where $n$ may be either finite or infinite. The [[probability]] that $X$ assumes the specific value $x_{i}$ is
$$P_{x_{i}}=P(X=x_{i})\quad\text{for }i\in \{ 1,\ldots,n \}$$
The set of all values of $P$ constitutes the probability distribution $\{ P_{X} \}$ associated with $X$ and the function that maps outcomes to these probabilities is called the [[probability mass function]]. The [[expected value]] $E\equiv \mu$ and [[variance]] $\text{var}\equiv\sigma ^{2}$ are defined as
$$E[X]\equiv\mu_{X}=\sum_{i=1}^{n} P_{i},\quad\text{var}(X)\equiv \sigma ^{2}_{X}=E[(x-\mu_{X})^{2}]=\sum_{i=1}^{n} (x_{i}-\mu_{x})^{2}P_{i}$$
Common discrete probability distributions are the [[binomial distribution]] and the [[Poisson distribution]]. 
### Continuous random variables
A discrete random variable $X$ is defined over a continuous sample space $\Omega=[a,b]$. The edges may or may not be included and the space may also be infinite (i.e. $a=-\infty$ and/or $b=+\infty$). It is nonsensical to define the probability for an exact event occurring: since there are infinite possible events, the probability of any finite number of them is exactly zero. If we call $n$ the total number of possibile outcomes, we write
$$\lim_{ n \to \infty } P=\lim_{ n \to \infty } \frac{1}{n}=0$$
What we can define is the probability that $X$ will give a value in a certain interval $[x_{1},x_{2}]$. Since we are working with continuous values, we represent this as an integral over a specific function over the interval $[x_{1},x_{2}]$:
$$P(x_{1}\leq X\leq x_{2})=\int_{x_{1}}^{x_{2}}f(x)dx$$
The function $f(x)$ is called the [[probability density function]] of the distribution. The expectation value $E\equiv\mu$ and the variance $\text{var}\equiv \sigma ^{2}$ are defined as
$$E[X]\equiv \mu_{X}=\int_{\Omega_{X}}xf(x)dx,\quad\text{var}(X)\equiv \sigma ^{2}_{X}=E[(x-\mu_{X})^{2}]=\int_{\Omega_{X}}(x-\mu_{X})^{2}f(x)dx$$
The most common continuous probability distribution is the [[Gaussian distribution]].