---
hl-publish: true
---
An **ammeter** is a tool used to measure [[electric current|electric currents]] within a circuit. It is attached in series to the circuit whose current needs to be measured and is specifically designed to have a low internal [[Electrical resistance|resistance]] to avoid causing a significant voltage drop in the circuit.
## Mechanism
Ammeters are not new instruments and about two centuries of engineering have brought about several different ways to measure current, both in analog and digital configurations.
### Moving coil ammeter
Consider a small circuit element traversed by current $I$ by charges ([[Electron|electrons]]) of [[electric charge]] $-e$ moving at velocity $\mathbf{v}$.

:::image
![[Schema Ammeter wiring|50%|center]]
A wire loop subject to a current $I$ and a magnetic field $\mathbf{B}$.
:::

We can place this whole circuit inside of a [[magnetic field]] $\mathbf{B}$ that is not necessarily aligned with the circuit's cross section (or even straight or uniform). We can generate the field through magnets.

The circuit is then wrapped around an iron cylinder that's designed to [[Magnetization|magnetize]] and demagnetize in short periods (milliseconds). This cylinder is shaped and located in between the magnet poles such that the field lines enter [[Orthogonality|orthogonally]] to its surface. This way, since the circuit is wrapped around it, the field lines are also orthogonal to the circuit.

Whenever a current passes through the circuit, a [[Lorentz force]] $\mathbf{F}$ is applied onto it. Since  $\mathbf{B}$ is orthogonal by construction, so is $\mathbf{F}$. This enacts a [[Moment of force|torque]] onto the wire and by extensions onto the cylinder it's attached to, causing both to rotate (the cylinder is intentionally not held in place to allow this). A pin extends outwards from the cylinder to show the rotation, which is displayed in front of a scale with ticks for current. Spiral springs mounted inside the cylinder provide a restoring force that counteracts the rotation, allowing the cylinder to stop rotating and to go back to a neutral position when current is removed. Finally, instead of a single wire loop, it is typical to loop the wire several times around the cylinder to create a proper magnetic coil, hence the name of the device.

:::image
![[Galvanometer_diagram.svg]]
A diagram of a moving coil ammeter. The red lines represent the coiled wire around the cylinder, whereas the green ones represent the restoring spiral spring.
By TiCPU - Own work, CC BY-SA 4.0, from [Wikipedia](https://commons.wikimedia.org/w/index.php?curid=5297642).
:::

Formally, the magnetic field $\mathbf{B}$ acts on the wire's electrons according to
$$\mathbf{F}=q\mathbf{v}\times \mathbf{B}$$
We ignore any possible [[electric field]] contribution. The velocity $\mathbf{v}$ is technically quite complicated due to internal electron-electron interaction. Here we consider only their drift velocity through the wiring; for models of electron behavior, start with the [[Drude model]]. We aim to keep $\lvert \mathbf{v}\times \mathbf{B} \rvert$ both constant and as high as we can. Larger response forces allow the instrument to be more sensitive to small variations and thus have higher resolution. Maximizing $\lvert \mathbf{v}\times \mathbf{B} \rvert$ implies keeping the two vectors orthogonal to each other. Meanwhile, the easiest way of keeping it constant is to keep both $\mathbf{v}$ and $\mathbf{B}$ constant. Creating a constant $\mathbf{B}$ can be easily done by using a permanent magnet.

As long as $\mathbf{B}$ is oriented as per the wire loop figure, orthogonal to the two sections of length $a$, the two forces in opposite directions arise at the opposite ends of the wire that produces a torque. If we call $\lambda$ the linear electron density, we can calculate $n_\text{tot}=\lambda a$ as the number of total electrons in a wire section of length $a$. We can express the total charge in that section as $\lvert q_\text{tot} \rvert=\lambda ae$. The magnitude of the force, so long $\mathbf{v}$ and $\mathbf{B}$ are orthogonal, then is $F=qvB=\lambda a evB$. Finally, the torque magnitude is
$$N=2F \frac{b}{2}=\lambda aevBb=S\lambda evB$$
where $S=ab$ is the inner surface of the coil. Recalling the definition of linear current, we know that $I=\lambda e v$. Thus, we can relate the input current with the observed torque:
$$N=SIB$$
This is how we turn the current into an observable quantity. $B$ and $S$ are chosen during manufacturing of the tool, so we only need a way to find $N$ to get $I$. The simplest way to measure torque is through a spring. Two identical ones, actually.

![[Schema Ammeter wiring springs]]

We place the spring at the ends of the coil, orthogonal to the field. We know that for spiral springs, the torque can be approximated at low turning angles $\theta$ as
$$N_\text{spr}\simeq k\theta$$
where $k$ is the [[Harmonic oscillator|spring constant]]. By "low angles" we mean at most a few degrees, $\theta\lesssim 3°$. This is a tiny amount and realistically not enough to properly display a measurement, even when doubled due to having two springs. However, the trick is that this approximation gets better the more spring turns there are. If the springs have 10 turns each, the limit of approximation increases around tenfold, so $\theta\lesssim 30°$, or $\theta\lesssim 60°$ with two springs. This is a much more reasonable amount, but it relies on having the right kind of springs and limits the kind of forces the ammeter can muster.

Since the spring torque opposes the magnetic torque, the two will balance out when
$$k\theta\simeq SIB$$
and so
$$\boxed{I\simeq \frac{k}{SB}\theta}$$
The ammeter can now provide measurements of current by measuring the angle of rotation of the coil. These measurements become progressively less precise as you get into higher angles $\theta$, where the linear spring torque approximation loses validity.

This kind of ammeter is fundamentally limited by the fact that the coil's wire needs to be quite thin to properly create a coil and wrap it around the cylinder. Thin wire can't sustain high currents as they will melt due to [[Joule effect]] thermal energy. Thus, moving coil ammeters are quite limited in the kinds of currents they can measure, usually somewhere in the tens or hundreds of milliamperes. However, it is possible to skirt around the problem using a [[current divider]]. As long as the resistances used by the divider are known, you can split the current and send the weaker one to the ammeter, measure that, and figure the original current through the divider's current formula.