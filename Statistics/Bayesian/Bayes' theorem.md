---
wiki-publish: true
---
**Bayes' theorem** is the central theorem of Bayesian statistics and relates [[Joint distribution function|joint probability distributions]] with [[Conditional distribution function|conditional distributions]]. For two [[random variable|random variables]] $X$ and $Y$, Bayes' theorem states
$$P(y|x)=\frac{P(x|y)P(y)}{P(x)}=\frac{P(x,y)}{P(x)}$$
The notable consequence of this theorem is that it allows one to invert a conditional probability into a joint probability, which makes it possible to determine the probability of the cause of an event from its effect.
### For parameter estimation
Bayes' theorem can be adapted to be used specifically for parameter estimation. In this form, it states that the *posterior distribution*, or simply the [[Posterior]], is given by
$$P(p|dM)=\frac{P(d|pM)P(p|M)}{P(d|M)}$$
where $d$ is the measured data, $M$ represents the model in use (a statistical distribution) and $p$ are the parameters of that model (e.g., mean and variance for the distribution). Each term in the equation has its own interpretation:
- $P(d|pM)$ is the *likelihood function*, simply called [[Likelihood]].
- $P(p|M)$ is the *prior knowledge*, or simply [[Prior]], which quantifies what we know about the model before measuring the data.
- $P(d|M)$ is the *evidence* (*marginalized likelihood*), computed by integrating the likelihood over all possible parameter values the posterior can take.
- The posterior distribution $P(p|dM)$, or [[Posterior]], represents the probability that the model parameters take a certain value. In other words, the posterior combines our prior knowledge with the insights gained from measurements (the likelihood).
