---
wiki-publish: true
tags:
  - spazi-metrici
---
Lo spazio $(\mathbb{R}^{N},||\cdot||_2)$ è uno [[Spazio metrico completo]]
*Dimostrazione.* La dimostrazione per $N = 1$ è stata data nel corso precedente. Poniamo quindi $N > 1$.
Consideriamo una [[Successione di Cauchy]] $\{x_n\}_{n\in\mathbb{N}} \subset \mathbb{R}^N$, dotato della norma euclidea, ovvero
$\forall\varepsilon>0\;\exists\bar{n}\in\mathbb{N}\;|\;\forall m,n\geq\bar{n}\; ||x^{m} - x^{n}||_{2}$ .
In particolare, usando l'[[Equivalenza di norme]],
$\forall\varepsilon>0\;\exists\bar{n}\in\mathbb{N}\;|\;\forall m,n\geq\bar{n}\; ||x^{m} - x^{n}||_{\infty}$ .
Ne consegue che la successione delle componenti $\{x^n_k \}_{n\in\mathbb{N}} \subset \mathbb{R}$ è di Cauchy in $\mathbb{R}$ per ogni $k = 1, . . . , N$.
Sfruttiamo ora che $(\mathbb{R}, |\cdot|)$ è uno spazio metrico completo: ognuna di queste successioni converge ad un punto $\bar{x}_k \in \mathbb{R}$. In particolare, per ogni $k$, $\forall\varepsilon>0\;\exists\hat{n}_k\in\mathbb{N}\; |\; \forall n \geq \hat{n}_k\; |x^n_k − x_k | < \varepsilon$.
Sia $x = (x_1,...,x^N)\in\mathbb{R}^N$ e ponendo $\hat{n}=\max{\{\hat{n}_1,...,\hat{n}^N}\}$, troviamo che $\forall\varepsilon>0\;\exists\hat{n}\in\mathbb{N}\;|\;\forall n \geq \hat{n}\; ||x^n − \bar{x}||_{\infty} < \varepsilon$.
Usando l'equivalenza delle norme, troviamo anche
$\forall\varepsilon>0\;\exists\hat{n}\in\mathbb{N}\;|\;\forall n \geq \hat{n}\; ||x^n − \bar{x}||_{2} < \varepsilon$