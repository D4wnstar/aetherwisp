---
wiki-publish: true
---
The **Dirac equation** is a relativistic [[wave equation]] that describes the dynamics of [[mass|massive]] [[Fermion|fermions]], such as [[Electron|electrons]] and [[Quark|quarks]]. The equation is:
$$(i\gamma^{\mu}\partial_{\mu} - m)\psi = 0$$
where $\gamma^{\mu}$ are the [[gamma matrices]]. The [[wavefunction]] $\psi$ that solves the equation has four components, unlike the complex-valued wavefunction of the [[Schrödinger equation]], and is called a **[[bispinor]]** or **Dirac spinor**. Using [[Feynman slash notation]] it reads
$$(i\cancel{ \partial }-m)\psi=0$$

It is a generalization of the Schrödinger equation that accounts for special relativity. It predicts the existence of [[antimatter]] and led to the discovery of many fermions, including the [[electron|positron]].
### History and derivation
It is very common for individual [[Particle|particles]] to be moving at speeds near the [[speed of light]], which encourages a treatment of quantum mechanics that incorporates the results of special relativity. We know that quantum mechanics is based on the Schrödinger equation, so our goal is to extend it so that it also accepts relativistic speeds and returns to the old form for nonrelativistic speeds.

The most natural approach to this task is to simply the [[relativistic energy]] instead of the usual one
$$E = \sqrt{ \hat{p}^{2} + m^{2} }$$
(we'll use [[natural units]] for all of this; also $\hat{p}$ is an [[operator]] as usual in QM). Then, we just put it in the time-independent Schrödinger equation:
$$\hat{H}\psi=E\psi$$
Recalling that [[Linear momentum|momentum]] is $\hat{p}=-i\nabla$ and the [[Hamiltonian]] is $\hat{H}=i\frac{ \partial  }{ \partial t }$, this leads to the time-dependent form
$$i \frac{\partial \psi}{\partial t}=\sqrt{(-i\nabla)^{2} + m^{2}}\ \psi$$
This form is, unfortunately, not very useful for anything. The issue is that space and time are still separate, which is completely against relativity. We want our equation to work well in [[spacetime]]. To make things worse, the square root makes the equation not [[relativistic invariant|relativistically invariant]], which prevents it from being consistent with electromagnetism.

The first problem can be fixed rather easily. Instead of using the derivatives openly, just use the [[d'Alembertian]]. With some algebra we can write:
$$(\Box + m^{2})\psi = 0$$
This is known as the **[[Klein-Gordon equation]]**. Thanks to the d'Alembertian, space and time are unified, and the square root eliminated itself without us even needing to do anything solving both earlier issues. So that's it, we solved relativistic quantum mechanics!

No, of course not, this article is about the Dirac equation for a reason. See, the KG equation hits on a new problem: being second-order in time and space, it admits both positive *and* negative energy solutions:
$$E=\pm \sqrt{ \hat{p}^{2}+m^{2} }$$
The positive-energy ones are just fine, but the negative-energy solutions are a disaster: they imply the existence of *negative [[probability|probabilities]]*, something that's fundamentally impossible in both physics and math. The KG equation is actually still useful in certain contexts, but it is by no means general enough for a proper description of quantum mechanics.

Also, something that I haven't mentioned yet is [[spin]]. Schrödinger quantum mechanics is, for the most part, written without taking spin into consideration. Of course you can solve for spin [[Stato|states]] with the Schrödinger equation, but they take extra care and your entire attention. Since *all* fermions have spin, we need a way to have it be "just a property", something that's automatically taken care of by the shape of the equation. The KG equation, like Schrödinger's, does not provide a way of doing so.

A better approach comes from Dirac himself, circa 1928. He proposed writing the Hamiltonian operator as a linear combination of energy and momentum:
$$\hat{H} = \sum_{i=x,y,z} \alpha_{i} \hat{p}_{i} + \beta m=\alpha_{x}\hat{p}_{x}+\alpha_{y}\hat{p}_{y}+\alpha_{z}\hat{p}_{z}+\beta m$$
where $\alpha_{i}$ and $\beta$ are $4\times 4$ [[matrix|matrices]] and $i=x,y,z$ for the three spatial axes[^1] The idea came from spacetime, where the [[four-momentum]] contains both three-momentum and energy, specifically [[Relativistic energy|rest mass energy]]. The four-dimensionality of spacetime is why the matrices are $4\times 4$. Then the Schrödinger equation becomes:
$$E\psi = \hat{H}\psi=\left( \sum_{i=x,y,z}\alpha_{i}\hat{p}_{i}+\beta m \right)\psi\equiv(\alpha_{i}p_{i}+\beta m)\psi\tag{1}$$
To avoid excessive verbosity, we drop the hat from $\hat{p}$ and summation will now be implied over the same index as per [[Einstein notation]], so $\alpha_{i}p_{i}\equiv \sum_{i} \alpha_{i}p_{i}$. Our energy must be the relativistic one, so
$$E^{2} = \hat{p}^{2} + m^{2} = ( \alpha_{i}p_{i} + \beta m )^{2}$$
Expanding the square yields
$$\begin{align}
p^{2}+m^{2}&=\alpha_{i}p_{i}\alpha_{j}p_{j} + (\alpha_{i}p_{i}\beta m + \beta m \alpha_{j}p_{j}) + \beta^{2}m^{2} \\
&= \alpha_{i}\alpha_{j}p_{i}p_{j} + (\alpha_{i}\beta + \beta\alpha_{i})mp_{i} + \beta^{2}m^{2}
 \\
&= \frac{1}{2}(\{\alpha_{i},\alpha_{j}\} + [\alpha_{i},\alpha_{j}])p_{i}p_{j}+\{\beta,\alpha_{i}\}mp_{i} + \beta^{2}m^{2}
\end{align}$$
using the [[commutator]] $[\cdot,\cdot]$ and anticommutator $\{ \cdot,\cdot \}$. We also used the property
$$AB=\frac{1}{2}(\{ A,B \}+[A,B])$$
specifically on $\alpha_{i}\alpha_{j}$.

Now, this whole thing needs to match $p^{2} + m^{2}$. For this to happen, several conditions must be met:
- Mixed terms must vanish: $\{\beta, \alpha_{i}\} = 0$.
- There must be no coefficients on $p^{2}$: $\{\alpha_{i}, \alpha_{j}\} = 2\delta_{ij}\mathrm{I}$ where $\delta_{ij}$ is the [[Kronecker delta]] and $\mathrm{I}$ is the [[identity matrix]].
- $[\alpha_{i}, \alpha_{j}] p_{i}p_{j} = 0$ is true as a consequence of the previous condition: $[\alpha_{i},\alpha_{j}]$ is a symmetric operator, $p_{i}p_{j}$ is antisymmetric, and the contraction (the sum over all indexes) of an symmetric and antisymmetric operator (or matrix) is zero.
- There must be no coefficients on $m^{2}$: $\alpha_{i}^{2} = \beta^{2} =\mathrm{I}$.

The only matrices that satisfy all these conditions are the [[block matrix|block matrices]]
$$\alpha_{i} = \begin{pmatrix} 0 & \sigma_{i} \\ -\sigma_{i} & 0 \end{pmatrix}, \quad
\beta = \begin{pmatrix} \mathrm{I}_{2} & 0 \\ 0 & -\mathrm{I}_{2} \end{pmatrix}$$
where $\sigma_{i}$ are the [[Pauli matrices]]. Note that $\mathrm{I}_{2}$ is the $2\times 2$ identity matrix, as opposed to before where $\mathrm{I}$ was implied to be $4\times 4$. For brevity, Dirac introduced what are now called the [[gamma matrices]]:
$$\gamma^{0} \equiv \beta, \quad \gamma^{i} \equiv \gamma^{0}\alpha_{i}=\beta \alpha_{i}$$
Then he defined the [[four-vector]] of matrices $\gamma^{\mu} = (\gamma^{0}, \gamma^{1}, \gamma^{2}, \gamma^{3})$. We need to put these in $(1)$. Start by multiplying both sides by $\beta$:
$$i\beta \frac{\partial \psi}{\partial t} = (\beta\alpha_{i}p_{i} + \beta^{2}m)\psi$$
Now, using the gamma matrices, $\beta^{2} = \mathrm{I}$ and substituting $p_{i}$ with its corresponding operator $-i\frac{ \partial  }{ \partial x_{i} }$ we find
$$i\gamma^{0} \frac{\partial \psi}{\partial t} = \left(-i\gamma^{i} \frac{\partial}{\partial x_{i}} + m\right)\psi$$
For even more brevity, we write the partial derivatives with reference to the indexes of spacetime axes:
$$\frac{ \partial  }{ \partial t } \equiv \partial_{0},\qquad \frac{ \partial  }{ \partial x } \equiv \partial_{1},\qquad \frac{ \partial  }{ \partial y } \equiv\partial_{2},\qquad \frac{ \partial }{ \partial z } \equiv\partial_{3}$$
then
$$i\left(\gamma^{0}\partial_{0} + \gamma^{i}\partial_{i} \right)\psi = m\psi$$
Introducing the relativistic concept of **[[covariant derivative]]** $\partial_{\mu}\gamma^{\mu} = \partial_{0}\gamma^{0} + \partial_{i}\gamma^{i}$, we finally write:
$$\boxed{(i\gamma^{\mu}\partial_{\mu} - m)\psi = 0}$$
This is the **Dirac equation**, the fundamental equation for time evolution of a relativistic quantum system of fermions. Since Feynman was quite the character, he decided that this notation was *still* not brief enough, so he invented the **[[Feynman slash notation|slash operator]]** $\cancel{ \partial }=\gamma^{\mu}\partial_{\mu}$, with which the Dirac equation comes out to be the ludicrously short form
$$\boxed{(i\cancel{\partial}-m)\psi}$$
The Dirac equation solves every single problem we've discussed before and opens the door to an entire new realm of physics:
- It treats space and time in unison thanks to $\gamma^{\mu }\partial_{\mu}$.
- The presence of the Pauli matrices in the gammas automatically solves the spin problem. The solutions of the Dirac equation are now four-dimension vectors called **bispinors** or **Dirac spinors** that innately include spin.
- The Dirac equation is an extension of the Klein-Gordon equation: solutions of Dirac's are also solutions of KG.
- All solutions $\psi$ are relativistic invariants.
- All solutions lead to positive probabilities.

So we're done! We solved relativistic quantum mechanics for real this time (at least for fermions). And... yes, you'd be right, but there's still a nagging question. You see, while the probabilities are now all positive, the energies predicted are *not*. Those nonsensical negative-energy solutions from before all persist. Now, of course, you might just say that the Dirac equation is wrong, but given that it does *literally everything else* right, it starts to become a questionable stance. What if *we* are wrong and the equation is desperately trying to tell us something we refuse to listen to?

Dirac made the attempt to listen. He accepted defeat and claimed that those nonsensical negative-energy solutions were the work of what he called **[[antiparticle|antiparticles]]**, essentially polar opposites of the particles he knew already. He said that for his equation to hold, the [[quantum vacuum]] must have been populated with negative-energy states; this collection of states is called the **[[Dirac sea]]**. Once one of these states is excited (say, by a [[photon]]), it is kicked into positive energy territory and becomes a proper particle, but the *hole* that is left behind in the sea is filled by the formation of an antiparticle with properties ([[Numero quantico|quantum numbers]] to be exact) entirely opposite to the particle[^2]. He finally postulated that if antiparticles could exist, they could also aggregate in the same way as ordinary [[matter]] to form **[[antimatter]]**.

As you might imagine, this concept was ludicrous at the time, but if you've gotten far enough in life as to be studying relativistic quantum mechanics, then you probably don't need me to tell you that antiparticles are, in fact, real. So real in fact that we've got a large number of experiments proving their existence and we've yet to find a particle that lacks an antiparticle.

Granted, there are still open questions. Some fermions are postulated to be their own antiparticles: we call them **[[Majorana fermion|Majorana fermions]]**, in opposition to **Dirac fermions** which have a separate antiparticle. As of 2025, we don't know of any Majorana fermion, but [[neutrino|neutrinos]] are still a potential candidate. Also, you don't *see* antimatter in daily life. This is because the [[Universe]] has an *enormous* asymmetry between matter (everything that you see) and antimatter (essentially extinct). We call this **[[baryon asymmetry]]** (because ordinary matter is made of [[barion|barions]]) and we don't yet have an answer as to why the Universe came out to be this way.

[^1]: Don't get confused between $\beta$ the matrix and $\beta$ the relativistic speed.

[^2]: The mass remains the same.
