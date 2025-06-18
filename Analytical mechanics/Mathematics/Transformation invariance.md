---
wiki-publish: true
aliases:
  - invariant under the transformation
---
A function $f(\mathbf{x})$ is said to be **invariant under the transformation** $\mathbf{x}\mapsto \varphi(\mathbf{x})=(\varphi_{1}(\mathbf{x}),\ldots,\varphi_{n}(\mathbf{x}))$ if applying the [[transformation]] leaves the function unchanged:
$$f(\varphi(\mathbf{x}))=f(\mathbf{x})$$
For example, consider the function $f(x,y)=xy$ and the transformation
$$\varphi:(x,y)\mapsto \varphi(x,y;\alpha)=\left( \alpha x, \frac{y}{\alpha} \right)$$
If we apply it we get
$$f(\varphi(x,y;\alpha))=\alpha x \frac{1}{\alpha}y=xy=f(x,y)$$
We get the original function again. When this happens we say that the function $f$ is invariant under the transformation $(x\to \varphi_{x},\ y\to \varphi_{y})$. This denomination works specifically for that pair: the function $f$ is only invariant under that specific transformation. If you take a different function or a different transformation, the property is no longer necessarily true.

Another example:
$$f(x,y)=3y,\quad \begin{cases}
x\to \varphi_{x}(x,y,\alpha)=x+\alpha \\
y\to \varphi_{y}(x,y,\alpha)=y
\end{cases}$$
$f$ is invariant under the transformation, but in a very specific way: it's invariant because the transformation only changes $x$, but $f(x,y)$ is actually independent of $x$. As such, $f(x,y)\equiv f(y)$ and so $f(\varphi_{y}(x,y,\alpha))=f(y)$.