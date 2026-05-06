---
hl-publish: true
---
The **multivariate normal distribution** is a real, multivariate [[probability distribution]] that is a generalization of the [[Gaussian distribution|normal distribution]] to multiple dimensions. For $N$ Gaussian [[Independent variables|independent]] [[Random variable|random variables]] $X_{1},\ldots,X_{N}$, the [[joint distribution function]] is:
$$f(x_{1},\ldots,x_{N})=f_{1}(x_{1})\ldots f_{N}(x_{N})=\frac{1}{(2\pi)^{N/2}\sigma_{1}\ldots\sigma_{N}}e^{-\sum_{i=1}^{N} (x_{i}-\mu_{i})^{2}/2\sigma_{i}^{2}}$$
$\mu_{i}$ and $\sigma_{i}^{2}$ are the [[mean]] and [[variance]] of the $i$-th distribution.

If the variables are not independent, it can be written in terms of the [[Covariance|covariance matrix]] $\Sigma$:
$$f(\mathbf{x})=\frac{1}{(2\pi)^{N/2}\sqrt{ \det \Sigma }}e^{-(\mathbf{x}-\boldsymbol{\mu})^{T}\Sigma^{-1}(\mathbf{x}-\boldsymbol{\mu})/2}$$
where $\boldsymbol{\mu}=(\mu_{1},\ldots,\mu_{N})$. Most of the exponent is often put in its own variable:
$$Q^{2}=(\mathbf{x}-\boldsymbol{\mu})^{T}\Sigma^{-1}(\mathbf{x}-\boldsymbol{\mu})$$
This quantity has interesting properties that can be used to analyze the dispersion of the distribution.

As a shorthand, a [[Random variable|random vector]] $\mathbf{X}$ can be said to follow a multivariate normal of mean vector $\boldsymbol{\mu}$ and covariance matrix $\Sigma$ with the notation
$$\mathbf{X}\sim \mathcal{N}(\boldsymbol{\mu},\Sigma)$$
### Moments
The [[moment-generating function]] of the multivariate normal is known in closed form for the independent variable case and is a direct extension of the univariate normal:
$$M_{\mathbf{X}}(\mathbf{t})=\exp\left( \sum_{i=1}^{N} \frac{\sigma_{i}^{2}t_{i}^{2}}{2} \right),\qquad M_{\mathbf{X}}^{*}(\mathbf{t})=\exp\left( \sum_{i=1}^{N} \frac{\sigma_{i}^{2}t_{i}^{2}}{2}+\mu_{i}t_{i} \right)$$
## Dispersion and $Q^{2}$ ellipses
The multivariate normal distribution is, like its univariate sibling, possibly the most important multivariate distribution, owing to the commonness of Gaussian random variables. Both the cases with independent and dependent random variables come up in practice, and it's therefore useful to discuss both.
### Independent variables
Since the variables are independent, the covariance matrix is [[Diagonalization|diagonal]]:
$$\Sigma=\begin{pmatrix}
\sigma_{1}^{2} & 0 & \ldots & \ldots &  0 \\
0 & \sigma_{2}^{2} & 0 & \ldots & 0 \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
0 & \ldots & \ldots & \ldots & \sigma_{N}^{2}
\end{pmatrix}$$
and its [[Invertible matrix|inverse]] is
$$\Sigma^{-1}=\begin{pmatrix}
\frac{1}{\sigma_{1}^{2}} & 0 & \ldots & \ldots &  0 \\
0 & \frac{1}{\sigma_{2}^{2}} & 0 & \ldots & 0 \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
0 & \ldots & \ldots & \ldots & \frac{1}{\sigma_{N}^{2}}
\end{pmatrix}$$
This effectively reduces the covariance matrix down to a variance vector.

The exponent $Q^{2}$ mentioned above is useful because its values trace [[hypersurface|hypersurfaces]] of equal [[probability]]. If you set a value of $Q^{2}$ and find the locus of $(x_{1},\ldots,x_{N})$ points that realize that value, you get a closed and quite well-behaved hypersurface that represents all points with equal probability. If this sounds confusing, just know that in the simplest case of $N=2$, they're just regular [[ellipse|ellipses]]. To see it, just write down the equation for $Q^{2}$:
$$Q^{2}=\frac{(x_{1}-\mu_{1})^{2}}{\sigma_{1} ^{2}}+ \frac{(x_{2}-\mu_{2})^{2}}{\sigma_{2}^{2}}$$
This is the equation of an ellipse with semiaxes $\sigma_{1}$ and $\sigma_{2}$, centered in $(\mu_{1},\mu_{2})$, scaled by a factor $Q$.[^1] For higher $N$, they are [[hyperellipsoid|hyperellipsoids]]. When they can be represented visually (mostly just $N=2$, possibly $N=3$), they serve as a useful way to visualize the dispersion of the multivariate normal. In fact, exactly because the [[standard deviation|standard deviations]] are the semiaxes, $Q^{2}$ is essentially the $N$-dimensional analog of the variance and $Q$ that of the standard deviation. Of course, the *real* variances are still $\sigma_{1}^{2},\ldots,\sigma_{N}^{2}$, but $Q^{2}$ is an efficient way to package all that information in a single variable. In the $N=2$ case, since the semiaxes are scaled by $Q$, setting $Q$ lets us draw the ellipse corresponding to whatever multiple of $\sigma$ we want. For $Q^{2}=1$, we get the ellipse with $(\sigma_{1},\sigma_{2})$, for $Q^{2}=4$, we get the ellipse with $(2\sigma_{1},2\sigma_{2})$, and so on.

:::image
![[multivariate_normal_independent.png]]
1000 random samples from an $N=2$ multivariate normal (so-called *bivariate*). The means are both zero so that the distribution is centered in the origin. The standard deviations are $\sigma_{1}=2$ and $\sigma_{2}=1$. The colored ellipses show $Q^{2}=1$ and $Q^{2}=4$.
:::

The area inside the hyperellipsoid is used to measure probability in the same way a [[cumulative distribution function]] does. The probability of a value being inside of a $Q^{2}=1$ hyperellipsoid is $P(Q^{2}\leq1)$. To properly evaluate this, we need the CDF of $Q^{2}$. As it happens, $Q^{2}$ is actually [[Chi-square distribution|chi-square distributed]], specifically with $N$ degrees of freedom. This is because $Q^{2}$ is the sum of squares of $x_{1},\ldots,x_{N}$, and the sum of squares of Gaussians follows a $\chi ^{2}_{N}$ distribution. Thus, we can find the probability just fine, even analytically. For an $N=2$ ellipse, the $\chi^{2}_{2}$ is just
$$f_{X}(x;2)=\frac{1}{2}e^{-x/2}$$
and so the integral is
$$P(Q^{2}\leq 1)=P(\chi ^{2}_{2}\leq 1)=\int_{0}^{1} \frac{1}{2}e^{-x/2}\ dx=-e^{-x/2}|_{0}^{1}=1- \frac{1}{\sqrt{ e }}\simeq0.39$$
For $Q^{2}=4$ we instead get
$$P(Q^{2}\leq 4)=P(\chi_{2}^{2}\leq 4)=\int_{0}^{4} \frac{1}{2}e^{-x/2}\ dx\simeq0.86$$
These numbers are the multivariate analog of the classic 1-2-3$\sigma$ rule of the Gaussian. Where $1\sigma\Rightarrow68\%$ and $2\sigma\Rightarrow95\%$ in a univariate Gaussian, $Q^{2}=1\Rightarrow39\%$ and $Q^{2}=4\Rightarrow 86\%$ in a multivariate Gaussian.
### Dependent variables
If the variables are not independent, things gets a lot more verbose as covariance can no longer be ignored. Let's consider $N=2$ variables only. We can no longer use the easy formula for $Q^{2}$ and need the full one:
$$Q^{2}=(\mathbf{x}-\boldsymbol{\mu})^{T}\Sigma^{-1}(\mathbf{x}-\boldsymbol{\mu})$$
In other words, we need the covariance matrix and its inverse:
$$\Sigma=\begin{pmatrix}
\sigma_{1}^{2} & \rho \sigma_{1}\sigma_{2} \\
\rho \sigma_{1}\sigma_{2} & \sigma_{2}^{2}
\end{pmatrix},\quad \det \Sigma=\sigma_{1}^{2}\sigma_{2}^{2}(1-\rho ^{2}),\quad \Sigma^{-1}=\frac{1}{\det \Sigma}\begin{pmatrix}
\sigma_{2}^{2} & -\rho \sigma_{1}\sigma_{2} \\
-\rho \sigma_{1}\sigma_{2} & \sigma_{1}^{2}
\end{pmatrix}$$
The second half of the formula is
$$\Sigma^{-1}(\mathbf{x}-\boldsymbol{\mu})=\frac{1}{\det \Sigma}\begin{pmatrix}
(x_{1}-\mu_{1})\sigma_{2}^{2} -\rho \sigma_{1}\sigma_{2}(\sigma_{2}-\mu_{2}) \\
\rho \sigma_{1}\sigma_{2}(x_{1}-\mu_{1}) +\sigma_{1}^{2}(x_{2}-\mu_{2})
\end{pmatrix}$$
and so putting it all together and doing the matrix multiplications:
$$\begin{align}
Q^{2}&=(\mathbf{x}-\boldsymbol{\mu})^{T}\Sigma^{-1}(\mathbf{x}-\boldsymbol{\mu}) \\
&=\frac{1}{\det \Sigma}[(x_{1}-\mu_{1})^{2}\sigma_{2}^{2}-2\rho \sigma_{1}\sigma_{2}(x_{1}-\mu_{1})(x_{2}-\mu_{2})+\sigma_{1}^{2}(x_{2}-\mu_{2})^{2}] \\
&=\frac{1}{1-\rho ^{2}}\left[ \frac{(x_{1}-\mu_{1})^{2}}{\sigma_{1}^{2}}-2\rho \frac{x_{1}-\mu_{1}}{\sigma_{1}}\frac{x_{2}-\mu_{2}}{\sigma_{2}}+ \frac{(x_{2}-\mu_{2})^{2}}{\sigma_{2}^{2}} \right]
\end{align}$$
If we find the draw the ellipses traced by this $Q^{2}$, we find that they are now angled. This angle is quite important, as it visually represents correlation between $x_{1}$ and $x_{2}$. Indeed, this angle is proportional to the correlation coefficient $\rho$ and is the major difference from the independent case above (where the ellipse was *axis-aligned*). When $\rho=0$, you get an axis-aligned ellipse.

:::image
![[Graph Multinormal equiprobability|80%|center]]
A general bivariate ellipse showing important points and lines. The red diagonals (passing through segments $\overline{C C'}$ and $\overline{DD'}$) are known as the **regression lines** of the distribution.
:::

We can get extract a lot of useful information with some geometry. The $x_{1}=\mu_{1}$ and $x_{2}=\mu_{2}$ lines intersect with the ellipse at points
$$A=(\mu_{2}-\sqrt{ 1-\rho ^{2} }\sigma_{2}, \mu_{2}),\quad A'=(\mu_{2}+\sqrt{ 1-\rho ^{2} }\sigma_{2}, \mu_{2})$$
$$B=(\mu_{1},\mu_{1}-\sqrt{ 1-\rho ^{2} }\sigma_{1}),\quad B'=(\mu_{1},\mu_{1}+\sqrt{ 1-\rho ^{2} }\sigma_{1})$$
and the segments inside the ellipse are
$$\overline{AA'}=2\sigma_{2}\sqrt{ 1-\rho ^{2} },\qquad \overline{BB'}=2\sigma_{1}\sqrt{ 1-\rho ^{2} }$$
### idk lol
Let's consider the variable $\mathbf{y}$ defined as
$$\mathbf{y}=\mathrm{A}\mathbf{x},\qquad \boldsymbol{\mu}_{y}=\mathrm{A}\boldsymbol{\mu}$$
where $\mathrm{A}$ is a matrix. The covariance matrix is
$$\mathrm{V}_{y}=\mathrm{A}\mathrm{V}\mathrm{A}^{T}$$
Let's also consider a vector $\mathbf{z}$ such that its components are standard-normal distributed:
$$z_{i}\sim N(0,1)\quad\Rightarrow \quad\sum_{i=1}^{n} z_{i}^{2}\sim \chi_{n}^{2}$$
$\mathbf{z}$ can be written as
$$\mathbf{z}=\mathrm{V}^{-1/2}(\mathbf{x}-\boldsymbol{\mu})$$
$\mathbf{z}$ follows a multinormal distribution with covariance matrix $\mathrm{V}_{z}$, so $N(0,\mathrm{V}_{z})$, where $\mathrm{V}_{z}$ is
$$\mathrm{V}_{z}=\mathrm{V}^{-1/2}\mathrm{V}\mathrm{V}^{-1/2}=\mathrm{I}$$
since the $z_{i}$ are independent of each other, $\text{cov}(z_{i},z_{j})=0$ for $i\neq j$. Thus, $Q^{2}$ in terms of $\mathbf{z}$ is
$$Q^{2}=\underbrace{ (\mathbf{x}-\boldsymbol{\mu})^{T}\mathrm{V}^{-1/2} }_{ \mathbf{z}^{T} }\underbrace{ \mathrm{V}^{-1/2}(\mathbf{x}-\boldsymbol{\mu}) }_{ \mathbf{z} }=\mathbf{z}^{T}\mathbf{z}=\sum_{i=1}^{n} z_{i}^{2}$$
which is indeed chi-square-distributed.

[^1]: Alternatively, an unscaled ellipse with semiaxes $Q\sigma_{1}$ and $Q\sigma_{2}$.
