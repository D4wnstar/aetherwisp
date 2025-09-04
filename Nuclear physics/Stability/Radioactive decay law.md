---
wiki-publish: true
aliases:
  - decay constant
---
The **radioactive decay law** is a macroscopic exponential law that describes the [[nuclear decay]] of a [[Nuclear decay|radioactive]] object, regardless of the decay mode. It is a stateless law, in the sense that it the decay behavior at some moment does not depend on previous moments in time.
### Formulation
Consider a macroscopic object made up of $N$ radioactive [[Atomic nucleus|nuclei]] and let it decay naturally for until time $t$ without introducing any new nuclei. In its simplest form, the decay law assumes the decay products are stable and don't themselves decay. Moreover, it is easiest to start by assuming there is only one mode of decay.

The number $dN$ of nuclei that decay in a time unit $dt$ is proportional to the number $N$ present. The ratio between decay rate $dN/dt$ and number of nuclei $N$ is
$$\lambda=-\frac{1}{N}\frac{dN}{dt}$$
which is known as the **decay constant**. The equation is a first-order [[ordinary differential equation]] in $N$, solved by direct integration:
$$\boxed{N(t)=N_{0}e^{-\lambda t}}$$
This is the **radioactive decay law**, where $N_{0}$ is the number of nuclei at the start of the observation. It is an exponential decay law whose rate is determined by the decay constant.
#### Properties
We can get some useful quantities out of this law. The time it takes for the original number of nuclei $N_{0}$ to halve is called the **[[half-life]]**:
$$t_{1/2}=\frac{\ln2}{\lambda}$$
Easily confused but not the same, the **[[mean lifetime]]** is the time it takes *on average* for a *single* nucleus to decay:
$$\tau=\frac{\displaystyle\int_{0}^{\infty}t\left|\frac{dN}{dt}\right|dt}{\displaystyle\int_{0}^{\infty}\left|\frac{dN}{dt}\right|dt}=\frac{1}{\lambda}$$
obtained by integrating $\left|\frac{dN}{dt}\right|dt$, the number of nuclei decaying between $t$ and $t+dt$. This value is relevant because nuclear decay is a [[random]] process, so the time it takes for a decay event to occur is a [[random variable]].

Under the assumption that the decay products are stable, it's easy to check that the total number of nuclei is conserved. Setting $N_{1}$ as the number of nuclei of the original material and $N_{2}$ as the number of product nuclei, we see
$$N_{1}=N_{0}e^{-\lambda t},\qquad N_{2}=N_{0}(1-e^{-\lambda t})$$
so
$$N_{2}=N_{0}-N_{1}\quad\Rightarrow\quad N_{0}=N_{1}+N_{2}$$
### Activity
In practice, measuring $N$ directly isn't feasible, but we can record the [[radiation]] emitted between in some time interval and extract the number of decay events in that time interval. If $\Delta N$ nuclei decay in time $t+\Delta t$, we have
$$\left|\Delta N\right|=N(t)-N(t+\Delta t)=N_{0}e^{-\lambda t}(1-e^{-\lambda\Delta t})$$
If $\Delta t\ll\tau\ll t_{1/2}$ we may drop higher-order terms, so we're left with:
$$\left|\Delta N\right|\approx\lambda N_{0}e^{-\lambda t}\Delta t$$
Divide both sides by $\Delta t$, move into the $\Delta N/\Delta t\to dN/dt$ limit and get
$$\left|\frac{dN}{dt}\right|=\lambda N(t)=\lambda N_{0}e^{-\lambda t}$$
This quantity is quite useful, as it represents the number of decays per unit time: we call it **[[activity]]**
$$A=\lambda N(t)=A_{0}e^{-\lambda t}$$
where $A_{0}=\lambda N_{0}$. We can write
$$\Delta N=\int_{t}^{t+\Delta t}A\,dt=A\Delta t$$
It should be stressed that this only works if the time spent measuring $\Delta t$ is much smaller than the half-life $t_{1/2}$, as what we've done is essentially approximate an exponential function into a linear one. As such, requiring a small $\Delta t$ is basically asking to draw many short line segments in order to approximately draw the exponential curve. This makes this method practical only for materials whose half-lives are not too short (measurements become really hard[^1]) but also not too long (it shouldn't take several generations of scientists to measure how fast a rock is dying). In practice, a reasonable bound is $1\text{ s}<t_{1/2}<\text{a few decades}$.
### Extensions
While the basic decay law describes the decay of a single nuclear species through a single decay mode with no external addition of nuclei, it is possible to extend the law in several ways to describe more complicated scenarios.
#### Multiple decay modes
Say the material decays in multiples modes. In reality, basically every unstable [[nuclide]] has several decay modes, so this is a rather important extension.

Consider two decay modes, labeled $a$ and $b$. For each we define a **partial decay constant**
$$\lambda_{a}=-\frac{1}{N}\left(\frac{dN}{dt}\right)_{a},\qquad \lambda_{b}=-\frac{1}{N}\left(\frac{dN}{dt}\right)_{b}$$
which is the decay constant due only to a single mode. Their total $\lambda_{a}+\lambda_{b}=\lambda_{t}$ is the **total decay constant**. Remember that this law is a macroscopic process: we only see the end result of the total decay and miss the nitty-gritty details. In practice, this means that we only ever measure the total decay constant: the partial ones are "invisible". Just like how you can't separate the liquors in a cocktail once it's mixed, you can't separate the decay constants when measuring them like this: it's all at once or none at all. The decay law then only responds to the total:
$$N(t)=N_{0}e^{-\lambda_{t}t}$$
The partial constants are nevertheless useful to describe the fractions of nuclei decayed due to one mode or the other. The fraction $\lambda_{a}/\lambda_{t}$ decays via mode $a$ and $\lambda_{b}/\lambda_{t}$ via mode $b$. The nuclei decayed due to $a$ and $b$ after a time $t$ are
$$N_{1}=N_{0}e^{-\lambda_{t}t}$$
$$N_{2a}=N_{0}\left(\frac{\lambda_{a}}{\lambda_{t}}\right)\bigl(1-e^{-\lambda_{t}t}\bigr),\qquad N_{2b}=N_{0}\left(\frac{\lambda_{b}}{\lambda_{t}}\right)\bigl(1-e^{-\lambda_{1}t}\bigr)$$

> [!example]- Multiple decay half-lives
> Suppose we have a sample containing two [[Nuclide|radionuclides]]:
> $$^{64}\text{Cu}\rightarrow t_{1/2}=12.7\text{ h},\qquad ^{61}\text{Cu}\rightarrow t_{1/2}=3.4\text{ h}$$
> Measuring the activity yields a curve like
> ![[Plot Multiple decay activities|60%|center]]
> Initially we observe a single decay curve. Because the lifetimes differ greatly, the shorter-lived isotope will eventually be nearly depleted while the longer-lived one is still going. Fitting the tail of the curve gives an estimate of the activity of the long-lived nuclide; subtracting this from the earlier data leaves the activity of the short-lived nuclide. The method works for any number of radionuclides provided their lifetimes are sufficiently different.

[^1]: Actually, super short measurements of decay down to even one picosecond are actually possible nowadays, but the method is different and requires multiple channels measuring the activity at the same time.
