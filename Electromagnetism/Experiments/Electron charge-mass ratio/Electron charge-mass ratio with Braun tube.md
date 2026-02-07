---
wiki-publish: true
---
This experiment measures the [[electron]]'s [[Electric charge|charge]] to [[mass]] ratio $e/m_{e}$ by determining the exact [[Electric field|electric]] and [[Magnetic field|magnetic fields]] that, when applied to a straight beam of electrons, cancel each other's force out and cause no net variation. Since the force depends on the charge-mass ratio, it can be indirectly measured by finding when the fields cancel each other's effects out. The experiment is similar in principle to the [[electron charge-mass ratio with thin beam]] experiment, but the theory behind is more elegant, at the cost of being more difficult to get precise and accurate results out of.

The experiment employs a [[Braun tube]], which is one of the first historical forms of the [[cathode ray tube]]. The function and structure is largely the same: an [[electron gun]] on the small end of an evacuated glass tube shoots an electron beam at a [[fluorescence|fluorescent]] screen on the larger end, which marks the point of collision of the beam. A single parallel plate [[capacitor]] placed in front of the gun allows the creation of a controllable electric field to deflect the beam. Unlike more modern CRTs, there is only one deflecting capacitor in a Braun tube, so it can only deflect on one axis. This is by design, as the second axis of deflection is controlled through an external magnetic. This needs to be created through an external apparatus, such as two Helmholtz coils surrounding the tube.

The two fields are intended to be [[Orthogonality|orthogonal]] to both each other and the trajectory of the electron beam. This geometry is chosen to simplify the calculations, as it allows us to not worry about angles of incidence. The [[Lorentz force]] is
$$\mathbf{F}=e(\mathbf{E}+\mathbf{v}\times \mathbf{B})$$
By picking opportune fields, we can nullify the force. This occurs when
$$0=e(\mathbf{E}+\mathbf{v}\times \mathbf{B})\quad\Rightarrow \quad \mathbf{E}=-\mathbf{v}\times \mathbf{B}\tag{1}$$
$\mathbf{v}$ is the velocity of an electron when entering the space between the capacitor plates. This is under the assumption that the local ambient magnetic field can be ignored, either because it's below margin of error or due to some scheme to cancel its effect, such as by aligning the beam with the ambient field's field lines to cancel its $\mathbf{v}\times \mathbf{B}_\text{local}$ term. It also requires that the electric and magnetic fields affect the same region of space: this no easy task and is the biggest problem point of the experiment, as it can have a significant impact on the measurements. More on this later.

Measuring the point in which the two fields cancel is done by looking at the glowing dot on the screen. The fields successfully cancel when the dot is in the same place is it would be if there were fields from the plates. In practice, you turn on the electron gun without any deflection, mark where the beam lands, then try to reproduce that spot with the fields active.

The deflecting electric field can be expressed in terms of its [[electric potential]] $V_\text{def}$ as
$$\lvert \mathbf{E} \rvert =\frac{V_\text{def}}{d}\tag{2}$$
where $d$ is the distance between the capacitor's plates. With this, we can take $(1)$, recall that $\mathbf{E}$ and $\mathbf{B}$ are orthogonal by construction to express $(1)$ in scalar form, $E=-vB$, and then equate it with $(2)$ to get
$$\frac{V_\text{def}}{d}=-vB\tag{3}$$
The speed $v$ of the electron is determined by the potential $V_\text{acc}$ of the electron gun, which is related to the [[kinetic energy]] by
$$\frac{1}{2}m_{e}v^{2}=eV_\text{acc}\quad\Rightarrow \quad v^{2}=\frac{2eV_\text{acc}}{m_{e}}$$
Extracting $v$ out of $(3)$, squaring it and equating it with the previous one yields
$$\frac{V_\text{def}^{2}}{d^{2}}=\frac{2eV_\text{acc}}{m_{e}}B^{2}$$
and hence
$$\boxed{\frac{e}{m_{e}}=\frac{V_\text{def}^{2}}{2d^{2}V_\text{acc}B^{2}}}$$
This is our experimental relation. All quantities on the right hand side can be empirically determined:
- $V_\text{acc}$ is chosen manually to power the electron gun.
- $V_\text{def}$ is chosen manually to power the deflecting capacitor's electric field.
- $d$ is chosen by the instrument's manufacturer and it's either in the Braun tube's manual or can be measured with a ruler or with a [[caliper]].
- $B$ depends on the specifics of the instrument used to generate it. If the details are known and simple, it can be calculated analytically, or it can be measured with a [[Hall effect]] sensor.

A few notes:
- The quality of the measurements rests on how clear the spot on the screen is. Strong electron beams will excite the screen more, making a strong glow and therefore making it more difficult to pinpoint where exactly the center is. Moreover, high deflections will cause the beam to hit the screen at a strong angle, which will distort the spot from a nice [[circle]] to an [[ellipse]]. Avoid using excessively strong fields.
- Being a CRT, the Braun tube probably has a beam collimator before the accelerator anode. You should tweak the potentials to focus the beam into as fine of a spot as you can.
- The greatest obstacle to a good measurement in this experiment is guaranteeing an accurate confinement of the magnetic field to just the space between the capacitor plates. Given how difficult magnetic fields are to contain, it is likely that the region of the magnetic field will be considerably larger than that of the electric one. This is not intended according to the theory, so this *will* give bad measurements, specifically overestimates of $e/m_{e}$. It is likely to be the largest source of [[systematic error|systematic errors]] in the experiment, so make sure you are aware of it.