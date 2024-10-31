The **grand canonical ensemble** is an [[ensemble]] where both [[energy]] and number of [[Particella|particles]] can fluctuate. The number of particles is determined by environmental conditions external to the ensemble.
### Partition function
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
$$\rho(\mathbf{q},\mathbf{p},N)=\frac{Z^{N}}{h^{3N}N!}e^{-\beta PV-\beta H(\mathbf{q},\mathbf{p},N)}$$
This is dependent on three variables: [[temperature]] $T$ (hidden in $\beta$), pressure $P$ and chemical potential $\mu$ (hidden in $Z$). We can finally write the **grand canonical partition function**:
$$\boxed{\mathcal{Z}(Z,V,T)\equiv \sum_{N=0}^{\infty} Z^{N}Q_{N}(V,T)}$$
which is an extended form of the canonical partition function.
### Properties
Since $N$ varies, we can express the [[mean]] number of particles as the [[ensemble average]]
$$\langle N \rangle =\frac{\sum_{N=0}^{\infty}NZ^{N}Q_{N}(V,T)}{\sum_{N=0}^{\infty} Z^{N}Q_{N}(V,T)}$$
But since
$$\frac{ \partial  }{ \partial Z } \log \mathcal{Z}=\frac{1}{\mathcal{Z}}\sum_{N=0}^{\infty} NZ^{N-1}Q_{N}(V,T)\tag{2}$$
we have
$$\boxed{\langle N \rangle =Z\frac{ \partial  }{ \partial Z } \log \mathcal{Z}(Z,V,T)}$$

From $(1)$ we get
$$1=\int \rho(\mathbf{q},\mathbf{p},N)\,dq\,dp =\frac{Z^{N}}{N!h^{3N}}e^{-\beta PV}\int e^{-\beta H}\,dq\,dp=Z^{N}e^{-\beta PV}Q_{N}$$
Also
$$\sum Z^{N}Q_{N}(V,T)=e^{\beta V???} $$
The [[internal energy]] is
$$U=\langle H \rangle =-\frac{ \partial  }{ \partial \beta } \log \mathcal{Z}(Z,V,T)$$
The [[specific heat]] is from the [[Maxwell relations]]:
$$C_{V}=\left( \frac{ \partial U }{ \partial T }  \right)_{V}$$
and [[entropy]] is[^1]
$$S=\int \frac{dQ}{T}=\int_{0}^{T}C_{V} \frac{dT}{T} $$
We define
$$W(N)\equiv Z^{N}Q_{N}=e^{\beta \mu N-\beta A(N,V,T)}$$
which is proportional to the [[probability]] that the system has $N$ particles.
#### Equations of state
We have
$$\beta \mu \langle N \rangle -\beta A(\langle N \rangle ,V,T)=\log Z^{\langle N \rangle }+\log Q_{\langle N \rangle }(V,T)$$
$$-\beta A(\langle N \rangle ,V,T)=-\beta \mu \langle N \rangle +\log Z^{\langle N \rangle }+\log Q_{N}$$
$$A(\langle N \rangle ,V,T)=\mu \langle N \rangle -k_{B}T\log Z^{\langle N \rangle }Q_{\langle N \rangle }$$
Since $\log \mathcal{Z}\simeq Z^{\langle N \rangle}Q_{\langle N \rangle}$ we have
$$\boxed{A(\langle N \rangle ,V,T)=k_{B}T\langle N \rangle \log Z-k_{B}T\log \mathcal{Z}(Z,V,T)}$$
which is the [[Helmholtz free energy]] of the ensemble. Invoking the [[Laws of thermodynamics|first law of thermodynamics]] and the definition of $A$ we have
$$A=U-TS,\qquad dA=dU-d(TS)=dQ-dW-TdS-SdT=-PdV-SdT$$
If the number of particles increases, the free energy also increases, so
$$dA=-PdV-SdT+\mu dN$$
The internal energy does something similar
$$dU=dQ-dW+\mu dN=TdS-PdV+\mu dV$$
Same for [[Gibbs free energy]] $G=A+PV$:
$$dG=dA+d(PV)=-PdV+\mu dV+PdV-VdP-SdT=VdP-SdT+\mu dN$$

The chemical potential is the [[Moltiplicatori di Lagrange|Lagrange multiplier]] that governs the number of particles.
### Equivalence with canonical ensemble
Consider the [[variance]] of the particle number:
$$\langle N^{2} \rangle -\langle N \rangle ^{2}=Z\frac{ \partial  }{ \partial Z } Z \frac{ \partial  }{ \partial Z } \log \mathcal{Z}(Z,V,T)$$
We have
$$\frac{ \partial  }{ \partial Z } Z\frac{ \partial  }{ \partial Z } \mathcal{Z}=\frac{ \partial  }{ \partial Z } \log \mathcal{Z}+Z\frac{ \partial ^{2} }{ \partial Z^{2} } \log \mathcal{Z}=\ldots$$
and using $(2)$
$$\begin{align}
\ldots&=\frac{ \partial  }{ \partial Z } \log \mathcal{ Z}+Z\left(  \frac{\sum_{N=0}^{\infty}N(N-1)Z^{N-1}Q_{N}}{\sum_{N=0}^{\infty} Z^{N}Q_{N}}  - \frac{\left( \sum_{N=0}^{\infty} NZ^{N-1}Q_{N} \right)^{2}}{\left( \sum_{N=0}^{\infty} Z^{N}Q_{N} \right)^{2}}\right) \\
&=\frac{ \partial  }{ \partial Z } \log \mathcal{Z}+Z\left( \frac{\sum_{N=0}^{\infty}N(N-1)Z^{N-1}Q_{N}}{\sum_{N=0}^{\infty} Z^{N}Q_{N}} - \frac{1}{Z^{2}}\langle N \rangle ^{2} \right) \\
&=\cancel{ \frac{\left\langle  N  \right\rangle}{Z} }+ \frac{\langle N^{2} \rangle }{Z}- \cancel{ \frac{\langle N \rangle }{Z} }- \frac{\langle N \rangle^{2} }{Z} \\
&=\frac{1}{Z}(\langle N^{2} \rangle -\langle N \rangle ^{2})=\frac{\text{var}(N)}{Z}
\end{align}$$
Which proves the previous formula. We also have
$$\frac{ \partial  }{ \partial Z } =\frac{ \partial \mu }{ \partial Z } \frac{ \partial  }{ \partial \mu } =\frac{1}{\beta Z}\frac{ \partial  }{ \partial \mu } $$
and so
$$\frac{ \partial P }{ \partial Z } =\frac{k_{B}T}{V} \frac{1}{Z} \frac{ \partial \mathcal{Z} }{ \partial Z } =\frac{k_{B}T}{VZ}\log \mathcal{Z}$$
We also somehow get
$$\frac{PV}{k_{B}T}=\log \mathcal{Z}$$
So we can find a second, more useful form for the variance of $N$:
$$\langle N^{2} \rangle -\langle  N \rangle ^{2}=k_{B}TV \frac{ \partial ^{2}P }{ \partial \mu ^{2} } $$
Also idk what this is
$$A(N,V,T)=Na(v)$$
where $v=V/N$ is the "volume density".
$$\mu=\frac{ \partial A }{ \partial N } =a+N \frac{ \partial a }{ \partial N } =a-v\frac{ \partial a }{ \partial v } $$
$$P=-\frac{ \partial A }{ \partial v } =-\frac{ \partial v }{ \partial V } \frac{ \partial  }{ \partial v } Na$$
...

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