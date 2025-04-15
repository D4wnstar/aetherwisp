---
aliases:
  - dual basis
  - dual space
---
A **dual vector space** $V^{*}$, or just **dual space**, is a special kind of [[vector space]] associated with another vector space $V$. It is the space of all linear [[functional|functionals]] on $V$, each defined as a linear map $a:V\to K$, where $K$ is the [[field]] both $V$ and $V^{*}$ are defined over. In symbols, the dual space is defined as:
$$V^{*}\equiv\{ a:V\to K\;|\; a(\alpha v+\beta w)=\alpha a(v)+\beta a(w)\quad\forall v,w\in V \}$$
The dimension of $V^{*}$ is the same as the dimension of $V$.

Being a vector space, the dual space comes equipped with a sum and a scalar multiplication operation:
- given $a,b\in V^{*}$, there exists a sum $(a+b)(v)=a(v)+b(v)$ for all $v\in V$.
- given $\alpha \in K$, there exists a scalar multiplication $(\alpha a)(v)=\alpha\cdot a(v)$ for all $v\in V$.

For any given [[basis]] $\{ e_{1},\ldots,e_{n} \}$ in $V$, there exists a corresponding **dual basis** $\{ e_{1}^{*},\ldots,e_{n}^{*} \}$ composed of linear functionals that, when applied to the normal basis vectors, return the [[Kronecker delta]]: $e^{*}_{i}(e_{j})=\delta_{ij}$.