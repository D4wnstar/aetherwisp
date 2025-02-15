> [!success] Esame
> Questo esperimento può essere fatto per l'esame di Lab 2.

The idea is that we have a circuit with a [[Electrical resistance|resistance]] $R$, a [[Capacitor]] $C$, a diode and a variable [[electric potential]]. The circuit is

```tikz
\usepackage{circuitikz}
\begin{document}
\begin{circuitikz}
\draw
(0,0) -- (1,0)
(1,0) to[R] (2,0)
(1,0) -- (1,1)
(2,1) -- (2,0)
(1,1) to[C] (2,1)
(2,0) -- (3,0)
(3,0) to[diode] (4,0)
(4,0) -- (5,0)
(5,0) -- (5,-2)
(5,-2) -- (3,-2)
(3,-2) -- (2,-2)
(2,-2) -- (0,-2)
(0,-2) -- (0,0)
;
\end{circuitikz}
\end{document}
```

The current varies like so:

![[Graph Correcting circuit current|center]]

The response of the diode is (ideally) linear with a threshold $V_{S}$. Under $V_{S}$, there is no current. Above $V_{S}$, the current increases linearly.

The point of the circuit is to turn a a fixed-frequency potential (in Europe it's 50 Hz, in the US it's 60 Hz) into a constant one (basically an AC to DC transformer). The oscillation period is given by a
$$\tau=R^{*}C$$
where $R^{*}$ is the internal resistance of the wire the capacitor is on. The original potential is a sinusoidal wave. The diode truncates low voltages and leaves only positive ones (through the [[Joule effect]], which heats up the diode and risks breaking it. It's also quite inefficient as we're wasting half of the energy). The addition of a capacitor and a resistance adds "inertia" to the circuit, which changes the range of the wave from 0 to the maximum potential $V_\text{max}$ to some $V_\text{min}$ to $V_\text{max}$, as it can no longer fully discharge before the next cycle comes. The time to discharge is $\tau'=RC$.

![[Graph Rectified potential over time 1|center|100%]]

![[Graph Rectified potential over time 2|center]]

The last wave (after RC) is referred to as a **ripple**. We can measure the **rippling factor** by approximating each "wave" as a triangle, from which we get
$$\text{Rippling factor}=\frac{\Delta V}{\langle V \rangle }=\frac{2(V_\text{max}-V_\text{min})}{V_\text{max}+V_\text{min}}$$
since $\Delta V=V_\text{max}-V_\text{min}$ and $\langle V \rangle=(V_\text{max}+V_\text{min})/2$.

The current iteration of the circuit is very inefficient, as the diode is wasting at least half of the energy that we put in. To make things more efficient, we can use a **diode bridge** in a transformer. (I'm not drawing the circuit diagram for that.)