Il **teorema della convergenza dominata** ci dà una condizione per garantire che sia possibile passare al limite dentro un integrale.
### Enunciato
Sia $f_{n}(x)$ una successione di [[Spazi Lp|funzioni sommabili]] su un intervallo $I$ che [[Convergenza puntuale|converge puntualmente]] quasi ovunque per $n \rightarrow \infty$ ad una funzione $f(x)$. Se esiste una funzione $F(x)$ sommabile, tale che, per ogni $n$, sia
$$|f_{n}(x)|\leq F(x)$$
allora
1. anche $f$ è sommabile
2. vale $$\lim\limits_{n \rightarrow\infty}\int_{I}f_{n}(x)dx=\int_{I}f(x)dx$$
La stessa conclusione vale per una famiglia di funzione $f_{\varepsilon}(x)$ dipendente da un parametro continuo $\varepsilon \rightarrow 0$.