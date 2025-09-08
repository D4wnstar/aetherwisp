---
wiki-publish: true
---
When the [[Universe]] was young, after the [[Big Bang nucleosynthesis]] era, the large majority of [[matter]] was simple [[Atomic nucleus|nuclei]], hydrogen and helium. These aggregated thanks to [[gravity]] to form the first [[Stella|stars]], triggering [[nuclear fusion]] and beginning *stellar* nucleosynthesis. Fusion formed [[Nuclide|nuclides]] up to iron and when the first large stars perished, their [[Supernova|supernovas]] formed even heavier elements. Many of these were [[Nuclear decay|radioactive]] and highly unstable, but some had very long [[half-life|half-lives]], so when the [[Disco protoplanetario|protoplanetary disk]] that would birth the [[Earth]] was created, many of these elements got embedded in what would become our planet. Then, four and half billion years later after the formation of the planet, many of them are still there, decaying. These form the so-called **background radiation of the Earth**.

If you were to go down a mine shaft, you'd eventually be at risk of [[radiation poisoning]] (though not that quickly). This is because the radioactive minerals are, of course, embedded in the rock in our underground. To better understand how decay occurs in practice, recall that [[alpha decay]] reduces the [[Atom|atomic mass number]] by 4 and that [[beta decay]] leaves it unchanged. Then, there must be four decay chains, one for each reminder of $A/4$. Call these $4n$, $4n+1$, $4n+2$ and $4n+3$.

| Chain     | Kind   | End point       | Element with longest half-life                   |
| --------- | ------ | --------------- | ------------------------------------------------ |
| Thorium   | $4n$   | $\ce{^{208}Pb}$ | $^{232}\text{Th}$ with $1.41\times10^{10}$ years |
| Neptunium | $4n+1$ | $\ce{^{209}Bi}$ | $^{237}\text{Np}$ with $2.14\times10^{6}$ years  |
| Uranium   | $4n+2$ | $\ce{^{206}Pb}$ | $^{238}\text{U}$ with $4.47\times10^{9}$ years   |
| Actinium  | $4n+3$ | $\ce{^{207}Pb}$ | $^{235}\text{U}$ with $7.04\times10^{8}$ years   |

A decay chain tends to create a surplus of the longest lived nuclide, since it's the one that takes the longest to "drain", so it's particularly common compared to the other radionuclides of the chain. Now, the Earth is more or less $4.5\times 10^{9}$ years old, so the Neptunium chain is all but depleted since the longest lived nuclide burns through more 1000 times faster than the age of the Earth. Uranium-235 is also in large part gone, though there's still a non-negligible amount left; about 0.72% of uranium on Earth is 235.

All the chains go through a particularly infamous component: radon. Radon is a gas that, due to this radioactive decay, has gotten embedded in rock throughout the underground. When the rocks are broken, say due to a mining effort, this radon is released in small quantities. It can get breathed in quite easily, leading it to decay within the human body. This is a severe health risks for miners, as it can very easily lead to acute symptoms as well as life-threatening long-term risks like increased cancer incidence. Something similar can occur when dismantling buildings made from material containing radioactive components, such as the now-phased-out asbestos-based concretes.
### Age of the Earth
We can use the abundance of uranium today to reverse-engineer the age of the Earth. Assume that all long-lived uranium [[Isotope|isotopes]] were in equal abundance at the formation of the Earth. That's to say 50-50 between $\ce{^{235}U}$ and $\ce{^{238}U}$. We can use their current ratio to determine how long it took for them to diverge this much.

The [[radioactive decay law]] says
$$N(t)=N_{0}e^{-\lambda t}$$
Then, the modern ratio gives us
$$\frac{N_{238}(t)}{N_{235}(t)}=\frac{99.28}{0.72}=\frac{e^{-\lambda_{238}t}}{e^{-\lambda_{235}t}}=e^{(\lambda_{235}-\lambda_{238})t}$$
where $t$ represents the time since the formation of the Earth and $N_{0}$ was taken to be equal for both. Extracting $t$ gives
$$t=\frac{\ln(99.28/0.72)}{\lambda_{235}-\lambda_{238}}$$
We know the half-lives of both isotopes from modern measurements
$$t_{1/2,238}=4.468\times10^{9}\text{ years},\quad t_{1/2,235}=7.038\times10^{8}\text{ years}$$
so the [[Radioactive decay law|decay constants]] are
$$\lambda_{238}=\frac{\ln2}{t_{1/2,238}}=1.55\times10^{-10}\text{ years}^{-1},\quad\lambda_{235}=9.85\times10^{-10}\text{ years}^{-1}$$
Then the Earth must have been formed
$$t=5.94\times10^{9}\text{ years ago}$$
That's about 25% off the mark, but for such a crude and simple estimate, it's a pretty impressive result!