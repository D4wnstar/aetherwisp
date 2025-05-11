---
wiki-publish: true
aliases:
  - Shannon entropy
  - information-theoretical entropy
  - joint entropy
  - Boltzmann entropy
---
In information theory, the **entropy** $H_{X}$ or $H(X)$ of a discrete [[random variable]] $X$ defined in the [[sample space]] $\mathcal{X}$ and following some [[probability distribution]] described by the [[probability mass function]] $p(x)$, is
$$H_{X}=-\sum_{x \in \mathcal{X}}p(x)\log_{2}p(x) $$
It is often called **Shannon entropy** due to it being originally introduced by Claude Shannon. If the [[probability]] is encoded in a [[Matrice di densità|density matrix]] $\hat{\rho}$, we can alternatively write
$$H=-\text{Tr}(\hat{\rho}\log_{2} \hat{\rho})$$
using the [[Traccia|trace]].

Strictly speaking, the base of the logarithm is arbitrary and may be any real number. Base two is the most common choice as it encodes the idea of "true or false" outcomes and is measured in **bits**. In physics, however, base $e$ (i.e. $\ln$) is the more common choice as it spontaneously arises in nature. Entropy in base $e$ is measured in **nats**.
### Interpretation
Shannon entropy can be described as a measure of the uncertainty of $X$. $H$ can be seen as  a sort of "missing information" or as a measure of "surprisingness" : the greater the entropy, the less information I have about $X$ a priori and the more unexpected the result is going to be. For instance, if $X$ only has one possible value, entropy is zero as there is no uncertainty; I already know everything that there is to know about $X$.
### Joint entropy
If $X$ and $Y$ are two random variables in sample spaces $\mathcal{X}$ and $\mathcal{Y}$, **joint entropy** is defined by just changing the normal distribution function to a [[joint distribution function]]:
$$H_{X,Y}=-\sum_{x \in \mathcal{X}} \sum_{y\in \mathcal{Y}}p_{X,Y}(x,y)\log p_{X,Y}(x,y)$$
If $X$ and $Y$ are [[independent variables]], it simplifies to
$$H_{X,Y}=-\sum_{x \in \mathcal{X}}\sum _{y \in \mathcal{Y}}p_{X,Y}(x,y)[\log p_{X}(x)+\log p_{Y}(y)]=H_{X}+H_{Y} $$
### Properties
- It is non-negative: $H_{X}\geq 0$. It is zero only if $X$ is certain (i.e. it only has one possible outcome).
- If $X$ has more than one possible outcome, then $H_{X}$ is maximized when all those outcomes are equiprobable.
- Joint entropy is generally less than the sum of the single entropies: $H_{X,Y}\leq H_{X}+H_{Y}$. It is equal only if $X$ and $Y$ are independent.
- Entropy is additive across non-interacting [[Physical system|systems]] (*not* across variables; see previous property): $H=H_{1}+H_{2}$. The entropy of a system is equal to the sum of entropies of disjoint subsystems (keyword being disjoint: if they are interacting, this is not true: $H\geq H_{1}+H_{2}$).
### Boltzmann's entropy
In the specific case that all outcomes are equally likely, $p(x)$ is a constant. If there are $W$ possible outcomes, we have $p=1/W$, in which case the entropy reduces to
$$H=\log W$$
This chiefly occurs in statistical mechanics under the [[equal a priori probability hypothesis]], where $W$ is interpreted as the number of [[stato|microstates]] a [[physical system]] can be found in. Turning it into physical [[entropy]] through the [[Boltzmann constant]], we get Boltzmann's formula for entropy:
$$\boxed{S=k_{B}\log W}$$
#### Second law of thermodynamics
This particular case has a very useful property that's true for a system with many particles, say $N\sim 10^{23}$ and defined energy $E_{\text{total}}$ (a [[microcanonical ensemble]]). Split the system in two non-interacting halves (that still exchange energy, somehow) with respective energies $E_{1}$ and $E_{2}$ ($E_{\text{total}}=E_{1}+E_{2}$) and call $W=\Gamma(E_{i})$ the function that counts all the states at energy $E_{i}$[^1]. $\Gamma_{1}(E_{i})$ and $\Gamma_{2}(E_{i})$ do the same, but for the two subsystems. We therefore have[^2]
$$\Gamma(E_\text{total})=\sum_{i}\Gamma_{1}(E_{i})\Gamma_{2}(E_\text{total}-E_{i})=\sum_{i}\exp\left( \frac{S_{1}(E_{i})}{k_{B}}+ \frac{S_{2}(E_\text{total}-E_{i})}{k_{B}} \right)$$
Now, since the state count goes like $\Gamma\sim e^{N}$ and the entropy goes like $S\sim N$, the sum above iterates over terms that go like $\sim e^{N}$ (remember that $N$ is itself exponentially large, $\sim 10^{23}$). Now, say that there is even a single term for which the exponent is twice as large as any other term (so the entropy is twice as large). That means it goes like $\sim e^{2N}=e^{N}e^{N}$. But that means that this terms is $\sim e^{N}$ times larger than any other terms, i.e. so massively  large every other term becomes vanishingly small in comparison. As such, this entire sum can be collapsed to just the term with maximum entropy (of energy $E_\text{max}$), which is found in exponentially more microstates than any other[^3]:
$$\Gamma(E_\text{total})\simeq \exp\left( \frac{S_{1}(E_{\text{max}})}{k_{B}} + \frac{S_{2}(E_\text{total}-E_\text{max})}{k_{B}} \right)$$
and so
$$S(E_\text{total})\simeq S_{1}(E_\text{max})+S_{2}(E_\text{total}-E_\text{max})\geq S_{1}(E_{1})+S_{2}(E_{2})$$
In our case, $E_\text{max}$ is found when
$$\frac{ \partial S_{1}(E_\text{max}) }{ \partial E }- \frac{ \partial S_{2}(E_\text{total}-E_\text{max}) }{ \partial E } = 0\tag{1}$$
In essence, when the two systems make contact, they will near certainly end up with fixed energies $E_\text{max}$ and $E_\text{total}-E_\text{max}$. It’s worth stressing that there is no a priori reason why this is the case. But the large number of particles involved means that system 1 is overwhelmingly likely to be found with energy $E_\text{max}$ which maximizes the number of states $\Gamma$ of the combined system. Conversely, once in this bigger set of states, it is highly unlikely that the system will ever be found back in a state with energy $E_{1}$ or, indeed, any other energy other than $E_{\text{max}}$. This is precisely the [[Laws of thermodynamics|second law of thermodynamics]] and as we can see, it is actually a *probabilistic* law, not a *deterministic* one. When it is said that an isolated system's entropy never increases, it would in fact be more correct to state that an isolated system's entropy *almost surely* never increases, and it is wrong to state that the chance does not exist. However, this chance is so trivially small[^4] that it might as well not exist, and thus for any purpose, real, theoretical, academic or educational, it is neglected.
#### Temperature
This definition of entropy is also satisfactory for the definition of [[absolute temperature]]. To see this, let's analyze if $T$ obeys the laws that we'd expect of it. If we take two objects in [[thermal equilibrium]] and at the same temperature, and we make the touch, nothing should happen. This is true: we've shown that two systems in contact maximize their entropy, which means that they're energies need to end up as $E_{1}=E_\text{max}$ and $E_{2}=E_\text{total}-E_\text{max}$. For nothing to happen, the systems need to have these energies from the get-go. But if they do, then $(1)$ is
$$\frac{ \partial S_{1}(E_{1}) }{ \partial E } =\frac{ \partial S_{2}(E_{2}) }{ \partial E } \quad\Rightarrow \quad T_{1}=T_{2}=T$$
which is exactly what we stated.

Say they are now at different temperatures. We know that they will exchange energy when they come into contact so, by conservation of energy, $\delta E_{1}=-\delta E_{2}$. The [[total differential]] of $S$ is
$$\delta S=\frac{ \partial S_{1}(E_{1}) }{ \partial E_{1} }\delta E_{1}+ \frac{ \partial S_{2}(E_{2}) }{ \partial E_{2} } \delta E_{2}=\left( \frac{ \partial S_{1}(E_{1}) }{ \partial E } - \frac{ \partial S_{2}(E_{2}) }{ \partial E }  \right)\delta E_{1}=\left( \frac{1}{T_{1}}- \frac{1}{T_{2}} \right)\delta E_{1} $$
$\delta S>0$ because of the second law, so if $T_{1}>T_{2}$ we need $\delta E_{1}<0$, so the hotter systems needs to lose energy. This behavior is also consistent, so this definition of temperature is valid. However, it doesn't prove why it's exactly $1/T$ and not, say, $1/T^{2}$, as the behavior would be the same. To prove this, we can plug this definition into a known system (probably an [[ideal gas]]) and show it is exactly $1/T$ that provides the correct result.
### Examples
> [!example] Fair coin
> A coin toss of a fair coin has a 50/50 chance of being head or tails. This means $p(\text{Heads})=1/2$ and $p(\text{Tails})=1/2$. So
> $$H_{X}=-\left( \frac{1}{2}\log_{2} \frac{1}{2}+ \frac{1}{2}\log_{2} \frac{1}{2} \right)=-\log_{2} \frac{1}{2}=-\log_{2}(2^{-1})=\log_{2}2=1\text{ bit}$$
> For $N$ fair coins, all tossed simultaneously, the probability of each combination of results is $p(x)=1/2^{N}=2^{-N}$ since they are all equiprobable and there are $2^{N}$ possible combinations. Thus, since all terms in the sum are identical, we have
> $$H_{X}=- 2^{N}(2^{-N}\log_{2}2^{-N})=N\log_{2}2=N \text{ bits}$$

> [!example] Fair dice
> A fair six-sided die has a $1/6$ chance of landing on each face, i.e. $p(x)=1/6$. Therefore
> $$H_{X}=-6\left( \frac{1}{6}\log_{2} \frac{1}{6} \right)=\log_{2}6\simeq 2.584\text{ bits}$$
> A fair $N$-sided die has a $1/N$ chance of landing on each face, so again
> $$H_{X}=-N\left( \frac{1}{N}\log_{2} \frac{1}{N} \right)=\log_{2} N \text{ bits}$$

> [!example] Unfair coin
> An unfair coin has chance $p$ to land on one side and $1-p$ to land on the other. The entropy of this coin is
> $$H_{X}=-p\log_{2}p-(1-p)\log_{2}(1-p)$$
> This function is important enough that it was given a special name: the [[Bernoulli entropy]]. It is applicable to any binary process of probability $p$.

> [!example] Horse racing
> Say there is a race with eight horses. The predictions say that each horse has the following chance to win the race
> $$\left( \frac{1}{2}, \frac{1}{4}, \frac{1}{8}, \frac{1}{16}, \frac{1}{64}, \frac{1}{64}, \frac{1}{64}, \frac{1}{64} \right)$$
> What is the entropy of this sequence? Well, this is a sequence of probabilities, so we can apply the definition of entropy directly:
> $$H=2\text{ bits}$$
> Same as two fair coin tosses. (For comparison, if the horses were all equally likely to win, it would have been $H=\log_{2}8=3\text{ bits}$). Now, say the winner of the race needs to be broadcasted. The simplest message to send would be the number of the horse that won in binary form so that we can take care of all possibilities. Since there are eight horses, and eight in binary is $111$, this makes us send over three bits of information per message. But note that the *actual* sequence above only has two bits of entropy. So, in theory, there's a method that, *on average*, only needs to send over two bits of information to fully convey the winning horse. We do this by exploiting the fact that we already know who is most likely to win.
> 
> To reduce average information being sent, we can make the most likely message shorter, at the cost of making the least likely ones longer. Thus, instead of sending over a message that is always three bits long as before, we can use the following convention to identify the eight horses:
> $$(0,10,110,1110,111100,111101,111110,111111)$$
> Here the message length is variable: the shortest message is a measly 1 bit, whereas the longest ones are 6 bits. But if we weigh these lengths by the likelihood of each being sent (i.e. that horse winning the race), we find that the *average* length is actually lower:
> $$\frac{1}{2} \times 1\text{ bit}+ \frac{1}{4}\times 2\text{ bits}+ \frac{1}{8}\times 3\text{ bits}+ \frac{1}{16}\times 4\text{ bits}+ 4\times \frac{1}{64} \times 6\text{ bits}=2\text{ bits}$$
> So while messages following this convention can on occasion be longer than before, they usually aren't, so on average, over many messages being sent out, this reduces the amount of bits being transferred by a lot. Note that the effectiveness of this convention is entirely dependent on the fact that we know those probabilities beforehand: had all horses been equally likely to win, this convention would have been on average worse.

[^1]: This is assuming discrete energy levels like the ones that occur in quantum mechanics. If $E$ is continuous, just change $E_{i}$ to $E$ and the sums to integrals. The result is the same.
[^2]: It can be argued that we have no guarantee that $E_\text{total}-E_{i}$ is a valid energy level for the other half if we are working with quantum levels. That said, energy levels for systems with massive $N$ are so closely packed they may as well be considered a continuum, so any energy level is pretty much guaranteed to be valid. To be more rigorous though, we would need to introduce an interaction term that guarantees the exchange of energy in a valid way.
[^3]: Since integrals don't have terms, the logic comes down to saying that the integral can be evaluated using [[Laplace's method]].
[^4]: I don't believe "trivially small" quite gets the point across. The chance of violating the second law of thermodynamics is so small that the average time it would take to find one violating event is so high, the *entire lifetime of the universe becomes negligible*.