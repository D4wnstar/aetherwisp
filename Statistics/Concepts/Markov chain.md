---
hl-publish: true
---
A **Markov chain** is a stateless statistical process. A Markov chain is fully defined by the state at the start of each step and does not need to "remember" any previous state. In a Markov chain, the [[Probability]] that a [[Random variable]] $X$ will take all the values in a sequence $(x_{1},\ldots,x_{N})$ in $N$ steps is
$$P_{N}(x_{1},\ldots,x_{N})=p_{1}(x_{1})\prod_{t=2}^{N-1} W(x_{t}\to x_{t+1})$$
where $p_{1}(x_{1})$ is the probability of starting at state $x_{1}$ and $W$ is called the **transition probability function**, which changes a random variable's state. Note how $W$ determines how the chain runs and how it is only dependent on the current state: there is no "memory". A stateless process is generally said to be **Markovian**. A Markovian [[time series]] is commonly also said to have **short memory**.
### Properties
- The quantity $P_{N}$ can be interpreted as the [[Joint distribution function]] of $N$ random variables $X_{1},\ldots,X_{N}$. These variables are not [[Independent variables|independent]] since the value of one is needed to determine the value of the next.
- In a Markov chain, the variables of the sequence are [[Independent variables|conditionally independent]]. This is because each variable is only [[Covariance|correlated]] with the previous one. The [[Conditional distribution function]] of the $i$-th step is
  $$f(x_{i}|x_{1},\ldots,x_{i-1})=f(x_{i}|x_{i-1})$$
  This property is used to prove the definition at the start of this article by using the general definition of joint distribution function.
