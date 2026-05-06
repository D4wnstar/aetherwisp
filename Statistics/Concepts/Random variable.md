---
hl-publish: true
aliases:
  - random vector
  - random matrix
---
A **random variable** (**RV**) is a quantity whose value cannot be known before measurement due to a dependency on [[random]] events. What can be known is the [[Probability distribution]] that the variable follows, which gives us no information on what the value we're investigating *is*, but does give us information on what the value *is likely to be*.

Generally speaking, it is assumed that a random variable is associated with a "[[true value]]", that is, the actual, errorless value of the quantity that an object or phenomenon possesses and that we then take measurements of. Our measurements are realizations of the random variable associated with the true value, with an error being introduced by our measurement process. For instance, a plank of wood has a true length, and our measurements try to come as close as possible to that true value.

It is also possible that the true value does not exist and that the quantity is fundamentally statistical. This may be something as simple as a die roll, which is exclusively random and has no true outcome, or as complicated as an quantum [[Funzione d'onda|wave functions]].

More formally, a random variable is a function $X:\Omega\to E$ whose domain (called the [[sample space]] $\Omega$) may be either discrete or continuous and includes all possible values that the variable can take, and its [[image]] is a [[measure|measurable]] [[set]] $E$. For instance, a coin flip may be described as the random variable $\text{Coin}:\{\text{Heads},\text{Tails}\}\to\{1,-1\}$. The benefit of this definition is that it allows binding non-mathematical concepts (like "heads", "tails", "win" or "loss") to mathematical ones (generally numbers).

In many cases, the sample space is naturally numeric. In these case, there is no need to "convert" the outcome's value and the random variabile is simply the identity function, so that $\Omega\equiv E$. For instance, the sample space of a six-sided die roll is $\{ 1,2,3,4,5,6 \}$, which we keep as-is. Even when $\Omega$ isn't numeric, it's common (but not obligatory) for the random variable to be [[bijective]], so that each distinct outcome has a distinct mathematical representation. In the coin flip above, "Heads" maps to $1$ and "Tails" maps to $-1$. This allows the two representations to be equivalent, which is convenient for clarity: you can say "heads" or "tails" to mean $1$ or $-1$ because they map uniquely. For these reasons, the distinction between $\Omega$ and $E$ is often left unspecified and the random variable is referred to using its outcomes (i.e., the elements of $\Omega$).

> [!question]- A note on notation
> Aetherwisp articles generally follow the advice above and limit themselves to defining $\Omega$, leaving $E$ unspecified unless relevant. Furthermore, they can employ the notation of referring to a random variable's values by their outcomes instead. For instance, $P(\text{Coin}=\text{Heads})$ is the probability of $\text{Coin}$ coming out as $\text{Heads}$. This is *wrong* because $\text{Heads}$ is the argument of $\text{Coin}$, not its value (which is $1$, since $\text{Coin}(\text{Heads})=1$), but it is *convenient* and generally clearer than the technically-correct notation $P(\text{Coin}=1)$.

Random variables are typically written with a capital letter like $X$, whereas specific values that the variable takes (sometimes called **realizations**) a written in a lowercase letter like $x$.

A [[Vector space|vector]] whose components are RVs is called a **random vector**. A [[matrix]] whose entries are RVs is called a **random matrix**.
### Discrete random variables
A discrete random variable $X$ in defined over a discrete sample space $\Omega=\{ x_{1},\ldots,x_{N} \}$ where $N$ may be either finite or infinite. The [[Probability]] that $X$ assumes the specific value $x_{i}$ is
$$P_{i}=P(X=x_{i})\quad\text{for }i\in \{ 1,\ldots,N \}$$
The set of probabilities $\{ P_{1},\ldots,P_{N} \}$ associated with $X$ are mapped to their respective outcomes by the [[probability mass function]] $p_{X}:\{ P_{1},\ldots,P_{N} \}\to \Omega$. Common discrete probability distributions are the [[Binomial distribution]] and the [[Poisson distribution]]. 
### Continuous random variables
A continuous random variable $X$ is defined over a continuous sample space $\Omega=[a,b]$. The edges may or may not be included and the space may also be infinite (i.e. $a=-\infty$ and/or $b=+\infty$). Unlike with discrete RVs, it is nonsensical to define the probability for a specific event occurring: since there are infinite possible events in a continuous distribution, the probability of any finite number of them is exactly zero. If we call $N$ the total number of possibile outcomes, the probability of seeing a specific outcome $x$ must behave like
$$\lim_{ N \to \infty } P_{x}=\lim_{ N \to \infty } \frac{1}{N}=0$$
We instead define the probability that $X$ will assume a value in a certain interval $[x_{1},x_{2}]$. We represent this probability as an integral over the interval $[x_{1},x_{2}]$:
$$P(x_{1}\leq X\leq x_{2})=\int_{x_{1}}^{x_{2}}f(x)dx$$
The function $f(x)$ is called the [[Probability density function]] of the distribution. For a more general space (not necessarily one dimensional), the probability of $X$ being in a subset $A\subset\Omega$ is
$$P(X\in A)=\int_{x \in A}dp(x)=\int _\text{all space}\mathbf{I}_{A}(x)dp(x)$$
where $dp(x)$ is the infinitesimal probability, which is often but not always equal to $f(x)dx$, and $\mathbf{I}_{A}$ is the **indicator function**, defined as[^1]
$$\mathbf{I}_{A}=\begin{cases}
1 & x \in A \\
0 & \text{otherwise}
\end{cases}$$
The most common continuous probability distribution is the [[Gaussian distribution]].

[^1]: $\mathbf{I}_{A}$ is functionally just a different way to represent an integral over $A$. The benefit is that you actually integrate over all space and $\mathbf{I}_{A}$ cuts out the parts that don't matter. This might make the integral nicer for analytical manipulation, as N-dimensional integrals over all space are usually easy to rewrite as nested 1D integrals.
