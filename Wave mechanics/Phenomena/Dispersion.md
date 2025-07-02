---
wiki-publish: true
aliases:
  - dispersive
  - dispersion relation
---
**Dispersion** is the phenomenon where the [[phase velocity]] $v_{p}$ of a [[wave]] is dependent on the [[frequency]] $\omega$ of the wave, $v_{p}\equiv v_{p}(\omega)$. This phenomenon depends on the nature of the medium the wave is traveling in. A medium that exhibits dispersion is said to be **dispersive**. In other words, dispersion occurs when the individual components of a wave's [[Fourier series]] (or [[Fourier transform]]) propagate at different speeds. As such, [[Frequency|monochromatic waves]] cannot show dispersion, as they're made up of only a single frequency.

In dispersive media, it is useful to analyze the relation between the [[Wavenumber|wavevector]] $\mathbf{k}$ and the angular frequency $\omega$, which is called the **dispersion relation** $\omega(k)$[^1]. In nondispersive media, the dispersion relation is always
$$\omega=v_{p}k$$
where $v_{p}$ is the phase speed. In dispersive media, the relation must be nonlinear
$$\omega=v_{p}(\omega)k$$
You can prove this is always nonlinear with some algebra. Just move the speed to the left to get $\omega/v_{p}(\omega)=k$, then invert $v_{p}(\omega)$ to $\omega(v_{p})$. This gets you $\omega/\omega(v_{p})\propto k$ (we are left with proportionality because we don't know what comes out of the inversion). Assume for instance that $\omega(v_{p})\propto \omega^{p}$ for some $p$. Then $\omega/\omega^{p}\propto k$. This is manifestly nonlinear unless $p=0$, in which case $v_{p}$ wouldn't depend on $\omega$ in the first place.

As an example, in regular glass the phase speed of an [[electromagnetic wave]] is $v_{p}=c/n$, where $c$ is the [[speed of light]] and $n$ is the [[refractive index]]. It is well-known that $n$ is frequency dependent in glass (think of the classic prism that turns a beam of light into a rainbow), so the dispersion relation is
$$v_{p}(\omega)=\frac{c}{n(\omega)}\quad\Rightarrow \quad\omega=\frac{c}{n(\omega)}k$$
which is nonlinear[^2]. Now, it should be noted that relations like this one, they *are* linear if you set a specific value of $\omega$, that is, if you're working with monochromatic waves. However, this is more of a consequence of dispersion not applying to monochromatic waves than something about the material specifically. Other dispersion relations are entirely nonlinear regardless of whether you are working with monochromatic waves or not, such as some [[Wave guide|wave guides]] or [[plasma]] which behave like $\omega \propto \sqrt{ k }$.

Dispersion causes waves to change their profile over time while traveling through dispersive media, usually by spreading out ("dispersing"). This is most obvious when analyzing [[wave packet|wave packets]], localized waveforms with a "shape". The outer profile of a wave packet, the **envelope**, moves at a different speed than each individual sinusoidal component of the wave's [[Fourier series]], which is called the **[[group velocity]]**
$$v_{g}=\frac{ \partial \omega }{ \partial k } $$
In nondispersive media, this is manifestly equal to the phase speed. In fact, you can alternatively define dispersion as occurring when phase speed and group speed do not coincide.

[^1]: You can also write this as $v_{p}(\omega)$, hence the definition. However, in physics the phase speed of a wave is often not very important, whereas the angular frequency and wavevector are. This is most evident in quantum mechanics due to the [[Planck formula]] giving [[energy]] from frequency.

[^2]: You can rerun the argument above if you want to check: move $n$ to the left to get $n(\omega)\omega=ck$, then invert to $\omega(n)\omega\propto ck$. Assume generically $\omega(n)\propto \omega^{p}$ for some $p$, then $\omega^{p+1}\propto ck$. Clearly nonlinear unless $p=0$, in which $n$ would be independent of $\omega$.
