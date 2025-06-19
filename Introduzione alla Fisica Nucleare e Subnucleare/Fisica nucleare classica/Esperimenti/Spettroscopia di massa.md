---
wiki-publish: true
---
La **spettroscopia di massa** è una tecnica per misure ad alta precisione ($\sim10^{-6}u$, con $u$ unità di massa atomica) della massa atomica di un [[Atom]]. Lo strumento in sé è detto **spettrometro di massa**.
### Funzionamento
Uno spettrometro di massa è tradizionalmente composto da tre componenti: una *sorgente di ioni* e due *selettori*.

![[Schema Spettroscopo di massa|80%|center]]

La *sorgente di ioni* è una qualunque sorgente che emana un fascio di [[ione|ioni]] di un elemento a diverse velocità. Una sorgente molto semplice è, ad esempio, un blocco di materiale puro dell'elemento che mi interessa che viene bombardato da un fascio di [[Elettrone|elettroni]], generando così un fascio di ioni.

Il primo selettore è un *selettore di velocità* composto da campi elettrici e magnetici perpendicolari. Il campo elettrico $\vec{E}$ genera un forza di modulo $qE$ che spinge gli ioni verso la parte superiore del selettore; il campo magnetico $\vec{B}$ genera una forza di modulo $qvB$ verso la parte inferiore. Se l'ione continua dritto, vuol dire che queste due forze si equilibrano (altrimenti colliderebbe con l'interno del selettore). Allora si ha
$$qE=qvB \quad\Rightarrow\quad v=\frac{E}{B}$$

Il secondo selettore è un *selettore di impulso* composto da un singolo campo magnetico uniforme che piega il fascio di un raggio $r$, dipendente dall'impulso $p$, tale che
$$p=mv=qBr \quad\Rightarrow\quad m = \frac{qrB^{2}}{E}$$
grazie al fatto che $v=E/B$ per il selettore di velocità.

Gli ioni, dopo la curvatura, collidono con un sensore (originariamente un piatto fotografico) da cui si possono misurare i raggi $r$ di curvatura. Ma dato che $q$, $B$ ed $E$ sono noti, ad ogni $r$ è associata una massa facilmente calcolabile.
### Misure
La precisione delle misure deriva dall'utilizza di un punto fisso nella scala delle masse atomiche, in genere la massa del carbonio 12:
$$m(^{12}C)=12.000\,000u$$
Si usa quindi un metodo detto **doppietto di massa**. Con questo metodo, non si va a misurare la massa dell'atomo direttamente, si prendono due molecole che differiscono solo per un atomo (o un multiplo) più atomi di massa nota e si trova la differenza tra le masse molecolari. Per esempio, per trovare la massa dell'idrogeno, si usano le molecole di $C_{9}H_{20}$ (*nonano*) e $C_{10}H_{8}$ (*naftalene*). La differenza tra le masse è[^1]
$$\Delta=m(C_{9}H_{20})-m(C_{10}H_{8})=12m(^{1}H)-m(^{12}C)$$
La massa del carbonio è carbonio 12 è nota, quindi la massa dell'idrogeno deve essere
$$m(^{1}H)=\frac{1}{12}[m(^{12}C)+\Delta]=1.007\,982\,503\pm0.000\,000\,01\text{ u}$$

Così facendo, posso "collezionare" valori molto precisi di masse atomiche per gli elementi comuni. Dopodiché, è possibile sfruttarle per ottenere la massa di altri atomi a partire da reazioni chimiche usando la conservazione dell'energia. Per esempio, da
$$^{1}H+\,^{14}N \rightarrow\, ^{12}N+\, ^{3}H$$
se conosciamo le masse di $^{1}H$, $^{14}N$ e $^{3}H$, possiamo ricavare quella di $^{12}N$ semplicemente eguagliando le energie prima e dopo:
$$E_{^{1}H}+E_{^{14}N}=E_{^{12}N}+E_{^{3}H}$$
dove l'energia è la somma della [[massa a riposo]] e dell'energia cinetica $Mv^{2}/2$. Questo è particolarmente utile per isotopi instabili che non hanno [[vita media]] sufficientemente lunga da sopravvivere per la durata dell'utilizzo dello spettrometro (come appunto il $^{12}N$).
### Abbondanze isotopiche
Uno spettrometro di massa permette anche di misurare le abbondanze relative dei vari [[Isotopo|isotopi]] di un elemento, rimpiazzando il sensore con delle fenditure di uscita e facendo uno scan degli intervalli di massa variando campo elettrico e magnetico. Un uso comune è misurare le abbondanze del Sistema Solare.

![[Schema Abbondanze isotopiche Sistema Solare|center]]

[^1]: In realtà qui manca l'[[Binding energy]], ma tra atomi è talmente piccola da essere trascurabile anche entro il margine di errore $\mathcal{O}(10^{-9}u)$.