It's possible to express the constraints of [[energy]] conservation and entropy increase in the [[Laws of thermodynamics|second law of thermodynamics]] through [[Moltiplicatori di Lagrange|Lagrange multipliers]]. Consider [[Entropy (information theory)|Boltzmann entropy]] $S=-k_{B}\sum_{x}p(x)\log p(x)$. The [[internal energy]] $U$ is
$$U=\langle E \rangle =\sum_{x}E(x)p(x) $$
where $\sum p(x)=1$ for all [[Probability|probabilities]]. Here $x$ represents one possible [[stato|state]] of the system, while $E$ is actually the [[Hamiltonian]] of that state. The usage of $E$ instead of $H$ is because it's common in information theory to use $H$ as entropy and $E$ as the [[cost function]] instead of $S$ and $H$ as usual in physics. This is true for all [[Ensemble|ensembles]].

Let's define the constraint $\mathcal{L}$ as
$$\mathcal{L}=-k_{B}\sum_{x}p(x)\log p(x)+\lambda_{1}(1-??)$$
where $k_{B}$ is the [[Boltzmann constant]]. Its derivative is
$$\delta \mathcal{L}=0=\delta\left( -k_{B}\sum_{x}p(x)\log p(x) \right)+\delta\left( \lambda-\sum \lambda_{1}p(x) \right)+\delta\left( \lambda_{2}U-\sum_{x}\lambda_{2}p(x)E(x) \right)=$$
$$=-k_{B}\sum_{x} \frac{\partial p}{\partial p } \delta p(x)-\lambda_{1}\sum_{x}\delta p(x)-\lambda_{2}\sum_{x}\frac{ \partial pE }{ \partial p } E(x)=$$
$$=-k_{B}\sum_{x}(\log p(x)+1)\delta p(x)-\lambda_{1}\sum_{x}\delta p(x)-\lambda_{2}\sum_{x}E(x)\delta p(x)=$$
$$=\sum_{x}\delta p(x)[ -k_{B}\log p(x)-k_{B}-\lambda_{1}-\lambda_{2}E(x) ]$$
So
$$0=-k_{B}\log p(x)-k_{B}-\lambda_{1}-\lambda_{2}E(x)$$
Extracting $\log p(x)$ we get
$$\log p(x)=\frac{k_{B}+\lambda_{1}+\lambda_{2}E(x)}{-k_{B}}$$
and therefore
$$p(x)=e^{(-k_{B}+\lambda_{1}+\lambda_{2}E(x))/k_{B}}$$
Exploiting probability [[Normalizzazione|normalization]], we get
$$\sum_{x}p(x)=1=\sum_{x}e^{(-k_{B}-\lambda_{1})/k_{B}}e^{-\lambda_{2}E(x)/k_{B}}=e^{(-k_{B}-\lambda_{1})/k_{B}}Z$$
where $Z$ is the [[partition function]], as
$$Z\equiv\sum_{x}e^{-\lambda_{2}E(x)/k_{B}}$$
We can therefore write
$$p(x)=\frac{1}{Z}\sum_{x}e^{-\lambda_{2}E(x)/k_{B}}$$
Since we know the probabilities, we can put them in the definition of entropy:
$$\begin{align}
S&=-k_{B}\sum_{x}p_{x}\log p(x) \\
&=-k_{B}\sum_{x}p(x)\left[ - \frac{\lambda_{2}E(x)}{k_{B}}-\log Z \right] \\
&=\lambda_{2}\sum_{x}p(x)E(x)\ldots \\
&=\ldots \\
&=\lambda_{2}U+k_{B}\log Z
\end{align}$$

For now, we've only used theoretical definition. To add physics constraints in, we invoke the [[Laws of thermodynamics|first law of thermodynamics]]
$$dU=dQ-dW=TdS-PdV$$
and the [[Laws of thermodynamics|second law of thermodynamics]], for which
$$\frac{dS}{dU}=\boxed{\lambda_{2}=\frac{1}{T}}$$
where $T$ is the [[temperature]]. Therefore, entropy is
$$\boxed{S=\frac{U}{T}+k_{B}\log Z}$$
Meanwhile, $\lambda_{1}$ is hidden within the $Z$, which determines the normalization.