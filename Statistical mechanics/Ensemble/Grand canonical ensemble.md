The **grand canonical ensemble** is an [[ensemble]] that is not [[Physical system|isolated]] from the environment, but is in [[Thermal equilibrium|thermal]] and [[chemical equilibrium]] with a much larger [[Heat reservoir|heat]] and particle reservoir. As such, both [[energy]] and number of [[Particella|particles]] can fluctuate. The conserved quantities are the [[temperature]] $T$ and the [[chemical potential]] $\mu$. Its density function is
$$\rho(z,V,T)=z^{N}Q_{N}(V,T)$$
where $z=e^{\beta \mu}$ is the [[fugacity]] and $Q_{N}$ is the [[Partition function|canonical partition function]]. Its [[partition function]] is
$$\mathcal{Z}(z,V,T)\equiv \sum_{N=0}^{\infty} z^{N}Q_{N}(V,T)$$
### Density function derivation
Let's consider a system and a particle and [[heat reservoir]] of particle numbers $N_{1}$ and $N_{2}$ bound by $N_{2}=N-N_{1}$ and volumes $V_{1}$ and $V_{2}=V-V_{1}$. Let's assume $V_{2}\gg V_{1}$ and $N_{2}\gg N_{1}$ and their [[Hamiltonian|Hamiltonians]] are separable:
$$H(\mathbf{q},\mathbf{p},N)=H_{1}(\mathbf{q}_{1},\mathbf{p}_{1},N_{1})+H_{2}(\mathbf{q}_{2},\mathbf{p}_{2},N_{2})$$
This implicitly means that we are neglecting interactions between the systems beyond the bare minimum required to exchange particles and [[heat]], which generally means that the interaction range is short.

Note how the grand canonical is just an extended version of the [[canonical ensemble]], so let's start from the [[Partition function|canonical partition function]]:
$$Q_{N}=\int \frac{e^{\beta H(\mathbf{q},\mathbf{p},N)}}{h^{3N}N!}d\mathbf{q}\,d\mathbf{p}$$
$N$ is now a variable, so we also need to take every possible combination of $N_{1}$ and $N_{2}$ into account. At a fixed $N_{1}$, the number of states due to $N$ is given by the [[binomial theorem]] as
$$\begin{pmatrix}N \\ N_{1}\end{pmatrix}=\frac{N!}{N_{1}!(N-N_{1})!}=\frac{N!}{N_{1}!N_{2}!}$$
but $N_{1}$ can go anywhere between $0$ and $N$, so the actual total is
$$\sum_{N_{1}=0}^{N}\begin{pmatrix}N \\ N_{1}\end{pmatrix} =\sum_{N_{1}=0}^{N} \frac{N!}{N_{1}!N_{2}!}$$
Since state combinations are found by multiplying, our new partition function looks as follows:
$$\begin{align}
\mathcal{Q}_{N}(V,T)&=\sum_{N_{1}=0}^{N} \frac{N!}{N_{1}!N_{2}!}Q_{N} \\
&=\sum_{N_{1}=0}^{N} \frac{\cancel{ N! }}{N_{1}!N_{2}!}\frac{1}{h^{3(N_{1}+N_{2})}\cancel{ N! }}\int\ e^{-\beta[H_{1}(\mathbf{q}_{1},\mathbf{p}_{1},N_{1})+H_{2}(\mathbf{q}_{2},\mathbf{p}_{2},N_{2})]}d\mathbf{q}d\mathbf{p} \\
&=\sum_{N_{1}=0}^{N}\int\frac{e^{-\beta H_{1}(\mathbf{q}_{1},\mathbf{p}_{1},N_{1})}}{h^{3N_{1}}N_{1}!} d\mathbf{q}_{1}d\mathbf{p}_{1}\int \frac{e^{-\beta H_{2}(\mathbf{q}_{2},\mathbf{p}_{2},N_{2})}}{h^{3N_{2}}N_{2}!} d\mathbf{q}_{2}d\mathbf{p}_{2}\\
&=\sum_{N_{1}=0}^{N} Q_{N_{1}}Q_{N_{2}}=\ldots
\end{align}$$
Note that
$$\sum_{N_{1}=0}^{N} \int  \rho(\mathbf{q}_{1},\mathbf{p}_{1},N_{1})d\mathbf{q}_{1}d\mathbf{p}_{1}=1 \tag{1}$$
We can get
$$\begin{align}
\ldots&=\frac{Q_{N_{2}}(V_{2},T)}{Q_{N}(V,T)} \frac{e^{-\beta H_{1}(\mathbf{q}_{1},\mathbf{p}_{1},N_{1})}}{h^{3N_{1}}N_{1}!}
\end{align}$$
The ratio of partition functions is
$$\frac{Q_{N_{2}}(V_{2},T)}{Q_{N}(V,T)}=e^{-\beta[A(N-N_{1},V-V_{1},T)-A(N,V,T)]}$$
where $A$ is the [[Helmholtz free energy]]
$$A(N-N_{1},V-V_{1},T)-A(N,V,T)\simeq-N_{1}\mu+PV$$
where $\mu$ is the [[chemical potential]]:
$$\mu=\left( \frac{ \partial A(N_{1},V_{1},T) }{ \partial N_{2} }  \right)_{N_{2}=N}$$
which is the rate of change of free energy with respect to number of particles. Also [[pressure]] $P$ from the [[Maxwell relations]]:
$$P=- \left( \frac{ \partial A(N_{2},V_{2},T) }{ \partial V_{2} }  \right)_{V_{2}=V}$$
Putting things together we get a density function
$$\rho(\mathbf{q}_{1},\mathbf{p}_{1},N_{1})=\frac{e^{-\beta(P_{1}V-N_{1}\mu)}}{h^{3N}N_{1}!} e^{-\beta H(\mathbf{q}_{1},\mathbf{p}_{1},N_{1})}$$
Now let's only consider system 1 (and drop the subscript for simplicity) and let's define [[fugacity]] as
$$z\equiv e^{\beta \mu}$$
The density function becomes
$$\boxed{\rho(\mathbf{q},\mathbf{p},N)=\frac{z^{N}}{h^{3N}N!}e^{-\beta PV-\beta H(\mathbf{q},\mathbf{p},N)}}$$
This is dependent on three variables: [[temperature]] $T$ (hidden in $\beta$), pressure $P$ and chemical potential $\mu$ (hidden in $z$).
### Partition function
Using what we found when deriving the density function, we can write the **grand canonical partition function**:
$$\boxed{\mathcal{Z}(z,V,T)\equiv \sum_{N=0}^{\infty} z^{N}Q_{N}(V,T)}$$
which is an extended form of the canonical partition function, weighed by the fugacity.
### Ensemble average
The [[ensemble average]] in the grand canonical ensemble is the canonical ensemble average weighted by the fugacity:
$$\langle O \rangle =\frac{\sum_{N=0}^{\infty}O\,Z^{N}Q_{N}}{\sum_{N=0}^{\infty} Z^{N}Q_{N}}$$
### Energy
Just like in the canonical ensemble, the energy is
$$U=\langle H \rangle =-\frac{ \partial  }{ \partial \beta } \ln \mathcal{Z}(Z,V,T)$$
### Particle number fluctuations
Since $N$ varies, we can express the [[mean]] number of particles as the [[ensemble average]]
$$\langle N \rangle =\frac{1}{\mathcal{Z}}\sum_{N=0}^{\infty}Nz^{N}Q_{N}(V,T)$$
We employ the common method using a derivative to make a quantity (here $N$) disappear:
$$Nz^{N}=z\frac{ \partial  }{ \partial z } z^{N}$$
so
$$\langle N \rangle =\frac{1}{\mathcal{Z}}\sum_{N=0}^{\infty} z\frac{ \partial  }{ \partial z } z^{N}Q_{N}(V,T)=\frac{z}{\mathcal{Z}}\frac{ \partial  }{ \partial z } \sum_{N=0}^{\infty} z^{N}Q_{N}(V,T)=\frac{z}{\mathcal{Z}}\frac{ \partial  }{ \partial z } \mathcal{Z}=z\frac{ \partial  }{ \partial z } \ln \mathcal{Z}$$
And so
$$\boxed{\langle N \rangle =z\frac{ \partial  }{ \partial z } \ln \mathcal{Z}(z,V,T)}\tag{2}$$
Now that we have the mean, we can also find the [[variance]]. The trick is the same as before. If doing $z\frac{ \partial  }{ \partial z }$ gave us $\langle N \rangle$, doing it twice should give us $\langle N^{2} \rangle$:
$$\begin{align}
z\frac{ \partial  }{ \partial z } z\frac{ \partial  }{ \partial z } \ln \mathcal{Z}&=z\frac{ \partial  }{ \partial z } \frac{1}{\mathcal{Z}} \sum_{N=0}^{\infty}Nz^{N}Q_{N} \\
&=z\left[ \frac{1}{\mathcal{Z}}\sum_{N=0}^{\infty} N\left( \frac{ \partial  }{ \partial z } z^{N} \right)Q_{N}+ \left( \frac{ \partial  }{ \partial z } \frac{1}{\mathcal{Z}} \right)\sum_{N=0}^{\infty} Nz^{N}Q_{N} \right] \\
&=z\left[ \frac{1}{\mathcal{Z}} \frac{1}{z}\sum_{N=0}^{\infty} N^{2}z^{N}Q_{N}- \frac{1}{\mathcal{Z}^{2}} \frac{1}{z}\left( \sum_{N=0}^{\infty} Nz^{N}Q_{N} \right)\left( \sum_{N=0}^{\infty} Nz^{N}Q_{N} \right) \right]= \\
&=\frac{\sum_{N=0}^{\infty}N^{2}z^{N}Q_{N}}{\mathcal{Z}}- \left( \frac{\sum_{N=0}^{\infty}Nz^{N}Q_{N}}{\mathcal{Z}} \right)^{2} \\
&=\langle N^{2} \rangle -\langle N \rangle ^{2}
\end{align}$$
which is precisely the variance. However, though we understand what the variance is, the left hand side of the equation is still cryptic. To find the physics in it, we can express the $Z$ derivative in terms of the chemical potential as
$$z\frac{ \partial  }{ \partial z } =z\frac{ \partial \mu }{ \partial z } \frac{ \partial }{ \partial \mu } =z\left( \frac{ \partial  }{ \partial z } k_{B}T\ln z \right)\frac{ \partial  }{ \partial \mu } =k_{B}T\frac{ \partial  }{ \partial \mu } $$
Plugging this back into the previous equation gives us a more interesting look on particle number fluctuations:
$$\boxed{\text{var}(N)=\langle N^{2} \rangle -\langle N \rangle ^{2}=k_{B}^{2}T^{2}\frac{ \partial ^{2}  }{ \partial \mu ^{2} } \ln \mathcal{Z}}$$
Unsurprisingly, higher temperatures mean higher variances.
#### Canonical ensemble equivalence
We can use the previous result to our advantage to prove that the grand canonical and [[Canonical ensemble|canonical ensembles]] are equivalent in the [[Thermodynamic limit]]. In fact, if we divide the particle variance by the square of the volume $V$ occupied the ensemble and we define the particle density $n=N/V$, we get
$$\langle n^{2} \rangle -\langle n \rangle ^{2}=\frac{k_{B}^{2}T^{2}}{V^{2}}\frac{ \partial ^{2} }{ \partial \mu ^{2} } \ln \mathcal{Z}$$
When $V\to \infty$ in the limit, this equation goes to zero, which means that particle density fluctuations nullify, which in turn also means that particle number fluctuations are also zero.
### Thermodynamics
To derive thermodynamics relations in the grand canonical, we can do something similar to keeping only the highest [[entropy]] state in the [[microcanonical ensemble]]. The grand canonical partition function is a sum:
$$\mathcal{Z}=\sum_{N=0}^{\infty} z^{N}Q_{N}$$
If one term (call it $\langle N \rangle$) is considerably larger than all the others, we can keep only that one and approximate the sum away. This happens if the number variance is vanishingly small, which is to say in the thermodynamic limit. In this case, we can state
$$\mathcal{Z}=\sum_{N=0}^{\infty} z^{N}Q_{N}\simeq z^{\langle N \rangle}Q_{\langle N \rangle}$$
The logarithm simplifies considerably:
$$\ln \mathcal{Z}\simeq \ln(z^{\langle N \rangle}Q_{\langle N \rangle})=\langle N \rangle\ln z+\ln Q_{\langle N \rangle}=\langle N \rangle\beta\mu-\beta A_{\langle N \rangle}$$
where $A_{\langle N \rangle}$ is the [[Helmholtz free energy]] in state $\langle N \rangle$. We can state $A_{N}=Na(v,T)$ by defining $a$ as the free energy per particle, using $v=V/N$ as the specific volume of the ensemble. Doing this, we get
$$\ln \mathcal{Z}\simeq \langle N \rangle\beta\mu-\beta\langle N \rangle a(\langle v \rangle,T)=\langle N \rangle\beta(\mu-a(\langle v \rangle,T))$$
where $\langle v \rangle=V/\langle N \rangle$. Unfortunately, $a(\langle v \rangle,T)$ is a somewhat cryptic quantity and it would be nice to express it in terms of better understood ones. Fortunately, this is possible by calculating a couple of thermodynamic quantities. [[Pressure]] is
$$P=-\left( \frac{ \partial A }{ \partial V } \right)_{N,T}=-N\frac{ \partial a\left( \frac{V}{T},T \right) }{ \partial V } =-\frac{ \partial a }{ \partial v } $$
and the chemical potential is
$$\mu=\left( \frac{ \partial A }{ \partial N }  \right)_{V,T}=\frac{ \partial N }{ \partial N } a+N\frac{ \partial a\left( \frac{V}{N},T \right) }{ \partial N } =a-N \frac{V}{N^{2}}\frac{ \partial a }{ \partial v }=a-v\frac{ \partial a }{ \partial v } =a+vP\tag{2}$$
Inverting this relation gives us $a=\mu-vP$. If we put this back in the partition function, we find
$$\ln \mathcal{Z}\simeq \langle N \rangle\beta(\mu-\mu+\langle v \rangle P)=\langle N \rangle\beta \langle v \rangle P=\langle N \rangle\beta \frac{V}{\langle N \rangle}P=\beta PV=\frac{PV}{k_{B}T}$$
Thus, in thermodynamic limit, we find an [[equation of state]]:
$$\boxed{\ln \mathcal{Z}=\frac{PV}{k_{B}T}}\tag{3}$$
Note that it is independent from the number of particles $\langle N \rangle$. Since $\langle N \rangle$ is also the only state that matters for the number of particles (as long as we are in the thermodynamic limit), we can write $\langle N \rangle=N$ without much loss.
#### Number fluctuations, again
Now that we have a sensible expression for $\ln \mathcal{Z}$, we can give a more satisfactory description of particle number fluctuations. In fact, we get
$$\langle n^{2} \rangle -\langle n \rangle ^{2}=\left( \frac{k_{B}T}{V} \right)^{2}\frac{ \partial ^{2} }{ \partial \mu ^{2} } \left( \frac{PV}{k_{B}T} \right)=\frac{k_{B}T}{V}\frac{ \partial ^{2}P }{ \partial \mu ^{2} }$$
We can use the following relation
$$\frac{ \partial \mu }{ \partial v } =-v\frac{ \partial ^{2}a(v) }{ \partial v^{2} } =v\frac{ \partial P }{ \partial v } \quad\to \quad \frac{ \partial P }{ \partial v } \frac{ \partial v }{ \partial \mu } =\frac{1}{v}$$
and so
$$\frac{ \partial P }{ \partial \mu }=\frac{ \partial P }{ \partial v } \frac{ \partial v }{ \partial \mu } =\frac{1}{v} $$
However, $v$ is itself dependent on $\mu$, which gives us
$$\frac{ \partial ^{2}P }{ \partial \mu ^{2} }= - \frac{1}{v^{2}}\frac{ \partial v }{ \partial \mu } =\frac{\kappa_{T}}{v^{2}}$$
where we defined the [[Compressibility|isothermal compressibility]] $\kappa_{T}$. As such, our fluctuations become
$$\frac{\langle n^{2} \rangle -\langle n \rangle ^{2}}{\langle n \rangle ^{2}}=\frac{k_{B}T\kappa_{T}}{V}$$
In the thermodynamic limit, these again vanish.
### Virial expansion
The equation of state $(3)$ can be rewritten using $(2)$ as
$$n=\frac{1}{V}Z\frac{ \partial  }{ \partial Z } \ln \mathcal{Z}(Z,V,T)$$
If the temperature is sufficiently high and the particle density is sufficiently low, the equation in both forms can be expanded as a [[serie di potenze|power series]] in $Z$:
$$\frac{P}{k_{B}T}=\frac{1}{\lambda ^{3}}\sum_{l=1}^{\infty} b_{l}Z^{l},\qquad n=\frac{1}{\lambda ^{3}}\sum_{l=1}^{\infty} lb_{l}Z^{l}$$
using the [[Formula di de Broglie|de Broglie thermal wavelength]] $\lambda$. The coefficients $b_{l}$ are known as **cluster integrals** and represents the internal correlation of a group of $l$ particles due to interactions. By definition, $b_{1}\equiv1$.

[^1]: Note how, unlike the [[microcanonical ensemble]], entropy is derived last.