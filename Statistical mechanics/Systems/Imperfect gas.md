An **imperfect gas** is a generalization of an [[ideal gas]] which also includes a two-body interaction term. The [[Hamiltonian]] of the [[Physical system|system]] is
$$H=\sum_{i=1}^{N} \frac{\mathbf{p}_{i}^{2}}{2m}+\sum_{i<j}^{N} v_{ij}$$
The second sum is the interaction term. Normally, the interaction depends on the distance between [[Particella|particles]]: $v_{ij}=v(|\mathbf{r}_{i}-\mathbf{r}_{j}|)$.
### In the canonical ensemble
As with the ideal gas, using the [[canonical ensemble]] is convenient. As usual, we want the [[Helmholtz free energy]], which we extract from the [[partition function]] as
$$A=-k_{B}T\ln Z$$
The issue is, as always, figuring out $Z$. Let's write it out explicitly:
$$\begin{align}
Z&=\frac{1}{h^{3N}N!}\int d^{3N}p \int re^{-\beta\left( \sum_{i=1}^{N} \frac{\mathbf{p}_{i}^{2}}{2m}+\sum_{i<j}^{N} v_{ij} \right)} \ d^{3N}q \\
&=\frac{1}{h^{3N}N!}\int d^{3N}p \int re^{-\beta \sum_{i}\mathbf{p}^{2}/2m} \left( e^{-\beta \sum_{i<j}v(r_{ij})}+1-1 \right)d^{3N}q \\
&=\frac{1}{h^{3N}N!}\int d^{3N}p \int \frac{e^{-\sum_{i}\mathbf{p}_{i}^{2}/2m}V^{N}}{V^{N}}\prod_{i<j}(1+f_{ij}) \ d^{3N}q \\
&=\ldots
\end{align}$$
where $f_{ij}(r)=e^{-\beta v(r)-1}$. Continuing:
$$\begin{align}
\ldots&=\frac{1}{h^{3N}N!} \int V^{N}e^{-\sum_{i}\mathbf{p}_{i}^{2}/2m} \ d^{3N}p \int \frac{1}{V^{N}}\prod_{i<j}(1+f_{ij}) \ d^{3N}r \\
&=\frac{1}{h^{3N}N!} V^{N}\left( \int e^{-\beta \mathbf{p}^{2}/2m}d\mathbf{p} \right)^{N}\int \prod_{i=1}^{N} \frac{1}{V^{N}}\prod_{i<j}(1+f_{ij}) d\mathbf{r}  \\
&=\frac{1}{N!}V^{N}\left( \sqrt{ \frac{2mk_{B}T\pi}{h^{2}} } \right)^{3N}\int \prod_{i=1}^{N} \frac{1}{V^{N}} \prod_{i<j}(1+f_{ij})d\mathbf{r} \\
&=\frac{1}{N!}\left( \frac{V}{\lambda ^{3}_{T}} \right)^{N}\int \prod_{i=1}^{N} \frac{1}{V^{N}}\prod_{i<j}(1+f_{ij}) d\mathbf{r} \\
&=\ldots
\end{align}$$
Recall the equation
$$\frac{PV}{Nk_{B}T}=\frac{Pv}{k_{B}T}=\frac{V}{N} \left( \frac{ \partial  }{ \partial v } \ln Z \right)_{T}$$
since $\frac{P}{k_{B}T}=\left( \frac{ \partial  }{ \partial v }\ln Z \right)_{T}$. Also
$$\ln Z=N\ln V-N\ln N-N\ln \lambda ^{3}_{T}+\ln \int \prod_{i=1}^{N} \frac{1}{V^{N}}\prod_{i<j}(1+f_{ij})d\mathbf{q}$$
using [[Stirling's approximation]]. We get
$$\frac{PV}{Nk_{B}T}=\frac{Pv}{k_{B}T}=1+v \frac{ \partial Z }{ \partial v } $$

$$Z=Z(v,T)=\frac{1}{N}\ln\left[ \frac{1}{V^{N}}\int \prod_{i=1}^{N} \prod_{j<k}(1+f_{jk}) \right]=\ldots$$
If $f_{ij}$ is small, we can approximate
$$\prod_{i<j}(1+f_{ij})\simeq 1+\sum_{i<j}f_{ij}$$
$$\begin{align}
\ldots&=\frac{1}{N}\ln\left[ \frac{1}{V^{N}}\int \prod_{i=1}^{N} \left( 1+\sum_{j<k}f_{jk} \right) \right] \\
&=\frac{1}{N}\ln\left[ 1+ \frac{V^{N-2}}{V^{N}}\int f_{12} \frac{N(N-1)}{2}d\mathbf{r}_{1}d\mathbf{r}_{2} \right] \\
&=\frac{1}{N}\ln\left[ 1+ \frac{N(N-1)}{2V}\int f(\mathbf{r})d\mathbf{r} \right] \\
&\simeq \frac{1}{N}\ln\left[ 1+ \frac{N^{2}}{2V}\int f(\mathbf{r})d\mathbf{r} \right]
\end{align}$$
The $v$ derivative is
$$\frac{ \partial Z }{ \partial v } =- \frac{1}{2v^{2}}\int f(\mathbf{r})d\mathbf{r}=- \frac{1}{2v^{2}}\int_{0}^{\infty} 4\pi r^{2}f(r)dr$$
Our equation of state therefore becomes
$$\boxed{\frac{PV}{Nk_{B}T}=1- \frac{1}{2v}\int_{0}^{\infty}4\pi r^{2}f(\mathbf{r})d\mathbf{r}}$$
The negative term is called **second virial coefficient**.
#### Virial expansion
The above result is a special case of a more general case called a **virial expansion**. In it, the equation of state becomes
$$\frac{P}{k_{B}T}=\frac{1}{\lambda ^{3}_{T}}\sum_{l=1}^{\infty} b_{l}z^{l}$$
where each $b_{l}$ are the **virial coefficients**.