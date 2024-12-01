---
tags:
  - calcolo-differenziale
---
La **serie di Taylor** è una [[serie]] che espande una funzione reale o complessa $f(x)$ infinitamente derivabile attorno ad un punto $x_{0}$ attraverso le sue derivate
$$f(x)=\sum_{n=0}^{\infty} \frac{f^{(n)}(x_{0})}{n!}(x-x_{0})^{n}=f(x_{0})+ f^{(1)}(x_{0})(x-x_{0})+ \frac{1}{2}f^{(2)}(x_{0})(x-x_{0})^{2}+\ldots$$
dove $f^{(n)}$ rappresenta l'$n$-esima derivata di $f$. Se $x_{0}=0$ la serie si riduce ad una **serie di Maclaurin**:
$$f(x)=\sum_{n=0}^{\infty} \frac{f^{(n)}(0)}{n!}x^{n}=f(0)+f^{(1)}(0)x+ \frac{1}{2}f^{(2)}(0)x^{2}+\ldots$$
### $N$ dimensioni
Per una funzione $f(\mathbf{x})$ in $N$ dimensioni, la serie centrata in un punto $\mathbf{x}_{0}$ diventa
$$f(\mathbf{x})=\sum\limits_{d=0}^{\infty} \frac{1}{d!}Q_{d}(\mathbf{x}-\mathbf{x}_{0})=\sum\limits_{d=0}^{\infty} \frac{1}{d!}\left[\sum\limits_{|\alpha|=d} \frac{|\alpha|!}{\alpha!}D^{\alpha}f(\mathbf{x}_{0})(\mathbf{x}-\mathbf{x}_{0})^\alpha\right]$$
$\alpha$ è il **multi-indice**, definito come un vettore $(\alpha_{1},\ldots,\alpha_{N})$ in $\mathbb{N}^{N}$ dove ogni componente è usato per rappresentare il numero di derivazioni in quell'indice. $\lvert \alpha \rvert\equiv\alpha_{1}+\alpha_{2}+\ldots+\alpha_{N}$ si dice lunghezza del multi-indice. Inoltre definiamo il suo fattoriale come $\alpha!=\alpha_{1}!\alpha_{2}!\ldots\alpha_{N}!$. La notazione $\mathbf{x}^{\alpha}$ rappresenta il monomio $x_{1}^{\alpha_{1}}x_{2}^{\alpha_{2}}\ldots x_{N}^{\alpha_{N}}$. $D^{\alpha}$ è l'[[operatore]] di derivazione corrispondente a quel multi-indice tale che
$$D^{\alpha}=\frac{ \partial ^{\lvert \alpha \rvert } }{ \partial^{\alpha_{1}}x_{1}\ldots\partial^{\alpha_{N}}x_{N} } $$
Per esempio, in $\mathbb{N}^{3}$, il multi-indice $(1,0,2)$ rappresenta una derivazione nella prima variabile, nessuna nella seconda e due nella terza, quindi corrisponde all'operatore
$$D^{(1,0,2)}=\frac{ \partial ^{3} }{ \partial x_{1}\partial ^{2}x_{3} } $$
e il monomio associato sarebbe $\mathbf{x}^{(1,0,2)}=x_{1}x_{3}^{2}$. Il polinomio $Q_{d}$ è
$$Q_{d}=\sum_{\lvert \alpha \rvert =d} \frac{\lvert \alpha \rvert !}{\alpha!} D^{\alpha}f(\mathbf{x}_{0})(\mathbf{x}-\mathbf{x}_{0})^{\alpha}$$
che racchiude tutte le possibili derivate di $d$-esimo grado.


Nel caso $\mathbf{x}_{0}=\mathbf{0}$ si ha
$$f(\mathbf{x})=\sum_{d=0}^{\infty} \frac{1}{d!}Q_{d}(\mathbf{x})=\sum_{d=0}^{\infty} \frac{1}{d!}\left[ \sum_{\lvert \alpha \rvert =d} \frac{\lvert \alpha \rvert !}{\alpha!} D^{\alpha}f(\mathbf{0})\mathbf{x}^{\alpha}  \right]$$
