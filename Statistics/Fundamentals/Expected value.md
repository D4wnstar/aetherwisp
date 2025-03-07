The **expected value** or **expectation** $E[X]$ of a [[random variable]] $X$ is a generalization of a weighted average over all possible values the variable can take. Despite the name, the expected value is strictly theoretical and may not even be achievable in the real world: for instance, the expected value of a fair six-sided die is 3.5, which is not even on the die itself. It does *not* represent the most *likely* value to occur: that would be the [[mode]]. The name "expectation" refers to both the value $E[X]$ itself and the [[operatore|operator]] $E$ that is applied onto $X$.

The definition differs between discrete and continuous variables, and also between countable and uncountable outcomes.
### Discrete variable with finite outcomes
Given a discrete random variable $X$ with a finite set of possible outcomes $\{ x_{1},\ldots,x_{n} \}$, with a [[probability mass function]] $p_{X}(x)$, the expected value is
$$E[X]=x_{1}p_{X}(x_{1})+\ldots+x_{n}p_{X}(x_{n})=\sum_{i=1}^{n} x_{i}p_{X}(x_{i})$$
which is just the average weighted by the probability of an outcome.
### Discrete variable with infinite countable outcome
In the same conditions as above, but with a countably infinite set of outcomes $\{ x_{i} \}_{i}$, the expected value can be easily defined by extending the sum as an infinite [[Serie|series]]:
$$E[X]=\sum_{i=1}^{\infty} x_{i}p_{X}(x_{i})$$
The [[Riemann series theorem]] states that the convergence value of some series with both positive and negative terms depends on the order in which the terms are given in. Since random variables are just that, random, it isn't possible to determine what order the terms are given in. Thus, this definition only holds if the series [[Absolute convergence|converges absolutely]], in which case the order is not important. If the series is not absolutely convergent, this definition may not hold. If it doesn't (i.e. the series diverges), it is said that the variable does not have finite expectation.
### Continuous variable
Given a continuous random variable $X$ with a [[probability density function]] $f_{X}(x)$, the expected value is
$$E[X]=\int_{-\infty}^{\infty} xf_{X}(x) \ dx$$
Similarly to the series above, integrals may diverge, in which case the variable does not have finite expectation.
### Properties
The expectation has some useful properties:
- If $X>0$ then $E[X]>0$.
- Linearity: $E[aX+bY]=aE[X]+bE[Y]$, where $a$ and $b$ are constants.
- Monotonicity: If $X\leq Y$, then $E[X]\leq E[Y]$.
- If $X=Y$, then $E[X]=E[Y]$.
- If $E[\lvert X \rvert]=0$ then $X=0$.
- If $X=c$ for a constant $c$, then $E[X]=c$. As a consequence, since the expectation is a constant, the expectation operator is [[idempotence|idempotent]]: $E[E[X]]=E[X]$.
- $E[XY]\neq E[X]E[Y]$ in general. It is only guaranteed to be equal if $X$ and $Y$ are [[independent variables]], though it may also be true if they are dependent.