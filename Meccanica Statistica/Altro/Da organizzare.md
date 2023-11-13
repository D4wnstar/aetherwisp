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

$$\frac{1}{V}\ln Z=\frac{1}{V}\sum\limits_{\alpha}\sigma\ln(1+\sigma e^{-\beta \epsilon_{\alpha}}z)=\frac{1}{V}\sum\limits_{\alpha}\sigma\ln(1+\sigma e^{-\beta(\epsilon_{\alpha}-\mu)})$$
con $z=e^{\beta \mu}$ la *fugacità*. Si ha
$$Z=\sum\limits_{n=0}^{\infty}e^{\beta\mu n}\sum\limits_{\{n_{\alpha}\}}\delta\left(n-\sum\limits_{\alpha}n_{\alpha}\right)e^{-\beta E \{n_{\alpha}\}}$$
Cerco la media
$$\langle n_{\gamma} \rangle=- \frac{\partial \ln Z}{\beta\partial \epsilon_{\gamma}}= \frac{1}{Z}\left\{- \frac{1}{\beta} \frac{\partial Z}{\beta\partial \epsilon_{\gamma}}\right\}=$$
$$=\frac{1}{Z}\left\{\sum\limits_{N=0}^{\infty} e^{\beta\mu N} \sum\limits_{\{n_{\alpha}\}} \delta\left(N-\sum\limits_{\alpha}n_{\alpha}\right)e^{-\beta E \{n_{\alpha}\}} \left[- \frac{1}{\beta} \frac{\partial }{\beta\partial \epsilon_{\alpha} }(-\beta E \{n_{\alpha}\})\right]\right\}=$$
$$=\frac{1}{Z}\left\{ \sum\limits_{N=0}^{\infty}e^{\beta \mu N}\sum\limits_{\{n_{\alpha}\}} \delta(N-\sum\limits_{\alpha}n_{\alpha})e^{-\beta E_{\alpha}n_{\alpha}y}n_{\gamma} \right\}$$

Usando la formula per $\ln Z$ troviamo
$$\langle n_{\gamma} \rangle=- \frac{1}{\beta}\frac{\partial }{\partial \epsilon_{\gamma}}\sum\limits_{\sigma}\sigma\ln(1+\sigma e^{-\beta \epsilon_{\alpha}}z)=- \frac{1}{\beta} \frac{\partial }{\partial \epsilon_{\alpha}}[\sigma\ln(1+\sigma e^{-\beta \epsilon_{\gamma}})z]=$$
$$=\frac{\sigma}{1+\sigma e^{-\beta \epsilon_{\gamma}}z}\sigma e^{-\beta \epsilon_{\gamma}}z= \frac{z}{e^{\beta \epsilon_{\gamma}}+\sigma z}$$
che ci dà l'*occupazione media dello stato*.
Questa formula cambia per fermioni e bosoni
$$\mbox{Fermioni: }\frac{1}{e^{\beta(E_{\gamma}-\mu)}+1}\quad\mbox{Bosoni: }\frac{1}{e^{\beta(E_{\gamma}-\mu)}-1}$$
ossia si ha $z=1$ e cambia il segno al denominatore.

Esiste un terzo tipo (teorico) di particelle chiamate *boltzmannioni*. Se prendiamo le funzioni di occupazioni di stato $\varphi_{\alpha_{1}}(x_{1})\varphi_{\alpha_{2}}(x_{2})\ldots\varphi_{\alpha_{N}}(x_{N})$ abbiamo
$$g \{n_{\alpha}\}= \frac{N!}{\prod\limits_{\alpha}n_{\alpha}!} \Rightarrow \tilde{g}\{n_{\alpha}\}=\frac{1}{N!} \frac{N!}{\prod_{\alpha}n_{\alpha}!}= \frac{1}{\prod_{\alpha}n_{\alpha}!}$$
$$Z_{\alpha}=\sum\limits_{N=0}^{\infty}e^{\beta \mu N}\sum\limits_{\{n_{\alpha}\}}\delta\left(N-\sum\limits_{\alpha}n_{\alpha}\right) \frac{1}{\prod\limits_{\alpha}n_{\alpha}!}e^{- \beta\sum\limits_{\alpha}n_{\alpha}\epsilon_{\alpha}}=$$
$$=\sum\limits_{\{n_{\alpha}\}}e^{\beta \mu \sum\limits_{\alpha}n_{\alpha}}\sum\limits_{\{n_{\alpha}\}}\delta\left(N-\sum\limits_{\alpha}n_{\alpha}\right) \prod\limits_{\alpha} \frac{e^{-\beta n_{\alpha}\epsilon_{\alpha}}}{n_{\alpha}!}=\sum\limits_{\{n_{\alpha}\}}\prod\limits_{\alpha}\frac{e^{-\beta(\epsilon_{\alpha} -\mu)n_{\alpha}}}{n_{\alpha}!}$$
Calcolo
$$Z_{B}=\sum\limits_{n_{1}}\sum\limits_{n_{2}}\ldots\prod\limits_{\alpha} \frac{e^{-\beta (\epsilon_{\alpha}-\mu)n_{\alpha}}}{n_{\alpha}!}=\prod\limits_{\alpha}\exp(e^{-\beta(\epsilon_{\alpha}-\mu)})$$
$$\frac{1}{V} \ln Z_{B}= \frac{1}{V}\sum\limits_{\alpha}\ln[\exp(e^{-\beta (\epsilon_{\alpha}-\mu)})]=\frac{1}{V}\sum\limits_{\alpha}e^{-\beta(\epsilon_{\alpha}-\mu)}$$
Si trova analogamente a sopra
$$\langle n_{\gamma}^{B} \rangle=e^{-\beta(\epsilon_\alpha-\mu)}$$
