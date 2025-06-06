---
wiki-publish: true
---
### Two-electron atom
**Hamiltonian**
$$\hat{H}=\underbrace{ - \frac{\hbar^{2}}{2m}\nabla ^{2}_{r_{1}}- \frac{Ze^{2}}{4\pi \varepsilon_{0}r_{1}} }_{ \text{Electron 1} }\underbrace{ - \frac{\hbar^{2}}{2m}\nabla ^{2}_{r_{2}}- \frac{Ze^{2}}{4\pi \varepsilon_{0}r_{2}} }_{ \text{Electron 2} }+ \underbrace{ \frac{e^{2}}{4\pi \varepsilon_{0}r_{12}} }_{ e-e\text{ interaction} }$$
**Singlet state** (antisymmetric)
$$\chi_{0,0}=\frac{1}{\sqrt{ 2 }}[\alpha(1)\beta(2)-\alpha(2)\beta(1)]$$
**Triplet states** (all symmetric)
$$\begin{align}
\chi_{1,1}&=\alpha(1)\alpha(2) \\
\chi_{1,0}&=\frac{1}{\sqrt{ 2 }}[\alpha(1)\beta(2)+\alpha(2)\beta(1)] \\
\chi_{1,-1}&=\beta(1)\beta(2)
\end{align}$$
- **Parastates** are wavefunctions where the spin component is antisymmetric (spin singlet) and the spatial component is symmetric. In independent electron model: $\Psi _\text{para}(q_{1},q_{2})=A_{+}\psi_{+}^{0}(\mathbf{r}_{1},\mathbf{r}_{2})\chi_{0,0}(1,2)$.
- **Orthostates** are wavefunctions where the spin component is symmetric (spin triplet) and the spatial component is antisymmetric. In independent electron model: $\Psi _\text{ortho}(q_{1},q_{2})=A_{-}\psi_{-}^{0}(\mathbf{r}_{1},\mathbf{r}_{2})\sum_{m_{S}}\chi_{1,m_{S}}(1,2)d_{m_{S}}$.-

**Energy eigenvalues in independent particle model** (same for both para and ortho)
$$E_{n_1, n_2} = - \frac{mZ^{2}}{2\hbar^{2}} \frac{ e^{4} }{(4 \pi \epsilon_{0})^{2}} \left( \frac{1}{n_{1}^{2}} + \frac{1}{n_{2}^{2}} \right)$$
### Many-electron atom
**Hamiltonian**
$$H=\sum_{i=1}^{N}\underbrace{ \left[  - \frac{\hbar^{2}}{2m}\nabla ^{2}_{\mathbf{r}_{i}}- \frac{Ze^{2}}{4\pi \varepsilon_{0}r_{i}} \right] }_{ \text{Individual electrons} }+\sum_{i>j} \underbrace{ \frac{e^{2}}{4\pi \varepsilon_{0}r_{ij}} }_{ e-e\text{ interaction} } $$
