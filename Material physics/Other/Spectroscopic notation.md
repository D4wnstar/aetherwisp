---
wiki-publish: true
---
**Spectroscopic notation** is a convention for denoting the values of [[Numero quantico|quantum numbers]], especially in the context of [[atom|atomic]] and [[Molecule|molecular]] quantum numbers.
### Atomic orbitals
Barring [[spin]], an [[atomic orbital]] is identified by the quantum numbers $n$, $l$ and $m$. This notation is used to represent the [[stato|state]] of an individual [[electron]] using the format
$$nl_{m}$$
- The principal quantum number $n$ is denoted with usual numbers, $n=1,2,3,\ldots$
- The azimuthal quantum number $l$ is denoted with a specific set of letters, as shown in the table below.
- The magnetic quantum number $m$ also uses numbers, $m=\ldots,-1,0,1,\ldots$. It is typically omitted for brevity since it often does not matter.

| Number | Letter |
| ------ | ------ |
| 0      | $s$    |
| 1      | $p$    |
| 2      | $d$    |
| 3      | $f$    |
| 4      | $g$    |
| 5      | $h$    |

Some examples are
- $(n,l,m)=(1,0,0)=1s_{0}$
- $(n,l,m)=(2,1,-1)=2p_{-1}$
- $(n,l,m)=(4,3,2)=4f_{2}$
### Overall atomic state
When an atom has two or more electrons, it's necessary to differentiate the atomic state from the electronic state. To do so, an extension to the notation is used to represent the overall state of the atom, which uses different quantum numbers. The format is
$$n^{2S+1}L_{J}$$
- $n$ is the principal quantum number of the most energetic electron (the outermost electron).
- $S$ is the total spin quantum number of the atom, given by $S=\sum_{i}m_{s,i}$. $2S+1$ is the spin degeneracy. Useful to easily differentiate between, for example, singlet and triplet states.
- $L$ is the total orbital angular momentum of the atom, given by $L=\sum_{i}m_{l,i}$. Like in atomic orbitals, it uses the same letters, but uppercase.
- $J$ is the total angular momentum of the atom. It is sometimes omitted if it is unnecessary. It is equal to $L+S$.

| Number | Letter |
| ------ | ------ |
| 0      | $S$    |
| 1      | $P$    |
| 2      | $D$    |
| 3      | $F$    |
| 4      | $G$    |
| 5      | $H$    |

Some examples are:
- The ground state helium atom has both electrons in $1s$, so the electron configuration is $1s^{2}$. The highest $n$ is $1$. The total spin has to be zero, since the only two electrons we have are in the same orbital, which means that their spins must be opposite. Both electrons have $l=0\equiv s$, so the total orbital momentum is also zero. Thus, with $n=1$, $S=0$, $L=0$, the overall atomic state is $1^{1}S_{0}$.
- The first excited state helium atom has one electron in $1s$ and one in $2s$. The electron configuration is $1s2s$. The highest $n$ is $2$. The total spin can be either $0$ or $1$, since the electrons are in different orbitals and there's no restriction on whether their spin is the same or opposite. The total orbital momentum is still zero because both electrons are still in $l=0$. Thus, with $n=0$, $S=0,1$ and $L=0$, we have two possible states: either $2^{1}S_{0}$ (singlet state) or $2^{3}S_{1}$ (triplet state).
