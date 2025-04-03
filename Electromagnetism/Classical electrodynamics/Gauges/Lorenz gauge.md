The **Lorenz gauge** is an electrodynamic [[gauge]] for [[Maxwell's equations]] where we set the [[divergence]] of the [[magnetic vector potential]] to
$$\nabla\cdot \mathbf{A}=-\mu_{0}\varepsilon_{0}\frac{ \partial V }{ \partial t } $$
The benefit of this specific choice is that it cancels out two terms in the potential formulation of Maxwell's equations. The differential equation for $\mathbf{A}$ then is
$$\nabla ^{2}\mathbf{A}-\mu_{0}\varepsilon_{0}\frac{ \partial ^{2}\mathbf{A} }{ \partial t^{2} } =-\mu_{0}\mathbf{J}$$
and the one for $V$ is
$$\nabla ^{2}V-\mu_{0}\varepsilon_{0}\frac{ \partial ^{2}V }{ \partial t^{2} } =- \frac{\rho}{\varepsilon_{0}}$$
The benefit of the Lorenz gauge is that it makes the equations for $V$ and $\mathbf{A}$ virtually identical; this can be rendered obvious by using the [[d'Alembertian]] operator $\square ^{2}$:
$$\square ^{2}V=- \frac{\rho}{\varepsilon_{0}},\quad\square ^{2}\mathbf{A}=-\mu_{0}\mathbf{J}$$
These two are inhomogeneous [[wave equation|wave equations]] $\square ^{2} \psi=f$. $f$ can be interpreted as a *source* term that's responsible for generating the [[electromagnetic wave]], and in this gauge, the entirety of electrodynamics can be regarded as just the solution to these two equations (plus boundary conditions); everything else follows.

They also make the connection to electro/magnetostatics very clear: if we take away time dependence, the d'Alembertian becomes the [[Laplacian]] and the our two equations become the usual
$$\nabla ^{2}V=- \frac{\rho}{\varepsilon_{0}},\quad \nabla ^{2}\mathbf{A}=-\mu_{0}\mathbf{J}$$
