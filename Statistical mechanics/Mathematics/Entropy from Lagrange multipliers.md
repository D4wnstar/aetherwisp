The [[Laws of thermodynamics|second law of thermodynamics]] can be described by using the [[Moltiplicatori di Lagrange|Lagrange multipliers]] method to maximize [[entropy]].

Consider an [[ensemble]] with [[Entropy (information theory)|information-theoretical entropy]] $S=-k_{B}\sum_{x}p(x)\log p(x)$, where $p(x)$ is the [[probability]] that the ensemble is in [[Stato|state]] $x$. As usual, $\sum_{x}p(x)=1$ Its [[internal energy]] is $U=\langle E \rangle =\sum_{x}E(x)p(x)$[^1]. The constraint functions are
$$g_{1}(x)=1-\sum_{x}p(x)$$
which determines the completeness of probabilities and
$$g_{2}(x)=U-\sum_{x}E(x)p(x)$$
which determines the internal energy.

The [[Lagrangian]] $\mathcal{L}$ for these constraints is
$$\begin{align}
\mathcal{L}(x) &= S(x) +\lambda_{1}g_{1}(x) +\lambda_{2}g_{2}(x) \\
&=-k_{B}\sum_{x}p(x)\log p(x)+\lambda_{1}\left( 1-\sum_{x}p(x) \right)+\lambda_{2}\left( U-\sum_{x}p(x)E(x) \right)
\end{align}$$
where $k_{B}$ is the [[Boltzmann constant]]. The Lagrange multiplier theorem tells us that if some value $\bar{x}$ is a maximum of $S$, then there exist specific values of $\lambda_{1}$ and $\lambda_{2}$ such that $\bar{x}$ is a [[Punto critico|stationary point]] for $\mathcal{L}$:
$$\text{If }S(\bar{x})\text{ is a maximum}\quad\Rightarrow \quad \nabla \mathcal{L}(\bar{x};\lambda_{1},\lambda_{2})=0$$
In our case, $\mathcal{L}$ is univariate, so the [[gradient]] is just the derivative in $p$:
$$\begin{align}
\frac{d\mathcal{L}}{d p}&=0 \\
&=\frac{d}{dp}\left( -k_{B}\sum_{x}p(x)\log p(x) \right)+ \lambda_{1}\frac{d}{dp}\left(1 -\sum p(x) \right)+ \lambda_{2}\frac{d}{dp}\left( U-\sum_{x}p(x)E(x) \right) \\
&=-k_{B}\sum_{x} \frac{d }{d p }(p\log p)-\lambda_{1}\sum_{x} \frac{d}{dp} p-\lambda_{2}\sum_{x}\frac{ d }{ dp } pE \\
&=-k_{B}\sum_{x}(\log p+1)-\lambda_{1}\sum_{x}1-\lambda_{2}\sum_{x}E \\
&=-\sum_{x}[k_{B}\log p(x)+k_{B}+\lambda_{1}+\lambda_{2}E(x) ]
\end{align}$$
Each term in the sum must individually be zero because they are all independent from each other:
$$0=k_{B}\log p(x)+k_{B}+\lambda_{1}+\lambda_{2}E(x)$$
Extracting $\log p(x)$ we get
$$\log p(x)=\frac{k_{B}+\lambda_{1}+\lambda_{2}E(x)}{-k_{B}}= \frac{-k_{B}-\lambda_{1}-\lambda_{2}E(x)}{k_{B}}$$
Therefore
$$p(x)=e^{(-k_{B}-\lambda_{1}-\lambda_{2}E(x))/k_{B}}$$
This equation must satisfy probability [[Normalizzazione|normalization]]:
$$\sum_{x}p(x)=1=\sum_{x}e^{(-k_{B}-\lambda_{1})/k_{B}}e^{-\lambda_{2}E(x)/k_{B}}=e^{(-k_{B}-\lambda_{1})/k_{B}}Z$$
where we introduced the [[partition function]] $Z$
$$Z\equiv\sum_{x}e^{-\lambda_{2}E(x)/k_{B}}$$
We can therefore write
$$p(x)=\frac{1}{Z} e^{-\lambda_{2}E(x)/k_{B}}$$
Note how the probability depends only on the second multiplier. Now that we know the probabilities, we can calculate entropy directly
$$\begin{align}
S&=-k_{B}\sum_{x}p(x)\log p(x) \\
&=-k_{B}\sum_{x}p(x)\left[ -\log Z- \frac{\lambda_{2}E(x)}{k_{B}} \right] \\
&=k_{B}\log Z\underbrace{ \sum_{x}p(x) }_{ 1 }+\lambda_{2}\underbrace{ \sum_{x}p(x)E(x) }_{ U } \\
&=k_{B}\log Z+\lambda_{2}U
\end{align}$$
We want to determine what $\lambda_{2}$ is. To do this, we can see that
$$\frac{ \partial S }{ \partial U } =\lambda_{2}$$
and using the [[Maxwell relations|Maxwell relation]]
$$T=\frac{ \partial U }{ \partial S } \quad\to \quad \frac{1}{T}=\frac{ \partial S }{ \partial U } $$
we can state
$$\boxed{\lambda_{2}=\frac{1}{T}}$$
where $T$ is the [[temperature]]. Therefore, entropy is
$$\boxed{S=\frac{U}{T}+k_{B}\log Z}$$

[^1]: $E$ is actually the [[Hamiltonian]]. The usage of $E$ instead of $H$ is due to $H$ being used for entropy in information theory, whereas $E$ is used for the [[cost function]]. Since this is an information theory problem, information theory conventions are favored.