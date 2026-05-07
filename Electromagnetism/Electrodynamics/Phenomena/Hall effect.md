---
hl-publish: true
---
The **Hall effect** is the formation of an [[electric potential]] between two surfaces of a solid material when [[electric charge|electric charges]] move through it while under a [[Orthogonality|perpendicular]] [[magnetic field]].
### Theory
Consider a rectangular pillbox-shaped solid object (called a **Hall sensor**) being traversed uniformly by a [[Electric current|steady current]] $I$ in the $y$ direction ($I=I_{y}$) and by a [[magnetic field]] in the $z$ direction $(B=B_{z})$.

![[Diagram Hall effect.svg]]

Due to the [[Lorentz force]] $\mathbf{F}=e\mathbf{v}\times \mathbf{B}$, the [[Electron|electrons]] in the current will be deflected by the magnetic field as it travels through the object. This will cause a centrifugal force applied onto the charges, which makes the charges get pushed (in the figure's case) across the $x$ axis.[^1] This makes the electron density over $x$ no longer uniform, which generates an [[electric potential]] $V_{H}$ between the $yz$ planes at $x=0$ and $x=a$. This in turn creates a parallel plate [[capacitor]]-like [[electric field]]
$$E=\frac{V_{H}}{a}$$
After a brief period of time of $\sim 10^{-8}\text{ s}$, the system gets into a state of dynamical equilibrium. In this state, the net total force on the electrons is zero
$$F=0\quad\Rightarrow \quad\frac{eV_{H}}{a}=ev_{y}B_{z}\quad\Rightarrow \quad V_{H}=av_{y}B_{z}$$
We know $a$ and $B_{z}$, so the last piece we need is a way to quantify the velocity of the electrons. Using the [[Drude model]], we can state
$$I_{y}=\rho av_{y}ec$$
where $\rho$ is the [[electrical resistivity]] of the material and $a$ and $c$ are the relevant sizes of the sensor. Inverting:
$$v_{y}=\frac{I_{y}}{\rho aec}$$
And substituting:
$$\boxed{V_{H}=\frac{I_{y}B_{z}}{\rho ac}}$$
The Hall potential depends on several factors. Directly through current and magnetic fields, but also inversely to the material ($\rho$) and geometry ($a$ and $c$) of the sensor. Smaller sensor make stronger Hall potentials, as do less resistive ones. In any case, though, they are pretty small. In realistic sensors, $V_{H}$ usually lies in the range of $10\text{-}500\text{ mV}$, maybe exceeding a few volts if pushed. It is difficult to scale them to higher potentials because, since they need to be so thin, the [[Joule effect]] can be very dangerous to the component when using high currents, not to mention the physical complexity of building sub-millimeter thin sensors.
### Measurement
$V_{H}$ can be measured experimentally, which means that we can reverse the formula to find, say, the magnetic field $B_{z}$ or the resistivity $\rho$:
$$B_{z}=\frac{V_{H}\rho ac}{I_{y}},\qquad \rho=\frac{I_{y}B_{z}}{V_{H}ac}$$
We can measure the Hall potential by connecting a [[voltmeter]] to the two ends of the sensor. While seemingly quite easy, this has considerable practical challenges due to the Hall sensor usually being tiny (because, remember, smaller sensors make bigger potentials). The measurement relies on getting the ends of the voltmeter *precisely* aligned on each  side.

:::image
![[Diagram Hall potential measurement.svg|center]]
Schematic representation of measuring a Hall sensor's potential. $\Delta y$ is the source of the error.
:::

The error occurs due to the misalignment $\Delta y$ between the voltmeter ends. This is because, even in lieu of a magnetic field, there still exist a potential due to the natural resistivity of the material. The region spanned by the misalignment has a resistance of
$$R=\frac{\rho \Delta y}{ac}$$
which according to [[Ohm's law]] $V=RI$ produces
$$V_\text{error}=\frac{I_{y}\rho \Delta y}{ac}$$
This quantity is *not small*. For reasonable quantities like $I\sim 1\text{ A}$ and $a\sim10\text{ mm}$, this can easily be in the order of several volts for misalignments as tiny as $\Delta y\sim 1\text{ mm}$. Considering that Hall potentials are usually pretty small, this can easily lead to >100% relative errors, so this measurement is very precise. On the one hand, it's a good thing, because sensitive measurements mean very high resolution. On the other, they are prone to complications, difficult and expensive manufacturing and overall fragile components. Still, Hall-sensor-based tools are quite useful and in active use, such as Hall sensor [[magnetometer|magnetometers]] for measuring magnetic fields.

[^1]: The electron being pushed by the Lorentz force will follow a circular trajectory as it moves, but due to the [[Drude model|drift velocity]] of an charge carrier in matter being so small, this trajectory is small enough ($\sim\mu m$) that it is negligible with respect to the size of the Hall sensor. This means that we can consider the effect to be applied to the entire sensor if it is large enough.
