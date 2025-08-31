---
wiki-publish: true
aliases:
  - processo beta
  - processo beta inverso
  - cattura elettronica
---
Il **decadimento $\beta$** è un tipo di [[Decadimento nucleare|decadimento]] nel quale un [[Atomic nucleus|nucleo]] corregge l'eccesso di [[protone|protoni]] o [[neutrone|neutroni]] convertendoli l'uno nell'altro. Esistono infatti due tipi di decadimento $\beta$, in base alla direzione della conversione:
$$\text{decadimento }\beta^{-}\text{: }\quad n \rightarrow p+e^{-}+\bar{\nu}_{e}$$
$$\text{decadimento }\beta^{+}\text{: }\quad p \rightarrow n+e^{+}+\nu_{e}$$
dove $e^{-}$ è un [[Elettrone]] e $e^{+}$ è un [[positrone]]. Vengono emessi anche (anti)[[neutrino|neutrini]] elettronici $\nu_{e}$. Esiste anche una terza reazione, chiamata **cattura elettronica** (o c.e.)
$$\text{cattura elettronica:}\quad p+e^{-}\rightarrow n+\nu_{e}$$
che "promuove" un protone ad un neutrone catturando un elettrone vicino al nucleo. Dato che lo scopo del decadimento $\beta$ è convertire protoni e neutroni, tutti i nuclei risultanti sono [[Isobar|isobari]].

È importante ricordare che il protone decade $\beta$ *solo nel nucleo*, non nel vuoto, dato che il $\beta^{+}$ termina in una massa superiore (da 938 MeV a ~939.5 MeV) ed c'è quindi bisogno di interazione esterna.

Il decadimento $\beta$ è mediato dall'[[Weak interaction]].

Queste reazioni nucleari sono dette *interazioni di contatto a 4 [[Fermion|fermioni]]*.

Una reazione tipo $\beta^{-}$ è
$$_{53}^{131}I_{78} \rightarrow _{54}^{131}Xe_{77}$$
con [[Legge di decadimento radioattivo|tempo di dimezzamento]] di 8.0 giorni. Per $\beta^{+}$ invece si ha
$$^{25}_{13}Al_{12} \rightarrow\, ^{25}_{12}Mg_{13}$$
con tempo di dimezzamento di 7.2 giorni. Per la cattura elettronica
$$^{54}_{25}Mn_{29} \rightarrow\, ^{54}_{24}Cr_{30}$$
con tempo di dimezzamento 312 giorni.
## Meccanismo
### Decadimento $\beta^{\pm}$
Consideriamo la [[Semi-empirical mass formula]]
$$M(Z,A)=Nm_{n}+Zm_{p}+Zm_{e}- a_{v}A+a_{s}A^{\frac{2}{3}}+a_{c} \frac{Z(Z-1)}{A^{\frac{1}{3}}}+a_{a} \frac{(N-Z)^{2}}{4A}+\delta$$
che può essere scritta come
$$M(A,Z)=\alpha A-\beta Z+\gamma Z^{2}+\delta$$
definendo
$$\begin{align}
\alpha &= m_{n}-a_{v}+a_{s}A^{-1/3}+ \frac{a_{a}}{4} \\
\beta &= a_{a}+(m_{n}-m_{p}-m_{e}) \\
\gamma &= \frac{a_{a}}{A}+ \frac{a_{c}}{A^{1/3}}
\end{align}$$
La forma della funzione dipende dalla parità di $A$.
- Per $A$ dispari ho una parabola singola.
- Per $A$ pari ho due parabole distinte, per i due casi possibili $A,Z$ pari-pari e $A,Z$ dispari-dispari. La parabola dispari-dispari giace sopra quella pari-pari di un fattore $2\delta$. Il minimo della parabola è $Z=\beta/2\gamma$. Nella parabola di uno spettro isobarico, il nucleo con massa minore è stabile per decadimento $\beta$.
#### $A$ dispari
Guardiamo il decadimento $\beta$ per nuclei con $A$ dispari. Ad esempio, per $A=101$:

![[Grafico Decadimento Beta dispari|80%|center]]

Qui il nucleo con massa minore è il rutenio-44, quindi i suoi isobari con più o meno protoni decadranno naturalmente ad esso.
- Il decadimento $\beta^{-}$ (neutroni a protoni) è possibile per gli isobari con troppi pochi protoni, per i quali la massa diminuisce dopo il $\beta^{-}$: $M(A,Z+1)<M(A,Z)$.
- Il decadimento $\beta^{+}$ (protoni a neutroni) è possibile nel caso opposto, ossia se ci sono troppi protoni. In questi casi, è il $\beta^{+}$ a far diminuire la massa: $M(A,Z)>M(A,Z-1)+2m_{e}$, che tiene conto di un eccesso di un $e^{-}$ nell'atomo genitore e della creazione di un $e^{+}$ dal decadimento.
Qui si parla della massa dell'intero atomo, non sono del nucleo, a modo di considerare anche l'elettrone prodotto dal decadimento.
#### $A$ pari
Ora guardiamo il decadimento per $A$ pari. Ad esempio $A=106$:
![[Grafico Decadimento Beta pari|80%|center]]
Se $A>70$, c'è più di un nucleo stabile nella catena di decadimento $\beta$. Sia $_{48}^{106}Cd$ che $_{46}^{106}Pd$ sono stabili dato che entrambi i loro vicini sono ad energia maggiore, ma il palladio lo è di più. Dunque, il cadmio può *molto raramente* decadere in palladio con la reazione
$$_{48}^{106}Cd \rightarrow _{46}^{106}Pd + 2e^{+}+ \nu_{e}$$
cioè un doppio decadimento $\beta^{+}$.
### Cattura elettronica
A causa dell'[[indeterminatezza quantistica]], la posizione di un elettrone non è definita se non al tempo della misura. C'è sempre quindi una possibilità che un elettrone "si trovi" all'interno del nucleo. In quell'intervallo di tempo, è possibile che l'elettrone interagisca con un protone per creare un neutrone con emissione di neutrino.

La cattura elettronica è più probabile per nuclei grandi, perché il nucleo, oltre ad essere più voluminoso, è anche più vicino alle shell interne della nuvola elettronica. Infatti, si trova empiricamente che gli elettroni ad essere catturati sono quasi sempre quelli delle shell basse, come 1s o 2p. Il "buco" lasciato nella shell bassa sarà riempito da un elettrone di una shell superiore che decade, che a sua volta sarà riempito da uno ad energia più alta, creando una catena di decadimenti elettroni.

È simile al decadimento $\beta^{+}$ ed infatti ci compete energeticamente. È possibile se $M(A,Z)>M(A,Z-1)+E$ con $E$ l'energia di eccitazione associata alla shell elettronica dell'elettrone catturato. L'energia cinetica della c.e. è maggiore di quella del $\beta^{+}$ di $2m_{e}c^{2}-E$ nello stato finale. Questo implica che la c.e. può avvenire anche se la massa dell'atomo genitore è simile a quella della figlia $M(A,Z)\simeq M(A,Z-1)$, mentre $\beta^{+}$ no.
### Vite medie
La vita media di nuclei soggetti a decadimento $\beta$ varia tra i pochi millisecondi a $10^{16}$ anni, a dipendenza dell'energia disponibile e dalle proprietà dei nuclei.

Per un esempio di emettitore $\beta$ a vita media breve, consideriamo il decadimento $\beta^{-}$ del neutrone libero nel vuoto
$$n \rightarrow p+e^{-}+\bar{\nu}_{e}$$
Esso rilascia 0.78 MeV di energia e ha una vita media di $\tau=889.1\pm2.1$ s o poco meno di un quarto d'ora.

Come esempio di emettitore a lunga vita media, guardiamo il $^{40}K$ che decade per $\beta^+$, $\beta^{-}$ e cattura elettronica, con [[Rapporto di ramificazione|rapporti di ramificazione]] molto a favore del $\beta^{-}$.

![[Grafico Decadimento Potassio|80%|center]]

La freccia piegata nel $\beta^{+}$ indica che la produzione di $e^{+}$ e la presenza di un $e^{-}$ in più nell'atomo di $^{40}Ar$ richiedono 1.022 MeV, mentre il resto dell'energia disponibile si trova sotto forma di energia cinetica del positrone e neutrino. Le reazioni sono
$$\beta^{-}:\, ^{40}_{19}K \rightarrow\ ^{40}_{20}Ca+e^{-}+\bar{\nu}_{e}$$
$$\beta^{+}:\ ^{40}_{20}K \rightarrow\ ^{40}_{18}Ar+e^{+}+\nu_{e}$$
$$\text{c.e.}:\ ^{40}_{20}K+e^{-} \rightarrow\ ^{40}_{18}Ar + \nu_{e}$$
Il $^{40}\text{Ar}$ a sua volta [[Decadimento Gamma|decade]] $\gamma$ dallo stato eccitato $2^{+}$ a quello fondamentale $0^{+}$ con rilascio di un [[Photon]].
## Rilascio energetico
### $\beta^{-}$ nel vuoto
Considero il decadimento $\beta^{-}$ del neutrone libero
$$n \rightarrow p+e^{-}+\bar{\nu}_{e}$$
che ha un tempo di dimezzamento $t_{1/2}\sim10$ minuti. Il [[Q-valore]] del decadimento è
$$Q=(m_{n}-m_{p}-m_{e}-m_{\bar{\nu}_{e}})c^{2}$$
La massa del neutrino è quasi nulla quindi la trascuriamo
$$m_{\bar{\nu}}< 2\frac{\text{ eV}}{c^{2}}\sim0 \quad \rightarrow \quad Q=0.8\text{ MeV}$$
Se $n$ è a riposo, l'energia totale è
$$Q=T_{p}+T_{e}+T_{\bar{\nu}}$$
L'energia cinetica di rinculo del protone $T_p$ è $\sim0.3$ keV, quindi è trascurabile. L'energia cinetica totale viene spartita tra $e^{-}$ e $\bar{\nu}_{e}$. Usando cinematica relativistica ho
$$Q=m_{n}c^{2}-m_{p}c^{2}-m_{e}c^{2}=0.8\text{ MeV}$$
Considero l'energia del neutrino pari alla sua energia cinetica $E_{\nu}=T_{\nu}$, dato che ha massa circa nulla. L'energia dell'elettrone invece è relativistica dato che l'energia cinetica è nei MeV, quindi paragonabile alla massa dell'elettrone. Allora ho $E_{e}=T_{e}+m_{e}^{2}c$. Il rinculo $T_{p}$ ha energia molto bassa e quindi non relativistica.
### $\beta^{-}$ nel nucleo
Considero il decadimento generico
$$_{Z}^{A}X_{N} \rightarrow _{Z+1}^{A}X_{N-1}'+e^{-}+\bar{\nu}_{e}$$
L'energia totale rilasciata dal decadimento è
$$Q_{\beta^{-}}=[m_{n}(_{Z}^{A}X)-m_{n}(_{Z+1}^{A}X')-m_{e}]c^{2}$$
con $m_{n}$ la massa del neutrone. Converto per masse atomiche
$$m(^{A}X)c^{2}=m_{n}(^{A}X)c^{2}+Zm_{e}- \sum\limits_{i=1}^{Z}B_{i}$$
dove l'[[Binding energy]] $B_{i}$ viene dal legame dell'$i$-esimo elettrone. Allora ho
$$Q_{\beta^{-}}=\{[m(^{A}X)-Zm_{e}]-[m(^{A}X')-(Z+1)m_{e}]-m_{e}\}c^{2}+ \sum\limits_{i=1}^{Z}B_{i}-\sum\limits_{i=1}^{Z+1}B_{i}$$
dove le differenze di energie di legame (le sommatorie) sono trascurabili. Dunque si ha
$$Q_{\beta^{-}}=[m(^{A}X)-m(^{A}X')]c^{2}$$
Le masse elettroniche si cancellano.
### $\beta^{+}$ nel nucleo
Considero il decadimento generico
$$_{Z}^{A}X_{N} \rightarrow _{Z-1}^{A}X_{N+1}'+e^{+}+\nu_{e}$$
Per lo stesso procedimento di sopra si trova
$$Q_{\beta^{+}}=[m(^{A}X)-m(^{A}X')-2m_{e}]c^{2}$$
Qui le masse elettroniche non si cancellano. Dato che si espellono due elettroni, il Q-valore può essere negativo, il che rende il $\beta^{+}$ possibile solo nei casi in cui non lo è. In particolare, $Q_{\beta^{+}}$ è positivo solo se la differenza di massi tra gli atomi è $>2m_{e}c^{2}=1.022$ MeV.
### Cattura elettronica nel nucleo
Considero il decadimento generico
$$_{Z}^{A}X_{N} + e^{-} \rightarrow _{Z-1}^{A}X_{N+1}'+\nu_{e}$$
L'energia emessa $E_{\gamma}$ per tornare allo stato fondamentale dopo la c.e. che l'aveva lasciato in uno stato eccitato è l'energia di legame dell'elettrone catturato $B_{e^{-}}$. L'energia è abbastanza alta da trovarsi nella banda dei raggi X. L'energia della cattura è
$$Q_{c.e.}=[m(^{A}X)-m(^{A}X')]c^{2}-B_{e^{-}}$$

Sia il $\beta^{+}$ che la c.e. terminano con la produzione di una specie con $Z-1$ e $N+1$, ma la soglia per far accadere $\beta^{+}$ è più alta di quella per la c.e., quindi è possibile che la c.e. sia l'unica delle due possibile.