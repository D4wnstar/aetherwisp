---
wiki-publish: true
---
The **Helmholtz equation** is a second-order [[elliptic partial differential equation]]
$$\nabla ^{2}\psi=-k^{2}\psi$$
for some constant $k$. It is a special case of [[Poisson's equation]] where $f=-k^{2}\psi$. It is also the [[eigenvalue equation]] of the [[Laplacian]] operator, of eigenfunction $\psi$ and eigenvalue $-k^{2}$.
### As a wave equation
This equation appears quite commonly in the study of [[wave|waves]], as it is a special case of the [[wave equation]] when the wavefunction is separable between time and space. In fact, consider the wave equation
$$\left( \nabla ^{2}- \frac{1}{v^{2}}\frac{ \partial ^{2} }{ \partial t^{2} } \right)u(\mathbf{r},t)=0$$
for a wavefunction $u(\mathbf{r},t)$. Assume that $u$ is [[separation of variables|separable]] as
$$u(\mathbf{r},t)=A(\mathbf{r})B(t)$$
Substitute this above to get
$$\left( \nabla ^{2}- \frac{1}{v^{2}}\frac{ \partial ^{2} }{ \partial t^{2} }  \right)A(\mathbf{r})B(t)=0\quad\Rightarrow \quad \frac{\nabla^{2}A(\mathbf{r})}{A(\mathbf{r})}=\frac{1}{B(t)v^{2}}\frac{ \partial ^{2}B(t) }{ \partial t^{2} } $$
We now employ the common technique of separation of variables: both sides of the equality are of course equal to each other, but they depend on different variables. It makes no sense that varying, say, $\mathbf{r}$ would also vary the right-hand side, which is only dependent on $t$. The converse also applies. Thus, the two sides must be *constant*. Let's call this constant $-k^{2}$ for reasons that will be apparent later[^1]. In the meantime, you can already start to read $k$ as the [[wavenumber]].

We are now left with *two* equations in *one* variable each:
$$\frac{\nabla^{2}A(\mathbf{r})}{A(\mathbf{r})}=-k^{2},\qquad \frac{1}{B(t)v^{2}}\frac{ \partial ^{2}B(t) }{ \partial t^{2} } =-k^{2}$$
The equation in $A$ rearranges to
$$\boxed{\nabla^{2}A(\mathbf{r})=-k^{2}A(\mathbf{r})}$$
This is the **Helmholtz equation**. Evidently, it must be the equation for the spatial part of a wavefunction $u(\mathbf{r},t)$. But don't stop here, see the other way around too: *the eigenfunctions of the Laplacian are always the spatial part of some wavefunction*. This very interesting characterization helps to understand why the Laplacian appears so incredibly often when it comes to wave phenomena; it basically "contains" wavefunctions, so *of course* it would appear all the time.

The second equation in $B$ to
$$\frac{ \partial ^{2}B(t) }{ \partial t^{2} } =-k^{2}v^{2}B(t)$$
If we define $\omega\equiv kv$ and use dot notation for time derivatives we meet an old friend:
$$\boxed{\ddot{B}(t)=-\omega ^{2}B(t)}$$
The temporal part of a spherical wave must therefore be a [[harmonic oscillator]]! This is why we made the weird choice of picking $-k^{2}$ as a constant in the first place. In fact, the Helmholtz equation itself is quite reminiscent of a harmonic oscillator, just instead of the time derivative we have the Laplacian.

Thus, in order to fully determine the nature of a spherical wave, one must solve a Helmholtz equation for space and a harmonic oscillator for time. By the way, if the wave is [[Frequency|monochromatic]], $\omega$ is its [[Frequency|angular frequency]].

[^1]: The shape of the constant is completely arbitrary. We choose $-k^{2}$ only because it makes the solutions more meaningful, but we could've just as well called it $k$ or $k^{3}+83k$.
