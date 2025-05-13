---
wiki-publish: true
aliases:
  - hermitian product
  - dot product
---
 The **scalar product**, also called **dot product**, is an operation between two [[Vector space|vectors]] that produces a [[scalar]], hence the name. If the vectors are complex, it is also called the **Hermitian product**. It is denoted in a variety of ways: $(v,w)$, $v\cdot w$ or $\braket{ v | w }$ (in [[notazione braket|braket notation]]).

In finite-dimensional vector spaces, such as $\mathbb{R}^{N}$ or $\mathbb{C}^{N}$, the scalar product is defined as a sum of products of the vector components. Let $v,w$ be two vectors in the space, then the scalar product between the two is
$$(v,w)\equiv\sum\limits_{i=0}^{N}v_{i}^{*}w_{i}$$
where $v_{i}$ and $w_{i}$ are the $i$-th component of the vectors and the $*$ symbol denotes the [[complex conjugate]]. If $v_{i}$ is real, it can safely be removed, as $v_{i}^{*}=v_{i}$ for any real. It can also be expressed geometrically as
$$(v,w)\equiv\lVert v \rVert \lVert w \rVert \cos\theta$$
where $\theta$ is the angle between the two vectors and $\lVert \cdot \rVert$ refers to the [[norm]] of a vector.

The scalar product of an element with itself satisfies all of the properties of a norm and is called the **norm induced by the scalar product**, and denoted as usual: $(v,v)=\lVert v \rVert$.

The scalar product can also be defined on infinite-dimensional spaces, such as [[Spazio di Hilbert|Hilbert spaces]] or [[Spazi Lp|L^p spaces]], by converting sums to integrals. Then taking two functions $f(x)$ and $g(x)$ in such a space, the scalar product between them is
$$(f,g)\equiv\int_{-\infty}^{+\infty}f^{*}(x)g(x)\ dx,\qquad( f, f)=\int_{-\infty}^{+\infty}|f(x)|^{2}\ dx$$

> [!question] A note on notation
> These notes employ all of the three shown notations for the scalar product, each in the context they are most likely to be found in in literature. Round brackets $(v,w)$ are used in mathematics, the dot $v\cdot w$, especially using bold font $\mathbf{v}\cdot \mathbf{w}$, is commonplace in physics in general, and [[Notazione braket|braket notation]] $\braket{ v | w }$ is standard in quantum physics.
### Properties
The scalar product satisfies the following properties:
1. It is linear in the right-hand member[^1]. Given $\alpha,\beta \in \mathbb{C}$, $( v, \alpha w + \beta z)=\alpha ( v, w)+\beta ( v, z)$. 
2. It is antilinear in the left-hand member, $( \alpha v + \beta w, z)=\alpha^{\ast} ( v, w)+\beta^{\ast} ( v, z)$. Over reals, it is linear in both members (also said to be bilinear).
3. It is distributive, $( v, w+u)=( v, w)+( v, z)$.
4. Commutation leads to the conjugate:  $( v, w)=\overline{( w, v)}$. Over reals, it is commutative.
5. The product of an element with itself is always nonnegative, $( v, v)\geq0$.
6. The product of an element with itself is zero only if and only if $v$ is zero, $( v, v)=0\Leftrightarrow v=0$.
7. It satisfies the [[Disuguaglianza di Cauchy-Schwarz|Cauchy-Schwarz inequality]], $(v,w)\leq \lVert v \rVert\lVert w \rVert$.
8. It is a continuous operation, i.e. given a sequence $\{x_{n}\}$ converging to $x\in \mathcal{H}$ where $\mathcal{H}$  is a Hilbert space, it holds that for every $y\in \mathcal{H}$ we have $\lim\limits_{n \rightarrow \infty}(y,x_{n})=(y,x)$.
### In basis expression
Consider the vectors $\mathbf{v}_{1}$ and $\mathbf{v}_{2}$ in some vector space $V$ equipped with a [[Basis]] $\{ \mathbf{e}_{1},\ldots,\mathbf{e}_{n} \}$. They can be expressed as a [[linear combination]] of basis vectors as $\mathbf{v}_{1}=\sum_{i=1}^{n}\alpha_{i}\mathbf{e}_{i}$ and $\mathbf{v}_{2}=\sum_{j=1}^{n}\beta_{j}\mathbf{e}_{j}$, using suitable values $\alpha_{i}$ and $\beta_{i}$. The scalar product between these two is
$$\begin{align}
\mathbf{v}_{1}\cdot \mathbf{v}_{2}&=\left( \sum_{i=1}^{n} \alpha_{i}\mathbf{e}_{i} \right)\cdot\left( \sum_{j=1}^{n} \beta_{j}\mathbf{e}_{j} \right)=\sum_{i=1}^{n} \alpha_{i}\mathbf{e}_{i}\cdot\left( \sum_{j=1}^{n} \beta_{j}\mathbf{e}_{j} \right)= \\
&=\sum_{i=1}^{n} \alpha_{i}\sum_{j=1}^{n} \beta_{j}(\mathbf{e}_{i}\cdot \mathbf{e}_{j})=\sum_{i=1}^{n}\sum_{j=1}^{n} \alpha_{i}\beta_{j}\delta_{ij}= \\
&=\sum_{i=1}^{n} \alpha_{i}\underbrace{ (\beta_{1}\delta_{i1}+\ldots+\beta_{n}\delta_{in}) }_{ \beta_{i}\delta_{ii} }=\sum_{i=1}^{n} \alpha_{i}\beta_{i}
\end{align}$$
using the [[Kronecker delta]].

---

### Su matrici
Il prodotto scalare può anche essere applicato su matrici. Prendiamo $\hat{A},\hat{B}\in M_{2}(\mathbb{C})$ matrici $2\times2$. Considero la *traccia* della matrice $Tr(\hat{A})=\sum\limits_{i=1}^{n}A_{ii}$. E' importante notare che la traccia è *unica* e non cambia *in base alla rappresentazione* della matrice (ossia la base rispetto al quale è espressa):
$$Tr\hat{A}=\sum\limits_{i=1}^{n}\langle\psi_{i}|\hat{A}\psi_{i}\rangle\;\forall\;\text{base o.n.}\{|\psi_{i}\rangle\}_{i=1}^{n}\in\mathbb{C}^{n}$$
La matrice $\hat{U}=[\langle \psi_{k}|\phi_{i}\rangle]$ è unitaria, ossia $\hat{U}\hat{U}^{\dagger}=\hat{\mathbb{1}}=\hat{U}^{\dagger}\hat{U}$.

Prendendo $|\psi\rangle,|\phi\rangle\in\mathbb{C}^{N}$. Il prodotto scalare possiamo scriverlo come
$$\langle \psi|\phi\rangle=\sum\limits_{i=1}^{n}\psi^{\ast}_{i}\phi_{i}=\sum\limits_{i=1}^{n}\langle \psi|\chi_{i}\rangle\langle \chi_{i}|\phi\rangle=\ldots$$usando una base ortonormale $\{|\chi_{i}\rangle\}^{n}_{i=1}\in\mathbb{C}^{N}$ da cui, usando la completezza dei [[Proiettore|proiettori]]
$$\ldots=\langle \psi|\underbrace{\left( \sum\limits_{i=i}^{n}\hat{P}_{\chi_{i}}\right)}\limits_{\hat{\mathbb{1}}}|\phi\rangle$$
Possiamo generalizzare a $|\psi\rangle,|\phi\rangle\in L^{2}(\mathbb{R},dx)$, ricordando che $\psi^{\ast}_{i}=\overline{\langle \chi_{i}|\psi\rangle}$,
$$\langle \psi|\phi\rangle=\int_{\mathbb{R}}\psi^{\ast}(x)\phi(x)dx=\int_{\mathbb{R}}\langle \psi|x\rangle \langle x|\phi\rangle=\ldots$$
ma possiamo descrivere $\phi(x)$ come
$$\phi(x)=\int \delta(\bar{x}-x)\phi(\bar{x})d\bar{x}$$
Si ha inoltre
$$\int_{\mathbb{R}}|x\rangle\langle x|dx=\hat{\mathbb{1}}$$
dove $|x\rangle\langle x|$ è uno *pseudoproiettore* di una base di pseudovettori. Allora tornando indietro
$$\ldots=\langle \psi|\left( \int_{\mathbb{R}}|x\rangle\langle x| dx\right)|\phi\rangle$$


[^1]: Being on the right-hand member specifically is actually a convention. Using the right-hand side is typical in physics. In mathematics, the left-hand side is more commonly used. The same applies to antilinearity, with mathematicians usually place on the right-hand side instead.
