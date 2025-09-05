---
wiki-publish: true
aliases:
  - alpha particle
---
**Alpha decay** is a mode of [[Nuclear decay|decay]] in which a [[Atomic nucleus|nucleus]] emits an **alpha particle**, which is another name for the helium-4 nucleus $\ce{_{2}^{4}He_{2}}$. The alpha particle is a proper nucleus, comprised of two [[proton|protons]] and two [[neutron|neutrons]], which is very tightly [[Binding energy|bound]] due to being [[Magic number|doubly magic]]. As such, alpha decay results in a considerable amount of energy being removed from the decaying nucleus, usually in the order of 4 to 9 [[Electronvolt|MeV]].

The nuclear process is
$$\ce{_{Z}^{A}X_{N}}\ \rightarrow\ \ce{_{Z-2}^{A-4}X'_{N-2}}+\alpha$$
where $\ce{X}$ and $\ce{X}'$ are the initial and final [[Nuclide|nuclides]] and $\alpha$ is the $\ce{^{4}_{2}He_{2}}$ alpha particle. The daughter nucleus $\ce{X}'$ is missing two protons and two neutrons, which are ejected through the alpha particle. As such, alpha decay is a type of [[cluster decay]].

The alpha decay is governed by a mixture of the [[strong interaction]] and [[electromagnetism]].

An example alpha decay is for radium-226:
$$\ce{_{88}^{226}Ra_{138}}\ \rightarrow\ \ce{_{86}^{222}Rn_{136}}+\ \ce{_{2}^{4}He_{2}}$$
The [[half-life]] of this decay is about 1600 years and the [[kinetic energy]] of the alpha particle is about 4.8 MeV.
## Mechanism  
Individual protons and neutrons have binding energies around 8 MeV, so they cannot escape unless special conditions are met. Emission of a *bound* cluster of nucleons as a $^{4}\text{He}$ nucleus can, however, be energetically favoured.

We study the [[Potential]] energy $V(r)$ of an α-particle at distance $r$ from the nucleus:

![[Alpha-decay potential|80%|center]]

At short range the strong force dominates, creating a deep potential well $-V_{0}$.  
At large range the α-particle feels Coulomb repulsion from the protons, shown as $V_{C}$.  
$Z$ is the atomic number of the parent nucleus, $Z-2$ that of the daughter.

- $Q$ is the disintegration energy.  
- For $r<a$ the strong interaction produces a potential well; the only way for the α-particle to leave (or enter, as in [[spontaneous fission]]) is by [[quantum tunnelling]].  
- For $a<r<b$ a potential barrier appears because the potential energy exceeds the available energy $Q$; the α-particle is classically forbidden here.  
- For $r>b$ the particle is outside the barrier.

The **disintegration constant** $\lambda$ for an α-emitter is

$$\lambda=fP,\qquad f\sim\frac{v}{a}$$

where $f$ is the frequency with which the α-particle hits the barrier, $P$ the tunnelling probability, and $v$ the α-velocity at the barrier.

The Coulomb barrier height at $r=a$ is

$$C=\frac{1}{4\pi\epsilon_{0}}\frac{2(Z-2)e^{2}}{a}$$

for an α-particle of charge $2e$ and a daughter nucleus of charge $(Z-2)e$.  
The barrier height ranges from $C-Q$ at $r=a$ to 0 at $r=b$; we take the average $\frac{1}{2}(C-Q)$ and mean width $d=\frac{1}{2}(b-a)$.

To understand the phenomenon we solve the one-dimensional [[Schrödinger equation]] for a particle encountering a potential barrier $V(x)$. For eigenstate $\psi$:

$$\frac{\hbar^{2}}{2m}\frac{d^{2}\psi(x)}{dx^{2}}+V(x)\psi(x)=E\psi(x).$$

With the barrier we have three regions:

- $V(x)=0$, $x<0$: $\psi_{1}(x)=Ae^{ik_{1}x}+Be^{-ik_{1}x}$  
- $V(x)=V_{0}$, $0\le x\le a$: $\psi_{2}(x)=Ce^{k_{2}x}+De^{-k_{2}x}$  
- $V(x)=0$, $x>a$: $\psi_{3}(x)=Ee^{ik_{3}x}+Fe^{-ik_{3}x}$  

with

$$k_{1}=k_{3}=\sqrt{\frac{2mE}{\hbar^{2}}},\qquad k_{2}=\sqrt{\frac{2m(V_{0}-E)}{\hbar^{2}}}.$$

The transmission probability is

$$P=\frac{j_{\text{transmitted}}}{j_{\text{incident}}}=\frac{1}{1+\frac{1}{4}\frac{V_{0}^{2}}{E(V_{0}-E)}\sinh^{2}(k_{2}a)}.$$

For a nucleus we identify

$$k_{2}=\sqrt{\frac{2m}{\hbar^{2}}\frac{1}{2}(C-Q)}.$$

For a heavy nucleus ($Z=90$, $a=7.5$ fm) $C\simeq34$ MeV; using

$$b=\frac{1}{4\pi\epsilon_{0}}\frac{zZ'e^{2}}{Q}$$

gives the exit radius. With $Q\sim6$ MeV, $b\sim42$ fm. Both $b$ and $P$ are extremely sensitive to $Q$; tiny changes in $Q$ can shift half-lives by orders of magnitude.

## Energy conservation  
If the parent nucleus $X$ is at rest, the initial energy is $m_{X}c^{2}$. The final state consists of $X'$ and $\alpha$, both moving to conserve linear momentum. The final energy is

$$m_{X'}c^{2}+T_{X'}+m_{\alpha}c^{2}+T_{\alpha}.$$

Energy conservation gives

$$m_{X}c^{2}=m_{X'}c^{2}+T_{X'}+m_{\alpha}c^{2}+T_{\alpha}$$

$$\Rightarrow\quad(m_{X}-m_{X'}-m_{\alpha})c^{2}=T_{X'}+T_{\alpha}.$$

The [[Q-value]] is therefore

$$Q=(m_{X}-m_{X'}-m_{\alpha})c^{2};$$

since the α-particle mass is known, the other two masses are taken from atomic-mass tables (electron masses cancel). With $c^{2}=931.5$ MeV/u and atomic masses in the hundreds, $Q$ is of order MeV.

Alternatively,

$$Q=T_{X'}+T_{\alpha},$$

and momentum conservation gives $p_{\alpha}=p_{X'}$. Typical $T_{\alpha}\approx5$ MeV, so both $T_{X'}$ and $T_{\alpha}$ are $\ll mc^{2}$; classical kinematics suffices. Using $T=p^{2}/2m$,
$$T_{\alpha}=\frac{Q}{1+\dfrac{m_{\alpha}}{m_{X'}}}\quad\text{with}\quad\frac{m_{\alpha}}{m_{X'}}\ll1$$
for a heavy nucleus. Hence

$$T_{\alpha}=\frac{Q}{1+\dfrac{4}{A}}\quad\text{for}\quad A\gg4\quad\Bigl(\frac{m_{\alpha}}{m_{X'}}\approx\frac{4}{A-4}\Bigr).$$