**Poynting's theorem** is a result expressing conservation of [[energy]] in electrodynamics. It states that in a given volume $V$, the stored electromagnetic energy $U$ changes at a [[power|rate]] $P$ given by the [[work]] done on the [[electric charge|charges]] within the volume, minus the rate at which energy leaves the volume. In integral form it reads
$$P=\frac{ \partial U }{ \partial t } =-\frac{ \partial  }{ \partial t } \int_{V}u(\mathbf{r})\ d\tau-\oint_{S}\mathbf{S}\cdot d\mathbf{a}$$
where $u(\mathbf{r})$ is the electromagnetic energy density, $S$ is the bounding [[Surface|surface]] of $V$ and $\mathbf{S}$ is the [[Poynting vector]]. It is closely related to the continuity equation for [[electric current]] $\nabla\cdot\mathbf{J}=-\frac{ \partial \rho }{ \partial t }$.

Knowing that $P=\int_{V}\mathbf{E}\cdot \mathbf{J}\ dV$, using the [[Divergence theorem|divergence theorem]] and reordering the terms in a more significant order, we can also rewrite the statement in differential form as
$$-\frac{ \partial u(\mathbf{r}) }{ \partial t }=\mathbf{E}\cdot \mathbf{J} -\nabla\cdot\mathbf{S}$$
### Derivation
We can express work through the electric current density. Starting from the work done by the Lorentz force $dW=q\mathbf{E}\cdot d\mathbf{s}$ over a line element $d\mathbf{s}$, if we take an infinitesimal volume $dV$, the charge inside is $dq=\rho dV$. If it moves at a velocity $\mathbf{v}$, the work over a time $dt$ is
$$dq\mathbf{E}\cdot \mathbf{v}dt=\rho dV\ \mathbf{E}\cdot \mathbf{v}dt=\mathbf{E}\cdot \rho \mathbf{v}\ dVdt=\mathbf{E}\cdot \mathbf{J}\ dVdt=d^{2}W$$
(the square on the work [[differential]] is because there are two infinitesimals now, and as such it is a second-order differential). If we "divide" by $dt$[^1] and integrate over the volume we get the power
$$P=\frac{dW}{dt}=\int_{V}\mathbf{E}\cdot \mathbf{J}\ dV$$
We can elaborate on $\mathbf{E}\cdot \mathbf{J}$:
$$\begin{align}
\mathbf{E}\cdot \mathbf{J}&=\mathbf{E}\cdot \frac{\nabla\times\mathbf{B}}{\mu_{0}}-\varepsilon_{0}\mathbf{E}\frac{ \partial \mathbf{E} }{ \partial t } \\
&=\mathbf{E}\cdot \frac{\nabla\times\mathbf{B}}{\mu_{0}}- \frac{\varepsilon_{0}}{2}\frac{ \partial E^{2} }{ \partial t }  \\
&=\frac{\mathbf{B}\cdot(\nabla\times\mathbf{E})}{\mu_{0}}- \frac{\nabla\cdot(\mathbf{E}\times \mathbf{B})}{\mu_{0}}- \frac{\varepsilon_{0}}{2} \frac{ \partial E^{2} }{ \partial t }  \\
&=- \frac{1}{\mu_{0}} \left( \mathbf{B}\cdot \frac{ \partial \mathbf{B} }{ \partial t } \right) - \frac{1}{\mu_{0}}(\nabla \cdot(\mathbf{E}\times \mathbf{B}))- \frac{\varepsilon_{0}}{2}\frac{ \partial E^{2} }{ \partial t } \\
&=- \frac{1}{2\mu_{0}}\frac{ \partial B^{2} }{ \partial t } - \frac{\varepsilon_{0}}{2}\frac{ \partial E^{2} }{ \partial t } -\nabla\cdot \mathbf{S}
\end{align}$$
where we used $\frac{ \partial E^{2} }{ \partial t }=\frac{ \partial  }{ \partial t }(\mathbf{E}\cdot \mathbf{E})=2\mathbf{E}\frac{ \partial \mathbf{E} }{ \partial t }$, expanded $\mathbf{E}\cdot \nabla\times\mathbf{B}$ using vector calculus, used [[Faraday's law]] and defined the [[Poynting vector]]
$$\mathbf{S}=\frac{1}{\mu_{0}}\mathbf{E}\times \mathbf{B}$$
If we extract and merge the time derivative from the first two terms, we are left with the electromagnetic energy density by volume $u$:
$$- \frac{1}{2\mu_{0}}\frac{ \partial B^{2} }{ \partial t } - \frac{\varepsilon_{0}}{2}\frac{ \partial E^{2} }{ \partial t }=-\frac{ \partial  }{ \partial t } \left( \frac{1}{2\mu_{0}}B^{2} + \frac{\varepsilon_{0}}{2}E^{2} \right)=-\frac{ \partial u }{ \partial t }$$
If we plug this back into the power expression, we get
$$P=-\frac{ \partial  }{ \partial t } \int_{V}u\ d\tau-\int_{V}\nabla\cdot\mathbf{S}=-\frac{ \partial  }{ \partial t } \int_{V}u\ d\tau-\oint_{S}\mathbf{S}\cdot d\mathbf{a}$$
where we used the [[Divergence theorem|divergence theorem]]. This final expression in commonly known as **Poynting's theorem**:
$$\boxed{P=-\frac{ \partial  }{ \partial t } \int_{V}u(\mathbf{r})\ d\tau-\oint_{S}\mathbf{S}\cdot d\mathbf{a}}$$

[^1]: Please do not say this in front of a mathematician if you value your life.
