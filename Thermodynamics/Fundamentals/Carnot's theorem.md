**Carnot's theorem** gives the maximum possible [[thermal efficiency]] of a [[heat engine]], by proving that the [[Carnot engine]] is the most theoretically efficient heat engine. In other words, it states that any irreversible engine is less efficient than a reversible one.

> [!info] Carnot's theorem
> Consider a generic heat engine $X$ and a Carnot engine $C$. Then, the [[thermal efficiency|thermal efficiencies]] of the two engines are related by
> $$\eta_{C}\geq \eta_{X}$$
> In plain terms, all heat engines are either as efficient or less efficient than the Carnot engine.
### Proof
Consider a Carnot engine $C$ and another engine $X$, which may or may not be reversible, working between two [[Heat reservoir|heat reservoirs]] at temperatures $T_{1}$ and $T_{2}$, with $T_{2}>T_{1}$. We run $C$ in reverse, as the refrigerator $\tilde{C}$, and feed the [[work]] of $X$ into $\tilde{C}$ to power it. The total work output is
$$W_\text{tot}=(Q_{2}'-Q_{1}')-(Q_{2}-Q_{1})$$
where the primed $Q'$s are [[heat]] input (2) and waste output (1) from $X$ and the non-primed $Q$s are heat input (1) and output (2) for $\tilde{C}$. Now, arrange the apparatus so that $Q_{2}'=Q_{2}$.

![[Schema Carnot Theorem.png]]
*From Kerson Huang's Introduction to Statistical Mechanics, 2nd Ed, page 21*

Since $Q_{2}'$ is extracted from $T_{2}$ by $X$ and put back in as $Q_{2}$ by $\tilde{C}$, and we arranged for them to be the same, there is no net heat going in or out of $T_{2}$. Meanwhile, net heat $Q_{1}-Q_{1}'$ was extracted from $T_{1}$ and converted entirely into work with no other effect (there is not heat exchanged for $T_{2}$ so the only thing left is work for $X$ to $\tilde{C}$). But this violates the [[Laws of thermodynamics|second law of thermodynamics]] unless we assume that $\tilde{C}$ is pulling less heat from $T_{1}$ than $X$ is putting in, which means $Q_{1}\leq Q_{1}'$. If we divide both sides of this inequality by $Q_{2}$, and remembering that $Q_{2}=Q_{2}'$, we get
$$\frac{Q_{1}}{Q_{2}}\leq \frac{Q_{1}'}{Q_{2}'}\quad \Rightarrow \quad 1- \frac{Q_{1}}{Q_{2}}\geq 1- \frac{Q_{1}'}{Q_{2}'}$$
Since thermal efficiency is defined as $\eta=Q_{1}/Q_{2}$ we can write
$$\boxed{\eta_{C}\geq \eta_{X}}$$
where $\eta_{C}$ is the efficiency of the Carnot engine and $\eta_{X}$ is that of the arbitrary engine. This proves the theorem.

As a corollary, the equality is saturated only if $X=C$, so the other engine is another Carnot engine. This proves that all Carnot engines have the same efficiency, regardless of what substance they're working on. The only thing that matters is the reservoir temperatures.