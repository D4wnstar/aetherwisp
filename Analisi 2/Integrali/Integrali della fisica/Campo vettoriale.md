---
tags:
  - integrali
  - integrali-fisica
---
Definiamo **campo vettoriale** una funzione continua $F : A ⊂ \mathbb{R}^3 → \mathbb{R}^3$. Un campo vettoriale si dice di classe $C^k$ se è una funzione di classe $C^k$.

Il rotore di un campo vettoriale di classe $C^1$ è definito come

$\nabla\times F = \left(\frac{\partial F_3}{\partial y} - \frac{\partial F_2}{\partial z}, \frac{\partial F_1}{\partial z} - \frac{\partial F_1}{\partial x}, \frac{\partial F_2}{\partial x} - \frac{\partial F_1}{\partial y}\right)$

$\nabla\times F = det\left(\begin{array}{cc} \vec{i} & \vec{j} & \vec{k} \\ \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\ F_{1} & F_{2} & F_{3} \end{array}\right)$

Se il rotore è nullo, il campo si dice **irrotazionale**.
La divergenza è definita come

$\nabla\cdot F = \frac{\partial F_1}{\partial x} + \frac{\partial F_2}{\partial y} + \frac{\partial F_3}{\partial z}$

Se la divergenza è nulla, il campo si dice **indivergente**.

Un campo vettoriale $F$ si dice **conservativo** se ammette un [[Potenziale]] $U$ tale che $\nabla U = -F$. Se $F$ è di classe $C^1$ e conservativo allora è anche irrotazionale. Alternativamente può ammettere un [[Potenziale vettore]] $\Psi$ tale che $\nabla\times\Psi = F$. Se $F$ è di classe $C^1$ e ammette potenziale vettore allora è anche indivergente.