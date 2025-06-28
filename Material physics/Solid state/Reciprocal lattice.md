---
wiki-publish: true
---
The **reciprocal lattice** of a [[Bravais lattice]] is, loosely speaking, the lattice formed by its [[Wavenumber|wavevectors]] in [[reciprocal space]]. In this context, the original Bravais lattice is said to be the **direct lattice** (or **real lattice**).

Mathematically, consider a Bravais lattice of points $\mathbf{R}$ and a [[Plane wave]] $e^{i\mathbf{k}\cdot \mathbf{r}}$. The set of all wavevectors $\mathbf{K}$ that yield plane waves with the same periodicity of the Bravais lattice identifies another lattice known as the reciprocal lattice. The vectors $\mathbf{K}$ are those that satisfy
$$e^{i\mathbf{K}\cdot (\mathbf{r}+\mathbf{R})}=e^{i\mathbf{K}\cdot \mathbf{r}}\quad \Rightarrow\quad e^{i\mathbf{K}\cdot \mathbf{R}}=1\quad\Rightarrow \quad \mathbf{K}\cdot \mathbf{R}=2\pi n\quad\text{where }n\in \mathbb{Z}$$
for all points $\mathbf{R}$. To visualize this, think of a 1D lattice (a line of equally spaced points). Now imagine a plane wave that passes through all of those points. The $\mathbf{K}$ that defines that wave, alongside all its periodic multiples ($2\pi \mathbf{K}$) makes the 1D reciprocal lattice.

The wavevector is the spatial frequency of a wave, and in this case the spatial frequency of the lattice points. But given a function describing position, the spatial frequency can be extracted by applying the [[Trasformata di Fourier|Fourier transform]]. Thus, a more powerful interpretation is that the reciprocal lattice is the Fourier transform of the direct lattice.
### Properties
- The reciprocal lattice is a Bravais lattice.
- When working with a [[Crystal|crystal structure]] (a lattice with a basis), the reciprocal lattice is exclusively defined from the underlying Bravais lattice. The basis makes no difference.
- The reciprocal lattice of a reciprocal lattice is the direct lattice. The proof can be developed explicitly, but you can intuitively convince yourself of this by recognizing that the antitransform of a Fourier transform is the original function.
### Reciprocal cell
Being a Bravais lattice, the reciprocal lattice comes equipped with a set of primitive vectors that non-uniquely determine a primitive cell. Call these vectors $\mathbf{b}_{1},\ldots,\mathbf{b}_{M}$ for an $M$-dimensional lattice. Any point on the reciprocal lattice can be identified by a [[linear combination]] of these:
$$\mathbf{K}=\sum_{i=1}^{M} m_{i}\mathbf{b}_{i}$$
It can be proven that in three dimensions, the reciprocal primitive vectors are related to the direct primitive vectors $\mathbf{a}_{1},\mathbf{a}_{2},\mathbf{a}_{3}$ by
$$\mathbf{b}_{1}=2\pi \frac{\mathbf{a}_{2}\times \mathbf{a}_{3}}{\mathbf{a}_{1}\cdot(\mathbf{a}_{2}\times \mathbf{a}_{3})},\quad \mathbf{b}_{2}=2\pi \frac{\mathbf{a}_{3}\times \mathbf{a}_{1}}{\mathbf{a}_{1}\cdot(\mathbf{a}_{2}\times \mathbf{a}_{3})},\quad \mathbf{b}_{3}=2\pi \frac{\mathbf{a}_{1}\times \mathbf{a}_{2}}{\mathbf{a}_{1}\cdot(\mathbf{a}_{2}\times \mathbf{a}_{3})}$$
### Brillouin zone
Just like how the choice of direct primitive cell is mostly arbitrary, so is the choice of reciprocal primitive cell. The most natural choice is to do the same thing as the direct lattice: construct a cell about a point as the region closest to that point. In direct space it is known as the [[Wigner-Seitz cell]], and in reciprocal space it is called the **[[Brillouin zone|first Brillouin zone]]**. Despite the different names, their definition is identical and use the same geometric construction. The difference in name is largely a historical question and a matter of convenience, since direct space and reciprocal space represent different things and it is useful to have different terminology for the two.