**Nöther's theorem** is a fundamental result is physics that relates conserved quantities and [[Simmetria|symmetries]]. It is given in one several statements, depending on the field of physics that one is working in. Most commonly, it is given in the [[Lagrangian]] and [[Hamiltonian]] formalisms of mechanics.

The benefit Nöther's theorem is very practical: constants of motion make solving mechanical systems easier, but they are really difficult to find. Symmetries, on the other hand, are usually readily apparent. Thus, the theorem gives us a *much* easier way to identify constants of motion, which in turn can *greatly* simplify the differential equations that we must solve to find the motion. At heart, the value of Nöther's theorem is that it makes really hard math a little less hard.

> [!info] Nöther's theorem (Lagrangian)
> Let $L$ be a [[Lagrangian]]. Let $q_{n}\to \varphi_{n}(q,\alpha)$ be a continuous [[transformation]]  that's defined and [[Differential|differentiable]] in $\alpha$ in a neighborhood of $\alpha=0$ such that $\varphi_{n}(q,0)=q_{n}$. Moreover, let
> $$\dot{q}_{n}\to \psi_{n}(q,\dot{q},\alpha)=\sum_{k=1}^{n}\frac{ \partial \varphi_{n} }{ \partial q_{k} } \dot{q}_{k}$$
> be a continuous transformation of $\dot{q}$. If, for every choice of $q,\dot{q},\alpha$, we see that $L$ is [[Transformation invariance|invariant under the transformation]]:
> $$L(\varphi(q,\alpha),\psi(q,\dot{q},\alpha),t)=L(q,\dot{q},t)$$
> then the [[dynamical variable]]
> $$\mathcal{P}(q,\dot{q},t)=\sum_{m=1}^{n} \frac{ \partial \varphi_{m} }{ \partial \alpha } (q,0)P_{m}(q,\dot{q},t)$$
> determined from the [[conjugate momenta]] $P_{m}$ is a [[constant of motion]].

More correctly, $\varphi$ and $\psi$ are single-parameter families of [[diffeomorphism|diffeomorphisms]].
### Proof
> [!info] Lagrangian case
> Let $L$ be a Lagrangian that's invariant under the transformations $\varphi$ and $\psi$, so
> $$L(\varphi(q,\alpha),\psi(q,\dot{q},\alpha),t)=L(q,\dot{q},t)$$
> Due to invariance, the derivative over $\alpha$ must be zero:
> $$\left.{\frac{d}{d\alpha}L(\varphi(q,\alpha),\psi(q,\dot{q},\alpha),t)}\right|_{\alpha=0}=0$$
> Now that we have a constraint, we can develop the derivative
> $$\begin{align}
> \frac{d}{d\alpha}L(\varphi(q,\alpha),\psi(q,\dot{q},\alpha),t)&=\left.{\sum_{k=1}^{n} \left[ \frac{ \partial L }{ \partial q_{k} }(\varphi,\psi,t)\frac{ \partial \varphi_{k} }{ \partial \alpha } +\frac{ \partial L }{ \partial \dot{q}_{k} } (\varphi,\psi,t)\frac{ \partial \psi_{k} }{ \partial \alpha }  \right]}\right|_{\alpha=0} \\
> &=\sum_{k=1}^{n} \left[ \frac{ \partial L }{ \partial q_{k} } (q,\dot{q},t)\frac{ \partial \varphi_{k} }{ \partial \alpha } (q,0)+\frac{ \partial L }{ \partial \dot{q}_{k} } (q,\dot{q},t)\frac{ \partial \psi_{k} }{ \partial \alpha } (q,\dot{q},0) \right]
> \end{align}$$
> We evaluate the functions of $q$ and $\dot{q}$ on solutions of the [[Lagrange equation]]. We get
> $$\begin{align}
> 0&=\sum_{k=1}^{n} \left[ \frac{ \partial L }{ \partial q_{k} } (q(t),\dot{q}(t),t)\frac{ \partial \varphi_{k} }{ \partial \alpha } (q(t),0)+\frac{ \partial L }{ \partial \dot{q}_{k} } (q(t),\dot{q}(t),t)\frac{ \partial \psi_{k} }{ \partial \alpha } (q(t),\dot{q}(t),t) \right]
> \end{align}$$
> To further compress the equation, we notice that the derivatives of $L$ collectively make a [[total derivative]] of $L$ in time. The same thing happens on $\varphi$ once we notice that
> $$\frac{ \partial \psi_{k} }{ \partial \alpha } (q(t),\dot{q}(t),t)=\sum_{l=1}^{n} \frac{ \partial  }{ \partial q_{l} } \left( \frac{ \partial \varphi }{ \partial \alpha } \dot{q}_{l} \right)=\frac{d}{dt} \frac{ \partial \varphi }{ \partial \alpha } (q(t),0)$$
> We can now state
> $$0=\frac{d}{dt} \left[ \sum_{k=1}^{n} \frac{ \partial L }{ \partial \dot{q}_{k} } (q(t),\dot{q}(t),t)\frac{ \partial \varphi_{k} }{ \partial \alpha } (q(t),0) \right]$$
> (Remember that this is true specifically for $q(t)$ that solve the system). But $\frac{ \partial L }{ \partial \dot{q}_{k} }=P_{l}$ are just the conjugate momenta. We call the entire term in brackets $\mathcal{P}$ and, since its time derivative is zero, it is a constant of motion.
> $$\boxed{\frac{d}{dt} \mathcal{P}=0\quad\Rightarrow \quad \mathcal{P}\text{ is a constant of motion}}$$
### Conservations
Nöther's theorem is truly general and can be applied to any continuous transformation, so long there's a Lagrangian that's invariant under it. However, some classes of transformations are very special: they are known to conserve very important physical quantities and are therefore of particular interest. Namely, the big ones are the following three:
- Invariance under spatial shifts is conservation of [[linear momentum]].
- Invariance under [[Rotation|rotations]] is conservation of [[angular momentum]].
- Invariance under temporal shifts is conservation of [[energy]].

The first two are axis-dependent: linear momentum is conserved over the axis of the shift, and angular momentum is conserved over the axis of rotation. Time is one dimensional has no axis: if a system is time-invariant, it conserves energy. The critical point here is, I suppose, the reverse. We know that the Universe as a whole abides by conservation of energy: clearly, then, it must be time-invariant.
### Examples
> [!example] Harmonic oscillator
> We know the [[harmonic oscillator]] has a constant of motion, so let's test the theorem out on it. The Lagrangian is
> $$L(q_{1},q_{2},\dot{q}_{1},\dot{q}_{2})=\frac{m}{2}(\dot{q}_{1}^{2}+\dot{q}_{2}^{2})- \frac{m\omega ^{2}}{2}(q_{1}^{2}+q_{2}^{2})$$
> The transformations we choose is the rotation in the plane of motion:
> $$\begin{pmatrix}
> q_{1} \\
> q_{2}
> \end{pmatrix}\to \begin{pmatrix}
> \cos \alpha & -\sin \alpha \\
> \sin \alpha & \cos \alpha
> \end{pmatrix}\begin{pmatrix}
> q_{1} \\
> q_{2}
> \end{pmatrix}=\begin{pmatrix}
> q_{1}\cos \alpha-q_{2}\sin \alpha \\
> q_{1}\sin \alpha+q_{2}\cos \alpha
> \end{pmatrix}$$
> $$\begin{pmatrix}
> \dot{q}_{1} \\
> \dot{q}_{2}
> \end{pmatrix}\to\begin{pmatrix}
> \cos \alpha & -\sin \alpha \\
> \sin \alpha & \cos \alpha
> \end{pmatrix}\begin{pmatrix}
> \dot{q}_{1} \\
> \dot{q}_{2}
> \end{pmatrix}=\begin{pmatrix}
> \dot{q}_{1}\cos \alpha-\dot{q}_{2}\sin \alpha \\
> \dot{q}_{1}\sin \alpha+\dot{q}_{2}\cos \alpha
> \end{pmatrix}$$
> We then apply these to the Lagrangian:
> $$\begin{align}
> L(\varphi(q,\alpha),\psi(q,\dot{q},\alpha))&=\frac{m}{2}[(\dot{q}_{1}\cos \alpha-\dot{q}_{2}\sin \alpha)^{2}+(\dot{q}_{1}\sin \alpha+\dot{q}_{2}\cos \alpha)^{2}]- \frac{m\omega ^{2}}{2}[(q_{1}\cos \alpha-q_{2}\sin \alpha)^{2}+(q_{1}\sin \alpha+q_{2}\cos \alpha)^{2}] \\
> &=\frac{m}{2}[\dot{q}_{1}^{2}+\dot{q}_{2}^{2}]- \frac{m\omega ^{2}}{2}[q_{1}^{2}+q_{2}^{2}] \\
> &=L(q,\dot{q})
> \end{align}$$
> Clearly, then, the Lagrangian is invariant under $(\varphi,\psi)$. This grants us permission to invoke Nöther's theorem:
> $$\mathcal{P}=\left.{(-q_{1}\sin \alpha-q_{2}\cos \alpha,q_{1}\cos \alpha-q_{2}\sin \alpha)}\right|_{\alpha=0}\begin{pmatrix}
> m \dot{q}_{1} \\
> m \dot{q}_{2}
> \end{pmatrix}=m(q_{1}\dot{q}_{2}-q_{2}\dot{q}_{1})$$
> This must be a constant of motion. Since the system is easy, we might as well double check that this is actually a constant. To do so, we need to evaluate it over the motion, which in turn requires us to know $q_{1}$, $q_{2}$, $\dot{q}_{1}$ and $\dot{q}_{2}$. These are
> $$q_{1}(t)=A_{1}\sin(\omega t+\phi_{1}),\quad q_{2}(t)=A_{2}\sin(\omega t+\phi_{2})$$
> $$\dot{q}_{1}(t)=A_{1}\omega \cos(\omega t+\phi_{1}),\quad \dot{q}_{2}(t)=A_{2}\omega \cos(\omega t+\phi_{2})$$
> Plug these into $\mathcal{P}$ and we see
> $$\mathcal{P}=m\omega A_{1}A_{2}[\sin(\omega t+\phi_{1})\cos(\omega t+\phi_{2})-\sin(\omega t+\phi_{2})\cos(\omega t+\phi_{1})]$$
> Using the trig identity $\sin \alpha \cos \beta-\cos \alpha \sin \beta=\sin(\alpha-\beta)$ we notice that $\omega t$ cancels out and we're left with
> $$\mathcal{P}=m\omega A_{1}A_{2}\sin(\phi_{1}-\phi_{2})$$
> But this is all time-independent. Clearly then, it is a constant of motion, which confirms that Nöther's theorem was correct all along.
> 
> While it's nice to have an abstract constant, it would be nice if we could understand what we're looking at. To do so, rewrite $\mathcal{P}$ with the [[Tensore di Levi-Civita|Levi-Civita tensor]]:
> $$\mathcal{P}=m(q_{1}\dot{q}_{2}-q_{2}\dot{q}_{1})=m\sum_{i,j=1}^{3} q_{i}q_{j}\varepsilon_{ij3}=m(\mathbf{q}\times \dot{\mathbf{q}})_{3}=M_{3}$$
> But this is just the definition of [[angular momentum]]. Evidently, then, what we're trying to say is the harmonic oscillator conserves the component of the angular momentum over the axis of rotation.
