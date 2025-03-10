---
aliases:
  - hydrogenoid atom
---
The **hydrogen atom** is a quantum [[physical system]] made up of a central positive [[Electric charge|charge carrier]] (a [[proton]]) and a negative charge carrier (an [[Elettrone|electron]]) surrounding it. It is the simplest case of a broader class of objects called **hydrogenoid atoms** which may possess more central charges, that is, a full atomic [[Nucleo atomico|nucleus]].

![[Schema modello idrogeno|center]]

The [[Hamiltonian]] for the [[Equazione di Schrödinger|Schrödinger equation]] of the hydrogen atom is
$$\hat{H}=- \frac{\hbar^{2}}{2M}\nabla ^{2}_{R}- \frac{\hbar^{2}}{2m}\nabla^{2}_{r}- \frac{Ze^{2}}{4\pi \varepsilon_{0}r}$$
where $M$ is the [[mass]] of the nucleus, $m$ is the mass of the electron, $\hbar$ is the [[Costante di Planck|reduced Planck constant]], $Z$ is the [[Atomo|atomic number]] (the number of protons), $\varepsilon_{0}$ is the [[Vacuum permittivity|electric permittivity of the vacuum]] and $r$ is the distance of the electron from the nucleus. The last term is the [[potential energy]] due to [[Interazione elettromagnetica|electromagnetic attraction]]. This Hamiltonian is not explicitly dependent on the [[spin]] of the electron.
### In spherical coordinates
Since we have a central potential, it is best to rewrite the equation in [[spherical coordinates]], as we have a general solution for the equation in this form. We can do so by introducing the [[Momento angolare quantistico|quantum angular momentum]] $\hat{L}=\hat{r}\times \hat{p}=-i\hbar (\hat{r}\times \nabla)$[^1] and rewriting in the [[frame of reference]] of the [[center of mass]]. We define the reduced mass as
$$\mu=\frac{Mm}{M+m}$$
Using $\mu$ and shifting the [[Laplacian]] to use the coordinates of the center of mass, the equation becomes
$$\hat{H}\psi(r)=\left[ - \frac{\hbar^{2}}{2\mu} \nabla ^{2}- \frac{Ze^{2}}{4\pi \varepsilon_{0}r}\right]\psi(r)=E\psi(r)$$
The spherical [[Coordinate transformation]] to [[Cartesian coordinates]] is
$$\begin{cases}
x=r\sin \theta \cos \phi \\
y=r\sin \theta \sin \phi \\
z=r\cos \theta
\end{cases},\quad-\pi\leq \theta\leq \pi,\quad 0\leq \phi\leq 2\pi$$
With this we can express the Laplacian in spherical coordinates. Hiding the potential behind $V(r)$ for brevity, the equation becomes
$$\begin{align}
\hat{H}&=- \frac{\hbar^{2}}{2\mu}\left[ \frac{1}{r^{2}}\frac{ \partial  }{ \partial r } \left( r^{2}\frac{ \partial  }{ \partial r }  \right)+ \frac{1}{r^{2}\sin \theta}\frac{ \partial  }{ \partial \theta } \left( \sin \theta \frac{ \partial  }{ \partial \theta }  \right)+ \frac{1}{r^{2}\sin ^{2}\theta}\frac{ \partial ^{2}  }{ \partial \phi ^{2} }  \right]+V(r) \\
\end{align}$$
Expressing the [[gradient]] in spherical coordinates, we similarly get
$$\hat{L}^{2}=-\hbar^{2}\left[ \frac{1}{\sin \theta}\frac{ \partial  }{ \partial \theta } \left( \sin \theta \frac{ \partial  }{ \partial \theta }\right) + \frac{1}{\sin ^{2} \theta}\frac{ \partial ^{2} }{ \partial \phi ^{2} }  \right]$$
We can see $\hat{L}^{2}$ come up in the Hamiltonian, so we substitute it to get
$$\hat{H}=- \frac{\hbar^{2}}{2\mu}\left[ \frac{1}{r^{2}}\frac{ \partial  }{ \partial r } \left( r^{2}\frac{ \partial  }{ \partial r }  \right)- \frac{\hat{L}^{2}}{\hbar^{2}r^{2}} \right]+V(r)$$
With this, the spherical Schrödinger equation for the hydrogen atom is
$$\boxed{\left[ - \frac{\hbar^{2}}{2\mu r}\frac{ \partial  }{ \partial r } \left( r^{2}\frac{ \partial  }{ \partial r }  \right)+ \frac{\hat{L}^{2}}{2\mu r^{2}}- \frac{Ze^{2}}{4\pi \varepsilon_{0}r} \right]\psi(r,\theta,\phi)=E\psi(r,\theta,\phi)}$$
where the angular dependence of the system was grouped inside of the angular momentum. As usual, the square angular momentum, the momentum on one axis ($z$) and the Hamiltonian all commute, $[\hat{L}^{2},\hat{L}_{z}]=[\hat{L}^{2},\hat{H}]=[\hat{L}_{z},\hat{H}]=0$, so they all share simultaneous eigenstates.

For a general solution of this equation in spherical coordinates, using a generic potential $V$, see [[Equazione di Schrödinger#Soluzione tridimensionale]]. In there, we find that the angular component of the solution is universal and completely independent on the potential. The radial component instead depends on $V$ and we must solve it uniquely for each the potential. As such, our next challenge is solving the radial component for our $V$.
#### Angular components
As a refresher, the angular components depend on the eigenstates of $\hat{L}^{2}$ and $\hat{L}_{z}$ and are found using the [[Armoniche sferiche|spherical harmonics]] $Y_{l,m}(\theta,\phi)$:
$$\boxed{\hat{L}^{2}Y_{l,m}(\theta,\phi)=l(l+1)\hbar^{2}Y_{l,m}(\theta,\phi)}\qquad\hat{L}_{z}Y_{l,m}(\theta,\phi)=m\hbar Y_{l,m}(\theta,\phi)$$
Using spherical harmonics on $\hat{L}_{z}$ is a bit overkill, since it's really only dependent on $\phi$. During the derivation by [[separation of variables]] one finds that $Y_{l,m}(\theta,\phi)=\Theta_{l,m}(\theta)\Phi_{m}(\phi)$. The $\Phi_{m}(\phi)$ function is pretty easy to solve and it is found to be $\Phi_{m}(\phi)=e^{im\phi}$. The $\Theta_{l,m}(\theta)$ function is more complicated is requires invoking the [[Polinomi di Legendre|associated Legendre functions]] $P_{l,m}(\cos \theta)$ to get $\Theta(\theta)=AP_{l,m}(\cos \theta)$ ($A$ is some constant). As such, we can rewrite the $\hat{L}_{z}$ eigenstates as
$$\boxed{\hat{L}_{z}\Phi_{m}(\phi)=m\hbar \Phi_{m}(\phi)}$$
In the context of the hydrogen atom, the number $l$ and $m$ take on specific interpretations: $l$ is the **angular momentum [[Numero quantico|quantum number]]** and $m$ is the **magnetic angular momentum quantum number**.

Still, spherical harmonics are generally complex functions. We know very well that only real numbers can be measured from a system, so we need to bridge the gap. What's done is the usual method of taking the square modulo of a complex number to reduce it to a real quantity. In this case, we take the square modulo of the spherical harmonics:
$$\lvert Y_{l,m}(\theta,\phi) \rvert^{2} =\lvert \Theta_{l,m}(\theta) \rvert^{2}\lvert \Phi_{m}(\phi) \rvert^{2}  $$
Luckily, the modulo of $\Phi_{m}(\phi)$ is very easy: $\lvert \Phi_{m}(\phi) \rvert^{2}=\lvert e^{im\phi} \rvert^{2}=1/2\pi$. Notably, it is completely independent of $m$. The issue is finding the square modulo of $\Theta(\theta)$. They can, for instance, be found computationally and plotted in graphs or animations. Analytically, we remain with
$$\lvert Y_{l,m}(\theta,\phi) \rvert^{2} =\frac{1}{2\pi}\lvert \Theta_{l,m}(\theta) \rvert^{2}$$

[^1]: The angular momentum operator is found by quantizing the classical quantities of $r$ and $p$, which become $\hat{r}$ and $-i\hbar \nabla$ respectively ($\nabla$ is the [[gradient]]). So, we get $\hat{L}=-i\hbar(\hat{r}\times \nabla)$.
