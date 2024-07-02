The **electric field** $\mathbf{E}$ is the [[Campo vettoriale|vector field]] that describes the action of an [[electric charge]] onto other charges. For a test charge $Q$, the force applied to it by another charged object is determined through the electric field as
$$\mathbf{F}=Q\mathbf{E}$$
### Point charges
Given a system of source point charges $q_{1}$, $q_{2}$, ..., the electric field is the quantity
$$\mathbf{E}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\sum\limits_{i=1}^{n} \frac{q_{i}}{\mathscr{r}_{i}^{2}}\hat{\mathscr{r}}_{i}\quad \left[\frac{\text{N}}{\text{C}}\right]$$
where $\epsilon_{0}$ is the [[Costante dielettrica del vuoto|permittivity of free space]] and $\mathscr{r}_{i}=|\mathbf{r}-\mathbf{r}'|$ is the distance between the $i$-th source charge (at position $\mathbf{r}'$) and the test charge (at position $\mathbf{r}$). $\hat{\mathscr{r}}$ is the unit vector that points from that charge to the test charge.
### Continuous charges
For continues charges, the field is derived by integration as
$$\mathbf{E}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\int \frac{1}{\mathscr{r}^{2}}\hat{\mathscr{r}}dq$$
where the domain of integration is the charge distribution in space. This is expressed in one, two and three dimensions as [[Integrale su una curva|line integrals]], [[Integrale su una superficie|surface integrals]] and volume integrals. 

For a linear charge distribution $dq=\lambda dt'$, with $\lambda$ the linear charge density and $dt'$ the line element onto the charge [[curva|curve]] $\gamma$, we have
$$\mathbf{E}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\int_{\gamma} \frac{\lambda(\mathbf{r}')}{\mathscr{r}^{2}}\hat{\mathscr{r}}dt'$$
For a surface charge distribution $dq=\sigma da'$ with $\sigma$ the surface charge density and $da'$ the area element onto the [[Superficie|surface]] $\Phi$, we have
$$\mathbf{E}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\int_{\Phi}\frac{\sigma(\mathbf{r}')}{\mathscr{r}^{2}}\hat{\mathscr{r}}da'$$
For a volume charge distribution $dq=\rho d\tau'$ with $\rho$ the volume charge density and $d\tau'$ the area element onto the volume $V$, we have
$$\mathbf{E}(\mathbf{r})=\frac{1}{4\pi\varepsilon_{0}}\int_{V}\frac{\rho(\mathbf{r}')}{\mathscr{r}^{2}}\hat{\mathscr{r}}d\tau'$$
In all of the above, $\mathscr{r}$ is the distance between the test charge and the charge object element.