---
wiki-publish: true
---
**Mass spectrometry** is a high-precision technique (about $10^{-6}$ [[atomic mass unit|atomic mass units]]) for measuring the [[mass]] of an [[atom]] or [[ion]]. The instrument itself is called a **mass spectrometer**. It was the first experimental technique to permit measurements of this precision.
### Operation
A mass spectrometer traditionally consists of three components: an *ion source* and two *selectors*.

![[Schematic Mass spectrometer|80%|center]]

The *ion source* is where the ion that need to measured come from. A simple source is, for example, a block of pure chemical element (e.g. iron, silver, etc.) bombarded by a beam of [[Electron|electrons]] to in order to produce free ions.

The beam produced by the source is then aimed at the first selector: a *velocity selector*. This is a component that contains perpendicular [[electric field|electric]] and [[magnetic field|magnetic fields]]. The electric field $\mathbf{E}$ enacts a [[Lorentz force]] $qE$ pushing the ions toward one end of the selector; the magnetic field $\mathbf{B}_{1}$ enacts another force $qvB_{1}$ toward the other end. The idea here is that all ions have the same [[electric charge]] $q$ (in theory, at least), but their velocities follow a [[probability distribution]]. This means that the electric force is the same for all of them, but the magnetic field changes. As such, the only ions that that will go straight, that is, those whose velocity is just right to balance out the opposing forces, are the only ones that'll make it through the selector. This velocity is given by
$$qE=qvB_{1} \quad\Rightarrow\quad v=\frac{E}{B_{1}}$$
so by modulating the ratio of electric-to-magnetic field, one can select for a specific velocity (up to a margin of error, of course).

Once the selected few ions make it through, they get into the second selector: the *[[Linear momentum|momentum]] selector*. This consists of a single uniform magnetic field that bends the beam into a circle of radius $r$ dependent on the momentum $p$ of the ion, such that
$$p=mv=qB_{2}r \quad\Rightarrow\quad m=\frac{qrB_{1}B_{2}}{E}$$
since $v=E/B_{1}$ from the velocity selector. Thus, if we can measure the curvature radius, we can get an estimate of mass. To do so, a [[Rivelatore]] plate is placed at an angle such that it detects the passing of an ion, from which we can measure the radius of curvature and finally get the mass.
### Measurements  
The high precision stems from using of well-known reference point for atomic mass. This is typically the mass of carbon-12:
$$m(\ce{^{12}C})=12.000\,000\ \text{u}$$
A method called the **mass doublet** is then employed. Instead of measuring an atom’s mass directly, one uses two [[molecule|molecules]] that differ by only one atom of interest, plus atoms of known mass. The molecular masses are then measured independently and the desired atomic mass is achieved by calculating the difference and, if necessary, removing extraneous masses theoretically. For example, to find the mass of hydrogen, it's possible to use the molecules $\text{C}_{9}\text{H}_{20}$ (*nonane*) and $\text{C}_{10}\text{H}_{8}$ (*naphthalene*). Their mass difference is[^1]
$$\Delta=m(\text{C}_{9}\text{H}_{20})-m(\text{C}_{10}\text{H}_{8})=12\,m(^{1}\text{H})-m(^{12}\text{C})$$
which is empirically measured to be
$$\Delta=0.093\ 900\ 32\pm 0.000\ 000\ 12\text{ u}$$
Since the mass of carbon-12 is known, the hydrogen mass ends up being
$$m(^{1}\text{H})=\frac{1}{12}\!\left[m(^{12}\text{C})+\Delta\right]=1.007\ 825\ 03\pm0.000\,000\,01\ \text{u}$$
This is extremely close to the modern value for hydrogen, which you can find on the [CIAAW](https://www.ciaaw.org/hydrogen.htm) website.

The benefit of this method is that it is a virtuous cycle, in the sense that the more high-precision atomic weights we know, that more creative we can get in atom and molecule choices since we can handle more and more weight differences theoretically. For example, in the [[nuclear scattering]]
$$\ce{^{1}H}+\ce{^{14}N}\rightarrow\ce{^{12}N}+\ce{^{3}N}$$
if the masses of $^{1}\text{H}$, $^{14}\text{N}$, and $^{3}\text{H}$ are known, the mass of $^{12}\text{N}$ can be extracted simply by equating the [[relativistic energy]] before and after:
$$E_{^{1}\text{H}}+E_{^{14}\text{N}}=E_{^{12}\text{N}}+E_{^{3}\text{H}},$$
This is particularly useful for unstable [[Nuclide|nuclides]] whose [[mean lifetime]] is too short to survive the whole spectrometer run (as is the case for $^{12}\text{N}$).
### Isotopic abundances  
A mass spectrometer is also useful to measure the relative abundances of [[Isotope|isotopes]] of an element by replacing the sensor plate with exit slits and scanning the mass range while varying the electric and magnetic fields. A common application is measuring the Solar-System abundances.

[^1]: Technically we're missing molecular [[binding energy]], but it is so small that it is negligible even within very high precision error margins like $\sim10^{-9}\text{ u}$.