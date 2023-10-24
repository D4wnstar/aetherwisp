L'energia potenziale di una stella in forma differenziale è
$$dU=- \frac{GM(r_{0})}{r_{0}}dm$$
dove $M(r_{0})$ è la massa della [[stelle|stella]] entro il raggio $r_{0}$. In questa formula siamo nell'approssimazione che la massa sia contenuta tutta in un punto al centro della stella, che è una buona approssimazione per quanto riguarda la forza gravitazionale. Sfruttando la conservazione dell'energia
$$\frac{1}{2}\left( \frac{dr}{dt} \right)^{2}= \frac{GM(r_{0})}{r}- \frac{GM(r_{0})}{r_{0}}$$
Calcoliamo il tempo che ci mette un oggetto a cadere da $r_{0}$ al centro della stella puramente per forza gravitazionale
$$\tau_{FF}=\int_{0}^{\tau_{FF}}dt=-\int_{r_{0}}^{0}2GM(r_{0})\left( \frac{1}{r}- \frac{1}{r_{0}} \right)^{- \frac{1}{2}}dr=$$
$$=\left( \frac{r_{0}^{3}}{2GM(r_{0})} \right)^{\frac{1}{2}}\underbrace{\int_{0}^{1}\left( \frac{x}{1-x} \right)^{\frac{1}{2}}dx}\limits_{\frac{\pi}{2}}=\left( \frac{3\pi}{32G\rho} \right)^{\frac{1}{2}}$$
usando la densità con volume sferico. Nel caso del Sole, che ha una densità $\rho_{\odot}=1.4g/cm^3$ ha un tempo di caduta libera di circa mezz'ora, il che vale a dire che se non ci fosse nessuna forza che spinge verso l'esterno, collasserebbe su se stesso in circa mezz'ora.

![[Introduzione all'Astrofisica/Disegni/Equilibrio idrostatico|Equilibrio idrostatico|50%|center]]

$$- \frac{GM(r)}{r^{2}}dm-AdP=0$$
con $dP$ il gradiente di pressione negativo. Quindi la pressione diminuisce all'aumentare del raggio.
$$\frac{dP(r)}{dr}=- \frac{GM(r)\rho(r)}{r^{2}}$$
$$\int_{0}^{r_{\star}}4\pi r^{3} \frac{dP}{dr}=- \int_{0}^{r_{\star}} \frac{GM(r)\rho(r)4\pi r^{2}}{r}dr=P(r)4\pi r^{3}|_{0}^{r_{\star}}-3\int_{0}^{r_{\star}}P(r)4\pi r^{2}dr$$
sapendo che $dM(r)=\rho(r)4\pi r^{2}dr$. Allora l'energia gravitazionale della stella, cioè una delle due energie che mantengono l'equilibrio idrostatico, è
$$\boxed{E_{gr}=-3\bar{P}V}$$
che si tratta del **teorema viriale**, con $\bar{P}$ la pressione media del sistema. Assumendo un gas ideale e $PV=nk_{B}T$ 
$$\boxed{\bar{P}= - \frac{E_{gr}}{3V}=\frac{2}{3} \frac{E_{T}}{V}}$$
con $E_{T}=\frac{3}{2}Nk_{B}T$ l'energia termica della stella. In altre parole
$$\bar{P}V= \frac{2}{3}E_{T}$$
L'energia totale della stella è
$$E_{tot}=E_{T}+E_{gr} = -E_{T} \Rightarrow \boxed{E_{T}=-\frac{E_{gr}}{2}}$$
Se la stella si scalda, la stella si espande e diventa meno densa.

Analizziamo l'energia gravitazionale di una stella
$$E_{gr}=-\int_{0}^{r_{\star}} \frac{GM(r)\rho(r)4\pi^{2}}{r}dr=\ldots$$
Assumiamo che la densità $\rho$ sia costante (cosa non vera, ma semplifica)
$$\ldots=\int_{0}^{r_{\star}} \frac{G\frac{4\pi}{3}r^{3}\rho^{2}4\pi r^{2}}{r}dr=- \frac{3}{5} \frac{GM^{2}}{r_{\star}}$$
Il valore vero (ottenuto senza assumere che $\rho$ sia costante) è
$$\boxed{E_{gr}=- \frac{GM^{2}}{r_{\star}}}$$
Usando il teorema viriale si può giungere alla pressione. Per esempio troviamo la pressione media del sole
$$\bar{P}_{\odot}\simeq \frac{1}{3} \frac{E_{gr}}{2} \frac{1}{V}\simeq \frac{1}{3} \frac{GM^{2}_{\odot}}{\frac{4}{3}\pi r^{4}_{\odot}}$$
che mettendo i numeri si trova essere circa $10^{9}$ Atm (o $1.013\cdot10^6$ nel sistema CGS), che è meno della pressione necessaria per formare un diamante.

Cerco ora la **temperatura viriale**, che non è altro che la temperatura trovata dal teorema del viriale. Possiamo calcolare l'energia potenziale del Sole
$$U= \frac{3}{2}Nk_{B}T= \frac{1}{2} \frac{GM^{2}_{\odot}}{r_{\odot}}\simeq \frac{1}{2} \frac{GM_{\odot}N\bar{m}}{r_{\odot}}$$
dove abbiamo semplificato una massa solare come massa delle particelle che lo compongono: $\bar{m}$ è la massa media delle particelle, in questo caso protoni e elettroni (cioè quella dell'idrogeno) e $N$ è il numero di particelle. Dato che la massa dell'elettrone è minuscola in paragone a quella del protone, si ha
$$\bar{m}= \frac{m_{p}+m_{e}}{2}= \frac{m_{H}}{2}\simeq 1.7\cdot10^{-24}$$
con $m_{H}$ la massa dell'idrogeno.
$$kT_{vir}\simeq \frac{GM_{\odot}m_{H}}{6r_{\odot}}=5.4\times10^{-10}\mbox{erg}$$
estraendo la temperatura si trova la temperatura (media)
$$T_{vir}=4\times10^{6}\mbox{ K}$$

Prendo un elemento di massa sferico (un "guscio")
$$dM(r)=\rho(r)4\pi r^{2}dr$$
e posso riscriverlo per trovare una forma dell'**equazione di continuità della massa** 
$$\boxed{\frac{dM(r)}{dr}=4\pi r^{2}\rho(r)}$$
