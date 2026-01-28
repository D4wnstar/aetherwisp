---
wiki-publish: true
---
A **chi-square test** or **$\chi ^{2}$-test** is a type of [[hypothesis test]] on a [[sample]] of [[Gaussian distribution|Gaussian]] [[Random variable|random variables]]. It is a [[Gaussian parameter tests|Gaussian parameter test]], but it's common enough to warrant it's own article. It's popularity is due to the commonness of Gaussian samples, alongside the simplicity and usefulness of the test.

Suppose the sample $\{ X_{1},\ldots,X_{N} \}$ is composed of $N$ Gaussian random variables, not necessarily [[iid]], of which we know the [[variance|variances]] $\sigma_{i}^{2}$, and we want to test that [[mean|means]] $\mu_{i}$ are equal to some values we're looking for, generally ones we expect from theory. Our null hypothesis is $H_{0}:\mu_{i}=\text{E}[X_{i}]\;\forall i$. The test [[statistic]] is
$$T=\sum_{i=1}^{N} \frac{(X_{i}-\mu_{i})^{2}}{\sigma_{i}^{2}}\sim \chi ^{2}_{N}\tag{1}$$
which follows a [[chi-square distribution]] with $N$ degrees of freedom. The critical region is defined as usual as a one-tailed region for high values of $t$.

The $\chi ^{2}$ test differs from the more typical parametric mean test because it does not require the Gaussian RVs to be iid, in both ways. They can be differently distributed, so that all Gaussian distributions have different $\mu$ and $\sigma ^{2}$ parameters, and the test still applies. They also don't need to be [[Independent variables|independent]]; in fact, if the RVs are dependent on each other, the test still holds as long as we use the more general test statistic
$$T=(\mathbf{X}-\boldsymbol{\mu})^{T}\mathrm{V}^{-1}(\mathbf{X}-\boldsymbol{\mu})\sim \chi_{N}^{2}$$
where $\mathrm{T}$ is the [[Covariance|covariance matrix]] of the RVs, $\mathbf{X}\equiv(X_{1},\ldots,X_{N})$ and $\boldsymbol{\mu}=(\mu_{1},\ldots,\mu_{N})$. It also follows the $\chi_{N}^{2}$ distribution and reduces to the previous form in the case independent variables.

The downside of this test is that it requires the variances to be known. If only the mean is known, then a parameter test for the mean is more appropriate.

Despite its popularity, the $\chi ^{2}$ test has a few weakness. For one, it is blind to the sign of the deviation from the mean. If the null hypothesis is rejected, the test can't tell you if the sample mean is an over- or an underestimate. Moreover, it's a rather low-confidence test for low $N$.
### Applications
> [!example]- Compatibility of measurements
> The $\chi ^{2}$ test is useful to determine if multiple measurements of the same quantity are compatible with each other. Suppose you have a realized sample of $\{ x_{1},\ldots,x_{N} \}$ measurements. All these measurements are about the same [[true value]], so $\mu_{i}=\mu\; \forall i$, but not necessarily $\sigma_{i}=\sigma$ as each measurement can have a different error. If $\mu$ is known (e.g., from theory or a previous independent experiment), the value of the test statistic is
> $$t=\sum_{i=1}^{N} \frac{(x_{i}-\mu)^{2}}{\sigma_{i}^{2}}$$
> The RV behind this number follows a $\chi_{N} ^{2}$, as outlined above. If $\mu$ is not known, then you can substitute the sample mean $\bar{x}$:
> $$t=\sum_{i=1}^{N} \frac{(x_{i}-\bar{x})^{2}}{\sigma_{i}^{2}}$$
> The RV behind this number instead follows $\chi_{N-1}^{2}$. In other words, using the sample mean removes one degree of freedom. If the null hypothesis is rejected, not all measurements as compatible, as for some $\mu_{i}\neq \mu$.

> [!example]- Validity of a relation
> Suppose you have a realized sample of $N$ measurements $\{ y_{1},\ldots,y_{N} \}$ of a quantity $\mathcal{Y}$, taken from a sample of Gaussian RVs $\{ Y_{1},\ldots,Y_{N} \}$ with known variances $\sigma_{i}^{2}$. These are taken jointly with another set of $N$ measurements $\{ x_{1},\ldots,x_{N} \}$ of a different quantity $\mathcal{X}$, and you want to prove that the two quantities are related according to some function $\mathcal{Y}=f(\mathcal{X};a_{1},\ldots,a_{k})$, where $a_{1},\ldots,a_{k}$ are the (known!) parameters of the function $f$. For example, you may want to prove that the [[electric field]] (magnitude) $E=\mathcal{Y}$ and the [[electric potential]] $V=\mathcal{X}$ are, in some particular condition, related by $E=(a_{1}/a_{2})V+a_{3}$, and you have collected $N$ pairs of empirical measurements to do so. The $\chi ^{2}$ test can do this.
>
> First, reinterpret the null hypothesis slightly as $H_{0}:\mu_{i}=\text{E}[Y_{i}]=f(x_{i};a_{1},\ldots,a_{k})\; \forall i$. Then, run the test using the statistic in $(1)$, using $f(x_{i};a_{1},\ldots,a_{k})$ instead of $\mu_{i}$. If the null hypothesis is accepted, your formula is valid.
>
> Note that the degrees of freedom of $\chi ^{2}$ are $N$ only if the parameters $a_{1},\ldots,a_{k}$ are known from source separated from your measurements. If you instead calculated $a_{1},\ldots,a_{k}$ from the same values $\{ x_{1},\ldots,x_{N} \}$ that you are testing, the $\chi ^{2}$ actually has $N-k$ degrees of freedom. Since $\chi ^{2}$ tests become less confident with less degrees of freedom, this makes your test a bit less reliable.
