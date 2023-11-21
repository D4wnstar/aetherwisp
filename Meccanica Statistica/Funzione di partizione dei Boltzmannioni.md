La funzione di ripartizione di [[boltzmannioni]] coincide con la funzione di gran partizione classica. Consideriamo
$$\frac{\ln Z}{V}= \frac{1}{V}\sum\limits_{\alpha}e^{\beta(\epsilon_{\alpha}-\mu)}$$
Prendiamo un sistema di boltzmannioni (massivi) in una scatola. Prendendo come etichette i valori di impulso delle particelle
$$\frac{1}{V}\sum\limits_{\bar{p}}e^{\beta(\epsilon_{p}-\mu)}=\int dE\;g(E)^{-\beta(E-\mu)}$$
dove la densità di stati $g(E)=\frac{1}{V}\sum\limits_{\bar{p}}\delta(\frac{p^{2}}{2m}-E)$. Possiamo riscrivere $g(E)$ come
$$g(E)=\frac{2}{\sqrt{\pi}} \left( \frac{2m\pi}{h^{2}} \right)^{\frac{3}{2}}\sqrt{E}\theta(E)\equiv c\sqrt{E}\theta(E)$$
Dunque
$$\frac{\ln Z}{V}=c\int_{0}^{\infty}dE\;\sqrt{E}e^{-\beta E}z=zc \frac{1}{\beta^{\frac{3}{2}}}\int_{0}^{\infty}dy\;y^{\frac{1}{2}}e^{-y}=2c(k_{B}T)^{\frac{3}{2}}\int_{0}^{\infty}dy\;y^{\frac{3}{2}-1}e^{-y}=$$
$$=z \frac{2}{\sqrt{\pi}}\left( \frac{2m\pi k_{B}T}{h^{2}} \right)^{\frac{3}{2}} \frac{\sqrt{\pi}}{2}=\frac{z}{\lambda_{T}^{3}}$$
$$Z=\sum\limits_{N=0}^{\infty}z^{N} \frac{V^{N}}{\lambda_{T}^{3}} \frac{1}{N!}=\sum\limits_{N=0}^{\infty} \frac{1}{N!} \left(\frac{zV}{\lambda_{T}^{3}}\right)^{N}$$
$$Z_{d}=\exp\left[\frac{zV}{\lambda_{T}^{3}}\right]\Rightarrow \frac{1}{V}\ln Z_{d}= \frac{1}{V} \frac{zV}{\lambda_{T}^{3}}=\frac{z}{\lambda_{T}^{3}}$$
