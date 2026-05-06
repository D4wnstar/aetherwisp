---
hl-publish: true
aliases:
  - distribution
---
A **probability distribution** is a function that gives the [[Probability]] that a [[Random variable]] will take on a specific value or set of values on measurement. If a probability distribution accurately describes the statistical behavior of a random variable, it is said that the variable *follows* that distribution.

The term "probability distribution" is sometimes used to refer to the [[image]] of the distribution function. For example, say that a loaded coin has a 40% chance to land as heads and 60% as tails, then "probability distribution" can refer to:
- The function $p:\{ \text{Heads},\text{Tails} \}\to[0,1]$ that maps $p(\text{Heads})=0.4$ and $p(\text{Tails})=0.6$. This is the formally correct definition.
- The image of $p$, $\{ 0.4, 0.6 \}$, which contains the two probabilities, leaving the mapping implied. This isn't correct, but it is sometimes used.

Probability distributions may be discrete or continuous.
- Discrete probability distributions are known as [[probability mass function|probability mass functions]]. 
- Continuous probability distributions are known as [[Probability density function|probability density functions]]. However, due to complexities arising from the infinite outcomes over a continuous [[sample space]], the distribution is only fully defined when the [[cumulative distribution function]] is also given.

Regardless of the type, most distribution functions have parameters. These are numerical values that modify the shape and behavior of the distribution and are chosen separately from the usual arguments. For example, the [[Gaussian distribution]] takes one real number $x$ as a regular argument and has two parameters: the [[mean]] $\mu$ and the [[variance]] $\sigma ^{2}$. To distinguish the two, it is typical to separate regular arguments from parameters with a semicolon. The Gaussian probability density function is commonly denoted $f(x;\mu,\sigma ^{2})$.