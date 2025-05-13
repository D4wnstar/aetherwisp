---
wiki-publish: true
aliases:
  - anticommutator
  - Baker-Campbell-Hausdorff formula
---
The **commutator** is a value indicating how two elements related by a binary operation fail to satisfy the commutative property. In the case of multiplication, given two elements $A$ and $B$, their commutator is defined as
$$[A,B] = AB - BA,$$
which equals zero if and only if the commutative property holds between $A$ and $B$ (and thus $AB = BA$).

The **anticommutator** is the same operation with the opposite sign:
$$\{A,B\} = AB + BA$$
Not to be confused with the identically denoted and often compared to [[Poisson brackets]].
### Properties  
The commutator has several properties:
1. $[A + B, C] = [A, C] + [B, C]$
2. $[AB, C] = ABC - CAB$
3. $[A, A] = 0$, meaning an element always commutes with itself.
4. $[A, B] = -[B, A]$, known as anticommutativity.
5. $[A, [B, C]] + [B, [C, A]] + [C, [A, B]] = 0$, known as the Jacobi identity.
6. $[A, B]^{+} = -[A, B]$, where $^{+}$ denotes the [[Adjoint operator|adjoint]].
7. $[T,c]=0$ where $T$ is an [[Operatore|operator]] and $c$ is a [[scalar]] constant.
8. $[T,f(T)]$, meaning an operator always commutes with functions of itself.
9. If two operators $A$ and $B$ commute up to a constant $c$, $[A, B] = c \hat{\mathbf{1}}$, then the **Baker-Campbell-Hausdorff formula** holds: $e^{A + B} = e^{-[A,B]/2} e^{A} e^{B}$. Note the additional scaling factor $e^{-[A,B]/2}$ compared to the usual case.

In the case of two operator exponentials $e^{-A}$ and $e^{A}$ acting on another operator $B$, one can use **nested commutators**:  
$$\begin{align}  
e^{A} B e^{-A} &= \sum_{k=0}^{\infty} \frac{1}{k!} \underbrace{[A, [A, \ldots [A, B] }_{k \text{ times}} \ldots]] \\  
&= B + [A, B] + \frac{1}{2}[A, [A, B]] + \frac{1}{3!}[A, [A, [A, B]]] + \ldots  
\end{align}$$

> [!info] Proof  
> We can expand the exponentials separately:  
> $$\begin{align}  
> &\quad\left( 1 + A + \frac{A^{2}}{2} + \ldots \right) B \left( 1 - A + \frac{A^{2}}{2} + \ldots \right) = \\  
> &= \left( 1 + A + \frac{A^{2}}{2} + \ldots \right) \left( B - BA + B \frac{A^{2}}{2} + \ldots \right) = \\  
> &= B - BA + \frac{BA^{2}}{2} + AB - ABA - \frac{A^{2}}{2}B + \ldots = \\  
> &= B + [A, B] + \left( \frac{1}{2}BA^{2} - ABA + \frac{1}{2}A^{2}B \right) + \ldots \\  
> &= B + [A, B] + \frac{1}{2} [A, [A, B]] + \ldots  
> \end{align}$$

This also holds for $e^{A} f(B) e^{-A}$ since $e^{A} f(B) e^{-A} = f(e^{A} B e^{-A})$. Just replace $B$ with $f(B)$ in the above formula.
### In quantum mechanics
The commutator is of fundamental importance in quantum mechanics, as it allows expressing numerous concepts related to the [[Disuguaglianza di Heisenberg|uncertainty principle]]. The most important commutation relation is the so-called **canonical commutation relation**, which shows that the position operator and the momentum operator do not commute[^1]
$$[\hat{q}, \hat{p}] = i\hbar,$$
where $\hbar$ is the [[Planck constant|reduced Planck constant]].

> [!example] Proof  
> Consider the [[Spazi Lp|L^2]] [[Spazio di Hilbert|Hilbert space]]  over $\mathbb{R}$. The commutator in this space is defined as $[\hat{q}, \hat{p}]: L^{2}(\mathbb{R}) = \mathcal{H} \to \mathcal{H}$. For a generic [[funzione d'onda|wave function]] $\psi(x)$ (operators must act on *something*), we have
> $$([\hat{q}, \hat{p}]\psi)(x) = (\hat{q}\hat{p}\psi)(x) - (\hat{p}\hat{q}\psi)(x) = x(\hat{p}\psi)(x) + i\hbar \partial_{x}(\hat{q}\psi)(x) = \ldots$$
> remembering that operators always act on what is to their right. Continuing,
> $$\ldots = -i\hbar x\partial_{x}\psi(x) + i\hbar\partial_{x}(x\psi(x)) = -\cancel{i\hbar x\partial_{x}\psi(x)} + i\hbar \psi(x) +\cancel{i\hbar x\partial_{x}(x)}$$
> thus
> $$([\hat{q}, \hat{p}]\psi(x)) = i\hbar \psi(x)$$
> which, being true for all $\psi(x) \in L^{2}(\mathbb{R})$, allows us to conclude
> $$[\hat{q}, \hat{p}] = i\hbar$$

In three dimensions, for the position vector $\mathbf{r}$ and the [[Linear momentum|momentum]] $\mathbf{p}$, we have
$$[r_{i}, p_{j}] = -[p_{i}, r_{j}] = i\hbar\delta_{ij}, \quad [r_{i}, r_{j}] = [p_{i}, p_{j}] = 0$$
with indices referring to the three spatial dimensions and $\delta_{ij}$ being the [[Kronecker delta]]. In other words, position always commutes with position; momentum always commutes with momentum; they commute between each other only in different coordinates, otherwise yielding $i\hbar$.

For the [[momento angolare quantistico|quantum angular momentum]] along the $z$-axis $L_{z}$, the following hold:
$$[L_{z}, x] = i\hbar y, \quad [L_{z}, y] = -i\hbar x, \quad [L_{z}, z] = 0$$
$$[L_{z}, p_{x}] = i\hbar p_{y}, \quad [L_{z}, p_{y}] = -i\hbar p_{x}, \quad [L_{z}, p_{z}] = 0$$

[^1]: Note that the commutator of two operators is itself an operator. To be precise, the equation is $[\hat{q},\hat{p}]=i\hbar \hat{\mathbf{1}}$, where $\hat{\mathbf{1}}$ is the [[identity operator]].
