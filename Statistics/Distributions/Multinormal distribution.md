The **multinormal distribution** is a real, multivariate [[probability distribution]] that [[Gaussian distribution]] to multiple dimensions. For $n$ [[independent variable|independent]], normally-distributed [[Random variable|random variables]] $X_{1},\ldots,X_{n}$, it is simply the [[joint distribution function]] of $n$ Gaussians:
$$f(x_{1},\ldots,x_{n})=f_{1}(x_{1})\ldots f_{n}(x_{n})=\frac{1}{(2\pi)^{n/2}\sigma_{1}\ldots\sigma_{n}}e^{-\sum_{i=1}^{n} (x_{i}-\mu_{i})^{2}/2\sigma_{i}^{2}}$$
where $\mu_{i}$ and $\sigma_{i}^{2}$ are the [[mean]] and [[variance]] of the $i$-th variable. In terms of the [[Covariance|covariance matrix]], it can be written in a more general form that also works for dependent variables:
$$f(x_{1},\ldots,x_{n})=\frac{1}{(2\pi)^{n/2}\sqrt{ \det V }}e^{-(\mathbf{x}-\mathbf{\mu})^{T}V^{-1}(\mathbf{x}-\mathbf{\mu})/2}$$
### Independent variables
Since the variables are independent, the covariance matrix is diagonal:
$$V=\begin{pmatrix}
\sigma_{1}^{2} & 0 & \ldots & \ldots &  0 \\
0 & \sigma_{2}^{2} & 0 & \ldots & 0 \\
\vdots & \vdots & \vdots & \vdots & \vdots \\
0 & \ldots & \ldots & \ldots & \sigma_{n}^{2}
\end{pmatrix}$$
and its inverse
$$V^{-1}=\begin{pmatrix}
\frac{1}{\sigma_{1}^{2}} & 0 & \ldots & \ldots &  0 \\
0 & \frac{1}{\sigma_{2}^{2}} & 0 & \ldots & 0 \\
\vdots & \vdots & \vdots & \vdots & \vdots \\
0 & \ldots & \ldots & \ldots & \frac{1}{\sigma_{n}^{2}}
\end{pmatrix}$$

Constant values of the exponent trace circular lines of equal probability:
$$\begin{align}
Q^{2}&=(\mathbf{x}-\mathbf{\mu})^{T}V^{-1}(\mathbf{x}-\mathbf{\mu})=\text{const} \\
\text{(for two variables)}&=\frac{(x_{1}-\mu_{1})^{2}}{\sigma_{1} ^{2}}+ \frac{(x_{2}-\mu_{2})^{2}}{\sigma_{2}^{2}}=1
\end{align}$$
The area inside of a region enclosed by one of this lines is used to measure [[probability]] in the same way an integral over the one-dimensional [[Probability density function|PDF]] can. For instance, the probability of a value being sampled inside of a circle of $1\sigma$ centered in $(\mu_{1},\mu_{2})$ is
$$P(Q^{2}\leq 1)=P(\chi_{2}^{2}\leq 1)=\int_{0}^{1} \frac{1}{2}e^{-z/2}\ dz=-e^{-z/2}|_{0}^{1}=1- \frac{1}{\sqrt{ e }}=0.39$$
where $\chi_{2}^{2}$ is the [[chi-square distribution]] with 2 degrees of freedom. In fact, $Q^{2}$ can be shown to follow a $\chi ^{2}$ distribution with degrees of freedom equal to the number of variables in the system (here two). For $4\sigma$ we get
$$P(Q^{2}\leq 4)=P(\chi_{2}^{2}\leq 4)=\int_{0}^{4} \frac{1}{2}e^{-z/2}\ dz=0.89$$
### Dependent variables
If the variables are not independent, it gets a lot more verbose. Let's consider two variables only. In this case, the covariance matrix is
$$V=\begin{pmatrix}
\sigma_{1}^{2} & \rho \sigma_{1}\sigma_{2} \\
\rho \sigma_{1}\sigma_{2} & \sigma_{2}^{2}
\end{pmatrix}\qquad \det V=\sigma_{1}^{2}\sigma_{2}^{2}(1-\rho ^{2})\qquad V^{-1}=\frac{1}{\det V}\begin{pmatrix}
\sigma_{2}^{2} & -\rho \sigma_{1}\sigma_{2} \\
-\rho \sigma_{1}\sigma_{2} & \sigma_{1}^{2}
\end{pmatrix}$$
We get
$$V^{-1}(\mathbf{x}-\mathbf{\mu})=\frac{1}{\det V}\begin{pmatrix}
(x_{1}-\mu_{1})\sigma_{2}^{2} -\rho \sigma_{1}\sigma_{2}(\sigma_{2}-\mu_{2}) \\
\rho \sigma_{1}\sigma_{2}(x_{1}-\mu_{1}) +\sigma_{1}^{2}(x_{2}-\mu_{2})
\end{pmatrix}$$
and so
$$\begin{align}
Q^{2}&=(\mathbf{x}-\mathbf{\mu})^{T}V^{-1}(\mathbf{x}-\mathbf{\mu}) \\
&=\frac{1}{\det V}[(x_{1}-\mu_{1})^{2}\sigma_{2}^{2}-2\rho \sigma_{1}\sigma_{2}(x_{1}-\mu_{1})(x_{2}-\mu_{2})+\sigma_{1}^{2}(x_{2}-\mu_{2})^{2}] \\
&=\frac{1}{1-\rho ^{2}}\left[ \frac{(x_{1}-\mu_{1})^{2}}{\sigma_{1}^{2}}-2\rho \frac{x_{1}-\mu_{1}}{\sigma_{1}}\frac{x_{2}-\mu_{2}}{\sigma_{2}}+ \frac{(x_{2}-\mu_{2})^{2}}{\sigma_{2}^{2}} \right] \\
\end{align}$$
If we find the lines traced by constant values of this function, we find that instead of being circles like they were in the independent case, they are now ellipses, squished either on the bottom-left top-right diagonal or the top-left bottom-right diagonal.

![[Graph Multinormal equiprobability|80%|center]]

In fact, the [[eccentricity]] of the ellipsis is a visual cue that shows how correlated two variables are. High correlation means high eccentricity, whereas no correlation means no eccentricity, hence why the independent variable case is just a circle. We can get a lot of useful information with some geometry.
$$A=\frac{1}{1-\rho ^{2}} \frac{(x_{1}-\mu_{1})^{2}}{\sigma_{1} ^{2}}=1,\qquad B=\frac{1}{1-\rho ^{2}} \frac{(x_{2}-\mu_{2})^{2}}{\sigma_{2} ^{2}}=1$$
$$\overline{AA'}=2\sigma_{1}\sqrt{ 1-\rho ^{2} },\qquad \overline{BB'}=2\sigma_{2}\sqrt{ 1-\rho ^{2} }$$

The red diagonals ($\overline{C C'}$ and $\overline{DD'}$) are known as the **regression lines**.
### idk lol
Let's consider the variable $\mathbf{y}$ defined as
$$\mathbf{y}=\mathrm{A}\mathbf{x},\qquad \mathbf{\mu}_{y}=\mathrm{A}\boldsymbol{\mu}$$
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