---
wiki-publish: true
---
A **physical electric dipole** is a system of two equal and opposite [[Electric charge|electric charges]] separated by a distance $d$. A **perfect electric dipole** is the limiting case when $d\to 0$. The magnetic analog is the [[magnetic dipole]].

:::image
![[VFPt_dipoles_electric.svg|400]]
By Geek3 - Own work, CC BY-SA 4.0, from [Wikipedia](https://commons.wikimedia.org/w/index.php?curid=85815210)
:::
### Potential
We can approximate the [[electric potential]] of an electric dipole for points far from it. Let $\mathfrak{r}_{-}$ be the distance from $-q$ and $\mathfrak{r}_{+}$ the distance from $+q$. Then
$$V(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\left( \frac{q}{\mathfrak{r}_{+}}- \frac{q}{\mathfrak{r}_{-}} \right)$$
Using the [[law of cosines]] we have
$$\mathfrak{r}_{\pm}^{2}=r^{2}+\left( \frac{d}{2} \right)^{2}\mp rd\cos \theta=r^{2}\left( 1\mp \frac{d}{r}\cos \theta+ \frac{d^{2}}{4r^{2}} \right)$$

```tikz
\begin{document}
\begin{tikzpicture}[domain=0:8]
\draw (0,0) -- (0,4);
\draw (0,4) -- (6,5);
\draw (0,0) -- (6,5);
\draw (0,2) -- (6,5);
\draw (0,2) node[anchor=east] {$d$};
\draw (2,3.2) node[anchor=east] {$\mathbf{r}$};
\draw (2,4.5) node[anchor=east] {${r}_{+}$};
\draw (2,0.9) node[anchor=east] {${r}_{-}$};
\draw (0.4,2.2) arc (0:89:12pt);
\draw (0.6,2.8) node[anchor=east] {$\theta$};
\fill[black] (0,0) circle (3pt) node[anchor=east] {$-q$};
\fill[black] (0,4) circle (3pt) node[anchor=east] {$+q$};
\fill[black] (6,5) circle (3pt);
\end{tikzpicture}
\end{document}
```

We're interested in what happens at $r\gg d$, so the the third term is negligible and the [[binomial theorem]] yields
$$\frac{1}{\mathfrak{r}_{\pm}}\simeq \frac{1}{r} \frac{1}{\sqrt{ 1\mp \frac{d}{r}\cos \theta }}\simeq \frac{1}{r}\left( 1\pm \frac{d}{2r}\cos \theta \right)$$
Thus
$$\frac{1}{\mathfrak{r}_{+}}- \frac{1}{\mathfrak{r}_{-}}\simeq \frac{d}{r^{2}}\cos \theta$$
and hence
$$V(\mathbf{r})\simeq \frac{1}{4\pi\varepsilon_{0}} \frac{qd\cos \theta}{r^{2}}\tag{1}$$
so the potential of a dipole goes like $\sim1/r^{2}$ at large enough distances and is therefore smaller than that of a point charge (which goes like $\sim1/r$). In fact, if we were to add more poles and get a quadrupole, it would go like $\sim 1/r^{3}$, an octopole would go like $\sim 1/r^{4}$ and so on.

A better description requires the use of [[multipole expansion]], in which terms beyond the dipole potential exist. The dipole term is
$$\boxed{V_\text{dip}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}} \frac{\mathbf{p}\cdot\hat{\mathbf{r}}}{r^{2}}}\tag{2}$$
where $\mathbf{p}$ is the [[electric dipole moment]]. For a physical dipole, it's simply $\mathbf{p}=q\mathbf{d}$, with $\mathbf{d}$ the vector that points from the negative pole to the positive one. The expansion reduces to $(1)$ when the distance $r$ is very high, but also when the distance $d$ between the poles is very small. In fact, to obtain a dipole whose potential is described exactly by $(2)$ and has no other terms, $d$ needs to approach zero. This scenario is called **perfect dipole** or **point dipole**. Of course, if $d$ goes to zero, then so does the entire potential. To retain the potential, the charge needs to go to infinity as $d$ goes down to counteract that.
### Electric field
Knowing the potential (mostly), we can now find the [[electric field]], at least that of a perfect dipole. Due to the origin-dependency of the dipole moment, we choose coordinates so that $\mathbf{p}$ is at the origin and points in the $z$ direction. This way, the potential is $(2)$. In [[Spherical coordinates]] it reads
$$V_\text{dip}(r,\theta)=\frac{1}{4\pi\varepsilon_{0}}\frac{\hat{\mathbf{r}}\cdot \mathbf{p}}{r^{2}}=\frac{1}{4\pi\varepsilon_{0}}\frac{p\cos \theta}{r^{2}}$$
(in these choice of coordinates, we have azimuthal symmetry). The negative [[Gradient]] is
$$\begin{align}
E_{r} & =-\frac{ \partial V }{ \partial r } =\frac{1}{4\pi\varepsilon_{0}} \frac{2\pi \cos \theta}{r^{3}} \\
E_{\theta} &= - \frac{1}{r}\frac{ \partial V }{ \partial \theta } =- \frac{1}{4\pi\varepsilon_{0}} \frac{p \sin \theta}{r^{3}} \\
E_{\phi} & =- \frac{1}{r\sin \theta}\frac{ \partial V }{ \partial \phi } =0
\end{align}$$
Thus
$$\boxed{\mathbf{E}_\text{dip}(r,\theta)=\frac{1}{4\pi\varepsilon_{0}} \frac{p}{r^{3}}(2\cos \theta\ \hat{\mathbf{r}}+\sin \theta\ \hat{\boldsymbol{\theta}})}$$
A more general, coordinate-free form can be derived by taking the gradient of the dipole potential directly:
$$\mathbf{E}_\text{dip}(\mathbf{r})=-\nabla V_\text{dip}(\mathbf{r})=- \frac{1}{4\pi \varepsilon_{0}} \nabla\left( \frac{\mathbf{p}\cdot \mathbf{r}}{r^{3}} \right)=- \frac{1}{4\pi \varepsilon_{0}}\left[ \frac{\nabla(\mathbf{p\cdot \mathbf{r}})}{r^{3}}-(\mathbf{p}\cdot \mathbf{r})\nabla\left( \frac{1}{r^{3}} \right) \right]$$
The first gradient is trivial, as $\mathbf{p}$ is constant and $\mathbf{r}=(x,y,z)$ is just what we are taking the derivative of, so $\nabla(\mathbf{p}\cdot \mathbf{r})=\mathbf{p}$[^1]. The second gradient is also easy, provided we use spherical coordinates:
$$\nabla\left( \frac{1}{r^{3}} \right)=\left( \frac{ \partial }{ \partial r } \frac{1}{r^{3}},0,0 \right)=\left( - \frac{3}{r^{4}},0,0 \right)=-3 \frac{\hat{\mathbf{r}}}{r^{4}}=-3 \frac{\mathbf{r}}{r^{5}}$$
Putting it all together yields
$$\boxed{\mathbf{E}_\text{dip}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}} \frac{1}{r^{3}}[3(\mathbf{p}\cdot \hat{\mathbf{r}})\hat{\mathbf{r}}-\mathbf{p}]}$$
Just like how the dipole term of potential goes like $\sim 1/r^{2}$ instead of $\sim 1/r$, the field goes like $\sim 1/r^{3}$ instead of $\sim 1/r^{2}$. Higher terms can be proven to go like $\sim 1/r^{4}$, $\sim 1/r^{5}$ and so on, since taking the derivative of an inverse power decreases it by one, like $r^{-n}\to r^{-n-1}=r^{-(n+1)}$.
### Energy and torque
When subject to an external source field, we can calculate the stored [[potential energy]] of a *rigid* dipole. The distinction here is important: a non-rigid dipole would move to adapt to the source field, ending up in the point of lowest potential energy. Given a dipole of charges $-q$ and $q$ set a distance $d\mathbf{s}$ apart, respectively in $\mathbf{r}$ and $\mathbf{r}+d\mathbf{s}$, we find the potential energy as
$$\mathbf{U}(\mathbf{r})=q[V(\mathbf{r}+d\mathbf{s})-V(\mathbf{r})]=q(d\mathbf{s}\cdot \nabla V(\mathbf{r}))=-\mathbf{p}\cdot \mathbf{E}(\mathbf{r})$$
where we used the fact that the infinitesimal difference of potential is given by the projection of the [[gradient]] over the $d\mathbf{s}$ axis (i.e. the [[directional derivative]])[^2]. Using the same argument, the [[moment of force]] (or torque) is given by
$$\begin{align}
\tau(\mathbf{r})&=-q\mathbf{r}\times \mathbf{E}(\mathbf{r})+q(\mathbf{r}+d\mathbf{s})\times \mathbf{E}(\mathbf{r}+d\mathbf{s}) \\
&=-q\mathbf{r}\times \mathbf{E}(\mathbf{r})+q\mathbf{r}\times \mathbf{E}(\mathbf{r}+d\mathbf{s})+qd\mathbf{s}\times \mathbf{E}(\mathbf{r}+d\mathbf{s}) \\
&=q\mathbf{r}[\mathbf{E}(\mathbf{r}+d\mathbf{s})-\mathbf{E}(\mathbf{r})]+\mathbf{p}\times \mathbf{E}(\mathbf{r}+d\mathbf{s}) \\
&=q\mathbf{r}[d\mathbf{s}\cdot \nabla \mathbf{E}(\mathbf{r})]+\mathbf{p}\times[\mathbf{E}(\mathbf{r})+d\mathbf{s}\cdot \nabla \mathbf{E}(\mathbf{r})] \\
&\simeq \mathbf{p}\times \mathbf{E}(\mathbf{r})
\end{align}$$
The last step is a valid approximation when $d\mathbf{s}\cdot \nabla \mathbf{E}(\mathbf{r})\simeq 0$. This is true if the separation distance $d\mathbf{s}$ is zero (we have a perfect dipole) or if the gradient is zero (the field is uniform). We can see that the torque is zero when $\mathbf{p}$ and $\mathbf{E}$ are parallel. Thus, if the dipole isn't rigid, it will rotate until its axis is set in the direction of the field, then come to rest. This has the important consequence that all dipoles under an electric field become collectively aligned in the same direction and therefore combine their individual dipole moments to form a single massive (physical) dipole. At heart, this is the mechanism behind [[dielectric polarization]], where the dipoles are all of the [[Atom|atoms]] and [[molecule|molecules]] that comprise the material.

Also, pay close attention to the directions: while the torque tells us the orientation, it gives us no information on the direction of $\mathbf{p}$. Thankfully, that's given by its definition: since we defined $\mathbf{p}$ to go from the negative to the positive pole ("countercurrent", if you would, since the electric field does the exact opposite), and electric forces attract opposite charges, then $\mathbf{p}$ must be directed *alongside* the source field.

![[Schema Dipole alignment|100%]]

When the dipole rotates due to the torque, it does [[work]]. In the most extreme case (the dipole is perpendicular to the field), calling $\theta$ the angle between $\mathbf{E}$ and $\mathbf{p}$, it does work
$$W=\int_{\pi}^{0}\tau(\mathbf{r})d\theta=\int_{\pi}^{0}\mathbf{p}\times \mathbf{E}(\mathbf{r})d\theta=pE\int_{\pi}^{0}\sin \theta d\theta=2pE$$
The potential energy, of course, diminishes by the same amount to preserve conservation of energy.
### Radiation
Like all static configurations, a standing dipole does not emit [[electromagnetic radiation]]. However, it does make for a very convenient foundation to produce controlled and analytically solvable radiation when we making the dipole *oscillate*. To do so, say now that the charges of the dipole are time-dependent, $q(t)$ and $-q(t)$, and that we drive the charge back and forth between one end and the other (through, say, a fine wire that doesn't otherwise affect the system). This exchange is periodic and has an [[Frequency|angular frequency]] $\omega$. Each charge changes according to:
$$q(t)=q_{0}\cos (\omega t)$$
The dipole moment then changes according to
$$\mathbf{p}(t)=p_{0}\cos (\omega t)\ \hat{\mathbf{z}}$$
where $p_{0}\equiv q_{0}d$ is the maximum value of the moment (and we set the moment on the $\hat{\mathbf{z}}$ axis because we may as well).
#### Potentials
The charges are not moving, so the [[retarded potentials|retarded potential]] is the [[Liénard-Wiechert potentials|Liénard-Wiechert potential]] with $\mathbf{v}=0$:
$$V(\mathbf{r},t)=\frac{1}{4\pi \varepsilon_{0}}\left[ \frac{q_{0}\cos[\omega(t-\mathfrak{r}_{+}/c)]}{\mathfrak{r}_{+}} - \frac{q_{0}\cos[\omega(t-\mathfrak{r}_{-}/c)]}{\mathfrak{r}_{-}} \right]$$
$\mathfrak{r}_{\pm}$ are defined as at the top of this article as
$$\mathfrak{r}_{\pm}=\sqrt{ r^{2}\mp rd\cos \theta+ \left( \frac{d}{2} \right)^{2} }$$
It would make our life a lot easier if we could revert back to a perfect dipole. We can't just set $d=0$, as that would nullify the potential, but we can approximate it to the first order by setting
$$d\ll r\tag{Perfect dipole approximation}$$
The first order approximation starts by factoring out $r^{2}$:
$$\mathfrak{r}_{\pm}=r\sqrt{ 1 \mp \frac{d}{r}\cos \theta+ \frac{1}{4} \frac{d^{2}}{r^{2}} }$$
Notice that $d/r\ll 1$, so $d^{2}/r^{2}$ is completely negligible to first order. We then apply the [[Binomial theorem|binomial expansion]] of the square root:
$$\mathfrak{r}_{\pm}\simeq r\sqrt{ 1\mp \frac{d}{r}\cos \theta }\simeq r\left( 1\mp \frac{d}{2r}\cos \theta \right)$$
With this equation we can say
$$\begin{align}
\cos\left[ \omega\left( t- \frac{\mathfrak{r}_{\pm}}{c} \right) \right]&\simeq \cos\left[ \omega\left( t- \frac{r}{c} \right)\pm \frac{\omega d}{2c}\cos \theta \right] \\
&=\cos\left[ \omega\left( t- \frac{r}{c} \right) \right]\cos\left( \frac{\omega d}{2c}\cos \theta \right)\mp \sin\left[ \omega\left( t- \frac{r}{c} \right) \right]\sin\left( \frac{\omega d}{2c}\cos \theta \right) \\
&=\ldots
\end{align}$$
where we used $\cos(\alpha\pm \beta)=\cos \alpha \cos \beta\mp \sin \alpha \sin \beta$. This is... verbose. Thankfully, in the perfect dipole limit we have another approximation that is automatically satisfied:
$$d\ll \lambda\sim\frac{c}{\omega}\tag{Large wavelength approximation}$$
since [[Wave|waves]] of frequency $\omega$ have a [[wavelength]] $\lambda=2\pi c/\omega$. With this we can say, truncating the [[sine and cosine series]] to first order:
$$\frac{\omega d}{c}\ll 1\quad\Rightarrow \quad \cos\left( \frac{\omega d}{2c}\cos \theta \right)\simeq 1,\qquad \sin\left( \frac{\omega d}{2c}\cos \theta \right)\simeq \frac{\omega d}{2c}\cos \theta$$
and so
$$\ldots\simeq \cos\left[ \omega\left( t- \frac{r}{c} \right) \right]\mp \frac{\omega d}{2c}\cos \theta \sin\left[ \omega\left( t- \frac{r}{c} \right) \right]$$
Using this result and
$$\frac{1}{\mathfrak{r}_{\pm}}\simeq \frac{1}{r}\left( 1\pm \frac{d}{2r}\cos \theta \right)$$
we can claim the potential in the perfect dipole and large wavelength approximations is
$$V(r,\theta,t)\simeq\frac{p_{0}\cos\theta}{4\pi \varepsilon_{0}r}\left[ - \frac{\omega}{c}\sin\left[ \omega\left( t- \frac{r}{c} \right) \right] + \frac{1}{r}\cos\left[ \omega\left( t- \frac{r}{c} \right) \right] \right]$$
This is correct and, in fact, if we send $\omega\to0$ (and thereby stop the oscillation), we go back to the usual static potential $(1)$. However, we are more interested in the fields that survive large distances from the source, in the so-called **radiation zone**:
$$r\gg \frac{c}{\omega} \quad\text{or equivalently}\quad r\gg \lambda\tag{Far field approximation}$$
Note that the far field approximation and large wavelength approximation now imply the perfect dipole limit and we are left with
$$d\ll \lambda \ll r$$
Here, the term $\sim r^{-1}$ dominates over the term $\sim r^{-2}$, so we can drop the latter. The potential then reduces to a single term:
$$\boxed{V(r,\theta,t)=- \frac{p_{0}\cos\theta}{4\pi \varepsilon r}\frac{\omega}{c} \sin\left[ \omega\left( t- \frac{r}{c} \right) \right]}\tag{3}$$
The [[magnetic vector potential]] induced by this oscillation starts from the [[electric current]]
$$\mathbf{I}(t)=\frac{dq}{dt}\hat{\mathbf{z}}=-q_{0}\omega \sin(\omega t)\hat{\mathbf{z}}$$
which leads to the integral
$$\mathbf{A}(\mathbf{r},t)=\frac{\mu_{0}}{4\pi}\int_{-d/2}^{d/2} \frac{\mathbf{I}(t_{r})}{\mathfrak{r}}dz=\frac{\mu_{0}}{4\pi}\int_{-d/2}^{d/2} \frac{-q_{0}\omega \sin[\omega(t-\mathfrak{r}/c)]\hat{\mathbf{z}}}{\mathfrak{r}}dz$$
where integration happens over the line that connects that two charges of the dipole (which we set on the $z$ axis) and $\mathfrak{r}$ is the distance from the element $dz$ and the point $\mathbf{r}$. Because integration introduces a factor of $d$ we can, to first order, replace the integrand by its value at the center, where $\mathfrak{r}=r$ :
$$\boxed{\mathbf{A}(r,\theta,t)=- \frac{\mu_{0}p_{0}\omega}{4\pi r}\sin\left[ \omega\left( t- \frac{r}{c} \right) \right]\hat{\mathbf{z}}}\tag{4}$$
#### Fields
Now that we have the potentials, we can go through the usual formulas to get the fields. We're in electrodynamics, so the electric field is $\mathbf{E}=-\nabla V-\frac{ \partial \mathbf{A} }{ \partial t }$. The potential gradient in [[polar coordinates]] is:
$$\begin{align}
\nabla V&=\frac{ \partial V }{ \partial r } \hat{\mathbf{r}}+ \frac{1}{r}\frac{ \partial V }{ \partial \theta } \hat{\boldsymbol{\theta}} \\
&=- \frac{p_{0}\omega}{4\pi \varepsilon_{0}c}\Big[ \cos \theta\left( - \frac{1}{r^{2}}\sin\left[ \omega\left( t- \frac{r}{c} \right) \right]- \frac{\omega}{rc}\cos\left[ \omega\left( t- \frac{r}{c} \right) \right] \right) \hat{\mathbf{r}} \\
&\qquad-\frac{\sin\theta}{r^{2}}\sin\left[ \omega\left( t- \frac{r}{c} \right) \right]\hat{\boldsymbol{\theta}}\Big] \\
&\simeq \frac{p_{0}\omega ^{2}}{4\pi \varepsilon_{0}c^{2}}\left( \frac{\cos\theta}{r^{2}} \right)\cos\left[ \omega\left( t- \frac{r}{c} \right) \right]\hat{\mathbf{r}}
\end{align}$$
where in the last step we dropped the first and last term since in the far field, $\sim r^{-2}$ are negligible. Likewise
$$\frac{ \partial \mathbf{A} }{ \partial t } =- \frac{\mu_{0}p_{0}\omega ^{2}}{4\pi r}\cos\left[ \omega\left( t- \frac{r}{c} \right) \right](\cos \theta \hat{\mathbf{r}}-\sin \theta \hat{\boldsymbol{\theta}})$$
Quite conveniently, the cosine term here cancels out the entire gradient (notice $\varepsilon_{0}c^{2}=1/\mu_{0}$). The electric field therefore is
$$\boxed{\mathbf{E}=- \frac{\mu_{0}p_{0}\omega ^{2}}{4\pi r}\sin \theta\cos\left[ \omega\left( t- \frac{r}{c} \right) \right]\hat{\boldsymbol{\theta}}}\tag{5}$$
The magnetic field is derived from the [[curl]] of $\mathbf{A}$:
$$\begin{align}
\nabla\times \mathbf{A}&=\frac{1}{r}\left[ \frac{ \partial  }{ \partial r } (rA_{\theta})- \frac{ \partial A_{r} }{ \partial \theta }  \right]\hat{\boldsymbol{\phi}} \\
&=- \frac{\mu_{0}p_{0}\omega}{4\pi r}\left[ \frac{\omega}{c}\sin \theta \cos\left[ \omega\left( t- \frac{r}{c} \right) \right]+ \frac{\sin\theta}{r}\sin \left[ \omega\left( t- \frac{r}{c} \right) \right] \right]\hat{\boldsymbol{\phi}} \\
&\simeq- \frac{\mu_{0}p_{0}\omega ^{2}}{4\pi c}\left( \frac{\sin\theta}{r} \right)\cos\left[ \omega\left( t- \frac{r}{c} \right) \right]\hat{\boldsymbol{\phi}}
\end{align}$$
Where again we used the far field approximation to eliminate the $\sim r^{-2}$ term. The magnetic field then is
$$\boxed{\mathbf{B}=- \frac{\mu_{0}p_{0}\omega ^{2}}{4\pi cr}\sin \theta\cos\left[ \omega\left( t- \frac{r}{c} \right) \right]\hat{\boldsymbol{\phi}}=\frac{1}{c}\hat{\mathbf{r}}\times \mathbf{E}}\tag{6}$$
The fields are in [[phase]], mutually [[Orthogonality|perpendicular]] and transverse. The ratio of their [[amplitude|amplitudes]] is exactly the speed of light: $E_{0}/B_{0}=c$. This should all be expected: after all, this is the behavior of electromagnetic waves in the vacuum.
#### Electromagnetic waves
Now that we have the fields, we can analyze the [[Wave|waves]] themselves. $(5)$ and $(6)$ represent monochromatic [[electromagnetic wave|electromagnetic waves]] of [[Frequency|angular frequency]] $\omega$ traveling at the [[speed of light]]. Since they are created from a point source, these are [[spherical wave|spherical waves]].

We can quantify the energy emitted by the oscillating dipole by starting from the [[Poynting vector]]:
$$\mathbf{S}(\mathbf{r},t)=\frac{1}{\mu_{0}}(\mathbf{E}\times \mathbf{B})=\frac{\mu_{0}}{c}\left[ \frac{p_{0}\omega ^{2}}{4\pi r} \sin\theta\cos\left[ \omega\left( t- \frac{r}{c} \right) \right] \right]^{2}\hat{\mathbf{r}}$$
The [[irradiance]] is the magnitude of the time average of the Poynting vector over a full oscillation:
$$I=\lvert \langle \mathbf{S} \rangle \rvert =\frac{\mu_{0}p_{0}^{2}\omega^{4}}{32\pi ^{2}c} \frac{\sin^{2}\theta}{r^{2}}$$
Note that it is dependent on the angle $\theta$. On the axis of the dipole, where $\theta=0$ and therefore $\sin \theta=0$, $I=0$. This means that oscillating dipoles *do not* emit radiation on their axis. On the other hand, the emission is maximized perpendicular to the axis, when $\theta=\pm\pi/2$ and $\sin ^{2}\theta=1$. Geometrically, this creates a sort of [[torus]] shape.

The average [[radiant power]] is found by "collecting" all of the energy that comes out of the dipole over time. We can do this by enclosing the dipole in a closed [[surface]], the simplest of which is a [[sphere]], and then integrate the [[radiant flux]] of energy going through that surface:
$$\boxed{\langle P \rangle =\int_{\mathcal{S}}\langle \mathbf{S} \rangle \cdot d\mathbf{a} =\frac{\mu_{0}p_{0}^{2}\omega^{4}}{32\pi ^{2}c}\int \frac{\sin^{2}\theta}{r^{2}}r^{2}\sin \theta d\theta d\phi=\frac{\mu_{0}p_{0}^{2}\omega^{4}}{12\pi c}}$$
We can see that the power is *strongly* dependent on $\omega$, to the fourth power. Evidently, as the frequency of oscillation increases, the power gets really high really fast (although not exponentially fast). On paper, you could emit near infinite energy from a dipole by just having it oscillate *really* fast. As you may imagine, this seems... hard to believe? And hard to believe it is, because this $\sim \omega^{4}$ behavior is the source of *a lot* of problems in the late 1800s, since experimental measurements just did not match for high frequencies. It was so far from reality in fact that measurements showed that around the ultraviolet range, energy emission would actually start going *down* instead of increasing like $\sim \omega^{4}$. The infinitely increasing power at large frequencies has come to be known as the **[[Black body|ultraviolet catastrophe]]**, and it was this very flaw that would spur the beginning of quantum physics.

> [!tip] Why is the sky blue?
> The spectrum of sunlight that illuminates Earth contains a very large number of frequencies ([[stella|stars]] are more or less [[black body|black bodies]]). The [[Atom|atoms]] and [[molecule|molecules]] in the atmosphere can be seen as tiny electric dipoles made up [[Electron|electrons]] and [[proton|protons]]. These are affected by the electromagnetic waves emitted by the Sun and are driven to oscillate at the same frequency of the wave that passes near them. In a simplified model, they become driven [[Harmonic oscillator|harmonic oscillators]]. The oscillation of the molecules then itself emits waves, which are what we see on the ground (unless you are staring directly at the Sun[^3]). The presence of the $\omega^{4}$ leads to a much stronger absorption and re-emission in the high frequencies, which means more blue light being emitted as opposed to green and especially red.
> 
> Since sunlight is a transverse wave, the dipoles oscillate perpendicular to the beam of light. There are infinite directions this can be, all arranged in a plane perpendicular to the beam. This is the basic idea of [[polarization]]. Sunlight is, however, unpolarized, which is to say the axis of oscillation changes fast and chaotically, so the axis of oscillation of the dipoles is random. We can only state that they oscillate in a plane normal to the propagation of the wave. From an observer on Earth, some will oscillate on the line of sight (i.e. you looking at the sky) and will therefore not emit anything (because oscillating dipoles don't emit on the axis of oscillations). Others will oscillate perpendicularly and maximize perceived emission. Most will be somewhere in between. Since oscillations are guaranteed to be perpendicular between Earth and the Sun, the dipole radiation you perceive will be weakest (in principle, zero) when looking into the Sun (your line of sight *is* the Earth-Sun axis and hence perpendicular to the polarization plane). This is why the sky is the least blue in a corona around the Sun[^4]. Similarly, the further away you angle your vision from the Sun, the more parallel you get to the plane of polarization, which makes you see more and more scattered dipole light. This is why the sky the the most blue around the horizon, furthest from the Sun.
> 
> Emission and scattering happens progressively as the beam of light travels through the atmosphere and stimulates molecules. The first frequencies to be absorbed and re-emitted are the high ones, so as you put on a thicker layer of atmosphere between you and the dipole, more and more of the high-frequency light will be removed, leaving only the low frequencies behind: red. This is why when the sun is low on the horizon at sunset we see an orange sky: sunlight must travel through considerably more atmosphere than at noon, and the light that we end up seeing has had all of the blue stripped out by the time it gets to us. It's also why the sky is orange usually only around the horizon; the high atmosphere is still bluish because there's less air to go through.
> 
>  The phenomenon is more complicated than this, as it involves [[photon]] scattering at a frequency-dependent [[probability distribution]] of angles as described by [[Thompson scattering]], but the source of the effect is the strong $\omega^{4}$ dependency. Were the dependency lower, like $\omega$, the sky would still be primarily blue, but with significant other components of the light (it would probably look a lot whiter, since mixed colors in light make for white light).

[^1]: Proof: $\nabla(\mathbf{p}\cdot \mathbf{r})=\nabla(p_{x}x+p_{y}y+p_{z}z)=\left( p_{x}\frac{ \partial x }{ \partial x }+p_{y}\frac{ \partial y }{ \partial y }+p_{z}\frac{ \partial z }{ \partial z } \right)=(p_{x},p_{y},p_{z})=\mathbf{p}$.

[^2]: The keyword here is infinitesimal: it is reliant on the fact that we specifically have $d\mathbf{s}$ and not any $\mathbf{s}$. In other words, this is only exact for an ideal dipole, and is a good approximation for physical dipoles with small separation $\mathbf{s}$.

[^3]: please don't stare at the sun

[^4]: There's also a biological factor of the Sun being so bright it completely snuffs out all other light to the extent that your eyes can no longer make out anything in the vicinity. Basically, it's so bright you can't see anything.
