---
wiki-publish: true
aliases:
  - generating function
---
In Hamiltonian mechanics, a **generating function** is a function whose [[partial derivative|partial derivatives]] are [[differential equation|differential equations]] that determine the dynamics of a [[physical system]]. The most important generating function is the [[Hamiltonian]] itself, whose dynamics are found through the [[Hamilton equations]]. The [[partition function]] of an [[ensemble]] is also a generating function.
### Derivation
Let's start with an example. Consider the following [[coordinate transformation]]:
$$\begin{cases}
p=\sqrt{ 2\tilde{p} }\cos \tilde{q} \\
q=\sqrt{ 2\tilde{p} }\sin \tilde{q}
\end{cases}$$
We can invert the first equation to extract $\tilde{p}$ as a function of $p$:
$$\tilde{p}=\frac{p^{2}}{2\cos ^{2}\tilde{q}}$$
We then substitute this in the equation for $q$ to get
$$q=p\tan \tilde{q}$$
These two are an equivalent description of the same transformation; we just rearranged the terms. The difference is, of course, that we are using different quantities. We started with $p(\tilde{p},\tilde{q})$ and $q(\tilde{p},\tilde{q})$, and now we have $\tilde{p}(p,\tilde{q})$ and $q(p,\tilde{q})$. We exchanged $p$ for $\tilde{p}$ and we can now use $(p,\tilde{q})$ as independent coordinates in [[phase space]] (though they are no longer [[canonical coordinates]] as this is not a [[canonical transformation]]).

In general, we have four coordinates $q,\tilde{q},p,\tilde{p}$ and four ways we can mix them:
$$(q,\tilde{q}),\quad(\tilde{p},q),\quad(p,\tilde{q}),\quad(p,\tilde{p})$$
Each of these encodes a way of describing a point in phase space when dealing with a transformation $(p,q)\mapsto(\tilde{p},\tilde{q})$.

Take for instance $(\tilde{\mathbf{p}},\mathbf{q})$ as independent coordinates. These, in general, will be given by
$$\begin{cases}
p_{i}=\rho_{i}(\tilde{\mathbf{p}},\mathbf{q},t) \\
\tilde{q}_{j}=\tilde{\mu}_{j}(\tilde{\mathbf{p}},\mathbf{q},t)
\end{cases}$$
where $\rho_{i}$ and $\tilde{\mu}_{j}$ are some appropriate functions. We can invert these to get $(\mathbf{p},\mathbf{q})$ back:
$$\begin{cases}
p_{i}=u_{i}(\tilde{\mathbf{p}},\tilde{\mathbf{q}},t)\equiv \rho_{i}(\tilde{\mathbf{p}},v(\tilde{\mathbf{p}},\tilde{\mathbf{q}},t),t) \\
q_{j}=v_{j}(\tilde{\mathbf{p}},\tilde{\mathbf{q}},t)
\end{cases}$$
We will claim that $\rho_{i}$ and $\tilde{\mu}_{j}$ are the partial derivatives of some function $F_{2}(\tilde{\mathbf{p}},\mathbf{q},t)$:
$$p_{i}=\rho_{i}(\tilde{\mathbf{p}},\mathbf{q},t)\equiv \frac{ \partial F_{2} }{ \partial q_{i} } (\tilde{\mathbf{p}},\mathbf{q},t),\quad \tilde{q}_{j}=\tilde{\mu}_{j}(\tilde{\mathbf{p}},\mathbf{q},t)\equiv \frac{ \partial F_{2} }{ \partial \tilde{p}_{j} } (\tilde{\mathbf{p}},\mathbf{q},t)$$
Note that we are specifically mixing the derivatives here: $p_{i}$ needs a derivative in $q_{i}$ and $\tilde{q}_{j}$ needs a derivative in $\tilde{p}_{j}$. For the inversion of $\tilde{\mathbf{q}}$ into $\mathbf{q}$ to occur, we must have
$$\det\left( \frac{ \partial ^{2}F_{2} }{ \partial \tilde{p}_{i}\partial q_{j}}  \right)\neq 0$$
Basically, the [[Hessian]] of $F_{2}$ must have nonzero [[determinant]]. We shall now make the following claim:

> [!info] Canonical transformations from generating functions
> If a coordinate transformation in phase space is defined by the derivatives of a function $F_{2}(\tilde{\mathbf{p}},\mathbf{q},t)$ whose Hessian has nonzero determinant, in the form
> $$\left\{\begin{align}
> p_{i}&=\frac{ \partial F_{2} }{ \partial q_{i} } (\tilde{\mathbf{p}},\mathbf{q},t) \\
> \tilde{q}_{j}&=\frac{ \partial F_{2} }{ \partial \tilde{p}_{j} } (\tilde{\mathbf{p}},\mathbf{q},t)
> \end{align}\right.$$
> the transformation is canonical and the conjugate Hamiltonian is
> $$K=\tilde{H}+\frac{ \partial F_{2} }{ \partial t } $$

> [!quote]- Proof
> Not reported here. See [here](https://mega.nz/file/YUVUSTzT#nQfNUxMWc52lOEjGbGXbUgPNaQNY0WkjAdV62qyptQs) if you can read Italian.

$F_{2}$ is not the only kind of function that can do this. There is actually one kind of function for each of the four pairs of mixed coordinates we saw above. These are typically called $F_{1},F_{2},F_{3}$ and $F_{4}$ and collectively they are known as the **generating functions** of canonical transformations (of the first, second, third and fourth kind). Each of these types comes equipped with a proposition similar to the one above for $F_{2}$, with a different mix of coordinates:
$$\left\{\begin{align}
p_{i}&=\frac{ \partial F_{1} }{ \partial q_{i} } (\mathbf{q},\tilde{\mathbf{q}},t) \\
\tilde{p}_{j}&=-\frac{ \partial F_{1} }{ \partial \tilde{q}_{j} } (\mathbf{q},\tilde{\mathbf{q}},t)
\end{align}\right.\qquad\qquad K=\tilde{H}+\frac{ \partial F_{1} }{ \partial t } $$
$$\left\{\begin{align}
q_{i}&=-\frac{ \partial F_{3} }{ \partial p_{i} } (\mathbf{p},\tilde{\mathbf{q}},t) \\
\tilde{p}_{j}&=-\frac{ \partial F_{3} }{ \partial \tilde{q}_{j} } (\mathbf{p},\tilde{\mathbf{q}},t)
\end{align}\right.\qquad\qquad K=\tilde{H}+\frac{ \partial F_{3} }{ \partial t }$$
$$\left\{\begin{align}
q_{i}&=-\frac{ \partial F_{4} }{ \partial p_{i} } (\mathbf{p},\tilde{\mathbf{p}},t) \\
\tilde{q}_{j}&=\frac{ \partial F_{4} }{ \partial \tilde{p}_{j} } (\mathbf{p},\tilde{\mathbf{p}},t)
\end{align}\right.\qquad\qquad K=\tilde{H}+\frac{ \partial F_{4} }{ \partial t }$$
The equivalence of all of these is proven by the fact that they are all related by a [[Legendre transform]]:
$$F_{1}=F_{1},\quad F_{2}=F_{1}+\tilde{q}\tilde{p},\quad F_{3}=F_{1}-qp,\quad F_{4}=F_{1}-qp+\tilde{q}\tilde{p}$$

$F_{2}$ is a particularly relevant case as many interesting canonical transformations are of the second kind. For example, the identity transformation $p_{i}=\tilde{p}_{i}$, $\tilde{q}_{i}=q_{i}$ is a second-kind transformation with
$$F_{2}(\tilde{\mathbf{p}},\mathbf{q},t)=\sum_{i}\tilde{p}_{i}q_{i}$$
Extended point transformations are also second-kind:
$$p_{i}=\sum_{j}\tilde{p}_{j}\frac{ \partial v_{j} }{ \partial q_{j} } (\mathbf{q},t),\quad \tilde{q}_{i}=v_{i}(\mathbf{q},t),\quad F_{2}(\tilde{\mathbf{p}},\mathbf{q},t)=\sum_{i}\tilde{p}_{i}v_{i}(\mathbf{q},t)$$
(this also automatically proves that all extended point transformations are canonical).