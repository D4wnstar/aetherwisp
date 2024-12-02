> [!success] Esame
> Questo esperimento può essere fatto per l'esame di Lab 2.

This experiment uses [[Lenz's law]] to determine the local [[magnetic field]].
### Theory
The Earth's magnetic field is on the order of $\sim 10^{-5}\text{ T}$.

![[Schema Earth magnetic field|center]]

Locally, the magnetic field is $\mathbf{B}_{L}$. It can be decomposed into two components in [[polar coordinates]], $\mathbf{B}_{\theta}$ and $\mathbf{B}_{r}$. These have formal expressions
$$B_{r}=\frac{\mu_{0}}{4\pi} \frac{2m\cos\theta}{R^{3}_{T}},\qquad B_{\theta}=\frac{\mu_{0}}{4\pi} \frac{2m\sin\theta}{R^{3}_{T}}$$
where $R_{T}$ is the radius of the Earth, $\mu_{0}$ is the [[permeability of free space]] and $m$ is the [[magnetic dipole moment]] of the Earth.
### Apparatus
The apparatus is a copper wire coiled many times in a loop mounted on an axis that can rotated manually through a crank. The construction is mostly made of plastic and non-magnetic metals, with only a few iron screws. The wire is coated in an insulator to make sure each loop of the wire does not conduct to the adjacent loops.

![[Drawing Local magnetic field apparatus|center]]

The wire has an ending that can connect to an oscilloscope.
### Method
The idea is to manually[^1] rotate the loop *at a constant speed* in order to produce a magnetic field from the coil through [[Lenz's law]]. This magnetic field then also induces a current through the coil because of [[self inductance]]. The current is then visualized in an oscilloscope.

We expect the [[Electromotive force|emf]] that we see due to induction to be periodic:
$$\mathcal{E}(t)=B_{L}n\omega(t)\pi R^{2}\sin \phi \sin \alpha \sin(\omega t)$$
with $n$ the number of wire loops, $R$ the radius of the coil and $\omega$ is the angular frequency of rotation (ideally constant). $\phi$ is the angle between the local magnetic field and normal vector of the coil surface. $\alpha$ is the angle between the local magnetic field and the axis of rotation of the coil.

In order to determine the direction of the local magnetic field, we can use the fact that if the axis of rotation $\alpha$ is parallel to the field, no field is induced as the magnetic flux does not vary. We can see this in the formula since if $\alpha=0$, $\sin \alpha=0$. To do this, we can take a measurement every 10 degrees or so for a full 180 degrees and figure out where the reading is smallest. We can put reference angles on the table to keep track of the orientation.

Once the direction is known, we can turn 90 degrees to instead maximize the induction. This gets rid of $\sin \alpha$.

To figure out the phase, we need to look at the initial acceleration, before $\omega$ becomes constant. At the start, the oscilloscope will something like either the blue or red signals:

![[Graph Local magnetic field initial oscilloscope reading|center]]

Whether the signal is the blue or red one determine the polarity of the magnetic field (i.e., where the north and south poles are).

The potential is going to be very small, in the tenths of a millivolt. This is unfortunate as the error margin is going to huge in comparison to the reading. As such, we make use of an amplifying filter to increase the potential. It contains a low-pass filter, which cuts out high frequencies to mostly remove the noise of the signal. The amplifier needs to be calibrated.

It may also be interesting to but the apparatus on its side and take measurements that way.

[^1]: We can't use a motor because electric motors produce considerable electric fields.