---
wiki-publish: true
aliases:
  - Runge-Kutta 4
  - Dormand-Prince 5(4)
---
The **Runge-Kutta methods** (**RK** for short) are a family of numerical integration methods of a variety of orders, the most popular of which is the **fourth-order Runge-Kutta method**. They are essentially evolutions of [[Euler's method]], using specifically chosen quantities and points to estimate to increase the order of the method (and thus the precision) in some instances at the cost of more computation.

Despite their age, RK methods are very commonly used thanks to their strong versatility, good enough precision and ease of implementation. More modern methods, like [[predictor-corrector method|predictor-corrector methods]] or [[Bulirsch-Stoer method|Bulirsch-Stoer methods]], can be more efficient and precise in some instances, but require more effort to implement and aren't always the best choice.
### Fourth-order Runge-Kutta
The fourth-order Runge-Kutta (RK4 for short) method is a very popular variant of the RK methods due to ease of implementation and excellent results. As the name suggests, it is a fourth order method and requires four evaluations per physics step. For a one-dimensional autonomous [[Ordinary differential equation|ODE]] $\dot{x}=f(x)$ and a timestep $\Delta t$, the update rule from point $x_{n}$ to $x_{n+1}$ is given by
$$\begin{align}
k_{1}&=f(x_{n})\Delta t \\
k_{2}&=f\left( x_{n}+ \frac{1}{2}k_{1} \right)\Delta t \\
k_{3}&=f\left( x_{n}+ \frac{1}{2}k_{2} \right)\Delta t \\
k_{4}&=f(x_{n}+k_{3})\Delta t \\
x_{n+1}&=x_{n}+ \frac{1}{6}(k_{1}+2k_{2}+2k_{3}+k_{4})
\end{align}\tag{1}$$
Being a fourth-order method, the solution is precise up to the fourth order of its [[Taylor series]]:
$$x_{n+1}=x_{n}+ \frac{1}{6}(k_{1}+2k_{2}+2k_{3}+k_{4})+O(\Delta t^{5})$$
### Adaptive stepsize
The Runge-Kutta algorithms benefit a lot from making the value of $\Delta t$ dynamically chosen at runtime based on the shape of the function at any given point. This way, uneven and swiftly-changing regions can be faced with many more steps, as to avoid skipping over important details, whereas flat and slow-changing regions can be glossed over with few large steps, as there's little to be lost.

The idea of adaptive stepsize is two get *two* estimates per step instead of one, say $x^{(1)}_{n+1}$ and $x^{(2)}_{n+1}$, using either two different RK methods or the same method with different parameters. Critically, one of the two methods must be known to be more precise than the other. Then, you can find the difference $\Delta\equiv x^{(2)}_{n+1}-x^{(1)}_{n+1}$ between the two and use it as an error estimate. The important part here is that using a more precise method is the same as using a less precise method with a smaller stepsize (barring [[floating point error]]). Thus, you can interpret $\Delta$ as how much you gain by using a smaller stepsize. If $\Delta$ is small, then realistically you're just doing a lot of math to get very little out of it, so you might as well make the steps larger on subsequent passes and safe yourself the time. On the contrary, if $\Delta$ is large, you're doing something *very* imprecise and a reduction of stepsize is in order before you accidentally skip over fine details (in this case, you should *reject* the step and redo it right away with a smaller stepsize; keep rejecting and reducing until the error is small enough to justify, and only then move on to the next step. This way, the end result is guaranteed to all be below the chosen precision level).
#### Step doubling
The most straightforward approach to adaptive stepsize is a technique known as **step doubling**. In plain terms, each step is done not once, but thrice: once on the full step as normal, then two times more by splitting the step in two and running the algorithm on each half. Since each pass of RK4 requires four evaluations, this leads to a total of 12 evaluations per step. However, since the starting point is the same for both the full step and the first half, in practice it can be brought down to 11 by sharing the result. This is opposed to the 8 evaluations you would normally get by just blindly halving $\Delta t$ the size in two: an increase of 1.375 in number of operations.

Let's call $x(t+2\Delta t)$ the solution to a single step advancement using step doubling. Similarly, let's call $x_{1}(t+2\Delta t)$ the solution using the full step of size $2\Delta t$ and $x_{2}(t+2\Delta t)$ the solution using two half-steps each of size $\Delta t$. Since the base method is fourth order, the exact solution is expressed as
$$\begin{align}
x(t+2\Delta t)&=x_{1}+(2\Delta t)^{5}\phi+O(\Delta t^{6}) \\
x(t+2\Delta t)&=x_{2}+2\Delta t^{5}\phi+O(\Delta t^{6})
\end{align}\tag{2}$$
where $\phi$ is the rest of the fifth term in the Taylor series, $\phi=x^{(5)}(t)/5!$. In the first, $(2\Delta t)^{5}$ appears since that's the stepsize of the full step. In the second, $\Delta t^{5}$ appears, but it is doubled because we are taking two steps of size $\Delta t$. If we take the difference between the two,
$$\Delta\equiv x_{2}-x_{1}$$
we can use this is as a convenient estimate of [[truncation error]]. Since the value of $\Delta$ is fundamentally dependent on that of $\Delta t$, we can adjust it by cleverly varying our $\Delta t$ to raise or lower $\Delta$ to the value any value we like. In practice, $\Delta$ is actually a vector (since $x_{n}$ is in general a vector), where each component $\Delta_{i}$ is the error for each ODE. The value of $\Delta$ that's used to measure error is typically its [[norm]], $\lvert \Delta \rvert$, or the largest component, $\max\limits_{i=1,\ldots,n}\Delta_{i}$.

But we needn't stop here: if we take the difference between the equations in $(2)$, we can express the fifth-order term using the difference $\Delta$:
$$\begin{align}
0&=x(t+2\Delta t)-x(t+2\Delta t) \\
&=x_{1}+32\Delta t^{5}\phi-x_{2}-2\Delta t^{5}+O(\Delta t^{6}) \\
&=\underbrace{ x_{1}-x_{2} }_{ -\Delta }+30\Delta t^{5}\phi+O(\Delta t^{6})
\end{align}$$
and so
$$\Delta=30\Delta t^{5}\phi+O(\Delta t^{6})\quad\to \quad \Delta t^{5}\phi=\frac{\Delta}{30}+O(\Delta t^{6})$$
Plug this into the second equation in $(2)$ and you get
$$\boxed{x(t+2\Delta t)=x_{2}+ \frac{\Delta}{15}+O(\Delta t^{6})}\tag{3}$$
This form is fifth-order accurate, as opposed to fourth-order of the usual RK4. However, it's not all perfect: this equation comes with the annoying baggage of not giving any information regarding *its own* truncation error (remember that $\Delta$ is about $(2)$ not $(3)$), so we can't directly know if $(3)$ is improving or worsening the result. That said, empirically $(3)$ is pretty much a direct improvement over just plain $(1)$, but in lieu of data regarding its error, we use $\Delta$ as our error estimate instead[^1].
### Embedded Runge-Kutta formulas
While step doubling is simple, it is also not a particularly good improvement over baseline. Later on in history, a newer, more efficient stepsize adjustment method was developed that is more versatile and more precise than it.

The idea is that not all Runge-Kutta methods require the same number of evaluations as the order. For RK4, this is the case: four evaluations for fourth-order. But when you walk up the ladder to higher orders, this stops being true. While an exact rule to determine how many evaluations are needed for a given order $M$ has yet to be discovered, we know a few by hand: order 4 needs 4, order 5 needs 6, order 6 needs 7, order 8 needs 11. The highest manually derived order is 10, needing a whole 17 evaluations for a single step. Moreover, it's known that from order 8 onwards, one needs at least $M+3$ evaluations.

So how does this tie into error estimation? Well, it's because there isn't one unique way of formulating an $M$-th order RK method. There may be multiple combinations of coefficients and function evaluations to get an estimate of the same order. Pivotal to this method was the discovery by Fehlberg of a fifth-order RK using 6 evaluations, but also a fourth-order RK using a different combination of the *same* 6 evaluations. This means that you can, knowing the coefficients for both methods, take the difference the two estimates and use that as an error estimate. This is the essence of **embedded Runge-Kutta formulas**, using the same evaluations to get two different estimates by just recombining them in a different way.
#### Fifth-order Dormand-Prince
A good introductory method to embedded RK is the **fifth-order Dormand-Prince** method (**Dormand-Prince 5(4)**), an improved version of the original method by Fehlberg with different coefficients and better error properties.

The general form of a fifth-order RK method for a nonautonomous vector field $f(t,x)$ is
$$\begin{align}
k_{1}&=f(t,x_{n})\Delta t \\
k_{2}&=f(t+c_{2}\Delta t,x_{n}+a_{21}k_{1})\Delta t \\
&\vdots \\
k_{6}&=f(t+c_{6}\Delta t,x_{n}+a_{61}k_{1}+\ldots+a_{65}k_{5}) \\
x_{n+1}&=x_{n}+b_{1}k_{1}+b_{2}k_{2}+b_{3}k_{3}+b_{4}k_{4}+b_{5}k_{5}+b_{6}k_{6}+O(\Delta t^{6})=x_{n}+\sum_{i=1}^{6} b_{i}k_{i}+O(\Delta t^{6})
\end{align}$$
Meanwhile, we said that the *embedded* RK formula used the same evaluations, which is to say the same $k_{1},\ldots,k_{6}$, and is instead fourth-order:
$$x^{*}_{n+1}=x_{n}+b_{1}^{*}k_{1}+b_{2}^{*}k_{2}+b_{3}^{*}k_{3}+b_{4}^{*}k_{4}+b_{5}^{*}k_{5}+b_{6}^{*}k_{6}+O(\Delta t^{5})=x_{n}+\sum_{i=1}^{6} b_{i}^{*}k_{i}+O(\Delta t^{5})$$
Take the difference between the two and you get
$$\Delta\equiv x_{n+1}-x_{n+1}^{*}=\sum_{i=1}^{6} (b_{i}-b_{i}^{*})k_{i}$$
That said, with FSAL (see below) we can actually increase this to 7 evaluations "for free":
$$x_{n+1}=x_{n}+\sum_{i=1}^{7} b_{i}k_{i}+O(\Delta t^{6}),\quad x_{n+1}^{*}=x_{n}+\sum_{i=1}^{7} b_{i}^{*}k_{i}+O(\Delta t^{5})$$
$$\Delta\equiv x_{n+1}-x_{n+1}^{*}=\sum_{i=1}^{7} (b_{i}-b_{i}^{*})k_{i}$$

:::image
![[Dormand-Prince 5 coefficients.png]]
The coefficients for the Dormand-Prince 5(4) method. From *Numerical Recipes § 17.2*.
:::

Now that we have a $\Delta$, we actually need to make use of it. We'll set the following condition:
$$\lvert \Delta \rvert =\lvert x_{n+1}-x_{n+1}^{*} \rvert \leq\text{scale}\quad\text{where}\quad\text{scale}=\text{atol}+\lvert x \rvert \text{rtol}$$
where $\text{atol}$ and $\text{rtol}$ refer to absolute and relative [[tolerance]] respectively[^2]. In practice they can be chosen separately for each component of $\Delta$, which makes them two vectors, but often times they are more easily defined as constants. Since $\lvert \Delta \rvert$ can be all sorts of values, we need some standardized form to determine how to accept or reject the step. We will define the *scaled* error as
$$\boxed{\text{error}=\sqrt{ \frac{1}{N}\sum_{i=0}^{N-1} \left( \frac{\Delta_{i}}{\text{scale}_{i}} \right)^{2} }}$$
where $N$ is the dimension of the system, and define the step acceptance condition as
$$\boxed{\text{if err}\leq 1\text{ accept, else reject}}$$
Now we need some way to adjust the stepsize. To do so, we need to understand the relationship between $\Delta t$ and $\text{error}$. We know that $\Delta$ goes like $\sim \Delta t^{5}$ (since it inherits the worse of the two methods), and therefore so does $\text{error}$. If we take a step $\Delta t_{1}$ and end up with some error $\text{error}_{1}$, then the step $\Delta t_{2}$ that would have made another error $\text{error}_{2}$ is
$$\Delta t_{1}=\Delta t_{2}\left\lvert  \frac{\text{error}_{1}}{\text{error}_{2}}  \right\rvert ^{1/5}$$
If we arbitrarily set $\text{error}_{1}=1$ (the threshold we set before), then we can use this to estimate what the stepsize should have been when we get a rejection, or alternatively how much we can safely increase the stepsize by without worsening precision when we get an acceptance. Like in step doubling, we are using information from less precise method (the fourth-order one here) to gauge the behavior of the more precise one (the fifth-order one here).

In general, since the error estimates are, well, estimates, it is best reduce the stepsize estimation by a bit just to avoid overestimation. Given a "safety factor" $S$, which is usually just under $1$ such as $S=0.95$ or $S=0.98$, setting $\text{error}_{1}=1$ and changing the indexes to be more significant we get the stepsize update rule:
$$\boxed{\Delta t_{n+1}=S\Delta t_{n}\left( \frac{1}{\text{error}_{n}} \right)^{1/5}}\tag{4}$$

Up until now, we've been discussing *local* errors, in that the check precision locally for each point and adapt as follows. This is called **error per step**. They don't have a "sense of progression" and can't respond to previous steps. Sometimes you might instead want *global* error estimation, especially if you are sensitive to the progressive accumulation of errors over the course of the integration that might throw off some assumption about the system. In such a case, the more steps we take, the more errors tend to pile up globally, so what we can do is make the scaling stepsize-dependent
$$\text{scale}=\epsilon f_{i}(x_{n},t)\Delta t$$
where $\epsilon$ is some small amount like $10^{-6}$. This way, the accuracy is not enforced on the values of $x$ themselves, but rather on its derivatives $f_{i}$. However, the stepsize adjustment needs to have its exponent updated:
$$\Delta t_{1}=\Delta t_{2}\left\lvert  \frac{\text{error}_{1}}{\text{error}_{2}}  \right\rvert ^{1/4}$$
This new method is called **error per unit step**, and unfortunately its often not that performant. The reason is that controlling the global error from the local one is very difficult. The global error at any given point is the sum of the global error up to the start of the last step, plus the local error of that step. Unsurprisingly, this makes global error cumulative and makes it depend on things that are not always the domain of the integration method, such as stability properties of the ODEs themselves. Thus, it's generally best to use error per step instead. Either way, the rule should be updated with the safety factor as before.

A practical note: it is best to not vary the stepsize in too large amounts at once, and the stepsize should also never increase if the previous step was rejected.
#### Control-theoretical stepsize controller
In control theory, the idea of adjusting the stepsize dynamically depending on the error could be considered a *process*, and the stepsize adaptation method above would be considered an *integrating controller*, with $\log \Delta t$ as the discrete control variable and $\text{error}$ as the control signal. It is known in control theory that a controller of this kind can be made more stable by adding an *additional* term proportional to $\text{error}$. Such a controller is known as a **PI controller**, where P refers to the proportionality and I to the integration. In this form, we get
$$\boxed{\Delta t_{n+1}=S\Delta t_{n} \frac{\text{error}_{n-1}^{\beta}}{\text{error}_{n}^{\alpha}}}$$
where $\alpha$ and $\beta$ are real constants. In the context of ODEs, both should be scaled by $1/k$, where $k$ is the order of the method ($k=5$ in Dormand-Prince 5(4)). If we set $\alpha=1/k$ and $\beta=0$, we get $(4)$ again. Setting nonzero $\beta$ helps with stability, but at the cost of making the system less willing to gloss over "easy" parts. Practical values to start are
$$\alpha=\frac{0.7}{k},\quad \beta=\frac{0.4}{k}$$
#### First-same-as-last (FSAL)
There exists a trick to improve the precision of the methods for "free", and it is to choose the coefficients $k_{1},\ldots,k_{n}$ such that the *last* coefficient $k_{n}$ is the same as the *first* coefficient $\hat{k}_{1}$ of the step *after*. This way, it can be reused without necessitating another evaluation. Mathematically, FSAL states that
$$k_{n}=f(t_{n}+c_{n}\Delta t,x_{n}+a_{n1}k_{1}+\ldots+a_{n(n-1)}k_{n-1})=f(t_{n+1},x_{n+1})=\hat{k}_{1}$$
Usage of FSAL is a strict improvement, since it's "free" performance, but it is not universal, as this condition is not always met by methods. For an example, the Dormand-Prince 5(4) method above uses FSAL.
### Interpolation
RK methods come packaged, at least in principle, with an associated [[interpolation]] method that makes use of the points, derivatives *and* intermediate trial steps $k_{1},\ldots,k_{7}$ that are evaluated by the method. This provides all RK methods with a [[dense output]] method of equal order to the method itself (or the less precise method for embedded RK).

The idea of this is to consider the method-specific parameters $b_{i}$ not as constants, but as *[[polynomial|polynomials]]* in some parameter $\theta \in[0,1]$. Here $\theta$ represents the "percentage progress" from one evaluated point $x_{n}$ to the next $x_{n+1}$, and varying $\theta$ continuously allows the calculation of arbitrarily many points between each step. In general, the interpolating polynomial will be of the form
$$x(t_{n}+\theta \Delta t)=x_{n}+\sum_{i} b_{i}(\theta)k_{i}$$
for however many $b$ and $k$ values there are in a method. Since the $k_{i}$ values are functionally derivatives, this is a kind of [[Hermite interpolation]]. It requires four pieces of information: $x_{n},x_{n+1},\dot{x}_{n}=f(t_{n},x_{n}),\dot{x}_{n+1}=f(t_{n+1},x_{n+1})$.
#### Dormand-Prince 5(4)
For Dormand-Prince 5(4) specifically, the polynomial can be rewritten in a different form using another set of coefficients $d_{1},\ldots,d_{7}$. For a step $\mathbf{x}_{n}\to \mathbf{x}_{n+1}$ with stepsize $\Delta t_{n}$, we define the normalized independent variable as
$$s(t)=\frac{t-t_{n}}{\Delta t}\in[0,1]$$
for $t\in[t_{n},t_{n}+\Delta t]$. This will more or less play the part of $\theta$ from before. Now, the interpolation polynomial *in this step specifically* is
$$\mathbf{x}(s)=\mathbf{r}_{1}+s \mathbf{r}_{2}+s(1-s)\mathbf{r}_{3}+s^{2}(1-s)\mathbf{r}_{4}+s^{2}(1-s)^{2}\mathbf{r}_{5}$$
where
$$\begin{align}
\mathbf{r}_{1}&=\mathbf{x}_{n} \\
\mathbf{r}_{2}&=\mathbf{x}_{n+1}-\mathbf{x}_{n} \\
\mathbf{r}_{3}&=\mathbf{k}_{1}- \mathbf{r}_{2} \\
\mathbf{r}_{4}&=\mathbf{r}_{2}- \mathbf{r}_{3}-\mathbf{k}_{7} \\
\mathbf{r}_{5}&=d_{1}\mathbf{k}_{1}+d_{3}\mathbf{k}_{3}+d_{4}\mathbf{k}_{4}+d_{5}\mathbf{k}_{5}+d_{6}\mathbf{k}_{6}+d_{7}\mathbf{k}_{7}
\end{align}$$
The coefficients $d_{1},\ldots,d_{7}$ are
$$\begin{align}
d_{1}&=-\frac{12715105075}{11282082432}\\
d_{2}&=0 \\
d_{3}&=\frac{87487479700}{32700410799} \\
d_{4}&=-\frac{10690763975}{1880347072} \\
d_{5}&=\frac{701980252875}{199316789632} \\
d_{6}&=-\frac{1453857185}{822651844} \\
d_{7}&=\frac{69997945}{29380423}
\end{align}$$

[^1]: This kind of procedure is known as **[[local extrapolation]]**.

[^2]: In practice, you should use $\max(\lvert x_{n} \rvert,\lvert x_{n+1} \rvert)$ instead of just $\lvert x \rvert$ in case one of them is near zero.
