A **capacitor** is an electronic component that consists of two [[Conductor|conducting]] surfaces designed to have high [[capacitance]].
### Energy required to charge
Charging a capacitor requires moving [[Elettrone|electrons]] from the positive plate to the negative one, which means going against the [[electric field]]. The energy required to charge a capacitor by an infinitesimal [[electric charge|charge]] $dq$ is
$$dW=\frac{q}{C}dq$$
where $q$ is the amount of charge already stored in the conductor. To go up to a charge $Q$ then we must integrate
$$W=\int_{0}^{Q} \frac{q}{C}dq=\frac{1}{2} \frac{Q^{2}}{C}=\frac{1}{2}CV^{2}$$
where $V$ is the final [[electric potential]] of the capacitor.
### Relevant cases
Some capacitor configurations are more common than others.
#### Parallel-plate capacitor
The simplest configuration is two parallel metal plates very close to each other. Assume the plates are rectangular. Both have area $A$ and are held at a distance $d$ apart. The charge of one surface is $Q$ and the other is $-Q$. The charges will (mostly) distribute evenly across the surface (the approximation is best when $A$ is large and $d$ is small), so the surface density is $\sigma=Q/A$. The electric field right over the surface is given by boundary conditions:
$$\mathbf{E}=\frac{\sigma}{\varepsilon_{0}}\hat{\mathbf{n}}=\frac{Q}{A\varepsilon_{0}}\hat{\mathbf{n}}$$
The electric potential difference between the plates is
$$V=\frac{Q}{A\varepsilon_{0}}d$$
and the capacitance therefore is
$$C=\frac{A\varepsilon_{0}}{d}$$
#### Concentric spheres
Consider two concentric spheres of radii $a$ and $b$. The charge is $Q$ on the inner one and $-Q$ on the outer one. The field between the spheres is
$$\mathbf{E}=\frac{1}{4\pi \varepsilon_{0}} \frac{Q}{r^{2}}\hat{\mathbf{r}}$$
so the potential difference is
$$V=-\int_{b}^{a}\mathbf{E}\cdot d\mathbf{r}=- \frac{Q}{4\pi \varepsilon_{0}}\int_{b}^{a} \frac{1}{r^{2}}\ dr=\frac{Q}{4\pi \varepsilon_{0}}\left( \frac{1}{a}- \frac{1}{b} \right)$$
and the capacitance is
$$C=\frac{Q}{V}=4\pi \varepsilon_{0} \frac{ab}{b-a}$$
