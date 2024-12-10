---
aliases:
  - indistinguishable
  - distinguishable
---
Two [[Particella|particles]] are said to be **identical** if all their characteristic properties (like [[Numero quantico|quantum numbers]]) are the same. Identical particles are **distinguishable** in classical mechanics, and **indistinguishable** in quantum mechanics.
### Fermions and bosons
In classical mechanics, two particles may be identical, but can always be distinguished. For instance, consider two pool balls tagged as 1 and 2. They strike each other and scatter, bouncing off. Let's call the balls after the scattering 3 and 4. Of course, these are still the same balls, with $1\to 3$ and $2\to 4$. If 1 and 2 are differently colored, it's trivial to tell which is which after the scattering. If they are colored the same, it's harder but still possible, as we can follow the motion instant-by-instant to check where each one goes, but tracing their trajectories.

Not so in quantum physics. Say the pool balls are now quantum objects. After the scattering they end up in some joint [[stato|state]] $\ket{\psi}=\ket{x_{1}=a,x_{2}=b}=\ket{ab}$. Classically, the states $\ket{ab}$ and $\ket{ba}$ would be different, as we'd be switching the positions and since the balls are distinguishable, this makes for a different end state. But due to the [[Disuguaglianza di Heisenberg|indeterminacy principle]], we can't follow trajectories in quantum physics (hell, the very concept of trajectory makes no sense), so our previous method of tracking movement to distinguish what happens no longer applies. Thus, we can't state that $\ket{ab}$ and $\ket{ba}$ are any different, as we just can't follow the dynamics. What we can do, is state that the two states are proportional to each other (they still arise from the same source, after all). In symbols, this means $\ket{ab}=\alpha \ket{ba}$, where $\alpha \in \mathbb{C}$. The end state is some linear combination of the two
$$\ket{\psi} =\beta \ket{ab} +\gamma \ket{ba} =\alpha[\beta \ket{ba} +\gamma \ket{ab} ]$$
We have $\beta=\alpha \gamma$ and $\gamma=\alpha \beta$, so $\alpha=\beta/\gamma=\gamma/\beta$. This implies $\alpha^{2}=1$ or $\alpha=\pm 1$. So, there are only two possible states
$$\ket{ab} =\pm \ket{ba} $$
This essentially shows that there is a [[Parità|parity]] phenomenon going on. Sometimes, inverting the position causes the state to flip sign, other times it remains the same. This suggests the presence of two types of particles, one which undergoes parity flipping, and another which does not. These two types of particles are called [[bosone|bosons]] and [[fermione|fermions]]. Fermions flip signs, bosons do not. This has the remarkable outcome that fermions just can't occupy the same state as another fermion in the same system simultaneously, whereas bosons can. This odd property is called the [[principio di esclusione di Pauli|Pauli exclusion principle]].

Take as an example the [[Oscillatore armonico quantistico|quantum harmonic oscillator]]. There are infinite discrete energy [[Equazione agli autovalori|eigenstates]] determined by the principal quantum number $n$. Since fermions can't occupy the same state, each energy state can be occupied by only one fermion at the same time[^1]. Meanwhile, bosons have no such restriction and can theoretically all pile up at the ground state.

If we call the energy level of the $k$-th particle $n_{k}$, the [[partition function]] can be calculated as
$$Z=\prod_{k}\sum_{n_{k}}e^{-nE_{k}n_{k}}$$
The exact form depends on whether we are working with bosons or fermions.
$$Z_{B}=\prod_{k}\sum_{n_{k}=0}^{\infty} e^{-\beta E_{K}n_{k}},\qquad Z_{F}=\prod_{k}\sum_{n_{k}=0}^{1}e^{-\beta E_{k} n_{k}}$$
The average energy state for each particle therefore is
$$\langle n_{\bar{k}} \rangle =\frac{1}{Z}\prod_{k}\sum_{n_{k}}n_{\bar{k}}e^{-\beta n_{k}E_{k}}= \frac{1}{\sum_{n_{\bar{k}}=0}^{1\text{ or }\infty} e^{-\beta n_{k}E_{k}}}\sum_{n_{\bar{k}}=0}^{1\text{ or }\infty} n_{\bar{k}}e^{-\beta n_{\bar{k}}E_{\bar{k}}}$$
For fermions, it becomes
$$\langle n_{k} \rangle =\frac{e^{-\beta E_{k}}}{1+e^{-\beta E_{k}}}=\frac{\sum_{n_{k}=0}^{i} n_{k}e^{-\beta n_{k}E_{k}}}{1+e^{-\beta E_{k}}}=\frac{\sum_{n_{k}=0}^{1} n_{k}e^{-\beta n_{k}E_{k}}}{\sum_{n_{k}=0}^{1} e^{-\beta n_{k}E_{k}}}=\frac{1}{e^{\beta E_{k}}+1}$$
For bosons, it becomes
$$\langle n_{k} \rangle =\frac{1}{\frac{1}{1-e^{\beta E_{k}}}} \sum_{n_{k}=0}^{\infty} n_{k}e^{-\beta n_{k}E_{k}}=\frac{1}{e^{\beta E_{k}}-1}$$
These are the [[Fermi-Dirac distribution]] and the [[Bose-Einstein distribution]] respectively. Combined, we can write
$$\boxed{\langle n_{k} \rangle =\frac{1}{e^{\beta E_{k}}\pm 1}}$$
The sign is determined the kind of particle in play.

> [!example] The T in TTRPG stands for thermodynamics
> Consider 2 three sided dice and let's play a game where the throw them at the same time and check the result, with some additional rules. The fundamental rule is that some combinations of results are legal and some aren't. If the roll is not legal, we must reroll until we get one that is. Let's define three variations of the game:
> - In the *Boltzmann game*, every combination of rolls is legal.
> - In the *Bose game*, a roll is illegal if the second dice is greater *or equal* ($\geq$) to the first.
> - In the *Fermi game*, a roll is illegal if the second is greater *but not equal* ($>$) to the first.
> 
> Let's find the probability of rolling a total of five in each of the games. We have two dice and each die has three possible states: 1, 2 and 3. That's $3^{2}=9$ possible combinations. In the Boltzmann game, all of these are legal. In the Bose and Fermi game, not all of them are. Since there aren't that many combinations, we can figure out which are legal by just listing them all out manually. 
> 
> idk im lazy there should be a list of possibilities here
> 
> So we found that there are 6 legal combinations in the Bose game, and 3 legal ones in the Fermi game. Of the 9 original combinations, the totals of each combinations are
> 
> |     | 1   | 2   | 3   |
> | --- | --- | --- | --- |
> | 1   | 2   | 3   | 4   |
> | 2   | 3   | 4   | 5   |
> | 3   | 4   | 5   | 6   |
> 
> In the Boltzmann game, the probability is obvious: just count the cells that are equal to 5. That's 2 over 9. In the Bose game, we have 6 probabilities:
> 
> |     | 1   | 2   | 3   |
> | --- | --- | --- | --- |
> | 1   | 2   | 3   | 4   |
> | 2   | 3   | 4   | 5   |
> | 3   | 4   | 5   | 6   |
> 
> (TODO: Finish this example, end of lesson from 15/11/2024)

[^1]: More than one, actually, because of different possible [[spin]] states, but if the particles were spinless, that's how it would be.