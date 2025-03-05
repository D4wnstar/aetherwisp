A **capacitor** is an electronic component that consists of two [[Conductor|conducting]] surfaces designed to have high [[capacitance]]. It is represented in circuit diagrams with the symbol

```tikz
\usepackage{circuitikz}
\begin{document}
\begin{circuitikz}
\draw
(0,0) to[capacitor, o-o] (2,0)
;
\end{circuitikz}
\end{document}
```

### Energy required to charge
Charging a capacitor requires moving [[Elettrone|electrons]] from the positive plate to the negative one, which means going against the [[electric field]]. The energy required to charge a capacitor by an infinitesimal [[electric charge|charge]] $dq$ is
$$dW=\frac{q}{C}dq$$
where $q$ is the amount of charge already stored in the conductor. To go up to a charge $Q$ then we must integrate
$$W=\int_{0}^{Q} \frac{q}{C}dq=\frac{1}{2} \frac{Q^{2}}{C}=\frac{1}{2}CV^{2}$$
where $V$ is the final [[electric potential]] of the capacitor.
### Relevant cases
Some capacitor configurations are more common than others.

> [!example] Parallel-plate capacitor
> The simplest configuration is two parallel metal plates very close to each other. Assume the plates are rectangular. Both have area $A$ and are held at a distance $d$ apart. The charge of one surface is $Q$ and the other is $-Q$. The charges will (mostly) distribute evenly across the surface (the approximation is best when $A$ is large and $d$ is small), so the surface density is $\sigma=Q/A$. The electric field right over the surface is given by boundary conditions:
> $$\mathbf{E}=\frac{\sigma}{\varepsilon_{0}}\hat{\mathbf{n}}=\frac{Q}{A\varepsilon_{0}}\hat{\mathbf{n}}$$
> The electric potential difference between the plates is
> $$V=\frac{Q}{A\varepsilon_{0}}d$$
> and the capacitance therefore is
> $$C=\frac{A\varepsilon_{0}}{d}$$

> [!example] Parallel-plate capacitor with dielectric
> Consider a parallel-plate capacitor that is filled with [[dielectric]] material of [[Permittivity|relative permittivity]] $\varepsilon_{r}$ in between the plates. Since the field is confined between the plates, it is entirely diminished by the dielectric, specifically by a factor $1/\varepsilon_{r}$. The same goes for the potential. Since $C=Q/V$, the capacitance of a dielectric-enhanced capacitor with respect to one in a vacuum is
> $$C=\varepsilon_{r}C_\text{vac}$$

> [!example] Concentric spheres
> Consider two concentric spheres of radii $a$ and $b$. The charge is $Q$ on the inner one and $-Q$ on the outer one. The field between the spheres is
> $$\mathbf{E}=\frac{1}{4\pi \varepsilon_{0}} \frac{Q}{r^{2}}\hat{\mathbf{r}}$$
> so the potential difference is
> $$V=-\int_{b}^{a}\mathbf{E}\cdot d\mathbf{r}=- \frac{Q}{4\pi \varepsilon_{0}}\int_{b}^{a} \frac{1}{r^{2}}\ dr=\frac{Q}{4\pi \varepsilon_{0}}\left( \frac{1}{a}- \frac{1}{b} \right)$$
> and the capacitance is
> $$C=\frac{Q}{V}=4\pi \varepsilon_{0} \frac{ab}{b-a}$$

> [!example] Coaxial cylinders
> Consider two coaxial cylinders of radii $a$ and $b$ and length $L$. The charge is $Q$ on the inner one and $-Q$ on the outer one. The field between the cylinders is
> $$\mathbf{E}=\frac{1}{2\pi \varepsilon_{0}} \frac{1}{rL}\hat{\mathbf{r}}$$
> so the potential difference is
> $$V=-\int_{b}^{a}\mathbf{E}\cdot d\mathbf{r}=\frac{Q}{2\pi \varepsilon_{0}L}\int_{a}^{b} \frac{1}{r}dr=\frac{Q}{2\pi \varepsilon_{0}L}\ln\left( \frac{b}{a} \right)$$
> and the capacitance is
> $$C=\frac{Q}{V}=\frac{2\pi\varepsilon_{0}L}{\ln(b/a)}$$
> The field used is a valid approximation when $L$ is very large compared to the radii, so the capacitance is also an approximation. It becomes correct when $L\to \infty$, in which case it is more useful to talk about the capacitance per unit length
> $$c=\frac{2\pi \varepsilon_{0}}{\ln(b/a)}$$
### Behavior in series and parallel
Consider two capacitors $C_{1}$ and $C_{2}$ in a circuit of total potential difference $\Delta V$. Say they are in series one after another:

```tikz
\usepackage{circuitikz}
\begin{document}
\begin{circuitikz}
\draw
(0,0) to[capacitor, o-o, l=$C_1$] (1,0)
(1,0) -- (3,0)
(3,0) to[capacitor, o-o, l=$C_2$] (4,0)
;
\end{circuitikz}
\end{document}
```

The charge $Q$ remains constant across all them (it just flips sign across plates), so
$$C_{1}=\frac{Q}{V_{1}},\quad C_{2}=\frac{Q}{V_{2}}$$
From [[Kirchhoff's laws|Kirchhoff's loop law]], we know that each potential must sum to the total:
$$\Delta V=V_{1}+V_{2}=QC_{1}+QC_{2}=Q(C_{1}+C_{2})$$
and inverting the relation
$$\frac{1}{C_{1}+C_{2}}=\frac{\Delta V}{Q}$$
which means that the total capacitance of capacitors in series is
$$\frac{1}{C}=\frac{1}{C_{1}+C_{2}}$$
and more generally, for $n$ capacitors,
$$\boxed{\frac{1}{C}=\sum_{i=1}^{n} \frac{1}{C_{i}}}$$

Say now they are in parallel:

```tikz
\usepackage{circuitikz}
\begin{document}
\begin{circuitikz}
\draw
(0,0) -- node[currarrow]{} (1,0)
(1,0) -- (1,1)
(1,0) -- (1,-1)
(1,1) to[capacitor, o-o, l=$C_1$] (3,1)
(1,-1) to[capacitor, o-o, l=$C_2$] (3,-1)
(3,1) -- (3,0)
(3,-1) -- (3,0)
(3,0) -- node[currarrow] {} (4,0)
;
\end{circuitikz}
\end{document}
```

The charge is now split across the capacitors before merging again after, $Q=Q_{1}+Q_{2}$, but the potential difference isn't, so
$$C_{1}=\frac{Q_{1}}{\Delta V},\quad C_{2}=\frac{Q_{2}}{\Delta V}$$
and using charge conservation
$$Q=C_{1}\Delta V+C_{2}\Delta V=(C_{1}+C_{2})\Delta V$$
so the total capacitance of capacitors in parallel is
$$C=C_{1}+C_{2}$$
and more generally, for $n$ capacitors,
$$\boxed{C=\sum_{i=1}^{n} C_{i}}$$
### Charge and discharge process
The process of charging and discharging a capacitor is of course not an electrostatics problem. That said, if the capacitor is (dis)charging *slowly*, then we can approximate the [[electric current]] in the circuit to be mostly constant in time as the propagation of change happens much faster than the (dis)charging[^1]. It's not *actually*, but if the (dis)charge is slow enough, we can consider it as if it were a (quasi-)steady current. In this regime, we can apply [[Kirchhoff's laws|Kirchhoff's loop law]].
#### Charge
Consider a circuit of this shape, composed of an [[electrical resistance]] $R$, a capacitor $C$ and a generator with [[electromotive force]] $\mathcal{E}$:

```tikz
\usepackage{circuitikz}
\begin{document}
\begin{circuitikz}
\draw
(0,0) to[battery1,l=$\mathcal{E}$] (2,0)
(2,0) -- (2,-2)
(2,-2) to[capacitor,l=$C$] (0,-2)
(0,-2) to[R,l=$R$] (0,0)
;
\end{circuitikz}
\end{document}
```

The current $I$ flows counterclockwise. This loop obeys by the hoop law
$$\mathcal{E}-RI-\Delta V=0$$
with $\Delta V$ the potential differences between the plates of the capacitor, which is
$$\Delta V=\frac{q}{C}$$
using its capacitance $C$ and the total charge on its surfaces $q$. The current is also the derivative of charge in time, so
$$I=\frac{dq}{dt}$$
and if we put those together we get
$$\mathcal{E}-R \frac{dq}{dt}- \frac{q}{C}=0$$
which is a first order [[Ordinary differential equation|ordinary differential equation]]. It can be easily solved by integration
$$\frac{1}{C\mathcal{E}-q}dq=\frac{1}{RC}dt$$
which, when integrated, gives us
$$\ln\left( \frac{C\mathcal{E}-q}{C\mathcal{E}} \right)=- \frac{t}{RC}\quad\Rightarrow \quad C\mathcal{E}-q=C\mathcal{E}e^{ -t/RC }$$
Extracting $q$ we can find its dependence on time
$$\boxed{q(t)=C\mathcal{E}(1-e^{ -t/RC })}$$
We can see that at time $t=0$, $q=0$, which makes sense as the capacitor has not even begun charging. Meanwhile, $RC$ has the interesting property of being a *time*. We call this the **circuit time constant** $\tau$ and it's a measure of how fast or slow a capacitor charges in that circuit. The bigger the time constant, the longer it takes for the capacitor to charge. It's usually tiny: for a 100 $\Omega$ resistance and a 1 picofarad capacitor, it's about $10^{-10}$ seconds, or a tenth of a nanosecond.

```mathpad
tau_1:=1/10
%$1:=1/10
%$2:=-e^(-t*tau^(-1))+1
%$3:=[-119696244^(10*t)*325368125^(-10*t)+1]
tau_2:=2
%$4:=2
%$5:=[-119696244^((1/2)*t)*325368125^((-1/2)*t)+1]
%$6:=[-119696244^(10*t)*325368125^(-10*t)+1,-119696244^((1/2)*t)*325368125^((-1/2)*t)+1]
q(t,tau):=1-e^(-t/tau)
plot(q(t, tau_1), q(t, tau_2), [0,4], [0,1])
```

The current intensity in time can be found by taking the time derivative:
$$\boxed{I=\frac{dq}{dt}=\frac{\mathcal{E}}{R}e^{-t/RC}}$$
Unsurprisingly, this has the opposite behavior as $q$. It starts off high and tapers off to zero as the capacitor gets to full charge.

```mathpad
tau_1:=1/10
%$1:=1/10
%$2:=-e^(-t*tau^(-1))+1
%$3:=[-119696244^(10*t)*325368125^(-10*t)+1]
tau_2:=2
%$4:=2
%$5:=[-119696244^((1/2)*t)*325368125^((-1/2)*t)+1]
%$6:=[-119696244^(10*t)*325368125^(-10*t)+1,-119696244^((1/2)*t)*325368125^((-1/2)*t)+1]
%$7:=[-119696244^(10*t)*325368125^(-10*t)+1,-119696244^((1/2)*t)*325368125^((-1/2)*t)+1]
%$9:=e^(-t*tau^(-1))
I(t,tau):=e^(-t/tau)
plot(I(t, tau_1), I(t, tau_2), [0,4], [0,1])==?
```

If we express [[work]] in terms of the current as $dW=\mathcal{E}dq=\mathcal{E}Idt$. We can integrate this over an infinite time period to find the total work required to charge a capacitor:
$$W=\int_{0}^{\infty} \mathcal{E}Idt=\int_{0}^{\infty} \frac{\mathcal{E}^{2}}{R}e^{-t/RC}dt=C\mathcal{E}^{2}$$
Curiously, this is twice as much as what we found before when integrating over the charge directly. What's going on? The issue is that this is not the work required to charge the capacitor. This is the *total* work required to be applied onto the *circuit* in order for the capacitor to be charged. This is important because unlike the previous result, this also takes into account the very relevant issue of the [[Joule effect]], which "wastes" [[energy]] by turning it into heat, and the energy wasted into [[heat]] exactly the same as the energy put into the capacitor. In fact, we can even find this by going through the Joule effect itself. The resistance does work outputting heat dependent on the Joule effect: $dW=Pdt=RI^{2}dt$, so
$$W=\int_{0}^{\infty}RI^{2}dt=\int_{0}^{\infty} \frac{\mathcal{E}^{2}}{R}e^{-2t/RC}=\frac{C\mathcal{E}^{2}}{2}$$
#### Discharge
To discharge a capacitor, we just remove the generator from the circuit (realistically we probably have a switch that causes a short-circuit or that redirects to ground):

```tikz
\usepackage{circuitikz}
\begin{document}
\begin{circuitikz}
\draw
(0,0) -- (2,0)
(2,0) -- (2,-2)
(2,-2) to[capacitor,l=$C$] (0,-2)
(0,-2) to[R,l=$R$] (0,0)
;
\end{circuitikz}
\end{document}
```

and we are left with the differential equation
$$-R \frac{dq}{dt}- \frac{q}{C}=0$$
and integrating
$$\frac{1}{q}dq=- \frac{1}{RC}dt$$
we get
$$\boxed{q(t)=C\mathcal{E}e^{-t/RC}}$$
This is almost exactly the equation for the current in the charging process, just scaled by a different constant (we find $\mathcal{E}$ instead of $1/R$ here). The current can be again found by derivation:
$$\boxed{I(t)=- \frac{\mathcal{E}}{R}e^{-t/RC}}$$
which is just the current in the charging case with the sign reversed. This means that when a capacitor is discharging, it'll elicit a current going in the *opposite* direction as the charging current.

[^1]: This is pretty much the same thought process used to call slow [[thermodynamic transformation|thermodynamic transformations]] (quasi-)[[adiabatic transformation|adiabatic]].

$$\phi(\mathbf{r})=\frac{q}{4\pi \varepsilon_{0}} \left( \frac{1}{\lvert \mathbf{r}- \mathbf{s}/2 \rvert} - \frac{1}{\lvert \mathbf{r}+ \mathbf{s}/2 \rvert } \right)=\frac{q}{4\pi \varepsilon_{0}} \frac{\mathbf{s}\cdot\mathbf{r}}{r^{3}}$$
