---
aliases:
  - Shannon entropy
  - information-theoretical entropy
---
In information theory, the **entropy** $H_{X}$ or $H(X)$ of a discrete [[random variable]] $X$ defined in the [[sample space]] $\mathcal{X}$ and following some [[probability distribution]] described by the [[probability mass function]] $p(x)$, is
$$H_{X}=-\sum_{x \in \mathcal{X}}p(x)\log_{2}p(x) $$
It is often called **Shannon entropy** due to it being originally introduced by Claude Shannon.

Strictly speaking, the base of the logarithm is arbitrary and may be any real number. Base two is the most common choice as it encodes the idea of "true or false" outcomes and is measured in **bits**. In physics, however, base $e$ (i.e. $\ln$) is the more common choice as it spontaneously arises in nature. Entropy in base $e$ is measured in **nats**.
### Interpretation
Shannon entropy can be described as a measure of the uncertainty of $X$. $H$ can be seen as  a sort of "missing information": the greater the entropy, the less information I have about $X$ a priori. For instance, if $X$ only has one possible value, entropy is zero as there is no uncertainty; I already know everything possible about $X$ before even sampling from it.
### Joint entropy
If $X$ and $Y$ are two random variables in sample spaces $\mathcal{X}$ and $\mathcal{Y}$, joint entropy is defined as follows
$$H_{X,Y}=-\sum_{x \in \mathcal{X}} \sum_{y\in \mathcal{Y}}p_{X,Y}(x,y)\log p_{X,Y}(x,y)$$
If $X$ and $Y$ are [[independent variable|independent variables]], it simplifies to
$$H_{X,Y}=-\sum_{x \in \mathcal{X}}\sum _{y \in \mathcal{Y}}p_{X,Y}(x,y)[\log p_{X}(x)+\log p_{Y}(y)]=H_{X}+H_{Y} $$
### Properties
- It is non-negative: $H_{X}\geq 0$. It is zero only if $X$ is certain (i.e. it only has one possible outcome).
- If $X$ has more than one possible outcome, then $H_{X}$ is maximized when all those outcomes are equiprobable.
- Joint entropy is generally less than the sum of the single entropies: $H_{X,Y}\leq H_{X}+H_{Y}$. It is equal only if $X$ and $Y$ are independent.
- Entropy is additive across [[Physical system|systems]] (*not* across variables; see previous property). The entropy of a system is equal to the sum of entropies of disjoint subsystems.
### Examples
> [!example] Fair coins
> A coin toss of a fair coin has a 50/50 chance of being head or tails. This means $p(\text{Heads})=1/2$ and $p(\text{Tails})=1/2$. So
> $$H_{X}=-\left( \frac{1}{2}\log_{2} \frac{1}{2}+ \frac{1}{2}\log_{2} \frac{1}{2} \right)=-\log_{2} \frac{1}{2}=-\log_{2}(2^{-1})=\log_{2}2=1\text{ bit}$$
> For $N$ fair coins, all tossed simultaneously, the probability of each combination of results is $p(x)=1/2^{N}=2^{-N}$ since they are all equiprobable and there are $2^{N}$ possible combinations. Thus, since all terms in the sum are identical, we have
> $$H_{X}=- 2^{N}(2^{-N}\log_{2}2^{-N})=N\log_{2}2=N \text{ bits}$$

> [!example] Fair dice
> A fair six-sided die has a $1/6$ chance of landing on each face, i.e. $p(x)=1/6$. Therefore
> $$H_{X}=-6\left( \frac{1}{6}\log_{2} \frac{1}{6} \right)=\log_{2}6\simeq 2.584\text{ bits}$$
> A fair $N$-sided die has a $1/N$ chance of landing on each face, so again
> $$H_{X}=-N\left( \frac{1}{N}\log_{2} \frac{1}{N} \right)=\log_{2} N \text{ bits}$$
