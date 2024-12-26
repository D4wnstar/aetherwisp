The **occupation number** $n$ of a quantum [[stato|state]] is the number of [[Particella|particles]] in that state at a given time. Its behavior differs between kinds of quantum particles. For [[Fermion|fermions]], it is either 0 or 1, as the [[Pauli exclusion principle|Pauli exclusion principle]] prevents multiple fermions from occupying the same state. For [[Boson|bosons]], it is can be any natural number, from 0 to infinity. In symbols,
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
$$Z=\sum_{n_{k}}e^{-\beta \sum_{k}\varepsilon_{k}n_{k}}=\prod_{k}\sum_{n_{k}}e^{-\beta\varepsilon_{k}n_{k}}=\prod_{k}Z_{k}$$
What values $n_{k}$ can take depends on the kind of particle:
$$Z_{F}=\prod_{k}\sum_{n_{k}=0}^{1}e^{-\beta \varepsilon_{k} n_{k}}=\prod_{k}(1+e^{-\beta \varepsilon_{k}})$$
$$Z_{B}=\prod_{k}\sum_{n_{k}=0}^{\infty} e^{-\beta \varepsilon_{k}n_{k}}=\prod_{k} \frac{1}{1+e^{-\beta \varepsilon_{k}}}$$
where we used the [[Serie geometrica|geometric series]] in the boson function. The average occupation number for a certain quantum number $\bar{k}$ therefore is
$$\langle n_{\bar{k}} \rangle =\frac{1}{Z}\prod_{k}\sum_{n_{k}}n_{\bar{k}}e^{-\beta n_{k}\varepsilon_{k}}=\frac{1}{\prod_{k}\sum_{n_{\bar{k}}=0}^{1\text{ or }\infty} e^{-\beta n_{k}\varepsilon_{k}}}\prod_{k}\sum_{n_{k}}n_{\bar{k}}e^{-\beta n_{k}\varepsilon_{k}}=\ldots$$
but all the $k$'s in the product except $\bar{k}$ simplify with the denominator, as for them, $n_{\bar{k}}=1$:
$$\ldots= \frac{1}{\sum_{n_{\overline{k}}=0}^{1\text{ or }\infty} e^{-\beta n_{\overline{k}}\varepsilon_{\overline{k}}}}\sum_{n_{\bar{k}}=0}^{1\text{ or }\infty} n_{\bar{k}}e^{-\beta n_{\bar{k}}E_{\bar{k}}}$$
For fermions, it becomes
$$\langle n_{k} \rangle =\frac{e^{-\beta \varepsilon_{k}}}{1+e^{-\beta \varepsilon_{k}}}=\frac{1}{e^{\beta \varepsilon_{k}}+1}$$
This is the [[Fermi-Dirac distribution]]. For bosons, it becomes
$$\begin{align}
\langle n_{k} \rangle &=\frac{1}{\frac{1}{1-e^{\beta \varepsilon_{k}}}} \sum_{n_{k}=0}^{\infty} n_{k}e^{-\beta n_{k}\varepsilon_{k}} \\
&=\frac{1}{\frac{1}{1-e^{\beta \varepsilon_{k}}}} \frac{ \partial  }{ \partial (\beta \varepsilon_{k}) } \sum_{n_{k}=0}^{\infty} e^{-\beta n_{k}\varepsilon_{k}} \\
&=\frac{1}{\frac{1}{1-e^{\beta \varepsilon_{k}}}} \frac{ \partial  }{ \partial (\beta \varepsilon_{k}) } \sum_{n_{k}=0}^{\infty} e^{-\beta n_{k}\varepsilon_{k}} \\
&=1-e^{\beta \varepsilon_{k}}\frac{ \partial  }{ \partial (\beta \varepsilon_{k}) } \frac{1}{1+e^{-\beta \varepsilon_{k}}} \\
&=\frac{1}{e^{\beta \varepsilon_{k}}-1}
\end{align}$$
This is the [[Bose-Einstein distribution]] respectively. Combined, we can write
$$\boxed{\langle n_{k} \rangle =\frac{1}{e^{\beta \varepsilon_{k}}\pm 1}}$$
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

[^1]: The exponential of a sum makes a product, since $e^{a+b}=e^{a}e^{b}$, so $\exp\left( \sum_{k}n_{k} \right)=\prod_{k}\exp(n_{k})$.