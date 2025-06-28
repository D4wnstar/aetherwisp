---
wiki-publish: true
---
The **harmonic series** is the [[serie|series]]
$$\sum\limits_{n=1}^{\infty} \frac{1}{n}=1+ \frac{1}{2}+ \frac{1}{3}+ \frac{1}{4}+\ldots$$
It is divergent. The **generalized harmonic series** is the [[serie|series]]
$$\sum\limits_{n=1}^{\infty} \frac{1}{n^{\alpha}},\quad \alpha\in \mathbb{R} \quad\begin{cases}\text{diverges for}& \alpha\in\ ]-\infty,1] \\ \text{converges for} & \alpha\in\ ]1,\infty[ \end{cases}$$

> [!quote] Proof of convergence interval
> For $\alpha\leq0$, the series does not satisfy the necessary limit for convergence, hence it diverges.
> 
> For $\alpha\in\;]0,1]$, note that
> $$\frac{1}{n}\leq \frac{1}{n^{\alpha}}\quad\text{for all } n\in\mathbb{N}^{+}$$
> so by the [[criterio del confronto|comparison test]], the series diverges.
> 
> For $\alpha\in[2,+\infty[$, we have
> $$\frac{1}{n^{\alpha}}\leq \frac{1}{n^{2}}\quad\text{for all }n\in \mathbb{N}^{+}$$
> 
> For $\alpha\in]1,2[$, we use the [[criterio della serie condensata|condensation test]]:
> $$\sum\limits_{n=0}^{\infty}a_{2^{n}}2^{n}=\sum\limits_{n=0}^{\infty} \frac{1}{2^{\alpha n}}2^{n}=\sum\limits_{n=0}^{\infty}\left( \frac{1}{2^{\alpha-1}}\right)^{n}$$
> which is a geometric series with ratio $\rho= 1/2^{\alpha-1}$. This converges if $\rho<1$, which happens when $\alpha>1$. Therefore, it converges for $\alpha\in]1,2[$.
