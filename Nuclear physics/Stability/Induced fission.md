---
wiki-publish: true
---
**Induced fission** is a mode of [[nuclear decay|decay]] in which a heavy [[Atomic nucleus|nucleus]] is struck by a [[neutron]], causing it [[nuclear fusion|fuse]] with the nucleus and producing a highly unstable excited [[isotope]] which then immediately undergoes [[nuclear fission]].

The nuclear reaction reads
$$\ce{^{A}X_{N}}+n\to \ce{^{A+1}X^{*}_{N+1}}\to\ce{X'}+\ce{X''}+\nu n$$
where $\ce{X}$ is the original nuclide, $\ce{^{A+1}X^{*}_{N+1}}$ is its isotope with one more neutron, left in an excited state, $\ce{X'}$ and $\ce{X''}$ are the fission fragments and $\nu n$ are the $\nu$ additional [[neutron|neutrons]] that are emitted as part of the fission. It is a two-step process in which the nucleus is first bombarded with a neutron, then the resulting isotope undergoes [[spontaneous fission]]. As such, induced fission is essentially a brute-force method to make spontaneous fission happen when it can't happen naturally, or when it doesn't happen sufficiently fast for the intended use case. For this reason, the physics behind induced fission are almost the same as the spontaneous case, with the only major difference being the first step.

Since induced fission relies on creating a highly unstable isotope that will spontaneously split, not all [[Nuclide|nuclides]] are a good fit for nuclear fuel. Materials that undergo fission after being struck with a low-energy neutron (**thermal neutron**, $\sim 0.025\text{ eV}$) are called **fissile materials**. The most common fissile materials is $\ce{^{235}U}$. Materials that undergo fission only when struck by a high-energy neutron (**fast neutron**, $\sim 1\text{ MeV}$) are called **fissionable materials**. The most common one is $\ce{^{238}U}$. The big difference is that fissile materials can sustain a thermal-neutron chain reaction, whereas fissionable ones cannot. Finally, materials that don't undergo fission when struck, but produce fissile or fissionable material are called **fertile materials**. The most common are $\ce{^{234}U}$ and, maybe surprisingly, $\ce{^{238}U}$ again. $\ce{^{234}U}$ produces $\ce{^{235}U}$, which we mentioned is a fissile. Meanwhile, $\ce{^{238}U}$ *can* momentarily become $\ce{^{239}U^{*}}$ and then split, but unless the neutron was very energetic, it generally becomes $\ce{^{239}U}$ (not excited) and then [[Beta decay|beta decays]] twice to become $\ce{^{239}Pu}$, which is fissile.

For example, one possible induced fission of $^{235}\text{U}$ reads
$$\ce{^{235}_{92}U_{143}} + n\to \ce{^{236}_{92}U^{*}_{144}} \rightarrow\ \ce{_{37}^{93}Rb_{56}}+ \ce{_{55}^{141}Cs_{86}}+2n$$
### Energy
In induced fission, there's *two* kinds of energy we're interested in. On one hand, we are interested in the [[Q value]], since that's what the fission finally yields in usable energy. But on the other hand, we also need to consider how much energy we need to give to the nucleus to trigger the fission. The latter is a bit more complicated and there are actually two metrics for it.

The **excitation energy** is the difference in rest energy between the excited and non-excited state of the isotope that's created by the neutron absorption:
$$E_\text{exc}=[M(\ce{^{A+1}X^{*}})-M(\ce{^{A+1}X})]c^{2}$$
where the excited isotope's mass is easily calculated by just adding a neutron to the original isotope's mass: $M(\ce{^{A+1}X^{*}})=M(\ce{^{A}X})+m_{n}$. This is different from the [[Q value]], which we don't care about for the neutron collision. This intentionally does not include the [[kinetic energy]] contribution of the neutron because...

...the **activation energy** is the energy that is *actually* required to induce fission. It's the energy that's needed overcome the [[potential energy|potential]] barrier that prevents the nucleus from splitting. Critically, this is *different* from excitation energy and this has important consequences on induced fission. If the activation energy is higher than the excitation energy, that means that just exciting that nucleus is *not* enough to induce fission. In that case, not only must you excite the nucleus, but the neutron you excite it with must *also* transfer enough kinetic energy to cover the difference between excitation and activation energy. Only then will the nucleus have enough to undergo fission. However, if the activation energy is lower than the excitation energy, that means that any excitation will result in a splitting of the nucleus. As such, materials that have a low activation energy are much more likely to be useful for induced fission. In fact, this is the difference between fissile and fissionable materials: if the activation energy is lower than excitation energy, it's fissile; if it's higher, it's fissionable.

Activation energy is often measured empirically, but we can use the [[nuclear shell model]] to make some theoretical predictions.

If you do manage to supply the activation energy, fission happens. This is where energy is actually released and where we care about the $Q$ value. Since this process is [[spontaneous fission]], you may refer to that article for discussion on the $Q$ value.

> [!example]- Uranium-235 and 238
> In the fission example of $\ce{^{235}U}$, the excitation energy is
> $$E_{\text{exc}}=[M(\ce{^{236}U^{*}})-M(\ce{^{235}U})]c^{2}=6.5\text{ MeV}$$
> Meanwhile, the activation energy is known to be about 6.2 MeV. As such, any excitation will cause it to overcome the potential barrier and split. This is why $\ce{^{235}U}$ is considered fissile and even extremely low energy neutrons cause it to crack.
> 
> Meanwhile, the excitation and activation energies of $\ce{^{238}U}$ are
> $$E_\text{exc}=4.8\text{ MeV},\qquad E_\text{act}=6.6\text{ MeV}$$
> The difference between these two is important and just exciting $\ce{^{239}U}$ will not cause it to split. The neutron must supply *at least* $E_\text{act}-E_\text{exc}=1.8\text{ MeV}$ of energy for it split. This is why $\ce{^{238}U}$ is considered fissionable.
