---
tags:
  - serie
---
## Serie armonica
La **serie armonica generalizzata** è

$$\sum\limits_{n=1}^{\infty} \frac{1}{n^{\alpha}},\quad \alpha\in \mathbb{R} \quad\begin{cases}\mbox{diverge per}& \alpha\in\;]-\infty,1[ \\ \mbox{converge per} & \alpha\in[1,\infty[ \end{cases}$$

*Dimostrazione.* Per $\alpha\leq0$ la serie non soddisfa il limite necessario per la convergenza, quindi diverge. Per $\alpha\in\;]0,1]$ notiamo che vale $\frac{1}{n}\leq \frac{1}{n^{\alpha}}$ per ogni $n\in\mathbb{N}^{+}$ quindi per il [[Criterio del confronto]] la serie diverge. Per $\alpha\in[2,+\infty[$ vale invece $\frac{1}{n^{\alpha}}\leq \frac{1}{n^{2}}$ per ogni $n\in\mathbb{N}^{+}$. Per $\alpha\in]1,2[$ usiamo la [[Criterio della serie condensata|serie condensata]]: $\sum\limits_{n=0}^{\infty}a_{2^{n}}2^{n}=\sum\limits_{n=0}^{\infty} \frac{1}{2^{\alpha n}}2^{n}=\sum\limits_{n=0}^{\infty}\left( \frac{1}{2^{\alpha-1}}\right)^{n}$, che è una serie geometrica di ragione $\rho= \frac{1}{2^{\alpha-1}}$. Converge se $\rho<1$, che accade quando $\alpha>1$. Quindi converge per $\alpha\in]1,2[$.

## Serie di Mengoli
La **serie di Mengoli** è
$$\sum\limits_{n=1}^{\infty} \frac{1}{n(n+1)}=1$$
## Serie esponenziale
La **serie esponenziale** è
$$\sum\limits_{n=0}^{\infty} \frac{x^n}{n!}=e^x$$
Converge con $x=1$.