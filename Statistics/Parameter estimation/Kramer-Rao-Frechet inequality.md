---
wiki-publish: true
---
The **Kramer-Rao-Frechet inequality** gives a lower bound to the [[Variance]] of an [[estimator]]. Given an estimator $\hat{\theta}$ for a parameter $\theta$ and a [[sample]] set of [[independent variables]] $\{ x_{1},\ldots,x_{n} \}$, each with their own [[probability distribution]] $f_{i}(x_{i};\theta)$, we have
$$\hat{\sigma}^{2}_{\hat{\theta}}\geq\frac{1}{E\left[ - \frac{d^{2}\ln \mathcal{L}}{d\theta ^{2}} \right]}$$
where $E[\cdot]$ is the [[Expected value]] and $\mathcal{L}$ is the [[Likelihood]] function
$$\mathcal{L}(x_{1},\ldots,x_{n};\theta)=f(x_{1},\ldots,x_{n};\theta)=\prod_{i=1}^{n} f_{i}(x_{i};\theta)$$
