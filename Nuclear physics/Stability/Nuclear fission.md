---
wiki-publish: true
aliases:
  - prompt neutron
  - delayed neutron
---
**Nuclear fission** is a nuclear reaction in which an [[atomic nucleus]] splits into two or more smaller nuclei, generally with the release of individual [[neutron|neutrons]]. It is a very high [[energy]] reaction, with a [[Q value]] around 200 [[Electronvolt|MeV]] regardless of [[nuclide]].

Nuclear fission can be both spontaneous or induced. **[[Spontaneous fission]]** occurs in superheavy nuclides where there is a very powerful [[Electromagnetism|electromagnetic]] repulsion due to a great excess of [[proton|protons]]. In these cases, the electrostatic forces can destabilize the nucleus enough to deform it until it splits. **[[Induced fission]]** is instead triggered by shooting a neutron at the nucleus, forcing it to split. This is done artificially in nuclear technology like nuclear reactors to use the very high $Q$ value to produce energy.
### Decay products
Fission is an unpredictable phenomenon, so its decay products are varied and in great part [[random]]. There's two categories of products:
- The fission always produces at least two daughter nuclei by splitting the parent[^1]. These are distributed according to known [[Probability distribution|probability distributions]] (see below).
- Fission also generally causes the ejection of a few individual neutrons which carry off a considerable chunk of the kinetic energy. Furthermore, the fragments are often left in a highly unstable state, so they can cause an immediate cascade of decays (most often [[Beta decay|beta]] and [[Gamma decay|gamma]]) which themselves produce more products.

These products are largely the same between spontaneous and induced fission. The latter can lead to more or higher-energy products due to the forced energy input by the incident neutron, but the physics is mostly the same.

For example, the induced fission of uranium-235 can lead to
$$\ce{^{235}_{92}U_{143}} + n\to \ce{^{236}_{92}U^{*}_{144}} \rightarrow\ \ce{_{37}^{93}Rb_{56}}+ \ce{_{55}^{141}Cs_{86}}+2n$$
Rubidium-93 and cesium-141 are the primary decay fragments. Two additional neutrons are emitted as secondary products. Rubidium-93 is highly unstable and $\beta^{-}$ decays a few seconds after. Cesium-141 is also unstable but not as a much, $\beta^{-}$ decaying with a [[half-life]] of about a month.

The fragments themselves are, curiously, known to follow two distinct distributions.

:::image
![[ThermalFissionYield.svg]]
Fission product distributions for three common radionuclides: uranium-233 (green), uranium-235 (red) and plutonium-239 (blue). Additionally, the black line is for a 65-35 mixture of uranium-235 and plutonium-239, a common choice for fuel in modern nuclear reactors.
By JWB, from [Wikipedia](https://commons.wikimedia.org/w/index.php?curid=16479803), CC BY 3.0
:::

As you can see in the figure, the fragments are sampled from two distinct [[Gaussian distribution|Gaussian-esque]] distributions, centered around $A=95$ and $A=135$. As such, the most typical fission event will create one small fragment and one big one. The chance of observing two same-sized fragment is hundreds of times smaller. Alas, we do not currently have an explanation for why this very particular distribution happens; we just know that it does.

*However*, the above plot primarily focuses on spontaneous fission and low-energy induced fission, that is, induced by low-energy neutrons. If the neutrons are much higher energy, the two distributions progressively merge and the chance of observing equally-sized fragments becomes larger. Again, we don't know why.

As for the secondary products, neutron emission is especially important in induced fission as these neutrons can themselves go on to induce the fission of other nuclei, initiating a chain reaction that can in theory last for as long as there are nuclei to split. This is the principle behind sustained fission in nuclear reactors.

Neutrons emitted during fission are categorized into two types:
- **Prompt neutrons** are those produced during the fission reaction itself (emitted within $10^{-16}$ seconds of the fission). The [[mean]] number of prompt neutrons $\nu$ per fission event is a property of each specific fission reaction.
- **Delayed neutrons** are produced by subsequent $\beta$ decays triggered by the fission. These can be delayed by anywhere between milliseconds to minutes. These are fewer in number than prompt neutrons, but are especially important in reactors as a method of controlling the chain reaction.

[^1]: Technically it's possible to create three or more fragments, and we have indeed observed such fissions, but these events are so rare that it's fair to ignore them outside of specialized analysis. They are called **ternary fission** (three fragments, 0.2-0.4% of fissions) and **quaternary fission** (four fragments, one-in-ten-million fissions). No five-fragment fission has ever been recorded. Usual two-fragment fission is called **binary fission**. The most common additional fragment is an [[Alpha decay|alpha particle]] (helium-4).
