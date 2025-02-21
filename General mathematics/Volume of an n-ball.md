An [[n-ball]] is the $n$-dimensional analog of a [[palla|ball]]. In one dimension, it is a segment. In two, it is a disk. In three it is a proper ball. The volume of an $n$-ball can be calculated generically for any dimension $n$. One way to do so is to recognize that the volume must be proportional to the radius $R$ of the ball to the $n$-th power (for dimensional constraints):
$$V_{n}=c_{n}R^{n}$$
where $c_{n}$ is some scaling constant. The [[Superficie|surface]] of such a ball will be
$$S_{n}=\frac{ \partial V_{n} }{ \partial R } =nc_{n}R^{n-1}$$
which is the surface of the bounding $(n-1)$-dimensional [[hypersphere]]. We can manually calculate these values for two and three dimensions as
$$\begin{align}
\text{(2D)}\quad&V_{2}=\pi R^{2}&S_{2}=2\pi R \\
\text{(3D)}\quad&V_{3}=\frac{4\pi}{3}R^{3}&S_{3}=4\pi R^{2}
\end{align}$$
The trick is to see the following integral:
$$\int_{-\infty}^{\infty} e^{-(x_{1}^{2}+x_{2}^{2}+\ldots+x_{n}^{2})} \ dx_{1}\ldots dx_{n}=\pi^{n/2}=\int_{0}^{\infty}e^{-R^{2}}S_{n}(R)\ dR=nc_{n}\int_{0}^{\infty}e^{-R^{2}}R^{n-1}\ dR$$
The $\pi^{n/2}$ comes by just solving the integral normally. The equality with the second integral comes from doing a coordinate shift to [[Polar coordinates]], introducing the variable $R^{2}=x_{1}^{2}+\ldots+x_{n}^{2}$ and finding that the coordinate change function is exactly $S_{n}(R)$. To determine $c_{n}$, we just need to recognize that the last integral is a [[Gaussian integral]] and, by substituting $R^{2}=t$ and expressing it as a [[Gamma function]], we get
$$V_{n}(R)=\frac{\pi^{n/2}}{\Gamma\left( \frac{n}{2}+1 \right)}R^{n}$$
