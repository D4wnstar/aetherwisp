---
tags:
  - calcolo-differenziale
---
Sia $f:A\subseteq\mathbb{R}^{N}\rightarrow\mathbb{R}$ con $A$ aperto. Siano $x^{0}, x^{1}\in A\;|\; x^{0}\neq x^{1}$ e il segmento $[x^{0},x^{1}]\subset A$. Sia $\nu= \frac{x^{1}-x^{0}}{||x^{1}-x^{0}||}$ il versore individuato dal segmento. Supponiamo che $f$ sia continua in $[x^{0}, x^{1}]$ e che $f$ ammetta derivata direzionale di versore $\nu$ su $]x^{0},x^{1}[$, allora esiste un punto $\xi\in]x^{0},x^{1}[$ dove
$$\frac{\partial f}{\partial \nu}(\xi)= \frac {f(x^{1})-f(x^{0})}{x^{1}-x^{0}}$$
*Dimostrazione.* Definisco $g:[0,1]\rightarrow\mathbb{R}$, $g(t)=f(x^{0}+t(x^{1}-x^{0}))=f(x^{0}+t\nu||x^{1}-x^{0}||)$.
$g$ è continua in $[0,1]$ e derivabile in $]0,1[$ con derivata
$$g'(t)=(x^{1}-x^{0})\frac{\partial f}{\partial \nu}(x^{0}+t\nu||x^{1}-x^{0}||)\quad\forall t\in ]0,1[$$
Usando il teorema di Lagrange in $\mathbb{R}$ si ha che esiste un $\tau\in]0,1[$ tale per cui
$$\begin{array}{cc}g'(\tau)=\frac{g(1)-g(0)}{1-0}\\
(x^{1}-x^{0})\frac{\partial f}{\partial \nu}(x^{0}+\tau\nu||x^{1}-x^{0}||)=f(x^{1})-f(x^{0})\end{array}$$
Definendo $\xi=x^{0}+\tau(x^{1}-x^{0})$
$$(x^{1}-x^{0})\frac{\partial f}{\partial \nu}(\xi)=f(x^{1})-f(x^{0})$$
$$\frac{\partial f}{\partial \nu}(\xi)=\frac{f(x^{1})-f(x^{0})}{x^{1}-x^{0}}$$
