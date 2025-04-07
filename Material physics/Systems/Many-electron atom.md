The **many-electron atom** is a [[physical system]] modeling an [[atom]] with an arbitrary number of [[elettrone|electrons]] around and arbitrary [[Nucleo atomico|nucleus]]. It is an extension of the [[two electron atom]] and the [[hydrogen atom]]. The [[Hamiltonian]] of the system is
$$H=\sum_{i=1}^{N}\left[  - \frac{\hbar^{2}}{2m}\nabla ^{2}_{\mathbf{r}_{i}}- \frac{Ze^{2}}{4\pi \varepsilon_{0}r_{i}} \right]+\sum_{i>j} \frac{e^{2}}{4\pi \varepsilon_{0}r_{ij}} $$
where the sum over $i>j$ is indexed that way to avoid double-counting [[interazione elettromagnetica|electromagnetic interactions]] between electrons.
### Central field approximation
With two electrons, the perturbative approximation was rather poor and required a more accurate treatment (namely, the [[variational method]]). As you add more electrons, it becomes even worse. Our approach is to try and enforce a central symmetry and split that Hamiltonian into a central term and an "everything else" term, the latter of which is ideally much smaller. The basis of this is that the nucleus still acts as the central attractor of the system and that the repulsions have a central component. This model is called the **central field approximation** and was proposed by Hartree and Slater. It is based on an independent particle model where each electron moves in an effective [[potential]] which represents both the central potential and the *average* of the repulsions between an electron and all the others.

The effect of the repulsion is to *screen* the central attraction to the nucleus and because of this, the inter-electron interaction term must have a strong central component to it, which we can write as $\sum_{i}S(r_{i})$, where $S(r_{i})$ is the **screening**. As such, if we *only* consider this central component (and use [[atomic units]]), we can broadly approximate the system's effective potential as
$$V(r)=- \frac{Z}{r}+S(r)$$
We can begin our investigation by figuring out what happens at the extremes: really far and really close to the nucleus.

Say an electron $r_{i}$ is very far from the nucleus but not that far from the other electrons. Mathematically, this means $r_{ij}\simeq r_{i}$ and $1/r_{ij}\simeq1/r_{i}$. In this case, the electron moves in a potential that is approximately given by
$$V(r)=- \frac{Z}{r_{i}}+\sum_{i>j} \frac{1}{r_{i}} =- \frac{Z-N+1}{r_{i}}\tag{1}$$
which corresponds to the Coulomb potential of the nucleus, screened by all the other $N-1$ electrons. In a neutral atom, where $Z=N$, it becomes as simple as it gets
$$V(r)=- \frac{1}{r_{i}}\tag{2}$$

Say now our electron $r_{i}$ is very close to the nucleus. When this happens, the screening becomes less pronounced and the central attraction takes over. In this regime, $r_{ij}\simeq r_{j}$ and the potential is approximately
$$V(r)- \frac{Z}{r_{i}}+\left\langle  \sum_{i>j} \frac{1}{r_{j}}  \right\rangle=- \frac{Z}{r_{i}}+C \tag{3}$$
where $\langle  \rangle$ denotes an average over the $r_{j}$ distances of all the other $N-1$ electrons and $C$ is a constant.

These limits are qualitatively interesting, but they also provide boundary conditions for further, more refined potentials. Any and all effective potentials that we employ must satisfy $(1)$ for $r\to \infty$ (and $(2)$ for neutral atoms) and $(3)$ for $r\to0$. The issue now is figuring out what happens outside of the extremes, which is everything but easy.

It should be noted that a central potential is fundamentally incompatible with a complete description of the many-electron atom. This is because the nature of the electron repulsion is dependent on the dynamics of the system: position is undefined in quantum mechanics, but the charge distribution is, and the repulsion must of course be directly dependent on the geometry of this distribution, which changes over time. A central potential enforces a static spherical distribution, so even with a perfect search algorithm, there is no "exact" central potential. Because of this, this kind of solution is mostly useful in the ground state and the first few excited state; anything more and it starts to show cracks. Fortunately, even these few states are more than enough to capture the essence of the system and see much of the complex behavior of the many-electron atom.
#### The Hamiltonian
We thus split our Hamiltonian as $H=H_\text{c}+H_{r}$, where $c$ and $r$ read as "center" and "rest". 

...

#### Spin
We can reintroduce spin by multiplying the orbital [[funzione d'onda|wave function]] by the spin component of the wave function
$$u_{nlmm_{s}}(q)=u_{nlm}(\mathbf{r})\chi_{1/2,m_{s}}$$
Denoting $\alpha,\beta,\chi$ the sets of (spatial and spin) [[Numero quantico|quantum numbers]], the $N$-particle wave function is going to be the wave function that's [[Permutation operator|antisymmetric]] with respect to single particle exchange. It is given by the [[Slater determinant]]:
$$\Psi(q_{1},q_{2},\ldots,q_{n})=\frac{1}{\sqrt{ N! }}\begin{vmatrix}
u_{\alpha}(q_{1}) & u_{\beta}(q_{1}) & \ldots & u_{v}(q_{1}) \\
u_{\alpha}(q_{2}) & u_{\beta}(q_{2}) & \ldots & u_{v}(q_{2}) \\
\vdots \\
u_{\alpha}(q_{N}) & u_{\beta}(q_{N}) & \ldots & u_{v}(q_{N})
\end{vmatrix}$$
