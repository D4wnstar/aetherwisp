---
wiki-publish: true
aliases:
  - crystal structure
---
A **crystal** is a material that exhibits a periodic structure at a microscopic level, called the **crystal structure**. If the periodicity is extended through the entire specimen, it is simply called a crystal or a **monocrystalline** material. Otherwise, if the specimen is made up of many smaller pieces, each with their own crystalline structure, then it is said to be a **polycrystalline** material. Polycrystalline specimens are much more common in nature.

Mathematically, a crystal can be described by giving its underlying [[Bravais lattice]] alongside a description of the arrangements of its [[atom|atoms]], [[Molecule|molecules]], [[ion|ions]], etc. within a particular primitive cell of the lattice. This arrangement is known as the **basis** of the lattice. The crystal structure then consists of copying each cell alongside its basis to fill space, using the lattice points as markers on where to place the cells[^1].

:::image
![[Bravais lattice basis.png]]
A honeycomb crystal. The honeycomb pattern is *not* the Bravais lattice. The Bravais lattice is the points at the intersections between the [[parallelogram|parallelograms]]. Each parallelogram is a primitive cell. Each cell contains two atoms, bonded as per the thick solid line, which constitutes the basis. The parallelogram alongside the basis is the crystal structure. Copying the crystal structure near every lattice points yields the actual physical crystal.

You can see how the honeycomb pattern is restored by the bonds (dotted lines) that spontaneously form by placing each piece of the crystal structure next to another. From *Ashcroft & Mermin, Chapter 4*.
:::
## Internal structure probing by X-rays
We know that the natural size scale of an atom is on the order of one or a few angstrom (see for instance the [[Bohr radius]]). Thus, if we are to shine a light on the internal structure of a crystal, both literally and figuratively, we need our [[electromagnetic radiation]] to be have a comparable [[wavelength]]. By using the [[Planck formula]], we can figure out that the [[photon]] [[energy|energies]] at this scale are in the order of [[Elettronvolt|kiloelectronvolts]]: this is well into the domain of X-rays. Thus, the use of X-rays is the tool of choice for the probing of structure of a crystal.
### Diffraction from a lattice
Experimentally, W. H. Bragg and W. L. Bragg (father and son) found that, when shining an X-ray source at a crystalline solid, it produced noticeable patterns characterized by very strong peaks: these came to be known as **Bragg peaks**[^2], a [[diffraction]] phenomenon. The explanation for this was as follows: the crystal can be considered as made up of parallel (crystal) planes, each a distance $d$ apart and containing a lattice of ions, and in order to have a strong peak of reflection, two conditions must be met:
1. the X-rays should be specularly reflected (following [[Snell's law]]) by the ions of a plane;
2. rays reflected by adjacent planes must [[interference|interfere]] constructively. It is this constructive interference that causes the peaks to be so high.

So, we have two rays of light. One strikes an ion in a plane, the other strikes the corresponding ion in the next plane. The difference in light path between the two is given by $2d\sin \theta$, where $\theta$ is the angle of incidence (and also reflection; condition 1). Then, we need to determine the distance at which constructive interference happens (condition 2). This must be an integer multiple $n$ of the wavelength $\lambda$ of the incident light. This leads to the **Bragg condition**:
$$n\lambda=2d\sin \theta$$
$n$ is called the **order** of the reflection.

![[X-ray Bragg reflection.png]]

This is the **Bragg formulation** of the patterns. Another formulation is due to von Laue, simply called the **von Laue formulation**, and it is an equivalent explanation of the same phenomenon. von Laue makes no assumption regarding the reflection method (i.e. specular reflection), nor does he section the crystal into planes. Instead, the von Laue formulation regards the crystal as composed of identical microscopic objects (sets of ions and/or atoms) all placed at the sites $\mathbf{R}$ of a Bravais lattice. Each of these points can reradiate the incident radiation in any direction. Peaks will be observed only in directions and at wavelengths for which the rays scattered from all lattice interfere constructively.

To start, consider two scattering objects, a distance $\mathbf{d}$ apart, each struck by an X-ray of wavelength $\lambda$ and [[Wavenumber|wavevector]] $\mathbf{k}=2\pi \hat{\mathbf{n}}/\lambda$ along the direction $\hat{\mathbf{n}}$. Assuming [[particle scattering|elastic scattering]][^3], the X-rays will be reradiated with the same wavelength in a different direction $\hat{\mathbf{n}}'$. The new wavevector is $\mathbf{k}'=2\pi \hat{\mathbf{n}}'/\lambda$.

![[X-ray von Laue reflection.png]]

For the two to interfere constructively, they must be parallel (same $\hat{\mathbf{n}}'$ for both) and their path difference must again be an integer multiple $m$ of their wavelength. From the figure we can see the path difference is $d\cos \theta+d\cos \theta'=\mathbf{d}\cdot \hat{\mathbf{n}}-\mathbf{d}\cdot \hat{\mathbf{n}}'=\mathbf{d}\cdot(\hat{\mathbf{n}}-\hat{\mathbf{n}}')$. This must be equal to
$$\mathbf{d}\cdot(\hat{\mathbf{n}}-\hat{\mathbf{n}}')=m\lambda$$
Multiplying both sides by $2\pi/\lambda$ yields
$$\mathbf{d}\cdot(\mathbf{k}-\mathbf{k}')=2\pi m$$
If we extend to an array of scatterers, at points of the Bravais lattice a distance $\mathbf{R}$ apart, the condition becomes
$$\mathbf{R}\cdot(\mathbf{k}-\mathbf{k}')=2\pi m$$
But this is identical to the definition of the [[reciprocal lattice]] vectors (since the [[scalar product]] is commutative). We therefore have that the difference $\mathbf{k}-\mathbf{k}'$ must be a reciprocal lattice vector. In other words, the **von Laue condition** states that constructive interference occurs when the difference between scattered wavevectors is a reciprocal lattice vector.

It is useful to have an alternate version of this condition that only mentions the incident wavevector $\mathbf{k}$. Since the reciprocal lattice is itself a Bravais lattice, if $\mathbf{k}-\mathbf{k}'$ is a lattice vector, then so is $\mathbf{k}'-\mathbf{k}$. If we call the latter $\mathbf{K}$, then the condition or $\mathbf{k}$ and $\mathbf{k}'$ to have the same magnitude is
$$k=\lvert \mathbf{k}-\mathbf{K} \rvert $$
Squaring both sides yields
$$\mathbf{k}\cdot \hat{\mathbf{K}}=\frac{1}{2}K$$
That is to say, the component of the incident wavevector along the reciprocal lattice vector must be half the length of $K$. This can be seen geometrically as follows: $\mathbf{k}$ satisfies the von Laue condition if and only if the tip of $\mathbf{k}$ lies in a plane that perpendicularly splits the space between the origin of the reciprocal lattice and a lattice point $\mathbf{K}$ in half. In other words, imagine the vector $\mathbf{K}$, then a plane normal to $\mathbf{K}$. Place the plane half-way through $\mathbf{K}$: that's the plane the wavevector's tip must lie in. These are called **Bragg planes**.

:::image
![[Bragg planes.png]]
From *Ashcroft and Mermin, Chapter 6*.
:::

Another related visualization is the **Ewald sphere**. Consider a vector $\mathbf{k}$, then draw a sphere centered in $\mathbf{k}$ and with radius equal to $k$, so that it passes through the origin of the reciprocal lattice. The only wavevectors $\mathbf{k}'$ that can satisfy the von Laue conditions are those that start from a point on the sphere and also end in $\mathbf{k}$. Alternatively, the only vectors $\mathbf{K}$ that satisfy it are those that start from the origin and end on a point on the sphere. The radius of this sphere is representative of the energy of absorbed and emitted photons.

:::image
![[Ewald sphere.png]]
From *Ashcroft & Mermin, Chapter 6*.
:::
### Diffraction from a basis
For now we've only talked about pure Bravais lattices. Many crystals however also require a basis to fully describe their structure, such as diamond which needs a two point basis. These points, ions, will of course be responsible for the diffraction peaks that are seen in the real world, so we need some way of quantifying this influence.
#### Geometrical structure factor
Consider a basis on $n$ points $\mathbf{d}_{1},\ldots,\mathbf{d}_{n}$, all representing the same atomic species. Say a Bragg peak is associated with the reciprocal vector $\mathbf{K}=\mathbf{k}'-\mathbf{k}$. Then, the [[phase]] difference generated by two atoms of the same basis is given by their distance, $\mathbf{K}\cdot(\mathbf{d}_{i}-\mathbf{d}_{j})$ and the [[Wave equation|amplitudes]] of the reflections will have a phase difference of $e^{i\mathbf{K}(\mathbf{d}_{i}-\mathbf{d}_{j})}$. The amplitudes of the scattered rays must hence be $e^{i\mathbf{K}\cdot \mathbf{d}_{i}},\ldots,e^{i\mathbf{K}\cdot \mathbf{d}_{j}}$, and their total contribution over the entire primitive cell is their sum:
$$S_{\mathbf{K}}=\sum_{j=1}^{n} e^{i\mathbf{K}\cdot \mathbf{d}_{j}}$$
This is known as the **geometrical structure factor** and essentially describes how much the interference between rays reflected by atoms of the basis can diminish the [[irradiance|intensity]] of the diffraction associated with $\mathbf{K}$. The intensity is related to the square of the amplitude, so the actual contribution to intensity is $\lvert S_{\mathbf{K}} \rvert^{2}$. This makes the particular case of $S_{\mathbf{K}}=0$ especially interesting to look for, since in this case, intensity is completely snuffed out and Bragg reflection just *isn't there*.
#### Atomic form factor
Now, the above works if all the ions in the basis are the same, but what if they aren't? In that case, the sum becomes
$$S_{\mathbf{K}}=\sum_{j=1}^{n} f_{j}(\mathbf{K})e^{i\mathbf{K}\cdot \mathbf{d}_{j}}$$
where $f_{j}(\mathbf{K})$ is a quantity known as the **[[form factor|atomic form factor]]**, which is an intrinsic property of the ion itself. Same ions have the same form factor regardless of where they are in the lattice. It quantifies the amplitude of the radiation that is scattered by the ion. The name comes from the fact that it depends on the shape (form) of the [[electron]] cloud surrounding the ion and in fact is generally taken to be proportional to the [[Trasformata di Fourier|Fourier transform]] of the electron charge distribution.

[^1]: In purely mathematical terms, the "crystal structure" would be (quite creatively) called a **lattice with a basis**.

[^2]: It would take much longer to have a fully general description of their nature, at least until the development of [[Particella|particle]] physics; see [[Range]] for more.

[^3]: An approximation, but nonetheless a good one. In practice, the bulk of radiation is elastically scattered.
