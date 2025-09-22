---
wiki-publish: true
---
The **Doppler effect** or **Doppler shift** is the change in [[frequency]] of a [[Wave]] due to its motion with respect to an observer. The frequency is increased if the wave is moving towards the observer or reduced otherwise. Being a relative effect, its description depends on whether we are using Galilean relativity or Einstein relativity. It is a consequences of the invariance of a [[phase]] across [[frame of reference|frames of reference]].
### Classical Doppler effect
Consider two frames of reference, $S$ and $S'$, and a wave of [[Frequency|angular frequency]] $\omega$ and $\omega'$ depending on which frame you are measuring it in. The frame $S$ is attached to the observer, whereas $S'$ is the source frame, so $\omega$ will be the observed frequency and $\omega'$ will be the "emission" frequency.

...

The modified angular frequency is
$$\boxed{\omega'=\omega\left( 1- \frac{\hat{\mathbf{n}}\cdot \hat{\mathbf{v}}}{\mu} \right)}$$
Say the source is standing still and the source is moving. If the source is moving *away*, then $\hat{\mathbf{n}}\cdot \hat{\mathbf{v}}<0$ and $\omega<\omega'$. This means that the observed frequency is lower: in case of light, it will be redder, and in case of sound, it will be lower pitched. Similarly, if the source is moving *towards the observer*, then $\hat{\mathbf{n}}\cdot \hat{\mathbf{v}}>0$ and $\omega>\omega'$. Light becomes bluer and sound becomes higher pitched.

Say now the source is standing still and the observer is the one moving. If the observer is moving *away*, then $\hat{\mathbf{n}}\cdot \hat{\mathbf{v}}>0$ and $\omega>\omega'$. Light becomes bluer and sounds go higher. As you may guess, if the observer is moving *towards the source*, then $\hat{\mathbf{n}}\cdot \hat{\mathbf{v}}<0$ and $\omega<\omega'$. Light becomes redder and sounds go deeper.

In general, if the distance between source and observer is getting smaller, the perceived frequency increases, otherwise it decreases.

> [!success] Doppler effect
> The frequency of a wave phenomenon as perceived by an observer depends on their relative motion.
> - If the source and observer are getting closer, the frequency is increased.
> - If they are getting farther, the frequency is decreased.

### Relativistic Doppler effect
The relativistic version of the effect is essentially the same as the classical one, with the key difference that we employ [[Lorentz transformation|Lorentz transformations]] instead of Galilean ones. It is still a consequence of phase invariance.

Consider a wave of phase $c\omega t-c\mathbf{k}\cdot \mathbf{x}=c\omega't'-c\mathbf{k}'\cdot \hat{\mathbf{x}}'$. The Lorentz transformation from $(x_{0},x_{1},x_{2},x_{3})$ to $(x_{0}',x_{1}',x_{2}',x_{3}')$ says
$$\begin{cases}
x_{0}'=\gamma(x_{0}-\beta x_{1}) \\
x_{1}'=\gamma(x_{1}-\beta x_{0}) \\
x_{2}'=x_{2} \\
x_{3}'=x_{3}
\end{cases}$$
With the [[Scalar product|scalar products]] expanded, the phase reads
$$\omega x_{0}-c(k_{1}x_{1}+k_{2}x_{2}+k_{3}x_{3})=\omega'x_{0}'-c(k_{1}'x_{1}'+k_{2}'x_{2}'+k_{3}'x_{3}')$$
Applying the reverse transformation (from $\mathbf{x}'$ to $\mathbf{x}$) yields
$$\omega \gamma(x_{0}'+\beta x_{1}')-ck_{1}\gamma(x_{1}'+\beta x_{0}')-ck_{2}x_{2}'-ck_{3}x_{3}'=\omega'x_{0}'-c(k_{1}'x_{1}'+k_{2}'x_{2}'+k_{3}'x_{3}')$$
We'll do some algebra to extract the [[Wavenumber|wavenumbers]]:
$$(\omega \gamma-c\gamma \beta k_{1})x_{0}'+(\omega \gamma \beta-ck_{1}\gamma)x_{1}'-ck_{2}x_{2}'-ck_{3}x_{3}'=\omega'x_{0}'-c(k_{1}'x_{1}'+k_{2}'x_{2}'+k_{3}'x_{3}')$$
Divide through by $c$ and compare term by term
$$\frac{\omega \gamma}{c}-\gamma \beta k_{1}=\frac{\omega'}{c},\quad \frac{\omega \gamma \beta}{c}-k_{1}\gamma=-k_{1}',\quad k_{2}=k_{2}',\quad k_{3}=k_{3}'$$
Further comparing this with the Lorentz transformation
$$k_{0}'=\gamma(k_{0}-\beta k_{1}),\quad k_{1}'=\gamma(k_{1}-\beta k_{0}),\quad k_{2}'=k_{2},\quad k_{3}'=k_{3}$$
we can define the wave [[four-vector]] as
$$k^{\mu}=\left( \frac{\omega}{c},\mathbf{k} \right)$$
???
$$k_{0}=\frac{\omega}{c}\lvert \mathbf{k} \rvert ,\quad k_{0}'=\frac{\omega'}{c}=\lvert \mathbf{k}' \rvert $$
From this we can write
$$\frac{\omega'}{c}=\gamma\left( \frac{\omega}{c}-\beta k_{x} \right)=\gamma\left( \frac{\omega}{c}-\beta k\cos \theta \right)$$
where $\theta$ is the angle between the velocity of the wave and the line between the wave and the observer. Using $k=\omega/c$ and extracting $\omega'$ gives use the relativistic Doppler effect:
$$\boxed{\omega'=\gamma \omega(1-\beta \cos \theta)}$$
The equation reads a little different, but the gist of it is the same. $\omega'$ is $\omega$ rescaled by some factor, in this case $\gamma(1-\beta \cos \theta)$. This factor is still determined by relative velocity and whether the motion is towards or away the observer.

Let's see what happens if $\theta=0$. In this case, $\mathbf{k}$ is perpendicular to $\mathbf{v}$. Let's call $\nu_{s}$ the "proper frequency" of the wave, the frequency as measured in the source's frame of reference. The observed frequency $\nu_{obs}$ will be given by
$$\nu_{obs}=\gamma \nu_{s}(1\mp\beta)=\nu_{s} \frac{1\mp \beta}{\sqrt{ 1-\beta ^{2} }}=\nu_{s}\sqrt{ \frac{(1\mp \beta)^{2}}{(1-\beta)(1+\beta)} }=\nu_{s}\sqrt{ \frac{1\mp \beta}{1\pm \beta} }$$
The sign depends on whether the source and observer are getting closer ($+$) or farther ($-$). If they are getting closer, $\nu_{obs}>\nu_{s}$, whereas if they are getting farther, $\nu_{obs}<\nu_{s}$, as we expect. In relativity and most often in astrophysics, these are called **[[Redshift]]** and **blueshift** respectively.