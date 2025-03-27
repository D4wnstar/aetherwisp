A multivariate function $f(x_{1},\ldots,x_{n})$ is said to be **homogeneous** of degree $\alpha$ if for all $\lambda>0$ and all points $(x_{1},\ldots,x_{n})$ the following equality holds:
$$f(\lambda x_{1},\ldots,\lambda x_{n})=\lambda^{\alpha}f(x_{1},\ldots,x_{n})$$
### Properties
For a homogeneous function of degree $\alpha$, the following is true:
$$\sum_{i=1}^{N} x_{i}\frac{ \partial f }{ \partial x_{i} } =\alpha f$$
In fact:
$$\begin{align}
0&=\left.{\frac{d}{d\lambda}(f(\lambda x_{1},\ldots,\lambda x_{n})-\lambda^{\alpha}f(x_{1},\ldots,x_{n}))}\right|_{\lambda=1} \\
&=\left.{\left( \sum_{i=1}^{N}x_{i}\frac{ \partial f }{ \partial x_{i} } (\lambda x)-\alpha \lambda^{\alpha-1}f(x) \right)}\right|_{\lambda=1} \\
&=\sum_{i=1}^{N} x_{i}\frac{ \partial f }{ \partial x_{i} } (x)-\alpha f(x)
\end{align}$$
### Examples
An example of a degree $2$ homogeneous function is
$$f(x_{1},x_{2},x_{3})=x_{1}x_{2}+x_{2}^{2}+x_{3}x_{1}$$
