---
wiki-publish: true
---
The **conditional distribution function**[^1] of a set of $N$ [[Random variable|random variables]] is the function that gives the [[Probability]] of any outcomes when the value of one or more of the random variables is already known in advance. For instance, if the variables are four dice being rolled together, the conditional distribution function answers the question "what's the probability that the fourth die will roll a 5 if the other dice rolled a 3, a 4 and a 1?"

Formally, given a [[Joint distribution function]] $f(x_{1},x_{2})$, the conditional distribution function for two random variables $X_{1},X_{2}$ is
$$f_{C}(x_{2}|X_{1}=x^{*}_{1})=\frac{f(x^{*}_{1},x_{2})}{f_{M}(x^{*}_{1})}$$
where $x^{*}_{1}$ is the specific value that $X_{1}$ is chosen to take and $f_{M}$ is the [[Marginal distribution function]] that $X_{1}$ follows, evaluated in $x^{*}_{1}$. The notation $f_{C}(x_{2}|X_{1}=x^{*}_{1})$ means "the probability that $X_{2}$ will be the value $x_{2}$ knowing in advance that $X_{1}$ will be $x^{*}_{1}$". It is commonly abbreviated to $f_{C}(x_{2}|x^{*}_{1})$.
### Properties
- It is [[Normalization|normalized]]: $\int_{\Omega_{2}}f_{C}(x_{2}|x^{*}_{1})\ dx_{2}=1$ where $\Omega_{2}$ is the [[sample space]] of $X_{2}$. Same goes for any other combination of variables.
- For [[independent variables]], it matches the [[probability density function]]:
  $$f_{C}(x_{2}|x_{1}^{*})=\frac{f(x_{1}^{*},x_{2})}{f_{M}(x_{1}^{*})}=\frac{f(x_{1}^{*})f(x_{2})}{f(x_{1}^{*})}=f(x_{2})$$
- With three or more variables, it is possible to mix marginal and conditional distributions. For instance, with three variables $X_{1},X_{2},X_{3}$ you might want the distribution of $X_{1}$ when you already know that $X_{2}$ will be $x_{2}^{*}$ and without caring about the value of $X_{3}$. This would be the distribution of $X_{1}$ conditional to $X_{2}=x_{2}^{*}$ and marginal in $X_{3}$. It is denoted as $f_{C}(x_{1}|x_{2}^{*})$. The lack of $x_{3}$ implies the marginal distribution.
- With two variables, the joint distribution function is related to the marginal and conditional distribution functions as $f(x_{1},x_{2})=f_{M}(x_{1})f_{C}(x_{2}|x_{1})$. With more than two variables, some relation between the three still holds but is more complicated. For instance, for three variables we have $f(x_{1},x_{2},x_{3})=f_{M}(x_{3})f_{C}(x_{1},x_{2}|x_{3})$ but also $f(x_{1},x_{2},x_{3})=f_{M}(x_{2},x_{3})f_{C}(x_{1}|x_{2},x_{3})$. The general definition for $N$ variables is
  $$\boxed{f(x_{1},\ldots,x_{N})=f(x_{1})f(x_{2}|x_{1})f(x_{3}|x_{1},x_{2})\ldots f(x_{N}|x_{1},\ldots,x_{N-1})}$$
  where we have omitted the subscripts because most terms are mixed marginal-conditional distributions.
- It's possible to invert conditional and marginal distributions and have the definition still hold. For instance, in two variables:
  $$f(x_{1},x_{2})=f_{M}(x_{1})f_{C}(x_{2}|x_{1})=f_{M}(x_{2})f_{C}(x_{1}|x_{2})$$
  Notice how we inverted the conditional and marginal definitions. If we extract $f_{C}(x_{1}|x_{2})$ we get
  $$f_{C}(x_{1}|x_{2})=\frac{f_{M}(x_{1})f_{C}(x_{2}|x_{1})}{f_{M}(x_{2})}$$
  This result of paramount importance is known as **[[Bayes' theorem]]**.

[^1]: Be careful with the abbreviation "CDF", which usually refers to the much more common [[Cumulative distribution function]].
