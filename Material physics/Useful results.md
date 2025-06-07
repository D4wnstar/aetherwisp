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
**Slater determinnat**
$$\Psi_{C}(q_{1},q_{2},\ldots,q_{n})=\frac{1}{\sqrt{ N! }}\begin{vmatrix}
u_{\alpha}(q_{1}) & u_{\beta}(q_{1}) & \ldots & u_{v}(q_{1}) \\
u_{\alpha}(q_{2}) & u_{\beta}(q_{2}) & \ldots & u_{v}(q_{2}) \\
\vdots \\
u_{\alpha}(q_{N}) & u_{\beta}(q_{N}) & \ldots & u_{v}(q_{N})
\end{vmatrix}$$
where $u$ are single-electron eigenfunctions, $\boldsymbol{\alpha}..,\nu$ are sets of quantum numbers $(n,l,m,m_{s})$, $N$ is number of electrons.
**Correzioni relativistiche**
$$H_{1}=\sum_{i>j} \frac{e^{2}}{4\pi \varepsilon_{0}r_{ij}}-\sum_{i=1}^{N} V_{C}(r_{i}),\quad H_{2}\equiv \sum_{i}\xi(\mathbf{r}_{i})\mathbf{L}_{i}\cdot \mathbf{S}_{i}\quad \text{where }\xi(\mathbf{r}_{i})=\frac{1}{2m^{2}c^{2}} \frac{1}{r_{i}} \frac{dV(r_{i})}{dr_{i}}$$
**L-S coupling**
Only when $H_{1}\gg H_{2}$ (small/medium $Z$). Uses term notation ($^{2S+1}L$).
**j-j coupling**
Only when $H_{2}\gg H_{1}$ (high $Z$). Splits energy levels, which now depend on $j=l+s$ as $E_{nlj}$ with degeneracy $2j+1$.
### Hund's rules
**Hund's rules** are a set of rules that explain how [[electron|electrons]] organize around an [[atom]]. They were originally found empirically and then developed theoretically later on.
1. Complete [[electron shell model|electron shells]] have $L=S=0$. The values of $L$ and $S$ are determined exclusively by the incomplete shells.
2. Equivalent electrons (electrons with the same $l$) are arranged as to maximize $S$. States with higher multiplicity have lower [[energy|energies]].
3. Electrons are arranged as to maximize $m_{L}=\sum m_{l}$.
4. In multiplets with subshells that are less than half filled, the term with *lowest* $j$ has the lowest energy. In mutliplets with subshells that are more than half filled, the term with *highest* $j$ has the lowest energy.