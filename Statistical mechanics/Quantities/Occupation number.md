---
wiki-publish: true
---
The **occupation number** $n$ of a quantum [[stato|state]] is the number of [[Particle|particles]] in that state at a given time. Its behavior differs between kinds of quantum particles. For [[Fermion|fermions]], it is either 0 or 1, as the [[Pauli exclusion principle|Pauli exclusion principle]] prevents multiple fermions from occupying the same state. For [[Boson|bosons]], it is can be any natural number, from 0 to infinity. In symbols,
$$n=\begin{cases}
0,1\quad&\text{for fermions} \\
0,1,2,\ldots \quad&\text{for bosons}
\end{cases}$$
For a [[Physical system|system]] of $N$ particles, occupation numbers satisfy
$$\sum_{i}n_{i}=N $$
where $i$ is some label used to distinguish the states (usually a [[Numero quantico|quantum number]]).
### Average occupation
For an example, consider a system with a discrete energy [[Spettro|spectrum]] $\{ \varepsilon_{k} \}_{k}$. There are infinite discrete energy [[Equazione agli autovalori|eigenstates]], each labelled by a quantum number $k$. Each energy state $\ket{\varepsilon_{k}}$ is simultaneously occupied by a number of particles $n_{k}$. Due to the Pauli exclusion principle, this is 0 or 1 for fermions and any natural number for bosons.

If we take the particles to be non-interacting, the [[Partition function|canonical partition function]] of the system can be calculated as follows[^1]:
$$Z=\sum_{\{ n_{k} \}}e^{-\beta \sum_{k}\varepsilon_{k}n_{k}}=\prod_{k}\sum_{n_{k}}e^{-\beta\varepsilon_{k}n_{k}}$$
What values $n_{k}$ can take depends on the kind of particle:
$$Z_{F}=\prod_{k}\sum_{n_{k}=0}^{1}e^{-\beta \varepsilon_{k} n_{k}}=\prod_{k}(1+e^{-\beta \varepsilon_{k}})$$
$$Z_{B}=\prod_{k}\sum_{n_{k}=0}^{\infty} e^{-\beta \varepsilon_{k}n_{k}}=\prod_{k} \frac{1}{1+e^{-\beta \varepsilon_{k}}}$$
where we used the [[Serie geometrica|geometric series]] for bosons. The average occupation number for a certain quantum number $\bar{k}$ therefore is
$$\langle n_{\bar{k}} \rangle =\frac{1}{Z}\prod_{k}\sum_{n_{k}}n_{\bar{k}}e^{-\beta n_{k}\varepsilon_{k}}=\frac{\prod_{k}\sum_{n_{\bar{k}}=0}^{1\text{ or }\infty}n_{\bar{k}}e^{-\beta n_{k}\varepsilon_{k}}}{\prod_{k}\sum_{n_{\bar{k}}=0}^{1\text{ or }\infty} e^{-\beta n_{k}\varepsilon_{k}}}=\ldots$$
but all the $k$'s in the product except $\bar{k}$ simplify with the denominator, as for them, $n_{\bar{k}}=1$:
$$\ldots=\frac{\cancel{ Z_{1} }\cancel{ Z_{2} }\ldots\sum_{n_{\bar{k}}=0}^{\infty}n_{\bar{k}}e^{-\beta n_{k}\varepsilon_{k}}\ldots}{\cancel{ Z_{1} }\cancel{ Z_{2} }\ldots Z_{\bar{k}}\ldots}= \frac{1}{\sum_{n_{\overline{k}}=0}^{1\text{ or }\infty} e^{-\beta n_{\overline{k}}\varepsilon_{\overline{k}}}}\sum_{n_{\bar{k}}=0}^{1\text{ or }\infty} n_{\bar{k}}e^{-\beta n_{\bar{k}}E_{\bar{k}}}$$
For fermions, it becomes
$$\langle n_{k} \rangle =\frac{e^{-\beta \varepsilon_{k}}}{1+e^{-\beta \varepsilon_{k}}}=\frac{1}{e^{\beta \varepsilon_{k}}+1}$$
This is the [[Fermi-Dirac distribution]]. For bosons, it becomes
$$\begin{align}
\langle n_{k} \rangle &=\frac{1}{\frac{1}{1-e^{\beta \varepsilon_{k}}}} \sum_{n_{k}=0}^{\infty} n_{k}e^{-\beta n_{k}\varepsilon_{k}} \\
&=(1-e^{\beta \varepsilon_{k}}) \frac{ \partial  }{ \partial (\beta \varepsilon_{k}) } \sum_{n_{k}=0}^{\infty} e^{-\beta n_{k}\varepsilon_{k}} \\
&=(1-e^{\beta \varepsilon_{k}}) \frac{ \partial  }{ \partial (\beta \varepsilon_{k}) } \frac{1}{1+e^{-\beta \varepsilon_{k}}} \\
&=\frac{1}{e^{\beta \varepsilon_{k}}-1}
\end{align}$$
This is the [[Bose-Einstein distribution]] respectively. Combined, we can write
$$\boxed{\langle n_{k} \rangle =\frac{1}{e^{\beta \varepsilon_{k}}\pm 1}}$$
The sign is determined the kind of particle in play.

> [!example] The T in TTRPG stands for thermodynamics
> As a practical example of how these statistics work, take 2 three sided dice and let's play a game where we roll them at the same time and check the result, with some additional rules. The fundamental rule is that some combinations of results are legal and some aren't. If the roll is not legal, we must reroll until we get one that is. Let's define three variations of the game:
> - In the *Boltzmann game*, every combination of rolls is legal.
> - In the *Bose game*, a roll is illegal if the second die is greater *but not equal* ($>$) to the first.
> - In the *Fermi game*, a roll is illegal if the second die is greater *or equal* ($\geq$) to the first.
> 
> Let's find the probability of rolling a total of five in each of the games. We have two dice and each die has three possible states: 1, 2 and 3. That's $3^{2}=9$ possible combinations. In the Boltzmann game, all of these are legal. In the Bose and Fermi game, not all of them are. Since there aren't that many combinations, we can analyze what happens by manually listing all the outcomes.
> 
> The 9 possible combinations can be written in a table. The first row is the result of the first die, while the first column is the result of the second.
> 
> |     | 1   | 2   | 3   |
> | --- | --- | --- | --- |
> | 1   | 2   | 3   | 4   |
> | 2   | 3   | 4   | 5   |
> | 3   | 4   | 5   | 6   |
> 
> In the Boltzmann game, these are all valid. After all, we are allowing every combination. However, this changes in the Bose and Fermi. In the Bose game, we must discard results where the second die is greater than the first:
>
> |     | 1   | 2   | 3   |
> | --- | --- | --- | --- |
> | 1   | 2   | 3   | 4   |
> | 2   | —   | 4   | 5   |
> | 3   | —   | —   | 6   |
>
> The entire lower triangle of the table got invalidated, leaving us with only 6 valid combinations. Similarly, with the Fermi game rule of discarding greater or equals results we see
> 
> |     | 1   | 2   | 3   |
> | --- | --- | --- | --- |
> | 1   | —   | 3   | 4   |
> | 2   | —   | —   | 5   |
> | 3   | —   | —   | —   |
> 
> Now we removed both the lower triangle *and* the diagonal, further reducing our chance of success down to 3 combinations.
> 
> If it wasn't clear enough from the game names, these are representations of the classical, Bose-Einstein and Fermi-Dirac statistics respectively, specifically regarding the amount of ways we can put 2 particles in 3 states. We can see that quantum states are fewer in number: this is because the constraints put on the [[Funzione d'onda|wavefunctions]] by [[Identical particles|indistinguishability]] reduce the number of valid states that the system can take. Because of this, if we were to count every possible state, we'd be overestimating how many ones we have in both cases.
> 
> This different count modify the likelihoods that we see: for instance, say you want the dice to make exactly 5. In the Boltzmann game, the chance is 2/9. In the Bose game, it is 1/6. In the Fermi game, it is 1/3. Here Fermi dice have the advantage. Meanwhile, the chance of getting the same number on both dice is 3/9 in the Boltzmann game, 3/6 in the Bose game and 0 in the Fermi game. Bose dice win this one.

[^1]: The exponential of a sum makes a product, since $e^{a+b}=e^{a}e^{b}$, so $\exp\left( \sum_{k}n_{k} \right)=\prod_{k}\exp(n_{k})$.