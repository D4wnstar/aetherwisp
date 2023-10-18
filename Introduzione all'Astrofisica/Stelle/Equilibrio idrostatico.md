L'energia potenziale di una stella in forma differenziale è
$$dU= \frac{GM(r_{0})}{r_{0}}dm$$
dove $M(r_{0})$ è la massa della [[stelle|stella]] entro il raggio $r_{0}$. In questa formula siamo nell'approssimazione che la massa sia contenuta tutta in un punto al centro della stella, che è una buona approssimazione per quanto riguarda la forza gravitazionale. Sfruttando la conservazione dell'energia
$$\frac{1}{2}\left( \frac{dr}{dt} \right)^{2}= \frac{GM(r_{0})}{r}- \frac{GM(r_{0})}{r_{0}}$$
Calcoliamo il tempo che ci mette un oggetto a cadere da $r_{0}$ al centro della stella puramente per forza gravitazionale
$$\tau_{FF}=\int_{0}^{\tau_{FF}}dt=-\int_{r_{0}}^{0}2GM(r_{0})\left( \frac{1}{r}- \frac{1}{r_{0}} \right)^{- \frac{1}{2}}dr=$$
$$=\left( \frac{r_{0}^{3}}{2GM(r_{0})} \right)^{\frac{1}{2}}\underbrace{\int_{0}^{1}\left( \frac{x}{1-x} \right)^{\frac{1}{2}}dx}\limits_{\frac{\pi}{2}}=\left( \frac{3\pi}{32G\rho} \right)^{\frac{1}{2}}$$
usando la densità con volume sferico. Nel caso del Sole, che ha una densità $\rho_{\odot}=1.4g/cm^3$ ha un tempo di caduta libera di circa mezz'ora, il che vale a dire che se non ci fosse nessuna forza che spinge verso l'esterno, collasserebbe su se stesso in circa mezz'ora.

![[Introduzione all'Astrofisica/Disegni/Equilibrio idrostatico|Equilibrio idrostatico|50%|center]]

$$- \frac{GM(r)}{r^{2}}dm+AdP=0$$
con $dP$ il gradiente di pressione negativo. Quindi la pressione diminuisce all'aumentare del raggio.
$$\frac{dP(r)}{dr}=- \frac{GM(r)\rho(r)}{r^{2}}$$
$$\int_{0}^{r_{\star}}4\pi r^{3} \frac{dP}{dr}=- \int_{0}^{r_{\star}} \frac{GM(r)\rho(r)4\pi r^{2}}{r}dr=P(r)4\pi r^{3}|_{0}^{r_{\star}}-3\int_{0}^{r_{\star}}P(r)4\pi r^{2}dr$$
sapendo che $dM(r)=\rho(r)4\pi r^{2}dr$. Allora l'energia gravitazionale della stella, cioè una delle due energie che mantengono l'equilibrio idrostatico, è
$$\boxed{E_{gr}=-3\bar{P}V}$$
che si tratta del **teorema viriale**, con $\bar{P}$ la pressione media del sistema. Assumendo un gas ideale e $PV=nk_{B}T$ 
$$\bar{P}= - \frac{E_{gr}}{3V}=\frac{2}{3} \frac{E_{T}}{V}$$
con $E_{T}=\frac{3}{2}Nk_{B}T$ l'energia termica della stella. In altre parole
$$\bar{P}V= \frac{2}{3}E_{T}$$
L'energia totale della stella è
$$E_{tot}=E_{T}+E_{gr}=-E_{T}=\frac{E_{gr}}{2}$$
Se la stella si scalda, la stella si espande e diventa meno densa.