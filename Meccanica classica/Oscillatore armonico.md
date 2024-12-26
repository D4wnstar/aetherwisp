---
aliases:
  - legge di Hooke
  - phonon
---
Un **oscillatore armonico** è un sistema dotato di un [[punto di equilibrio]] che, dopo aver subito una perturbazione, sperimenta una forza di ritorno $F$ proporzionale alla distanza di spostamento $x$ secondo la **legge di Hooke**:
$$\vec{F}=-k\vec{x}$$
con $k$ una costante positiva detta **costante elastica**.
### Moto armonico semplice
Se la forza $F$ è l'unica che agisce sul sistema, esso prende il nome di **oscillatore armonico semplice** e l'oggetto in movimento descrive un **moto armonico semplice**. In questo caso, possiamo usare la [[Newton's laws|seconda legge del moto]] per analizzare il sistema:
$$F=ma=m\ddot{x}=-kx$$
che ci dà un'equazione differenziale lineare di secondo ordine
$$\ddot{x}=- \frac{k}{m}x=-\omega^{2}x$$
dove $\omega=\sqrt{k/m}$ è la frequenza angolare. La soluzione generale è della forma
$$x(t)=A\cos(\omega t)+B\sin(\omega t)=C\cos(\omega t+\varphi)$$
con le costanti determinate dalle condizioni al contorno, come di norma. Questo moto è periodico e il periodo è $T=2\pi/\omega$.

La velocità e l'accelerazione oscillano con la stessa frequenza, ma hanno fase diversa dalla posizione. In particolare, la velocità è minima quando lo spostamento è massimo e viceversa.

L'oscillatore ha energia [[potenziale]] in posizione $x$ pari a
$$V=\frac{1}{2}kx^{2}\tag{1}$$
e la forza è conservativa.
### Approssimazioni
L'oscillatore armonico è estremamente importante perché *qualunque* potenziale $V(x)$ associato ad un moto oscillatorio può essere approssimato come una parabola della forma $(1)$ fintantoché l'oscillazione è piccola. Per dimostrarlo, espandiamo $V(x)$ in [[Serie di Taylor|serie di Taylor]] centrata in un minimo locale $x_{0}$:
$$V(x)=V(x_{0})+V'(x_{0})(x-x_{0})+ \frac{1}{2}V''(x_{0})(x-x_{0})^{2}+O(x^{3})$$
Dato che la costante $V(x_{0})$ si annulla derivando per ottenere la forza, possiamo sottrarla senza perdita di generalità. Inoltre, dato che $x_{0}$ è un [[punto critico]], $V'(x_{0})=0$. Dunque ci rimane la forma esatta
$$V(x)=\frac{1}{2}V''(x_{0})(x-x_{0})^{2}+O(x^{3})$$
che possiamo approssimare troncando tutti i termini di terzo ordine e superiore, che sono piccoli se anche le oscillazioni lo sono:
$$V(x)\simeq \frac{1}{2}V''(x_{0})(x-x_{0})^{2}$$
che ha la stessa forma di $(1)$. $V''(x_{0})>0$ perché $x_{0}$ è un minimo per costruzione. Ciò significa che, per piccole oscillazioni, ogni moto oscillatorio può essere trattato come se fosse un oscillatore armonico.
### Oscillator chains
A system made of a chain of harmonic oscillators can be solved analytically by exploiting the fact that all quadratic forms can [[diagonalizzazione|diagonalized]]. These are commonly employed in atomic and solid state physics, especially crystals.
#### 1D crystal
Consider a series of $N$ particles on a one dimensional line (possibly embedded in a higher dimensional plane), each equally spaced by a distance $a$. We define the position vector $\mathbf{n}=n\mathbf{a}$, where $n=0,1,2\ldots,N$. Each point is subject to harmonic oscillations. If we call $\xi_{\mathbf{n}}$ the distance from the [[equilibrium point]] for the particle in $\mathbf{n}$, we can write
$$K=\frac{m}{2}\sum_{\mathbf{n}}\dot{\xi}_{\mathbf{n}}^{2}$$
and potential energy
$$U=\frac{\gamma}{2}\sum_{\mathbf{n}}(\xi_{\mathbf{n}}-\xi_{\mathbf{n}-\mathbf{a}})^{2}$$
with $\gamma \in \mathbb{R}$. The distance $\xi$ has the periodic relation $\xi_{\mathbf{n}}=\xi_{\mathbf{n}+\mathbf{a}}$, which is our boundary condition. If we describe the oscillation across all particles as a traveling [[plane wave]] of condition $e^{i\mathbf{k}\cdot \mathbf{x}}\to e^{-i\mathbf{k}\cdot (\mathbf{x}+\mathbf{a})}$, we can write our [[wave vector]] as
$$\mathbf{k}=\frac{2\pi \mu}{Na^{2}}\mathbf{a}$$
where $\mu \in \mathbb{N}$ determines the number of possible oscillation states
$$\mu=- \frac{N}{2},\ldots, \frac{N}{2}-1$$
In a lattice containing $N$ elements, there are exactly $N$ modes of oscillation. The region $-\pi\leq \mathbf{k}\cdot \mathbf{a}\leq \pi$ is called a **Brillouin zone**. In this context, we can write the distance $\xi$ as
$$\xi_{\mathbf{n}}=\frac{1}{\sqrt{ N }}\sum_{\mathbf{k}}A_{\mathbf{k}}e^{i\mathbf{k}\cdot \mathbf{n}},\qquad A_{\mathbf{k}}=\frac{1}{\sqrt{ N }}\sum_{\mathbf{n}}\xi_{\mathbf{n}}e^{-i\mathbf{k}\cdot \mathbf{n}}$$
which are [[Trasformata di Fourier|Fourier transforms]] of each other. We also have $A_{\mathbf{k}}=A_{-\mathbf{k}}^{*}$ and
$$\frac{1}{N}\sum_{\mathbf{n}}e^{i(\mathbf{k}-\mathbf{k}')\cdot\mathbf{n}}=\delta_{\mathbf{k}\mathbf{k'}},\qquad \frac{1}{N}\sum_{\mathbf{k}}e^{i\mathbf{k}\cdot(\mathbf{n}-\mathbf{n}')}=\delta_{\mathbf{n}\mathbf{n'}}$$
Through undisclosed magic (???) we have
$$K=\frac{m}{2}\sum_{\mathbf{n}}\dot{A}_{\mathbf{k}}\dot{A}_{-\mathbf{k}},\qquad U=\frac{m}{2}\sum_{\mathbf{k}}\Omega^{2}(\mathbf{k})A_{\mathbf{k}}A_{-\mathbf{k}}$$
By evenness of $\Omega ^{2}$ we have
$$m\Omega ^{2}(\mathbf{k})=m\Omega ^{2}(-\mathbf{k})=4\gamma \sin ^{2} \frac{\mathbf{k}\cdot \mathbf{a}}{2}$$
The [[Lagrangian]] is
$$L=K-U=\frac{m}{2}\sum_{\mathbf{k}}(\dot{A}_{\mathbf{k}}\dot{A}_{-\mathbf{k}}-\Omega ^{2}(\mathbf{K})A_{\mathbf{k}}A_{-\mathbf{k}})$$
If we defined
$$P_{\mathbf{k}}=\frac{ \partial L }{ \partial \dot{A}_{\mathbf{k}} } =m \dot{A}$$
$$P=\frac{1}{}\sum p_{\mathbf{n}}e^{i\mathbf{k}\cdot \mathbf{n}}$$
with momentum $p_{\mathbf{n}}=m \dot{\xi}_{vn}$. With this, we make the jump to a [[Hamiltonian]]
$$H=???$$
...

A **phonon** is the quantum of a normal mode of oscillation. It has frequency $\omega$ and energy $\hbar \omega$.
$$\hat{H}=\frac{\hbar}{2}\sum_{\mathbf{k}}\Omega(\mathbf{k})(\hat{b}^{+}_{\mathbf{k}}\hat{b}_{\mathbf{k}}+\hat{b}_{\mathbf{k}}\hat{b}^{+}_{\mathbf{k}})$$
The velocity of a phonon is usually denoted as $c$ and called the **speed of sound**. Note that it's not the [[velocità della luce|speed of light]], despite using the same letter. It depends on the properties of the material. A crystal of $N$ atoms has $3N$ modes of oscillations. These modes are bound by the condition
$$\int_{0}^{\omega_{\text{max}}}f(\omega)d\omega=3N$$
where $\omega _\text{max}$ is known as the **Debye frequency**. We have
$$f(\omega)d\omega=\frac{3V}{(2\pi)^{3}}4\pi k^{2}dk=\frac{3V\omega ^{2}}{2\pi^{2}c^{3}}d\omega$$
The maximum frequency
$$\omega_{\text{max}}=c\left( \frac{6\pi ^{2}N}{V} \right)=c\left( \frac{6\pi ^{2}}{v} \right)^{1/3}$$
with $v=V/N$. The speed of sound is
$$c=\frac{\lambda_{\text{max}}}{2\pi} \frac{2\pi}{T}=\frac{\lambda _\text{max}\omega}{2\pi}$$
Notice how the speed of sound is acting as a limiter on what the maximum wavelength is. This is, in a way, the same role as the speed of light plays in electromagnetism, by being a speed limit. Although light is limited by fundamental physics, sound is limited because oscillations are movements of a discretely-spaced lattice. Any wavelength shorter than the lattice spacing is bound to be irrelevant as it gets "lost" between the particles.
$$\lambda _\text{max}=\frac{2\pi c}{\omega _\text{max}}\sim v^{1/3}\sim\text{distance between atoms}$$

We can describe a 1D crystal as a [[canonical ensemble]] of phonons. The total energy is
$$E(\{ n_{i} \})=\sum_{i=1}^{3N} n_{i}\hbar \omega_{i}$$
The [[partition function]] is
$$Q=\sum_{\{ n_{i} \}}e^{-\beta E(\{ n_{i} \})}=\prod_{i=1}^{3N} \frac{1}{1-e^{-\beta \hbar \omega_{i}}}$$
and its logarithm
$$\log Q=-\sum_{i=1}^{3N} \log(1-e^{-\beta \hbar \omega_{i}})$$
The average [[occupation number]] is
$$\langle n_{i} \rangle =- \frac{1}{\beta \frac{ \partial  }{ \partial (\hbar \omega) } }\log Q=\frac{1}{e^{\beta \hbar \omega}-1}$$
The [[internal energy]] is
$$U=-\frac{ \partial  }{ \partial \beta } \log Q=\sum_{i=1}^{3N} \hbar \omega_{i}\langle n_{i} \rangle =\sum_{i=1}^{3N} \frac{\hbar \omega_{i}}{e^{\beta \hbar \omega_{i}}-1}$$
In the [[Thermodynamic limit]] it becomes
$$U=\frac{3V}{2\pi ^{2}c^{3}}\int_{0}^{\omega _\text{max}}\omega ^{2} \frac{1}{e^{\beta \hbar \omega}-1}d\omega$$
The energy density by particle is
$$\frac{U}{N}=\frac{g(k_{B}T)^{4}}{(\hbar \omega _\text{max})^{3}}\int_{0}^{\beta \hbar \omega _\text{max}} \frac{t^{3}}{e^{t}-1}dt$$
If we defined the **Debye function** $D(x)$ as
$$D(x)\equiv\frac{3}{x^{3}}\int_{0}^{x} \frac{t^{3}}{e^{t}-1}dt$$
and the **Debye temperature** $T_{D}\equiv \hbar \omega _\text{max}/k_{B}$, we can simplify the form as
$$\boxed{\frac{U}{N}=3k_{B}TD\left( \frac{T}{T_{D}} \right)}$$
which is the [[equation of state]] for phonons. We can also recover [[heat capacity]] as
$$\frac{C_{V}}{Nk_{B}}=3D(\lambda)+3T \frac{ \partial D(\lambda) }{ \partial T }=3\left[ 4D(\lambda)- \frac{3\lambda}{e^{\lambda}-1} \right] $$
In the limit of high temperatures ($T\gg T_{D}$), we can see the classical [[Dulong-Petit law]]:
$$\frac{C_{V}}{Nk_{B}}=3=\frac{3}{2}+ \frac{3}{2}$$
which shows that all crystalline solids have the same heat capacity.