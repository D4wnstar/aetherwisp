---
wiki-publish: true
aliases:
  - MDF
---
The **marginal distribution function** (**MDF**) of a set of $N$ [[random variable|random variables]] is the function that gives the [[probability]] of a specific outcome for one of the variables, regardless of what the other variables do. For instance, if the variables are four dice being rolled together, the marginal distribution function answers the question "what's the probability that the first die will roll a 3? I don't care what the other three dice do."

Formally, given a [[joint distribution function]] $f(x_{1},\ldots,x_{N})$, the marginal distribution function is
$$f_{M}(x_{1})=\int_{\Omega_{2}}\ldots \int_{\Omega_{N}}f(x_{1},\ldots,x_{N})\ dx_{2}\ldots dx_{N} $$
where the $\Omega$ are the [[sample space|sample spaces]] of the random variables. In other words, you are integrating over the sample spaces of all variables except the one that matters to you. This "gets rid" of all other variables by considering all the possible cases they can take and leaves you with just the one you are interested in.
### Properties
- It is [[Normalization|normalized]]: $\int_{\Omega}f_{M}(x)=1$.

If the variable is [[Independent variables|independent]] of all others, its MDF matches its [[probability density function]]. In fact, for independent variables the joint distribution function is
$$f(x_{1},\ldots,x_{N})=f_{1}(x_{1})\ldots f_{N}(x_{N})$$
so the integral becomes
$$f_{M}(x_{1})=f_{1}(x_{1})\int_{\Omega_{2}}f_{2}(x_{2})\ dx_{2}\ldots \int_{\Omega_{N}}f_{N}(x_{N})\ dx_{N}$$
but by definition, the integral of a PDF over its entire sample space is 1 (probability is [[Normalization|normalized]]), so all the PDFs integrate to 1 and we're left with
$$f_{M}(x_{1})=f_{1}(x_{1})$$
The MDF differs from the natural PDF of the random variable only if it's [[Covariance|correlated]] to other variables.