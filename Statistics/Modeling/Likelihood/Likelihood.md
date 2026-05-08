---
hl-publish: true
---
The **likelihood function** or simply **likelihood** provides a measure of how well a set of [[Sample|population parameters]] applied to a statistical [[model]] describes a [[sample]]. Mathematically, it is a specific interpretation of the [[joint distribution function]] that the sample's [[Random variable|random variables]] follow, but instead of setting parameters and changing samples, one sets the sample and changes the parameters.

If we consider an [[iid]] random sample $\mathbf{X}=(X_{1},\ldots,X_{N})$ of size $N$ and a model with $M$ parameters $\boldsymbol{\theta}=(\theta_{1},\ldots,\theta_{M})$, the [[probability]] $P$ of observing a realization $\mathbf{x}=(x_{1},\ldots,x_{N})$ of $\mathbf{X}$ given a specific set of parameters $\boldsymbol{\theta}^{*}$ is given by the joint distribution function, which maps[^1]
$$\mathbf{x} \mapsto P(\mathbf{x}|\boldsymbol{\theta}^{*})$$
We can logically invert the relationship to find the probability (*likelihood*) $\mathcal{L}$ of observing parameters $\boldsymbol{\theta}$ given a specific observation $\mathbf{x}^{*}$:
$$\boldsymbol{\theta} \mapsto P(\boldsymbol{\theta}|\mathbf{x}^{*})\equiv \mathcal{L}(\boldsymbol{\theta}|\mathbf{x}^{*})$$
Strictly speaking, these two functions are identical. What changes is which arguments we set and which we allow to vary, which changes the information that the function gives. The likelihood, in essence, asks the question: "Given our specific observation $\mathbf{x}^{*}$, how confident are we that the process that generated it has parameters $\boldsymbol{\theta}$ under our model?"

For an iid sample, we can call the [[probability density function]] of the common distribution $f_{X}(x;\boldsymbol{\theta})$. Then, since the likelihood is the joint density function, which itself is just the product of PDFs in an iid set, we can state
$$\mathcal{L}(\boldsymbol{\theta};\mathbf{x})=\prod_{i=1}^{N} f_{X}(x_{i};\boldsymbol{\theta})$$
Thus evaluating the likelihood amounts to evaluating a product of probability density functions.

More generally, given some statistical model $f(\mathbf{x};\boldsymbol{\theta})$, its likelihood is formally defined as
$$\begin{align}
\mathcal{L}:\Theta&\to \mathbb{R}^{+} \\
\boldsymbol{\theta}&\mapsto c_{\mathbf{x}}f(\mathbf{x};\boldsymbol{\theta})
\end{align}$$
where $\Theta$ is the space of all possible parameters and $c_{\mathbf{x}}$ is some constant for the given $\mathbf{x}$. This function allows for comparison between the credibility of different sets of parameters. Higher likelihood means higher credibility. Notably, the ratio of two likelihoods, $\mathcal{L}(\boldsymbol{\theta}_{1})/\mathcal{L}(\boldsymbol{\theta}_{2})$, provides a relative comparison in which the constant $c(\mathbf{x})$ drops out. A formal justification of this credibility interpretation is given by the [[Wald inequality]].
### Log-likelihood
It is common to instead use the **log-likelihood**, which is simply the logarithm of the likelihood: $\ell(\boldsymbol{\theta};\mathbf{x})\equiv \log \mathcal{L}(\boldsymbol{\theta};\mathbf{x})$. The base of the logarithm is usually $e$ or 10. This form greatly reduces the range of numbers that are observed in practice, which helps with numerical stability. Analytically, it also turns many products into sums.

The [[Gradient]] of the log-likelihood is sometimes called the **score function** $U(\boldsymbol{\theta})\equiv(\partial_{\theta_{1}}\log \mathcal{L},\ldots,\partial_{\theta_{M}}\log \mathcal{L})$. The negative [[Hessian]] is called the **observed information matrix** $J_{ij}(\boldsymbol{\theta})\equiv- \frac{ \partial ^{2}\log \mathcal{L} }{ \partial \theta_{i}\partial \theta_{j} }$.

These functions possess some interesting properties, provided they are sufficiently regular:
1. The expected score is zero: $\text{E}[U(\boldsymbol{\theta})]=0$.
2. The **second Bartlett identity** holds: $\text{cov}_{\boldsymbol{\theta}}(U(\boldsymbol{\theta}))=\text{E}_{\boldsymbol{\theta}}[J(\boldsymbol{\theta})]=\mathcal{I}(\boldsymbol{\theta})$. The function $\mathcal{I}(\boldsymbol{\theta})$ (the [[Covariance]] of the score) is called the **Fisher information matrix** (or **expected information matrix**). This notation is shorthand for each combination of $\theta_{i},\theta_{j}$ in the covariance.
3. The **[[Cramer-Rao inequality]]** holds. In one dimension, $\mathcal{I}(\theta)=\text{E}[J(\theta)]$ and so $\text{var}_{\theta}(\hat{\theta})\geq 1/\mathcal{I}(\theta)$. In multiple dimension, this generalizes by adding the condition that $\text{cov}(\hat{\boldsymbol{\theta}})=\mathcal{I}^{-1}(\boldsymbol{\theta})$ is [[Matrix sign definitions|positive semidefinite]].
### Applications
The likelihood function is generally used in [[maximum likelihood estimation]], which attempts to find the global maximum of $\mathcal{L}$ in order to find the most realistic parameters $\boldsymbol{\theta}$ for a model. It is also a key component of [[Bayes' theorem]], where it is multiplied by the [[prior]] to obtain the [[posterior]].

[^1]: Actually, this is a bit tricky with continuous variables. For discrete variable, the JDF gives probability. For continuous ones, it's the integral of the JDF that gives the probability, as the JDF gives probability *density*. Either way, the likelihood interpretation is the same.
