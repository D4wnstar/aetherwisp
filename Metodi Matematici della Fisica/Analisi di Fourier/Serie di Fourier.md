Data una [[funzione generalmente continua]] $f(x)$ definita su un intervallo $]-L,L[$, la sua espansione in **serie trigonometrica di Fourier** è
$$f(x)=\alpha_{0}+\sum\limits_{n=1}^{\infty}\alpha_{n}\cos\left(\frac{n\pi}{L}x\right)+\sum\limits_{n=1}^{\infty}\beta_{n}\sin\left(\frac{n\pi}{L}x\right)$$
dove i coefficienti $\alpha_{0}$, $\alpha_{n}$ e $\beta_{n}$ sono
$$\begin{cases}
\alpha_{0}=\frac{1}{2L}\int_{-L}^{+L}f(x)dx \\
\alpha_{n}=\frac{1}{L}\int_{-L}^{+L}f(x)\cos(\frac{n\pi}{L}x)dx \\
\beta_{n}=\frac{1}{L}\int_{-L}^{+L}f(x)\sin(\frac{n\pi}{L}x)dx
\end{cases}$$
Valgono le seguenti proprietà
1. se $f(x)$ è continua con derivata generalmente continua e vale $f(L)=f(-L)$, allora la serie converge uniformemente
2. se $f(x)$ è generalmente continua con derivata generalmente continua, la serie converge in ogni punto e ha per somma la $f(x)$ in tutti i punti in cui è continua. Nei punti in cui non è continua e agli estremi, ha per somma la "media" $\frac{1}{2}[f(x_{0}^{+})+f(x_{0}^{-})]$
3. se $f(x)$ è pari, allora $\alpha_{0}=\frac{1}{L}\int_{0}^{L}f(x)dx$, $\alpha_{n}=\frac{2}{L}\int_{0}^{L}f(x)\cos\left(\frac{n\pi}{L}x\right)dx$ e $\beta_{n}=0$; un risultato analogo vale se $f(x)$ è dispari
4. se vale $\sum\limits_{n}|\alpha_{n}|+\sum\limits_{n}|\beta_{n}|<\infty$, allora $f(x)$ è continua e $f(L)=f(-L)$. Questo segue dalla definizione di convergenza totale

