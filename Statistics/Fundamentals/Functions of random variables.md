---
wiki-publish: true
---
A **function of one or more random variables** is any function that depends on a set of [[random variable|random variables]]. Call $y$ a function dependent on variables $X_{1},\ldots,X_{N}$, it is denoted $y=y(x_{1},\ldots,x_{n})$.
### Expectation and variance
It is generally useful to know the [[Expected value]] and [[Variance]] of such a function. Assume the expectation and variance of the $i$-th variable are $E[X_{i}]=\mu_{i}$ and $\sigma_{i}^{2}$, and the [[Covariance]] of the $ij$ pair is $\text{cov}(x_{i},x_{j})=\rho_{y}\sigma_{i}\sigma_{j}$.

Let's initially consider just the univariate case $y=y(x)$ and let's call $E[y]=\mu$ the expected value and $\sigma^{2}$ the variance of $y$. We can do a [[Taylor series|Taylor expansion]] of $y$ centered in $\mu$ as
$$y(x)\simeq y(\mu)+ \underbrace{ \left. \frac{dy}{dx}\right|_{x=\mu}(x-\mu) }_{ 0 }+ \frac{1}{2}\left. \frac{d^{2}y}{dx^{2}}\right|_{x=\mu}(x-\mu)^{2}+\ldots$$
We have
$$\mu_{y}=E[y]=y(\mu)+ \frac{1}{2}\left. \frac{d^{2}y}{dx^{2}}\right|_{x=\mu}\sigma ^{2}+\ldots$$
The variance is $\text{var}(y)=E[y^{2}]-E[y]^{2}$, so we need $y^{2}$, which is, through another series expansion in $\mu$:
$$y^{2}\simeq y^{2}(\mu)+2y(\mu) \left. \frac{dy}{dx}\right|_{x=\mu}(x-\mu)+ y(\mu) \frac{1}{2} \left. \frac{d^{2}y}{dx^{2}}\right|_{x=\mu}(x-\mu)^{2}+\left[ \left. \frac{dy}{dx}\right|_{x=\mu}(x-\mu) \right]^{2}+$$
$$+y(\mu) \frac{1}{2} \left.\frac{d^{2}y}{dx^{2}}\right|_{x=\mu}(x-\mu)^{2}+\ldots$$
So $E[y^{2}]$ is
$$E[y^{2}]=y^{2}(\mu)+y(\mu) \left. \frac{d^{2}y}{dx^{2}}\right|_{x=\mu}\sigma ^{2}+ \left( \left. \frac{dy}{dx}\right|_{x=\mu} \right)^{2}+\ldots$$

Meanwhile, $E[y]^{2}$ is idk teach deleted blackboard, same for $\sigma^{2}$, but it's just the propagation of variances

The multivariate case $y=y(x_{1},\ldots,x_{n})$ instead requires us to do a multivariate series expansion in $(\mu_{1},\ldots,\mu_{n})$:
$$y(x_{1},\ldots,x_{n})=y(\mu_{1},\ldots,\mu_{n})+\sum_{i=1}^{n} \left.\frac{ \partial y }{ \partial x_{i} }\right|_{\mathbf{x}=\boldsymbol{\mu}} (x_{i}-\mu_{i})+ \frac{1}{2}\sum_{i=1}^{n} \sum_{j=1}^{n} \left. \frac{ \partial ^{2}y }{ \partial x_{i}x_{j} }  \right|_{\mathbf{x}=\boldsymbol{\mu}}(x_{i}-\mu_{i})(x_{j}-\mu_{j})+\ldots$$
The expectation is
$$\boxed{E[y]=y(\mu_{1},\ldots,\mu_{n})+ \frac{1}{2}\sum_{i=1}^{n} \sum_{j=1}^{n} \left. \frac{ \partial ^{2}y }{ \partial x_{i}x_{j} }  \right|_{\mathbf{x}=\boldsymbol{\mu}}\text{cov}(x_{i},x_{j})}$$
idk what $y^{2}$, $E[y^{2}]$ or $E[y]^{2}$ are but if you find them you get
$$\boxed{\text{var}(y)=\sum_{i=1}^{n} \left( \left.\frac{ \partial y }{ \partial x_{i} } \right|_{\mathbf{x}=\boldsymbol{\mu}} \right)^{2}\sigma ^{2}_{i}+\sum_{i\neq j}^{n} \left.\frac{ \partial y }{ \partial x_{i} } \right|_{\mathbf{x}=\boldsymbol{\mu}}\left.\frac{ \partial y }{ \partial x_{j} } \right|_{\mathbf{x}=\boldsymbol{\mu}}\text{cov}(x_{i},x_{j})}$$

Say instead we have two functions $y_{1}$ and $y_{2}$ of the same variables $(x_{1},\ldots,x_{n})$. It is also possible to find their covariance in the same way, using series expansions. It is
$$\boxed{\text{cov}(y_{1},y_{2})=E[y_{1}y_{2}]-E[y_{1}]E[y_{2}]=\sum_{i=1}^{n} \left.\frac{ \partial y_{1} }{ \partial x_{i} }\right|_{\mathbf{x}=\boldsymbol{\mu}} \left.\frac{ \partial y_{2} }{ \partial x_{i} }\right|_{\mathbf{x}=\boldsymbol{\mu}}\sigma ^{2}_{i}}$$
#### Sum of two variables
Let's consider two random variables $X_{1}$ and $X_{2}$ of [[mean|means]] $\mu_{1}$ and $\mu_{2}$ and variances $\sigma_{1}$ and $\sigma_{2}$. Let's also consider a function $y$ that is just their sum $y=x_{1}+x_{2}$. The mean and variance of $y$ are simply
$$\mu_{y}=\mu_{1}+\mu_{2},\qquad \sigma_{y}^{2}=\sigma_{1}^{2}+\sigma_{2}^{2}+2\rho \sigma_{1}\sigma_{2}$$
#### Linear regression
Consider the linear relationship $X=mZ+q$ and a set of $n$ empirical measurements $(z_{i},x_{i})$. $X$ is a univariate function of $Z$, so we can use the theory above for estimates. Let's call $\hat{m}$ and $\hat{q}$ estimates of $m$ and $q$ and $\sigma_{\hat{m}}^{2}$ and $\sigma ^{2}_{\hat{q}}$ their variances. $\text{cov}(\hat{m},\hat{q})=\rho \sigma_{\hat{m}}\sigma_{\hat{q}}$ is their covariance. The expected value and variance of $X$ are
$$x^{*}=\hat{m}z^{*}+\hat{q},\qquad\sigma ^{2}_{x^{*}}=(z^{*})^{2}\sigma ^{2}_{\hat{m}}+\sigma ^{2}_{\hat{q}}+2z^{*}\rho \sigma_{\hat{m}}\sigma_{\hat{z}}$$
Using the [[minimum squares method]] and introducing the sum
$$S_{jk}=\sum_{i=1}^{n} \frac{z_{i}^{j}x_{i}^{k}}{\sigma_{i}^{2}}$$
the best estimates of $m$ and $q$ are
$$\hat{m}=\frac{1}{D}(S_{00}S_{11}-S_{10}S_{01}),\qquad\hat{q}=\frac{1}{D}(S_{01}S_{20}-S_{11}S_{10})$$
where $D=S_{00}S_{20}-S_{10}^{2}$. The partial derivatives are
$$\frac{ \partial \hat{m} }{ \partial x_{i} } =\frac{1}{D}\left( S_{00} \frac{z_{i}}{\sigma_{i}^{2}}- S_{10} \frac{1}{\sigma_{i}^{2}} \right),\qquad \frac{ \partial \hat{q} }{ \partial x_{i} }=\frac{1}{D}\left( S_{20} \frac{1}{\sigma_{i}^{2}}- S_{10} \frac{z_{i}}{\sigma_{i}^{2}} \right) $$
Their covariance is
$$\begin{align}
\text{cov}(\hat{m},\hat{q})&=\sum_{i=1}^{n} \frac{1}{D^{2}}\left( S_{00} \frac{z_{i}}{\sigma_{i}^{2}}- S_{10} \frac{1}{\sigma_{i}^{2}} \right)\left( S_{20} \frac{1}{\sigma_{i}^{2}}- S_{10} \frac{z_{i}}{\sigma_{i}^{2}} \right)\sigma_{i}^{2} \\
&=\frac{1}{D^{2}}\left( \cancel{ S_{00}S_{20}\underbrace{ \sum_{i=1}^{n} \frac{z_{i}}{\sigma_{i}^{2}} }_{ S_{10} } }-S_{10}S_{20}\underbrace{ \sum_{i=1}^{n} \frac{1}{\sigma_{i}^{2}} }_{ S_{00} }- \cancel{ S_{00}S_{10}\underbrace{ \sum_{i=1}^{n} \frac{z_{i}^{2}}{\sigma_{i}^{2}} }_{S_{20}} } + S_{10}^{2}\underbrace{ \sum_{i=1}^{n} \frac{z_{i}}{\sigma_{i}^{2}} }_{ S_{10} } \right) \\
&= \frac{1}{D^{2}}S_{10}(\underbrace{ -S_{20}S_{00}+S_{10}^{2} }_{ -D }) \\
&=- \frac{S_{10}}{D}
\end{align}$$
#### Sampled square
Consider two [[independent variables|independent]] random variables $X_{1}$ and $X_{2}$ and a function
$$f(x_{i})=\begin{cases}
1 & 0\leq x_{i}\leq 1 \\
0 & \text{altrimenti}
\end{cases}$$
These variables occupy a $1\times 1$ square between 0 and 1. Let's define the variables
$$y_{1}=x_{1}+x_{2},\qquad y_{2}=x_{1}-x_{2}$$
We want to find what space these two occupy. The maximum and minimum of $y_{1}$ are 0 and 2, whereas for $y_{2}$ they are -1 and 1. Therefore, they at most occupy a diamond shape like the following

![[Graph Regions of random variables|80%|center]]

We can express $x_{1}$ and $x_{2}$ as functions of $y_{1}$ and $y_{2}$ as
$$x_{1}=\frac{1}{2}(y_{1}+y_{2}),\qquad x_{2}=\frac{1}{2}(y_{1}-y_{2})$$
The derivatives are
$$\frac{ \partial x_{1} }{ \partial y_{1} } =\frac{1}{2},\qquad \frac{ \partial x_{1} }{ \partial y_{2} } =\frac{1}{2},\qquad \frac{ \partial x_{2} }{ \partial y_{1} } =\frac{1}{2},\qquad \frac{ \partial x_{2} }{ \partial y_{2} } =- \frac{1}{2}$$
so the [[determinante|determinant]] of the [[Jacobian]] is $\det J=- \frac{1}{2}$. We have idk (TODO: Finish this, lesson 04/11/2024, near the end)
$$g(y_{1})=\int _{-y_{1}}^{+y_{1}} \frac{1}{2}\ldots$$
#### Something-something formula
Same premise as above for $X_{1}$ and $X_{2}$, but the functions instead are
$$y_{1}=\sqrt{ -2\ln x_{1} }\cos(2\pi x_{2}),\qquad y_{2}=\sqrt{ -2\ln x_{1} }\sin(2\pi x_{2})$$
Summing the squares of the two we get $y_{1}^{2}+y_{2}^{2}=-2\ln x_{1}$, so $\ln x_{1}=- \frac{1}{2}(y_{1}^{2}+y_{2}^{2})$. Dividing the two we get something with a tangent idk
$$x_{1}=e^{- (1/2)(y_{1}^{2}+y_{2}^{2})},\qquad x_{2}=\frac{1}{2\pi}\arctan\left( \frac{y_{2}}{y_{1}} \right)$$
The partial derivatives are
$$\frac{ \partial x_{1} }{ \partial y_{1} } =-y_{1}e^{-(1/2)(y_{1}^{2}+y_{2}^{2})},\qquad \frac{ \partial x_{1} }{ \partial y_{2} } =-y_{2}e^{-(1/2)(y_{1}^{2}+y_{2}^{2})}$$
$$\frac{ \partial x_{2} }{ \partial y_{1} } =\frac{1}{2\pi} \frac{1}{1+ \frac{y_{2}^{2}}{y_{1}^{2}}}\left( - \frac{y_{2}}{y_{1}^{2}} \right)=- \frac{1}{2\pi} \frac{y_{2}}{y_{1}^{2}+y_{2}^{2}},\qquad \frac{ \partial x_{2} }{ \partial y_{2} } =\frac{1}{2\pi} \frac{1}{1+ \frac{y_{2}^{2}}{y_{1}^{2}}} \frac{1}{y_{1}}=\frac{1}{2\pi} \frac{y_{1}}{y_{1}^{2}+y_{2}^{2}}$$
The determinant of the Jacobian is
$$\det J=\lvert J \rvert =\left\lvert  \frac{1}{2\pi} \frac{y_{1}^{2}}{y_{1}^{2}+y_{2}^{2}} e^{-(1/2)(y_{1}^{2}+y_{2}^{2})}+ \frac{1}{2\pi} \frac{y_{2}^{2}}{y_{1}^{2}+y_{2}^{2}} e^{-(1/2)(y_{1}^{2}+y_{2}^{2})}\right\rvert =\frac{1}{2\pi}e^{-(1/2)(y_{1}^{2}+y_{2}^{2})}$$

Then $h(y_{1},y_{2})$ is
$$h(y_{1},y_{2})=\frac{1}{2\pi}e^{-(1/2)(y_{1}^{2}+y_{2}^{2})}=\frac{1}{\sqrt{ 2\pi }}e^{-y_{1}^{2}/2}\ \frac{1}{\sqrt{ 2\pi }}e^{-y_{2}^{2}/2}$$
