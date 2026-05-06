---
hl-publish: true
aliases:
  - jointly-distributed
  - joint distribution
  - JDF
---
The **joint distribution function** (**JDF**) of a set of $N$ [[Random variable|random variables]] defined in the same [[sample space]] is the function that describes the [[Probability]] of every possible combination of outcomes. The [[Probability distribution]] of all the variables together is called the **joint distribution**. For instance, if the variables are four dice being rolled together, the joint distribution function answers the question "what's the probability I'll roll 3, 4, 1 and 5?"

Formally, it is the function $f(x_{1},\ldots,x_{N})$ that, when integrated over all desired intervals $I_{1}\in \Omega_{1},\ldots,I_{N}\in \Omega_{N}$, returns the probability of all variables being observed in their respective interval:
$$P(X_{1}=x_{1},\ldots,X_{N}=x_{N})=\int_{I_{N}}\ldots \int_{I_{1}}f(x_{1},\ldots,x_{N})\ dx_{1}\ldots dx_{N}$$

For [[independent variables]], the joint distribution function is just the product of each individual [[Probability density function]] or [[Probability mass function]]:
$$f(x_{1},,\ldots,x_{N})=f_{1}(x_{1})\ldots f_{N}(x_{N})$$
For [[iid]] variables, it's simply the product of the shared distribution $g(x)$
$$f(x_{1},\ldots,x_{N})=\prod_{i=1}^{N} g(x_{i})$$
### Properties
- It is [[Normalization|normalized]]: $\int_{\Omega_{N}}\ldots \int_{\Omega_{1}}f(x_{1},\ldots,x_{N})\ dx_{1}\ldots dx_{N}=1$ where the $\Omega$ are the sample spaces of the variables.