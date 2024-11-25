The **Hall effect** is the formation of an [[electric potential]] between two surfaces of a solid material when [[electric charge|electric charges]] move through it while under a perpendicular [[magnetic field]].
### Explanation
Consider a rectangular pillbox-shaped solid object (called a **Hall sensor**) being traversed uniformly by a [[Electric current|steady current]] $I$ in the $y$ direction ($I=I_{y}$) and by a [[magnetic field]] in the $z$ direction $(B=B_{z})$.

![[Diagram Hall effect|center]]

Due to the [[Lorentz force]], the current will be deflected by the magnetic field as it travels through the object. This will cause a centrifugal force applied onto the charges, which makes the charges get pushed from (in this case) the bottom to the top[^1]. This makes the current no longer uniform and makes the current towards the top (slightly) more intense than the one towards the bottom. But since there is now a difference in charges, an [[electric potential]] $V_{H}$ is produced between the plate, which in turn creates an [[electric field]]
$$E=\frac{V_{H}}{e}$$
where $e$ is the [[Carica elementare|electron charge]] (or more generally the charge of whatever charge carrier is being considered). The Lorentz force here is
$$\mathbf{F}=e\mathbf{E}+e(\mathbf{v}_{y}\times \mathbf{B}_{z})$$
The total force needs to be zero (???)
$$F=0\quad\Rightarrow \quad\frac{eV_{H}}{e}=ev_{y}B_{z}$$
We want some way to express the velocity of the charge carriers. Using the [[Drude model]], we can state
$$I_{y}=\rho av_{y}ec$$
where $\rho$ is the [[electrical resistivity]] of the material, $a$ is the width of the sensor and $c$ is its thickness. So
$$v_{y}=\frac{I_{y}}{\rho aec}$$
and finally
$$\boxed{V_{H}=\frac{I_{y}B_{z}}{\rho ac}}$$
So the potential becomes greater the more intense the current or magnetic field.
#### Measurement
It is possible to measure $V_{H}$ experimentally, which means that we can reverse the formula to find, say, the magnetic field $B_{z}$ or the resistivity $\rho$:
$$B_{z}=\frac{V_{H}\rho ec}{I_{y}},\qquad \rho=\frac{I_{y}B_{z}}{V_{H}ac}$$
We can measure the Hall potential be connecting the two sides of the sensor to a voltmeter. This has considerable practical challenges due to the Hall sensor usually being microscopic. In fact, the error on the potential reading depends on how aligned the two ends of the voltmeter are. See this figure

![[Diagram Hall potential measurement|center]]

The error $\Delta y$ appears in
$$\Delta V_{H}=\frac{I_{y}\rho \Delta y}{ac}$$
Since $V_{H}$ is usually small even for considerable currents (in the Amperes) and magnetic fields (in the Teslas), even small errors on $y$ (even fractions of a millimeter) can cause massive errors (like, >100% kind of error), so the measurement itself is very precise.

[^1]: The electron being pushed by the Lorentz force will follow a circular trajectory as it moves up, but due the [[Drude model|drift velocity]] of an charge carrier in matter being so small, this trajectory is small enough ($\sim\mu m$) that it is negligible with respect to the size of the Hall sensor. This means that we can consider the effect to be applied to the entire sensor if the sensor is large enough.