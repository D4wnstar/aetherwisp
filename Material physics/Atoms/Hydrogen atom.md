---
wiki-publish: true
aliases:
  - hydrogenoid atom
---
The **hydrogen atom** is the [[atom]] of the element hydrogen, a quantum [[physical system]] made up of a central positive [[Electric charge|charge carrier]] (a [[proton]]) and a negative charge carrier (an [[Elettrone|electron]]) surrounding it. It is the simplest case of a broader class of objects called **hydrogenoid atoms** which may possess a stronger central charge, that is, a full atomic [[Nucleo atomico|nucleus]].

![[Schema modello idrogeno|center]]

The [[Hamiltonian]] for the [[Equazione di Schrödinger|Schrödinger equation]] of the hydrogen atom is
$$\hat{H}=- \frac{\hbar^{2}}{2M}\nabla ^{2}_{R}- \frac{\hbar^{2}}{2m}\nabla^{2}_{r_{e}}- \frac{Ze^{2}}{4\pi \varepsilon_{0}r_{e}}$$
where $M$ is the [[mass]] of the nucleus, $m$ is the mass of the electron, $\hbar$ is the [[Planck constant|reduced Planck constant]], $Z$ is the [[Atom|atomic number]] (the number of protons), $\varepsilon_{0}$ is the [[vacuum permittivity]] and $r_{e}$ is the distance of the electron from the origin. The last term is the [[potential energy]] due to [[Interazione elettromagnetica|electromagnetic attraction]].
## Derivation
First things first, the end goal is finding the [[Funzione d'onda|wavefunction]] of the system. This wavefunction is of course dependent on the spatial coordinates, but since the electron carries [[spin]] ($s=1/2$ and $m_{s}=\pm1/2$ specifically), this will also be parameter. If we call $q$ the [[generalized coordinates]] of the wavefunction, we can write it as $\psi\equiv \psi(q)=\psi(r_{e},R,s,m_{s})$.

However, the Hamiltonian has no spin term. $s$ and $m_{s}$ never appear. This suggests that the wavefunction that we get by solving $\hat{H}\psi=E\psi$ is actually just the spatial part, with the spin part being a separate piece. Using [[separation of variables]], we can split the two:
$$\psi(q)\equiv \chi_{s,m_{s}}\psi(r_{e},R)$$
We can now solve these separately.
### The spin part
Since the Hamiltonian does not affect or depend on spin in any way, the spin part is just the eigenstates of the generic spin operator $\hat{S}$:
$$\hat{S}^{2}\chi_{s,m_{s}}=\hbar ^{2} s(s+1)\chi_{s,m_{s}},\quad S_{z}\chi_{s,m_{s}}=\hbar m_{s}\chi_{s,m_{s}}$$
Thankfully, we know the spin: it's $s=1/2$, and this is the special case that is already solved in [[Spin#Spin 1/2]]. We know the eigenvectors of both $\hat{S}^{2}$ and $\hat{S}_{z}$ in spin 1/2: they're somewhat up to preference, so we'll choose
$$\chi_{1/2,+1/2}=\begin{pmatrix}
1 \\ 0
\end{pmatrix},\quad \chi_{1/2,-1/2}=\begin{pmatrix}
0 \\ -1
\end{pmatrix}$$
And that's the spin part done already. The real challenge is solving the spatial part.
### The spatial part
Since we have a central potential, the system lends itself well to be rewritten in [[spherical coordinates]], as the Schrödinger equation has a general solution in this form. To do so, we make a first [[coordinate transformation]] to the [[frame of reference]] of the [[center of mass]]. We define the reduced mass as usual:
$$\mu=\frac{Mm}{M+m}$$
Then, using $\mu$ and expressing the [[Laplacian]] in the relative coordinate $\mathbf{r}=\mathbf{r}_{e}-\mathbf{R}$, the equation becomes
$$\hat{H}\psi(r)=\left[ - \frac{\hbar^{2}}{2\mu} \nabla ^{2}_{r}- \frac{Ze^{2}}{4\pi \varepsilon_{0}r}\right]\psi(r)=E\psi(r)$$
The benefit is that now we only depend on one [[Degrees of freedom|degree of freedom]] ($r$) instead of two ($r_{e},R$). (The frame follows the center of mass, so its coordinates are the origin; we don't need another variable for that). Then, the spherical coordinate transformation from [[Cartesian coordinates]] is
$$\begin{cases}
x=r\sin \theta \cos \phi \\
y=r\sin \theta \sin \phi \\
z=r\cos \theta
\end{cases},\quad-\pi\leq \theta\leq \pi,\quad 0\leq \phi\leq 2\pi$$
With this we can express the Laplacian in spherical coordinates. Writing the potential as $V(r)$ for brevity, the Hamiltonian operator in spherical coordinates is
$$\begin{align}
\hat{H}&=- \frac{\hbar^{2}}{2\mu}\left[ \frac{1}{r^{2}}\frac{ \partial  }{ \partial r } \left( r^{2}\frac{ \partial  }{ \partial r }  \right)+ \frac{1}{r^{2}\sin \theta}\frac{ \partial  }{ \partial \theta } \left( \sin \theta \frac{ \partial  }{ \partial \theta }  \right)+ \frac{1}{r^{2}\sin ^{2}\theta}\frac{ \partial ^{2}  }{ \partial \phi ^{2} }  \right]+V(r) \\
\end{align}$$
We now introduce what is arguably the key component of the system: the [[Momento angolare quantistico|quantum angular momentum]] $\hat{L}=\hat{r}\times \hat{p}=-i\hbar (\hat{r}\times \nabla)$[^1]. It is so important because if we express its [[gradient]] in spherical coordinates, then take the square, we get the equation
$$\hat{L}^{2}=-\hbar^{2}\left[ \frac{1}{\sin \theta}\frac{ \partial  }{ \partial \theta } \left( \sin \theta \frac{ \partial  }{ \partial \theta }\right) + \frac{1}{\sin ^{2} \theta}\frac{ \partial ^{2} }{ \partial \phi ^{2} }  \right]$$
We can see that $\hat{L}^{2}$ comes up exactly in the Hamiltonian, so with a simple substitution
$$\hat{H}=- \frac{\hbar^{2}}{2\mu}\left[ \frac{1}{r^{2}}\frac{ \partial  }{ \partial r } \left( r^{2}\frac{ \partial  }{ \partial r }  \right)- \frac{\hat{L}^{2}}{\hbar^{2}r^{2}} \right]+V(r)$$
With this, the spherical Schrödinger equation for the hydrogen atom is
$$\boxed{\left[ - \frac{\hbar^{2}}{2\mu r^{2}}\frac{ \partial  }{ \partial r } \left( r^{2}\frac{ \partial  }{ \partial r }  \right)+ \frac{\hat{L}^{2}}{2\mu r^{2}}- \frac{Ze^{2}}{4\pi \varepsilon_{0}r} \right]\psi(r,\theta,\phi)=E\psi(r,\theta,\phi)}$$
where the angular dependence of the system is entirely contained inside the angular momentum. As usual, the square angular momentum, the momentum on one axis ($z$) and the Hamiltonian all commute, $[\hat{L}^{2},\hat{L}_{z}]=[\hat{L}^{2},\hat{H}]=[\hat{L}_{z},\hat{H}]=0$, so they all share simultaneous eigenstates. This sets the foundation of our final solution.

For a general solution of this equation in spherical coordinates, using a generic potential $V$, see [[Equazione di Schrödinger#Soluzione tridimensionale]]. In there, we set $\psi(r,\theta,\phi)=R(r)Y(\theta,\phi)$, find that the angular component $Y(\theta,\phi)$ of the solution is universal, completely independent on the potential and described by the [[spherical harmonics]]. The radial component instead depends on $V$ and we must solve it uniquely for each the potential. As such, our next goal is to solve the radial component for our $V$. But first, a refresher on the angular part.
#### Angular part
The angular components depend on the eigenstates of $\hat{L}^{2}$ and $\hat{L}_{z}$ and are found using the spherical harmonics $Y_{l,m}(\theta,\phi)$:
$$\boxed{\hat{L}^{2}Y_{l,m}(\theta,\phi)=l(l+1)\hbar^{2}Y_{l,m}(\theta,\phi)}\qquad\hat{L}_{z}Y_{l,m}(\theta,\phi)=m\hbar Y_{l,m}(\theta,\phi)$$
Using spherical harmonics on $\hat{L}_{z}$ is a bit overkill, since it's really only dependent on $\phi$. In the general derivation, one finds that the harmonics themselves can go through [[separation of variables]] as $Y_{l,m}(\theta,\phi)=\Theta_{l,m}(\theta)\Phi_{m}(\phi)$. The $\Phi_{m}(\phi)$ function is pretty easy to solve and is found to be $\Phi_{m}(\phi)=e^{im\phi}$. The $\Theta_{l,m}(\theta)$ function is more complicated is requires invoking the [[Polinomi di Legendre|associated Legendre functions]] $P_{l,m}(\cos \theta)$ to get $\Theta(\theta)=AP_{l,m}(\cos \theta)$ ($A$ is some constant). As such, we can rewrite the $\hat{L}_{z}$ eigenstates as
$$\boxed{\hat{L}_{z}\Phi_{m}(\phi)=m\hbar \Phi_{m}(\phi)}$$
In the context of the hydrogen atom, the numbers $l$ and $m$ are given special names: $l$ is the **angular momentum [[Numero quantico|quantum number]]** and $m$ is the **magnetic angular momentum quantum number**.

Still, spherical harmonics are generally complex functions. We know very well that only real numbers can be measured from a system, so we need to bridge the gap. We do the usual: take the square modulus
$$\lvert Y_{l,m}(\theta,\phi) \rvert^{2} =\lvert \Theta_{l,m}(\theta) \rvert^{2}\lvert \Phi_{m}(\phi) \rvert^{2}  $$
Luckily, the modulus of $\Phi_{m}(\phi)$ is very easy: $\lvert \Phi_{m}(\phi) \rvert^{2}=\lvert e^{im\phi} \rvert^{2}=1/2\pi$. (Notably, it is completely independent of $m$.) Unluckily, the square modulus of $\Theta(\theta)$ isn't. They can, for instance, be found computationally and plotted in graphs or animations. Analytically, we'll remain with
$$\lvert Y_{l,m}(\theta,\phi) \rvert^{2} =\frac{1}{2\pi}\lvert \Theta_{l,m}(\theta) \rvert^{2}$$
An important detail: since the spherical harmonics for a given $l$ is spherically symmetrical over all $m$, so is the charge distribution (see [[Spherical harmonics#Symmetry]]).
#### Radial part
The radial part of the equation is is
$$\left[ - \frac{\hbar^{2}}{2\mu r^{2}} \frac{d}{dr} \left( r^{2} \frac{d}{dr}  \right)+ \frac{\hbar^{2}l(l+1)}{2\mu r^{2}}- \frac{Ze^{2}}{4\pi \varepsilon_{0}r} \right]R(r)=ER(r)$$
where we used $\hat{L}^{2}\psi=\hbar ^{2}l(l+1)\psi$ and rewrote the [[partial derivative|partial derivatives]] as regular derivatives since $r$ is now the only variable. We set $u(r)\equiv rR(r)$ to simplify things:
$$\left[ - \frac{\hbar^{2}}{2\mu } \frac{d^{2}}{dr^{2}}+ \frac{\hbar^{2}l(l+1)}{2\mu r^{2}}- \frac{Ze^{2}}{4\pi \varepsilon_{0}r} \right]u(r)=Eu(r)$$
Notice how there is a term dependent on the angular momentum number $l$ even in the radial term. What we do is to combine it with the potential term in a single, *effective* potential $V_\text{eff}$ defined as[^2]
$$\boxed{V_\text{eff}=-\frac{Ze^{2}}{4\pi \varepsilon_{0}r}+ \frac{\hbar^{2}l(l+1)}{2\mu r^{2}}}$$
which reduces the equation even further to
$$\left[ - \frac{\hbar^{2}}{2\mu}\frac{d^{2}}{dr^{2}}+ V_\text{eff}\right]u(r)=Eu(r)$$
This potential looks something like this:

![[Plot Effective spherical Schrodinger potential]]

Note that for $l=0$, the potential is purely attractive: nothing is stopping the electron from falling and crashing into the nucleus. But if we add a rotation ($l>0$), suddenly there is a spike of potential beyond a certain point which explains why electrons don't just collide with the nucleus. The value of $r$ at each potential well for $l>0$ should, in principle at least, correspond to the "allowed orbits" that the [[Bohr model]] identified. As always, the system is [[Stati in meccanica quantistica|bound]] if $E<0$ and [[Stati in meccanica quantistica|scattering]] if $E>0$.

Now, solving the radial part is not exactly trivial. For convenience, we introduce a few variables
$$\rho\equiv\sqrt{ - \frac{8\mu E}{\hbar ^{2}} } r,\qquad \lambda\equiv\frac{Ze^{2}}{4\pi \varepsilon_{0}\hbar}\sqrt{ - \frac{\mu}{2E} } =Z\alpha \sqrt{ - \frac{\mu c^{2}}{2E} }$$
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
Of course, as is, the wavefunctions have limited intepretability. But as with all quantum mechanical system, the square modulus of $\psi$ gives the [[probability]] of finding the system in a given state. Specifically, $\lvert \psi(r,\theta,\phi) \rvert^{2}d\mathbf{r}$ is the probability of finding an [[electric charge]] (the electron) in an infinitesimal volume element $d\mathbf{r}$. The probability of finding the electron at a set distance $r$ from the nucleus is found by integrating $\lvert \psi(r,\theta,\phi) \rvert^{2}$ over all angles.

[^1]: The angular momentum operator is found by quantizing the classical quantities of $r$ and $p$, which become $\hat{r}$ and $-i\hbar \nabla$ respectively ($\nabla$ is the [[gradient]]). So, we get $\hat{L}=-i\hbar(\hat{r}\times \nabla)$.

[^2]: If you recall the general solution, this extra term is known as the "centrifugal term". It represent the fact that more intense rotations (high $l$) tend to "push" outwards more. It's to quantum mechanics what the centrifugal force is to classical mechanics.
