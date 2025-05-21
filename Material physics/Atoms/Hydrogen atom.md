---
wiki-publish: true
aliases:
  - hydrogenoid atom
---
The **hydrogen atom** is the [[atom]] of the element hydrogen, a quantum [[physical system]] made up of a central positive [[Electric charge|charge carrier]] (a [[proton]]) and a negative charge carrier (an [[Elettrone|electron]]) surrounding it. It is the simplest case of a broader class of objects called **hydrogenoid atoms** which may possess more central charges, that is, a full atomic [[Nucleo atomico|nucleus]].

![[Schema modello idrogeno|center]]

The [[Hamiltonian]] for the [[Equazione di Schrödinger|Schrödinger equation]] of the hydrogen atom is
$$\hat{H}=- \frac{\hbar^{2}}{2M}\nabla ^{2}_{R}- \frac{\hbar^{2}}{2m}\nabla^{2}_{r}- \frac{Ze^{2}}{4\pi \varepsilon_{0}r}$$
where $M$ is the [[mass]] of the nucleus, $m$ is the mass of the electron, $\hbar$ is the [[Planck constant|reduced Planck constant]], $Z$ is the [[Atom|atomic number]] (the number of protons), $\varepsilon_{0}$ is the [[Vacuum permittivity|electric permittivity of the vacuum]] and $r$ is the distance of the electron from the nucleus. The last term is the [[potential energy]] due to [[Interazione elettromagnetica|electromagnetic attraction]]. This Hamiltonian is not explicitly dependent on the [[spin]] of the electron.
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
$$\boxed{\left[ - \frac{\hbar^{2}}{2\mu r^{2}}\frac{ \partial  }{ \partial r } \left( r^{2}\frac{ \partial  }{ \partial r }  \right)+ \frac{\hat{L}^{2}}{2\mu r^{2}}- \frac{Ze^{2}}{4\pi \varepsilon_{0}r} \right]\psi(r,\theta,\phi)=E\psi(r,\theta,\phi)}$$
where the angular dependence of the system was grouped inside of the angular momentum. As usual, the square angular momentum, the momentum on one axis ($z$) and the Hamiltonian all commute, $[\hat{L}^{2},\hat{L}_{z}]=[\hat{L}^{2},\hat{H}]=[\hat{L}_{z},\hat{H}]=0$, so they all share simultaneous eigenstates.

For a general solution of this equation in spherical coordinates, using a generic potential $V$, see [[Equazione di Schrödinger#Soluzione tridimensionale]]. In there, we set $\psi(r,\theta,\phi)=R(r)Y(\theta,\phi)$, find that the angular component $Y(\theta,\phi)$ of the solution is universal and completely independent on the potential. The radial component instead depends on $V$ and we must solve it uniquely for each the potential. As such, our next challenge is solving the radial component for our $V$.
#### Angular part
As a refresher, the angular components depend on the eigenstates of $\hat{L}^{2}$ and $\hat{L}_{z}$ and are found using the [[Armoniche sferiche|spherical harmonics]] $Y_{l,m}(\theta,\phi)$:
$$\boxed{\hat{L}^{2}Y_{l,m}(\theta,\phi)=l(l+1)\hbar^{2}Y_{l,m}(\theta,\phi)}\qquad\hat{L}_{z}Y_{l,m}(\theta,\phi)=m\hbar Y_{l,m}(\theta,\phi)$$
Using spherical harmonics on $\hat{L}_{z}$ is a bit overkill, since it's really only dependent on $\phi$. During the derivation by [[separation of variables]] one finds that $Y_{l,m}(\theta,\phi)=\Theta_{l,m}(\theta)\Phi_{m}(\phi)$. The $\Phi_{m}(\phi)$ function is pretty easy to solve and it is found to be $\Phi_{m}(\phi)=e^{im\phi}$. The $\Theta_{l,m}(\theta)$ function is more complicated is requires invoking the [[Polinomi di Legendre|associated Legendre functions]] $P_{l,m}(\cos \theta)$ to get $\Theta(\theta)=AP_{l,m}(\cos \theta)$ ($A$ is some constant). As such, we can rewrite the $\hat{L}_{z}$ eigenstates as
$$\boxed{\hat{L}_{z}\Phi_{m}(\phi)=m\hbar \Phi_{m}(\phi)}$$
In the context of the hydrogen atom, the number $l$ and $m$ take on specific interpretations: $l$ is the **angular momentum [[Numero quantico|quantum number]]** and $m$ is the **magnetic angular momentum quantum number**.

Still, spherical harmonics are generally complex functions. We know very well that only real numbers can be measured from a system, so we need to bridge the gap. What's done is the usual method of taking the square modulo of a complex number to reduce it to a real quantity. In this case, we take the square modulo of the spherical harmonics:
$$\lvert Y_{l,m}(\theta,\phi) \rvert^{2} =\lvert \Theta_{l,m}(\theta) \rvert^{2}\lvert \Phi_{m}(\phi) \rvert^{2}  $$
Luckily, the modulo of $\Phi_{m}(\phi)$ is very easy: $\lvert \Phi_{m}(\phi) \rvert^{2}=\lvert e^{im\phi} \rvert^{2}=1/2\pi$. Notably, it is completely independent of $m$. The issue is finding the square modulo of $\Theta(\theta)$. They can, for instance, be found computationally and plotted in graphs or animations. Analytically, we remain with
$$\lvert Y_{l,m}(\theta,\phi) \rvert^{2} =\frac{1}{2\pi}\lvert \Theta_{l,m}(\theta) \rvert^{2}$$
#### Radial part
The radial part is
$$\left[ - \frac{\hbar^{2}}{2\mu r^{2}} \frac{d}{dr} \left( r^{2} \frac{d}{dr}  \right)+ \frac{\hbar^{2}l(l+1)}{2\mu r^{2}}- \frac{Ze^{2}}{4\pi \varepsilon_{0}r} \right]R(r)=ER(r)$$
As in the general case, we set $u(r)=rR(r)$ to simplify things:
$$\left[ - \frac{\hbar^{2}}{2\mu } \frac{d^{2}}{dr^{2}}+ \frac{\hbar^{2}l(l+1)}{2\mu r^{2}}- \frac{Ze^{2}}{4\pi \varepsilon_{0}r} \right]u(r)=Eu(r)$$
Notice how there is a term dependent on the angular momentum $l$ even in the radial term. This has the same dimensions as the usual potential term, and what we do is to combine in the two in a single, *effective* potential $V_\text{eff}$ defined as
$$V_\text{eff}=V(r)+ \frac{\hbar^{2}l(l+1)}{2\mu r^{2}}$$
This potential looks something like this:

![[Plot Effective spherical Schrodinger potential]]

As always, the system is [[Stati in meccanica quantistica|bound]] if $E<0$ and [[Stati in meccanica quantistica|scattering]] if $E>0$. As we can see, at low distances ($r\to0$) there exists a potential barrier for any $l>0$, which means that it is repulsive, *except* for $l=0$, where it is attractive. Conversely, the higher the $l$, the more repulsive it is.

For convenience, we introduce a few variables
$$\rho\equiv\left( - \frac{8\mu E}{\hbar ^{2}} \right)^{1/2}r,\qquad \lambda=\frac{Ze^{2}}{4\pi \varepsilon_{0}\hbar}\left( - \frac{\mu}{2E} \right)^{1/2}=Z\alpha\left( - \frac{\mu c^{2}}{2E} \right)^{1/2}$$
where $\alpha$ is the [[fine-structure constant]] and $c$ is the [[speed of light]]. If we substitute these in the equation, we get
$$\left[ \frac{d^{2}}{d\rho ^{2}} - \frac{l(l+1)}{\rho ^{2}}+ \frac{\lambda}{\rho}- \frac{1}{4}\right]u_{E,l}(\rho)=0\tag{1}$$
A much simpler form, but still quite abstract. Instead of diving head-first into solving it, we can start by analyzing asymptotic behavior. When $\rho\to \infty$, the equations greatly simplifies to
$$\left[ \frac{d^{2}}{d\rho ^{2}}- \frac{1}{4} \right]u(\rho)=0$$
This a second order [[Ordinary differential equation|ODE]] of the form $\ddot{u}- \frac{1}{4}u=0$ and the solution is an exponential. Thus, for high $\rho$, we have
$$u(\rho)\simeq e^{\pm \rho/2}$$
Since we have an asymptotic solution, we can claim that the general solution behaves in the same manner as the asymptote, but scaled by some other function $f(\rho)$. Thus, in general, in and out of the asymptote:
$$u(\rho)=f(\rho)e^{-\rho/2}\tag{2}$$
By definition, $f(\rho)$ contains all of the information about $E$ and $l$, since those are lost at the asymptote, $f(\rho)\equiv f_{E,l}(\rho)$. Our next problem is finding $f(\rho)$.
#### Finding $f(\rho)$
To start, we make the ansatz $f(\rho)=\rho^{l+1}g(\rho)$ where $g(\rho)$ is a function defined by its [[power series]]
$$g(\rho)=\sum_{k=0}^{\infty} c_{k}\rho^{k}$$
where $c_{0}\neq0$. We now substitute $(2)$ in $(1)$ to get
$$\left[ \rho \frac{d^{2}}{d\rho ^{2}}+ (2l+2-\rho) \frac{d}{d\rho}+ (\lambda-l-1) \right]g(\rho)$$
This equation can be solved analytically by expanding $g(\rho)$ and solving for the coefficients (see e.g. Bransden). We find the recurrence relation
$$c_{k+1}=\left[ \frac{k+l-1-\lambda}{(k+1)(k+2l+2)} \right]c_{k}$$
For large $k$, the ratio is approximately
$$\frac{c_{k+1}}{c_{k}}\simeq \frac{1}{k}$$
This ratio is the same as that of the series for $\rho^{p}e^{\rho}$ for some $p \in \mathbb{R}$. This, alongside $(2)$ and our ansatz $f(\rho)=\rho^{l+1}g(\rho)$, suggests that the asymptotic behavior is something of the form $u_{E,l}(\rho)\sim\rho^{l+1-p}e^{-\rho/2}$. But this can't be, so the $g(\rho)$ series must terminate early to some $n_{r}$ terms, which means that it is a polynomial of rank $n_{r}$. We call $n_{r}$ the **radial quantum number** and it is a positive integer. Thus, any $c_{k}=0$ if $k>n_{r}$ and using the recurrence relation, we have $\lambda=n_{r}+l+1$.  We can further define the **principal quantum number**
$$n\equiv n_{r}+l+1$$
and of course $n=\lambda$.
#### Eigenvalues
Since we know what $\lambda$ is, we can extract $E$ out of it, substitute $\lambda$ for $n$ and get the [[Stationary state|energy eigenvalues]]:
$$E_{n}=- \frac{1}{2n^{2}}\left( \frac{Ze^{2}}{4\pi \varepsilon_{0}} \right) \frac{\mu}{\hbar ^{2}}=- \frac{e^{2}}{4\pi \varepsilon_{0}a_{0}} \frac{\mu}{m} \frac{Z^{2}}{2n^{2}}=- \frac{e^{2}}{4\pi \varepsilon_{0}a_{\mu}} \frac{Z^{2}}{2n^{2}}$$
where we defined $a_{0}$ as the [[Bohr radius]] and $a_{\mu}=a_{0} (m/\mu)$ as the modified Bohr radius. Notably, the energy eigenvalues are *not* (directly) dependent on $l$. This means that the energy eigenstates are [[Degenerazione|degenerate]] in $l$ too, no just $m$. Notably, these are identical to semiclassical Bohr model of the atom. Next stop: eigenstates.
#### Eigenstates
What the Bohr model does *not* give are the [[Funzione d'onda|wavefunctions]] of the quantum states of the atom. Luckily, the hydrogen atom is one of the very few systems that can be solved analytically, although the solution isn't exactly simple. Invoking the [[Laguerre polynomials|associated Laguerre polynomials]] $L_{i}^{j}(\rho)$, the solution to the radial part in its most general case is
$$R_{nl}(r)=-\left[ \left( \frac{2z}{na_{\mu}} \right)^{3} \frac{(n-l-1)!}{2n[(n+l)!]^{3}} \right]^{1/2}e^{-\rho/2}\rho^{l}L_{n+l-1}^{2l+1}(\rho)$$
where
$$\rho=\frac{2zr}{na_{\mu}}=\frac{2zr}{na_{0}} \frac{M}{m}$$
Now that we now both the angular part $Y_{lm}$ and the radial part $R_{nl}$, the eigenfunction for the eigenstate determined by the numbers $(n,l,m)$ is
$$\psi(r,\theta,\phi)=R_{nl}(r)Y_{lm}(\theta,\phi)=\ldots$$
Of course, as is, the wavefunctions have limited intepretability. But as with all quantum mechanical system, the square modulo of $\psi$ gives the [[probability]] of finding the system in a given state. Specifically, $\lvert \psi(r,\theta,\phi) \rvert^{2}d\mathbf{r}$ is the probability of finding an [[electric charge]] (the electron) in an infinitesimal volume element $d\mathbf{r}$. The probability of finding the electron at a set distance $r$ from the nucleus is found by integrating $\lvert \psi(r,\theta,\phi) \rvert^{2}$ over all angles.

[^1]: The angular momentum operator is found by quantizing the classical quantities of $r$ and $p$, which become $\hat{r}$ and $-i\hbar \nabla$ respectively ($\nabla$ is the [[gradient]]). So, we get $\hat{L}=-i\hbar(\hat{r}\times \nabla)$.
