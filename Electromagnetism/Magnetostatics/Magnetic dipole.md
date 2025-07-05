---
wiki-publish: true
---
A **physical magnetic dipole** is a tiny [[electric current]] loop. If the size of the loop is infinitesimal, it is called a **perfect magnetic dipole**. They are characterized by a [[magnetic dipole moment]]. The electric analog is the [[electric dipole]].
### Under a magnetic field
Consider a rectangular magnetic dipole of sides $a$ and $b$ subject to a uniform [[magnetic field]] $\mathbf{B}$. Any loop can be built up from an infinite number of arbitrarily small rectangles (a [[Riemann sum]]), so this discussion can be extended without loss of generality to any shape of the loop. For simplicity, center the loop at the origin and, using [[Cartesian coordinates]], tilt the loop by an angle $\theta$ from the $z$ axis towards the $y$ axis. Let $\mathbf{B}$ be in the $z$ direction.

![[Schema Magnetic dipole rotation|100%]]

The forces on the sloping sides cancel out (they stretch the loop, but they don't rotate it). The forces horizontal to the loop $\mathbf{F}$ also cancel each other out linearly, but not rotationally. They apply a moment of force
$$\mathbf{N}=aF\sin \theta\ \hat{\mathbf{x}}$$
The magnitude of these forces is
$$F=IbB$$
and therefore
$$\mathbf{N}=IabB\sin \theta\ \hat{\mathbf{x}}=mB\sin \theta\ \hat{\mathbf{x}}$$
or
$$\boxed{\mathbf{N}=\mathbf{m}\times \mathbf{B}}$$
where $m=Iab$ is the magnetic dipole moment. This moment of force is exact on any magnetic dipole if the field is uniform. If it is not uniform, it is exact only for perfect dipoles, which have no spatial extension and therefore ignore the fact that it's not uniform.

This torque tends to align the dipole in the direction of the magnetic field and accounts for [[Paramagnet|paramagnetism]]. It might seem then that paramagnetism is the only form of magnetism, as there's nothing here to account for the existence of a [[diamagnet]]. However, the magnetic dipole in matter is given by [[spin|spinning]] [[Elettrone|electrons]] and these, due to the [[Pauli exclusion principle|Pauli exclusion principle]], tend to pair up with electrons of opposite spin, canceling each other out magnetically. Thus, this rotation is only observed in [[Atom|atoms]] with odd number of electrons. Even here, the alignment can be broken by thermal collisions.

If the field is uniform, the force over the current loop is zero:
$$\mathbf{F}=I\oint d\mathbf{I}\times \mathbf{B}=I\left( \oint \mathbf{dI} \right)\times \mathbf{B}=\mathbf{0}$$
but if the field is non-uniform, for a perfect dipole of magnetic moment $\mathbf{m}$ we have
$$\boxed{\mathbf{F}=\nabla(\mathbf{m}\cdot \mathbf{B})}$$
### Radiation
If the current going through the loop is alternating, the dipole moment becomes variable. The magnetic field starts to change, inducing an [[electric field]] and emitting of [[electromagnetic radiation]].

For a simple model, let's assume the dipole is a circular loop of radius $b$ and that the current is alternating in a sinusoidal fashion at [[Frequency|angular frequency]] $\omega$:
$$I(t)=I_{0}\cos(\omega t)$$
The dipole moment becomes
$$\mathbf{m}(t)=\pi b^{2}I(t)\hat{\mathbf{z}}=m_{0}\cos(\omega t)\hat{\mathbf{z}}$$
by setting the dipole axis on the $z$ axis and calling $m_{0}\equiv \pi b^{2}I_{0}$.
#### Potentials
We want to find the [[retarded potentials]]. We do so in a very similar manner as [[Electric dipole#Potentials]]. The loop has no [[electric charge]], so very simply
$$\boxed{V=0}$$
Due to the current we have
$$\mathbf{A}(\mathbf{r},t)=\frac{\mu_{0}}{4\pi}\oint_{\gamma} \frac{I_{0}\cos\left( \omega\left( t- \frac{\mathfrak{r}}{c} \right) \right)}{\mathfrak{r}}d\mathbf{I}'$$

![[Diagram Magnetic dipole radiation]]


For a point $\mathbf{r}$ above the $x$ axis, $\mathbf{A}$ must aim in the $y$ direction, since the $x$ component is canceled by equal contributions from both sides of the $x$ axis, so
$$\mathbf{A}(\mathbf{r},t)=\frac{\mu_{0}I_{0}b}{4\pi}\hat{\mathbf{y}}\int_{0}^{2\pi} \frac{\cos\left[ \omega\left( t- \frac{\mathfrak{r}}{c} \right) \right]}{\mathfrak{r}}\cos \phi'd\phi'$$
where $\cos \phi'$ picks out the $y$ component of $d\mathbf{I}'$. Using the [[law of cosines]]
$$\mathfrak{r}=\sqrt{ r^{2}+b^{2}-2rb\cos \psi }$$
Since $\psi$ is the angle between $\mathbf{r}$ and $\mathbf{b}$, we have the [[scalar product]] $rb\cos \psi=\mathbf{r}\cdot \mathbf{b}=rb\sin \theta \cos \phi'$, since
$$\mathbf{r}=r\sin \theta\ \hat{\mathbf{x}}+r\cos \theta\ \hat{\mathbf{y}},\qquad \mathbf{b}=b\cos \phi'\ \hat{\mathbf{x}}+b\sin \phi'\ \hat{\mathbf{y}}$$
The law of cosines then becomes
$$\mathfrak{r}=\sqrt{ r^{2}+b^{2}-2rb\sin \theta \cos \phi' }$$
We now make the perfect dipole approximation
$$b\ll r\tag{Perfect dipole approximation}$$
which means that the loop is very small compared to the distances we're studying. We can then state
$$\mathfrak{r}=r^{2}\sqrt{ 1- 2 \frac{b}{r}\sin \theta \cos \phi'+ \frac{b^{2}}{r^{2}} }$$
$b^{2}/r^{2}$ is negligible to first order. The rest can be rewritten using the [[Binomial theorem|binomial expansion]] to first order:
$$\mathfrak{r}\simeq r^{2}\left( 1- \frac{b}{r}\sin \theta \cos \phi' \right)$$
The cosine in the integral can then be rewritten as
$$\begin{align}
\cos\left[ \omega\left( t- \frac{\mathfrak{r}}{c} \right) \right]&\simeq \cos\left[ \omega\left( t- \frac{r}{c} \right)+ \frac{\omega b}{c}\sin \theta \cos \phi' \right] \\
&=\cos\left[ \omega\left( t- \frac{r}{c} \right) \right]\cos\left( \frac{\omega b}{c}\sin \theta \cos \phi' \right) \\
&\qquad-\sin\left[ \omega\left( t- \frac{r}{c} \right) \right]\sin\left( \frac{\omega b}{c}\sin \theta \cos \phi' \right) \\
&=\ldots
\end{align}$$
using $\cos(\alpha+\beta)=\cos \alpha \cos \beta-\sin \alpha \sin \beta$. We now make the second approximation:
$$b\ll \lambda\sim \frac{c}{\omega}\tag{Large wavelength approximation}$$
With this we can truncate the [[sine and cosine series]] to first order:
$$\frac{\omega b}{c}\ll 1\quad\Rightarrow \quad \cos\left( \frac{\omega b}{c}\sin \theta \cos \phi' \right)\simeq 1,\qquad \sin\left( \frac{\omega b}{c}\sin \theta \cos \phi' \right)\simeq \frac{\omega b}{c}\sin \theta \cos \phi'$$
and so
$$\ldots=\cos\left[ \omega\left( t- \frac{r}{c} \right) \right]- \frac{\omega b}{c}\sin \theta \cos \phi'\sin\left[ \omega\left( t- \frac{r}{c} \right) \right]$$
Using this result and
$$\frac{1}{\mathfrak{r}_{\pm}}\simeq \frac{1}{r}\left( 1\pm \frac{b}{r}\sin \theta \cos \phi' \right)$$
we can compute the integral:
$$\begin{align}
\mathbf{A}(\mathbf{r},t)&\simeq \frac{\mu_{0}I_{0}b}{4\pi r}\hat{\mathbf{y}}\int_{0}^{2\pi}\Big[ \cos\left[ \omega\left( t- \frac{r}{c} \right) \right]+  \\
&\qquad \qquad \quad +b\sin \theta \cos \phi'\left( \frac{1}{r}\cos\left[ \omega \left( t- \frac{r}{c} \right) \right]- \frac{\omega}{c}\sin\left[ \omega\left( t- \frac{r}{c} \right) \right] \right) \Big]\cos \phi'd\phi'
\end{align}$$
The first term integrates to zero, since
$$\cos\left[ \omega\left( t- \frac{r}{c} \right) \right]\int_{0}^{2\pi}\cos \phi'd\phi'=0$$
The second and third terms both involve $\cos ^{2}\phi'$:
$$\frac{b}{r}\sin \theta \cos\left[ \omega\left( t- \frac{r}{c} \right) \right]\underbrace{ \int_{0}^{2\pi}\cos ^{2}\phi'd\phi' }_{ \pi }=\frac{\pi b}{r}\sin \theta \cos\left[ \omega\left( t- \frac{r}{c} \right) \right]$$
and
$$\frac{b\omega}{c}\sin \theta \sin\left[ \omega\left( t- \frac{r}{c} \right) \right]\underbrace{ \int_{0}^{2\pi}\cos ^{2}\phi'd\phi' }_{ \pi }=\frac{\pi b\omega}{c}\sin \theta \sin\left[ \omega\left( t- \frac{r}{c} \right) \right]$$
Putting them all together, while noticing that $\mathbf{A}$ points in the $\hat{\boldsymbol{\phi}}$ direction, gives
$$\mathbf{A}(r,\theta,t)=\frac{\mu_{0}m_{0}}{4\pi r}\sin \theta\left[ \frac{1}{r}\cos\left[ \omega\left( t- \frac{r}{c} \right) \right]- \frac{\omega}{c}\sin\left[ \omega\left( t- \frac{r}{c} \right) \right] \right]\hat{\boldsymbol{\phi}}$$
In the static limit, when $\omega=0$, we get the usual
$$\mathbf{A}(r,t)=\frac{\mu_{0}}{4\pi} \frac{m_{0}\sin \theta}{r^{2}}\hat{\boldsymbol{\phi}}$$
In the radiation zone
$$r\gg \frac{c}{\omega} \quad\text{or equivalently}\quad r\gg \lambda\tag{Far field approximation}$$
the first term is $\sim r^{-2}$, so it is negligible and we get
$$\boxed{\mathbf{A}(r,\theta,t)=- \frac{\mu_{0}m_{0}\omega}{4\pi cr}\sin \theta \sin\left[ \omega\left( t- \frac{r}{c} \right) \right]\hat{\boldsymbol{\phi}}}$$
#### Fields
Since $\nabla V=0$, the fields are quite simple:
$$\boxed{\mathbf{E}(r,t)=-\frac{ \partial \mathbf{A} }{ \partial t } =\frac{\mu_{0}m_{0}\omega ^{2}}{4\pi cr}\sin \theta \cos\left[ \omega\left( t- \frac{r}{c} \right) \right]\hat{\boldsymbol{\phi}}}$$
and
$$\boxed{\mathbf{B}(r,t)=\nabla\times \mathbf{A}=- \frac{\mu_{0}m_{0}\omega ^{2}}{4\pi c^{2}r}\sin \theta \cos\left[ \omega\left( t- \frac{r}{c} \right) \right]\hat{\boldsymbol{\theta}}=- \frac{1}{c}\hat{\mathbf{r}}\times \mathbf{E}}$$
where the far field approximation is used to calculated $\mathbf{B}$. Like the electric dipole case, the fields are in [[phase]], mutually [[Orthogonality|perpendicular]] and transverse. The ratio of their [[amplitude|amplitudes]] is exactly the [[speed of light]]: $E_{0}/B_{0}=c$.
#### Electromagnetic waves
These fields produce [[Electromagnetic wave|electromagnetic waves]] of angular frequency $\omega$. Since they are created from a point source, they are [[spherical wave|spherical waves]].

We can quantify the energy emitted by the oscillating dipole by starting from the [[Poynting vector]]:
$$\mathbf{S}(\mathbf{r},t)=\frac{1}{\mu_{0}}(\mathbf{E}\times \mathbf{B})=\frac{\mu_{0}}{c}\left[ \frac{m_{0}\omega ^{2}}{4\pi cr} \sin\theta\cos\left[ \omega\left( t- \frac{r}{c} \right) \right] \right]^{2}\hat{\mathbf{r}}$$
The [[irradiance]] is the magnitude of the time average of the Poynting vector over a full oscillation:
$$I=\lvert \langle \mathbf{S} \rangle \rvert =\frac{\mu_{0}m_{0}^{2}\omega^{4}}{32\pi ^{2}c^{3}} \frac{\sin^{2}\theta}{r^{2}}$$
Like the electric dipole, the irradiance is dependent on the angle and makes a [[torus]] shape, with no emission on the axis and maximum emission perpendicular to the axis. The average [[radiant power]] is
$$\langle P \rangle =\frac{\mu_{0}m_{0}^{2}\omega^{4}}{12\pi c^{3}}$$
Compared to the electric dipole however, a magnetic dipole emits far less energy. We can see this by comparing powers:
$$\frac{P_\text{magnetic}}{P_\text{electric}}=\left( \frac{m_{0}}{p_{0}c} \right)^{2}$$
Since by definition $m_{0}=\pi b^{2}I_{0}$ and $p_{0}=q_{0}d$ this is equal to, when setting $d=\pi b$ for comparison,
$$\frac{P_\text{magnetic}}{P_\text{electric}}=\left( \frac{\omega b}{c} \right)^{2}$$
This is precisely the quantity that we assumed was small in the large wavelength approximation, and it is *squared*. This means that the electric power output is enormously greater than the magnetic one and will pretty much always drown it out. The only cases in which it appears are when the system is specifically designed to only emit magnetic dipole radiation, such as the in the pure magnetic dipole itself.