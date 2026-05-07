---
hl-publish: true
---
Despite being [[random]], a [[random variable]] is still a variable and as such can be used as the argument of a function. **Functions of random variables** thus play a significant role in statistics and knowing their properties sets the foundation for a significant chunk of the field. Importantly, they themselves are random variables and as such share all the statistical machinery that comes attached with them.
### Distribution, expectation, variance
Call $Y$ a univariate function dependent on an RV $X$. We denote it $Y\equiv Y(X)$. Since $Y$ is itself an RV, it follows some [[probability distribution]]. If $f_{X}(x)$ is the [[probability density function]] of $X$, then the PDF of $Y$ is given by
$$\boxed{f_{Y}(y)=f_{X}(X(y))\left\lvert  \frac{dX(y)}{dY}  \right\rvert }$$
This is true under the assumption that the function $Y(X)$ is monotonic and invertible to $Y^{-1}(Y)=X(Y)$. If that is not true and $Y(X)$ is not monotonic, such that there are $m$ RVs $X_{i}$ for which $Y=Y(X_{i})$, then the above formula generalizes to
$$\boxed{f_{Y}(y)=\sum_{i=1}^{N} f_{X}(X_{i}(y))\left\lvert   \frac{dX_{i}(y)}{dY}  \right\rvert }$$
In essence, this formula is the same as before, except you break the function down into $m$ monotonic pieces, recycle the previous formula to find their individual contribution and then sum them up.

A couple of examples that can be derived from these are:
- If $X\sim \mathcal{N}(\mu,\sigma^{2})$ then $Y(X)=(X-\mu)/\sigma$ is $Y\sim \mathcal{N}(0,1)$.
- If $X\sim \mathcal{N}(0,1)$, then $Y(X)=X^{2}$ is $Y\sim \chi_{1}^{2}$.

> [!quote]- Proof: Square of a standard normal is chi-square
> Let $X\sim \mathcal{N}(0,1)$. We want to prove that $Y=X^{2}\sim \chi ^{2}_{1}$. Inverting $Y=X^{2}$ gives $X=\pm \sqrt{ Y }$. The square is evidently not monotonic, as each there are two possible values of $x$ for each $y$. Thus, we use the non-monotonic form with $m=2$. The PDF of $X$ is the usual standard normal, so
> $$f_{X}(X(y))=\frac{1}{\sqrt{ 2\pi }}e^{ -y/2 }$$
> for both $\pm \sqrt{ y }$, as it is an even function. We then differentiate
> $$\left\lvert  \frac{dX_{+}(y)}{dY}  \right\rvert =\left\lvert  \frac{d\sqrt{ Y }}{dY}  \right\rvert = \frac{1}{2\sqrt{ Y }},\qquad\left\lvert  \frac{dX_{-}(y)}{dY}  \right\rvert =\left\lvert  \frac{d(-\sqrt{ Y })}{dY}  \right\rvert = \frac{1}{2\sqrt{ Y }}$$
> which are also both equal. Then, applying the formula
> $$f_{Y}(y)=\frac{1}{\sqrt{ 2\pi }}e^{-y/2} \left( \frac{1}{2\sqrt{ y }}+ \frac{1}{2\sqrt{ y }} \right)=\frac{1}{\sqrt{ \pi }} \frac{1}{\sqrt{ 2 }} \frac{1}{\sqrt{ y }}e^{-y/2}=\frac{1}{\Gamma\left( \frac{1}{2} \right)} \frac{1}{2^{1/2}}y^{1/2-1}e^{-y/2}$$
> which is exactly the PDF of a $\chi_{1}^{2}$.

Calculating the entire distribution of $Y$ is rather overkill in many cases. Most of the time, the [[function moments]] of $Y$ are more useful. Out of them, it is generally useful to know the [[expected value]] and [[variance]]. Finding exact formulas for these is tricky however; instead, it is best to use approximations. For the [[mean]], given $\mu_{X}=\mathrm{E}[X]$, we can do a [[Taylor series|Taylor expansion]] of $Y$ centered in $\mu$ to get
$$Y(X)\simeq Y(\mu_{X})+ \underbrace{ \left. \frac{dY}{dX}\right|_{x=\mu_{X}}(X-\mu_{X}) }_{ 0 }+ \frac{1}{2}\left. \frac{d^{2}Y}{dX^{2}}\right|_{x=\mu_{X}}(X-\mu_{X})^{2}+\ldots$$
If we wrap this in an expectation operator we get
$$\mathrm{E}[Y(X)]=\mu_{Y}\simeq Y(\mu_{X})+ \frac{1}{2} \left.{\frac{d^{2}Y}{dX^{2}}}\right|_{x=\mu_{X}}\sigma_{X}^{2}$$
If $\sigma ^{2}_{X}$ is small, then we can approximate even more to simply state
$$\mu_{Y}\simeq Y(\mu_{X})$$
Similarly, the variance becomes
$$\text{var}(Y(X))=\sigma ^{2}_{Y}\simeq\left( \left.{\frac{dY}{dX}}\right|_{x=\mu_{X}} \right)^{2}\sigma_{X}^{2}$$
These results can be extended to the multivariate case. Given a multivariate $Y\equiv Y(X_{1},\ldots,X_{N})$, the approximate mean and variance can be found using the same Taylor expansion above, just in $N$ dimensions:
$$\boxed{\begin{align}
\mu_{Y}&\simeq Y(\mu_{X_{1}},\ldots,\mu_{X_{N}})+ \frac{1}{2}\sum_{i=1}^{N} \sum_{j=1}^{N} \left. \frac{ \partial ^{2}Y }{ \partial x_{i}x_{j} }  \right|_{\mathbf{x}=\boldsymbol{\mu}_{X}}\text{cov}(X_{i},X_{j}) \\ \\
\sigma ^{2}_{Y}&\simeq \sum_{i=1}^{N} \left( \left.{\frac{dY}{dX_{i}}}\right|_{\mathbf{x}=\boldsymbol{\mu}_{X}} \right)^{2}\sigma ^{2}_{X_{i}}+\sum_{j=1}^{N} \sum_{\substack{k=1 \\ k\neq j}}^{N} \left.{\frac{ \partial Y }{ \partial x_{j} } }\right|_{\mathbf{x}=\mu_{X}}\left.{\frac{ \partial Y }{ \partial x_{k} }}\right|_{\mathbf{x}=\boldsymbol{\mu}_{X}}\text{cov}(X_{j},X_{k})
\end{align}}$$
The variance formula is known as the **[[law of propagation of variance]]** and finds considerable use in experimental science to propagate measurement errors. For [[independent variables]], the [[covariance]] terms vanish, leaving a much simpler sum of squares.

If we instead have two functions $Y_{1}$ and $Y_{2}$ of the same variables $(X_{1},\ldots,X_{N})$, their covariance can be through the same series expansions method. It is
$$\boxed{\text{cov}(Y_{1},Y_{2})=E[Y_{1}Y_{2}]-E[Y_{1}]E[Y_{2}]=\sum_{i=1}^{N} \left.\frac{ \partial Y_{1} }{ \partial x_{i} }\right|_{\mathbf{x}=\boldsymbol{\mu}_{X}} \left.\frac{ \partial Y_{2} }{ \partial x_{i} }\right|_{\mathbf{x}=\boldsymbol{\mu}_{X}}\sigma ^{2}_{X_{i}}}$$

---

#### Linear regression
Consider the linear relationship $X=mZ+q$ and a set of $n$ empirical measurements $(z_{i},x_{i})$. $X$ is a univariate function of $Z$, so we can use the theory above for estimates. Let's call $\hat{m}$ and $\hat{q}$ estimates of $m$ and $q$ and $\sigma_{\hat{m}}^{2}$ and $\sigma ^{2}_{\hat{q}}$ their variances. $\text{cov}(\hat{m},\hat{q})=\rho \sigma_{\hat{m}}\sigma_{\hat{q}}$ is their covariance. The expected value and variance of $X$ are
$$x^{*}=\hat{m}z^{*}+\hat{q},\qquad\sigma ^{2}_{x^{*}}=(z^{*})^{2}\sigma ^{2}_{\hat{m}}+\sigma ^{2}_{\hat{q}}+2z^{*}\rho \sigma_{\hat{m}}\sigma_{\hat{z}}$$
Using the [[Minimum squares method]] and introducing the sum
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

![[Graph Regions of random variables.svg|80%|center]]

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
