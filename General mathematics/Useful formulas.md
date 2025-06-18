---
wiki-publish: true
---
## Trigonometry
$$\sin^{2}(x)+\cos^{2}(x)=1$$
$$\sin(\arctan(x))=\frac{x}{\sqrt{x^{2}+1}}$$
$$\tan^{2}(x)+1=\frac{1}{\cos^{2}(x)}=\sec^{2}(x)$$
## Complex numbers
Modulus of a phase is always one:
$$\lvert e^{\pm i\omega t} \rvert =1$$
## Integrals
Gaussian integral
$$\int_{-\infty}^{\infty} e^{-a(x+b)^{2}} \ dx =\sqrt{ \frac{\pi}{a} },\qquad \int_{0}^{\infty}x^{n}e^{-ax^{2}}\ dx=\frac{1}{2}\left( \frac{1}{a} \right)^{(n+1)/2}\Gamma\left( \frac{n+1}{2} \right)$$
Related
$$\int_{0}^{\infty}x^{n}e^{-ax}dx=\frac{n!}{a^{n+1}}$$
Other
$$\int_{a}^{b} \frac{1}{\sqrt{ x^{2}+y^{2} }} \, dx =\left.{\ln(x+\sqrt{ x^{2}+y^{2} })}\right|_{a}^{b}$$
$$\int_{a}^{b} \frac{1}{(x^{2}+z^{2})^{3/2}} \ dx =\left.{\frac{x}{ z^{2}\sqrt{ x^{2}+z^{2} }}}\right|_{a}^{b}$$
$$\int_{a}^{b} \frac{x}{(x^{2}+z^{2})^{3/2}} \ dx =\left.{-\frac{1}{ \sqrt{ x^{2}+z^{2} }}}\right|_{a}^{b}$$
$$\int_{} \cos ^{2}\theta\ d\theta=\frac{1}{2}(\theta+\sin \theta \cos \theta)+\text{const}$$
### Substitutions
$$x^{2}+y^{2}; \quad x=y\tan(u),\ dx=\frac{y}{\cos^{2}(u)}du \quad \Rightarrow \quad x^{2}+y^{2}=y^{2}(\tan^{2}(u)+1)=\frac{y^{2}}{\cos^{2}(u)}$$
Example:
$$\int \frac{1}{(x^{2}+y^{2})^{3/2}}dx \quad\Rightarrow\quad \int \frac{\cos^{3}(u)}{y^{3}} \frac{y}{\cos^{2}(u)}du=\frac{1}{y^{2}}\int\cos(u)du$$