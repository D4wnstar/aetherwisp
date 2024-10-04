The **binomial distribution** is a real univariate discrete [[probability distribution]] that describes events that can only take two values: true or false, head or tails, etc.. It is described by two parameters: $p$ and $q=1-p$, such that $p+q=1$. Its [[probability mass function]] is
$$P_{k}=P(k;n,p)=\begin{pmatrix}n \\ k\end{pmatrix}p^{k}q^{n-k}$$
using the [[Binomial theorem|binomial coefficient]], hence the name. $P_{k}$ is the probability that $k$ events will all be true (or head, or anything else), each with probability $p$ of occurring, over $n$ total attempts. For instance, the probability that 6 coin tosses will all result in head is, with probability $p=0.5$ and $q=0.5$:
$$P_{6}=\begin{pmatrix}n \\ 6\end{pmatrix}0.5^{6}0.5^{n-6}$$
Unsurprisingly, as the number of attempts $n$ goes up, the probability that it'll occur also goes up.

Its [[expectation value]] is $E[k]=np$ and its [[variance]] is $\text{var}(k)=npq=np(1-p)$.
### Moments
The algebraic [[moment-generating function]] is
$$M_{k}^{*}(t)=E[e^{tk}]=\sum_{k=0}^{n} e^{tk}\begin{pmatrix}n \\ k\end{pmatrix}p^{k}q^{n-k}=\sum_{k=0}^{n} \begin{pmatrix}n \\ k\end{pmatrix}(e^{t}p)^{k}q^{n-k}=(e^{t}p+q)^{n}$$
The central moment-generating function is
$$M_{k}(t)=E[e^{t(k-np)}]=e^{-tnp}M_{k}^{*}(t)=(e^{-tp}e^{t}p+e^{-tp}q)^{n}=(e^{tq}p+e^{-tp}q)^{n}$$
Taking the derivatives and evaluating in zero we get the algebraic moments
$$\mu_{0}^{*}=1,\quad \mu_{1}^{*}=\left.\frac{dM_{x}^{*}}{dt}\right|_{t=0}=np$$
and central moments
$$\mu_{0}=1,\quad \mu_{1}=0,\quad \mu_{2}=npq=\sigma ^{2},\quad \mu_{3}=npq(q-p),\quad \mu_{4}=(1-6pq+3npq)npq$$
The [[asymmetry coefficient]] is
$$\gamma_{1}=\frac{\mu_{3}}{\mu_{2}^{3/2}}=\frac{q-p}{\sqrt{ npq }}$$
which goes to zero for as $n\to \infty$. The [[kurtosis]] is
$$\gamma_{2}=\frac{\mu_{4}}{\mu_{2}^{2}}-3=\frac{1-6pq}{npq}+3-3=\frac{1-6pq}{npq}$$
