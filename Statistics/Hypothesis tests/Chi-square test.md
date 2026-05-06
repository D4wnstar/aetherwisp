---
hl-publish: true
---
A **chi-square test** or **$\chi ^{2}$-test** is a type of [[hypothesis test]] on a [[sample]] of [[Gaussian distribution|Gaussian]] [[Random variable|random variables]]. It is a [[Gaussian parameter tests|Gaussian parameter test]], but it's common enough to warrant it's own article. It's popularity is due to the commonness of Gaussian samples, alongside the simplicity and usefulness of the test.

Suppose the sample $\{ X_{1},\ldots,X_{N} \}$ is composed of $N$ Gaussian random variables, not necessarily [[iid]], of which we know the [[variance|variances]] $\sigma_{i}^{2}$, and we want to test that [[mean|means]] $\mu_{i}$ are equal to some values we're looking for, generally ones we expect from theory. Our hypotheses are
$$\begin{cases}
H_{0}:&\mu_{i}=\mu_{0,i} \\
H_{1}:&\mu_{i}\neq\mu_{0,i}
\end{cases}\quad\forall i=1,\ldots,N$$
We ask that each distribution individually has a mean equal to some value $\mu_{0,i}$. It is (almost) like $N$ simultaneous [[Gaussian parameter tests|Z-tests]] for $N$ separate Gaussians. Instead of testing that a mean equals a test mean, you are testing that a *vector* of means equals a *vector* of test means. The test [[statistic]] is
$$T=\sum_{i=1}^{N} \frac{(X_{i}-\mu_{0,i})^{2}}{\sigma_{i}^{2}}\sim \chi ^{2}_{N}\tag{1}$$
which follows a [[chi-square distribution]] with $N$ degrees of freedom. The critical region is defined as a one-tailed region for high values of $t$.

The $\chi ^{2}$ test differs from $N$ different applications of the Z-test because it does not require the Gaussian RVs to be iid and also considers correlations. They can be differently distributed, so that all Gaussian distributions have different $\mu$ and $\sigma ^{2}$ parameters, and the test still applies. They also don't need to be [[Independent variables|independent]]; in fact, if the RVs are dependent on each other, the test still holds as long as we use the more general test statistic
$$T=(\mathbf{X}-\boldsymbol{\mu}_{0})^{T}\Sigma^{-1}(\mathbf{X}-\boldsymbol{\mu}_{0})\sim \chi_{N}^{2}$$
where $\Sigma$ is the [[Covariance|covariance matrix]] of the RVs, $\mathbf{X}\equiv(X_{1},\ldots,X_{N})$ and $\boldsymbol{\mu}_{0}=(\mu_{0,1},\ldots,\mu_{0,N})$. It also follows the $\chi_{N}^{2}$ distribution and reduces to the previous form in the case independent variables.

Despite its popularity, the $\chi ^{2}$ test has a few weakness:
- It requires the variances to be known. If only the mean is known, then a parameter test for the mean might be more appropriate.
- It is blind to the sign of the deviation from the mean. If the null hypothesis is rejected, the test can't tell you if the sample mean is an over- or an underestimate.
- Finally, it's a rather low [[power (hypothesis test)|power]] (confidence) test for low $N$ due to $\chi ^{2}_{N}$ having broad tails.
### Applications
> [!example]- Compatibility of measurements
> The $\chi ^{2}$ test is useful to determine if multiple measurements of the same quantity are compatible with each other. Suppose you have a realized sample of $\{ x_{1},\ldots,x_{N} \}$ measurements. Because they are all measurements of the same quantity, it is assumed that they are iid. Therefore, there is one true mean $\mu_{0}$ so that $\mu_{i}=\mu_{0}\; \forall i$, but not necessarily $\sigma_{i}=\sigma$ as each measurement can have a different error. If $\mu_{0}$ is known (e.g., from theory or a previous independent experiment), the value of the test statistic is
> $$t=\sum_{i=1}^{N} \frac{(x_{i}-\mu_{0})^{2}}{\sigma_{i}^{2}}$$
> The RV behind this number follows a $\chi_{N} ^{2}$, as outlined above. If $\mu_{0}$ is not known, then you can substitute the sample mean $\bar{x}$:
> $$t=\sum_{i=1}^{N} \frac{(x_{i}-\bar{x})^{2}}{\sigma_{i}^{2}}$$
> The RV behind this number instead follows $\chi_{N-1}^{2}$, because using the sample mean removes one degree of freedom. If the null hypothesis is rejected, not all measurements are compatible, as for some $\mu_{i}\neq \mu_{0}$.

> [!example]- Validity of a relation
> Suppose you have a realized sample of $N$ measurements $\{ y_{1},\ldots,y_{N} \}$ of a quantity $\mathcal{Y}$, taken from a sample of Gaussian RVs $\{ Y_{1},\ldots,Y_{N} \}$ with known variances $\sigma_{i}^{2}$. These are taken jointly with another set of $N$ measurements $\{ x_{1},\ldots,x_{N} \}$ of a different quantity $\mathcal{X}$, and you want to prove that the two quantities are related according to some function $\mathcal{Y}=f(\mathcal{X};a_{1},\ldots,a_{k})$, where $a_{1},\ldots,a_{k}=\mathbf{a}$ are the (known!) parameters of the function $f$. For example, you may want to prove that the [[electric field]] (magnitude) $E=\mathcal{Y}$ and the [[electric potential]] $V=\mathcal{X}$ are, in some particular condition, related by $E=(a_{1}/a_{2})V+a_{3}$, and you have collected $N$ pairs of empirical measurements to do so. The $\chi ^{2}$ test can do this.
>
> First, reinterpret the null hypothesis slightly as
> $$H_{0}:\mu_{i}=\text{E}[Y_{i}]=f(x_{i};\mathbf{a})\; \forall i$$
> We're taking the test means to be the values of our expected relation. Then, run the test using the statistic in $(1)$, using $f(x_{i};\mathbf{a})$ instead of $\mu_{0,i}$. If the null hypothesis is accepted, your formula is valid.
>
> Note that the degrees of freedom of $\chi ^{2}$ are $N$ only if the parameters $\mathbf{a}$ are known from source external from your measurements. If you instead calculate $\mathbf{a}$ from the same values $\{ x_{1},\ldots,x_{N} \}$ that you are testing, the $\chi ^{2}$ actually has $N-k$ degrees of freedom, as you are imposing $k$ constraints due to the estimates. Since $\chi ^{2}$ tests become less confident with less degrees of freedom, this makes your test a bit less reliable.

> [!example]- Pearson's goodness-of-fit test
> The $\chi ^{2}$ test can also quantify how well an empirical distribution matches an expected distribution. Say you have a sample of $x_{1},\ldots,x_{N}$ data points sampled from a RV $X$. You [[histogram]] them to see their empirical distribution. The histogram has $\nu$ bins, each containing $n_{1},\ldots,n_{\nu}$ samples. The expected occupation of a bin in a histogram can be approximated with the [[binomial distribution]], as long as the [[Probability density function|PDF]] $f_{X}(x;\boldsymbol{\theta})$ is known (which it should be, since you're choosing it). The expected occupation is
> $$\mathrm{E}[n_{i}]=\mu_{n_{i}}\simeq Np_{i}$$
> where $p_{i}$ is the total probability of falling in a bin, as given by the PDF. It can be found either from the [[Cumulative distribution function|CDF]] $F(x)$ or approximated from the PDF if the bins are thin enough:
> $$p_{i}=F(x_{i+1})-F(x_{i})\simeq \Delta_{i}f(x^{*}_{i})$$
> Here $x_{i}$ and $x_{i+1}$ are the left and right edges of the bin, $\Delta_{i}=\lvert x_{i+1}-x_{i} \rvert$ is the width of the bin and $x_{i}^{*}=(x_{i+1}-x_{i})/2$ is the center of the bin. Now we are back in the state of a typical $\chi ^{2}$ test, but instead of testing the means of the random sample, we are testing the means of the *bins* made from the random sample:
> $$H_{0}:n_{i}=\mu_{n_{i}}\;\forall i$$
> The test statistic is
> $$t=\sum_{i=1}^{\nu} \frac{(n_{i}-\mu_{n_{i}})^{2}}{\mu_{n_{i}}}\sim \chi ^{2}$$
> Be careful to sum over $\nu$ bins, not $N$ samples like the other $\chi ^{2}$ tests! This statistic follows a $\chi ^{2}$ distribution. The degrees of freedom are $\nu-1$ if the parameters $\boldsymbol{\theta}=(\theta_{1},\ldots,\theta_{k})$ of $f_{X}(x;\boldsymbol{\theta})$ are known independently. If they are estimated from the test sample, the degrees are $\nu-1-k$ because you set $k$ constraints for the estimation. If you accept the null hypothesis, then the data follows the distribution $f_{X}$ you selected.

> [!example]- Independence test
> The $\chi ^{2}$ test can also be used to determine the independence of two quantities. Say you have a sample of data $(x_{1},y_{1}),\ldots,(x_{N},y_{N})$ from two RVs $X$ and $Y$. For instance, this could be a sample of $N$ people's heights ($x$) and weights ($y$) and you want to see if the two are independent or not. Our metric of independence uses the fact that the [[joint distribution function]] of two independent variables is just the product of the two:
> $$f_{XY}(x,y)=f_{X}(x)f_{Y}(y)$$
> You then essentially just apply the Pearson's goodness-of-fit test to see if the product of $f_{X}$ and $f_{Y}$ as found empirically is indeed $f_{XY}$. You proceed in a similar manner, but you have to work with a multidimensional [[histogram]]. In the example case, a 2D histogram with $\nu$ height bins and $\kappa$ weight bins. This kind of histogram can be represented as an $\nu\times \kappa$ table or [[matrix]] where each cell $n_{ij}$ is the occupation of the $ij$ bin. Similarly to the Pearson test, we use the estimates for expected bin counts:
> $$\mathrm{E}[n_{ij}]=\mu_{n_{ij}}=Np_{ij}$$
> The probability can estimated from the data itself using the frequentist interpretation (observed events over total events), which involves finding the occupation of each row and column and dividing by the sample size. For example, the probability of a value of $X$ falling in the $j$-th column (first height bin) is $p_{:j}=n_{:j}/N=(n_{1j}+n_{2j}+\ldots+n_{\nu j})/N$, where the subscript $:j$ indicates the sum of all values of the $j$-th column. Similarly, for the $i$-th row, $p_{i:}=n_{i:}/N=(n_{i1}+n_{i2}+\ldots+n_{i\kappa})/N$. Then, the mean bin occupations are
> $$\mu_{n_{ij}}=N(p_{i:}+p_{:j})=N \frac{n_{i:}}{N} \frac{n_{:j}}{N}=\frac{n_{i:}n_{:j}}{N}$$
> If the probability of falling in any given bin is small, you can use the [[Poisson distribution]] to state that $\sigma ^{2}_{ij}=\mu_{ij}$. Moreover, since the Poisson distribution obeys the [[central limit theorem]], if the bin counts are large enough (at least 5, ideally more), the bin occupation distribution becomes approximately Gaussian. The test therefore becomes a regular Pearson's goodness-of-fit test extended to multiple dimensions:
> $$t=\sum_{i=1,j=1}^{\nu,\kappa} \frac{(n_{ij}-\mu_{n_{ij}})^{2}}{\mu_{n_{ij}}}\sim \chi ^{2}$$
> This has a $\chi ^{2}$ distribution of course, and has degrees of freedom $(\nu-1)(\kappa-1)$. If the null hypothesis is accepted, the two quantities are independent.
> 
> In principle, extending this to testing the independence of more than two variables at the same time is easy. You just need one dimension per variable in the histogram, then calculate the probability and the test statistic in the same way, and add one more $(\text{bins}-1)$ factor to the degrees of freedom. In practice, this is problematic in all sorts of ways. For one, high-dimensional data explodes in complexity very fast and is incredibly difficult to visualize. Moreover, it's easier to make mistakes in indexing, both by hand and in programming. Finally, histograms suffer the "curse of dimensionality", which makes the bins become very sparse as the dimensions go up, which messes with the CLT assumption for the Poisson distribution. In general, it is possibly more sensible to only independence-test two variables at once because of these reasons.
