---
wiki-publish: true
---
The **Hamilton-Jacobi equation** (or **HJ equation**) is the equation
$$H\left( \frac{ \partial F_{2} }{ \partial q } (\tilde{\mathbf{p}},\mathbf{q},t),\mathbf{q},t \right)+\frac{ \partial F_{2} }{ \partial t } (\tilde{\mathbf{p}},\mathbf{q})=0$$
where $H$ is a [[Hamiltonian]] and $F_{2}$ is a [[Generating function (physics)|generating function]] of the second kind. Solving the HJ equation implies finding $F_{2}$, which is generates a [[canonical transformation]] that conjugates $H$ into $K=0$. Since the Hamiltonian $K=0$ is trivial to solve, leading to [[Constant of motion|constants of motion]], it automatically also solves the original system by transforming those constants back into the original system of $H$. It is an alternative way of solving for motion.
### Derivation
A [[canonical transformation]] $(u,v)$ conjugates the Hamiltonian $H(\mathbf{p},\mathbf{q},t)$ into
$$K(\tilde{\mathbf{p}},\tilde{\mathbf{q}},t)=H(u(\tilde{\mathbf{p}},\tilde{\mathbf{q}},t),v(\tilde{\mathbf{p}},\tilde{\mathbf{q}},t),t)+\frac{ \partial F_{2} }{ \partial t } (\tilde{\mathbf{p}},v(\tilde{\mathbf{p}},\tilde{\mathbf{q}},t),t)\tag{1}$$
where $F_{2}$ is a [[Generating function (physics)|generating function]] of the second kind. An important problem to solve (you'll see why in a moment) is this:

> Given some Hamiltonian $H$, what canonical transformation, if any, conjugates $H$ into $K=0$?

Say we have somehow found such a transformation. Its functions $\mathbf{p}=u(\tilde{\mathbf{p}},\tilde{\mathbf{q}},t)$ and $\mathbf{q}=v(\tilde{\mathbf{p}},\tilde{\mathbf{q}},t)$ conjugate $H$ into $K=0$. But if $K=0$, the [[Hamilton equations]] of the transformed system are *trivial*:
$$\left\{\begin{align}
&\dot{\tilde{p}}_{i}=-\frac{ \partial K }{ \partial \tilde{q}_{i} } =0 \\
&\dot{\tilde{q}}_{i}=\frac{ \partial K }{ \partial \tilde{p}_{i} } =0
\end{align}\right.$$
But if the derivatives to $\tilde{\mathbf{p}}$ and $\tilde{\mathbf{q}}$ are zero, then both must be *[[Constant of motion|constants of motion]]*:
$$\tilde{\mathbf{p}}(t)=\tilde{\mathbf{p}}_{0},\quad \tilde{\mathbf{q}}(t)=\tilde{\mathbf{q}}_{0}$$
The original motion $\mathbf{p}(t)$ and $\mathbf{q}(t)$ is then trivially solved by functions of constants and time:
$$\mathbf{p}(t)=u(\tilde{\mathbf{p}}_{0},\tilde{\mathbf{q}}_{0},t),\quad \mathbf{q}(t)=v(\tilde{\mathbf{p}}_{0},\tilde{\mathbf{q}}_{0},t)$$
This can be done as long as we have some way to find $F_{2}$, the transformation that leads to this. Looking at $(1)$, setting $K=0$ and expressing the transformation functions $(u,v)$ in its terms, we see that $F_{2}$ must satisfy
$$\boxed{H\left( \frac{ \partial F_{2} }{ \partial q } (\tilde{\mathbf{p}},\mathbf{q},t),\mathbf{q},t \right)+\frac{ \partial F_{2} }{ \partial t } (\tilde{\mathbf{p}},\mathbf{q})=0}$$
If $F_{2}$ satisfies this equation, then it conjugates $H$ into $K=0$ and we basically solved the system. This equation is called the **Hamilton-Jacobi equation**.
### Examples
> [!example] Harmonic oscillator
> As usual, we solve the [[harmonic oscillator]]. The Hamiltonian is
> $$H=\frac{1}{2m}(p^{2}+m^{2}\omega ^{2}q^{2})$$
> which makes the HJ equation into
> $$\frac{1}{2m}\left[ \left( \frac{ \partial F_{2} }{ \partial q } \right)^{2}+m^{2}\omega ^{2}q^{2} \right]+\frac{ \partial F_{2} }{ \partial t } =0$$
> $H$ is not time-dependent: this suggests a solution of the form
> $$F_{2}(\tilde{p},q,t)=W(\tilde{p},q,t)-a(\tilde{p})t$$
> Substitute this in HJ to get an equation for $W$
> $$\frac{1}{2m}\left[ \left( \frac{ \partial W }{ \partial q }  \right)^{2}+m^{2}\omega ^{2}q^{2} \right]=a(\tilde{p})$$
> We will pick a $\tilde{p}$ such that $a(\tilde{p})=\omega \tilde{p}$. This way we find
> $$\left( \frac{ \partial W }{ \partial t }  \right)^{2}=2m\omega \tilde{p}-m^{2}\omega ^{2}q^{2}$$
> Integrating twice yields
> $$W(\tilde{p},q)=\sqrt{ 2m\omega \tilde{p} }\int_{q_{0}}^{q}\sqrt{ 1- \frac{m\omega q'^{2}}{2\tilde{p}} }dq'=\int_{q_{0}}^{q}\sqrt{ 2m\omega \tilde{p} - m^{2}\omega ^{2}q^{2}}dq'$$
> We *could* attempt to solve the integral, but it doesn't matter: we only care about the derivatives of $F_{2}=W(\tilde{p},q)-\omega \tilde{p}t$, so the integral will disappear anyway. In fact:
> $$p=\frac{ \partial F_{2} }{ \partial q } =\sqrt{ 2m\omega \tilde{p} }\sqrt{ 1- \frac{m\omega q^{2}}{2\tilde{p}} }$$
> $$\begin{align}
> \tilde{q}&=\frac{ \partial F_{2} }{ \partial \tilde{p} } =\int_{q_{0}}^{q} \frac{2m\omega}{2\sqrt{ 2m\omega \tilde{p}-m^{2}\omega ^{2}q'^{2} }} dq'-\omega t \\
> &=\sqrt{ \frac{m\omega}{2\tilde{p}} }\int_{q_{0}}^{q} \frac{dq'}{\sqrt{ 1- \frac{m\omega}{2\tilde{p}} }}-\omega t \\
> \left ( \text{sub: }x\equiv \sqrt{ \frac{m\omega}{2\tilde{p}} }q' \right)&=\int_{\sqrt{ m\omega/2\tilde{p} }\ q_{0}}^{\sqrt{ m\omega/2\tilde{p} }\ q} \frac{ dx}{\sqrt{ 1-x^{2} }}-\omega t \\
> &=\arcsin\left( \sqrt{ \frac{m\omega}{2\tilde{p}} }q \right)-\tilde{q}_{c}-\omega t
> \end{align}$$
> Inverting $\tilde{q}$ gives
> $$q=\sqrt{ \frac{2\tilde{p}}{m\omega} }\sin(\tilde{q}+\tilde{q}_{c}+\omega t)$$
> Put this in $p$ to get
> $$p=\sqrt{ 2m\omega \tilde{p} }\sqrt{ 1-\sin ^{2}(\tilde{q}+\tilde{q}_{c}+\omega t) }=\sqrt{ 2m\omega \tilde{p} }\cos(\tilde{q}+\tilde{q}_{c}+\omega t)$$
> The conjugate Hamiltonian for $F_{2}$ is $K=0$ so as we said $\tilde{p}(t)=\tilde{p}_{0}$ and $\tilde{q}(t)=\tilde{q}_{0}$. Put these in $p$ and $q$ to get the motion $p(t)$ and $q(t)$:
> $$p(t)=\sqrt{ 2m\omega \tilde{p}_{0} }\cos(\omega t+\tilde{q}_{0}'),\quad q(t)=\sqrt{ \frac{2\tilde{p}_{0}}{m\omega} }\sin(\omega t+\tilde{q}_{0}')$$
> where $\tilde{q}_{0}'\equiv \tilde{q}_{0}+\tilde{q}_{c}$. These are the usual harmonic oscillator solutions.

