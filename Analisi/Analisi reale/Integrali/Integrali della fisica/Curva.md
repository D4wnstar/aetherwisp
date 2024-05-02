---
tags:
  - integrali
  - integrali-fisica
---
Si dice **curva** una funzione continua $γ : I → \mathbb{R}^N$ dove $I$ è un intervallo. L’immagine $γ(I)$ si dice **sostegno della curva**.
Una curva si dice *limitata* (*illimitata*) se il suo sostegno è un insieme limitato (illimitato).
Una curva si dice *chiusa* se $I = [a,b]$ è un intervallo chiuso e limitato e vale $\gamma(a) = \gamma(b)$.
Una curva si dice *semplice* se è iniettiva eccetto al più agli estremi, cioè se e solo se vale $\gamma(t_1)=\gamma(t_2)\;\Rightarrow\;t_1=t_2\;o\;t_1=a,\;t_2=b$.
Una curva si dice *regolare* se è di classe $C^1$ e vale $\gamma'(t)\neq0\;\forall t\in \mathring{I}$. Si dice *regolare a tratti* se esiste una partizione $P$ dell'intervallo $I$ 
$a=x_0<x_1<x_2<\cdots<x_N=b$
tale che la restrizione su $[x_{i-1},x_i]$ è una curva regolare.

Posso considerare i vettori tangenti $\hat{\tau}$ come
$\hat{\tau}:\mathring{I}\rightarrow\mathbb{R}^{N}\quad\hat{\tau}(t)= \frac{\gamma'(t)}{||\gamma'(t)||}$

Due curve regolari $\gamma_1:I_1\rightarrow\mathbb{R}^N$ e $\gamma_2:I_2\rightarrow\mathbb{R}^N$ si dicono *equivalenti* se hanno lo stesso sostegno ed esiste un $C^1$-diffeomorfismo $\varphi:I_1\rightarrow I_2$ tale che $\gamma_1=\gamma_2\circ\varphi$. Si dirà che le due curve hanno la stessa orientazione se $\varphi'(s)>0\;\forall s\in I_1$.