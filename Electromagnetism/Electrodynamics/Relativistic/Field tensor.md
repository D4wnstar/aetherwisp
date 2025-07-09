---
wiki-publish: true
aliases:
  - dual tensor
---
The **field tensor** is the [[Lorentz transformation|relativistic]] generalization of the [[Electric field|electric]] and [[Magnetic field|magnetic fields]]:
$$F^{\mu \nu}\equiv \begin{pmatrix}
0 & E_{x}/c & E_{y}/c & E_{z}/c \\
-E_{x}/c & 0 & B_{z} & -B_{y} \\
-E_{y}/c & -B_{z} & 0 & B_{x} \\
-E_{z}/c & B_{y} & -B_{x} & 0
\end{pmatrix}$$
It is a second-rank antisymmetric [[tensor]]. It plays the part of the [[Lorentz transformation]] matrix in relativity. An alternative and equivalent formulation is the **dual tensor**
$$G^{\mu \nu}\equiv \begin{pmatrix}
0 & B_{x} & B_{y} & B_{z} \\
-B_{x} & 0 & -E_{z}/c & -E_{y}/c \\
-B_{y} & E_{z}/c & 0 & -E_{x}/c \\
-B_{z} & -E_{y}/c & E_{x}/c & 0
\end{pmatrix}$$
which is used in the same way and leads to the same transformations.
### Derivation
It's quite evident from the [[transformations of E and B]] that when you move from one [[frame of reference]] to another, the fields don't just change on their own: they mix. As such, we can't just describe them as (the spatial parts of) plain old [[Four-vector|four-vectors]]. We need some way of expressing them together, as a single joint object that encodes not just the fields, but the relationship between the fields. Looking back, we already did something similar in the past: when we wanted to represent the action of an electromagnetic field as one cohesive object, we made a *[[tensor]]*, specifically, the [[Maxwell stress tensor]]. Here, we follow in our own footsteps: the object we're looking for is an *antisymmetric, second order tensor*[^1]. But we are not working in 3D anymore, we're in [[spacetime]]! So this tensor is going to need to be $4\times4$.

Let's start from a four-vector in a frame $\mathcal{S}$. Such a vector, call it $a^{\mu}$, changes in relativity using a simple [[Lorentz transformation]] matrix $\Lambda$:
$$\bar{a}^{\mu}=\Lambda_{\nu}^{\mu}a^{\nu}$$
In $\Lambda$, superscript ($\mu$) is the row and subscript ($\nu$) is the column. We'll use the overbar now to denote the new frame $\bar{\mathcal{S}}$ instead of the prime $\mathcal{S}'$ (which gets in the way of the superscript). In case of constant-speed motion over the $x$ axis,
$$\Lambda=\begin{pmatrix}
\gamma & -\gamma \beta & 0 & 0 \\
-\gamma \beta & \gamma & 0 & 0 \\
 0 & 0 & 1 & 0 \\
 0 & 0 & 0 & 1
\end{pmatrix}$$
A second-rank tensor, call it $t$, has two indexes (it's a [[matrix]]) and will need two transformations, one for each index:
$$\bar{t}^{\mu \nu}=\Lambda_{\lambda}^{\mu}\Lambda_{\sigma}^{\nu}t^{\lambda \sigma}\tag{1}$$
We also claimed we wanted our tensor to be antisymmetric. This just means $t^{\mu \nu}=-t^{\nu \mu}$, which is the same as saying that the diagonal is all zeros and that the off-diagonals are mirrored across the diagonal, with their sign flipped. In practice, a generic antisymmetric tensor reads
$$t^{\mu \nu}=\begin{pmatrix}
0 & t^{01} & t^{02} & t^{03} \\
-t^{01} & 0 & t^{12} & t^{13} \\
-t^{02} & -t^{12} & 0 & t^{23} \\
-t^{03} & -t^{13} & -t^{23} & 0
\end{pmatrix}$$
Count the unique elements: there's only *six*. Hopefully you start to see why we want an antisymmetric tensor and what these components are. But why not *symmetric*? Because a symmetric tensor would also have elements on the diagonal, for a total of *ten*. That's four too many, so that can't happen.

We, of course, want to see what the components are. To do so, let's look at what the transformation rule $(1)$ does to this tensor. $\bar{t}^{01}$ goes like
$$\bar{t}^{01}=\Lambda_{\lambda}^{0}\Lambda_{\sigma}^{1}t^{\lambda \sigma}$$
By definition of $\Lambda$, $\Lambda_{\lambda}^{0}$ (the first row) is nonzero only when $\lambda=0,1$. Similarly, $\Lambda_{\sigma}^{1}$ (the second row) is also nonzero only in $\sigma=0,1$. So, explicitly
$$\bar{t}^{01}=\Lambda_{0}^{0}\Lambda_{0}^{1}t^{00}+\Lambda_{0}^{0}\Lambda_{1}^{1}t^{01}+\Lambda_{1}^{0}\Lambda_{0}^{1}t^{10}+\Lambda_{1}^{0}\Lambda_{1}^{1}t^{11}$$
Due to antisymmetry, $t^{00}=t^{11}=0$ and $t^{10}=-t^{01}$ so
$$\bar{t}^{01}=(\Lambda_{0}^{0}\Lambda_{1}^{1}-\Lambda_{1}^{0}\Lambda_{0}^{1})t^{01}=(\gamma ^{2}-(\gamma \beta)^{2})t^{01}=t^{01}$$
You can repeat these procedure for every single one of the six unique elements:
$$\begin{align}
\bar{t}^{01}=t^{01},\quad \bar{t}^{02}&=\gamma(t^{02}-\beta t^{12}),\quad \bar{t}^{03}=\gamma(t^{03}+\beta t^{31}) \\
\bar{t}^{23}=t^{23},\quad \bar{t}^{31}&=\gamma(t^{31}+\beta t^{03}),\quad \bar{t}^{12}=\gamma(t^{12}-\beta t^{02})
\end{align}\tag{2}$$
The lettering might be a little different, but these are *precisely* the [[transformations of E and B]]:
$$\begin{align}
&\bar{E}_{x}=E_{x},&\bar{E}_{y}&=\gamma(E_{y}-vB_{z}),&\bar{E}_{z}&=\gamma(E_{z}+vB_{y}) \\
&\bar{B}_{x}=B_{x},&\bar{B}_{y}&=\gamma\left( B_{y}+ \frac{v}{c^{2}}E_{z} \right),&\bar{B}_{z}&=\gamma\left( B_{z}- \frac{v}{c^{2}}E_{y} \right)
\end{align}\tag{3}$$
If we compare the elements of the tensor directly with their corresponding electromagnetic transformation rule (first line of $(2)$ with first line of $(3)$, second line with second line), we can construct the tensor we were looking for[^2]
$$\boxed{F^{\mu \nu}\equiv \begin{pmatrix}
0 & E_{x}/c & E_{y}/c & E_{z}/c \\
-E_{x}/c & 0 & B_{z} & -B_{y} \\
-E_{y}/c & -B_{z} & 0 & B_{x} \\
-E_{z}/c & B_{y} & -B_{x} & 0
\end{pmatrix}}$$
This is known as the **field tensor** and it collectively describes the behavior of the entire electromagnetic field.

If you look closely, the field tensor is not the *only* tensor we can define. In fact, we if we compare the first line of $(3)$ with the *second* line of $(2)$ and the second with the first we get
$$\boxed{G^{\mu \nu}\equiv \begin{pmatrix}
0 & B_{x} & B_{y} & B_{z} \\
-B_{x} & 0 & -E_{z}/c & -E_{y}/c \\
-B_{y} & E_{z}/c & 0 & -E_{x}/c \\
-B_{z} & -E_{y}/c & E_{x}/c & 0
\end{pmatrix}}$$
This alternative tensor is known as the **dual tensor** and it describes much the same thing as field tensor. In fact, you can get $G$ from $F$ by substituting $\mathbf{E}/c\to \mathbf{B}$ and $\mathbf{B}\to-\mathbf{E}/c$. Which one you end up using is a matter of preference.

Thus, the field tensor packs up the entirety of the electromagnetic fields into a single object, which plays the part of a Lorentz transformation matrix.

[^1]: Essentially a fancy name for an [[Symmetric matrix|antisymmetric matrix]].

[^2]: There's a bit of conventional wiggle room here: some authors don't divide the electric fields by $c$ and instead multiply the magnetic field by it, so that they get $E_{x}$ and $cB_{z}$ instead of $E_{x}/c$ instead of $B_{z}$. Also, some others flip the signs so that the minuses are in the top right instead of bottom left. These are all equivalent notations, but do lead to aesthetically different formulas, so be a little careful.
