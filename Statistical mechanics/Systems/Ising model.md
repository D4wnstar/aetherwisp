idk watch lesson from 10/11/2024

The [[Hamiltonian]] of the Ising model is
$$H=-J\sum_{\langle i,j \rangle}S_{i}S_{j}-h\sum_{i=1}^{N}S_{i}$$
$i$ denotes a position on a lattice. The [[potenziale|potential]] $-h\sum_{i=1}^{N}S_{i}$ is a so-called **single-body potential** because it does not interact between different bodies. $-J\sum_{\langle i,j \rangle}S_{i}S_{j}$ is a **two-body potential** because it causes inter-body interaction.
### Lattice gas
A **lattice gas** is a primitive model for a fluid (can also be used for, say, water, in lieu of molecular dynamics) and an early usage of the Ising model[^1]. It represents space as a grid where each cell can either contain a particle ($S_{i}=+1$) or not ($S_{i}=-1$). The Hamiltonian in this case becomes
$$H=-\phi \sum_{\langle i,j \rangle } \frac{1}{2}(1+S_{i}) \frac{1}{2}(1+S_{j})-\mu \sum_{i} \frac{1}{2}(1+S_{i})\equiv-J\sum_{\langle i,j \rangle }S_{i}S_{j}-h\sum_{i}S_{i}$$
### Binary alloy
In a **binary alloy**, each cell in the grid contains a particle, and each particle can be aligned in direction $A$ ($S_{i}=+1$) or $B$ ($S_{i}=-1$). The Hamiltonian is
$$H=\frac{1}{4}\sum_{\langle i,j \rangle }J_{AA}(1+S_{i})(1+S_{j})+ \frac{1}{4}\sum_{\langle i,j \rangle }J_{BB}(1+S_{i})(1+S_{j})+ \frac{1}{4}\sum_{\langle i,j \rangle }J_{AB}(1+S_{i})(1+S_{j})$$
The interaction is determined by how the particles want to align (for instance, in columns or rows of same alignment).
### Potts model
The **spin-1 Ising model** is an Ising model applied to [[spin]]-1 particles. It can be extend to an arbitrary spin $s$. The $S$ here can be $S_{i}=1,\ldots,q$ (TODO: Rewatch lesson from 13/11/2024). The Hamitonian for is
$$H=-J\sum_{\langle i,j \rangle }\delta_{S_{i},S_{j}}-h\sum_{i} \delta_{i,S_{i}}$$
There is a further extension called the **Potts model**, where the Hamiltonian is
$$H=-J\sum_{\langle i,j \rangle }\overline{S}_{i}\overline{S}_{j}$$
where
$$\overline{S}_{i}=(S_{i}^{(1)},\ldots,S_{i}^{(n)})\quad\text{with}\quad S_{i}^{(k)}\in \mathbb{R},\quad \sum_{k=1}^{n} (S_{i}^{(k)})^{2}=1$$
### XY model
idk
### Free energy and partition function
The [[partition function]] in the general form is
$$Q_{N}=Z=\sum_{\{ S_{i} \}}e^{-\beta H}$$
Consider a square lattice with $N$ cells where each cell can be $S_{i}=\pm 1$. The number of possible configurations goes like $2^{N}$. In order to find the partition function, we need to sum over every possible combination, which is to say
$$Q_{N}=\underbrace{ \sum_{S_{1}=\pm_{1} }\sum_{S_{2}\pm 2}\ldots\sum_{S_{N}\pm 1} }_{ N\text{ times} }e^{-\beta H(S_{1},\ldots,S_{N})}$$
Just to give a sense of scale, $N$ is usually in the order of the [[Avogadro number]], so $\sim 10^{23}$, which makes the number of possible combinations so large it becomes completely unreasonable to calculate any of this directly, even on the greatest supercomputer in the world. There are only two ways forward: an ingenious analytical solution through combinatorics, or an approximate method to simplify things. For the one dimensional case, there is actually a general solution by Ising himself from 1925. For the two dimensional case, there is a solution in the specific case $J\neq 0$ but $h=0$ by Onsager from 1944. For the three dimensional case, there is no known solution in any case. Thus, let's find some approximation.
#### Mean field
The **mean field approximation** is arguably one of the most common approximations in statistical mechanics. In it, we simply have $J=0$. The Hamiltonian therefore becomes
$$H=-h\sum_{i}S_{i}=\sum_{i}H_{i}$$
where $H_{i}=-hS_{i}$. In plain terms, we just ignore inter-particle interactions and split the solution in independent, single-body Hamiltonians. Thus, the partition function is
$$\begin{align}
Z&=\sum_{\{ S_{i} \}}e^{-\beta H}=\sum_{S_{1}\pm 1}\ldots\sum_{S_{N}=\pm 1}e^{\beta h(S_{1}+S_{2}+\ldots+S_{N})} \\
&=\left( \sum_{S_{1}\pm 1}e^{\beta hS_{1}} \right)\left( \sum_{S_{2}\pm 1}e^{\beta hS_{2}} \right)\ldots\left( \sum_{S_{N}\pm 1}e^{\beta hS_{N}} \right) \\
&=(2\cosh(\beta h))^{N}
\end{align}$$


[^1]: In fact, the original idea predates it and was later solved with the Ising model when that was developed.