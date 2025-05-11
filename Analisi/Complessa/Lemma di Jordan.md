---
wiki-publish: true
---
Considera l'integrale
$$\int_{-\infty}^{+\infty}f(x)e^{i\nu x}dx$$
con $\nu$ un numero reale diverso da zero. Assumi che la funzione $f(x)$ sia estendibile ad una funzione complessa $f(z)$ [[Funzione meromorfa|meromorfa]] senza [[Singolarità isolata|singolarità]] sull'asse reale. Allora si prenda $\nu>0$ (o $\nu<0$). Considerando $\Gamma$ una semicirconferenza centrata nell'origine, di raggio $R$, posta nel semipiano complesso superiore (o inferiore), se vale la seguente condizione
$$\lim\limits_{R \rightarrow \infty} \max\limits_{z\in\Gamma}|f(z)|=0$$
allora vale anche
$$\lim\limits_{R \rightarrow \infty}\int_{\Gamma}f(z)e^{i\nu z}dz=0$$
e
$$2\pi i\sum\limits_{z_{i}, \text{Im}(z_{i})>0}\text{Res}_{fe^{i\nu z}}(z_{i})=0 \quad \text{se } \nu > 0$$
$$-2\pi i\sum\limits_{z_{i}, \text{Im}(z_{i})<0}\text{Res}_{fe^{i\nu z}}(z_{i})=0 \quad \text{se } \nu < 0$$
