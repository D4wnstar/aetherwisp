---
wiki-publish: true
---
[[Electromagnetic wave|Electromagnetic waves]] are complicated. They have a lot of related quantities with similar names that are often useful, but also equally often misnamed in as many ways as there are branches of physics. This article is a survival guide on radiometric nomenclature to try to convey a common standard to make sense of all of this. It does not attempt to be a complete or exhaustive explanation of these quantities: the point is to dispel confusion, clarify the connections between them and provide a common terminology.

Some conventions:
1. by "wave" I always mean "electromagnetic wave".
2. by "radiation" I always mean "electromagnetic radiation".
3. square brackets contain the SI units for the quantity in question.
4. I generally do not provide a conventional letter or symbol for the quantity. This may change in the future.

**Radiant energy** $[\text{J}]$ is the [[energy]] carried by a wave. **Radiant energy density** $[\text{J/m}^{3}]$ is the volume density of radiant energy. "Radiant" is often dropped for brevity if it's obvious that we're talking about waves.

**[[Radiant power]]** $[\text{W}]$ is the [[power]] of radiant energy (energy per unit time). It is also called **radiant flux**. This is a ludicrous name since it is *not* an energy [[flux]] (power per unit area) and will therefore not be used anywhere in these notes. Radiant power is a key quantity since it describes a movement of energy, which is generally what you are interested in when talking about radiation. In practice, however, it's not often the quantity you are looking for. Rather, you are looking the power spread over a certain region of space. There are a several quantities to express this depending on the context:
1. **[[Irradiance]]** $[\text{W/m}^{2}]$ is radiant power *received* by a *surface*. Also confusingly called "intensity". Generally speaking the most useful quantity in physics.
2. **Radiant exitance** $[\text{W/m}^{2}]$ is radiant power *emitted* by a *surface*. Also confusingly called "intensity".
3. **Radiosity** $[\text{W/m}^{2}]$ is radiant power *leaving* a *surface*. This includes emission, reflection and transmission. As such, radiosity is a broader concept than exitance and fully includes it. Also confusingly called "intensity".
4. **Radiant intensity** $[\text{W/sr}]$ is radiant power per *solid angle* ($\text{sr}$ is steradian). It includes all energy: emitted, reflected, transmitted and received. It is the amount of power going through a specific direction (the solid angle).
5. **Radiance** $[\text{W/sr/m}^{2}]$ is radiant intensity per unit *area*. It is the amount of power going through a direction over a surface.

:::image
![[Photometry_radiometry_units.svg|500]]
Visual guide to radiometric quantities. The red quantities are the significant ones. (The purple ones are *photometric*, that is, weighed by what the human eye can see).
By Cmglee - Own work, CC BY-SA 4.0, from [Wikipedia](https://commons.wikimedia.org/w/index.php?curid=121743159).
:::

One last note. I could not find specific terms for the "intensity" of reflected and transmitted radiation specifically, since radiant exitance is technically only for *emitted* waves, which are distinct from reflected and transmitted ones. Since these come up all the time when dealing with material interfaces, I'll call them **reflected exitance** and **transmitted exitance**, with hopefully clear meaning.