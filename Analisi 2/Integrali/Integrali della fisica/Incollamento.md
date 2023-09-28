---
tags:
  - integrali
  - integrali-fisica
---
## Di curve
Date due [[curva|curve]] regolari a tratti $γ_1 : [a, b] → \mathbb{R}^{N}$ e $γ_2 : [α, β] → \mathbb{R}^{N}$ tali che $γ_1(b) = γ_2 (α)$, allora è possibile definire una curva regolare a tratti $γ : [a, c] → \mathbb{R}^{N}$ che *incolla le due curve*. Infatti possiamo definire $c = b + β − α$ e definire la curva regolare a tratti $γ$ nel modo seguente

$\gamma(t)=\begin{cases}\gamma_{1}(t) & t\in[a,b] \\ \gamma_{2}(t-b+\alpha) & t\in[b,c]\end{cases}$

## Di superfici
Consideriamo un insieme chiuso $\Sigma ⊂ \mathbb{R}^{3}$ tale che esistano dei sottoinsiemi chiusi $\Sigma_{1} , . . . , \Sigma_N$ tali che $\Sigma = \Sigma_{1}\; \cup\;...\;\cup\; \Sigma_N$ che siano sostegno di [[superficie|superfici]] regolari, ovvero assumiamo che esistano $\Phi_k : \Omega_k ⊂ \mathbb{R}^{2} → \mathbb{R}^{3}$ , tali che $\Sigma_k = \Phi_k (\Omega_k)$ per ogni $k = 1, . . . , N$. In questo caso l’insieme $\Sigma$ è il sostegno dell’incollamento di $N$ superfici.