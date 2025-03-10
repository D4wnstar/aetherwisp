---
aliases:
  - path
---
A **curve**, technically a **parametric curve**, is a continuous function that maps a one-dimensional interval to a higher $N$-dimensional space: $γ : I → \mathbb{R}^N$, $t\to \gamma(t)$ where $I$ is a real interval, $t$ is called the **parameter** of the curve and $N\geq2$. The image $γ(I)$ is called the **support** of the curve.
### Properties
- A curve is said to be **bounded** (**unbounded**) if its support is a bounded (unbounded) set.
- A curve is said to be **closed** if $I = [a,b]$ is a closed and bounded interval and $\gamma(a) = \gamma(b)$ holds.
- A curve is said to be **simple** if it is injective except at most at the endpoints, that is, if and only if
$$\gamma(t_1)=\gamma(t_2)\;\Rightarrow\;t_1=t_2\;o\;t_1=a,\;t_2=b$$
- A curve is said to be **regular** if it is of class $C^1$ and $\gamma'(t)\neq0\;\forall t\in \mathring{I}$ holds. It is said to be **piecewise regular** if there exists a partition $P$ of the interval $I$ defined as $a=x_0<x_1<x_2<\cdots<x_N=b$ such that the restriction to $[x_{i-1},x_i]$ is a regular curve.
- Two regular curves $\gamma_1:I_1\rightarrow\mathbb{R}^N$ and $\gamma_2:I_2\rightarrow\mathbb{R}^N$ are said to be **equivalent** if they have the same support and there exists a class $C^{1}$ [[diffeomorphism]] $\varphi:I_1\rightarrow I_2$ such that $\gamma_1=\gamma_2\circ\varphi$. The two curves have the same orientation if $\varphi'(s)>0\;\forall s\in I_1$.

The tangent vectors $\hat{\tau}$ of a curve are given by
$$\hat{\tau}:\mathring{I}\rightarrow\mathbb{R}^{N}\quad\hat{\tau}(t)= \frac{\gamma'(t)}{||\gamma'(t)||}$$
