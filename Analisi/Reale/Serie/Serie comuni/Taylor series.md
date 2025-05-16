---
wiki-publish: true
---
The **Taylor series** is a [[serie|series]] that expands a real or complex infinitely [[Differential|differentiable]] function $f(x)$ around a point $x_{0}$ using its derivatives
$$\begin{align}
f(x)&=\sum_{n=0}^{\infty} \frac{f^{(n)}(x_{0})}{n!}(x-x_{0})^{n} \\
&=f(x_{0})+ f^{(1)}(x_{0})(x-x_{0})+ \frac{1}{2}f^{(2)}(x_{0})(x-x_{0})^{2}+\ldots
\end{align}$$
where $f^{(n)}$ represents the $n$-th derivative of $f$. If $x_{0}=0$ the series is also known as a **Maclaurin series**:
$$\begin{align}
f(x)&=\sum_{n=0}^{\infty} \frac{f^{(n)}(0)}{n!}x^{n} \\
&=f(0)+f^{(1)}(0)x+ \frac{1}{2}f^{(2)}(0)x^{2}+\ldots
\end{align}$$
### N dimensions
For a function $f(\mathbf{x})$ in $N$ dimensions, the series centered at a point $\mathbf{x}_{0}$ becomes
$$f(\mathbf{x})=\sum\limits_{d=0}^{\infty} \frac{1}{d!}Q_{d}(\mathbf{x}-\mathbf{x}_{0})=\sum\limits_{d=0}^{\infty} \frac{1}{d!}\left[\sum\limits_{|\alpha|=d} \frac{|\alpha|!}{\alpha!}D^{\alpha}f(\mathbf{x}_{0})(\mathbf{x}-\mathbf{x}_{0})^\alpha\right]$$
$\alpha$ is the **multi-index**, defined as a vector $(\alpha_{1},\ldots,\alpha_{N})$ in $\mathbb{N}^{N}$ where each component is used to represent the number of differentiations with respect to that index. We define two operations on it:
1. Its [[norm]] is $\lvert \alpha \rvert\equiv\alpha_{1}+\alpha_{2}+\ldots+\alpha_{N}$ and is called the length of the multi-index.
2. Its factorial is $\alpha!=\alpha_{1}!\alpha_{2}!\ldots\alpha_{N}!$.

The notation $\mathbf{x}^{\alpha}$ represents the monomial $x_{1}^{\alpha_{1}}x_{2}^{\alpha_{2}}\ldots x_{N}^{\alpha_{N}}$. $D^{\alpha}$ is the differentiation [[operator]] corresponding to that multi-index such that
$$D^{\alpha}=\frac{ \partial ^{\lvert \alpha \rvert } }{ \partial^{\alpha_{1}}x_{1}\ldots\partial^{\alpha_{N}}x_{N} } $$
For example, in $\mathbb{N}^{3}$, the multi-index $(1,0,2)$ represents a differentiation with respect to the first variable, none with respect to the second, and two with respect to the third, so it corresponds to the operator
$$D^{(1,0,2)}=\frac{ \partial ^{3} }{ \partial x_{1}\partial ^{2}x_{3} } $$
and the associated monomial would be $\mathbf{x}^{(1,0,2)}=x_{1}x_{3}^{2}$. The polynomial $Q_{d}$ is
$$Q_{d}=\sum_{\lvert \alpha \rvert =d} \frac{\lvert \alpha \rvert !}{\alpha!} D^{\alpha}f(\mathbf{x}_{0})(\mathbf{x}-\mathbf{x}_{0})^{\alpha}$$
which includes all possible $d$-th degree derivatives.

In the case $\mathbf{x}_{0}=\mathbf{0}$, we have
$$f(\mathbf{x})=\sum_{d=0}^{\infty} \frac{1}{d!}Q_{d}(\mathbf{x})=\sum_{d=0}^{\infty} \frac{1}{d!}\left[ \sum_{\lvert \alpha \rvert =d} \frac{\lvert \alpha \rvert !}{\alpha!} D^{\alpha}f(\mathbf{0})\mathbf{x}^{\alpha}  \right]$$
