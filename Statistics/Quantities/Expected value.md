---
wiki-publish: true
---
The **expected value** or **expectation** $\text{E}[X]$ of a [[random variable]] $X$ is a generalization of a weighted average over all possible values the variable can take. It is what the word "[[mean]]" typically refers to in the context of statistics, though there's many other possible meanings. It is the first raw [[Function moments|moment]] of the [[probability distribution]].

The name can be misleading: the expected value is not the most likely value (that would be the [[mode]]). It is strictly theoretical and may not even be an allowed value of the random variable: for instance, the expected value of a fair six-sided die is 3.5, which is not on the die. The name "expectation" refers to both the value $\text{E}[X]$ itself and the [[operatore|operator]] $\text{E}$ that is applied onto $X$.

The definition differs between discrete and continuous variables, and also between countable and uncountable outcomes.
### Discrete variable with finite outcomes
Given a discrete random variable $X$ with a finite set of possible outcomes $\{ x_{1},\ldots,x_{N} \}$, with a [[probability mass function]] $p_{X}(x)$, the expected value is
$$\text{E}[X]=x_{1}p_{X}(x_{1})+\ldots+x_{n}p_{X}(x_{n})=\sum_{i=1}^{N} x_{i}p_{X}(x_{i})$$
which is just the average weighted by the probability of an outcome.
### Discrete variable with countably infinite outcomes
In the same conditions as above, but with a countably infinite set of outcomes $\{ x_{i} \}_{i}$, the expected value can be easily defined by extending the sum as an infinite [[Serie|series]]:
$$\text{E}[X]=\sum_{i=1}^{\infty} x_{i}p_{X}(x_{i})$$
The [[Riemann series theorem]] states that the convergence value of some series with both positive and negative terms depends on the order in which the terms are given in. Since random variables are just that, random, it isn't possible to determine what order the terms are given in. Thus, this definition only holds if the series [[Absolute convergence|converges absolutely]], in which case the order is not important. If the series is not absolutely convergent, this definition may not hold. If it doesn't (i.e. the series diverges), it is said that the variable does not have finite expectation.
### Continuous variable
Given a continuous random variable $X$ with a [[probability density function]] $f_{X}(x)$, the expected value is
$$\text{E}[X]=\int_{-\infty}^{\infty} xf_{X}(x) \ dx$$
Similarly to the series above, integrals may diverge, in which case the variable does not have finite expectation.
### Properties
The expectation has some useful properties:
- If $X>0$ then $\text{E}[X]>0$.
- Linearity: $\text{E}[aX+bY]=a\text{E}[X]+b\text{E}[Y]$, where $a$ and $b$ are constants.
- Monotonicity: If $X\leq Y$, then $\text{E}[X]\leq \text{E}[Y]$.
- If $X=Y$, then $\text{E}[X]=\text{E}[Y]$.
- If $\text{E}[\lvert X \rvert]=0$ then $X=0$.
- If $X=c$ for a constant $c$, then $\text{E}[X]=c$. As a consequence, since the expectation is a constant, the expectation operator is [[idempotence|idempotent]]: $\text{E}[\text{E}[X]]=\text{E}[X]$.
- $\text{E}[XY]\neq \text{E}[X]\text{E}[Y]$ in general. It is only guaranteed to be equal if $X$ and $Y$ are [[independent variables]], though it may also be true if they are dependent.