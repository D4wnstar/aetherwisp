---
wiki-publish: true
---
Magnetism has, chronologically speaking, always been its own thing. It has its own origin ([[electric current]]) and manifestation ([[magnetic field]]) distinct from electricity ([[electric charge]] and [[electric field]]), its own pair of laws in [[Maxwell's equations]] and its own half of the [[electromagnetic wave]]. And yet, despite all this, magnetism isn't real. Okay, that's a strong statement, it certainly *is* real, but it is not an independent phenomenon. Magnetism as we know it cannot exist alone. Magnetism isn't a cause, it's a consequence. Specifically, it's a consequence of the joint efforts of relativity and electrostatics.

Start off how electromagnetism history taught us: a line of charges moving straight at some speed $v$. Assume that the charges are close enough as to treat the whole river of charges as a continuous line distribution $\lambda$. Now assume that, overlapping this line, there's *another* line of charge, with *negative* charge, moving in the opposite direction, with the same speed. The line distribution will be $-\lambda$. We now have a net electric current of
$$I=2\lambda v$$
since inverting both charge and direction of motion leads to the same current, so we have two identical currents $\lambda v$ overlapping. Say that near the line of charges, we have a lone free charge $q$ passing by at some constant speed $u$, moving in the same direction as the positive charges. In this [[frame of reference]], call it $\mathcal{S}$, attached to the line of charges in such a way that both go at the speed in opposite directions, there is no electrical [[force]] on $q$, because the line charges cancel out. However, in the frame of reference attached to $q$, call it $\mathcal{S}'$, things change. In here, $q$ is at rest and its the line charges that are doing all the moving — asymmetrical moving, now. In fact, the velocities of the positive and negative lines are summed with the speed $u$ of the origin according to the [[Postulates of special relativity|Einstein velocity addition rule]]:
$$v_{\pm}=\frac{v\mp u}{1\mp vu/c^{2}}$$
where $c$ is the [[speed of light]]. $v_{-}$ is now greater than $v_{+}$. "So... what now?" I hear you ask. Well, due to relativity, the motion of the particles enacts a [[Length contraction|contraction of lengths]]. Certainly it did the same before, but since the speeds were the same for both lines, we didn't really care. Now that they are no longer the same, we *do* care, because they now feel different contractions. Namely, the contraction of the space in which the negative charges travel is more intense than that of the positive charges, which means that the line charge distribution, which *depends on space*, must vary for both and do so in different ways. The negative charge distribution becomes *larger* than the positive ones because negative charges are more compressed. As such, the line now has net negative charge, as demanded by
$$\lambda_\text{tot}=\lambda_{+}+\lambda_{-}$$
where
$$\lambda_{\pm}=\pm \gamma_{\pm}\lambda_{0}$$
The [[Lorentz transformation|relativistic]] gamma is the usual:
$$\gamma_{\pm}=\frac{1}{\sqrt{ 1- v^{2}_{\pm}/c^{2} }}$$
$\lambda_{0}$ is not the old $\lambda$, but rather the charge distribution of the positive line in a frame of reference in which its at rest (equivalently, the distribution of the negative line in a frame in which *that* is at rest). The two are related by $\lambda=\gamma \lambda_{0}$, where $\gamma=1/\sqrt{ 1-v^{2}/c^{2} }$. Now, we want to substitute $v_{\pm}$ in $\gamma_{\pm}$. There's no easy trick here, it's just doing math:
$$\begin{align}
\gamma_{\pm}&=\frac{1}{\sqrt{ 1- \frac{1}{c^{2}}(v\mp u)^{2}(1\mp vu/c^{2})^{-2} }} \\
&=\frac{c^{2}\mp uv}{\sqrt{ (c^{2}\mp uv)^{2}-c^{2}(v\mp u)^{2} }} \\
&=\frac{c^{2}\mp uv}{\sqrt{ (c^{2}-v^{2})(c^{2}-u^{2}) }} \\
&=\gamma \frac{1\mp uv/c^{2}}{\sqrt{ 1-u^{2}/c^{2} }}
\end{align}$$
So, our total line charge in $\mathcal{S}'$ is
$$\lambda _\text{tot}=\lambda_{+}+\lambda_{-}=\lambda_{0}(\gamma_{+}-\gamma_{-})= \frac{-2\lambda uv}{c^{2}\sqrt{ 1-u^{2}/c^{2} }}$$
Thus, we have a line charge that only exists in one frame but not in another[^1]. This charge will create an (evidently relative) electric field
$$E=\frac{\lambda _\text{tot}}{2\pi \varepsilon_{0}s}$$
at some distance $s$ to the line. [[Electric field|Coulomb's law]] tells us this makes a [[force]]
$$F'=qE=- \frac{\lambda v}{\pi \varepsilon_{0}c^{2}s} \frac{qu}{\sqrt{ 1-u^{2}/c^{2} }}$$
in $\mathcal{S}'$. But if there's a force in $\mathcal{S}'$, there must be a force *somewhere* in $F$ too. We can bypass the whole search by anti-[[Lorentz transformation|Lorentz transforming]] back from $\mathcal{S}'$ to $\mathcal{S}$:
$$F=\sqrt{ 1- \frac{u^{2}}{c^{2}} }F'=- \frac{\lambda v}{\pi \varepsilon_{0}c^{2}} \frac{qu}{s}$$
(since $\mathbf{F}'_{\perp}=\mathbf{F}_{\perp}/\gamma$ if the particle is instantaneously at rest in the original system; see [[Minkowski force#Dynamics and derivation]]). This force attracts towards the wire, as seen evidently by the negative charge in $\mathcal{S}'$, but in $\mathcal{S}$ it *cannot* be electrical as there is no net charge there, so there must be another kind of force that's not electrical but still causes the same attraction in the absence of charges. This is, as you may imagine, the magnetic force
$$F=-qu \frac{\mu_{0}I}{2\pi s}=q \mathbf{u}\times\left( \frac{\mu_{0}\mathbf{I}}{2\pi s} \right)$$
since $\lambda v=I$ and $\mu_{0}=1/\varepsilon_{0}c^{2}$. This is the familiar [[Lorentz force]] of the magnetic field of a wire on a charge particle moving at some velocity $\mathbf{u}$, and yet we never claimed there even was a magnetic field in the first place. We just took the charges as the universe gave them and we saw what happened next. Thus, the theory of magnetism is, in a way, complete. We always knew it was a consequence of the motion of charges, but we didn't know *why*. Well, *relativity* is why. That motion causes distortions in perceived [[spacetime]] and, as a consequence, creates forces that we'd otherwise not see. But it all fundamentally stems for a single physical property: electric charge.

[^1]: Do not confuse this with electric charge changing! Electric charge is both conserved and [[Relativistic invariant|relativistically invariant]]. It *never* changes. But space can change and by consequence geometric distributions of charge.
