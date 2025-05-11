---
wiki-publish: true
---
The **Ising model** is a simplified model of [[ferromagnetism]] through statistical mechanics. It represents the total [[magnetization]] of a material by denoting each [[Atomo|atom]] as being either [[spin]] up or down, with nearby atoms possessing an interaction that tends to move them to the same spin. The total magnetization arises from the collective arrangement of nearby atoms in the same spin. The model also shows a [[phase transition]].

Consider a [[lattice]] of $N$ sites (i.e. atoms).  Each atom is given a discrete variable $S=\pm 1$ representing whether it is spin up or down. The set of all spins describes the [[stato|state]] of the [[Physical system|system]] and is denoted $\{ S_{i} \}_{i\in N}$. Adjacent atoms have an interaction $J\in \mathbb{R}$ and the system is subject to an external [[magnetic field]] $h$. The [[Hamiltonian]] of the Ising model is therefore
$$H=-J\sum_{\langle i,j \rangle}S_{i}S_{j}-h\sum_{i=1}^{N}S_{i}$$
where $\langle i,j \rangle$ denotes a sum over adjacent atoms. This is the simplest case, in which we have a constant interaction and a constant magnetic field. It possible for these to change for every site, in which case we'd have
$$H=-\sum_{\langle i,j \rangle}J_{ij}S_{i}S_{j}-\sum_{i=1}^{N}h_{i}S_{i}$$
The total magnetization of an Ising system is
$$M=\sum_{i=1}^{N} S_{i}$$
### Applications
The Ising model has been used as the basis of a number of physical descriptions.
#### Lattice gas
A **lattice gas** is a primitive model for a fluid (can also be used for, say, water, in lieu of molecular dynamics) and an early usage of the Ising model[^1]. It represents space as a grid where each cell can either contain a particle ($S_{i}=+1$) or not ($S_{i}=-1$). The Hamiltonian in this case becomes
$$H=-\phi \sum_{\langle i,j \rangle } \frac{1}{2}(1+S_{i}) \frac{1}{2}(1+S_{j})-\mu \sum_{i} \frac{1}{2}(1+S_{i})\equiv-J\sum_{\langle i,j \rangle }S_{i}S_{j}-h\sum_{i}S_{i}$$
#### Binary alloy
In a **binary alloy**, each cell in the grid contains a particle, and each particle can be aligned in direction $A$ ($S_{i}=+1$) or $B$ ($S_{i}=-1$). The Hamiltonian is
$$H=\frac{1}{4}\sum_{\langle i,j \rangle }J_{AA}(1+S_{i})(1+S_{j})+ \frac{1}{4}\sum_{\langle i,j \rangle }J_{BB}(1+S_{i})(1+S_{j})+ \frac{1}{4}\sum_{\langle i,j \rangle }J_{AB}(1+S_{i})(1+S_{j})$$
The interaction is determined by how the particles want to align (for instance, in columns or rows of same alignment).
#### Potts model
The **spin-1 Ising model** is an Ising model applied to [[spin]]-1 particles. It can be extend to an arbitrary spin $s$. The $S$ here can be $S_{i}=1,\ldots,q$ (TODO: Rewatch lesson from 13/11/2024). The Hamitonian for is
$$H=-J\sum_{\langle i,j \rangle }\delta_{S_{i},S_{j}}-h\sum_{i} \delta_{i,S_{i}}$$
There is a further extension called the **Potts model**, where the Hamiltonian is
$$H=-J\sum_{\langle i,j \rangle }\overline{S}_{i}\overline{S}_{j}$$
where
$$\overline{S}_{i}=(S_{i}^{(1)},\ldots,S_{i}^{(n)})\quad\text{with}\quad S_{i}^{(k)}\in \mathbb{R},\quad \sum_{k=1}^{n} (S_{i}^{(k)})^{2}=1$$
#### XY model
idk
### Partition function
An Ising model is typically treated as a [[canonical ensemble]]. The [[Partition function|canonical partition function]] is 
$$Q_{N}=\sum_{\{ S_{i} \}}e^{-\beta H}$$
Consider a square lattice with $N$ cells where each cell can be $S_{i}=\pm 1$. The number of possible configurations goes like $2^{N}$. In order to find the partition function, we need to sum over every possible combination, which is to say
$$Q_{N}=\underbrace{ \sum_{S_{1}=\pm_{1} }\sum_{S_{2}\pm 2}\ldots\sum_{S_{N}\pm 1} }_{ N\text{ times} }e^{-\beta H(S_{1},\ldots,S_{N})}$$
Just to give a sense of scale, $N$ is usually in the order of the [[Avogadro number]], so $\sim 10^{23}$, which makes the number of possible combinations so large it becomes completely unreasonable to calculate any of this directly, even on the greatest supercomputer in the world. Realistically speaking, there's only two ways forward: an ingenious analytical solution through combinatorics, or an approximate method to simplify things. For the one dimensional case, there is a general solution by Ising himself from 1925. For the two dimensional case, there is a solution for interacting atoms ($J\neq 0$) but under no external field ($h=0$) by Onsager from 1944. For the three dimensional case, there is no known analytical solution. Thus, let's find some approximations.
#### No interaction
If we take the particles to be non-interacting, we simply have $J=0$. The Hamiltonian therefore becomes
$$H=-h\sum_{i}S_{i}=\sum_{i}H_{i}$$
where $H_{i}=-hS_{i}$. In plain terms, we just ignore inter-particle interactions and split the solution in independent, single-body Hamiltonians. Thus, the partition function is
$$\begin{align}
Q_{N}&=\sum_{\{ S_{i} \}}e^{-\beta H}=\sum_{S_{1}=\pm 1}\ldots\sum_{S_{N}=\pm 1}e^{\beta h(S_{1}+S_{2}+\ldots+S_{N})} \\
&=\left( \sum_{S_{1}\pm 1}e^{\beta hS_{1}} \right)\left( \sum_{S_{2}\pm 1}e^{\beta hS_{2}} \right)\ldots\left( \sum_{S_{N}\pm 1}e^{\beta hS_{N}} \right) \\
&=(2\cosh(\beta h))^{N}
\end{align}$$
#### Mean field approximation
The **mean field approximation** is arguably one of the most common approximations in statistical mechanics. In it, we do not ignore the interactions themselves ($J\neq 0$), but we do ignore the cross terms caused by the interaction. To see this, consider the quantity
$$S_{i}=\langle S_{i} \rangle +\underbrace{ S_{i}-\langle S_{i} \rangle }_{ -\delta S_{i} }=\langle S_{i} \rangle -\delta S_{i} =m-\delta S_{i}$$
where we renamed $\langle S_{i} \rangle=m$ as the average [[magnetic dipole moment]]. If we substitute this in the Hamiltonian, we get
$$H=-J\sum_{\langle i,j \rangle }(m -\delta S_{i})(m -\delta S_{j} )-h\sum_{i=1}^{N} S_{i}$$
We now have cross-terms in the first sum. The essence of the interaction is more or less hidden within the term $\delta S_{i}\delta S_{j}$. It also contains all the complexity of the system, so our best bet to solving it is to just pretend it doesn't exist: $\delta S_{i}\delta S_{j}=0$. This is the mathematical statement of the mean field approximation.

This leaves only independent terms for each lattice point, which lead to independent Hamiltonians and a solution very similar to the "no interaction" case above, just with some additional terms due to the interaction. If we actually compute the product step-by-step for a generic $d$-dimensional lattice we find
$$\begin{align}
H&\simeq-Jm^{2}N_{B}-Jm\sum_{\langle i,j \rangle }(\delta S_{i}+\delta S_{j})-h\sum_{i=1}^{N} S_{i} \\
&=-Jm^{2}N_{B}-Jmz\sum_{i=1}^{N} \delta S_{i}-h\sum_{i=1}^{N} S_{i} \\
&=-Jm^{2}N_{B}-Jmz\sum_{i=1}^{N} (S_{i}-m)-h\sum_{i=1}^{N} S_{i} \\
&=-Jm^{2}N_{B}+Jmz\sum_{i=1}^{N} m-\sum_{i=1}^{N}(Jmz+h) S_{i} \\
&=\text{const.}+\sum_{i=1}^{N} H_{i}
\end{align}$$
where we set $H_{i}=(Jmz+h)S_{i}$ and the rest was hidden away in a generic constant. $N_{B}$ is the number of bonds, the total number of "connections" there are between sites. The term $z$ is the [[coordination number]], the number of other sites each site interacts with. For example, in a hypercubic lattice it is twice the dimension, $z=2d$. Knowing the Hamiltonians, we can calculate the [[partition function]]:
$$Z=\sum_{S=\pm 1} e^{-\beta H_{i}}=2\cosh(\beta(Jmz+h)) $$
and then the average spin:
$$m=\langle S_{i} \rangle =\frac{1}{Z}\sum_{S=\pm 1}S_{i}e^{-\beta H_{i}}=\frac{2\sinh(\beta(Jmz+h))}{2\cosh(\beta(Jmz+h))}=\tanh(\beta(Jmz+h))$$
Specifically, we get
$$\boxed{m=\tanh(H_{i})=\tanh(\beta(Jmz+h))}$$
Note that this is a transcendental equation, so the best we can do is show it numerically, graphically or with an approximation.

![[Plot Ising model magnetic moment|center]]

This plot is the phase diagram of the model. The diagonal line is the $m=0$ case. The phase transition occurs when this line is crossed. Proving that a phase transition occurs just means proving that there are temperature for which non-trivial $m=0$ solutions are possible (that is, $m=0$ outside of the origin). These solution can be found using, for instance, the hyperbolic tangent [[Serie di Taylor|Taylor series]] $\tanh x=x-x^{3}/3+\ldots$.

When the temperature is $T>T_{C}$, the only solution is at the origin. When $T<T_{C}$, we have three solutions: one at the origin and two somewhere else, shown in the figure as red crosses. This is an important fact: the magnetization *must* have two solutions for it to make sense, as it must be symmetrical. A phase transition is fundamentally the [[symmetry break|breaking of a symmetry]].
### Quantum model
The Ising model can be rewritten in quantum mechanical terms. The classical Ising Hamiltonian is
$$H=-J\sum_{\langle i,j \rangle }S_{i}S_{j}-h\sum_{i}S_{i},\quad S_{i}=\pm 1$$
This is classical in the sense that the $S_{i}$ are just numbers, bits. They naturally [[Commutatore|commute]] with each other. Some things are reminiscent of quantum mechanics, such as the fact that there are discrete energy levels for each [[Stato|microstate]]. But they are not states in the quantum sense, they're just due to the kind of description of the system we are using (which employs a set of discrete quantities). Each element of the system can classically be either *up* or *down*, $\uparrow$ or $\downarrow$, true or false, 1 or -1. When we make the quantum leap, these become individual quantum states $\ket{S}$, which are no longer discrete: they are linear combinations in $\mathbb{C}^{2}$ of the two [[Equazione agli autovalori|eigenstates]] $\ket{\uparrow}$ and $\ket{\downarrow}$, such that
$$\ket{S} =\alpha \ket{\uparrow} +\beta \ket{\downarrow} $$
In other words, we went from bits to [[qubit|qubits]]. The $S$ values become [[Osservabile|observables]] and are described by [[Operatore autoaggiunto|self-adjoint operators]] $\hat{S}_{i}$. In particular, since these are (two-dimensional) spin states, they are described by the [[Matrici di Pauli|Pauli matrices]]:
$$S_{i}\quad\to \quad \hat{S}_{i}=\sigma_{z}^{i}=\begin{pmatrix}
1 & 0 \\
0 & -1
\end{pmatrix}$$
(yes, it's missing an $\hbar/2$, it's just to prove the point). If we make this substitution in the Hamiltonian, we get the quantum Ising model Hamiltonian
$$\boxed{\hat{H}=-J\sum_{\langle i,j \rangle }\sigma_{z}^{i}\sigma_{z}^{j}-h\sum_{i}\sigma_{z}^{i}-h_{T}\sum \sigma_{x}^{i}}$$
The addition of the last terms is due to the non-commutativity of $\sigma_{x}$ and $\sigma_{z}$. In fact, we have
$$[\sigma_{z}^{1}\sigma_{z}^{2},\sigma_{x}^{1}]\neq 0$$
though still $[\sigma_{z}^{i},\sigma_{z}^{j}]=0$. The matrix form of the quantum Hamiltonian is $2^{N}\times 2^{N}$ dimensional. For an example, consider the two dimensional case. We only have two atoms, with spins $\hat{\sigma}_{z}^{1}$ and $\hat{\sigma}_{z}^{2}$. These operators are the [[Prodotto tensoriale|tensor product]] between $\hat{\sigma}_{z}$ and the unit operator, so
$$\hat{\sigma}_{z}^{1}=\hat{\sigma}_{z}\otimes \hat{\mathbf{1}}=\begin{pmatrix}
1 & 0 \\
0 & -1
\end{pmatrix}\otimes \begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}
=\begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & -1 & 0 \\
0 & 0 & 0 & -1
\end{pmatrix}$$
The same applies to $\hat{\sigma}_{z}^{2}=\hat{\mathbf{1}}\otimes \hat{\sigma}_{z}$. If we add more elements (increasing $N$) we get $N$ tensor products in sequence. Since we are multiplying 2-dimensional matrices, each product multiplies the dimensions by two, which means that the $N$-th product $\hat{\mathbf{1}}\otimes \hat{\mathbf{1}}\otimes\ldots\otimes \hat{\sigma}_{z}\otimes\ldots\otimes \hat{\mathbf{1}}$ is going to be $2^{N}\times 2^{N}$ dimensional. This is a sensible result: after all, the classical case also has $2^{N}$ possible combinations.

[^1]: In fact, the original idea predates it and was later solved with the Ising model when that was developed.