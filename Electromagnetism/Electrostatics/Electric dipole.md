A **(physical) electric dipole** is a system of two equal and opposite [[Electric charge|electric charges]] separated by a distance $d$.

![[VFPt_dipoles_electric.svg|400]]
*By Geek3 - Own work, CC BY-SA 4.0, https://commons.wikimedia.org/w/index.php?curid=85815210*
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
$$V_\text{dip}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}} \frac{\mathbf{p}\cdot\hat{\mathbf{r}}}{r^{2}}\tag{2}$$
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
where we used the fact that the infinitesimal difference of potential is given by the projection of the [[Gradient]] over the $d\mathbf{s}$ axis (i.e. the [[directional derivative]])[^2]. Using the same argument, the [[moment of force]] (or torque) is given by
$$\begin{align}
\tau(\mathbf{r})&=-q\mathbf{r}\times \mathbf{E}(\mathbf{r})+q(\mathbf{r}+d\mathbf{s})\times \mathbf{E}(\mathbf{r}+d\mathbf{s}) \\
&=-q\mathbf{r}\times \mathbf{E}(\mathbf{r})+q\mathbf{r}\times \mathbf{E}(\mathbf{r}+d\mathbf{s})+qd\mathbf{s}\times \mathbf{E}(\mathbf{r}+d\mathbf{s}) \\
&=q\mathbf{r}[\mathbf{E}(\mathbf{r}+d\mathbf{s})-\mathbf{E}(\mathbf{r})]+\mathbf{p}\times \mathbf{E}(\mathbf{r}+d\mathbf{s}) \\
&=q\mathbf{r}[d\mathbf{s}\cdot \nabla \mathbf{E}(\mathbf{r})]+\mathbf{p}\times[\mathbf{E}(\mathbf{r})+d\mathbf{s}\cdot \nabla \mathbf{E}(\mathbf{r})] \\
&\simeq \mathbf{p}\times \mathbf{E}(\mathbf{r})
\end{align}$$
The last step is a valid approximation when $d\mathbf{s}\cdot \nabla \mathbf{E}(\mathbf{r})\simeq 0$. This is true if the separation distance $d\mathbf{s}$ is zero (we have a perfect dipole) or if the gradient is zero (the field is uniform). We can see that the torque is zero when $\mathbf{p}$ and $\mathbf{E}$ are parallel. Thus, if the dipole isn't rigid, it will rotate until its axis is set in the direction of the field, then come to rest. This has the important consequence that all dipoles under an electric field become collectively aligned in the same direction and therefore combine their individual dipole moments to form a single massive (physical) dipole. At heart, this is the mechanism behind [[dielectric polarization]], where the dipoles are all of the [[atomo|atoms]] and [[molecule|molecules]] that comprise the material.

Also, pay close attention to the directions: while the torque tells us the orientation, it gives us no information on the direction of $\mathbf{p}$. Thankfully, that's given by its definition: since we defined $\mathbf{p}$ to go from the negative to the positive pole ("countercurrent", if you would, since the electric field does the exact opposite), and electric forces attract opposite charges, then $\mathbf{p}$ must be directed *alongside* the source field.

![[Schema Dipole alignment|100%]]

When the dipole rotates due to the torque, it does [[work]]. In the most extreme case (the dipole is perpendicular to the field), calling $\theta$ the angle between $\mathbf{E}$ and $\mathbf{p}$, it does work
$$W=\int_{\pi}^{0}\tau(\mathbf{r})d\theta=\int_{\pi}^{0}\mathbf{p}\times \mathbf{E}(\mathbf{r})d\theta=pE\int_{\pi}^{0}\sin \theta d\theta=2pE$$
The potential energy, of course, diminishes by the same amount to preserve conservation of energy.

[^1]: Proof: $\nabla(\mathbf{p}\cdot \mathbf{r})=\nabla(p_{x}x+p_{y}y+p_{z}z)=\left( p_{x}\frac{ \partial x }{ \partial x }+p_{y}\frac{ \partial y }{ \partial y }+p_{z}\frac{ \partial z }{ \partial z } \right)=(p_{x},p_{y},p_{z})=\mathbf{p}$.

[^2]: The keyword here is infinitesimal: it is reliant on the fact that we specifically have $d\mathbf{s}$ and not any $\mathbf{s}$. In other words, this is only exact for an ideal dipole, and is a good approximation for physical dipoles with small separation $\mathbf{s}$.
