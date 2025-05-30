---
wiki-publish: true
aliases:
  - hydrogenic atom
---
The **hydrogen atom** is the [[atom]] of the element hydrogen, a quantum [[physical system]] made up of a central positive [[Electric charge|charge carrier]] (a [[proton]]) and a negative charge carrier (an [[Elettrone|electron]]) surrounding it. It is the simplest case of a broader class of objects called **hydrogenic atoms** (or **hydrogen-like atoms**) which may possess a stronger central charge, that is, a full atomic [[Nucleo atomico|nucleus]].

![[Schema modello idrogeno|center]]

The [[Hamiltonian]] for the [[Equazione di Schrödinger|Schrödinger equation]] of the hydrogen atom is
$$\hat{H}=- \frac{\hbar^{2}}{2M}\nabla ^{2}_{R}- \frac{\hbar^{2}}{2m}\nabla^{2}_{r_{e}}- \frac{Ze^{2}}{4\pi \varepsilon_{0}r_{e}}$$
where $M$ is the [[mass]] of the nucleus, $m$ is the mass of the electron, $\hbar$ is the [[Planck constant|reduced Planck constant]], $Z$ is the [[Atom|atomic number]] (the number of protons), $\varepsilon_{0}$ is the [[vacuum permittivity]] and $r_{e}$ is the distance of the electron from the origin. The last term is the [[potential energy]] due to [[Interazione elettromagnetica|electromagnetic attraction]].
## Derivation
First things first, the end goal is finding the [[Funzione d'onda|wavefunction]] of the system. We'll solve it in [[Rappresentazioni dello stato|position representation]], $\psi(r)=\braket{ r | \psi }$. This wavefunction is of course dependent on the spatial coordinates, but since the electron carries [[spin]] ($s=1/2$ and $m_{s}=\pm1/2$ specifically), this will also be parameter. If we call $q$ the [[generalized coordinates]] of the wavefunction, we can write it as $\psi\equiv \psi(q)=\psi(r_{e},R,s,m_{s})$.

However, the Hamiltonian has no spin term. $s$ and $m_{s}$ never appear. This suggests that the wavefunction that we get by solving $\hat{H}\psi=E\psi$ is actually just the spatial part, with the spin part being a separate piece. Using [[separation of variables]], we can split the two:
$$\psi(q)\equiv \chi_{sm_{s}}\psi(r_{e},R)$$
We can now solve these separately.
### The spin part
Since the Hamiltonian does not affect or depend on spin in any way, the spin part is just the eigenstates of the generic spin operator $\hat{S}$:
$$\hat{S}^{2}\chi_{sm_{s}}=\hbar ^{2} s(s+1)\chi_{sm_{s}},\quad S_{z}\chi_{sm_{s}}=\hbar m_{s}\chi_{sm_{s}}$$
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
The benefit is that now we only depend on one [[Degrees of freedom|degree of freedom]] ($r$) instead of two ($r_{e},R$). (Effectively, it's a single particle located in $r$ of mass $\mu$ subject to the potential). Then, the spherical coordinate transformation from [[Cartesian coordinates]] is
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
In the context of the hydrogen atom, the numbers $l$ and $m$ are given special names: $l$ is the **azimuthal [[Numero quantico|quantum number]]** and $m$ is the **magnetic azimuthal quantum number**.

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
or equivalently
$$\frac{d^{2}u(r)}{dr^{2}}+ \frac{2\mu}{\hbar ^{2}}[E-V_\text{eff}]u(r)=0$$
This potential looks something like this:

![[Plot Effective spherical Schrodinger potential]]

Note that for $l=0$, the potential is purely attractive: nothing is stopping the electron from falling and crashing into the nucleus. But if we add a rotation ($l>0$), suddenly there is a spike of potential beyond a certain point which explains why electrons don't just collide with the nucleus. The value of $r$ at the bottom of each potential well for $l>0$ should, in principle at least, correspond to the "allowed orbits" that the [[Bohr model]] identified. As always, the system is [[Stati in meccanica quantistica|bound]] if $E<0$ and [[Stati in meccanica quantistica|scattering]] if $E>0$.

Now, solving the radial part is not exactly trivial. First, to solve a (1D) differential equation like the Schrödinger equation we need a boundary condition, which we have not set up until now. We'll set $u(0)=0$, as that prevents the wavefunction from blowing up to infinity when $r=0$[^3].

For convenience, we introduce a couple of dimensionless variables
$$\rho\equiv\sqrt{ - \frac{8\mu E}{\hbar ^{2}} } r,\qquad \lambda\equiv\frac{Ze^{2}}{4\pi \varepsilon_{0}\hbar}\sqrt{ - \frac{\mu}{2E} }$$
This leads to
$$\frac{d}{dr}=\frac{d}{d\rho} \frac{d\rho}{dr}=\frac{d}{d\rho} \sqrt{ - \frac{8\mu E}{\hbar ^{2}} } \frac{dr}{dr}=\sqrt{ - \frac{8\mu E}{\hbar ^{2}} } \frac{d}{d\rho}$$
and so
$$\frac{d^{2}}{dr^{2}}=- \frac{8\mu E}{\hbar ^{2}} \frac{d^{2}}{d\rho ^{2}}$$
If we substitute these in the equation (with $V_\text{eff}$ expanded), we get
$$\begin{align}
&- \frac{8\mu E}{\hbar ^{2}} \frac{d^{2}u(\rho)}{d\rho ^{2}}+ \frac{2\mu}{\hbar ^{2}}\left[ E- \frac{Ze^{2}}{4\pi \varepsilon_{0}\rho}\sqrt{ - \frac{8\mu E}{\hbar ^{2}} } + \frac{\hbar^{2}l(l+1)}{2\mu \rho ^{2}}\left( - \frac{8\mu E}{\hbar ^{2}} \right) \right]u(\rho)=0 \\
&\left[ - \frac{8\mu E}{\hbar ^{2}} \frac{d^{2}}{d\rho ^{2}}+ \frac{2\mu}{\hbar ^{2}}E- \frac{2\mu}{\hbar ^{2}} \frac{Ze^{2}}{4\pi \varepsilon_{0} \rho}\sqrt{ - \frac{8\mu E}{\hbar ^{2}} }+ \frac{2\mu}{\hbar ^{2}} \frac{4El(l+1)}{\rho ^{2}} \right] u(\rho)=0 \\
&- \frac{8\mu E}{\hbar ^{2}}\left[ \frac{d^{2}}{d\rho ^{2}}- \frac{1}{4} + \frac{2\mu}{\hbar ^{2}} \frac{Ze^{2}}{4\pi \varepsilon_{0}\rho}\sqrt{ - \frac{\hbar^{2}}{8\mu E} }- \frac{1}{4} \frac{4l(l+1)}{\rho ^{2}} \right]u(\rho)=0 \\
&\left[ \frac{d^{2}}{d\rho ^{2}}- \frac{1}{4}+ \frac{Ze^{2}}{4\pi \varepsilon_{0}\hbar\rho} \sqrt{ - \frac{\mu}{2E} }- \frac{l(l+1)}{\rho ^{2}} \right]u(\rho)=0
\end{align}$$
Noticing $\lambda$ in the middle leads us to
$$\left[ \frac{d^{2}}{d\rho ^{2}} - \frac{l(l+1)}{\rho ^{2}}+ \frac{\lambda}{\rho}- \frac{1}{4}\right]u(\rho)=0$$
A much simpler form, but still quite abstract. Instead of diving head-first into solving it, we can start by analyzing asymptotic behavior. When $\rho\to \infty$, the equations greatly simplifies to
$$\left[ \frac{d^{2}}{d\rho ^{2}}- \frac{1}{4} \right]u(\rho)=0$$
This a linear second order [[Ordinary differential equation|ODE]] of the form $\ddot{u}- \frac{1}{4}u=0$ and the solution is an exponential. Thus, for high $\rho$, we have
$$u(\rho)\sim e^{\pm \rho/2}$$
Using the fact that $u(\rho)$ must be bounded everywhere, we keep only the negative sign. Since we have an asymptotic solution, we can claim that the general solution behaves in the same manner as the asymptote, but scaled by some other function $f(\rho)$. Thus, in general, in and out of the asymptote:
$$u(\rho)=f(\rho)e^{-\rho/2}$$
By definition, $f(\rho)$ must contain all of the information about $E$ and $l$, since those are not present in the asymptotic term: $f(\rho)\equiv f_{E,l}(\rho)$. Thus, since
$$\frac{d^{2}}{d\rho ^{2}}(f(\rho)e^{-\rho/2})=e^{-\rho/2}\left[ \frac{d^{2}}{d\rho ^{2}}- \frac{d}{d\rho}+ \frac{1}{4} \right]f(\rho)$$
our new equation to solve is
$$\left[ \frac{d^{2}}{d\rho ^{2}}- \frac{d}{d\rho} - \frac{l(l+1)}{\rho ^{2}}+ \frac{\lambda}{\rho}\right]f(\rho)=0\tag{1}$$
Our next problem is finding $f(\rho)$.
#### Finding $f(\rho)$
To start, we again look at asymptotic behavior:
$$\lim_{ \rho \to 0 } \left[ \frac{d^{2}}{d\rho ^{2}}- \frac{d}{d\rho}- \frac{l(l+1)}{\rho ^{2}} + \frac{\lambda}{\rho}\right]f(\rho)=0$$
This can only be true if $f(\rho)\sim \rho^{l+1}$. In fact, using the definition of $f(\rho)\sim \rho^{s+1}$:
$$(s+1)s \rho^{s-1}- (s+1)\rho^{s}-l(l+1)\rho^{s-1}+\lambda \rho^{s}\to0$$
But only the dominant term $\rho^{s-1}$ matters in the limit so this is like saying
$$(s+1)s\rho^{s-1}-l(l+1)\rho^{s-1}=[s(s+1)-l(l+1)]\rho^{s-1}\to 0$$
Since $\rho^{s-1}>0$ for all $\rho$, this is true only if $s=l$, which proves that $f(\rho)\sim \rho^{l+1}$.

Outside of the asymptote, $f(\rho)$ must behave something like $f(\rho)=\rho^{l+1}g(\rho)$ where $g(\rho)$ is some function. As an added note, this means that our current understanding of $u(\rho)$ is $u(\rho)=e^{-\rho/2}\rho^{l+1}g(\rho)$. We now substitute this in $(1)$ to get
$$\left[ \rho \frac{d^{2}}{d\rho ^{2}}+ (2l+2-\rho) \frac{d}{d\rho}+ (\lambda-l-1) \right]g(\rho)=0\tag{2}$$
This equation can be solved analytically by expanding $g(\rho)$ in its [[power series]]
$$g(\rho)=\sum_{k=0}^{\infty} c_{k}\rho^{k}\quad\text{for }c_{0}\neq 0$$
Taking the derivatives of this power series yields
$$\sum_{k=0}^{\infty}\left[ k(k-1)c_{k}\rho^{k-1}+ (2l+2-\rho)kc_{k}\rho^{k-1}+(\lambda-l-1)c_{k}\rho^{k} \right]=0$$
Split the sum like so
$$\sum_{k=0}^{\infty} [k(k-1)c_{k}\rho^{k-1}+(2l+2-\rho)kc_{k}\rho^{k-1}]+\sum_{k=0}^{\infty}(\lambda-l-1)c_{k}\rho^{k} =0$$
and the first sum is further split as
$$\sum_{k=0}^{\infty} [k(k-1)c_{k}\rho^{k-1}+(2l+2)kc_{k}\rho^{k-1}]+\sum_{k=0}^{\infty} [-kc_{k}\rho^{k}]+\sum_{k=0}^{\infty}(\lambda-l-1)c_{k}\rho^{k} =0$$
Changing the index from $k$ to $k+1$ in the first yields the equivalent form
$$\sum_{k=0}^{\infty} [k(k+1)+(2l+2)(k+1)]c_{k+1}\rho^{k}$$
Plug this in, combine the sums again and collect $\rho^{k}$ to get
$$\sum_{k=0}^{\infty} [(k(k+1)+(2l+2)(k+1))c_{k+1}+(\lambda-l-1-k)c_{k}]\rho^{k}=0$$
This is true for all $\rho$, which means that each component must be zero termwise:
$$(k(k+1)+(2l+2)(k+1))c_{k+1}+(\lambda-l-1-k)c_{k}=0$$
which yields the recurrence relation
$$c_{k+1}=\left[ \frac{k+l+1-\lambda}{(k+1)(k+2l+2)} \right]c_{k}$$
For large $k$, the ratio is approximately
$$\frac{c_{k+1}}{c_{k}}\sim \frac{1}{k}$$
As it happens, this ratio is the same as that of the series for $\rho^{p}e^{\rho}$ with $p \in \mathbb{R}$. This implies that $g(\rho)$ has this very behavior
$$g(\rho)\sim \rho^{p}e^{\rho}\quad\text{for some }p \in \mathbb{R}$$
Combined with our previous result $u(\rho)=e^{-\rho/2}\rho^{l+1}g(\rho)$, this implies that the asymptotic behavior of $u(\rho)$ is something of the form $u(\rho)\sim\rho^{l+1+p}e^{\rho/2}$. But this can't be, for it would break our previous assumption of $u(\rho)\sim e^{-\rho/2}$ (and by extension the normalizability of the wavefunction). Thus the series must terminate early, which is to say that it must be a polynomial in $\rho$. We shall call $n_{r}$ the rank of the polynomial, the **radial quantum number**, and it is a nonnegative integer (possibly zero). This means that any terms of index $k>n_{r}$ must be zero and that the highest term is $c_{n_{r}}\rho^{n_{r}}$.

Using the recurrence relation we can state
$$c_{n_{r}+1}=0=\frac{n_{r}+l+1-\lambda}{(n_{r}+1)(n_{r}+2l+2)}c_{n_{r}}$$
Multiply both sides by the denominator to get
$$(n_{r}+l+1-\lambda)c_{n_{r}}=0$$
but we know that $c_{n_{r}}\neq 0$, so it must be that
$$\lambda=n_{r}+l+1$$
We'll rename this to $n$
$$n\equiv n_{r}+l+1$$
and we shall call it the **principal quantum number**. Since $n_{r}=0,1,2,\ldots$ and $l=0,1,2,\ldots$, we have $n=1,2,3,\ldots$.
#### Eigenvalues
Now that we finally know what $\lambda$ is, we can invert its definition to extract $E$, substitute $\lambda$ for $n$ and get the [[Stationary state|energy eigenvalues]]:
$$E_{n}=- \frac{1}{2n^{2}}\left( \frac{Ze^{2}}{4\pi \varepsilon_{0}} \right)^{2} \frac{\mu}{\hbar ^{2}}=- \frac{e^{2}}{4\pi \varepsilon_{0}a_{0}} \frac{\mu}{m} \frac{Z^{2}}{2n^{2}}=- \frac{e^{2}}{4\pi \varepsilon_{0}a_{\mu}} \frac{Z^{2}}{2n^{2}}$$
where we used the [[Bohr radius]] $a_{0}$ and modified Bohr radius $a_{\mu}=a_{0} (m/\mu)$. Thus, after all this derivation, we have the expression for the allowed energy levels of the hydrogen atom:
$$\boxed{E_{n}=- \frac{e^{2}}{4\pi \varepsilon_{0}a_{\mu}} \frac{Z^{2}}{2n^{2}}}$$

:::image
![[Hydrogen atom energy levels.png]]
A plot depicting the energy levels of the hydrogen atom for different $n$ and $l$. Notice how the variation of $l$ makes no difference due to degeneracy. From *Bransden & Joachain - Physics of atoms and molecules*.
:::

Notably, the energy eigenvalues are *not* dependent on $l$ (not directly, at least). This means that the energy eigenstates are [[Degenerazione|degenerate]] in $l$ too, not just $m$. For each $n$ there are $n-1$ values of $l$, and for each $l$ there are $2l+1$ values of $m$, which leads to a total eigenvalue degeneracy of
$$d=\sum_{l=0}^{n-1} (2l+1)=2 \frac{n(n-1)}{2}+n=n^{2}$$
The degeneracy with respect to $m$ is universal for spherically symmetric systems, but the degeneracy in $l$ is actually specific to the Coulomb potential, or rather potentials that go like $V\sim 1/r$. In fact, were the potential to behave differently, the $l$ degeneracy would be lifted and we'd have $n$ distinct states for each principal level $n$. This happens, for instance, in the outer electrons of an atom with more than one [[electron shell model|electron shell]], which are also subject to the repulsion of inner electrons, changing the effective potential to a different shape than $\sim1/r$. You can see this in the [[Many-electron atom]] article. In a sense, the $l$ degeneracy has little to do with the shape of an atom specifically: anything around a point charge would work the same.

The levels themselves are infinite and tend towards zero as you get further from the nucleus: this shouldn't be surprising considering that the electromagnetic potential of a point charge (the thing that is responsible for keeping the electron anchored to the nucleus) falls off with distance. They also get progressively closer to one another for larger $n$. The difference between $n=1$ and $n=2$ is bigger than that between $n=2$ and $n=3$ and so on.

Furthermore, these energy levels are *identical* to those obtained from the Bohr model of the atom. Despite being a (semi)classical model, it already got the quantum levels correct down to the equation. But what it couldn't do, however, are the eigenstates themselves.
#### Eigenstates
To compute the eigenstate, we look back at $(2)$. Earlier, we looked only at the asymptotic behavior, which led us to the definition of the radial and principal quantum numbers and $\lambda=n$. We now want to find the actual solutions themselves. This is a second order [[ordinary differential equation]] in $\rho$ and luckily, a similar equation has already been solved in the past.

The (generalized) [[Laguerre's differential equation]] is the following second order [[Ordinary differential equation|ODE]]:
$$\left[ \rho \frac{d^{2}}{d\rho^{2}}+(p+1-\rho) \frac{d}{d\rho}+q \right]L_{q}^{p}(\rho)=0$$
whose solutions $L_{q}^{p}(\rho)$ are the [[Laguerre polynomials|associated Laguerre polynomials]]
$$L_{q}^{p}(\rho)\equiv \frac{x^{-p}e^{\rho}}{q!} \frac{d^{q}}{d\rho^{q}}(\rho^{q+p}e^{-\rho})$$
for some nonnegative integers $q$ and $p$. This should ring a bell: it is basically just $(2)$ with slightly different variables. In fact, if we equate the differences we get
$$\begin{cases}
p+1-\rho=2l+2-\rho \\
q=n-l-1 \\
g(\rho)=L_{q}^{p}(\rho)
\end{cases}\quad\Rightarrow \quad \begin{cases}
p=2l+1 \\
q=n-l-1 \\
g(\rho)=L_{q}^{p}(\rho)
\end{cases}$$
Thus, the physically valid solutions of $(2)$ are
$$g(\rho)=AL_{n-l-1}^{2l+1}(\rho)$$
where $A$ is some [[normalization]] constant. Substituting $r$ for $\rho$ and substituting $g(\rho)$ into $R(r)$ (after unwinding all the functions we've added)
$$R_{nl}(r)=\frac{u(r)}{r}=\frac{na_{\mu}}{2Z} \frac{f(\rho)e^{-\rho/2}}{\rho}=\frac{na_{\mu}}{2Z}\frac{g(\rho)\rho^{l+1}e^{-\rho/2}}{\rho}=A\rho^{l}e^{-\rho/2}L_{n-l-1}^{2l+1}(\rho)$$
where in the last step we have absorbed $na_{\mu}/2Z$ inside $A$ since they are both constants. Calculating the constant (see below) yields the radial wavefunction:
$$\boxed{R_{nl}(\rho)=- \sqrt{ \left( \frac{2Z}{na_{\mu}} \right)^{3} \frac{(n-l-1)!}{2n[(n+l)!]^{3}} }\rho^{l}e^{-\rho/2}L_{n-l-1}^{2l+1}(\rho)}$$
#### Spatial wavefunction
This completes our proof: we've assembled all the pieces we need to determine the spatial wavefunction of the hydrogenic atom, which is the product of the the radial part and the angular part:
$$\boxed{\psi_{nlm}(r,\theta,\phi)=- \sqrt{ \left( \frac{2Z}{na_{\mu}} \right)^{3} \frac{(n-l-1)!}{2n[(n+l)!]^{3}} }\left( \frac{2Z}{na_{\mu}} \right)^{l}e^{-Z/na_{\mu}}L_{n-l-1}^{2l+1}\left( \frac{2Z}{na_{\mu}} \right)Y_{lm}(\theta,\phi)}$$
where
$$\rho=\frac{2Z}{na_{\mu}}r=\frac{2Z}{na_{0}} \frac{M}{m}r$$

> [!tip]- Wavefunction normalization
> To normalize the wavefunction, start as usual
> $$\begin{align}
> 1=\int_{\mathbb{R}^{3}}\lvert \psi_{nlm}(\rho,\theta,\phi) \rvert ^{2}d^{3}r & =\int_{\mathbb{R}^{3}} \lvert R_{nl}(\rho)Y_{lm}(\theta,\phi) \rvert r^{2}\sin \theta \ dr d\theta d\phi \\
> &=\int_{0}^{\infty}\lvert R_{nl}(\rho) \rvert ^{2}r^{2}\ dr\underbrace{ \int_{0}^{2\pi}\int_{0}^{\pi}\lvert Y_{lm}(\theta,\phi) \rvert ^{2} \sin \theta  d\phi d\theta }_{ 1 } \\
> &=\int_{0}^{\infty}\lvert R_{nl}(\rho) \rvert ^{2}r^{2}\ dr
> \end{align}$$
> since spherical harmonics are already normalized. Then
> $$1=\lvert A \rvert^{2} \int_{0}^{\infty} \rho^{2l}e^{-\rho}[L_{n-l-1}^{2l+1}(\rho)]^{2} r^{2} dr$$
> Use the definition of $\rho$ to substitute
> $$dr=\frac{na_{\mu}}{2Z}d\rho,\quad r^{2}=\left( \frac{na_{\mu}}{2Z} \right)^{2}\rho ^{2}$$
> and get
> $$1=\lvert A \rvert^{2} \left( \frac{na_{\mu}}{2Z} \right)^{3}\int_{0}^{\infty}\rho^{2l}e^{-\rho}[L_{n-l-1}^{2l+1}(\rho)]^{2}\rho ^{2}d\rho$$
> Now, this integral is *very hard*[^4]. Fortunately, someone else did the math already: in the [Mathematical Handbook of Formulas and Tables](http://mcb111.org/w01/Mathematical_Handbook_of_Formulas_and_Ta.pdf), a special result for the associated Laguerre polynomials (Eq. 30.50) precisely solves this integral. After due substitutions[^5], the result is
> $$\begin{align}
> \int_{0}^{\infty}\rho^{2l+2}e^{-\rho}[L_{n-l-1}^{2l+1}(\rho)]^{2}d\rho&=\frac{[2(n-l-1)+2l+2](n-l-1+2l+1)!}{(n-l-1)!} \\
> &=\frac{2n(n+l)!}{(n-l-1)!}
> \end{align}$$
> If we plug this in the former equation, extract $\lvert A \rvert^{2}$, take the square root and choose the negative solution, we get
> $$A=-\sqrt{ \left( \frac{2Z}{na_{\mu}} \right)^{3} \frac{(n-l-1)!}{2n(n+l)!} }$$

##### Results
Each of these wavefunctions represents a possible state of the electron around the nucleus, bringing along the baggage of all the probabilities of *where* it might be at any given time while "orbiting" the nucleus. In fact, this classical concept of "orbit" remained so prevalent throughout the years that it gave the special name we use to refer to these wavefunctions: **[[orbital|orbitals]]**. Common in chemistry too, we use a specific naming scheme to specify which orbital we are talking about, called [[spectroscopic notation]].

As is, the orbitals have limited intepretability. But as with all quantum mechanical system, the square modulus of $\psi_{nlm}$ gives the [[probability]] of finding the system in a given state. Specifically, $\lvert \psi_{nlm}(r,\theta,\phi) \rvert^{2}d\mathbf{r}$ is the probability of finding the electron in an infinitesimal volume element $d\mathbf{r}$ and is thus effectively the (shape of the) *volume charge distribution* of the hydrogen atom. Meanwhile, the probability of finding it at a distance $r$ anywhere around the nucleus is found by integrating $\lvert \psi_{nlm}(r,\theta,\phi) \rvert^{2}$ over all angles. This leads to what's known as a **density function**
$$\boxed{D_{nl}(r)=r^{2}\lvert R_{nl}(r) \rvert ^{2}}$$
since $Y_{lm}(\theta,\phi)$ are normalized. The first few radial wavefunction and their corresponding densities look like this.

:::image
![[Hydrogen atom radial distribution.png]]
From *Bransden & Joachain - Physics of atoms and molecules*
:::

Other visualizations of the wavefunctions are the $xy$-plane section plot below, where you can see the black lines representing the nodes (i.e. the zeros) of the wavefunctions.

:::image
![[Hydrogen atom orbitals.png]]
Unknown author - Originally uploaded by FlorianMarquardt, 14 Oct 2002., CC BY-SA 3.0, from [Wikipedia](https://commons.wikimedia.org/w/index.php?curid=75046)
:::

Also see this website, which provides an interactive simulation of the orbitals: https://www.falstad.com/qmatom/.
### Total wavefunction
Now that we painstakingly solved both the spin and spatial parts, we can put them together to officially have the full wavefunction of the hydrogen atom:
$$\boxed{\psi_{nlm_{l}sm_{s}}(r,\theta,\phi)=\chi_{sm_{s}}R_{nl}(r)Y_{lm_{l}}(\theta,\phi)}$$
where $m$ was renamed to $m_{l}$ to better distinguish it from the spin magnetic number $m_{s}$. It is dependent on five quantum numbers, of which four variable:
- $n$ is the principal quantum number ($n=1,2,3,\ldots$)
- $l$ is the azimuthal quantum number ($l< n$)
- $m_{l}$ is the magnetic azimuthal quantum number ($-l\leq m_{l}\leq l$)
- $s$ is the spin quantum number ($s=1/2$ for electrons)
- $m_{s}$ is the magnetic spin quantum number ($s=\pm 1$ for electrons)

Notably, the spatial part of the wavefunction is a usual complex valued function. However, the spin part is a *vector*, with two components. This means that the operation we're doing here is scalar multiplication of the spin vector by the spatial wavefunction: in other words, the total wavefunction is a two-dimensional vector, not a number.

For the curious, this is what the wavefunction looks like with all nested functions written out explicitly
$$\begin{align}
\psi_{nlm_{l}sm_{s}}(r,\theta,\phi)=&-\chi_{sm_{s}} \sqrt{ \left( \frac{2Z}{na_{\mu}} \right)^{3} \frac{(n-l-1)!}{2n[(n+l)!]^{3}} }\left( \frac{2Z}{na_{\mu}} \right)^{l}e^{-Z/na_{\mu}} \\
&\left( \frac{2Z}{na_{\mu}} \right)^{-2l-1}\frac{e^{ 2Z/na\mu }}{(n-l-1)!} \frac{d^{n-l-1}}{d\left( \frac{2Z}{na_{\mu}} \right)^{n-l-1}} \\
&\left[ \left( \frac{2Z}{na_{\mu}} \right)^{n+l}e^{-2Z/na_{\mu}} \right]\sqrt{\frac{2l+1}{4\pi} \frac{(l-m_{l})!}{(l+m_{l})!}}e^{im_{l}\phi}(1-\cos^{2}\theta)^{|m_{l}|/2}  \\
&\frac{d^{\lvert m \rvert }}{d\cos \theta^{\lvert m \rvert }}\left[ \frac{1}{2^{l}l!} \left(\frac{d}{d\cos \theta}\right)^{l}(\cos^{2}\theta-1)^{l} \right]
\end{align}$$
## The fine structure
Although the wavefunction above provides good results, it still uses the Schrödinger equation as its starting point. The issue with this is that the Schrödinger equation does not consider the effects of relativity, and since electrons move with average speeds in the order of 1% of the [[speed of light]], this leads to minor, but still significant discrepancies when comparing theory with experiment.

The formally correct way of handling this would be to start from relativistic quantum mechanics and the [[Dirac equation]]. However, that is beyond the scope of this section, and it is also historically misplaced. Before the Dirac equation was even developed, relativistic corrections to the hydrogen atom were already discovered and calculated by using [[Teoria delle perturbazioni|perturbation theory]], specifically time-independent perturbation theory. Namely, three corrections were developed: **relativistic kinetic energy**, **spin-orbit coupling** and the **Darwin term**. Each of these made the eigenvalues just a little closer to reality, matching the differences that we see in the laboratory. Together, these corrections are known as the **fine structure** of the hydrogen atom.

This is a very qualitative description of the fine structure. Please refer to e.g. Appendix 7 of Bransden & Joachaim for a rigorous derivation.

Our perturbed Hamiltonian will be
$$H=H_{0}+H'$$
where
$$H_{0}=\frac{p^{2}}{2m}- \frac{Ze^{2}}{4\pi \varepsilon_{0}r}$$
is our usual Hamiltonian (the quantity, not the operator, note the lack of hat on $H$) for a charged particle (our electron) in a central Coulomb potential and
$$H'\equiv H_{1}'+H_{2}'+H_{3}'$$
will be the perturbation due to the three aforementioned corrections.
### Relativistic kinetic energy
In relativity, the energy of the body is not just [[Kinetic energy|kinetic]]. We must use the full [[relativistic energy]] $E=\sqrt{ p^{2}c^{2}+m^{2}c^{4} }$, from which we get the kinetic energy as
$$K=E-E_{0}=\sqrt{ p^{2}c^{2}+m^{2}c^{4} }-mc^{2}=mc^{2}\sqrt{ 1+ \frac{p^{2}}{m^{2}c^{2}} }-mc^{2}$$
If $p^{2}/mc^{2}\ll 1$, which is our case, we can expand the square root in a [[Taylor series]] of $p^{2}/mc^{2}$:
$$\sqrt{ 1+ \frac{p^{2}}{m^{2}c^{2}} }\simeq1+ \frac{1}{2} \frac{p^{2}}{m^{2}c^{2}}- \frac{1}{8} \frac{p^{4}}{m^{4}c^{4}}$$
Plugging this into the previous equation gives an approximate kinetic energy of
$$K\simeq \frac{p^{2}}{2m}- \frac{1}{8} \frac{p^{4}}{m^{3}c^{2}}$$
The first term is very clearly the classical kinetic energy, whereas the second is a term that is unique to relativity. This is the **relativistic correction to kinetic energy**:
$$\boxed{H_{1}'=- \frac{1}{8} \frac{p^{4}}{m^{3}c^{2}}}$$
The correction to the eigenvalues is given by the average of the perturbation in the generic orbital (i.e. the eigenstates of $H_{0}$)
$$\begin{align}
\Delta E_{1}&=\braket{ \psi_{nlm_{l}m_{s}} | - \frac{p^{4}}{8m^{3}c^{2}} | \psi_{nlm_{l}m_{s}} }  \\
&=- \frac{1}{2mc^{2}}\braket{ \psi_{nlm_{l}} | \left( \frac{p^{2}}{2m} \right)^{2} | \psi_{nlm_{l}}  }  \\
&=- \frac{1}{2mc^{2}}\braket{ \psi_{nlm_{l}} | \left( H_{0}+ \frac{Ze^{2}}{4\pi \varepsilon r} \right)^{2} | \psi_{nlm_{l}}  } \\
\end{align}$$
This equation can be further developed to get
$$\boxed{\Delta E_{1}=- E_{n} \frac{(Z\alpha)^{2}}{n^{2}}\left[ \frac{3}{4}- \frac{n}{l+1/2} \right]}$$
where $\alpha$ is a constant aptly known as the **[[fine-structure constant]]**.
### Spin-orbit correction
The spin-orbit term takes the effect of the interaction between spin and angular momentum of the electron into account. The easiest way to reach it is by considering the [[frame of reference]] in which the electron is not moving and the nucleus is rotating around it. In such a frame, the [[Electric field|electric]] and [[Magnetic field|magnetic fields]] are
$$\mathbf{E}=- \frac{dV}{dr}\hat{\mathbf{r}},\quad\mathbf{B}=- \frac{1}{c^{2}}\mathbf{v}\times \mathbf{E}$$
The magnetic field can be developed as
$$\mathbf{B}=- \frac{1}{c^{2}}\mathbf{v}\times\left( - \frac{1}{r} \frac{dV}{dr} \right)\mathbf{r}=- \frac{1}{c^{2}r} \frac{dV}{dr}(\mathbf{r}\times \mathbf{v})=- \frac{1}{mc^{2}r} \frac{dV}{dr}\mathbf{L}$$
The intrinsic [[magnetic dipole moment]] of the electron is the [[Bohr magneton]]:
$$\boldsymbol{\mu}_{B}=- \frac{e}{m}\mathbf{S}$$
Thus, the energy is given by the usual formula for a [[magnetic dipole]]:
$$H_{2}'=-\boldsymbol{\mu}_{B}\cdot \mathbf{B}=- \frac{1}{mc^{2}} \frac{e}{r} \frac{dV}{dr} \mathbf{L}\cdot \mathbf{S}$$
Evaluating the derivative gives the **spin-orbit correction**:
$$\boxed{H_{2}'=\frac{Ze^{2}}{8m^{2}c^{2}\pi \varepsilon_{0}r^{3}}\mathbf{L}\cdot \mathbf{S}}$$
This correction does not commute with neither $L_{z}$ nor $S_{z}$, so to find the eigenvalue correction we must first identify some states that [[Diagonalization|diagonalize]] $H_{2}'$. To do so, we introduce the total angular momentum
$$\mathbf{J}\equiv \mathbf{L}+\mathbf{S}$$
which associated quantum numbers $j$ and $m_{j}$. This allows us to write the [[scalar product]] as
$$\mathbf{L}\cdot \mathbf{S}=\frac{1}{2}(\mathbf{J}-\mathbf{L}^{2}-\mathbf{S}^{2})$$
A good [[basis]] is the one given by the states
$$\ket{\psi_{nlm_{l}m_{s}}} \equiv \sum_{m_{l},m_{s}}\braket{ \frac{1}{2}lm_{l}m_{s} | jm_{j} } \ket{\chi_{m_{s}}\psi_{nlm_{l}}} $$
The scalar product in the sum are a well-known set of numbers called the [[Clebsch-Gordan coefficients]] for $s=1/2$. In these states we have the eigenvalue equations
$$\begin{cases}
\mathbf{L}^{2}\ket{\psi_{nljm_{j}}} =\hbar l(l+1)\ket{\psi_{nljm_{j}}}  \\
\mathbf{S}^{2}\ket{\psi_{nljm_{j}}} =\hbar s(s+1)\ket{\psi_{nljm_{j}}} =\frac{3}{4}\hbar \ket{\psi_{nljm_{j}}}  \\
\mathbf{J}^{2}\ket{\psi_{nljm_{j}}} =\hbar j(j+1)\ket{\psi_{nljm_{j}}} \\
J_{z}\ket{\psi_{nljm_{j}}} =\hbar m_{j}\ket{\psi_{nljm_{j}}}  \\
H_{0}\ket{\psi_{nljm_{j}}} =E_{n}\ket{\psi_{nljm_{j}}} 
\end{cases}$$
Since $s=1/2$, the values for $j$ are $j=s\pm1/2$, while $m_{j}=-j,-j+1,\ldots,j-1,j$ as with all magnetic spin numbers. The energy correction can now be calculated:
$$\Delta E_{2}=\braket{ \psi_{nljm_{j}} | H_{2}'|\psi_{nljm_{j}} } =\frac{\hbar^{2}}{2}\left[ j(j+1)-l(l+1)- \frac{3}{4} \right]\braket{ \psi_{nljm_{j}} | \frac{Ze^{2}}{4m^{2}c^{2}\pi \varepsilon_{0}r^{3}}| \psi_{nljm_{j}} } $$
It can be proven that
$$\braket{ \psi_{nljm_{j}} | \frac{1}{r^{3}} |\psi_{nljm_{j}} }=\frac{Z^{3}}{a_{0}^{3}n^{3}l\left( l+ \frac{1}{2} \right)(l+1)}$$
Using
$$E_{n}=- \frac{mc^{2}}{2} \frac{(Z\alpha)^{2}}{n^{2}}$$
this leads to three possible values:
$$\boxed{\Delta E_{2}=\left\{\begin{align}
&-\frac{E_{n}}{2}\frac{(Z\alpha)^{2}}{ nl\left( l+ \frac{1}{2} \right)(l+1) }&\text{if }j=l+ \frac{1}{2} \\
&\frac{E_{n}}{2}\frac{(Z\alpha)^{2}}{ nl\left( l+ \frac{1}{2} \right)(l+1) }&\text{if }j=l- \frac{1}{2} \\
&0&\text{if }j=\frac{1}{2}
\end{align}\right.}$$
### Darwin term
The last correction is due to the [[Disuguaglianza di Heisenberg|Heisenberg inequality]]. Since the concept of "size" is not well-defined in quantum mechanics, the electron is non-localized and is not very well described by a point charge. The Darwin term consists of treating the electron as a cloud of charge described by a volume charge distribution. To do so, we starting by recalling that the usual [[electric potential]] for a point charge $e$ goes like
$$\phi(r)\sim \frac{e}{r}$$
We now introduce a new vector $\mathbf{u}$ which identifies the position of a point in the cloud, starting from the center of the cloud. If $\mathbf{r}$ is the center of the cloud, then $\mathbf{r}+\mathbf{u}$ is a point $\mathbf{u}$ away from the center. The corrected potential energy $\tilde{V}$ will then be a function of $\mathbf{r}+\mathbf{u}$:
$$\tilde{V}(\mathbf{r}+\mathbf{u})=\int_{q_{e}}\phi(\mathbf{r}+\mathbf{u})dq_{e}$$
where we are integrating over the entire charge. We introduce the volume charge distribution we mentioned before as
$$\rho(\mathbf{u})\equiv-e\rho_{0}(\mathbf{u})\quad\text{where}\quad \rho_{0}(\mathbf{u})\text{ such that }\int_{V_{e}} \rho_{0}(\mathbf{u})dq=1$$
This makes our corrected potential energy into
$$\tilde{V}(\mathbf{r}+\mathbf{u})=\int_{V_{e}} \rho(\mathbf{u})\phi(\mathbf{r}+\mathbf{u})d^{3}u=\int_{V_{e}} \rho_{0}(\mathbf{u})V(\mathbf{r}+\mathbf{u})d^{3}u$$
We can expand $\tilde{V}$ in a Taylor series in $\mathbf{r}+\mathbf{u}$ around $\mathbf{r}$ to get
$$V(\mathbf{r}+\mathbf{u})\simeq V(\mathbf{r})+\sum_{i} \frac{ \partial V }{ \partial x_{i} } (\mathbf{r})u_{i}+ \frac{1}{2}\sum_{ij} \frac{ \partial ^{2}V }{ \partial x_{i}\partial x_{j} }(\mathbf{r}) u_{i}u_{j}$$
We can plug this into the equation for $\tilde{V}$ to get
$$\begin{align}
\tilde{V}(\mathbf{r})&\simeq\int_{V_{e}} \rho_{0}(\mathbf{u})V(\mathbf{r})d^{3}u+ \int_{V_{e}} \rho_{0}(\mathbf{u})\sum_{i} \frac{ \partial V }{ \partial x_{i} } (\mathbf{r})u_{i}d^{3}u+\int_{V_{e}} \rho_{0}(\mathbf{u})\frac{1}{2}\sum_{ij} \frac{ \partial ^{2}V }{ \partial x_{i}\partial x_{j} }(\mathbf{r}) u_{i}u_{j}d^{3}u \\
&=V(\mathbf{r})+ \frac{1}{6}\nabla ^{2}V(\mathbf{r})\int_{V_{e}}\rho_{0}(\mathbf{u})u^{2}du
\end{align}$$
Let's assume that the potentials takes the shape given by
$$\rho_{0}(u)=\begin{cases}
\left( \frac{4}{3}\pi \frac{\lambda}{2\pi} \right)^{-1}&\text{if }u\leq \frac{\lambda}{2\pi} \\
0&\text{if }u> \frac{\lambda}{2\pi}
\end{cases}$$
In other words, it fades off spherically, with a radius given by the reduced wavelength $\lambda/2\pi$. We also know that the [[Laplacian]] of $1/r$ is
$$\nabla ^{2}\left( \frac{1}{r} \right)=\delta(\mathbf{r})$$
so, a three-dimensional [[Delta di Dirac|Dirac delta]]. Putting this together and solving results in the **Darwin term**:
$$\boxed{H_{3}'=\frac{\pi \hbar^{2}}{2m^{2}c^{2}}\left( \frac{Ze^{2}}{4\pi \varepsilon_{0}} \right)\delta(\mathbf{r})}$$
The presence of a Dirac delta here is critical: since the delta kills every value outside of $\mathbf{r}=0$, the only time this correction matters is, well, when we are evaluating $\mathbf{r}=0$. This is significant because if you go back to look at the wavefunction we've derived above, the *only* ones which are nonzero in the origin are the $s$ orbitals, so when $l=0$. Everything else is zero in the origin, which means that this correction does *not* matter to them. The Darwin term is just an $s$ orbital correction.

Using this knowledge allows us to calculate the eigenvalue difference in just the $s$ orbitals, which is to say when $l=0,m=0$:
$$\begin{align}
\Delta E_{3}&=\frac{\pi \hbar^{2}}{2m^{2}c^{2}} \frac{Ze^{2}}{4\pi \varepsilon_{0}}\braket{ \psi_{n00} | \delta(\mathbf{r}) | \psi_{n00} }  \\
&=\frac{\pi \hbar^{2}}{2m^{2}c^{2}} \frac{Ze^{2}}{4\pi \varepsilon_{0}}\lvert \psi_{n00}(\mathbf{r}) \rvert ^{2} \\
&=\frac{mc^{2}}{2} \frac{(Z\alpha)^{2}}{n^{2}} \frac{(Z\alpha)^{2}}{n}
\end{align}$$
And hence
$$\boxed{\Delta E_{3}=-E_{n} \frac{(Z\alpha)^{2}}{n}\quad\text{if }l=0}$$
### Putting it all together
Now that we have all three corrections, we can put the together to find the total correction to the energy eigenvalues:
$$\boxed{\Delta E=\Delta E_{1}+\Delta E_{2}+\Delta E_{3}=E_{n} \frac{(Z\alpha)^{2}}{n^{2}}\left( \frac{n}{j+ \frac{1}{2}}- \frac{3}{4} \right)}$$
and adding this to the energy eigenvalues themselves we get the fine structure energy states:
$$\boxed{E_{nj}=E_{n}\left[ 1+ \frac{(Z\alpha)^{2}}{n^{2}}\left( \frac{n}{j+ \frac{1}{2}}- \frac{3}{4} \right) \right]}$$
As we can see, there is no direct dependence on the azimuthal angular momentum: the only thing that matters is the total angular momentum. As such, despite the fine structure leading to a great deal of splitting in the energy spectrum, it does not fully eliminate the degeneracy in $l$.

:::image
![[Hydrogen_fine_structure_energy_2.png]]
The last column to the right shows an additional effect, the [[Zeeman effect]], which is not covered here.

By ReyHahn - Own work, CC BY-SA 4.0, from [Wikipedia](https://commons.wikimedia.org/w/index.php?curid=92060559). Altered to have a white background.
:::

We can see that, since $\alpha \simeq 1/137$, its square is $\alpha ^{2}\sim10^{-4}$. As such, when $Z=1$ (so, when dealing with hydrogen), the correction is quite small, in the order of $10^{-4}\text{ eV}$. Recalling that the ground state energy is the [[Rydberg constant|Rydberg energy]], at about $-13.6\text{ eV}$, it's quite a small contribution indeed. However, do note the dependence on $Z$. This derivation is not just for the hydrogen atom, but rather all *hydrogenic* atoms. This includes any atom with just a single valence electron, which for instance includes all alkali metals. Thus, while the fine structure may not be all that significant for hydrogen outside of high-precision experiments or extreme conditions, it may be quite relevant for heavier hydrogenic atoms, such as cesium (symbol: $^{55}\text{Cs}$) for which $Z^{2}=55^{2}=3025\sim 10^{3}$, thus causing the whole term to be $\sim0.1\text{ eV}$.

Also, the relativistic correction is strictly positive, which means that the corrected states are *more strongly bound* (since $E_{n}$ is negative). In a sense, relativity makes it harder to break an electron off its atom. This becomes progressively less and less relevant as you climb the states, due to the $n^{-2}$ dependence, which means that the ground state ($n=1$) is the most affected.
## State transitions
Once the stationary states themselves are determined, it's fair to ask how the electron goes from one to another. After all, there's little point in knowing all possible states if the electron is perpetually confined to the ground state. As such, we now take on the investigation of [[State transition|state transitions]] of the electron.
### Electromagnetic field
Of course, since stationary states are stable, we need some external influence to trigger a state transition. We will choose the application of an external [[electric field]] $\boldsymbol{\mathcal{E}}$ and [[magnetic field]] $\boldsymbol{\mathcal{B}}$ for this section, respectively determined by an [[electric potential]] $\phi$ and a [[magnetic vector potential]] $\mathbf{A}$. The Hamiltonian of an [[Electric charge|point charge]] $q$ of mass $m$ in these fields is
$$H=\frac{1}{2m}(\mathbf{p}-q\mathbf{A})^{2}+q\phi$$
(ignoring small spin-dependent terms.) Changing $q\to-e$ and plugging this into the time-dependent Schrödinger equation yields
$$i\hbar \frac{ \partial  }{ \partial t } \psi(\mathbf{r},t)=\left[ \frac{1}{2m}(-i\hbar \nabla+e\mathbf{A})^{2}- \frac{Ze^{2}}{4\pi \varepsilon_{0} r} \right]\psi(\mathbf{r},t)$$
Before we move on: the entirety of electrodynamics hinges on an arbitrary choice, which we called [[gauge freedom]]. Though proof won't be given here, the Schrödinger equation is **gauge invariant**, which means that regardless of the gauge we choose, the equation does not change. The only thing that changes is that the resulting wavefunction acquires a [[phase]], and different gauges lead to different phases. However, since phases vanish when taking the square modulus $\lvert \psi(\mathbf{r},t) \rvert^{2}$, it makes no physical difference. For this section, we choose to fix the gauge to $\nabla\cdot \mathbf{A}=0$, known as the [[Coulomb gauge]].

Theoretical calculation of the transition [[Probability|probabilities]] is arduous and only a surface level analysis will be reported here. See Bransden & Joachaim Chapters 4.1 and 4.2 for more discussion.

We'll assume that the incident perturbation is a nearly monochromatic pulse of radiation peaked about some [[Frequency|angular frequency]] $\omega_{0}$ and nonzero only in a small region of width $\Delta \omega$. As usual, a generic pulse can be represented as a superposition of [[Plane wave|plane waves]] of frequency $\omega$, which we assume to all share the same [[Wavenumber|wavevector]] $\hat{\mathbf{k}}$ and (linear) polarization vector $\hat{\varepsilon}$ (the two are [[Orthogonality|orthogonal]], $\hat{\mathbf{k}}\cdot \hat{\varepsilon}=0$). A plane wave is solved by the real vector potential
$$\mathbf{A}(\omega;\mathbf{r},t)=\mathbf{A}_{0}(\omega)[e^{i(\mathbf{k}\cdot \mathbf{r}-\omega t+\delta_{\omega})}-e^{-i(\mathbf{k}\cdot \mathbf{r}-\omega t+\delta_{\omega})}]$$
with $\mathbf{A}_{0}(\omega)=A_{0}(\omega)\hat{\varepsilon}$. $\delta_{\omega}$ is a real phase term. The superposition in therefore
$$\mathbf{A}(\omega;\mathbf{r},t)=\int_{\Delta \omega}A_{0}(\omega)\hat{\varepsilon}[e^{i(\mathbf{k}\cdot \mathbf{r}-\omega t+\delta_{\omega})}-e^{-i(\mathbf{k}\cdot \mathbf{r}-\omega t+\delta_{\omega})}]d\omega$$
Since we're looking for the state transition caused by this perturbation, we set the time-dependent wavefunction to be generated by the usual superposition
$$\Psi(\mathbf{r},t)=\sum_{k}c_{k}(t)\psi_{k}(\mathbf{t})e^{-iE_{k}t/\hbar}$$
where $c_{k}(t)$ are the coefficients of the expansion, $\psi_{k}$ are the stationary states and $E_{k}$ are the eigenstates. We already know the $\psi_{k}$ and $E_{k}$, so to find the time evolution, we need to solve for the $c_{k}(t)$. We do this with [[time-dependent perturbation theory]] and by ignoring the $\mathbf{A}^{2}$ terms, which leaves a perturbation of
$$H'(t)=- \frac{i\hbar e}{m}\mathbf{A}(t)\cdot \nabla$$
The coefficients satisfy
$$\dot{c}_{b}(t)=- \frac{i}{\hbar}\sum_{k}\braket{ \psi_{b} | H'(t) | \psi_{k} } c_{k}(t)e^{i\omega_{bk}t}$$
where $\omega_{bk}=(E_{b}-E_{k})/\hbar$. If we take the system to initially be in the stationary state $\ket{\psi_{a}}$ of energy $E_{a}$, to first order, the coefficients are
$$c_{b}^{(1)}(t)=- \frac{i}{\hbar}\int_{0}^{t}\braket{ \psi_{b} | H'|\psi_{a} } e^{i\omega_{ba}t'}dt'$$
Solving this for the $\mathbf{A}(t)$ above yields
$$\begin{align}
c_{b}^{(1)}(t)=- \frac{e}{m}\int_{\Delta \omega}A_{0}(\omega)&\Big[ e^{i\delta_{\omega}}\braket{ \psi_{b} | e^{i\mathbf{k}\cdot \mathbf{r}}\hat{\varepsilon}\cdot \nabla| \psi_{a} }\int_{0}^{t}e^{i(\omega_{ba}-\omega)t'}dt'+ \\
&+e^{-i\delta_{\omega}}\braket{ \psi_{b} | e^{-i\mathbf{k}\cdot \mathbf{r}}\hat{\varepsilon}\cdot \nabla|\psi_{a} }\int_{0}^{t}e^{i(\omega_{ba}+\omega)t'}dt'   \Big]d\omega
\end{align}$$
The square brackets contain two terms: the first is the *absorption* term, which is nonzero only if $E_{b}=E_{a}+\hbar \omega$, and the second is the *emission* term, which is nonzero only if $E_{b}=E_{a}-\hbar \omega$. This is because the first integral over $dt'$ vanishes in realistic scenarios where the duration of the pulse is far larger than the periodic time $2\pi/\omega_{ba}$, thus leading that integral to be negligible unless $\omega \simeq \omega_{ba}$, which happens precisely when $E_{b}=E_{a}+\hbar \omega$. Similarly, the second integral is negligible unless $\omega \simeq-\omega_{ba}$ and so $E_{b}=E_{a}-\hbar \omega$.

This shouldn't come as a surprise: after all, energy is conserved, so the state transition must absorb or emit precisely the difference in energy between the states.

In an absorption process, when only the first half of the square brackets is nonzero, the probability that an atom will be found in a certain state upon measurement goes like
$$\lvert c_{b}^{(1)}(t) \rvert ^{2}\sim \int_{\Delta \omega}\left[ \frac{eA_{0}(\omega)}{m} \right]^{2}\lvert M_{ba}(\omega) \rvert ^{2}$$
where $M_{ba}$ is an element of the **transition matrix** $\mathrm{M}$, and is given by
$$M_{ba}=\braket{ \psi_{b} | e^{i\mathbf{k}\cdot \mathbf{r}}\hat{\varepsilon}\cdot \nabla|\psi_{a} }=\int \psi_{b}^{*}(\mathbf{r})e^{i\mathbf{k}\cdot \mathbf{r}}\hat{\varepsilon}\cdot \nabla \psi_{a}(\mathbf{r})d\mathbf{r} $$
This allows us to define the **absorption transition probability**
$$W_{ba}=\frac{4\pi ^{2}}{m^{2}c}\left( \frac{e^{2}}{4\pi \varepsilon_{0}} \right) \frac{I(\omega_{ba})}{\omega ^{2}_{ba}}\lvert M_{ba}(\omega_{ba}) \rvert^{2} $$
where
$$I(\omega)=\int_{\Delta \omega}I_{0}(\omega)d\omega=\int_{\Delta \omega}2\varepsilon_{0}\omega ^{2}cA_{0}^{2}(\omega)d\omega$$
The transition probability is also bound to its absorption **[[cross-section]]** by dividing the rate at which energy is absorbed by the atom, $\hbar \omega_{ba}W_{ba}$ by the intensity $I(\omega_{ba})$ to get
$$\sigma_{ba}=\frac{4\pi ^{2}\alpha \hbar^{2}}{m^{2}\omega_{ba}}\lvert M_{ba}(\omega_{ba}) \rvert ^{2}$$
Emission is complicated by the fact that there are two kinds of emission: stimulated and spontaneous. For stimulated emission, the transition rate is
$$W_{ab}=\frac{4\pi ^{2}}{m^{2}c}\left( \frac{e^{2}}{4\pi \varepsilon_{0}} \right) \frac{I(\omega_{ab})}{\omega ^{2}_{ba}}\lvert M_{ab}(\omega_{ba}) \rvert ^{2}$$
and similarly
$$\sigma_{ab}=\frac{4\pi ^{2}\alpha \hbar^{2}}{m^{2}\omega_{ab}}\lvert M_{ab}(\omega_{ba}) \rvert ^{2}$$
Spontaneous emission is more difficult to explain due to the inherent quantum nature of it, requiring quantum electrodynamics to properly solve. In fact, spontaneous emission is actually not a "real" process, in that it is actually stimulated emission, where the stimulating field is the vacuum quantum field, which is always present.
#### The dipole approximation
The calculation of the matrix element $M_{ba}=\braket{ \psi_{b} | e^{i\mathbf{k}\cdot \mathbf{r}}\hat{\varepsilon}\cdot \nabla|\psi_{a} }$ can be greatly simplified by making an assumption on how the field looks like. Namely, we ask that the field is essentially uniform at atomic scales, so that the field does not change in space over the volume of the atom (but still changes in time of course). The characteristic size of the atom is on the order of $\sim10^{-10}\text{ m}$, so we ask that the [[wavelength]] of the incoming radiation is considerably larger than this[^6]. In so doing, we allow ourselves to expand the $e^{i\mathbf{k}\cdot\mathbf{r}}$ in the matrix element in its [[Serie esponenziale|exponential series]]:
$$e^{i\mathbf{k}\cdot \mathbf{r}}=1+i\mathbf{k}\cdot \mathbf{r}+ \frac{1}{2}(i\mathbf{k}\cdot \mathbf{r})^{2}+\ldots$$
For large enough wavelengths, and thus small enough $\mathbf{k}$ compared to $\mathbf{r}$, we might as well say $e^{i\mathbf{k}\cdot \mathbf{r}}\simeq 1$. The expression for a transition probability can thus be expressed in terms of $\mathbf{r}_{ba}=\braket{ \psi_{b} | \mathbf{r} | \psi_{a} }$, where we wrote the nabla operator through its first order equation of motion. This yields
$$W_{ba}=\frac{4\pi ^{2}}{c\hbar ^{2}}\left( \frac{e^{2}}{4\pi \varepsilon_{0}} \right)I(\omega_{ba})\lvert \hat{\varepsilon}\cdot \mathbf{r}_{ba} \rvert ^{2}$$
Now, this new term $\mathbf{r}_{ba}$ can be shown to be not null only in very specific scenarios, which are when the new and old state satisfy the following two conditions:
$$\boxed{\Delta l=l_{b}-l_{a}=\pm 1,\quad \Delta m=m_{b}-m_{a}=0,\pm 1}$$
But then the transition probability must follow these conditions: we call these **selection rules**, as they allow us to determine which transitions are allowed and which aren't, for if these rules are not met, then $W_{ba}=0$ and the transition is impossible. These rules actually happen to be quite general, despite having derived them from a specific approximation in a specific kind of field and specifically for electrons. These even function, for instance, in transitions between vibrational states of [[molecule|molecules]], so keep these rules on hand, as they might very well reappear later.

[^1]: The angular momentum operator is found by quantizing the classical quantities of $r$ and $p$, which become $\hat{r}$ and $-i\hbar \nabla$ respectively ($\nabla$ is the [[gradient]]). So, we get $\hat{L}=-i\hbar(\hat{r}\times \nabla)$.

[^2]: If you recall the general solution, this extra term is known as the "centrifugal term". It represent the fact that more intense rotations (high $l$) tend to "push" outwards more. It's to quantum mechanics what the centrifugal force is to classical mechanics.

[^3]: Strictly speaking, the finiteness of the wavefunction is not mandatory. What is mandatory is that all possible physical states are described by a complete orthogonal set of wavefunctions. However, for many potentials, including the central electromagnetic one, this condition can be proven to simplify down to $u(0)=0$.

[^4]: It can be solved using the generating function of the Laguerre polynomials. See for instance Bransden & Joachaim Appendix 3. Be careful with definitions, as Bransden uses the alternative definition of the polynomials which omits $1/q!$, whereas this article includes it.

[^5]: We have $x\to\rho$, $m\to2l+1$ and $n\to n-l-1$. Be careful of the definition: the handbook's definition of the polynomials omits $1/n!$ whereas we include it, so we need to do two things before anything else: divide the polynomial by $n!$ (which becomes $(n!)^{2}$ due to the square) and convert $n\to n+m$. Then do the substitutions above.

[^6]: What "considerably" means is clearly quite arbitrary. It depends, as always, on how precise one wants to be. Most everyday radiation, such as visible light is well over the threshold, as its wavelength is around $\sim 10^{-6}\text{ m}$.
