---
wiki-publish: true
tags:
  - calcolo-differenziale
---
Sia $f:A\subseteq\mathbb{R}^{N}\rightarrow\mathbb{R}$ con $A$ aperto. $x^{0}\in A$ e $i,j\in{1,\ldots,N}$. Supponiamo esistano $\frac{\partial^{2}f}{\partial x_{i}\partial x_{j}}$ e $\frac{\partial^{2}f}{\partial x_{j}\partial x_{i}}$ in un intorno di $x^{0}$ e che siano continue un $x^{0}$. Allora
$$\frac{\partial^{2}f}{\partial x_{i}\partial x_{j}}(x^{0}) = \frac{\partial^{2}f}{\partial x_{j}\partial x_{i}}(x^{0})$$
*Dimostrazione.* Per semplicità, $\mathbb{R}^{2}$. Consideriamo $A=B_{r}(x^{0})$ una [[Palla]] centrata in $x^{0}=(x_{0},y_{0})$. Definiamo $F:A \rightarrow\mathbb{R}$
$$F(x,y)=f(x,y)-f(x_{0},y)-f(x,y_{0})+f(x_{0},y_{0})$$
Fissiamo un generico $(x_{1},y_{1})\in A$ e supponiamo $x_{1}>x_{0}$ e $y_{1}>y_{0}$. Definiamo $g:[y_{0},y_{1}]\rightarrow\mathbb{R}$ tale che $g(y)=f(x_{1},y)-f(x_{0},y)$.
$$\begin{align}
F(x_{1},y_{1})&=f(x_{1},y_{1})-f(x_{0},y_{1})-f(x_{1},y_{0})+f(x_{0},y_{0})\\
&=g(y_{1})-g(y_{0})\\
&=g'(\eta)(y_{1}-y_{0})\quad\mbox{(Th. di Lagrange)}\\
&=\left[\frac{\partial f}{\partial y}(x_{1},\eta)-\frac{\partial f}{\partial y}(x_{0},\eta)\right](y_{1}-y_{0})\\
&=[G_{\eta}(x_{1})-G_{\eta}(x_{0})](y_{1}-y_{0})\quad \mbox{con }G_{\eta}=\frac{\partial f}{\partial y}(x,\eta)\\
&=\frac{\partial^{2}f}{\partial x\partial y}(\xi,\eta)(x_{1}-x_{0})(y_{1}-y_{0})\quad\mbox{(Th. di Lagrange)}
\end{align}$$
con $\eta\in]y_{0},y_{1}[$ e $\xi\in]x_{0},x_{1}[$. Definiamo ora $h:[x_{0},x_{1}]\rightarrow\mathbb{R}$ tale che $h=f(x,y_{1})-f(x,y_{0})$.
$$\begin{align}
F(x_{1},y_{1})&=f(x_{1},y_{1})-f(x_{0},y_{1})-f(x_{1},y_{0})+f(x_{0},y_{0})\\
&=h(x_{1})-h(x_{0})\\
&=h'(\alpha)(x_{1}-x_{0})\quad\mbox{(Th. di Lagrange)}\\
&=\left[\frac{\partial f}{\partial x}(\alpha, y_{1})-\frac{\partial f}{\partial x}(\alpha,y_{0})\right](x_{1}-x_{0})\\
&=[H_{\alpha}(y_{1})-H_{\alpha}(y_{0})](x_{1}-x_{0})\quad \mbox{con }H_{\alpha}=\frac{\partial f}{\partial x}(\alpha,y)\\
&=\frac{\partial^{2}f}{\partial y\partial x}(\alpha,\beta)(y_{1}-y_{0})(x_{1}-x_{0})\quad\mbox{(Th. di Lagrange)}
\end{align}$$
con $\alpha\in]x_{0},x_{1}[$ e $\beta\in]y_{0},y_{1}[$. Eguagliando le precedenti affermazioni si trova
$$\frac{F(x_{1},y_{1})}{(y_{1}-y_{0})(x_{1}-x_{0})}=\frac{\partial^2 f}{\partial x\partial y}(\xi,\eta)=\frac{\partial^{2} f}{\partial x \partial y}(\alpha,\beta)$$
Al limite $(x_{1},y_{1})\rightarrow(x_{0},y_{0})$ abbiamo $\xi,\alpha \rightarrow x_{0}$ e $\eta,\beta \rightarrow y_{0}$. Dato che le derivate sono continue in $(x_{0},y_{0})$ vale la tesi.