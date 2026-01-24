---
wiki-publish: true
---
This experiment measures the [[electron]]'s [[Electric charge|charge]] to [[mass]] ratio $e/m_{e}$ by determining the exact [[Electric field|electric]] and [[Magnetic field|magnetic fields]] that, when applied to a straight beam of electrons, cancel each other's force out and cause no net variation. Since the force depends on the charge-mass ratio, it can be indirectly measured by finding when the fields cancel each other's effects out. The experiment is similar in principle to [[Thomson's experiment]] and the [[electron charge-mass ratio with thin beam]] experiment, but the theory behind is more elegant, at the cost of being more difficult to get precise and accurate results out of.

The experiment employs a [[Braun tube]], which is the first historical form of the [[cathode ray tube]]. It's a vacuumed glass tube with an electron blaster on the smaller end, aimed straight through the tube. Not far after the blaster, a set of metallic plates creates a parallel plate [[capacitor]] with a controllable electric field. An additional magnetic field must be created externally for the experiment to work, for instance by placing two magnetic coils surrounding the tube. The two fields must be [[Orthogonality|orthogonal]] to each other and to the trajectory of the electron beam, which passes through the capacitor. This geometry is chosen to simplify the calculations, as it allows us to not worry about angles of incidence. The [[Lorentz force]] is
$$\mathbf{F}=e[\mathbf{E}+\mathbf{v}\times \mathbf{B}]$$
By picking opportune fields, we can nullify the force. This occurs when
$$0=e[\mathbf{E}+\mathbf{v}\times \mathbf{B}]\quad\Rightarrow \quad \mathbf{E}=-\mathbf{v}\times \mathbf{B}\tag{1}$$
$\mathbf{v}$ is the velocity of an electron when entering the space between the capacitor plates. This is under the assumption that the local ambient magnetic field can be ignored, either because it's below error margin or some other scheme to cancel its effect, such as by aligning the beam with the ambient field's field lines to cancel its $\mathbf{v}\times \mathbf{B}_\text{local}$ term. It also requires being able to ignore fringe effects on the capacitor's edges, which is no easy task, but is nevertheless crucial to get an accurate measurement.

Measuring the point in which the two fields cancel each other out requires some way to track the electrons' trajectory. In a typical cathode ray tube, the far end of the tube from the blaster is coated in a fluorescent material that glows when electrons collide with it. Using this screen, one can track the trajectory by seeing where the glowing spot is on the screen. The fields successfully cancel when the spot is in the same place is it would be if there were fields from the plates.

Being a simple parallel plate capacitor, we can express the electric force's action in terms of its [[electric potential]] $V_\text{cap}$ as
$$\lvert \mathbf{E} \rvert =\frac{V_\text{cap}}{D}\tag{2}$$
where $D$ is the distance between the capacitor's plates. $D$ is chosen by the capacitor manufacturer and is constant, whereas $V_\text{cap}$ is chosen in the lab through a laboratory power supply or some other similar tool. With this, we can take $(1)$, recall that $\mathbf{E}$ and $\mathbf{B}$ are orthogonal by construction to express it in scalar form $E=-vB$ and then mix it with $(2)$ to get
$$\frac{V_\text{cap}}{D}=-vB$$
The speed $v$ of the electron is given by the force it was subject to as it came out of the blaster. The blaster's force is itself due to own electric potential $V_\text{blast}$, which is related to the [[kinetic energy]] by
$$\frac{1}{2}m_{e}v^{2}=eV_\text{blast}\quad\Rightarrow \quad v^{2}=\frac{2eV_\text{blast}}{m_{e}}$$
Extracting $v$ out of the previous equation, squaring it and equating it with this one yields
$$\frac{V_\text{cap}^{2}}{D^{2}}=\frac{2eV_\text{blast}}{m_{e}}B^{2}$$
and hence
$$\boxed{\frac{e}{m_{e}}=\frac{V_\text{cap}^{2}}{2D^{2}V_\text{blast}B^{2}}}$$
This is our experimental relation. All quantities on the right hand side can be empirically determined:
- $V_\text{blast}$ is chosen manually to power the blaster.
- $V_\text{cap}$ is chosen manually to power the capacitor's electric field.
- $D$ is chosen by the instrument's manufacturer.
- $B$ depends on the specifics of the instrument used to generate it. If the details are known and simple, it can be calculated analytically, or it can be measured with a [[Hall effect]] sensor.

The greatest obstacle to a good measurement in this experiment is guaranteeing an accurate confinement of the magnetic field to just the space between the capacitor plates. Given how difficult magnetic fields are to contain, it is likely to be the largest source of systematic errors in the measurement.