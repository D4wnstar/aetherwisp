---
aliases:
  - Mayer function
---
An **interacting gas** is a generalization of an [[ideal gas]] which also includes a two-body interaction term. The [[Hamiltonian]] of the [[Physical system|system]] is
$$H=\sum_{i=1}^{N} \frac{\mathbf{p}_{i}^{2}}{2m}+\sum_{i<j} u_{ij}$$
The second sum represents the interaction as a sum of interparticle [[Potenziale|potentials]] $u_{ij}$. Normally, the interaction depends on the distance between [[Particella|particles]]: $u_{ij}\propto |\mathbf{r}_{i}-\mathbf{r}_{j}|$.
### Using cluster integrals
Our goal is to find an [[equation of state]] similar to the ideal gas one, that is $PV=Nk_{B}T$, so that we can compare the two. We'll do this by using a [[canonical ensemble]], for which
$$\frac{PV}{Nk_{B}T}=v \frac{ \partial  }{ \partial v } \ln Q_{N}\tag{1}$$
where $v=V/N$. The issue is, as always, figuring out the [[Partition function|canonical partition function]] $Q_{N}$. Let's write it out explicitly:
$$\begin{align}
Q_{N}&=\frac{1}{h^{3N}N!}\int d^{3N}p \int e^{-\beta\left( \sum_{i=1}^{N} \frac{\mathbf{p}_{i}^{2}}{2m}+\sum_{i<j} u_{ij} \right)} \ d^{3N}r \\
&=\frac{1}{h^{3N}N!}\int e^{-\beta \sum_{i}\mathbf{p}^{2}/2m} d^{3N}p \int  e^{-\beta \sum_{i<j}u_{ij}}\ d^{3N}r \\
&=\ldots
\end{align}$$
The integral on the left is the usual momentum integral that's common to all ideal gases. Including the $h^{3N}$, it evaluates to $1/\lambda ^{3N}$ , using the [[Formula di de Broglie|de Broglie thermal wavelength]] $\lambda$. Using $e^{\sum n}=\prod e^{n}$, we can write
$$\begin{align} \\
\ldots&=\frac{1}{\lambda^{3N}N!}\int \prod_{i<j}e^{-\beta u_{ij}} \\
&=\frac{1}{\lambda^{3N}N!}\int \prod_{i<j}(1+e^{-\beta u_{ij}}-1) \\
&=\frac{1}{\lambda^{3N}N!} \int \prod_{i<j}(1+f_{ij}) \ d^{3N}r \\
\end{align}$$
Where we defined the **Mayer function** $f_{ij}(r)=e^{-\beta u_{ij}}-1$. The integral we have left is generally referred to as the **configuration integral** $Z_{N}$ of the system. For non-interacting particles, the Mayer function is zero and the integral is just the [[measure]] of the space occupied by the system to the $N$-th power, i.e. $V^{N}$. In that case, we just find our usual $Q_{N}=V^{N}/(\lambda ^{3N}N!)$. This shows that the ideal gas really is just a specific case of the interacting gas.

When the particles do interact, the Mayer function describes how they do so. Its utility lies in the fact that at high [[temperature|temperatures]], it is a very small number and can therefore be expressed in an approximate form with little error. The following is a typical shape for an interparticle potential of effective range $r_{0}$.

![[Mayer function and distance.png]]
*From Pathria & Beale's Statistical Mechanics, 3rd ed., page 301*

We can modify the partition function as follows:
$$Q_{N}=\frac{V^{N}}{\lambda^{3N}N!}\int\frac{1}{V^{N}} \prod_{i=1}^{N} \prod_{i<j}(1+f_{ij})d\mathbf{r}=\frac{V^{N}}{\lambda ^{3N}N!}Z_{N}$$
We multiplied and divided by $V^{N}$ and noticed that the position integrals over $d^{3N}r$ are actually $N$ almost identical integrals over $d^{3}r=d\mathbf{r}$, each with a different $i$. We also included $1/V^{N}$ in $Z_{N}$. Using [[Stirling's approximation]]:
$$\ln Q_{N}=N\ln V-N\ln N-N\ln \lambda ^{3}+\ln Z_{N}$$
The derivative is
$$v\frac{ \partial  }{ \partial v } \ln Q_{N}=N+v\frac{ \partial  }{ \partial v } \ln Z_{N}$$
If we put this in $(1)$ we get (???)
$$\frac{PV}{Nk_{B}T}=1+v \frac{ \partial Z_{N} }{ \partial v }$$
If we solve $Z_{N}$ and take the derivative we are done. As mentioned before, $f_{ij}$ is small for large temperatures, so
$$\prod_{i<j}(1+f_{ij})\simeq 1+\sum_{i<j}f_{ij}$$
Using this approximation we find
$$\begin{align}
Z_{N}&=\frac{1}{N}\ln\left[ \frac{1}{V^{N}}\int \prod_{i=1}^{N} \prod_{j<k}(1+f_{jk}) \right] \\
&\simeq\frac{1}{N}\ln\left[ \frac{1}{V^{N}}\int \prod_{i=1}^{N} \left( 1+\sum_{j<k}f_{jk} \right) \right] \\
&=\frac{1}{N}\ln\left[ 1+ \frac{V^{N-2}}{V^{N}}\int f_{12} \frac{N(N-1)}{2}d\mathbf{r}_{1}d\mathbf{r}_{2} \right] \\
&=\frac{1}{N}\ln\left[ 1+ \frac{N(N-1)}{2V}\int f(\mathbf{r})d\mathbf{r} \right] \\
&\simeq \frac{1}{N}\ln\left[ 1+ \frac{N^{2}}{2V}\int f(\mathbf{r})d\mathbf{r} \right]
\end{align}$$
The $v$ derivative is
$$\frac{ \partial Z }{ \partial v } =- \frac{1}{2v^{2}}\int f(\mathbf{r})d\mathbf{r}=- \frac{1}{2v^{2}}\int_{0}^{\infty} 4\pi r^{2}f(r)dr$$
Our equation of state therefore becomes
$$\boxed{\frac{PV}{Nk_{B}T}=1- \frac{1}{2v}\int_{0}^{\infty}4\pi r^{2}f(r)dr}$$
The negative term is called **second virial coefficient**.
#### Virial expansion
The above result is a special case of a more general case called a **virial expansion**. In it, the equation of state becomes
$$\frac{P}{k_{B}T}=\frac{1}{\lambda ^{3}_{T}}\sum_{l=1}^{\infty} b_{l}z^{l}$$
where each $b_{l}$ are the **virial coefficients**.