$$\frac{1}{k_{B}T}=\frac{1}{\epsilon}\ln\left( \frac{N\epsilon}{E}-1\right)$$
Calcolare $E(T)$.
$$e^{\frac{\epsilon}{k_{B}T}}=\frac{N\epsilon}{E}-1$$
$$\frac{N\epsilon}{E}=1+e^{\frac{\epsilon}{k_{B}T}} \Rightarrow E=\frac{N\epsilon}{1+e^{\frac{\epsilon}{k_{B}T}}}$$
![[Drawing 2023-10-10 09.08.09.excalidraw|center]]

In generale, per quantità piccole, conviene sempre fare uno sviluppo in serie che calcolare la derivata.

---
Calcoliamo la densità di energia.
$$g(E)=\frac{1}{V}\sum\limits_{\bar{p}}\delta\left(E- \frac{p^{2}}{2m}\right) \Rightarrow \frac{4\pi}{h^{3}}\int_{0}^{\infty}dp\;p^{2}\delta\left(E- \frac{p^{2}}{2m}\right)$$
Uso la sostituzione
$$y = \frac{p^{2}}{2m}\quad;\quad p=2my \quad;\quad dp=\frac{\sqrt{2m}}{2\sqrt{y}}dy$$
Allora ho
$$g(E)=4\pi\int_{0}^{\infty}dy \frac{\sqrt{2m}}{2\sqrt{y}}2my \delta(E-y)=\frac{4\pi}{h^{3}} \frac{(2m)^{\frac{3}{2}}}{2}\int_{0}^{\infty}dy\;y^{\frac{1}{2}}\delta(E-y)=$$
$$=\frac{4\pi}{h^{3}}\frac{(2m)^{\frac{3}{2}}}{2} \int_{0}^{\infty}dy\; y^{\frac{1}{2}}\delta(E-y)=\frac{2}{\sqrt{\pi}} \left(\frac{2\pi m}{h^{2}}\right)^{\frac{3}{2}}$$
dunque sostituendo l'energia ho
$$\boxed{g(E)=\frac{2}{\sqrt{\pi}} \left(\frac{2\pi m}{h^{2}}\right)^\frac{3}{2}\sqrt{E}}$$

---
