A **(physical) electric dipole** is a system of two equal and opposite [[Electric charge|electric charges]] separated by a distance $d$.

```tikz
\begin{document}
\begin{tikzpicture}[domain=-4:4]
\draw[red!60!white] (-2,-2) circle (5pt) node[anchor=north east] {$+q$};
\draw[blue!60!white] (2,2) circle (5pt) node[anchor=north west] {$-q$};
\draw (-2,-2) -- (2,2);
\draw (-2,-2) .. controls (1,-1) .. (2,2);
\draw (-2,-2) .. controls (-1,1) .. (2,2);
\draw (-2,-2) .. controls (2,-2) .. (2,2);
\draw (-2,-2) .. controls (-2,2) .. (2,2);
\draw (-2,-2) .. controls (4,-4) .. (2,2);
\draw (-2,-2) .. controls (-4,4) .. (2,2);
\end{tikzpicture}
\end{document}
```

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
Knowing the potential (mostly), we can now find the [[electric field]], at least that of a perfect dipole. Due to the origin-dependency of the dipole moment, we choose coordinates so that $\mathbf{p}$ is at the origin and points in the $z$ direction. This way, the potential is $(2)$. In [[spherical coordinates]] it reads
$$V_\text{dip}(r,\theta)=\frac{1}{4\pi\varepsilon_{0}}\frac{\hat{\mathbf{r}}\cdot \mathbf{p}}{r^{2}}=\frac{1}{4\pi\varepsilon_{0}}\frac{p\cos \theta}{r^{2}}$$
(in these choice of coordinates, we have azimuthal symmetry). The negative [[gradient]] is
$$\begin{align}
E_{r} & =-\frac{ \partial V }{ \partial r } =\frac{1}{4\pi\varepsilon_{0}} \frac{2\pi \cos \theta}{r^{3}} \\
E_{\theta} &= - \frac{1}{r}\frac{ \partial V }{ \partial \theta } =- \frac{1}{4\pi\varepsilon_{0}} \frac{p \sin \theta}{r^{3}} \\
E_{\phi} & =- \frac{1}{r\sin \theta}\frac{ \partial V }{ \partial \phi } =0
\end{align}$$
Thus
$$\boxed{\mathbf{E}_\text{dip}(r,\theta)=\frac{1}{4\pi\varepsilon_{0}} \frac{p}{r^{3}}(2\cos \theta\ \hat{\mathbf{r}}+\sin \theta\ \hat{\boldsymbol{\theta}})}$$
A more general, coordinate-free form can be proven to be
$$\boxed{\mathbf{E}_\text{dip}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}} \frac{1}{r^{3}}[3(\mathbf{p}\cdot \hat{\mathbf{r}})\hat{\mathbf{r}}-\mathbf{p}]}$$
Just like how the dipole term of potential goes like $\sim 1/r^{2}$ instead of $\sim 1/r$, the field goes like $\sim 1/r^{3}$ instead of $\sim 1/r^{2}$. Higher terms can be proven to go like $\sim 1/r^{4}$, $\sim 1/r^{5}$ and so on, since taking the derivative of an inverse power decreases it by one, like $r^{-n}\to r^{-n-1}=r^{-(n+1)}$.