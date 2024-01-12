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

La funzione $f$ così trovata può essere vista intuitivamente come una "combinazione lineare infinita" di una "base" costituita dai vettori
$$\left[1,\;\cos\left(\frac{n\pi}{L}x\right),\;\sin\left(\frac{n\pi}{L}x\right)\right]\quad\forall n\in\mathbb{N}$$
Possiamo anche normalizzare questi vettori
$$\left[\frac{1}{\sqrt{2L}},\; \frac{1}{\sqrt{L}} \cos\left(\frac{n\pi}{L}x\right),\; \frac{1}{\sqrt{L}}\sin\left(\frac{n\pi}{L}x\right)\right]\quad\forall n\in\mathbb{N}$$
e ottenere un sistema ortonormale, dove vale $(f^{(m)}, f^{(n)})=\delta_{mn}$, avendo segnato $f^{(n)}$ come la generica funzione. Allora $f$ vale
$$f=\sum\limits_{n=0}^{\infty}a_{n}f_{n}$$
con $a_{0}=\sqrt{2L}\alpha_{0}$, $a_{2n}=\sqrt{L}\alpha_{n}$ e $a_{2n-1}=\sqrt{L}\beta_{n}$. È anche possibile invertire la relazione per ottenere i coefficienti dalle funzione
$$a_{n}=(f_{n},f)$$
