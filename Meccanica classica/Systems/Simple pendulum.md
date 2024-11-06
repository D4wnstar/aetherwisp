The **simple pendulum** is an approximate model of a pendulum, comprised of a zero-dimensional point mass hanging at the end of a mass-less wire attached with no [[friction]] to a fixed point. The mass is only subject to [[Interazione gravitazionale|gravity]] and ignores other forces like air drag. It is a specific case of the [[Foucault pendulum]] where the angle $\theta$ is constant and angular speed $\omega$ can be taken to be zero. This makes the pendulum swing on a plane and the system simplifies to a two-dimensional problem.

Starting from the Foucault pendulum equations of motion, equation $(1)$ becomes trivial when $\theta=\text{const.}$ and $\omega=0$. Equation $(2)$ becomes
$$\ddot{\phi}+ \frac{g}{L}\sin\phi=0\tag{1}$$
which is a second order, non-linear differential equation in $\phi$.
### Small swings
For small swings, where the angle $\phi$ of oscillation is small, we can approximate $\sin\phi\simeq\phi$. This leaves us with
$$\ddot{\phi}+ \frac{g}{L}\phi=0$$
which is the [[Oscillatore armonico|harmonic oscillator]] equation, for which we know the solution. $g$ is the gravitational acceleration and $L$ is the length of the wire. If we call $\omega_{0}=\sqrt{g/L}$ the angular frequency of oscillation, the general solution is
$$\phi(t)=\phi_{0}\cos(\omega_{0}t+\psi_{0})$$
where $\phi_{0}$ is the amplitude of the oscillations. The period of oscillation is
$$T=\frac{2\pi}{\omega_{0}}=2\pi\sqrt{\frac{L}{g}}$$
Since the frequency is constant, the period is also constant. This means that small oscillations are *isochronal*. It is also independent of the mass of the object.
### General case
Let the initial conditions be $\phi(0)=\phi_{0}>0$ and $\dot{\phi}(0)=0$. These mean that the mass begins at some nonzero angle from the vertical and with no starting velocity. As there is no friction, motion must still be periodic, as in the small oscillation approximation. The period $T$ is however not so easily solved, as the non-linear differential is considerably more difficult to solve.

To procede, multiply $(1)$ by $2\dot{\phi}$:
$$0=2\dot{\phi}\ddot{\phi}+ \frac{2g}{L}\dot{\phi}\sin\phi=\frac{d}{dt}\left(\dot{\phi}^{2}- \frac{2g}{L}\cos\phi\right)$$
Integrating gives us
$$\dot{\phi}^{2}=\frac{2g}{L}(\cos\phi-\cos\phi_{0})$$
We can take the square root and pick the sign to be minus, so that the angle is decreasing (i.e. it's swinging towards the center). This way, we get
$$\dot{\phi}=\frac{d\phi}{dt}=-\sqrt{\frac{2g}{L}(\cos\phi-\cos\phi_{0})}$$
Splitting the differentials, we can [[separazione di variabili|separate the variables]]
$$\frac{d\phi}{\sqrt{\cos\phi-\cos\phi_{0}}}=-\sqrt{\frac{2g}{L}}dt$$
We can now solve this by integration from $\phi_{0}$ to $\phi$ on the left and $0$ to $t$ on the right:
$$\int_{\phi_{0}}^{\phi} \frac{d\psi}{\sqrt{\cos\psi-\cos\phi_{0}}}=-\sqrt{\frac{2g}{L}}t$$
We can use the boundary condition $\phi(T)=-\phi_{0}$ to get
$$\int_{\phi_{0}}^{-\phi_{0}}\frac{d\psi}{\sqrt{\cos\psi-\cos\phi_{0}}}=-\sqrt{\frac{2g}{L}}T$$
If we extract $T$ we get
$$T=\sqrt{\frac{L}{2g}}\int_{-\phi_{0}}^{\phi_{0}} \frac{d\psi}{\sqrt{\cos\psi-\cos\phi_{0}}}=\sqrt{\frac{2L}{g}}\int_{0}^{\phi_{0}} \frac{d\psi}{\sqrt{\cos\psi-\cos\phi_{0}}}$$
where we used symmetry between $[-\phi_0,0]$ and $[0,\phi_{0}]$. Unfortunately, this integral is not solvable in closed form, so we must resort to numerical methods.

Since the motion is periodic, we only need to solve for one period and then we can reuse the results for every subsequent swing. If solved numerically, intermediate positions can be interpolated from the sampled solutions. More specifically, we can solve for just the half period, which is the time difference between to angles where the pendulum has stopped (i.e. the time to go from one extreme of a swing to the other).

By looking at the integral, we can see that it is improper, as the integrand shoots up to infinity when $\psi \rightarrow \phi_{0}$. For such an integral, we can use the [[Parte principale di Cauchy|Cauchy principal part]]:
$$\int_{0}^{\phi_{0}-\varepsilon} \frac{d\psi}{\sqrt{\cos\psi-\cos\phi_{0}}}+\int_{\phi_{0}-\varepsilon}^{\phi_{0}} \frac{d\psi}{\sqrt{\cos\psi-\cos\phi_{0}}}$$
(without stating the limit $\varepsilon \rightarrow 0$ as it doesn't make much sense on a computer. $\varepsilon$ is nevertheless very small). The first term can be numerically solve as usual, as it has no discontinuities. In the second, we can expand the cosine in a [[Serie di Taylor|Taylor series]] about $\phi_{0}$ like
$$\cos\psi=\cos\phi_{0}-\sin\phi_{0}(\psi-\phi_{0})- \frac{1}{2}\cos\phi_{0}(\psi-\phi_{0})^{2}+\mathcal{O}(\psi^{3})$$
Changing variable to $z=(\phi_{0}-\psi)$ we get
$$\int_{\phi_{0}-\varepsilon}^{\phi_{0}} \frac{d\psi}{\sqrt{\cos\psi-\cos\phi_{0}}}=\int_{0}^{\varepsilon} \frac{dz}{\sqrt{\sin\phi_{0}\ z- \cos\phi_{0}\ \frac{z^{2}}{2}}}=\ldots$$
which can be solved analytically to get
$$\ldots=\sqrt{\frac{2}{\cos\phi_{0}}}\left(\frac{\pi}{2}-\arcsin\left(1- \frac{\varepsilon}{\tan\phi_{0}}\right)\right)$$
As $\varepsilon$ approaches zero, this approximation (and therefore the integral itself) approaches zero. This means that $\varepsilon$ needs to be chosen with care to avoid floating point errors when the denominator approaches zero. In total, the approximation is
$$\boxed{T\simeq\int_{0}^{\phi_{0}-\varepsilon} \frac{d\psi}{\sqrt{\cos\psi-\cos\phi_{0}}}+\sqrt{\frac{2}{\cos\phi_{0}}}\left(\frac{\pi}{2}-\arcsin\left(1- \frac{\varepsilon}{\tan\phi_{0}}\right)\right)}$$
