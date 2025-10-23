---
wiki-publish: true
---
The **likelihood function** or simply **likelihood** is the probability of observing a specific set of data given the parameters of the [[Statistics/Modeling/Model|model]] used to estimate it. If we consider a [[random variable]] $X$ and a model with parameters $\boldsymbol{\theta}$, the [[probability]] of observing $x$ from $X$ given those parameters is
$$\mathbf{x} \mapsto P(x|\boldsymbol{\theta})$$
We can invert the relationship to find the probability (*likelihood*) $\mathcal{L}$ of observing parameters $\boldsymbol{\theta}$ given an observation $x$:
$$\theta \mapsto P(\boldsymbol{\theta}|x)\equiv \mathcal{L}(\boldsymbol{\theta}|x)$$
which can be interpreted as the confidence level in the parameters $\boldsymbol{\theta}$ after observing $x$. We are asking the question "given the observation $x$, what is the probability that the process that generated it has parameters $\boldsymbol{\theta}$ under our model?" More commonly, the likelihood is evaluated over a [[sample]] of observations $\{ x_{i} \}_{i\in \mathbb{N}}\equiv \mathbf{x}$ in order to [[Parameter estimation|fit]] the model on that data.

Given some statistical model $f(\mathbf{x};\boldsymbol{\theta})$, its likelihood is defined as
$$\begin{align}
\mathcal{L}:\Theta&\to \mathbb{R}^{+} \\
\theta&\mapsto c(\mathbf{x})f(\mathbf{x};\boldsymbol{\theta})
\end{align}$$
where $\Theta$ is the space of all possible parameters and $c(\mathbf{x})$ is some constant for the given $\mathbf{x}$. This function allows for comparison between the credibility of different sets of parameters. Higher likelihood means higher credibility. Notably, the ratio of two likelihoods, $\mathcal{L}(\boldsymbol{\theta}_{1})/\mathcal{L}(\boldsymbol{\theta}_{2})$, provides a relative comparison in which the constant $c(\mathbf{x})$ drops out. A formal justification of this credibility interpretation is given by the [[Wald inequality]].

Since $\mathcal{L}$ and $\log \mathcal{L}$ share maxima, it is common to maximize $\log \mathcal{L}$ instead since it makes the expression easier to solve and constrains numerical range, which makes numerical precision better in computer evaluations.
### Log-likelihood
It is common to instead use the **log-likelihood**, which is simply the logarithm of the likelihood: $\ell(\boldsymbol{\theta};\mathbf{x})\equiv \log \mathcal{L}(\boldsymbol{\theta};\mathbf{x})$. The base of the logarithm is usually 10. This form greatly reduces the range of numbers that are observed in practice, which helps with numerical stability. Analytically, it also turns many products into sums.

The [[gradient]] of the log-likelihood is sometimes called the **score function** $U(\boldsymbol{\theta})\equiv(\partial_{\theta_{1}}\log \mathcal{L},\ldots,\partial_{\theta_{M}}\log \mathcal{L})$. The negative [[Hessian]] is called the **observed information matrix** $J_{ij}(\boldsymbol{\theta})\equiv- \frac{ \partial ^{2}\log \mathcal{L} }{ \partial \theta_{i}\partial \theta_{j} }$. These function possess some interesting properties, provided they are sufficiently regular:
1. The expected score is zero: $\text{E}[U(\boldsymbol{\theta})]=0$.
2. The **second Bartlett identity** holds: $\text{cov}_{\boldsymbol{\theta}}(U(\boldsymbol{\theta}))=\text{E}_{\boldsymbol{\theta}}[J(\boldsymbol{\theta})]=\mathcal{I}(\boldsymbol{\theta})$. The function $\mathcal{I}(\boldsymbol{\theta})$ (the [[covariance]] of the score) is called the **Fisher information matrix** (or **expected information matrix**). This notation is shorthand for each combination of $\theta_{i},\theta_{j}$ in the covariance.
3. The **[[Cramer-Rao-Frechet inequality]]** holds. In one dimension, $\mathcal{I}(\theta)=\text{E}[J(\theta)]$ and so $\text{var}_{\theta}(\tilde{\theta})\geq 1/\mathcal{I}(\theta)$. In multiple dimension, this generalizes by adding the condition that $\text{cov}(\tilde{\boldsymbol{\theta}})=\mathcal{I}^{-1}(\boldsymbol{\theta})$ is [[Matrix sign definitions|positive semidefinite]].
### Applications
The likelihood function is generally used in [[maximum likelihood estimation]], which attempts to find the global maximum of $\mathcal{L}$ in order to find the most realistic parameters $\boldsymbol{\theta}$ for a model. It is also a key component of [[Bayes' theorem]], where it is multiplied by the [[prior]] to obtain the [[posterior]].