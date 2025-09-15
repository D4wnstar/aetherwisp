---
wiki-publish: true
---
### Nuclear
**Semi-empirical mass formula**
$$m(Z,A)=N m_n+Z m_p+Z m_e-\frac{B(Z,A)}{c^{2}}$$
$$\frac{B(Z,A)}{c^{2}}=a_v A-a_s A^{2/3}-a_{C}\frac{Z(Z-1)}{A^{1/3}}-a_a\frac{(N-Z)^2}{4A}+\delta$$
$$\begin{aligned}
\delta &= +a_p A^{-3/4} &&\text{if }A,Z,N\text{ even}\\
\delta &= 0 &&\text{if }A\text{ odd}\\
\delta &= -a_p A^{-3/4} &&\text{if }A\text{ even and }Z,N\text{ odd}
\end{aligned}$$
$$\begin{align}
a_v &= 15.67\,\tfrac{\text{MeV}}{c^{2}}\\
a_s &= 17.23\,\tfrac{\text{MeV}}{c^{2}}\\
a_{C} &= 0.714\,\tfrac{\text{MeV}}{c^{2}}\\
a_a &= 93.15\,\tfrac{\text{MeV}}{c^{2}}\\
a_p &= 34\,\tfrac{\text{MeV}}{c^{2}}
\end{align}$$
**Decay law**
$$N(t)=N_{0}e^{-\lambda t}\quad t_{1/2}=\frac{\ln2}{\lambda},\quad \tau=\frac{1}{\lambda},\quad A=\lambda N(t)=A_{0}e^{-\lambda t}$$
Production-decay
$$N_{1}(t)=\frac{R}{\lambda_{1}}(1-e^{-\lambda_{1}t})$$
Chain decay
$$N_{2}(t)=\frac{\lambda_{1}}{\lambda_{2}-\lambda_{1}}N_{0}(e^{ -\lambda_{1}t }-e^{ -\lambda_{2}t })$$

**Alpha decay**
$$\ce{_{Z}^{A}X_{N}}\ \rightarrow\ \ce{_{Z-2}^{A-4}X'_{N-2}}+\alpha$$
$$Q=(m_{\ce{X}}-m_{\ce{X}'}-m_{\alpha})c^{2},\quad K_{\alpha}\simeq \frac{A-4}{A}Q$$
**Beta decay**
$$\begin{align}
\beta^{+}\text{ decay:}\quad &p\to n+e^{+}+\nu_{e}\\
\beta^{-}\text{ decay:}\quad &n\to p+e^{-}+\bar\nu_{e}\\
\text{EC:}\quad &p+e^{-}\to n+\nu_{e}
\end{align}$$
$$Q_{\beta^{-},\text{vacuum}}=(m_{n}-m_{p}-m_{e}-m_{\nu})c^{2}\simeq 0.8\ \text{MeV}$$
$$Q_{\beta^{-},\text{nucleus}}=[M(\ce{^{A}X})-M(\ce{^{A}X}')]c^{2}$$
$$Q_{\beta^{+},\text{nucleus}}=[m(^{A}\text{X})-m(^{A}\text{X}')-2m_{e}]c^{2}$$
$$Q_{\text{EC}}=[m(^{A}\text{X})-m(^{A}\text{X}')]c^{2}-B_{e^{-}}$$
**Gamma decay**
$$\ce{X^{*}}\to \ce{X}+\gamma$$
$$E_{\gamma}\simeq\Delta E, \quad K_{R}= \frac{(\Delta E)^{2}}{2Mc^{2}}$$
The selection rules are
1. Gamma radiation is the linear combination of all multipole terms $L$ allowed by $\lvert J_{i}-J_{f} \rvert\leq L\leq J_{i}+J_{f}$, excluding $L=0$.
2. If parity doesn't change, odd poles are electric and even ones are magnetic. If parity changes, odd poles are magnetic and even ones are electric.
**Spontaneous fission**
$$\ce{X}\to\ce{X'}+\ce{X''}+\nu n$$
$$Q=[M(\ce{X})-M(\ce{X}')-M(\ce{X}'')-\nu m_{n}]c^{2}\simeq Q=0.9A\text{ MeV}$$
**Q value**
$$Q=(m_\text{before}-m_\text{after})c^{2}=K_\text{after}-K_\text{before}$$
**Nuclear shell model**
![[Oxygen shells.png]]
$$J=\text{that of the missing shell},\quad P=(-1)^{l}$$
Even-even: $J^{P}_\text{ground}=0^{+}$, $J^{P}_\text{exc,1}=2^{+}$,...
Odd-odd: $J=\lvert J_{1}-J_{2} \rvert,\ldots,\lvert J_{1}+J_{2} \rvert$. $P=(-1)^{l_{1}+l_{2}}$.
### Particles
See [[Tabella di proprietà delle particelle]]
### Detectors
**Bethe-Bloch formula**
$$S(K)=- \frac{dK}{dx} = 4\pi m_{e}c^{2}r^{2}_{e}N_{A} \frac{\rho Z}{A} \frac{z^{2}}{\beta^{2}} \ln\left( \frac{\beta^{2} \gamma^{2}m_{e}c^{2}}{h\nu} \right)$$
Simplified for nonrelativistic particles
$$\frac{dK}{dx} \sim \frac{z^{2}}{\beta^{2}}=\frac{z^{2}c^{2}(M/2)}{v^{2}(M/2)} = C\frac{Mz^{2}}{K}$$
**Stopping power for light particles**
$$S(K) = \frac{K}{L_{R}}\quad\Rightarrow \quad K(x) = K_{0} e^{-x / L_{R}}$$
**Cherenkov radiation**
$$\cos\theta_{C}=\frac{1}{n\beta}$$
Minimum $\beta$ to occur is $\beta _\text{min}=1/n$ (must be above speed of light in medium). If you know $\theta_{C}$, you can get $\beta$ out of it.
**Time of flight**
Error on measurement:
$$\sigma _\text{TOF}=\sqrt{ 2 }\sigma_{t}\quad\Rightarrow \quad \frac{\sigma _\text{TOF}}{\text{TOF}}=\sqrt{ 2 } \frac{v}{L}\sigma _{t}$$
when start and end detectors are same. More distance, more precision.
**Photoelectric effect**
Energy released
$$E_{e^{-}}=E_{\gamma}-B$$
Energy of the electron is photon minus electron binding energy. Cross section is dependent on $Z$ to the fifth power, $\sigma \propto Z^{5}$.
**Electron-positron pair production**
$$\gamma X\to Xe^{-}e^{+}$$
must happen in matter because $\gamma$ invariant mass is zero. Emitted electron/positrons will emit high-energy photons by bremmstrahlung, which themselves pair-produce in about a radiation length $L_{R}$, creating a cascade:
$$E(t_\text{max})=E_{C}=\frac{E_{0}}{2^{t_\text{max}}}\quad \Rightarrow \quad t_\text{max}=\frac{ \ln\left( \frac{E_{0}}{E_{C}} \right)}{\ln 2}$$
**Compton scattering**
$$\lambda=\lambda_{0}+ \lambda_{C}(1-\cos \theta)\quad\text{where}\quad \lambda_{C}=\frac{h}{mc}$$
