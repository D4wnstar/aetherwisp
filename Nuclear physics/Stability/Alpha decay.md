---
wiki-publish: true
aliases:
  - alpha particle
---
**Alpha decay** is a mode of [[Nuclear decay|decay]] in which a [[Atomic nucleus|nucleus]] emits an **alpha particle**, which is another name for the helium-4 nucleus $\ce{_{2}^{4}He_{2}}$. The alpha particle is a proper nucleus, comprised of two [[proton|protons]] and two [[neutron|neutrons]], which is very tightly [[Binding energy|bound]] due to being [[Magic number|doubly magic]]. As such, alpha decay is a type of [[cluster decay]], and the most common one by far.

The nuclear process is
$$\ce{_{Z}^{A}X_{N}}\ \rightarrow\ \ce{_{Z-2}^{A-4}X'_{N-2}}+\alpha$$
where $\ce{X}$ and $\ce{X}'$ are the parent and daughter [[Nuclide|nuclides]] and $\alpha$ is the alpha particle. The missing two protons and neutrons in the daughter nucleus $\ce{X}'$ are ejected through the alpha particle.

The alpha decay is governed by the opposition of the nuclear attraction due to the [[Strong interaction|strong force]] and the repulsion due to [[electromagnetism]].

An example alpha decay is for radium-226:
$$\ce{_{88}^{226}Ra_{138}}\ \rightarrow\ \ce{_{86}^{222}Rn_{136}}+\ \ce{_{2}^{4}He_{2}}$$
The [[half-life]] of this decay is about 1600 years and the [[kinetic energy]] of the alpha particle is about 4.8 [[Electronvolt|MeV]].
### Mechanism
Within the nucleus, protons and neutrons are subject to binding energies around 8 MeV each. The exact number depends on the nucleus: see [[Semi-empirical mass formula]] for a theoretical prediction. For them to escape, the nucleus must be in a condition where ejecting an alpha particle would leave the nucleus with more binding energy per nucleon than it started. Beyond $A\sim56$, binding energy per nucleon begins to progressively drop. As such, from this point on, it can be energetically favored to eject one or more nucleons, resulting in a smaller, more bound nucleus. It is this condition that makes alpha decay feasible, which is why it occurs primarily in large, heavy nuclei ($A\gtrsim 100$ at least, often $A\gtrsim 200$)[^1].

We start from the [[potential energy]] $U(r)$ of an $\alpha$ particle at distance $r$ from the nucleus:

![[Plot Alpha decay potential|80%|center]]

Let's unpack what is happening. The figure shows an $\alpha$ particle (the circle with four smaller circles in it, representing two protons and neutrons), which is taken to be a part of a larger nucleus, inside the potential well of the nucleus. Remember that by the [[least action principle]], the particle will spontaneously fall to the region of lowest potential energy, so to answer the question of why the alpha particle is ejected, we need to analyze the potential.

At short range the attractive strong force dominates, creating a deep potential well $-U_{0}$ that holds the nucleus together. The strong force is very range-limited however, dropping off to near-zero at just a few femtometers, so at longer ranges it's Coulomb repulsion that dominates, shown in the figure as $U_{C}$[^2]. In the formula, $Z$ is the atomic number of the nucleus, $2e$ is the [[electric charge]] of the $\alpha$ particle and $(Z-2)e$ is the charge of the nucleus not including the $\alpha$ particle.

In small nuclei, the $\alpha$ particle is comfortably in the nuclear potential well and there is no chance of it escaping. However, when the proton count becomes really large, two things happen: on one hand, the outer [[Nuclear shell model|shell]] nucleons get further away from the center, getting closer to the strong force cutoff distance; on the other, the higher proton number means an increased electrostatic repulsion. Both these effects combine to make outer nucleus quite unstable and inclined to be emitted.

The question of why emit specifically an $\alpha$ particle and not individual protons and nucleons is answered, at least in part, by the considerable binding energy of the doubly magic $\ce{^{4}_{2}He_{2}}$ nucleus, which makes it prone to being emitted as a single cluster instead of being broken apart, which would be very energetically expensive.

So, to summarize, we have an $\ce{^{4}_{2}He_{2}}$ cluster in a large nucleus. For it to be emitted, it must possess sufficient [[kinetic energy]] to overcome the potential barrier $U_\text{barrier}$ created by the strong force holding the nucleus together. Experimentally, however, we know that the kinetic energy $K_{\alpha}$ of an emitted $\alpha$ particle is generally in the range of 4 to 9 MeV, which is a good deal less than $U_{0}$, which we know to often be in the order of $\sim 30\text{ MeV}$ or more. The $\alpha$ particle should never be capable of crossing the barrier. So what happens?

What happens is [[quantum tunnelling]]. Due to quantum mechanical effects and the [[Equazione di Heisenberg|uncertainty principle]], there is always a [[Probability|chance]] that a particle behind a (spatially finite) potential barrier will *tunnel* through the barrier and end up on the other side. The likelihood of this happening is dependent on energy, and as one might expect it grows higher as the particle's energy is higher. As such, even if the $\alpha$ particle's kinetic energy isn't sufficient to cross the barrier *classically*, there is still a *quantum* chance that it will get through. Note that the barrier that is tunneled through is $U_\text{barrier}$, not $U_{0}$.

Say an $\alpha$ particle tunnels through from point $a$, its initial distance from the center of the nucleus, to point $b$, on the other side of the barrier. The value $U_\text{barrier}$ is
$$U_\text{barrier}=U_{C}(a)-U_{C}(\infty)=\frac{2(Z-2)e^{2}}{4\pi \varepsilon_{0}a}$$
The effective height of the barrier to cross will be $U_\text{cross}=U_\text{barrier}-K_{\alpha}$ in $a$ and $U_\text{cross}=0$ in $b$. We consider the midpoint value as an estimate:
$$U_\text{cross}\simeq \frac{1}{2}(U_\text{barrier}-K_{\alpha})$$
To get the tunneling probability, we need to solve the one-dimensional [[Schrödinger equation]]. Thanks to our midpoint approximation, this is basically a [[Buca finita quantistica|finite square well]], just with a positive potential making a barrier instead of a well. In general, the [[Rappresentazioni dello stato|position representation]] [[wavefunction]] $\psi(x)$ of a particle that interacts with a finite square barrier of potential $V(x)$ is determined by:
$$\frac{\hbar^{2}}{2m}\frac{d^{2}\psi(x)}{dx^{2}}+V(x)\psi(x)=E\psi(x)$$
where $E$ is the [[Stationary state|energy eigenvalue]] and
$$V(x)=\begin{cases}
0 & \text{if }x<a \\
V_{0} & \text{if }a\leq x\leq b \\
0 & \text{if }x>b
\end{cases}$$
is the potential of the barrier. There are three regions:
- Before the barrier, $\psi_{1}(x)=Ae^{ik_{1}x}+Be^{-ik_{1}x}$;
- Inside the barrier, $\psi_{2}(x)=Ce^{k_{2}x}+De^{-k_{2}x}$;
- After the barrier, $\psi_{3}(x)=Fe^{-ik_{3}x}$.

Careful with the complex exponentials before and after the barrier. The [[Wavenumber|wavenumbers]] are
$$k_{1}=k_{3}=\sqrt{\frac{2mE}{\hbar^{2}}},\qquad k_{2}=\sqrt{\frac{2m(V_{0}-E)}{\hbar^{2}}}$$
The transmission coefficient $P_{T}$ is the ratio $F^{2}/A^{2}$, which ends up being
$$T^{-1}=\frac{A^{2}}{F^{2}} =1+\frac{1}{4}\frac{V_{0}^{2}}{E(V_{0}-E)}\sinh^{2}(k_{2}a)$$
(given as its reciprocal because it's easier to read). This is the probability of the $\alpha$ particle tunneling through the barrier.

Now, in our specific case, the quantity $V_{0}-E$ (the difference in energy between the barrier and the particle) is $U_\text{cross}$, so the wavenumber becomes
$$k_{2}\simeq\sqrt{\frac{m}{\hbar^{2}}(U_\text{barrier}-K_{\alpha})}$$
Similarly, $E\to K_{\alpha}$ and $V_{0}\to U_\text{barrier}$, so
$$\boxed{T^{-1}\simeq1+\frac{1}{2}\frac{U_{\text{barrier}}^{2}}{K_{\alpha}U_\text{cross}}\sinh^{2}(k_{2}a)}$$
The distance $b$ at which the $\alpha$ particle tunnels to can be approximated with
$$b\simeq\frac{1}{4\pi\epsilon_{0}}\frac{2(Z-2)e^{2}}{K_{\alpha}}$$
Both $b$ and $T$ are very sensitive to $K_{\alpha}$; small changes in $K_{\alpha}$ can change rates of decay by orders of magnitude. The only thing that's left to conclude is to figure out how often the particle attempts to tunnel, which can be imagined as the particle physically colliding with the particle barrier[^3]. The tunneling frequency $f$ is in the order of
$$f\sim \frac{v}{a}$$
where $v$ is the velocity of the $\alpha$ particle inside the nucleus. Then, given the transmission probability, we define the **disintegration constant**:
$$\boxed{\lambda=fT}$$
This constant tells you how fast an alpha-unstable piece of matter decays. It is a decay constant in the sense of the [[radioactive decay law]], so with it you can get the decay half-life $t_{1/2}=\ln 2/\lambda$ and decay lifetime $\tau=1/\lambda$, which give you an estimate of the how long, statistically speaking, it takes for alpha-unstable matter to decay.
### Energy conservation
Energy conservation is useful to draw more quantitative conclusions about alpha decay, especially regarding the kinetic energy of the decay products. If the parent nucleus $\ce{X}$ is at rest at the time of decay, the initial energy is its [[Relativistic energy|rest energy]] $E_{i}=m_{\ce{X}}c^{2}$. The final state consists of $\ce{X}'$ and $\alpha$. Both of them are in motion because [[Linear momentum|momentum]] must be conserved, so $\ce{X}'$ recoils backwards when $\alpha$ is emitted. The final energy therefore is
$$E_{f}=m_{\ce{X}'}c^{2}+K_{\ce{X}'}+m_{\alpha}c^{2}+K_{\alpha}$$
Energy conservation demands $E_{i}=E_{f}$ so
$$m_{\ce{X}}c^{2}=m_{\ce{X}'}c^{2}+K_{\ce{X}'}+m_{\alpha}c^{2}+K_{\alpha}\quad\Rightarrow\quad(m_{\ce{X}}-m_{\ce{X}'}-m_{\alpha})c^{2}=K_{\ce{X}'}+K_{\alpha}$$
Both sides represent the energy released during the decay (i.e. energy transformed into kinetic energy). This is the [[Q value]] of the process:
$$\boxed{Q=(m_{\ce{X}}-m_{\ce{X}'}-m_{\alpha})c^{2}}\tag{1}$$
This value can be determined entirely from empirical tabulated data since we have tables of nuclear masses (thanks to e.g. [[mass spectrometry]]). It is more or less always in the range of 4 to 9 MeV. Equivalently:
$$Q=K_{\ce{X}'}+K_{\alpha}$$
Due to the known range of $Q$ being in MeV, this suggests that the associated kinetic energies are not high enough ($\ll mc^{2}$) to require the use of special relativity. As such, and also due to conservation of momentum $p_{\ce{X}'}=p_{\alpha}\equiv p$, the kinetic energies are quite simply
$$K_{\ce{X}'}=\frac{p^{2}}{2m_{\ce{X}'}},\qquad K_{\alpha}=\frac{p^{2}}{2m_{\alpha}}$$
so the $Q$ value is
$$Q=K_{\ce{X}'}+K_{\alpha}=\frac{p^{2}}{2}\left( \frac{1}{m_{\ce{X}'}}+ \frac{1}{m_{\alpha}} \right)=K_{\alpha}\left( 1+ \frac{m_{\alpha}}{m_{\ce{X}'}} \right)$$
and so
$$K_{\alpha}=\frac{Q}{1+\dfrac{m_{\alpha}}{m_{X'}}}=\frac{m_{\ce{X}'}}{m_{\ce{X}'}+m_{\alpha}}Q$$
Now, for any nucleus concerned with alpha decay ($A\gg 100$) the alpha particle's mass will be almost insignificant by comparison, so $m_{\alpha}/m_{X'}\ll1$. Hence we afford to approximate masses. Every nucleus' mass is more or less given by $m\simeq Am_{u}$ where $u$ is the [[atomic mass unit]] $m_{u}=931\text{ MeV/c}^{2}$. So
$$\frac{m_{\ce{X}'}}{m_{\ce{X}'}+m_{\alpha}}\simeq \frac{(A-4)m_{u}}{(A-4)m_{u}+4m_{u}}=\frac{A-4}{A}$$
and so
$$\boxed{K_{\alpha}\simeq \frac{A-4}{A}Q}$$
This is the fraction of the released energy that is transferred to the alpha particle. The rest is recoil in the nucleus. You can easily see how the bigger the nucleus is, the closer to 100% it gets. Since alpha decay matters only in large nuclei, the alpha particle kinetic energy generally amounts to the near totality of the energy being released. For instance, in antimony-104, which is the smallest [[nuclide]] known to alpha decay[^1], we have
$$K_{\alpha}\simeq \frac{100}{104}Q=0.962Q$$
or in uranium-238
$$K_{\alpha}\simeq \frac{234}{238}Q=0.983Q$$
Suffice to say that recoil is a minimal (but very necessary!) part of energy conservation.

Another very interesting piece of data is that if we use express $(1)$ in terms of component masses ($m_\text{nucleus}=Zm_{p}+Nm_{n}+Zm_{e}-B/c^{2}$), we get
$$Q=B(X')+B(\alpha)-B(X)$$
where $B$ is binding energy. Rearrange to get
$$\Delta B=B(X')-B(X)=Q-B(\alpha)$$
But we *know* $B(\alpha)$, because $\alpha$ is always the same thing (it's $B(\alpha)\simeq28.30\text{ MeV}$), so $Q$ is the only thing we need to determine the binding energy difference which, remember, is the whole *point* of decay. But we also know the range of $Q$, it's 4 to 9 MeV. So, the range of $\Delta B$ comes out to be between -24 and -19 MeV of energy. Thus, the daughter nucleus possesses less binding energy than its parent. But wait, doesn't that make it less stable? *No*, because we're *also* removing nucleons. Yes, the binding energy decreases, but *of course* it does, we're removing the very things that are keeping the nucleus together. What matters in nuclear stability is binding energy *per nucleon* and *that* increases:
$$B(X')<B(X)\quad\text{but}\quad \frac{B(X')}{A-4}> \frac{B(X)}{A}$$

> [!example]- Uranium-238 to Thorium-234
> Take uranium-238, probably the most famous radionuclide even outside of science. It alpha decays into thorium-234 with a known $Q$ value of $4.270\text{ MeV}$, so
> $$\Delta B=B(\ce{^{234}Th})-B(\ce{^{238}U})=Q-B(\alpha)=4.270\text{ MeV}-28.30\text{ MeV}=-24.03\text{ MeV}$$
> Empirically, the mass of uranium-238 is
> $$m(\ce{^{238}U})=238.051\text{u}$$
> It's binding energy therefore is
> $$B(\ce{^{238}U})=(92m_{p}+148m_{n}+92m_{e}-m(\ce{^{238}U}))c^{2}=1801\text{ MeV}$$
> This tells us that the binding energy of thorium-234 should be
> $$B(\ce{^{234}Th})=B(\ce{^{238}U})-24.03\text{ MeV}=1777\text{ MeV}$$
> Let's check the binding energy per nucleon:
> $$\frac{B(\ce{^{238}U})}{238}=7.569\text{ MeV/nucleon},\quad \frac{B(\ce{^{234}Th})}{234}=7.594\text{ MeV/nucleon}$$
> It increased! By about $7.594/7.569=1.003$ times, or a 0.3% increase.

[^1]: Actually, beryllium-8 is known to alpha decay into two identical helium-4 atoms, essentially splitting in half. This is an exceptional case however.

[^2]: To be clear, this is electric potential *energy* (in joules), not electric potential (in volts).

[^3]: Of course, at this scale the localization of the $\alpha$ particle is all over the place due to the uncertainty principle, so this is not at all a rigorous statement, but it makes for a useful mental image.
