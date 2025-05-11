---
wiki-publish: true
---
The **chi-square distribution** or **$\chi ^{2}$ distribution** is a real, continuous [[probability distribution]]. For a [[random variable]] $X$, the [[probability density function]] is
$$f_{X}(x;k)=\frac{1}{2^{k/2}\Gamma\left( \frac{k}{2} \right)}x^{k/2 -1}e^{-x/2}$$
where $k$ is a positive parameter called the *degrees of freedom* of the distribution and $\Gamma$ is the [[Gamma function]]. Though not strictly necessary by definition, $k$ is usually taken to be integer, as $\Gamma$ has closed form solutions for integer $k$.

![[Chi-square_pdf.svg]]

It is mostly used for [[hypothesis test|hypothesis testing]].
### Moments
The algebraic [[moment-generating function]] is
$$\begin{align}
M_{X}^{*}(t)=E[e^{tX}]&=\frac{1}{2^{k/2}\Gamma\left( \frac{k}{2} \right)}\int_{0}^{\infty}e^{tx}x^{k/2-1}e^{-x/2}\ dx \\
&=\frac{1}{2^{k/2}\Gamma\left( \frac{k}{2} \right)}\Gamma\left( \frac{k}{2} \right) \frac{1}{2^{-k/2}}(1-2t)^{-k/2} \\
&=(1-2t)^{-k/2}
\end{align}$$
which is a very similar MGF to the [[exponential distribution]] one. We can make the substitution $Y=\frac{X-k}{\sqrt{ 2k }}$. With this, the MGF becomes
$$M_{Y}^{*}(t)=e^{t^{2}/2}$$
which is the [[Gaussian distribution|standard normal distribution]]'s central MGF.

The [[expected value]] is
$$E[X]=k$$
and the [[variance]] is
$$\text{var}(X)=2k$$

The [[Function moments|moments]] are
0. $\mu_{0}^{*}=1$
1. $\mu_{1}^{*}=k$ ([[mean]])

0. $\mu_{0}=1$
1. $\mu_{1}=0$
2. $\mu_{2}=2k$ ([[variance]])
3. $\mu_{3}=8k$
4. $\mu_{4}=12k^{2}+48k$

and the coefficients are
1. $\gamma_{1}=2 \sqrt{ \frac{2}{k} }$ ([[skewness]], it has a peak at low values and tapers off to the right, goes to zero for $k\to \infty$)
2. $\gamma_{2}=\frac{12}{k}$ ([[kurtosis]], goes to zero for $k\to \infty$)
### As sum of normal variables
Given a set of normally-distributed variables $\{ X_{i} \}_{i}$, the sum of their squares $Y=\sum_{i=1}^{N}X_{i}^{2}$ is chi-square-distributed with a number of degrees of freedom equal to the number of normal variables being summed, $k=N$. This is the primary reason why this distribution is so common and often given as its definition.
### Relation to other distributions
It is a specific case of the [[Gamma distribution]] with $\alpha=k/2$ and $\beta=2$. If $k\gg 1$, the distribution approximately becomes a [[Gaussian distribution]] $N(k,2k)$.
### In molecular velocity analysis
The chi-square distribution can be used to derive a statistical description of the motion of molecules in a gas. Consider a gas of identical molecules each with velocity $\mathbf{v}=(v_{1},v_{2},v_{3})\in \mathbb{R}^{3}$. Each component of each $\mathbf{v}$ is considered a normally-distributed random variable with parameters $N(0,\sigma ^{2})$. We can define the scale-independent variable $\mathbf{q}$ as $\mathbf{q}=\mathbf{v}/\sigma=(q_{1},q_{2},q_{3})$, the components of which are also normally distributed but following the standard normal $N(0,1)$ instead. The square [[Norma|norm]] of $\mathbf{q}$, $\lvert \mathbf{q} \rvert^{2}\equiv q^{2}=q_{1}^{2}+q_{2}^{2}+q_{3}^{2}$ is therefore chi-squared-distributed with 3 degrees of freedom: $\chi ^{2}_{3}$. The probability density function for $q^{2}$ thus is
$$f(q^{2})=\frac{1}{\sqrt{ 2\pi }}(q^{2})^{1/2}e^{-q^{2}/2}$$
and therefore the one for $v^{2}$ is, by substitution,
$$g(v^{2})=\frac{1}{\sqrt{ 2\pi }}\left( \frac{v^{2}}{\sigma ^{2}} \right)^{1/2}e^{-v^{2}/2\sigma ^{2}} \frac{1}{\sigma ^{2}}=\frac{1}{\sqrt{ 2\pi }} \frac{v}{\sigma ^{3}}e^{-v^{2}/2\sigma ^{2}}$$
and for $v$ we get
$$h(v)=g(v^{2})2v=\frac{2}{\sqrt{ 2\pi }}\frac{v^{2}}{\sigma ^{3}}e^{-v^{2}/2\sigma ^{2}}$$
This is called the [[Maxwell-Boltzmann distribution]] and is used for modeling stochastic motion at molecular or atomic scale. It can be found that $\sigma=k_{B}T/m$ where $k_{B}$ is the [[Boltzmann constant|Boltzmann constant]], $T$ is the gas temperature and $m$ is the mass of the molecules.