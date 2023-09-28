---
tags:
  - serie
---
Data una successione di numeri reali $\{a_n\}_{n\in \mathbb{N}}$ di numeri reali, definisco per ogni $n\in \mathbb{N}$ la **somma parziale**

$s_{n}=\sum\limits_{i=0}^{n}a_{i}=a_{0}+a_{1}+\cdots+a_{n-1}+a_{n}$

La coppia di successioni $(\{a_n\}_{n\in \mathbb{N}},\;\{s_{n}\}_{n\in \mathbb{N}})$ si dice **serie** di termine generico $a_n$ e si indica con il simbolo $\sum\limits_{n=0}^{\infty}a_{n}$. I valori $a_n$ si dicono *termini* della serie. Si chiama **somma** della serie l'elemento $\lim\limits_{n\rightarrow\infty}s_n=\sum\limits_{n=0}^{\infty}a_n = S$, che può essere finito (**serie convergente**) o infinito (**serie divergente**). Può anche darsi che il limite non esista (**serie indeterminata**).

### Serie resto
Data una serie $\sum\limits_{n=0}^{\infty}a_n$ definisce **serie resto** da un certo $n_{0}\in \mathbb{N}$ in poi la serie $\sum\limits_{n=n_{0}+1}^{\infty}a_n$. Il carattere della serie resto è lo stesso della serie da cui proviene.

### Linearità di serie convergenti
Siano $\sum\limits_{n=0}^{\infty}a_{n}$ e $\sum\limits_{n=0}^{\infty}b_{n}$ due serie convergenti. Allora, per ogni $\lambda,\mu\in \mathbb{R}$, la serie $\sum\limits_{n=0}^{\infty}(\lambda a_{n}+\mu b_{n})$ è convergente e vale $\lambda \sum\limits_{n=0}^{\infty}a_{n}+\mu \sum\limits_{n=0}^{\infty}b_{n}$.

### Condizione necessaria per la convergenza
Se una serie $\sum\limits_{n=0}^{\infty}a_{n}$ converge, allora vale $\lim\limits_{n}a_{n}=0$.