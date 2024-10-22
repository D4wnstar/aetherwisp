**Conditional entropy** is a quantification of [[Entropy (information theory)|Shannon entropy]] for two correlated variables. Given two [[random variable|random variables]] $X$ and $Y$, the conditional entropy for $Y$ given $X$ is
$$H_{Y|X}=-\sum_{x \in \mathcal{X}} p(x)\sum_{y\in \mathcal{Y}} p(y|x)\log_{2}p(y|x)$$
where $p(y|x)$ is the [[conditional distribution function]] for $y$ given $x$. The chain rule for conditional probabilities applies here too:
$$H_{X,Y}=H_{X}+H_{Y|X}=H_{Y}+H_{X|Y}$$

If $X$ and $Y$ are [[independent variables]], conditional entropy is just normal entropy:
$$H_{Y|X}=H_{Y},\quad H_{X|Y}=H_{X}$$
