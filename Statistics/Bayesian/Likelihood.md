---
wiki-publish: true
---
The **likelihood function** or **likelihood** is the probability of observing data given the parameters of the model used to estimate it. If we consider a random variable $X$ and a model with parameters $\theta$, the probability of an outcome $x$ of $X$ given those parameters is
$$x \rightarrow P(x|\theta)$$
and the likelihood of the parameters given $x$ is
$$\theta \rightarrow P(\theta|x):= L(\theta|x)$$
which can be interpreted as the confidence level in the parameters $\theta$ after observing $x$.  
The likelihood is a key component of [[Bayes' theorem]], where it is multiplied by the [[Prior]] to obtain the [[Posterior]].