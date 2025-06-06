---
wiki-publish: true
aliases:
  - symmetric state
  - antisymmetric state
---
The **permutation operator** $P_{ij}$ is an [[operatore|operator]] that permutes the variables $q_{i}$ and $q_{j}$. It [[Commutator|commutes]] with the [[Hamiltonian]]: $[P_{ij},H]=0$. For some [[funzione d'onda|wave function]] $\psi(q_{1},\ldots,q_{N})$ of $N$ [[generalized coordinates]], the permutation operator acts on it as
$$P_{ij}\psi(q_{1},\ldots,q_{i},\ldots,q_{j},\ldots,q_{N})=\psi(q_{1},\ldots,q_{j},\ldots,q_{i},\ldots,q_{N})$$
The is a [[Operatore unitario|unitary operator]] since $P_{ij}^{2}=\hat{\mathbf{1}}$ and hence its [[Equazione agli autovalori|eigenvalues]] are $\epsilon=\pm1$. $\epsilon=1$ represents a symmetry, $\epsilon=-1$ an antisymmetry.

The operator can be generalized to make multiple swaps in one application. In other words, it does a [[permutation]] of the coordinates. We define the operator as $P:q_{n}\to q_{P_{n}}$, where $P_{n}$ represents the new index after the permutation. The application is the same:
$$P\psi(q_{1},\ldots,q_{N})=\psi(q_{P_{1}},\ldots,q_{P_{N}})$$
This operator is even if the number of swaps is even, and odd otherwise.

A state $\psi$ for which the operator $P_{ij}$ is even is said to be **symmetric** (under permutation) and a state for which it is odd is said to be **antisymmetric** (under permutation). In quantum physics, symmetric states are associated with [[boson|bosons]] and antisymmetric ones with [[Fermion|fermions]] (this fact is known as the **symmetrization postulate**). These constraints the explain quantum statistics ([[Bose-Einstein distribution]] and [[Fermi-Dirac distribution]]) and are a consequence of the [[Identical particles|indistinguishabilty of particles]]. (Anti)symmetry remains unchanged under superposition, which means that superimposing multiple (anti)symmetric states leads to an (anti)symmetric state.