---
wiki-publish: true
aliases:
  - conditional independence
  - conditionally independent
---
Two variables are **independent** if changing one has no effect on the other. Formally, their [[Joint distribution function]] is the product of individual [[Probability density function|probability density functions]]:
$$\text{independent if }f(x,y)=f(x)f(y)$$
Two variables may be **conditionally independent** if they are independent only when given a third one:
$$\text{conditionally independent if }f(x,y|z)=f(x|z)f(y|z)$$
where we're using [[Conditional distribution function|conditional distribution functions]]. An example of conditional independence are the steps of a [[Markov chain]].
### Properties
- The [[covariance]] is zero: $\text{cov}(X,Y)=0$. By extension, the correlation is also zero: $\rho=0$. Note that the converse does not hold. Covariance being zero is a necessary but not sufficient condition for independence.
