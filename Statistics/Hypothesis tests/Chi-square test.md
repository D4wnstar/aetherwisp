---
wiki-publish: true
---
A **chi-square test** or **$\chi ^{2}$-test** is a type of [[hypothesis test]] where the test statistic is a [[chi-square distribution]] and the data is [[Gaussian distribution|Gaussian-distributed]]. For a data [[sample]] $(x_{1},\ldots,x_{n})$, the value of the test statistic is
$$t=\sum_{i=1}^{N} \frac{(x_{i}-\mu_{i})^{2}}{\sigma_{i}^{2}}=(\mathbf{x}-\boldsymbol{\mu})^{T}\mathrm{V}^{-1}(\mathbf{x}-\boldsymbol{\mu})$$
where $\mu_{i}$ is the $i$-th [[mean]] of the distribution and $\mathrm{V}$ is the [[Covariance|covariance matrix]]. For this test to work, $\mu_{i}\geq 5$ must hold. The [[Expected value|expectation]] is $E[T]=n-1$.