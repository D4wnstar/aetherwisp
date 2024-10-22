The **mutual information** $I$ measures the reduction of uncertainty of a [[probability distribution]] due to the knowledge of another distribution. It is called "mutual information" because it quantifies how much information one distribution gives about the other. This inherently means that two distributions must be correlated for there to be (nonzero) mutual information, as if they are [[independent variables|independent]], one cannot give information about the other; in this case, $I=0$.

Given two correlated [[random variable|random variables]] $X$ and $Y$ defined over [[sample space|sample spaces]] $\mathcal{X}$ and $\mathcal{Y}$, their mutual information is
$$I_{X,Y}=\sum_{x \in \mathcal{X}}\sum_{y\in \mathcal{Y}} p_{X,Y}(x,y)\log_{2} \frac{p_{X,Y}(x,y)}{p_{X}(x)p_{Y}(y)}$$
where $p_{X}$ and $p_{Y}$ are the [[Probability mass function|probability mass functions]] of the random variables and $p_{X,Y}$ is their [[joint distribution function]].
### Properties
- It is non-negative: $I_{X,Y}\geq 0$. It is zero only if $X$ and $Y$ are independent.
- It is related to [[Entropy (information theory)|information-theoretical entropy]] and [[conditional entropy]] by $I_{X,Y}=H_{Y}-H_{Y|X}$.