---
wiki-publish: true
aliases:
  - separation energy
---
The **binding energy** of a [[physical system]] is the [[energy]] required to remove one of its components. The larger the binding energy is, the more energy needs to be transferred to break a piece off the system, hence the name. It is found in many fields of physics in different forms.
## Nuclear separation energy
In nuclear physics, the term **separation energy** is preferred over binding energy when referring to the removal of [[Nucleon|nucleons]] from the [[Atomic nucleus|nucleus]].

It is defined as the difference between the mass of the individual constituents of the system and the mass of the system, multiplied by $c^{2}$. The difference between the mass of the bound system and its constituents is also called the **mass defect**. For a nucleus, it is the mass difference between the nucleus $^{A}_{Z}X_{N}$ and its constituent $Z$ [[proton|protons]] and $N$ [[neutron|neutrons]].

It is convenient to express the separation energy in terms of [[atom|atomic]] [[mass|masses]], as they are experimentally measurable with great precision ($\sim10^{-6}$) using [[mass spectrometry]]. Then we have
$$B(Z,A)=[Zm(^{1}H)+Nm_{n}-m(A,Z)]c^{2}$$
where
* $m_{n}$ is the mass of the [[neutron]].
* $m(^{1}H)=m_{e}+m_{p}$, with $m_{e}$ and $m_{p}$ being the masses of the [[Electron]] and the [[proton]].
* $A$, $N$ and $Z$ are the [[Atom|atomic mass number]], [[Atom|neutron number]] and [[Atom|atomic number]].
* $c$ is the [[speed of light]].
Essentially, this formula measures the difference between the mass of the atom and the mass the system would have if it were composed of separate hydrogen atoms and neutrons.

![[Diagram Helium binding energy|100%]]

### Parameterization
For an atomic nucleus, the binding energy is the difference between the mass of its protons and neutrons and the energy that binds them together. It is more convenient to write $B$ as
$$B(Z,A)=[Zm_{p}+Nm_{n}-(M(^{A}X)-Zm_{e})]c^{2}=\ldots$$
Grouping the $Z$ masses of protons and electrons into $Z$ hydrogen atoms, I get
$$\ldots=[ZM(^{1}H)+Nm_{n}-m(^{A}X)]c^{2}$$
where the mass of the nucleus $m(^{A}X)$ remains. Knowing the mass defect $\Delta = (m-A)c^{2}$, you can invert this relation to find the atomic mass.

The **neutron separation energy** $S_{n}$ is the energy required to remove a neutron from a nucleus, i.e., the binding energy difference between $_{Z}^{A}X_{N}$ and $_{Z}^{A-1}X_{N-1}$:
$$S_{n}=B(_{Z}^{A}X_{N})-B(_{Z}^{A-1}X_{N-1})=[m(_{Z}^{A-1}X_{N-1})-m(_{Z}^{A}X_{N})+m_{n}]c^{2}$$
The **proton separation energy** $S_{p}$ is defined analogously:
$$S_{p}=B(_{Z}^{A}X_{N})-B(_{Z-1}^{A-1}X_{N})=[m(_{Z-1}^{A-1}X_{N})-m(_{Z}^{A}X_{N})+m(^{1}H)]c^{2}$$

The binding energy of a nucleus depends on its atomic mass number $A$. One might expect the ratio of binding energy to the number of nucleons to be constant, but this is not the case.

![[Plot Separation energy per nucleon|80%|center]]

$B$ increases sharply for the first few atoms (up to $A\simeq20$), after which it begins to flatten out and decline with a slight slope. The vast majority of nuclei reside in a relatively narrow band, ranging from 7.2 to 8.8 MeV/nucleon ($8.0\pm0.8$ MeV/nucleon). The only elements not included in this band are the very light ones, with $A<10$, such as hydrogen and helium. The peak of energy per nucleon is at $A\sim60$, where the nuclei are evidently particularly bound.

This plot gives us information on which process is energetically viable to release energy:
1. For $A\lesssim 60$, it is more efficient to combine nuclei together through [[nuclear fusion]].
2. For $A\gtrsim60$, it is more efficient to break nuclei to create smaller ones through [[spontaneous fission]].

The breaking point of these processes is around $A\sim60$. For example, nuclear fusion cannot create nuclei heavier than iron ($A=56$) without external energy input.