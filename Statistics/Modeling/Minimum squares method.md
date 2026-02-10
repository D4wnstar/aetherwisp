---
wiki-publish: true
aliases:
  - least squares method
  - MSM
  - LSM
  - linear minimum squares
---
The **minimum squares method** (**MSM**) or **least squares method** (**LSM**) is a [[Parameter estimation]] method. It assumes that the outputs $y$ are related to the inputs $x$ according to a [[Statistics/Modeling/Model|model]] function $y=f(x;\boldsymbol{\theta})$ for some set parameters $\boldsymbol{\theta}$. The method provides a set of [[estimator|estimators]] of $\boldsymbol{\theta}$.

The general method goes as follows. Given a [[sample]] of $N$ data pairs $(x_{1},y_{1}),\ldots,(x_{N},y_{N})$ drawn from [[Independent variables|independent]] [[Random variable|random variables]] $X_{1},\ldots,X_{N}$ and $Y_{1},\ldots,Y_{N}$ that we assume to be related by a known function $Y_{i}=f(X_{i};\boldsymbol{\theta})$ of parameters $\boldsymbol{\theta}$, we define the quantity
$$Z ^{2}=\sum_{i=1}^{N} w_{i}(y_{i}-\mu_{i})^{2}$$
where $\mu_{i}=f(x_{i};\boldsymbol{\theta})$ are the expected values according to our desired relation and $w_{i}$ are weights that are related to the uncertainty on $y_{i}$. In essence, it's a weighted sum of squares. The MSM states the best estimates of the parameters are those for which this quantity is minimized, hence the name of the method:
$$\frac{ \partial (Z ^{2}) }{ \partial \theta_{i} } =0,\quad \frac{ \partial ^{2} (Z^{2}) }{ \partial \theta_{i}^{2} } >0\quad\ \forall\ i\in[1,N]$$
To properly quantify the MSM, you need two things (besides the data): an expected relation $f$ and a set of weights $w$. The function is completely dependent on the problem you're trying solve, but the set of weights has a somewhat general answer: $w_{i}=1/\sigma_{Y_{i}}^{2}$, where $\sigma ^{2}_{Y_{i}}$ are the [[Variance|variances]] of the distributions of $Y_{1},\ldots,Y_{N}$. If these are not known, other weights might be used, or they can be estimated.

The benefits of MSM are several. For one, the estimators are well-behaved and carry good properties. Indeed, MSM estimators achieve the [[Cramer-Rao inequality|Cramer-Rao lower bound]] and are unbiased even with small sample sizes. Furthermore, it's a very simple method, both in terms of interpretation and of analytical form. It's just minimizing a sum of squares, weighed by the uncertainty. More uncertain measurements will weigh less, whereas more confident ones weigh more, so that it converges to the highest confidence estimate that minimizes the distance between the model and the data. The simplicity makes estimators often solvable analytically, although numerical optimization is certainly an option.
### Dependent measurements
If the random variables for the samples are not independent (say, because one measurement affects the next), the MSM can still apply, but it requires knowing the [[Covariance|covariance matrix]] $\Sigma$ of the $Y_{1},\ldots,Y_{N}$. If known then the squares to minimize are
$$Z^{2}=(\mathbf{y}-\boldsymbol{\mu})^{T}\Sigma^{-1}(\mathbf{y}-\boldsymbol{\mu})$$
### Uncertain measurements
The MSM works as long as the uncertainty on the $X$ measurements is negligible compared to the one on the $Y$ measurements. Formally, this means that the uncertainty on $\mu_{i}$ due to the uncertainty of $x_{i}$ is small compared to the uncertainty on $y_{i}$. If this is not true, then there's two scenarios:
- If the uncertainty on $y_{i}$ is small compared to the one on $x_{i}$, then you can just invert the relation and predict $x$ from $y$. The methods works the same both ways.
- If both uncertainties are large, it is possible to use $\sigma ^{2}_{Y_{i}}+\sigma ^{2}_{\mu _{i}}$ in the weights instead of just $\sigma ^{2}_{Y_{i}}$, where $\sigma ^{2}_{\mu_{i}}$ is the variance of $\mu_{i}$ as calculated from $\sigma ^{2}_{X_{i}}$. However, the $\sigma ^{2}_{\mu_{i}}$ depend on the choice of parameters $\boldsymbol{\theta}$, which is what the method is supposed to give you *after* you know them. In this case, it's impossible to get quality estimates from the MSM in a single run and the process must be iterated: calculate $\sigma ^{2}_{\mu_{i}}$ using an arbitrary (but sensible) set of parameters, then run MSM to get some estimates, recalculate $\sigma ^{2}_{\mu_{i}}$ with those estimates; rinse and repeat until you are satisfied with the estimates.
### Gaussian measurements
The MSM makes no assumption about what distribution $Y_{1},\ldots,Y_{N}$ follow. It's a universal method, in this sense. However, if the $Y_{1},\ldots,Y_{N}$ happen to follow [[Gaussian distribution|Gaussian distributions]], then the quadratic form $Z^{2}$ often follows a [[chi-square distribution]] (since $\chi ^{2}$ appears from the sum of squares of iid Gaussians). How many degrees of freedom it has is a bit complicated. If $Z^{2}$ is calculated using the true parameters, then it has $N$ degrees of freedom. This is because for true parameters, $f(x_{i};\boldsymbol{\theta})=\mu_{i}$ is the true mean, so $(y_{i}-\mu_{i})/\sigma_{i}$ is precisely a standard normal, and the sum of $N$ squared standard normals is $\chi ^{2}_{N}$. However, if you're using the MSM, it's probably because you don't know the true parameters. In this case, it depends on the shape of $f(x;\boldsymbol{\theta})$. If it's linear, it's still $\chi ^{2}$  but with $N-k$, where $k$ is the number of parameters to estimate ($k=\dim\boldsymbol{\theta}$). Each estimate removes one degree of freedom. If $f(x;\boldsymbol{\theta})$ is nonlinear, then it's actually not $\chi ^{2}$ at all. If $N$ is large enough, then it can loosely be approximated as such even for nonlinear forms, but formally it isn't and it requires special attention.

The MSM estimators for Gaussian $Y_{1},\ldots,Y_{N}$ are identical to the [[Maximum likelihood estimation|maximum likelihood ones]].
### Linear minimum squares
A particularly interesting case is the one where the relation $f$ is a linear model. This is known as the **linear minimum squares method** (**LMSM**) and its most general case is a linear model with $k$ parameters:
$$\mu_{i}=f(x_{i};\boldsymbol{\theta})=\sum_{j=1}^{k} a_{ij}(x_{i})\theta_{j}$$
or in [[matrix]] notation: $\boldsymbol{\mu}=\mathrm{A}\boldsymbol{\theta}$. The matrix $\mathrm{A}$ is known as the **[[design matrix]]** (of dimensions $N\times k$) and is a concept of linear models even outside of statistics. The $a_{ij}$ elements represents the value of the functions (called **basis functions**, usually denoted $\phi_{1},\ldots,\phi_{k}$) for each term, evaluated in $x_{i}$. In a simple line $f=mx+q$, the basis functions are  $\phi_{1}(x)=x$ and $\phi_{2}(x)=1$. The general form is $f=m\phi_{1}(x)+q\phi_{2}(x)$. Then, $a_{ij}=\phi_{j}(x_{i})$.

The LMSM has even nicer properties than the general MSM: on top of being unbiased and minimum-variance, the estimators are also asymptotically Gaussian.
#### On a line
The simplest case of LMSM is on a line $f(x;\boldsymbol{\theta})=mx+q$. The parameters to estimate are $m$ and $q$. Then, $Z ^{2}$ reads
$$Z ^{2}=\sum_{i=1}^{N} \frac{(y_{i}-mx_{i}-q)^{2}}{\sigma ^{2}_{i}} $$
We need to minimize two derivatives:
$$\begin{align}
\frac{ \partial Z ^{2} }{ \partial m } =0\quad&\Rightarrow \quad \sum_{i=1}^{N} \frac{ \partial  }{ \partial m } (y_{i}-mx_{i}-q)^{2}=0 \\
\frac{ \partial Z ^{2} }{ \partial q } =0\quad&\Rightarrow \quad \sum_{i=1}^{N} \frac{ \partial  }{ \partial q } (y_{i}-mx_{i}-q)^{2}=0
\end{align}$$
This system can be solved to find
$$\boxed{\hat{m}=\frac{S_{0}S_{xy}-S_{x}S_{y}}{D},\qquad \hat{q}=\frac{S_{x^{2}}S_{y}-S_{x}S_{xy}}{D}}$$
where
$$S_{0}=\sum_{i=1}^{N} \frac{1}{\sigma ^{2}_{i}},\quad S_{x}=\sum_{i=1}^{N} \frac{x_{i}}{\sigma ^{2}_{i}},\quad S_{y}=\sum_{i=1}^{N} \frac{y_{i}}{\sigma ^{2}_{i}}\quad S_{xy}=\sum_{i=1}^{N} \frac{x_{i}y_{i}}{\sigma ^{2}_{i}},\quad S_{x^{2}}=\sum_{i=1}^{N} \frac{x_{i}^{2}}{\sigma ^{2}_{i}}$$
and $D=S_{0}S_{x^{2}}-S_{x}^{2}$. These equations can be further handled using [[Variance#Propagation of variance]] to find
$$\boxed{\sigma_{\hat{m}}^{2}=\frac{S_{0}}{D},\qquad \sigma ^{2}_{\hat{q}}=\frac{S_{x^{2}}}{D},\qquad\text{cov}(\hat{m},\hat{q})=- \frac{S_{x}}{D}}$$
#### In general
The general is still solvable analytically. Start from $\boldsymbol{\mu}=\mathrm{A}\boldsymbol{\theta}$. The squares to minimize are given by the general MSM for dependent variables
$$Z^{2}=(\mathbf{y}-\mathrm{A}\boldsymbol{\theta})\Sigma^{-1}(\mathbf{y}-\mathrm{A}\boldsymbol{\theta})$$
Taking the derivatives in the components of $\boldsymbol{\theta}$, it's possible to prove that
$$\boldsymbol{\theta}=B\mathbf{y}\quad\text{where}\quad B\equiv(\mathrm{A}^{T}\Sigma^{-1}\mathrm{A})^{-1}\mathrm{A}^{T}\Sigma\equiv \Sigma_{\hat{\boldsymbol{\theta}}}\mathrm{A}^{T}\Sigma$$
As long as calculating [[Invertible matrix|inverse matrices]] is viable, then $B$ can be found numerically.[^1]
### Nonlinear minimum squares
In case of a nonlinear $f(x;\boldsymbol{\theta})$, using minimum squares is more involved. The easiest way is to linearize the equation.

Take for example the freefall equation
$$s=\frac{1}{2}gt^{2}$$
where $g$ is [[gravitational acceleration]] and $t$ is time. Of course, this is a quadratic relation in time, so $s=f(t;g)$ won't be linear. Let's do some algebra to make it linear. Invert to get $t$:
$$t=\sqrt{ \frac{2s}{g} }$$
This is of course also not linear, since the square root of $\sqrt{ s }$ isn't linear. However, we don't *have* to use $s$ as our input. We can just $\sqrt{ s }$ directly! In this case we could write
$$\underbrace{ t }_{ y }=\underbrace{ \sqrt{ \frac{2}{g} } }_{ m }\underbrace{ \sqrt{ s } }_{ x }+\underbrace{ t_{0} }_{ q }$$
and we get a linear relation again, which can be solved using the method above. ($t_{0}$ was added manually since it's possible there might be some bias in our measurements. Ideally we get $t_{0}=0$ and it disappears.) Just be careful of taking the square roots of your values of $s$ before using them in this model, since you need $\sqrt{ s }$. Once we're done with the estimation, we get $g$ out of $m$ with
$$m=\sqrt{ \frac{2}{g} }\quad\Rightarrow \quad g=\frac{2}{m^{2}}$$
The variance of $m$ is known from the linear minimum squares. The variance of $g$ is hence given by the propagation of variance
$$\sigma_{g}^{2}=\left( \frac{ \partial g }{ \partial m }  \right)^{2}\sigma_{m}^{2}$$

[^1]: However, since $\Sigma$ is $N\times N$ and $\mathrm{A}$ is $N\times k$, for large sample sizes it might be prohibitively time-consuming even on a computer.
