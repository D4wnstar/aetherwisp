---
wiki-publish: true
aliases:
  - back emf
  - RL circuit
---
**Self inductance** is the phenomenon where changing the [[electric current]] within a loop induces an additional current within the loop itself counteracting the change. If the current is increased, the induced current will run in reverse, thereby trying to reduce the current back to its original value. Likewise, decreasing the current will prompt the loop to try to increase its own current. This can be thought of as an inertial phenomenon, as a sort of [[Newton's laws|Newton's first law]] for currents.

It is quantified by a constant also called the **self inductance** (or simply **inductance**) and denoted $L$. Like its sibling quantity [[mutual inductance]], it is a purely geometric quantity, determined by the size and shape of the loop. It is measured in henries $\text{H}$, which are volt-second per ampere. In circuits, inductance is added through high self inductance components called **[[inductor|inductors]]** and are represented as

```tikz
\usepackage{circuitikz}
\begin{document}
\begin{circuitikz}
\draw
(0,0) to[L] (2,0)
;
\end{circuitikz}
\end{document}
```
### Derivation
Consider any loop traversed by an [[Electric current|steady current]] $I$. This current produces a [[magnetic field]] running through the loop with a certain flux. Say now that the current is changed (so it's not steady anymore). This prompts an increase or decrease in the flux going through the loop, but this change [[Electromagnetic induction|induces]] an [[electric field]] and thus a current through the wire itself. [[Lenz's law]] tells us the induced field must be such as to oppose change, which means that the current will be run in a direction that tends to keep the total current constant. If the current is decreased, it'll try to increase it and viceversa. In other words, the induced current tries to maintain the "status quo"[^1].

The flux change is proportional to the current
$$\Phi=LI$$
where $L$ is the constant of proportionality called **self inductance**. The [[Electromotive force|emf]] induced by this change is
$$\mathcal{E}=-L \frac{dI}{dt}$$
which is known as the **back emf**, because it tries to push back against any change. The larger the inductance, the harder it gets to change a circuit's current.
### RL circuit
An **RL circuit** is a circuit made of a [[Electrical resistance|resistor]] $R$ and an inductor $L$. If we attach a generator of emf $\mathcal{E}_{0}$ and no internal resistance, [[Ohm's law|Ohm's first law]] says
$$\mathcal{E}_{0}-L \frac{dI}{dt}=IR$$
which is a first order [[Ordinary differential equation|ordinary differential equation]]. It can be solved by [[separation of variables]] followed by integration:
$$I(t)=\frac{\mathcal{E}_{0}}{R}[1-e^{ -(R/L)t }]$$
We can call $L/R=\tau$ the **inductive time constant** of the circuit. Its inverse, $\Gamma=R/L$ is also called the **dampening frequency**. The function and has a shape of this sort

```mathpad
%$1:=-e^(-t*tau^(-1))+1
tau:=2
%$2:=2
%$3:=[-e^((-1/2)*t)+1]
%$4:=[-e^((-1/2)*t)+1]
%$5:=[-e^((-1/2)*t)+1]
I(t,tau):=1-e^(-t/tau)
plot(I(t, tau), [0,6], [0,1])==?
```

so it converges to the final current at infinite time and gets to about 2/3 of the way at $1\tau$ and is mostly there at $3\tau$.

[^1]: It also usually fails, as induced electric fields are almost always tiny and do not have the intensity required to actually make a major change. That said, if the current is changed extremely fast (say, by violently pulling a plug out of a socket), the induced field can actually become enormous, if for a minuscule amount of time. Such a strong field can even be enough to force air to become a [[conductor]] for a split second and in so doing carry a massive current through the air between the socket and the plug in a desperate attempt to keep the current going. Visually, we see this as bright sparks and electric arcs running through the air, which is why it's dangerous to pull plugs out really fast when the power is on.