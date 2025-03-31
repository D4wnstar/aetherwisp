The **two electron atom** is a [[physical system]] modeling an [[atom]] with two [[elettrone|electron]]. It is a generalization of the [[Hydrogen atom|hydrogenoid atom]]. The key challenge of the system is the [[Identical particles|indistinguishability]] of electrons. The [[Hamiltonian]] of the system is
$$\hat{H}=- \frac{\hbar^{2}}{2m}\nabla ^{2}_{r_{1}}- \frac{Ze^{2}}{4\pi \varepsilon_{0}r_{1}}- \frac{\hbar^{2}}{2m}\nabla ^{2}_{r_{2}}- \frac{Ze^{2}}{4\pi \varepsilon_{0}r_{2}}+ \frac{e^{2}}{4\pi \varepsilon_{0}r_{12}}$$

![[Diagram Two electrom atom|50%]]

The solved [[Equazione agli autovalori|eigenfunction]] (in [[Rappresentazioni dello stato|position representation]]) will be of the form $\Psi\equiv \Psi(q_{1},q_{2})$, where $q_{1}$ and $q_{2}$ are the coordinates of the electrons. Electrons are [[spin]] $1/2$ [[Fermion|fermions]] and so $\Psi$ must be an [[Permutation operator|antisymmetric state]]: $\Psi(q_{1},q_{2})=-\Psi(q_{2},q_{1})$. Since $\hat{H}$ does not directly depend on spin, we can factor out the spin and leave a coordinate-only and spin-only [[Funzione d'onda|wave function]]:
$$\Psi(q_{1},q_{2})=\psi (\mathbf{r}_{1},\mathbf{r}_{2})\chi(1,2)$$
The spin wave functions $\chi(1,2)$ can be constructed from the more general $\chi_{1/2,m_{s}}(1)$ and $\chi_{1/2,m_{s}}(2)$. We denote $\mathbf{S}_{1}$ and $\mathbf{S}_{2}$ the spin operators of the electrons and by $(S_{1})_{z}$ and $(S_{2})_{z}$ their $z$ components. We denote the basic spin functions of the electrons $\alpha(1)$, $\beta(1)$, $\alpha(2)$ and $\beta(2)$. $\mathbf{S}_{1}$ only acts on $\alpha(1)$ and $\beta(1)$, whereas $\mathbf{S}_{2}$ only acts on $\alpha(2)$ and $\beta(2)$. In turn, this means that $\mathbf{S}_{1}$ and $\mathbf{S}_{2}$ [[Commutatore|commute]].

The total spin is $\mathbf{S}=\mathbf{S}_{1}+\mathbf{S}_{2}$ and the total $z$ component is $S_{z}=(S_{1})_{z}+(S_{2})_{z}$. The square of the total is
$$\mathbf{S}^{2}=\mathbf{S}_{1}^{2}+\mathbf{S}_{2}^{2}+2\mathbf{S}_{1}\cdot \mathbf{S}_{2}=\frac{3}{2}+2\mathbf{S}_{1}\cdot \mathbf{S}_{2}$$
since $\mathbf{S}_{1}^{2}=\mathbf{S}_{2}^{2}=3/4$. Since the interaction between electrons is purely [[Interazione elettromagnetica|electromagnetic]], it is independent of spin. As such, each electron's spin is simply either up $(\uparrow)$ or down $(\downarrow)$ without reference to the other, which leads to four distinct spin states:
$$\begin{align}
\chi_{1}(1,2)&=\alpha(1)\alpha(2)&\uparrow\uparrow \\
\chi_{2}(1,2)&=\alpha(1)\beta(2)&\uparrow\downarrow \\
\chi_{3}(1,2)&=\beta(1)\alpha(2)&\downarrow\uparrow \\
\chi_{4}(1,2)&=\beta(1)\beta(2)&\downarrow\downarrow
\end{align}$$
Applying the $z$ spin operator to $\chi_{1}$ leads to
$$\begin{align}
S_{z}\chi_{1}(1,2)&=[(S_{1})_{z}+(S_{2})_{z}]\alpha(1)\alpha(2) \\
&=[(S_{1})_{z}\alpha(1)]\alpha(2)+\alpha(1)[(S_{2})_{z}\alpha(2)] \\
&=\frac{1}{2}\alpha(1)\alpha(2)+ \frac{1}{2}\alpha(1)\alpha(2) \\
&=\alpha(1)\alpha(2) \\
&=\chi_{1}(1,2)
\end{align}$$
Clearly, the total spin over $z$ in the $\chi_{1}$ spin state is $1$ (in $\hbar$ units). More generally, we have
$$S_{z}\chi=M_{S}\chi_{}$$
Here $M_{S}=1$.