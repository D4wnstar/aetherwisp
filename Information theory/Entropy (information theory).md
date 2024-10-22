---
aliases:
  - Shannon entropy
  - information-theoretical entropy
  - joint entropy
---
In information theory, the **entropy** $H_{X}$ or $H(X)$ of a discrete [[random variable]] $X$ defined in the [[sample space]] $\mathcal{X}$ and following some [[probability distribution]] described by the [[probability mass function]] $p(x)$, is
$$H_{X}=-\sum_{x \in \mathcal{X}}p(x)\log_{2}p(x) $$
It is often called **Shannon entropy** due to it being originally introduced by Claude Shannon.

Strictly speaking, the base of the logarithm is arbitrary and may be any real number. Base two is the most common choice as it encodes the idea of "true or false" outcomes and is measured in **bits**. In physics, however, base $e$ (i.e. $\ln$) is the more common choice as it spontaneously arises in nature. Entropy in base $e$ is measured in **nats**.
### Interpretation
Shannon entropy can be described as a measure of the uncertainty of $X$. $H$ can be seen as  a sort of "missing information": the greater the entropy, the less information I have about $X$ a priori. For instance, if $X$ only has one possible value, entropy is zero as there is no uncertainty; I already know everything possible about $X$ before even sampling from it.
### Joint entropy
If $X$ and $Y$ are two random variables in sample spaces $\mathcal{X}$ and $\mathcal{Y}$, **joint entropy** is defined by just changing the normal distribution function to a [[joint distribution function]]:
$$H_{X,Y}=-\sum_{x \in \mathcal{X}} \sum_{y\in \mathcal{Y}}p_{X,Y}(x,y)\log p_{X,Y}(x,y)$$
If $X$ and $Y$ are [[independent variables]], it simplifies to
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
