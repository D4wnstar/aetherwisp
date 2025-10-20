---
wiki-publish: true
---
The **likelihood function** or **likelihood** is the probability of observing data given the parameters of the [[Statistics/Modeling/Model|model]] used to estimate it. If we consider a [[random variable]] $X$ and a model with parameters $\boldsymbol{\theta}$, the probability of an observation $x$ of $X$ given those parameters is
$$x \rightarrow P(x|\boldsymbol{\theta})$$
and the likelihood $L$ of the parameters given $x$ is
$$\theta \rightarrow P(\boldsymbol{\theta}|x)\equiv L(\boldsymbol{\theta}|x)$$
which can be interpreted as the confidence level in the parameters $\boldsymbol{\theta}$ after observing $x$. We are asking the question "given the observation $x$, what is the probability that the process that generated it has parameters $\boldsymbol{\theta}$ under our model?"

The likelihood is a key component of [[Bayes' theorem]], where it is multiplied by the [[prior]] to obtain the [[posterior]].