---
aliases:
  - processo beta
  - processo beta inverso
  - cattura elettronica
---
Il **decadimento $\beta$** è un tipo di [[decadimento]] nel quale un [[Nucleo atomico|nucleo]] corregge l'eccesso di [[protone|protoni]] o [[neutrone|neutroni]] convertendoli l'uno nell'altro. Esistono infatti due tipi di decadimento $\beta$, in base alla direzione della conversione:
$$\text{decadimento }\beta^{-}\text{: }\quad n \rightarrow p+e^{-}+\nu_{e}^{-}$$
$$\text{decadimento }\beta^{+}\text{: }\quad p \rightarrow n+e^{+}+\nu_{e}$$
dove $e^{-}$ è un [[elettrone]] e $e^{+}$ è un [[positrone]]. Vengono emessi anche (anti)[[neutrino|neutrini]] elettronici $\nu_{e}$. Esiste anche una terza reazione, chiamata **cattura elettronica** (o c.e.)
$$\text{cattura elettronica:}\quad p+e^{-}\rightarrow n+\nu_{e}$$
che "promuove" un protone ad un neutrone catturando un elettrone vicino al nucleo. Dato che lo scopo del decadimento $\beta$ è convertire protoni e neutroni, tutti i nuclei risultanti sono [[Isobaro|isobari]].


È importante ricordare che il protone decade $\beta$ *solo nel nucleo*, non nel vuoto, dato che il $\beta^{+}$ termina in una massa superiore (da 938 MeV a ~939.5 MeV) ed c'è quindi bisogno di interazione esterna.

Il decadimento $\beta$ è mediato dall'[[interazione debole]].

Queste reazioni nucleari sono dette *interazioni di contatto a 4 [[fermione|fermioni]]*.

Una reazione tipo $\beta^{-}$ è
$$_{53}^{131}I_{78} \rightarrow _{54}^{131}Xe_{77}$$
con [[Legge di decadimento radioattivo|tempo di dimezzamento]] di 8.0 giorni. Per $\beta^{+}$ invece si ha
$$^{25}_{13}Al_{12} \rightarrow\, ^{25}_{12}Mg_{13}$$
con tempo di dimezzamento di 7.2 giorni. Per la cattura elettronica
$$^{54}_{25}Mn_{29} \rightarrow\, ^{54}_{24}Cr_{30}$$
con tempo di dimezzamento 312 giorni.
## Meccanismo
### Decadimento $\beta^{\pm}$
Partiamo dalla [[Formula semiempirica di massa]] che nel nostro caso diventa
$$M(A,Z)=\alpha A-\beta Z+\gamma Z^{2}+\delta$$
con
$$\begin{align}
\alpha &= m_{n}-a_{V}+a_{s}A^{-1/3}+ \frac{a_{a}}{4} \\
\beta &= a_{a}+(m_{n}-m_{p}-m_{e}) \\
\gamma &= \frac{a_{a}}{A}+ \frac{a_{c}}{A^{1/3}}
\end{align}$$
Fisso $A$. Per $A$ dispari ho una parabola. Per $A$ pari abbiamo due parabole distinte, per i due casi $A,Z$ pari-pari e $A,Z$ dispari-dispari. La parabola dispari-dispari giace sopra quella pari-pari di $2\delta$. Il minimo della parabola è $Z=\beta/2\gamma$. Un nucleo con massa minore è stabile.

Per esempio, guardiamo il decadimento $\beta$ per nuclei con $A$ dispari. Ad esempio $A=101$
![[Grafico Decadimento Beta dispari|80%|center]]
Il decadimento $\beta^{-}$ è possibile se $M(A,Z+1)<M(A,Z)$. Il decadimento $\beta^{+}$ è possibile se $M(A,Z)>M(A,Z-1)+Zm_{e}$.

Ora guardiamo il decadimento per $A$ pari. Ad esempio $A=106$
![[Grafico Decadimento Beta pari|80%|center]]
Se $A>70$, c'è più di un nucleo stabile nella catena di decadimento $\beta$. Sia $_{48}^{106}Cd$ che $_{46}^{106}Pd$ sono sono nella parte bassa della parabola e stabili, ma il palladio lo è di più. Dunque, il cadmio può *molto raramente* decadere in palladio con la reazione
$$_{48}^{106}Cd \rightarrow _{46}^{106}Pp + 2e^{+}+ \nu_{e}$$
che un doppio decadimento $\beta^{+}$.
### Cattura elettronica
La cattura elettronica è più probabile per nuclei grandi, perché il nucleo è più vicino alla nuvola elettronica. Compete energeticamente con il decadimento $\beta^{+}$. È possibile se $M(A,Z)>M(A,Z-1)+E$ con $E$ l'energia di eccitazione dell'elettrone catturato.
### Vite medie
Consideriamo il decadimento $\beta^{-}$ del neutrone libero nel vuoto
$$n \rightarrow p+e^{-}+\bar{\nu}_{e}$$
Esso rilascia 0.78 MeV di energia e ha una vita media di $\tau=889.1\pm2.1$ s. Come esempio, guardiamo il $^{40}K$ che decade per $\beta^+$, $\beta^{-}$ e cattura elettronica.
![[Grafico Decadimento Potassio|80%|center]]
## Rilascio energetico
Considero il decadimento $\beta^{-}$ del neutrone libero
$$n \rightarrow p+e^{-}+\bar{\nu}_{e}$$
che ha un tempo di dimezzamento $t_{1/2}\sim10$ minuti. L'energia è
$$Q=(m_{n}-m_{p}-m_{e}-m_{\bar{\nu}_{e}})c^{2}$$
La massa del neutrino è quasi nulla
$$m_{\bar{\nu}}< 2\frac{\text{ eV}}{c^{2}}\sim0$$
Se $n$ è a riposo, l'energia totale è
$$Q=T_{p}+T_{e}+T_{\bar{\nu}}$$
$T_p\sim0.3$ keV è trascurabile. L'energia cinetica totale viene spartita tra $e^{-}$ e $\bar{\nu}_{e}$. Usando cinematica relativistica ho
$$Q=m_{n}c^{2}-m_{p}c^{2}-m_{e}c^{2}=0.8\text{ MeV}$$
Considero $E_{\nu}$ relativistica dato che l'energia è nei MeV. Allora ho $E_{e}=T_{e}+m_{e}^{2}c$.
### $\beta^{-}$ nel nucleo
Considero il decadimento generico
$$_{Z}^{A}X_{N} \rightarrow _{Z+1}^{A}X_{N-1}'+e^{-}+\bar{\nu}_{e}$$
L'energia totale rilasciata dal decadimento è
$$Q_{\beta^{-}}=[m_{n}(_{Z}^{A}X)-m_{n}(_{Z+1}^{A}X')-m_{e}]c^{2}$$
con $m_{n}$ la massa del neutrone. Converto per masse atomiche
$$m(^{A}X)c^{2}=m_{N}(^{A}X)c^{2}+Zm_{e}- \sum\limits_{i=1}^{Z}B_{i}$$
dove l'energia di legame $B$ viene dall'elettrone. Allora ho
$$Q_{\beta^{-}}=\{[m(^{A}X)-Zm_{e}]-[m(^{A}X')-(Z+1)m_{e}]-m_{e}\}c^{2}+ \sum\limits_{i=1}^{Z}B_{i}-\sum\limits_{i=1}^{Z+1}B_{i}$$
dove le sommatorie sono trascurabili. Dunque si ha
$$Q_{\beta^{-}}=\{[m(^{A}X)-Zm_{e}]-[m(^{A}X')-(Z+1)m_{e}]-m_{e}\}c^{2}$$
### $\beta^{+}$ nel nucleo
Considero il decadimento generico
$$_{Z}^{A}X_{N} \rightarrow _{Z+1}^{A}X_{N-1}'+e^{+}+\nu_{e}$$
Per lo stesso procedimento di sopra si trova
$$Q_{\beta^{+}}=[m(^{A}X)-m(^{A}X')-2m_{e}]c^{2}$$
### Cattura elettronica nel nucleo
Considero il decadimento generico
$$_{Z}^{A}X_{N} + e^{-} \rightarrow _{Z-1}^{A}X_{N+1}'+\nu_{e}$$
L'energia emessa $E_{\gamma}$ per tornare allo stato fondamentale dopo la c.e. che l'aveva lasciato in uno stato eccitato è l'energia di legame dell'elettrone catturato $B_{e^{-}}$. L'energia della cattura è
$$Q_{c.e.}=[m(^{A}X)-m(^{A}X')]c^{2}-B_{e^{-}}$$
La soglia per far accadere $\beta^{+}$ è più alta di quella per la c.e..