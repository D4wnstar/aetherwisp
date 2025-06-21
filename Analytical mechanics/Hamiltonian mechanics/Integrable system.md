---
wiki-publish: true
---
A [[Hamilton equations|Hamiltonian system]] of $n$ [[degrees of freedom]] is said to be **integrable** if there exists a [[canonical transformation]] $p_{i}=u_{i}(J,\psi)$ and $q_{j}=v_{j}(J,\psi)$ with functions $u$ and $v$ periodic in the coordinates $\psi_{i}$ and $(J,\psi)\equiv(J_{1},\ldots,J_{n},\psi_{1},\ldots,\psi_{n})\in \mathbb{R}^{n}\times T^{n}$ such that the conjugate Hamiltonian of $H(\mathbf{p},\mathbf{q})$ is a function $K$ that depends only on $J$, that is $K\equiv K(J)$. $(J,\psi)$ are known as the **[[action-angle variables]]** and $T^{n}$ is an $n$-dimensional [[torus]].

In the action-angle variables, the [[Hamilton equations]] become
$$\left\{\begin{align}
&\dot{J}_{i}=0 \\
&\dot{\psi}_{i}=\frac{ \partial K }{ \partial J_{i} } \equiv \omega_{i}(J)
\end{align}\right.$$
The variables $J_{i}(t)=J_{i}^{0}$ are [[Constant of motion|constants of motion]] and are said to be **in involution**, which means $\{ J_{i},J_{j} \}=0$ for all $i,j$. The variables $\psi_{i}(t)=\omega_{i}(J^{0})t+\psi_{0}$ are [[Lagrangian|cyclical coordinates]].

Since $\psi$ are defined on a torus $T^{n}$, they are angles of period $2\pi$. The motion variables $\psi_{i}(t)$ are therefore angles of period $T_{i}=2\pi/\omega_{i}(J)$.

In an integrable system, trajectories in [[phase space]] are **limited** and **quasi-periodic**. They exists on the [[level set|level sets]] $J_{i}(t)=J_{i}^{0}$ and are [[circle|circles]] in the directions $\psi_{i}$. Each of these levels sets is a copy of $T^{n}$ and trajectories are curves in $T^{n}$. Also, since trajectories are independent of the coordinate system that is used to describe them, the $(p,q)$ coordinates are also limited and quasi-periodic.

> [!info] Integrability condition
> Let $H$ be the Hamiltonian for a system with $n$ degrees of freedom. Assume that there exist $n$ constants of motion $f_{i}(\mathbf{p},\mathbf{q})$ all independent and in involution, so that $\{ f_{i},f_{j} \}=0$ for all $i,j$. Also assume that for some $\mathbf{a}\in \mathbb{R}^{n}$, the level set $M_{\mathbf{a}}=\{ f_{i}(\mathbf{p},\mathbf{q})=a_{i} \}$ is compact and connected. Then, the system is integrable.
> 

$M_{\mathbf{a}}$ is parameterized by the angles $\psi_{i}$. By varying $\psi_{i}$ you obtain a [[curve]] $\gamma_{i}$ in $M_{\mathbf{a}}$. The action variables are defined by
$$J_{i}=\frac{1}{2\pi}\oint_{\gamma_{i}}\sum_{k=1}^{n}p_{k}dq_{k}$$
These are only dependent on the constants of motion $f_{i}$ are independent and in involution. It can be proven that the variables that are conjugated to the $J_{i}$ are angles of period $2\pi$.
### Use case
Many integrable systems (such as the ones below) are plenty easily solved without even invoking Hamiltonian mechanics (i.e. using a [[Lagrangian]] instead). Furthermore, most systems in nature are not integrable. It is therefore fair to ask why even bother with all of this (evidently difficult) formalism. The answer is that it is very common to be able to *approximate* a non-integrable system into an integrable one, and Hamiltonian mechanics becomes quite useful when dealing with these approximations (using [[Teoria delle perturbazioni|perturbation theory]]).
### Examples
- [[Central potential problems]]. A body in a [[vector field]] of central [[force|forces]] with [[potential]] $V\equiv V(r)$ in $\mathbb{R}^{3}$ ($n=3$) is an integrable system. There exist three constants of motion in involution: $\{ H,L_{z} \}=0$, $\{ H,L^{2} \}=0$ and $\{ L_{z},L^{2} \}=0$ where $\mathbf{L}$ is the [[angular momentum]].
- A [[spinning top]] ($n=3$). The three constants of motion are $\{ H,p_{\varphi} \}=0$, $\{ H,p_{\psi} \}=0$ and $\{ p_{\varphi},p_{\psi} \}=0$.
- All one-dimensional systems ($n=1$) with a time-independent Hamiltonian. There is one constant of motion and it's the Hamiltonian itself.

> [!example] Point mass in Keplerian potential
> In [[spherical coordinates]], the Hamiltonian is
> $$H(p_{r},p_{\theta},p_{\varphi},r,\theta,\varphi)=\frac{1}{2m}\left( p_{r}^{2}+ \frac{p_{\theta}^{2}}{r^{2}}+ \frac{p_{\varphi}^{2}}{r^{2}\sin ^{2}\theta} \right)- \frac{k}{r}$$
> The Hamilton equations yield
> $$\dot{p}_{r}=\frac{1}{m} \frac{p_{\varphi}^{2}}{r^{3}\sin ^{2}\theta}- \frac{k}{r^{2}},\quad \dot{p}_{\theta}=\frac{1}{m} \frac{p_{\varphi}^{2}}{r^{2}\sin ^{3}\theta}\cos \theta,\quad \dot{p}_{\varphi}=0$$
> $$\dot{r}=\frac{p_{r}}{m},\quad \dot{\theta}=\frac{p_{\theta}}{mr^{2}},\quad \dot{\varphi}=\frac{p_{\varphi}}{mr^{2}\sin ^{2}\theta}$$
> The constants of motion are $H$, $L^{2}$ and $L_{z}$.
> $$\begin{align}
> L^{2}&=\lvert \mathbf{r}\times \mathbf{p} \rvert ^{2}=\left\lvert  r\mathbf{e}_{r}\times\left( p_{r}\mathbf{e}_{r}+ \frac{p_{\theta}}{r}\mathbf{e}_{\theta}+ \frac{p_{\varphi}}{r\sin \theta} \mathbf{e}_{\varphi}\right)  \right\rvert ^{2}=\left\lvert  -r \frac{p_{\theta}}{r}\mathbf{e}_{\varphi} +r \frac{p_{\varphi}}{r\sin \theta}\mathbf{e}_{\theta}  \right\rvert^{2} \\
> &=p_{\theta}^{2}+ \frac{p_{\varphi}^{2}}{\sin ^{2}\theta}
> \end{align} $$
> $$L_{z}=\left( -p_{\theta}\mathbf{e}_{\varphi}+ \frac{p_{\varphi}}{\sin \theta}\mathbf{e}_{\theta} \right)\cdot \mathbf{e}_{3}=\frac{p_{\varphi}}{\sin \theta}\cos\left( \frac{\pi}{2}-\theta \right)=p_{\varphi}$$
> We can rename the constants as $(L^{2},L_{z},H)\mapsto(l,l_{z},E)$. The action variables will be functions of these constants. We consider the level set defined by $L^{2}=l$, $M_{z}=l_{z}$ and $H=E$. For negative energies ($E<0$), the space $M_{\mathbf{a}}$ where the trajectories are allowed is compact. We define $\gamma_{\varphi}$ as the curve obtained by varying $\varphi$ and keeping $\theta$ and $r$ constant. We define $\gamma_{\theta}$ and $\gamma_{r}$ in a similar manner. The action variables therefore are[^1]
> $$\begin{align}
> J_{\varphi}&=\frac{1}{2\pi}\oint_{\gamma_{\varphi}}p_{\varphi}d\varphi=\frac{1}{2\pi}l_{z}2\pi=l_{z} \\
> J_{\theta}&=\frac{1}{2\pi}\oint_{\gamma_{\theta}}p_{\theta}d\theta=\ldots=l-l_{z} \\
> J_{r}&=\frac{1}{2\pi}\oint_{\gamma_{r}}p_{r}dr=\ldots=-l+\kappa \sqrt{ \frac{m}{-2E} }
> \end{align}$$
> Combined, these result in
> $$E=- \frac{m\kappa ^{2}}{2(J_{r}+J_{\theta}+J_{\varphi})^{2}}$$
> To find $K(J)$, we note that it must be a function of $J_{r},J_{\theta},J_{\varphi}$ such that when these are substituted by their expressions in terms of $l,l_{z},E$ we get $K(J)=E$. But this means
> $$K(J)=E=- \frac{m\kappa ^{2}}{2(J_{r}+J_{\theta}+J_{\varphi})^{2}}$$
> From here we can find the frequencies
> $$\omega_{r}=\frac{ \partial K }{ \partial J_{r} } ,\quad \omega_{\theta}=\frac{ \partial K }{ \partial J_{\theta} },\quad \omega_{\varphi}=\frac{ \partial K }{ \partial J_{\varphi} } $$
> But due to the specific shape of $K(J)$, all of these derivatives are identical:
> $$\omega_{r}=\omega_{\theta}=\omega_{\varphi}\equiv \omega=\frac{m\kappa ^{2}}{(J_{r}+J_{\theta}+J_{\varphi})^{3}}=m\kappa ^{2}\left( - \frac{2E}{m\kappa ^{2}} \right)^{3/2}$$
> The period in which the trajectory in phase space closes (which is also the period of the body's orbit) is
> $$T=\frac{2\pi}{\omega}=\frac{2\pi}{m\kappa ^{2}}\left( \frac{m\kappa ^{2}}{-2E} \right)^{3/2}=\frac{2\pi\sqrt{ m\kappa ^{2} }}{(-2E)^{3/2}}$$
> If we define
> $$e^{2}=1+ \frac{2El^{2}}{m\kappa ^{2}},\quad\eta=\frac{l^{2}}{m\kappa},\quad a=\frac{\eta}{1-e^{2}}=\frac{l^{2}}{m\kappa} \left( \frac{m\kappa ^{2}}{-2El^{2}} \right)=\frac{\kappa}{-2E}$$
> we can see
> $$\frac{T^{2}}{a^{3}}=\frac{4\pi ^{2}m\kappa ^{2}}{-2E} \frac{(-2E)^{3}}{\kappa ^{3}}=\frac{4\pi ^{2}m}{\kappa}$$
> This is the [[Kepler's laws#Third law|third Kepler's law]], which we managed to derive even without finding the orbit itself (which would require inverting the canonical transformation).

[^1]: See *Fasano & Marmi* for the steps.
