---
aliases:
  - invariant under the transformation
---
A function $f(x_{1},\ldots,x_{n})$ is said to be **invariant under the transformation** $(x_{1}\to \varphi_{x_{1}}(x_{1},\ldots,x_{n}),\ldots,x_{n}\to\varphi_{x_{n}}(x_{1},\ldots,x_{n}))$ if applying the [[transformation]] leaves the function unchanged:
$$f(\varphi_{x_{1}},\ldots,\varphi_{x_{n}})=f(x_{1},\ldots,x_{n})$$
For example, consider the function $f(x,y)=xy$. If we transform $x\to \varphi_{x}(x,y,\alpha)=\alpha x$ and $y\to \varphi_{y}(x,y,\alpha)=\frac{1}{\alpha}y$. If we apply it we get
$$f(\varphi_{x}(x,y,\alpha),\varphi_{y}(x,y,\alpha))=\alpha x \frac{1}{\alpha}y=xy=f(x,y)$$
We get the original function again. When this happens we say that the function $f$ is invariant under the transformation $(x\to \varphi_{x},\ y\to \varphi_{y})$. This denomination works specifically in a pair: the function $f$ is only invariant under a specific transform. If you take a different function or a different transformation, the property is no longer necessarily true.

Another example:
$$f(x,y)=3y,\quad \begin{cases}
x\to \varphi_{x}(x,y,\alpha)=x+\alpha \\
y\to \varphi_{y}(x,y,\alpha)=y
\end{cases}$$
$f$ is invariant under the transformation, but in a very specific way: it's invariant because the transformation only changes $x$, but $f(x,y)$ is actually independent of $x$. As such, $f(x,y)\equiv f(y)$ and so $f(\varphi_{y}(x,y,\alpha))=f(y)$.