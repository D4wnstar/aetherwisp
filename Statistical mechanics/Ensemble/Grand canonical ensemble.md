The **grand canonical ensemble** is an [[ensemble]] that is not [[Physical system|isolated]] from the environment, but is in [[Thermal equilibrium|thermal]] and [[chemical equilibrium]] with a much larger [[Heat reservoir|heat]] and particle reservoir. As such, both [[energy]] and number of [[Particella|particles]] can fluctuate. The conserved quantities are the [[temperature]] $T$ and the [[chemical potential]] $\mu$. Its density function is
$$\rho(Z,V,T)=Z^{N}Q_{N}(V,T)$$
where $Z=e^{\beta \mu}$ and $Q_{N}$ is the [[Partition function|canonical partition function]]. Its [[partition function]] is
$$\mathcal{Z}(Z,V,T)\equiv \sum_{N=0}^{\infty} Z^{N}Q_{N}(V,T)$$
### Density function derivation
Let's consider two gases of particle numbers $N_{1}$ and $N_{2}$ bound by $N_{2}=N-N_{1}$ and volumes $V_{1}$ and $V_{2}$. Let's assume $V_{2}\gg V_{1}$ and $N_{2}\gg N_{1}$ and that the [[Hamiltonian]] is additive:
$$H(\mathbf{q},\mathbf{p},N)=H(\mathbf{q}_{1},\mathbf{p}_{1},N_{1})+H(\mathbf{q}_{2},\mathbf{p}_{2},N_{2})$$
This implicitly means that we are neglecting interactions between the gases, which generally means that the interaction range is short.

Note how the grand canonical is just an extended version of the [[canonical ensemble]], so let's start from that [[partition function]]:
$$Q_{N}=\int \frac{e^{\beta H(\mathbf{q},\mathbf{p},N)}}{h^{3N}N!}dq\,dp$$
$N$ becomes variable in time so
$$\begin{align}
Q_{N}(V,T)&=\frac{1}{h^{3N}N!}\int dq_{1}dp_{1}\sum_{N_{1}=0}^{N} \frac{N!}{N_{1}!N_{2}!}\int_{V_{1}}dq_{1}\int_{V_{2}}dq_{2}\ e^{-\beta[H(\mathbf{q}_{1},\mathbf{p}_{1},B_{1})+H(\mathbf{q}_{2},\mathbf{p}_{2},N_{2})]} \\
&=\sum_{N_{1}=0}^{N} \frac{1}{h^{3N}N!}\int dp_{1}\int_{V_{1}} dq_{1}\ \frac{e^{-\beta H(\mathbf{q}_{1},\mathbf{p}_{1},N_{1})}}{h^{3N_{1}}N_{1}!} \frac{1}{h^{3N_{2}}N_{2}!}\int dp_{2}\int_{V_{2}} dq_{2}\ e^{-\beta H(\mathbf{q}_{2},\mathbf{p}_{2},N_{2})} \\
&=\ldots
\end{align}$$
Note that
$$\sum_{N_{1}=0}^{N} \int dp_{1}\int_{V_{1}}dq_{1}\rho(\mathbf{q}_{1},\mathbf{p}_{1},N_{1})=1\tag{1}$$
We can get
$$\begin{align}
\ldots&=\frac{Q_{N_{2}}(V_{2},T)}{Q_{N}(V,T)} \frac{e^{-\beta H(\mathbf{q}_{1},\mathbf{p}_{1},N_{1})}}{h^{3N_{1}}N_{1}!}
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
$$Z\equiv e^{\beta \mu}$$
The density function becomes
$$\boxed{\rho(\mathbf{q},\mathbf{p},N)=\frac{Z^{N}}{h^{3N}N!}e^{-\beta PV-\beta H(\mathbf{q},\mathbf{p},N)}}$$
This is dependent on three variables: [[temperature]] $T$ (hidden in $\beta$), pressure $P$ and chemical potential $\mu$ (hidden in $Z$).
### Partition function
Using what we found when deriving the density function, we can write the **grand canonical partition function**:
$$\boxed{\mathcal{Z}(Z,V,T)\equiv \sum_{N=0}^{\infty} Z^{N}Q_{N}(V,T)}$$
which is an extended form of the canonical partition function, weighed by the fugacity.
### Ensemble average
The [[ensemble average]] in the grand canonical ensemble is the canonical ensemble average weighted by the fugacity:
$$\langle O \rangle =\frac{\sum_{N=0}^{\infty}O\,Z^{N}Q_{N}}{\sum_{N=0}^{\infty} Z^{N}Q_{N}}$$
### Energy
Just like in the canonical ensemble, the energy is
$$U=\langle H \rangle =-\frac{ \partial  }{ \partial \beta } \ln \mathcal{Z}(Z,V,T)$$
### Particle number fluctuations
Since $N$ varies, we can express the [[mean]] number of particles as the [[ensemble average]]
$$\langle N \rangle =\frac{\sum_{N=0}^{\infty}NZ^{N}Q_{N}(V,T)}{\sum_{N=0}^{\infty} Z^{N}Q_{N}(V,T)}$$
The trick is to take the $Z$ derivative of $\ln Z$:
$$\frac{ \partial  }{ \partial Z } \ln \mathcal{Z}=\frac{1}{\sum_{N=0}^{\infty} Z^{N}Q_{N}}\frac{ \partial  }{ \partial Z } \mathcal{Z}=\ldots$$
The $Z$ derivative of the partition function reduces to
$$\frac{ \partial  }{ \partial Z } \mathcal{Z}=\sum_{N=0}^{\infty} \left( \frac{ \partial  }{ \partial Z } Z^{N} \right)Q_{N}=\sum_{N=0}^{\infty} NZ^{N-1}Q_{N}=\frac{1}{Z}\sum_{N=0}^{\infty} NZ^{N}Q_{N}$$
and so we have
$$\ldots=\frac{1}{Z} \frac{\sum_{N=0}^{\infty} NZ^{N}Q_{N}}{\sum_{N=0}^{\infty} Z^{N}Q_{N} }=\frac{1}{Z}\langle N \rangle $$
By inverting the equation, can get
$$\boxed{\langle N \rangle =Z\frac{ \partial  }{ \partial Z } \log \mathcal{Z}(Z,V,T)}$$
Now that we have the mean, we can also find the [[variance]]. The trick is the same as before. If doing $Z\frac{ \partial  }{ \partial Z }$ gave us $\langle N \rangle$, doing it twice should give us $\langle N^{2} \rangle$:
$$\begin{align}
Z\frac{ \partial  }{ \partial Z } Z\frac{ \partial  }{ \partial Z } \ln \mathcal{Z}&=Z\frac{ \partial  }{ \partial Z } \frac{\sum_{N=0}^{\infty}NZ^{N}Q_{N}}{\mathcal{Z}} \\
&=Z\left[ \frac{1}{\mathcal{Z}}\sum_{N=0}^{\infty} N\left( \frac{ \partial  }{ \partial Z } Z^{N} \right)Q_{N}+ \left( \frac{ \partial  }{ \partial Z } \frac{1}{\mathcal{Z}} \right)\sum_{N=0}^{\infty} NZ^{N}Q_{N} \right] \\
&=Z\left[ \frac{1}{\mathcal{Z}} \frac{1}{Z}\sum_{N=0}^{\infty} N^{2}Z^{N}Q_{N}- \frac{1}{\mathcal{Z}^{2}} \frac{1}{Z}\left( \sum_{N=0}^{\infty} NZ^{N}Q_{N} \right)\left( \sum_{N=0}^{\infty} NZ^{N}Q_{N} \right) \right]= \\
&=\frac{\sum_{N=0}^{\infty}N^{2}Z^{N}Q_{N}}{\mathcal{Z}}- \left( \frac{\sum_{N=0}^{\infty}NZ^{N}Q_{N}}{\mathcal{Z}} \right)^{2} \\
&=\langle N^{2} \rangle -\langle N \rangle ^{2}
\end{align}$$
which is precisely the variance. However, though we understand what the variance is, the left hand side of the equation is still cryptic. To find the physics in it, we can express the $Z$ derivative in terms of the chemical potential as
$$Z\frac{ \partial  }{ \partial Z } =Z\frac{ \partial \mu }{ \partial Z } \frac{ \partial }{ \partial \mu } =Z\left( \frac{ \partial  }{ \partial Z } k_{B}T\ln Z \right)\frac{ \partial  }{ \partial \mu } =k_{B}T\frac{ \partial  }{ \partial \mu } $$
Plugging this back into the previous equation gives us a more interesting look on particle number fluctuations:
$$\boxed{\langle N^{2} \rangle -\langle N \rangle ^{2}=k_{B}^{2}T^{2}\frac{ \partial ^{2}  }{ \partial \mu ^{2} } \ln \mathcal{Z}}$$
Unsurprisingly, higher temperatures mean higher variances.
#### Canonical ensemble equivalence
We can use the previous result to our advantage to prove that the grand canonical and [[Canonical ensemble|canonical ensembles]] are equivalent in the [[thermodynamic limit]]. In fact, if we divide the particle variance by the square of the volume $V$ occupied the ensemble and we define the particle density $n=N/V$, we get
$$\langle n^{2} \rangle -\langle n \rangle ^{2}=\frac{k_{B}^{2}T^{2}}{V^{2}}\frac{ \partial ^{2} }{ \partial \mu ^{2} } \ln \mathcal{Z}$$
When $V\to \infty$ in the limit, this equation goes to zero, which means that particle density fluctuations nullify, which in turn also means that particle number fluctuations are also zero.
### Thermodynamics
To derive thermodynamics relations in the grand canonical, we can do something similar to keeping only the highest [[entropy]] state in the [[microcanonical ensemble]]. The grand canonical partition function is a sum:
$$\mathcal{Z}=\sum_{N=0}^{\infty} Z^{N}Q_{N}$$
If one term (call it $\langle N \rangle$) is considerably larger than all the others, we can keep only that one and approximate the sum away. This happens if the number variance is vanishingly small, which is to say in the thermodynamic limit. In this case, we can state
$$\mathcal{Z}=\sum_{N=0}^{\infty} Z^{N}Q_{N}\simeq Z^{\langle N \rangle}Q_{\langle N \rangle}$$
The logarithm simplifies considerably:
$$\ln \mathcal{Z}\simeq \ln(Z^{\langle N \rangle}Q_{\langle N \rangle})=\langle N \rangle\ln Z+\ln Q_{\langle N \rangle}=\langle N \rangle\beta\mu-\beta A_{\langle N \rangle}$$
where $A_{\langle N \rangle}$ is the [[Helmholtz free energy]] in state $\langle N \rangle$. We can state $A_{N}=Na(v,T)$ by defining $a$ as the free energy per particle, using $v=V/N$ as the specific volume of the ensemble. Doing this, we get
$$\ln \mathcal{Z}\simeq \langle N \rangle\beta\mu-\beta\langle N \rangle a(\langle v \rangle,T)=\langle N \rangle\beta(\mu-a(\langle v \rangle,T))$$
where $\langle v \rangle=V/\langle N \rangle$. Unfortunately, $a(\langle v \rangle,T)$ is a somewhat cryptic quantity and it would be nice to express it in terms of better understood ones. Fortunately, this is possible by calculating a couple of thermodynamic quantities. [[Pressure]] is
$$P=-\left( \frac{ \partial A }{ \partial V } \right)_{N,T}=-N\frac{ \partial a\left( \frac{V}{T},T \right) }{ \partial V } =-\frac{ \partial a }{ \partial v } $$
and the chemical potential is
$$\mu=\left( \frac{ \partial A }{ \partial N }  \right)_{V,T}=\frac{ \partial N }{ \partial N } a+N\frac{ \partial a\left( \frac{V}{N},T \right) }{ \partial N } =a-N \frac{V}{N^{2}}\frac{ \partial a }{ \partial v }=a-v\frac{ \partial a }{ \partial v } =a+vP\tag{2}$$
Inverting this relation gives us $a=\mu-vP$. If we put this back in the partition function, we find
$$\ln \mathcal{Z}\simeq \langle N \rangle\beta(\mu-\mu+\langle v \rangle P)=\langle N \rangle\beta \langle v \rangle P=\langle N \rangle\beta \frac{V}{\langle N \rangle}P=\beta PV=\frac{PV}{k_{B}T}$$
Thus, in thermodynamic limit, we have
$$\boxed{\ln \mathcal{Z}=\frac{PV}{k_{B}T}}$$
Note that it is independent from the number of particles $\langle N \rangle$. Since $\langle N \rangle$ is also the only state that matters for the number of particles (as long as we are in the thermodynamic limit), we can write $\langle N \rangle=N$ without much loss.
#### Number fluctuations, again
Now that we have a sensible expression for $\ln \mathcal{Z}$, we can give a more satisfactory description of particle number fluctuations. In fact, we get
$$\langle n^{2} \rangle -\langle n \rangle ^{2}=\left( \frac{k_{B}T}{V} \right)^{2}\frac{ \partial ^{2} }{ \partial \mu ^{2} } \left( \frac{PV}{k_{B}T} \right)=\frac{k_{B}T}{V}\frac{ \partial ^{2}P }{ \partial \mu ^{2} }$$
We can invert $(2)$ to get
$$P=\frac{\mu-a}{v}$$
and so
$$\frac{ \partial P }{ \partial \mu }  =\frac{1}{v}$$
However, $v$ is itself dependent on $\mu$, which gives us
$$\frac{ \partial ^{2}P }{ \partial \mu ^{2} }= - \frac{1}{v^{2}}\frac{ \partial v }{ \partial \mu } $$
TODO: Finish this section

---

From $(1)$ we get
$$1=\int \rho(\mathbf{q},\mathbf{p},N)\,dq\,dp =\frac{Z^{N}}{N!h^{3N}}e^{-\beta PV}\int e^{-\beta H}\,dq\,dp=Z^{N}e^{-\beta PV}Q_{N}$$
Also
$$\sum Z^{N}Q_{N}(V,T)=e^{\beta V???} $$
The [[specific heat]] is from the [[Maxwell relations]]:
$$C_{V}=\left( \frac{ \partial U }{ \partial T }  \right)_{V}$$
and [[entropy]] is[^1]
$$S=\int \frac{dQ}{T}=\int_{0}^{T}C_{V} \frac{dT}{T} $$
We define
$$W(N)\equiv Z^{N}Q_{N}=e^{\beta \mu N-\beta A(N,V,T)}$$
which is proportional to the [[probability]] that the system has $N$ particles.

---

We get yet another form for the variance of $N$:
$$\langle N^{2} \rangle -\langle N \rangle ^{2}=\frac{Vk_{B}T}{v^{3}\left( -\frac{ \partial P }{ \partial v }  \right)}$$
If we define a few parameters, this can be simplified. The [[thermal expansion coefficient]] is
$$\alpha=\frac{1}{V}\left( \frac{ \partial V }{ \partial T }  \right)_{P}$$
The [[compressibility]] is
$$K_{T}=- \frac{1}{V}\left( \frac{ \partial V }{ \partial P }  \right)_{T}$$
and the adiabatic compressibility is
$$\mathcal{K}_{T}=- \frac{1}{V}\left( \frac{ \partial V }{ \partial P }  \right)_{S}$$
So the variance can be written as
$$\langle N^{2} \rangle -\langle N \rangle ^{2}=k_{B}T \frac{1}{v\left( -\frac{ \partial P }{ \partial v }  \right)} \frac{V}{v^{2}}=k_{B}T\langle N \rangle \frac{\mathcal{K}_{T}}{v}\sim \langle N \rangle $$
which goes like $\langle N \rangle$ for large $N$. The variance of energy is
$$\langle H^{2} \rangle -\langle H \rangle ^{2}\propto T^{2}C_{V}\sim \langle N \rangle $$
which also goes like $\langle N \rangle$ for large $N$. This is precisely what happens with the canonical ensemble, so for large $N$, the two are equivalent. But since the canonical is itself equivalent to the microcanonical for large $N$, the grand canonical is also equivalent to the microcanonical.

The canonical ensemble has internal energy $U$ with fluctuations $\sqrt{ N }$. The grand canonical has number of particles $\langle N \rangle$ with fluctuations $\sqrt{ N }$.

[^1]: Note how, unlike the [[microcanonical ensemble]], entropy is derived last.