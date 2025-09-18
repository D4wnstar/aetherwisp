---
wiki-publish: true
---
Measuring the [[mean lifetime]] of an object is a very variable task. There's a lot of different objects to measure ([[Particle|particles]], [[Atomic nucleus|nuclei]], [[atom|atoms]], [[Molecule|molecules]]...) as well as enormous jumps in scale (anywhere from $10^{-24}$ seconds to $10^{10}$ years).  There are therefore a number of ways one may go about measuring lifetime.
### Near-stable
If the duration of the measurement is tiny compared to the lifetime ($t\ll \tau$), we're probably dealing with a [[nuclide]] with many tens of thousands of years of lifetime, possible even billions, that decays extremely slowly. There's not much we can do about extended measurements here considering that the sample will outlast humanity a thousand times over, so what we do is rely on the [[radioactive decay law]] and a little approximation. The number of [[Nuclear decay|decays]] in a time interval are
$$\Delta N(t)=N(0)-N(t)=N(0)(1-e^{-t/\tau})\simeq N(0)\left( 1- 1+ \frac{t}{\tau} \right)=\frac{t}{\tau}N(0)$$
We used a first-order expansion of the [[exponential series]] since $t/\tau$ is tiny. Then, assuming we know $N(0)$, can measure the number of decays $N_{D}(t)$ and have good timer for $t$, we get
$$\tau=\frac{N(0)}{\Delta N(t)}t$$
### Manageable lifetime
If the lifetime is comparable to the time we can afford to spend measuring it ($t\sim \tau$), it's a little more involved. In this situation, it's common to get a large sample of the decaying object, separate them to the best of our abilities, keep them trapped at rest and measure the decay time of each individually. Then, join all the measurements in a [[histogram]] to get the lifetime [[Probability distribution|distribution]] and finally find the [[mean]] the old-fashioned way. The histogram should show the radioactive decay law:
$$\frac{dN}{dt}=- \frac{N(0)}{\tau}e^{-t/\tau}$$
from which we can extract $\tau$.

To create the histogram, our instruments require a resolution that's shorter than the lifetime, else we'd just have one big bin with all the measurements. That's not a problem for high lifetimes, in which there's nothing more to talk about, but absolutely is for smaller ones where technology might not be advanced enough to provide good consistent measurements. In the unfortunate latter case, we need to resort to more involved treatment.

What we can do is, instead of trapping the object, we let it move freely for a certain distance before decaying. Then, we construct a histogram as before, but instead of measuring the decay times, we measure the distance covered before decaying. The two quantities are of course related, so if we don't have the tools to measure time we'll measure space instead. As before, the radioactive decay law provides a formula, though we start from decays per unit distance since that's what we binned:
$$\frac{dN}{dx}=\frac{dN}{dt} \frac{dt}{dx}=- \frac{N(0)}{\tau}e^{-t/\tau} \frac{1}{v}$$
Now, if the decaying object has a small enough lifetime to cause issues with modern technology, it's probably a nucleus or subatomic particle. In other words, it's probably moving at relativistic speeds. This matters because we need to take [[time dilation]] into account, since the moving object's [[proper time]] is different from ours. The lifetime is dilated from $\tau$ to $\gamma \tau$ and our formula becomes
$$\frac{dN}{dx}=- \frac{N(0)}{\gamma \tau}e^{-t/\gamma \tau} \frac{1}{\beta c}$$
Using $t=x/v=x/\beta c$ and then the [[mean free path]] $\lambda=\beta c\gamma \tau$ we get
$$\frac{dN}{dx}=- \frac{N(0)}{\lambda}e^{-x/\lambda}$$
Our histogram is now fully converted to spatial data, from which we can extract the mean free path $\lambda$ and from it $\tau$.

> [!example]-
> Say we know $\lambda=30\ \mu\text{m}$ and the particle is going at the [[speed of light]] (e.g. a [[photon]]), so $\beta=1$. Then, solving for $\gamma \tau$ we get
> $$\gamma \tau=\frac{\lambda}{\beta c}=10^{-4}\text{ ns}=10^{-13}\text{ s}$$
> This method allows for measuring very small lifetimes if the particle is moving near the speed of light.
### Extremely unstable
If the object's lifetime is so small there's no way any instrumentation will properly measure it ($t\gg \tau$), we need to use indirect methods. Specifically, we need to analyze the decay products. In particular, we exploit conservation by measuring the [[invariant mass]] of the products. Since the invariant mass is conserved in decays, we can find the invariant mass of the products as a whole and use conservation to state that it's the same as the old one. Now, the [[Disuguaglianza di Heisenberg|uncertainty principle]] gets in the way by forcing an imprecise measurement, so what we actually get is an invariant mass distribution, the peak of which is the invariant mass of the original particle. The width of this distribution provides us with an estimate of the lifetime: it's the [[Breit-Wigner distribution|decay width]] of the [[Breit-Wigner distribution]] for that particle.