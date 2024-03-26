Consideriamo il [[campo elettromagnetico]] espresso tramite il [[potenziale vettore]] $\vec{A}$
$$\nabla^{2}\vec{A}(r,t)- \frac{1}{c^{2}}\frac{\partial ^{2}}{\partial t^{2}}\vec{A}(r,t)=-N_{0}J_{T}=0$$
dove $J_{T}$ è la [[corrente]] trasversa alla direzione di propagazione $\vec{k}$, che consideriamo nulla. Il campo elettrico (trasverso) e magnetico si trovano con
$$\vec{E}_{T}=-\frac{\partial \vec{A}}{\partial t}\quad;\quad\vec{B}=\vec{\nabla}\times\vec{A}\tag{1}$$
Allora il potenziale vettore, risolvendo questa equazione, è
$$A(r,t)=\sum\limits_{k,\lambda}[A_{k,\lambda}(\omega)\hat{e}_{\lambda}e^{i(kr-\omega t)}+\hat{e}A^{*}_{k,\lambda}(\omega)e^{-i(kr-\omega t)}]\tag{2}$$
Noi vogliamo pensare al campo come una serie di fotoni discreti. Dobbiamo quindi quantizzare il campo. Per fare ciò bisogna:
1. trovare l'[[Hamiltoniana]] $H(A(r,t))$
2. trovare le variabili canoniche del campo $q$ e $p$
3. "promuovere" variabili a [[operatore|operatori]] e imporre regole di commutazione

Cerchiamo $q$. Considerando un sistema chiuso dove non esce energia di un certo volume, la densità di energia $U$ è
$$U=\frac{1}{2}\int \left[\epsilon_{0}\vec{E}_{T}(r,t)\cdot\vec{E}_{T}(r,t)+ \frac{1}{\mu_{0}}\vec{B}(r,t)\cdot\vec{B}(r,t)\right]dV$$
Dato che il campo elettrico è trasversale, in mancanza di cariche il campo magnetico ha una sola possibile orientazione ed è ortogonale rispetto sia al campo elettrico che alla direzione di propagazione.

Usando $(1)$ e $(2)$, il campo elettrico può essere espresso come
$$\vec{E}(r,t)=\sum\limits_{k,\lambda}[i\omega_{k}\hat{e}_{k}A_{k,\lambda}(\omega)e^{i(\vec{k}\cdot\vec{r}-\omega t)}-i\omega_{k}\hat{e}_{\lambda}A^{*}_{k,\lambda}(\omega)e^{-i(\vec{k}\cdot\vec{r}-\omega t)}]$$
e quello magnetico
$$\vec{B}(r,t)=\sum\limits_{k,\lambda}(i\vec{k}\times\vec{e}_{\lambda})...$$
Ora calcolo $\vec{E}_{T}(r,t)\cdot\vec{E}_{T}(r,t)$
$$\frac{\epsilon_{0}}{2}\int \Big[\sum\limits_{k,\lambda}i\omega_{k}\hat{e}_{\lambda}A_{k,\lambda}(\omega)\hat{e}^{i\left(kr-\omega t\right)}\sum\limits_{k',\lambda'}i\omega_{k'}\hat{e}_{\lambda'}A_{k',\lambda'}(\omega)e^{i(k'r-\omega t)}+$$
$$+\sum\limits_{k,\lambda}i\omega_{k}\hat{e}_{\lambda}A^{*}_{k,\lambda}(\omega)\hat{e}^{-i(kr-\omega t)}\sum\limits_{k',\lambda'}i\omega_{k'}\hat{e}_{\lambda'}A^{*}_{k',\lambda'}(\omega)e^{-i\left(k'r-\omega t\right)}-$$
$$-2\sum\limits_{k,\lambda}i\omega_{k}\hat{e}_{\lambda}A_{k,\lambda}\left(\omega\right)\hat{e}^{i(kr-\omega t)}\sum\limits_{k',\lambda'}i\omega_{k'}\hat{e}_{\lambda'}A^{*}_{k',\lambda'}(\omega)e^{-i(k'r-\omega t)}\Big]dV$$
Ricordo che $\hat{e}_\lambda\cdot\hat{e}_{\lambda'}=\delta_{\lambda,\lambda'}$ e che
$$\int e^{i(k\pm k')r}dV=V\delta(k\mp k')$$
La densità di energia elettrica $U_{E}$ è
$$U_{E}=V \frac{\epsilon_{0}}{2}\Big[-\sum\limits_{k,\lambda}\omega^{2}_{k}A_{k,\lambda}(\omega)A_{-k,\lambda}(\omega)e^{-2i\omega t}+\sum\limits_{k,\lambda}\omega^{2}A^{*}_{k,\lambda}(\omega)A^{*}_{-k,\lambda}(\omega)e^{2i\omega t}+$$
$$+ 2\sum\limits_{k,\lambda}\omega^{2}_{k}A_{k,\lambda}(\omega)A^{*}_{k,\lambda}(\omega) \Big]$$
Si può anche calcolare la densità di energia magnetica $U_{B}$ con lo stesso procedimento. Allora l'energia totale è
$$U_{E}+U_{B}=\sum\limits_{k,\lambda}2\epsilon_{0}V\omega_{k}^{2}A_{k,\lambda}(\omega)A^{*}_{k,\lambda}(\omega)$$
Cerchiamo $\dot{q}$ e $\dot{p}$.
$$\dot{q}=\frac{\partial H}{\partial p}\quad;\quad \dot{p}=- \frac{\partial H}{\partial q}$$
$$A_{k,\lambda}=\frac{1}{\sqrt{4\epsilon_{0}V\omega_{k}^{2}}}[\omega_{k}q_{k,\lambda}+ip_{k,\lambda}]\quad;\quad A^{*}_{k,\lambda}=\frac{1}{\sqrt{4\epsilon_{0}V\omega_{k}^{2}}}[\omega_{k}q_{k,\lambda}-ip_{k,\lambda}]$$
Allora
$$E=\sum\limits_{k,\lambda} \frac{1}{2}(p^{2}_{k,\lambda}+\omega^{2}q^{2}_{k,\lambda})$$
Promuoviamo $A$ ad un operatore
$$A_{k,\lambda}=\sqrt{\frac{\hbar}{2\epsilon_{0}V\omega_{k}}}\hat{a}_{k,\lambda}\quad;\quad A_{k,\lambda}=\sqrt{\frac{\hbar}{2\epsilon_{0}V\omega_{k}}}\hat{a}^{+}_{k,\lambda}$$
con $\hat{a}$ e $\hat{a}^{+}$ sono gli [[operatori di creazione e distruzione]]. Anche l'Hamiltoniana viene promossa da
$$H=\sum\limits_{k,\lambda}\epsilon_{0}V\omega^{2}_{k}(A_{k,\lambda}A^{*}_{k,\lambda}+A^{*}_{k,\lambda}A_{k,\lambda})$$
a
$$\hat{H}=\sum\limits_{k,\lambda} \frac{\hbar\omega_{k}}{2}[\hat{a}_{k,\lambda}\hat{a}_{k,\lambda}^{+}+\hat{a}^{+}_{k,\lambda}\hat{a}_{k,\lambda}]$$
e le regole di commutazione devono essere
$$[\hat{q}_{k,\lambda},\hat{p}_{k,\lambda}]=-i \Leftrightarrow [\hat{a}_{k,\lambda},\hat{a}_{k,\lambda}^{+}]=\delta_{k,k',\lambda,\lambda'}$$

Controlliamo la commutazione di $\hat{H}$ con gli operatori di distruzione.
$$[\hat{H},\hat{a}^{+}]=\hbar\omega\left[\left(\hat{a}^{+}\hat{a} + \frac{1}{2}\right), \hat{a}^{+}\right]=\hbar\omega(\hat{a}^{+}\hat{a}\hat{a}^{+}-\hat{a}^{+}\hat{a}^{+}\hat{a})=\hbar\omega\hat{a}^{+}(\hat{a}\hat{a}^{+}-\hat{a}^{+}\hat{a})=\hbar\omega\hat{a}^{+}$$
e calcoliamo anche l'azione dell'Hamiltoniana sull'operatore $\hat{a}^{+}$
$$H(\hat{a}^{+}|?\rangle)=(H\hat{a}^{+}-\hat{a}^{+}H+\hat{a}^{+}H)|?\rangle=([H,\hat{a}^{+}]+a^{+}H)|?\rangle=(\hbar\omega\hat{a}^{+}+\hat{a}^{+}E_{n})|?\rangle=$$
$$=(\hbar\omega+E_{n})\hat{a}^{+}|?\rangle$$
Quindi vediamo che l'energia varia di un valore $\hbar\omega$. Da qui è nata l'idea di [[fotone]] come quanto di eccitazione del campo elettromagnetico.

Ora possiamo scrivere il campo elettrico in funzione degli operatori di creazione e distruzione
$$\hat{E}(r,t)=\vec{e}_{i}(i\omega\hat{a}e^{i(kr-\omega t)}-i\omega\hat{a}^{+}e^{-i(kr-\omega t)})(c)=\alpha[\hat{X}\sin(\omega t-kr)+\hat{Y}\cos(\omega t-kr)]$$
con
$$\hat{X}=\frac{1}{2}(\hat{a}^{+}+\hat{a})\quad;\quad\hat{Y}=\frac{1}{2}i(\hat{a}^{+}-\hat{a})$$
che sono gli [[operatori di quadratura]], che sono [[Osservabile|osservabili]].
$$\langle n|\hat{X}|n\rangle=\langle n| \frac{1}{2}(\hat{a}^{+}+\hat{a})|n\rangle=\frac{1}{2}\langle n|\hat{a}^{+}+\hat{a}|n\rangle=\frac{1}{2}[\langle n|\hat{a}^{+}|n\rangle+\langle n|\hat{a}|n\rangle]=$$
$$=\frac{1}{2}[\langle n|n+1\rangle+\langle n|n-1\rangle]=\frac{1}{2}[0 + 0]=0$$
quindi vale anche
$$\langle n|\hat{E}(r,t)|n\rangle=0$$
Quindi il valore di aspettazione del campo elettrico è nullo. Ma visto che il campo elettrico non è in generale nullo (dato che lo possiamo misurare), deve essere soggetto a fluttuazioni: in altre parole, la varianza è non nulla.
$$\Delta E^{2}=\langle n|\hat{E}^{2}|n\rangle-\langle n|\hat{E}^{2}|n\rangle^{2}=\langle n|\hat{E}^{2}|n\rangle$$
dato che il $\langle n|\hat{E}^{2}|n\rangle=0$ per quanto appena trovato. Per calcolare $\langle n|\hat{E}^{2}|n\rangle$ cerco prima come interagiscono $\hat{X}$ e $\hat{Y}$
$$\langle n|\hat{X}^{2}|n\rangle=\langle n| \frac{1}{2}(\hat{a}+\hat{a}) \frac{1}{2}(\hat{a}^{+}+\hat{a})|n\rangle=\frac{1}{2}\langle n|\hat{a}^{+}\hat{a}^{+}+\hat{a}\hat{a}|n\rangle=$$
$$=\frac{1}{4}\langle n|\hat{a}^{+}\hat{a}+\hat{a}\hat{a}^{+}+1-1+1-\hat{a}\hat{a}^{+}+\hat{a}^{+}\hat{a}|n\rangle=\frac{1}{2}\langle n| \hat{a}^{+}\hat{a}+ \frac{1}{2}|n\rangle$$
Se non metto alcun fotone nel sistema, $\hat{a}^{+}\hat{a}$ si annulla, ma rimane una fluttuazione non nulla: $\frac{1}{2}\langle n| \frac{1}{2}|n\rangle$. Questa si chiama **fluttuazione di punto zero**. Ora troviamo le fluttuazioni del campo elettrico
$$\langle n|\hat{E}^{2}|n\rangle=\frac{\hbar\omega}{2\epsilon_{0}V}\left[ \frac{1}{2}\langle n|\hat{a}^{+}\hat{a}+ \frac{1}{2}|n\rangle\right]$$

Qualcosa qualcosa beam splitter e apparato di Mach-Zender (???), digressione per simpatia. Fotoni sovrapposizione di ogni possibile linea temporale.