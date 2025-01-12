---
aliases:
  - ideal gas law
---
An **ideal gas** is an approximate model of the behavior of a gas that holds for low density gases. It is sparse and has weak internal interactions that limit [[information]] exchange. The dynamics are determined by the **ideal gas law**:
$$PV=Nk_{B}T=nRT=\frac{2}{3}U$$
where $P$ is the [[pressure]], $V$ is the volume occupied by the gas, $N$ is the number of [[particella|particles]] composing the gas, $k_{B}$ is the [[Boltzmann constant]], $T$ is the [[temperature]], $n$ is the number of [[mole|moles]], $R$ is the [[ideal gas constant]] and $U$ is the [[internal energy]][^1]. The first and second forms apply only to classical gases, whereas the third is also valid for quantum gases (if the particles have [[mass]]).

An ideal gas is a [[Physical system|system]] of free particles enclosed in a finite enclosure with rigid, perfectly elastic walls. The system [[Hamiltonian]] is
$$H=\sum_{i=1}^{N} \frac{\mathbf{p}^{2}_{i}}{2m}$$
### Classical thermodynamics
Many properties of the ideal gas were already derived with classical thermodynamics.
#### Heat capacity
The [[heat capacity]] by volume of a monatomic ideal gas is
$$C_{V}=\frac{3}{2}Nk_{B}$$
#### Entropy
The [[entropy]] of an ideal gas can calculated as a function of volume $V$ and temperature $T$ by explicitly integrating $dS=dQ/T$. Let's consider a [[stato|state]] $A$, which we approach from two different states: one using an constant-volume transformation (path 1), the other using a isothermal one (path 2).

Along path 1, $V$ is constant, so
$$\int \frac{dQ}{T}=C_{V}\int \frac{dT}{T}$$
and thus if we start the transformation at temperature $T_{0}$ we get
$$S(V,T)=S(V,T_{0})+C_{V}\int_{T_{0}}^{T} \frac{dT}{T}=S(V,T_{0})+C_{V}\ln \frac{T}{T_{0}}$$

Along path 2, $T$ is constant, so
$$dU=0$$
and thus, using the [[Laws of thermodynamics|first law of thermodynamics]] and the ideal gas law, we get
$$dQ=dW=PdV=Nk_{B}T \frac{dV}{V}$$
which gives us, starting from $V_{0}$,
$$S(V,T)=S(V_{0},T)+Nk_{B}\int_{V_{0}}^{V} \frac{dV}{V}=S(V_{0},T)+Nk_{B}\ln \frac{V}{V_{0}}$$

The entropy for the two paths must be equal, so comparing the two expressions for $S(V,T)$ we get (TODO: Figure out how this even works)
$$S(V,T_{0})=C_{0}+Nk_{B}\ln V$$
 where $C_{0}$ is an arbitrary constant. Absorbing $V_{0}$ into $C_{0}$ we can write
 $$S(V,T)=C_{0}+Nk_{B}\ln V+C_{V}\ln T$$
 This depends on the nature of the gas itself, because of $C_{V}$. For a monatomic ideal gas, we have
$$S(V,T)=C_{0}+Nk_{B}\ln(VT^{3/2})$$
### Pressure
The pressure of an ideal gas is the average force per unit area that it exerts on the wall of its container. By calculating the energy transferred from each particle collision on the walls per unit time, we can derive the pressure directly from particle mechanics.

Take the wall to be normal to the $x$ axis and assume the wall is perfectly reflecting. When a particle of velocity $v_{x}$ hits the wall, it transfers $2p_{x}=2mv_{x}$ momentum to the wall. The total force on the wall is given by this momentum transfer multiplied by the amount of particles hitting a unit area of the wall, i.e. the particle [[flux]].

The flux is the number of particles crossing a unit area per second. If the particles are moving over $x$, this is equal to a cylinder of unit cross-section and length $v_{x}\Delta t\equiv v_{x}$, since $\Delta t=1\text{ second}$. Thus, the flux is given by
$$\Phi=v_{x}f(\mathbf{p})d\mathbf{p}$$
where $f(\mathbf{p})$ is the [[Maxwell-Boltzmann distribution]] for momentum
$$f(\mathbf{p})=n\left( \frac{\beta}{2\pi m} \right)^{3/2}e^{-\beta \lvert \mathbf{p} \rvert ^{2}/2m}$$
which is weighted by the particle density $n=N/V$. The pressure is therefore
$$P=\int_{v_{x}>0}2mv_{x}\ v_{x}f(\mathbf{p})d\mathbf{p}=m\int_{v_{x}>0}v_{x}^{2}f(\mathbf{p})d\mathbf{p}$$
Since motion in an ideal gas is isotropic, we can make the substitution
$$v_{x}^{2}=\frac{1}{3}(v_{x}^{2}+v_{y}^{2}+v_{z}^{2})=\frac{1}{3}\lvert \mathbf{v} \rvert^{2}=\frac{1}{3} \frac{\lvert\mathbf{p}\rvert^{2}}{m^{2}} $$
and so
$$P=\frac{1}{3m}\int _{v_{x}} \lvert \mathbf{p} \rvert ^{2}f(\mathbf{p})d\mathbf{p}=\frac{2}{3} \frac{U}{V}$$
which is solved with a [[Gaussian integral]]. $U$ is the [[internal energy]].
### In the classical microcanonical ensemble
The entropy can also be calculated by modeling an ideal gas as a [[microcanonical ensemble]]. We use the entropy given by the sigma function $S=k_{B}\log \Sigma(E)$ where
$$\Sigma(E)=\frac{1}{h^{3N}}\int\limits_{H(\mathbf{q},\mathbf{p})<E}d^{3}q_{1}\ldots d^{3}q_{N}\,d^{3}p_{1}\ldots d^{3}p_{N}$$
and $h$ is a dimensionally appropriate constant, specifically $\text{impulse}\times\text{length}$, which gives $\text{energy}\times\text{seconds}$. We can develop this as
$$\Sigma(E)=\left( \frac{V}{h^{3}} \right)^{N}\int\limits_{H(\mathbf{q},\mathbf{p})<E}d^{3}p_{1}\ldots d^{3}p_{N}$$
Since the energy of a particle under no potential is $E=p^{2}/2m$, the momentum is $p=\sqrt{ 2mE }$. This momentum describes a $n$-[[palla|ball]] of radius $R=p=\sqrt{ 2mE }$ in the momentum-only [[phase space]], but the integral finds the volume of that ball in phase space (by finding the representative points contained therein), so we can rename the integral as a function $\Omega_{3N}(R)$ which finds the volume of a $3N$-dimensional ball of radius $R$:
$$\Sigma(R)=\left( \frac{V}{h^{3}} \right)^{N}\Omega_{3N}(R)$$
In general, $\Omega_{3N}$ is
$$\Omega_{3N}(R)=\int\limits_{x_{1}^{2}+x_{2}^{2}+\ldots+x_{n}^{2}<R^{2}}dx_{1}\ldots dx_{n}$$
(in our case, $x\equiv p$). We know both $V$ and $h$ ($h$ just needs to have the correct dimensions, so might as well be $h=1 \text{ Js}$ in this case), so in order to find $\Sigma$ and therefore $S$, we just need to solve $\Omega$ in $3N$ dimensions. Thankfully, $\Omega$ can be solved generally for any integer $N$ (see [[Volume of an n-ball]]), which gives
$$\Omega_{3N}=\frac{\pi^{3N/2}}{\Gamma\left( \frac{3N}{2}+1 \right)}R^{3N}$$
where $\Gamma$ is the [[Gamma function]]. Thus, we have
$$\Sigma(R)=\left( \frac{V}{h^{3}} \right)^{N} \underbrace{ \frac{\pi^{3N/2}}{\Gamma\left( \frac{3N}{2}+1 \right)} }_{ c_{n} }R^{3N}=\left( \frac{V}{h^{3}} \right)^{N}c_{3N} (2mE)^{3N/2}$$
and entropy
$$S=k_{B}\log \Sigma(R)$$
We can use the fact that $\Gamma(n+1)=n!$ and [[Stirling's approximation]] $\log n!=n\log n-n+O(\log n)$ to get [[Steps Entropy microcanonical ideal gas]].
### In the classical canonical ensemble
An ideal gas can also be describe by a [[canonical ensemble]]. The partition function is
$$\begin{align}
Q_{N}&=\int \frac{e^{-\beta(\mathbf{p}_{1}^{2}+\ldots+\mathbf{p}_{N}^{2})/2m}}{h^{3N}N!} \ d^{3N}q\ d^{3N}p \\ \\
&= \frac{1}{N!} \int d^{3N}q\int \frac{e^{-\beta(\mathbf{p}_{1}^{2}+\ldots+\mathbf{p}_{N}^{2})/2m}}{h^{3N}}d^{3N}p \\
&= \frac{V^{N}}{N!}\left( \int_{-\infty}^{\infty} \frac{e^{-\beta p^{2}/2m}}{h} \ dp  \right)^{3N}
\end{align} $$
Solving the [[Gaussian integral]] and using the [[Formula di de Broglie|de Broglie thermal wavelength]] $\lambda$, we write
$$Q_{N}=\frac{1}{N!}\left( \frac{V}{\lambda ^{3}} \right)^{N}$$
and its logarithm is
$$\ln Q_{N}=-\ln N!+N\ln \frac{V}{\lambda ^{3}}\simeq N-N\ln N+N\ln \frac{V}{\lambda ^{3}}=N(1-\ln n\lambda ^{3})$$
where we defined the particle density $n=N/V$. Now that we have the partition function, thermodynamics follows suit naturally. The Helmholtz free energy is
$$A=- \frac{1}{\beta}\ln Q_{N}\simeq- \frac{1}{\beta}N(1-\ln (n\lambda ^{3}))=k_{B}TN[\ln(n\lambda ^{3})-1]$$
and the entropy
$$\begin{align}
S&=-\left( \frac{ \partial A }{ \partial T }  \right)_{V} \\
&=-k_{B}N\frac{ \partial  }{ \partial T } [T(\ln(n\lambda ^{3})-1)] \\
&=-k_{B}N\left[ \ln(n\lambda ^{3})-1 + T\frac{ \partial  }{ \partial T } \ln(n\lambda ^{3}) \right] \\
&=-k_{B}N\left[ \ln(n\lambda ^{3})-1- T\frac{3}{2T} \right] \\
&=k_{B}N\left[ \frac{5}{2}-\ln(n\lambda ^{3}) \right]
\end{align}$$
which is the [[Sackur-Tetrode equation]], as expected.
### In the quantum microcanonical ensemble
It is possible to derive the behavior of an ideal gas using the [[quantum microcanonical ensemble]]. Consider a cube of side $L$ and volume $V=L^{3}$ filled with the ideal gas.
### In the quantum canonical ensemble
In the [[quantum canonical ensemble]], analytic calculation is actually not possible. The reason is that the quantum canonical partition function $Q_{N}$ cannot be solved. In fact, given the sets of [[Occupation number|occupation numbers]] $\{ n \}$ identified by some quantity (say, momentum $\mathbf{p}$), we have
$$Q_{N}(V,T)=\text{Tr}\hat{\rho}=\sum_{\{ n \},\sum_{p}n_{p}=N}e^{-\beta E(\{ n \})}$$
where the sum happens over all sets $\{ n \}$ where $\sum_{\mathbf{p}}n_{\mathbf{p}}=N$. The state energy is $E(\{ n \})=\sum_{\mathbf{p}}\varepsilon_{\mathbf{p}}n_{\mathbf{p}}$, where $\varepsilon_{\mathbf{p}}$ is the energy of a single particle of momentum $\mathbf{p}$, so $\varepsilon_{\mathbf{p}}=\lvert \mathbf{p} \rvert^{2}/2m$. This constraint makes it impossible to calculate the sum explicitly, along with all thermodynamic quantities.
### In the quantum grand canonical ensemble
The [[quantum grand canonical ensemble]] works just fine however. The quantum grand partition function is
$$\mathcal{Z}(z,V,T)=\sum_{N=0}^{\infty} z^{N}Q_{N}(V,T)=\sum_{N=0}^{\infty} \sum_{\{ n \},\sum_{p}n_{p}=N}z^{N}e^{-\beta E(\{ n \})}$$
where the inner sum satisfies $\sum_{\mathbf{p}}n_{\mathbf{p}}=N$ (see quantum canonical ensemble above). The important part in this equation is that the two sums can be merged, removing the inner sum's constraint:
$$\sum_{N=0}^{\infty}\ \sum_{\{ n \},\sum_{p}n_{p}=N}\equiv \sum_{\{ n \}}$$
This is because constraining to a specific $N$ no longer matters when you are summing over all possible $N$'s, leaving us with the same sum as the canonical ensemble, but over every possible set, not just ones whose total is $N$. As such, representing the sums as separate or single is just a matter of preference over how you group the terms. Thus
$$\mathcal{Z}(z,V,T)=\sum_{\{ n \}}z^{N}e^{-\beta E(\{ n \})}=\ldots$$
with no constraint. We can use the property $e^{\sum n}=\prod_{n}e^{n}$ to rewrite both terms, since both $N$ and $E(\{ n \})$ are sums:
$$\begin{align}
\ldots&=\sum_{\{ n \}}\prod_{\mathbf{p}}z^{n_{\mathbf{p}}}\prod_{\mathbf{p}}e^{-\beta \varepsilon_{\mathbf{p}}n_{\mathbf{p}}} \\
&=\sum_{\{ n \}}\prod_{\mathbf{p}}(ze^{-\beta \varepsilon_{\mathbf{p}}})^{n_{\mathbf{p}}} \\
&=\sum_{\{ n \}}(ze^{-\beta \varepsilon_{0}})^{n_{0}}(ze^{-\beta \varepsilon_{1}})^{n_{1}}\ldots \\
&=\sum_{n_{0}=0}^{1\text{ or }\infty} (ze^{-\beta \varepsilon_{0}})^{n_{0}}\sum_{n_{1}=0}^{1\text{ or }\infty} (ze^{-\beta \varepsilon_{1}})^{n_{1}}\ldots \\
&=\prod_{\mathbf{p}}\sum_{n_{\mathbf{p}}=0}^{1\text{ or }\infty} (ze^{-\beta \varepsilon_{\mathbf{p}}})^{n_{\mathbf{p}}}
\end{align}$$
where we momentarily expanded the product by labeling each momentum state with a number. The sum now has two possibilities, depending on whether we are dealing with fermions or bosons:
$$\boxed{\mathcal{Z}(z,V,T)=\left\{\begin{align}
\prod_{\mathbf{p}} (1+ze^{-\beta \varepsilon_{p}})&\quad\text{(Fermions)} \\
\prod_{\mathbf{p}} \frac{1}{1-ze^{-\beta \varepsilon_{p}}}&\quad\text{(Bosons)}
\end{align}\right.}$$
where the first is directly obtained and the second is from the [[Serie geometrica|geometric series]]. Now that we have the grand partition function, we can derive everything else.
#### Particle number
The average particle number is
$$\langle N \rangle =z\frac{ \partial  }{ \partial z } \mathcal{Z}(z,V,T)=\left\{\begin{align}
\left( \prod_{\mathbf{p}}(1+ze^{-\beta \varepsilon_{\mathbf{p}}}) \right)\sum_{\mathbf{p}} \frac{1}{z^{-1}e^{\beta \varepsilon_{\mathbf{p}}}+1} &\quad \text{(Fermions)} \\
\left( \prod_{\mathbf{p}} \frac{1}{1-ze^{-\beta \varepsilon_{\mathbf{p}}}} \right)\sum_{\mathbf{p}} \frac{1}{z^{-1}e^{\beta \varepsilon_{\mathbf{p}}}-1} & \quad\text{(Bosons)}
\end{align}\right\}=\mathcal{Z}\sum_{\mathbf{p}}\langle n_{\mathbf{p}} \rangle $$
found using the generalized [[product rule]] and $e^{\sum n}=\prod_{n}e^{n}$.
#### Equation of state
The [[equation of state]] can be expressed with the grand [[partition function]] $\mathcal{Z}$ as
$$\frac{PV}{k_{B}T}=\ln \mathcal{Z}(z,V,T)=\pm\sum_{\mathbf{p}} \ln(1\pm ze^{-\beta \varepsilon_{\mathbf{p}}})$$
where $+$ is for fermions, $-$ is for bosons. Calculating the actual value is, unfortunately, not possible analytically. However, we can check the [[thermodynamic limit]] and find an approximate quantum solution.
##### Fermions
We start from
$$\frac{PV}{k_{B}T}=\ln \mathcal{Z}=\sum_{\mathbf{p}}\ln(1+ze^{-\beta \varepsilon_{\mathbf{p}}})$$
In the thermodynamic limit, we move to density (divide by $V$) and get
$$\begin{align}
\frac{P}{k_{B}T}&=\frac{1}{V}\ln \mathcal{Z}\\
&\to \frac{1}{h^{3}}\int \ln(1+ze^{-\beta p^{2}/2m})d^{3}p \\
&=\frac{4\pi}{h^{3}}\int_{0}^{\infty}p^{2}\ln(1+ze^{-\beta p^{2}/2m})\ dp \\
&=\ldots
\end{align}$$
where we used [[spherical coordinates]] (see [[Ideal gas#Determining the parameters]] for more info). We can't solve this integral directly, but we can introduce a class of functions $f_{k}(z)$ called [[Fermi and Bose functions|Fermi functions]]. Expanding $\ln(1+x)$ in [[Serie di Taylor|Taylor series]] we find
$$\begin{align}
\ldots&=\frac{4\pi}{h^{3}}\int_{0}^{\infty}p^{2}\sum_{j=1}^{\infty} \frac{(-1)^{j+1}z^{j}e^{-j\beta\varepsilon_{p}}}{j} \\
&=\frac{4\pi}{h^{3}}\sum_{j=1}^{\infty} \frac{(-1)^{j+1}z^{j}}{j}\int_{0}^{\infty}p^{2}e^{-j\beta p^{2}/2m} \\
&=\frac{4\pi}{h^{3}}\sum_{j=1}^{\infty} \frac{(-1)^{j+1}z^{j}}{j} \frac{\sqrt{ \pi }}{4(j\beta/2m)^{3/2}} \\
&=\left( \frac{2\pi m}{\beta h^{2}} \right)^{3/2} \sum_{j=1}^{\infty} \frac{(-1)^{j+1}z^{j}}{j^{5/2}}  \\
&=\frac{1}{\lambda ^{3}}f_{5/2}(z)
\end{align}$$
where we used the [[Formula di de Broglie|de Broglie thermal wavelength]]. This gives us the equation of state of a fermion ideal gas
$$\boxed{\frac{P\lambda ^{3}}{k_{B}T}=f_{5/2}(z)}$$
This equation substitutes (and extends) the well-known classical $PV=Nk_{B}T$. Notice that volume does not make an appearance here, instead substituted by the cube of the thermal wavelength. Clearly then, a quantum gas depends not on the size of its enclosure (at least, not directly), but rather on the wave properties of its components.

From the previous steps we can retroactively state
$$\int_{0}^{\infty}p^{2}\ln(1+ze^{-\beta \varepsilon_{p}})dp=\frac{\sqrt{ \pi }}{4} \left( \frac{2m}{\beta} \right)^{3/2} f_{5/2}(z)$$

The particle density is
$$\begin{align}
n&=\frac{1}{V}\sum_{\mathbf{p}}\langle n_{\mathbf{p}} \rangle  \\
&\to \frac{1}{h^{3}}\int \frac{1}{z^{-1}e^{\beta \varepsilon_{\mathbf{p}}}+ 1}d^{3}p \\
&=\frac{4\pi}{h^{3}}\int_{0}^{\infty} \frac{p^{2}}{z^{-1}e^{\beta \varepsilon_{p}}+ 1}dp \\
\text{(pull }z^{-1}e^{\beta \varepsilon_{p}}\text{ out)}&=\frac{4\pi}{h^{3}}\int_{0}^{\infty} \frac{ze^{-\beta \varepsilon_{p}}p^{2}}{ze^{-\beta \varepsilon_{p}}+1}dp \\
&=\ldots
\end{align}$$
We ideally want to reuse the previous integral. However, the integral does not look the same at all. The trick is to reverse engineer a logarithm into existence by remembering that the derivative of a logarithm is a fraction of the argument. Conveniently, the denominator here is just the argument we need:
$$\frac{ \partial  }{ \partial z } \ln(1+ze^{-\beta \varepsilon_{p}})=\frac{1}{ze^{-\beta \varepsilon_{p}}+1}e^{-\beta \varepsilon_{p}}\quad\rightarrow \quad \frac{1}{ze^{-\beta \varepsilon_{p}}+1}=e^{\beta \varepsilon_{p}}\frac{ \partial  }{ \partial z } \ln(1+ze^{-\beta \varepsilon_{p}})$$
Substituting this in the integral gives us
$$\begin{align}
\ldots&=\frac{4\pi}{h^{3}}z\int_{0}^{\infty} p^{2}e^{-\beta \varepsilon_{p}}e^{\beta \varepsilon_{p}}\frac{ \partial  }{ \partial z } \ln(1+ze^{-\beta \varepsilon_{p}}) dp\\
&=\frac{4\pi}{h^{3}}z\frac{ \partial  }{ \partial z } \int_{0}^{\infty}p^{2}\ln(1+ze^{-\beta \varepsilon_{p}})dp \\
&=\frac{4\pi}{h^{3}} \frac{\sqrt{ \pi }}{4}\left( \frac{2m}{\beta} \right)^{3/2}z\frac{ \partial  }{ \partial z } f_{5/2}(z) \\
&=\frac{1}{\lambda ^{3}}z\frac{ \partial  }{ \partial z } f_{5/2}(z)
\end{align}$$
This is pleasantly compact, but the derivative is an eyesore. Thankfully, now that we know that we are working with $f_{5/2}$, we can compute its derivative:
$$\begin{align}
\frac{ \partial  }{ \partial z } f_{5/2}(z)&=\frac{ \partial  }{ \partial z } \sum_{j=1}^{\infty} \frac{(-1)^{j+1}z^{j}}{j^{5/2}} \\
&=\sum_{j=1}^{\infty} \frac{(-1)^{j+1}}{j^{5/2}}\frac{ \partial  }{ \partial z } z^{j} \\
&=\sum_{j=1}^{\infty} \frac{(-1)^{j+1}}{j^{5/2}}jz^{j-1} \\
&=\frac{1}{z}\sum_{j=1}^{\infty} \frac{(-1)^{j+1}z^{j}}{j^{3/2}}=\frac{1}{z}f_{3/2}(z)
\end{align}$$
This result is actually a specific case of a more general recurrence relation among Fermi (and Bose) functions. It inverts to $f_{3/2}(z)=z\frac{ \partial  }{ \partial z }f_{5/2}(z)$, which very nicely exists in our previous result as-is. As such, our final formula is
$$\boxed{n=\frac{1}{\lambda ^{3}}f_{3/2}(z)}$$
##### Bosons
We start from
$$\frac{PV}{k_{B}T}=\ln \mathcal{Z}=-\sum_{\mathbf{p}}\ln(1-ze^{-\beta \varepsilon_{\mathbf{p}}})$$
The process is the same as with fermions, except we use [[Fermi and Bose functions|Bose functions]] $g_{k}$ instead. We can find
$$\frac{P}{k_{B}T}=\frac{4\pi}{h^{3}}\int_{0}^{\infty}p^{2}\ln(1-ze^{-\beta \varepsilon_{p}})\ dp$$
which resolves to
$$\boxed{\frac{P}{k_{B}T}=\frac{1}{\lambda ^{3}}g_{5/2}(z)}$$
Similarly, the particle density is
$$n=\frac{4\pi}{h^{3}}\int_{0}^{\infty} p^{2} \frac{1}{z^{-1}e^{\beta \varepsilon_{p}}}dp$$
which yields
$$\boxed{n=\frac{1}{\lambda ^{3}}g_{3/2}(z)}$$

A more precise result can be reached by taking [[Bose-Einstein condensation]] into consideration. Condensation occurs at minimal temperatures, which in turn implies minimal particle energies, $\varepsilon_{p}\to 0$. In this state, the occupation number blows up and causes a [[Singolarità isolata|singularity]], making it technically impossible to calculate the integral at the lower bound $p=0$. Because of this, we can extract the term $p=\varepsilon_{p}=0$ from the equation of state sum *before* going to integral notation, which leaves us with
$$\boxed{\frac{P}{k_{B}T}=\frac{1}{\lambda ^{3}}g_{5/2}(z)- \frac{1}{V}\ln(1-z)}$$
(a single point is a [[Insiemi a misura trascurabile|negligible set]] in a 1D integral, so it still evaluates to $g_{5/2}(z)$). Similarly, the particle density is
$$\boxed{n=\frac{1}{\lambda ^{3}}g_{3/2}(z)+ \frac{1}{V} \frac{z}{1-z}}$$
In fact, we can use this to describe how the occupation number blows up:
$$\langle n_{p=0} \rangle =nV=\frac{z}{1-z}$$
$z$ blows up at low temperatures, and this does too. In fact, in the condensed phase, $z$ is locked at $1$.
#### Internal energy
The grand canonical [[internal energy]] $U$ is given by
$$U(z,V,T)=-\left( \frac{ \partial  }{ \partial \beta } \ln \mathcal{Z} \right)_{P,V}=-\frac{ \partial  }{ \partial \beta }  \frac{PV}{k_{B}T}$$
In the thermodynamic limit, we can use the equations of state above.
##### Fermions
For fermions we have
$$\frac{U}{V}=-\frac{ \partial  }{ \partial \beta } \frac{P}{k_{B}T}=-\frac{ \partial  }{ \partial \beta } \frac{1}{\lambda ^{3}}f_{5/2}(z)=-\left( \frac{ \partial  }{ \partial \beta } \frac{1}{\lambda ^{3}} \right)f_{5/2}(z)- \frac{1}{\lambda ^{3}}\left( \frac{ \partial  }{ \partial \beta } f_{5/2}(z) \right)$$
Computing the derivatives separately
$$\frac{ \partial  }{ \partial \beta } \frac{1}{\lambda ^{3}}=-\frac{1}{\lambda ^{3}} \frac{3}{2\beta},\qquad \frac{ \partial  }{ \partial \beta } f_{5/2}(z)=\sum_{j=1}^{\infty} \frac{(-1)^{j+1}}{j^{5/2}}\frac{ \partial  }{ \partial \beta } z^{j}=\mu\sum_{j=1}^{\infty} \frac{(-1)^{j+1}}{j^{3/2}}z^{j}=\mu f_{3/2}(z)$$
and so
$$\frac{U}{V}=\frac{3}{2\beta} \frac{f_{5/2}(z)}{\lambda ^{3}}-\mu \frac{f_{3/2}(z)}{\lambda ^{3}}=\frac{3}{2\beta}\beta P-\mu n$$
If we move $V$ over to the right side, we get
$$\boxed{U=\frac{3}{2}PV-\mu N}$$
This is identical to the classical result, which is what we want.
##### Bosons
Since the equation of state of bosons is identical to that of fermions, but with Bose functions instead of Fermi functions, the internal energy is itself identical, derived in the same way as above. It should be noted that the additional term due to condensation in the equation of state does not make a difference.

[^1]: The form $PV=nRT$ exists because, besides being convenient in a laboratory setting, thermodynamics was historically developed at a time where the existence of the [[atomo|atom]] had yet to be proven and with it, the [[Particella|particle]] division of matter. In fact, classical thermodynamics as a whole does not strictly require the existence of particles like atoms.