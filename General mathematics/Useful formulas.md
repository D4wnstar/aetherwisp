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
**Gaussian integral**
$$\int_{-\infty}^{\infty} e^{-a(x+b)^{2}} \ dx =\sqrt{ \frac{\pi}{a} },\qquad \int_{0}^{\infty}x^{n}e^{-ax^{2}}\ dx=\frac{1}{2}\left( \frac{1}{a} \right)^{(n+1)/2}\Gamma\left( \frac{n+1}{2} \right)$$
**Related**
$$\int_{0}^{\infty}x^{n}e^{-ax}dx=\frac{n!}{a^{n+1}}$$
**Trigonometry**
Useful formulas
$$\sin ^{2}\theta+\cos ^{2}\theta=1,\quad \cos ^{2}\theta=\frac{1+\cos(2\theta)}{2},\quad\sin ^{2}\theta=\frac{1-\cos(2\theta)}{2}
$$
Most trig integrals are solved by some combination of the above formulas, substitution and integration by parts. In integrals with only sines and cosines:
- if both powers are odd (e.g. $\cos^{2}\theta \sin^{2}\theta d\theta$) then use the double angle identities above to reduce the integrand (e.g. in this case $\sin ^{2}\theta \cos ^{2}\theta=(1-\cos(4\theta))/8$).
- if one power is odd (e.g. $\cos ^{2}\theta \sin \theta d\theta$), substitute the even trig function and solve (e.g. in this case $u=\cos \theta$ which makes $du=-\sin \theta d\theta$ and so $-u^{2}du$).
- if you have a product with different arguments (e.g $\cos(4\theta)\cos \theta$), complex definitions of sine and cosine can be used to convert the product into a sum (or memorize the product-to-sum formulas): $\cos \theta=(e^{i\theta}+e^{-i\theta})/2$ and $\sin \theta=(e^{i\theta}-e^{-i\theta})/2i$.

$$\int \cos ^{2}\theta\ d\theta=\frac{1}{2}(\theta+\sin \theta \cos \theta)+\text{const}$$
**Other**
$$\int_{a}^{b} \frac{1}{\sqrt{ x^{2}+y^{2} }} \, dx =\left.{\ln(x+\sqrt{ x^{2}+y^{2} })}\right|_{a}^{b}$$
$$\int_{a}^{b} \frac{1}{(x^{2}+z^{2})^{3/2}} \ dx =\left.{\frac{x}{ z^{2}\sqrt{ x^{2}+z^{2} }}}\right|_{a}^{b}$$
$$\int_{a}^{b} \frac{x}{(x^{2}+z^{2})^{3/2}} \ dx =\left.{-\frac{1}{ \sqrt{ x^{2}+z^{2} }}}\right|_{a}^{b}$$
### Substitutions
$$x^{2}+y^{2}; \quad x=y\tan(u),\ dx=\frac{y}{\cos^{2}(u)}du \quad \Rightarrow \quad x^{2}+y^{2}=y^{2}(\tan^{2}(u)+1)=\frac{y^{2}}{\cos^{2}(u)}$$
Example:
$$\int \frac{1}{(x^{2}+y^{2})^{3/2}}dx \quad\Rightarrow\quad \int \frac{\cos^{3}(u)}{y^{3}} \frac{y}{\cos^{2}(u)}du=\frac{1}{y^{2}}\int\cos(u)du$$