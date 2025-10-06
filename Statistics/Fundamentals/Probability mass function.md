---
wiki-publish: true
---
A **probability mass function** (**PMF**) is a function associated with a discrete [[random variable]] that gives the [[probability]] that the variable, when measured, is exactly equal to some value. The PMF describes the [[probability distribution]] that a discrete variable follows.

Given a discrete random variable $X$, its probability mass function $p_{X}$ is defined as $p_{X}:\Omega_{X}\mapsto[0,1]$, where $\Omega_{X}$ is $X$'s [[sample space]]. It is equal to
$$p_{X}(x)=P(X=x)$$
where $P$ is a [[measure]] of probability. By definition of probability, the total probability must be 1:
$$\sum_{x \in \Omega}p_{X}(x)=1 $$
### Transformations
Given a discrete random variable $X$ of [[probability mass function]] $f_{X}$ and an invertible [[transformation]] $g(x)$, we can define the transformed random variable as $Y=g(X)$. The PMF of $Y$ is
$$f_{Y}(y)=f_{X}(g^{-1}(y)) $$
The same definition applies to a discrete [[Random variable|random vector]] $\mathbf{X}$ that is invertibly transformed into another random vector $\mathbf{Y}=g(\mathbf{X})$:
$$f_{\mathbf{Y}}(\mathbf{y})=f_{\mathbf{X}}(g^{-1}(\mathbf{y}))$$
