---
wiki-publish: true
aliases:
  - decay constant
  - rate of production
  - production rate
  - decay chain
---
The **radioactive decay law** is a macroscopic exponential law that describes the [[nuclear decay]] of a [[Nuclear decay|radioactive]] object, regardless of the decay mode. It is a stateless law, in the sense that it the decay behavior at some moment does not depend on previous moments in time.
### Formulation
Consider a macroscopic object made up of $N$ radioactive [[Atomic nucleus|nuclei]] and let it decay naturally for until time $t$ without introducing any new nuclei. In its simplest form, the decay law assumes the decay products are stable and don't themselves decay. Moreover, it is easiest to start by assuming there is only one mode of decay.

The number $dN$ of nuclei that decay in a time unit $dt$ is proportional to the number $N$ present. The ratio between decay rate $dN/dt$ and number of nuclei $N$ is
$$\lambda=-\frac{1}{N}\frac{dN}{dt}$$
which is known as the **decay constant**, measured in inverse seconds. The equation is a first-order [[ordinary differential equation]] in $N$, solved by direct integration:
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
The partial constants are nevertheless useful to describe the fractions of nuclei decayed due to one mode or the other. The fraction $\lambda_{a}/\lambda_{t}$ decays via mode $a$ and $\lambda_{b}/\lambda_{t}$ via mode $b$. The nuclei decayed due to $a$ and $b$ after a time $t$ are the same as the usual decay law
$$N_{1}=N_{0}e^{-\lambda_{t}t}$$
but we can make estimates of the fraction of nuclei
$$\boxed{N_{2a}=N_{0}\left(\frac{\lambda_{a}}{\lambda_{t}}\right)\bigl(1-e^{-\lambda_{t}t}\bigr),\qquad N_{2b}=N_{0}\left(\frac{\lambda_{b}}{\lambda_{t}}\right)\bigl(1-e^{-\lambda_{1}t}\bigr)}$$

> [!example]- Multiple decay half-lives
> Suppose we have a sample containing two [[Nuclide|radionuclides]]:
> $$^{64}\text{Cu}\rightarrow t_{1/2}=12.7\text{ h},\qquad ^{61}\text{Cu}\rightarrow t_{1/2}=3.4\text{ h}$$
> Measuring the activity yields a curve like
> ![[Plot Multiple decay activities|60%|center]]
> Initially we observe a single decay curve. Because the lifetimes differ greatly, the shorter-lived isotope will eventually be nearly depleted while the longer-lived one is still going. Fitting the tail of the curve gives an estimate of the activity of the long-lived nuclide; subtracting this from the earlier data leaves the activity of the short-lived nuclide. The method works for any number of radionuclides provided their lifetimes are sufficiently different.

#### Production-decay
Say there is an external source of radioactive nuclei that is constantly adding new unstable nuclei to the material. In many cases, the source is instead *causing* the material's nuclei to become unstable by transferring large amounts of energy to them, but the effect is the same. An example would be a nuclear reactor producing high-energy neutrons that hit an otherwise stable target and get [[neutron capture|captured]] by the nuclei, causing them to become unstable and [[beta decay]].

The rate at which new nuclei are added or rendered unstable is called the **rate of production** $R$. This varies based on the exact process being used, but for destabilization, it is dependent on the number of (stable) nuclei of the target $N_{0}$, the [[flux]] of incident particles $I$ (measured in $\text{particles}/\text{s cm}^{2}$) and the [[cross-section]] of the nuclear reaction $\sigma$:
$$R=N_{0}\sigma I\quad\text{[particles/s]}$$
Call $N_{1}$ the number of unstable nuclei created this way. They decay with constant $\lambda_{1}$ into $N_{2}$ stable nuclei. As such, $N_{1}$ *increases* due to the rate of production, but *decreases* due to its natural decay. The unit change of $N_{1}$ per unit time is
$$dN_{1}=Rdt-\lambda_{1}N_{1}dt$$
so, "diving" by $dt$ and solving the first-order ODE
$$\boxed{N_{1}(t)=\frac{R}{\lambda_{1}}(1-e^{-\lambda_{1}t})}$$
and activity
$$\boxed{A_{1}(t)=\lambda_{1}N_{1}(t)=R(1-e^{ -\lambda_{1}t })}$$
Recalling that $t_{1/2}=1/\lambda_{1}$, we can see two interesting cases: for a short time after the reaction starts, $t\ll t_{1/2}$, we can approximate the exponential to first order as $e^{-\lambda_{1}t}\simeq 1-\lambda_{1}t$, so the behavior is
$$A_{1}(t)\simeq R\lambda_{1}t$$
So, for a short time after the reaction starts, we can largely approximate the activity as linear. Similarly, after a long time, $t\gg t_{1/2}$, the exponential is basically null, so we get
$$A_{1}(t)\simeq R$$
which is constant. But not just any constant, it's equal to the rate of production. This means that, given sufficient time, the reaction will balance itself out and start decaying at the same rate as new nuclei are being made unstable. This state of equal production-decay is called **[[secular equilibrium]]**.
#### Chain decay
Say the material decays into nuclei that are themselves unstable. This is a very common occurrence in practice, especially on highly unstable [[chemical element|elements]] like plutonium. The daughter nucleus then decays itself, creating a secondary decay product (sometimes called **granddaughter nucleus**). If this is also unstable, the process keeps going and going until all decay products left are stable. The sequence is called a **decay chain**.

To extend the decay law to describe this, we start with $N_{0}$ mother nuclei at $t=0$ and zero of all daughter, granddaughter, etc. nuclei, $N_{2}=\ldots=N_{n}=0$. We'll assume each stage of the chain decays by one mode[^2] with one product. The decay constants are then $\lambda_{1},\ldots,\lambda_{n}$. Chain decay is explained by recursive application of the decay law, considering the activity of the parent nucleus to be the rate of production of the daughter nucleus.

As an example, let's say there's only two steps to the chain: mother → daughter → granddaughter. The mother will decay according to
$$dN_{1}=-\lambda_{1}N_{1}dt$$
which is the usual decay law, which gives $N_{1}(t)=N_{0}e^{ -\lambda_{1}t }$. The daughter will decay as per the [[#Adding unstable nuclei]] section above:
$$dN_{2}=\lambda_{1}N_{1}dt-\lambda_{2}N_{2}dt\tag{1}$$
Now, in order to solve this, we can use the following [[ansatz]]:
$$N_{2}(t)=Ae^{ -\lambda_{1}t }+Be^{ -\lambda_{2}t }$$
where $A$ and $B$ are some constants to be determined. Then, using the starting conditions $N_{2}(0)=0$ and $\dot{N}_{2}(0)=-\dot{N}_{1}(0)=\lambda_{1}N_{0}$, we get
$$\boxed{N_{2}(t)=\frac{\lambda_{1}}{\lambda_{2}-\lambda_{1}}N_{0}(e^{ -\lambda_{1}t }-e^{ -\lambda_{2}t })}$$
This the decay law for the daughter nuclei. Their activity is
$$\boxed{A_{2}(t)=\lambda_{2}N_{2}(t)=\frac{\lambda_{1}\lambda_{2}}{\lambda_{2}-\lambda_{1}}N_{0}(e^{ -\lambda_{1}t }-e^{ -\lambda_{2}t })}$$
Note that if the daughter nuclei were stable, then $\lambda_{2}=0$ and the formula goes back to the original $N_{2}(t)=N_{0}(1-e^{ -\lambda_{1}t })$.

Just like with production-decay, we can isolate some interesting cases.

If $\lambda_{1}\ll \lambda_{2}$, the mother nuclei live so long that the decay is more or less constant and we can say, to zeroth order, $e^{ -\lambda_{1}t }\simeq 1$. In this scenario
$$N_{2}(t)\simeq N_{0} \frac{\lambda_{1}}{\lambda_{2}}(1-e^{ -\lambda_{2}t })$$
with activity given by $A_{2}(t)\simeq \lambda_{1}N_{0}(1-e^{ -\lambda_{2}t })$. In the long term $t\gg 1/\lambda_{2}$, the activity drops to a constant $A_{2}(t)\simeq \lambda_{1}N_{0}$. But this is equal to the activity of the parent nucleus, $A_{1}(t)\simeq \lambda_{1}N_{0}$, which is the production rate of daughter nuclei. The two cancel each other out, leaving a constant number of daughter nuclei (if you don't trust this, just use $(1)$ and check yourself: you get $\dot{N}_{2}=0$). This is another example of secular equilbrium.

If $\lambda_{1}<\lambda_{2}$, the ratio between activities becomes
$$\frac{A_{2}(t)}{A_{1}(t)}=\frac{\lambda_{2}N_{2}}{\lambda_{1}N_{1}}=\frac{\lambda_{2}}{\lambda_{2}-\lambda_{1}}(1-e^{ -(\lambda_{2}-\lambda_{1})t })$$
which in the long term ($t\to \infty$) becomes
$$\frac{A_{2}(t)}{A_{1}(t)}\quad\to \quad \frac{\lambda_{2}}{\lambda_{2}-\lambda_{1}}$$
The ratio becomes constant. This situation, where the ratio of activities tends to a constant number, is called **[[transient equilibrium]]**.

If $\lambda_{1}>\lambda_{2}$, the mother nuclei decay rapidly. The activity of the daughters $A_{2}(t)$ grows rapidly to a maximum, then after some time begins falling according to $\lambda_{2}$ once the mother nuclei run out. When $t\to \infty$, the mother population is negligible, $N_{1}\to 0$, and so $e^{ -\lambda_{1}t }\to0$, so
$$N_{2}(t)\simeq N_{0} \frac{\lambda_{1}}{\lambda_{1}-\lambda_{2}}e^{ -\lambda_{2}t }$$
which is the usual decay law with an effective population $N_{0}\lambda_{1}/(\lambda_{1}-\lambda_{2})$.
##### Arbitrary chains
The derivation above works for a chain of three nuclei (two decaying, one stable). The behavior of an arbitrarily long decay chain is known and is codified by the [[Bateman equation]].

[^1]: Actually, super short measurements of decay down to even one picosecond are actually possible nowadays, but the method is different and requires multiple channels measuring the activity at the same time.

[^2]: If not, since different decay modes lead to different decay products, the chain branches into several chains with different partial decay constants.
