**Electromagnetic induction** is a phenomenon occurring in electrodynamics that can be summarized as follows:

> **A changing magnetic field induces an electric field.**

> **A changing electric field induces a magnetic field.**
### Induced electric field
This [[electric field]] is determined much in the same way as the magnetostatic field, by way of its [[Curl]]:
$$\nabla\cdot\mathbf{E}=0,\quad \nabla\times\mathbf{E}=- \frac{ \partial \mathbf{B} }{ \partial t } $$
These are mathematically equivalent restrictions as those put on the magnetic field, just with $\mu_{0}\mathbf{J}$ changed to $-\frac{ \partial \mathbf{B} }{ \partial t }$. We can even find an analog for the [[Biot-Savart law]] with
$$\mathbf{E}=- \frac{1}{4\pi}\int \frac{1}{\mathfrak{r}^{2}}\left( \frac{ \partial \mathbf{B} }{ \partial t } \times \hat{\boldsymbol{\mathfrak{r}}} \right)\ d\tau=- \frac{1}{4\pi} \frac{ \partial  }{ \partial t } \int \frac{\mathbf{B}\times \hat{\boldsymbol{\mathfrak{r}}}}{\mathfrak{r}^{2}}\ d\tau  $$
Notably, unlike the Biot-Savart law, this works even for time-dependent currents. This implies we can use [[Ampere's law]] in the same way we can for magnetic fields too:
$$\oint \mathbf{E}\cdot d\mathbf{r}=- \frac{d\Phi}{dt}$$
where the quantity passing through the loop is now the change of magnetic flux instead of $\mu_{0}I_\text{enc}$.
### Induced magnetic field
For the discovery and derivation of the induced magnetic field, see [[Ampere's law#In electrodynamics]].