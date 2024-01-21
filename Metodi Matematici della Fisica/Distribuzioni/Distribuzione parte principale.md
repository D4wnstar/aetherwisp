La **distribuzione parte principale**, scritta $\mathscr{P}(1/x)$, è una [[distribuzione]] definita come
$$\left\langle \mathscr{P} \frac{1}{x},\varphi\right\rangle= \mathscr{P}\int_{-\infty}^{+\infty} \frac{1}{x}\varphi(x)dx=\lim\limits_{\sigma \rightarrow 0}\left[\int_{-\infty}^{-\sigma} \frac{1}{x}\varphi(x)dx + \int_{+\sigma}^{+\infty} \frac{1}{x}\varphi(x)dx\right]$$
con $\sigma>0$, dove $\mathscr{P}$ denota la [[parte principale di Cauchy]]. Dalla definizione segue che è il limite per $\sigma \rightarrow 0$ della funzione $u_\sigma(x)$ definita come
$$u_{\sigma}(x)= \begin{cases}
0&\text{ per }|x|<\sigma \\
\frac{1}{x}&\text{ per }|x|>\sigma
\end{cases}$$
### Risultati utili
La parte principale ha una [[trasformata di Fourier]]
$$\mathscr{F}\left(\mathscr{P} \frac{1}{x}\right)=\pi i\text{sgn}(\omega)=\begin{cases}
-\pi i & \text{per }\omega<0 \\
+\pi i & \text{per }\omega>0
\end{cases}$$
e antitrasformata
$$\mathscr{F}^{-1}\left(\mathscr{P} \frac{1}{x}\right)=\frac{1}{2i}\text{sgn}(x)$$
