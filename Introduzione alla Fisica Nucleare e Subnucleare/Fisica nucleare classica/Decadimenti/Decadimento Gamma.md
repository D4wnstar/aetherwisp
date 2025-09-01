---
wiki-publish: true
---
Il **decadimento $\gamma$** è un tipo di [[Decadimento nucleare|decadimento]] nel quale un [[nucleone]] in uno [[stato]] eccitato decade in uno [[stato]] diseccitato o in quello fondamentale emettendo un [[Photon]] $\gamma$ con energia pari alla differenza di energia tra livelli, meno una piccola componente cinetica dovuta al rinculo del nucleo. Spesso segue il [[decadimento alpha]] o [[Decadimento Beta|beta]] dato che questi di solito lasciano il [[Atomic nucleus|nucleo]] in uno stato eccitato.
## Bilanciamento energetico
Prendiamo un nucleo di massa $M$ a riposo che decade $\gamma$ da uno stato eccitato con $E_{i}$ ad uno stato con $E_{f}$. Allora
1. il momento lineare si conserva.
2. il momento di rinculo del nucleo finale $\vec{p}_{R}$ ha energia cinetica assunta non relativistica $T_{R}=p^{2}_{R}/2M$.
Si conservano energia e momento
$$\begin{cases}
E_{i}=E_{f}+E_{\gamma}+T_{R} \\
0=\vec{p}_{R}+\vec{p}_{\gamma}
\end{cases} \quad\rightarrow\quad \vec{p}_{R}=-\vec{p}_{\gamma}$$
quindi l'impulso di rinculo è uguale e opposto a quello del fotone.

Uso l'energia relativistica $E_{\gamma}=cp_{\gamma}$ e chiamo $\Delta E=E_{i}-E_{f}$. Si ha
$$\Delta E =E_{\gamma}+ \frac{E_{\gamma}^{2}}{2Mc^{2}}\quad\text{ e }\quad E_{\gamma}=\sqrt{m^{2}_\gamma c^{4}+c^{2}p_{\gamma}^{2}}$$
Il fotone ha massa nulla $m_{\gamma}=0$, quindi ho soluzioni
$$E_{\gamma}=Mc^{2}\left[-1\pm \sqrt{1 + \frac{2\Delta E}{Mc^{2}} }\right]$$
L'energia è nell'ordine dei [[Electronvolt|MeV]] e $Mc^{2}$ è nell'ordine di $A\times10^{3}$ MeV, quindi $\Delta E$ è molto minore di $Mc^{2}$. Approssimo considerando solo i primi tre termini dell'espansione della radice:
$$E_{\gamma}\sim\Delta E- \frac{(\Delta E)^{2}}{2Mc^{2}} \rightarrow E_{\gamma}\sim\Delta E$$
perché $\frac{(\Delta E)^{2}}{2Mc^{2}}\sim10^{-5}$, che è il contributo del rinculo. Per $\gamma$ a basse energie si ha energia di rinculo di circa 1 eV, ma per $\gamma$ ad alte energie (5-10 MeV) si ha arriva ai $\sim100$ eV. Energie così alte possono spostare gli atomi nella materia allo stato solido: questo viene detto **danno da radiazione**.
## Radiazione elettromagnetica
La radiazione $\gamma$ ha un contributo sia elettrico che magnetico.
- La radiazione elettrica è causata da una variazione del campo elettrico nel nucleo per la ridistribuzione di carica elettrica.
- La radiazione magnetica è causata da una variazione del momento magnetico del nucleo per la ridistribuzione degli [[spin]] e dei momenti angolari orbitali dei nucleoni.
Il decadimento in generale può essere descritto come sovrapposizione di contributi di diverse polarità, ciascuna caratterizzata da una tipica distribuzione angolare.

La conservazione del momento angolare e della parità determinano le transizioni possibili. La transizione $\gamma$ da un nucleo iniziale con momento angolare $J_{i}$ e parità $\pi_{i}$ ad uno con momento angolare $J_{f}$ e parità $\pi_{f}$. Parità definita in funzione del suo momento angolare come nel [[Nuclear shell model]]. Per conservazione angolare
$$\vec{J}_{i}=\vec{J}_{f}+\vec{L}_{\gamma}$$
con $\vec{L}_{\gamma}$ è il momento angolare del fotone.

Un multipolo di ordine $L$ trasferisce un momento angolare $L\hbar$ ($L=1$ per dipolo, $L=2$ per quadripolo, ma non c'è $L=0$, ossia il monopolo, che non emette radiazione nemmeno classicamente). Considero i valori permessi di $L$
$$|J_{i}-J_{f}|\leq L \leq J_{i}+J_{f}$$
Sapendo questo posso capire che tipo di mistura è la radiazione. Per esempio, se $J_{i}=3/2$ e $J_{f}=5/2$, allora $L=1,2,3,4$, ossia la radiazione è una combinazione di dipolo, quadrupolo, ottupolo e esadecapolo.

Dalle parità di $i$ ed $f$ determino il tipo (elettrico o magnetico) di transizione. La transizione magnetica
$$\pi(ML)=(-1)^{L+1}$$
ha parità opposta a $L$, ossia è dispari se $L$ è pari. Per esempio, nel dipolo magnetico $L=1$, si ha parità pari perché $\vec{\mu}=q\vec{r}\times\vec{v}$ (il vettore assiale del momento) rimane invariato sotto inversione di coordinate.

La transizione elettrica
$$\pi(EL)=(-1)^{L}$$
ha parità uguale ad $L$, ossia è pari se $L$ è pari. Per esempio, nel dipolo elettrico $L=1$, si ha parità dispari perché $\vec{d}=q\vec{r}$ (il vettore polare) si trasforma in $-q\vec{r}$ sotto inversione di coordinate.

Nell'esempio di $J_{i}=3/2$ e $J_{f}=5/2$, se assumo $\pi_{i}=\pi_{f}$ non ho variazione di parità perché $\Delta\pi=0$. In questo caso, le transizione sono $M_{1}$, $E_{2}$, $M_{3}$ e $E_{4}$. Se invece ci fosse $\pi_{i}=-\pi_{f}$ avrei variazione di parità perché $\Delta \pi\neq0$ e le transizioni sarebbero $E_{1},M_{2},E_{3},M_{4}$.
### Regole di selezione
Vista la teoria precedente, possiamo enunciare delle **regole di selezione** per la radiazione $\gamma$.

Per l'ordine $L$ vale il momento angolare possibile
$$|J_{i}-J_{f}|\leq L \leq J_{i}+J_{f}\quad\text{escluso }L=0$$
 mentre per la parità valgono
$$\Delta\pi\neq0\quad \rightarrow \quad\text{transizioni pari magnetiche, dispari elettriche}$$
$$\Delta\pi=0\quad \rightarrow \quad\text{transizioni dispari magnetiche, pari elettriche}$$
 Nel caso limite $J_{i}=J_{f}$ si dovrebbe avere $L=0$, ma ciò non è possibile. In questi casi, si ha $L=1$.

Le regole di selezione sono le seguenti:
1. la radiazione di polo più basso domina.
2. l'emissione di multipolo elettrica è più probabile di quella dello stesso multipolo magnetico di 100 volte.
3. l'emissione di multipolo $L+1$ è meno probabile di quella precedente $L$ di $10^{-5}$ volte.
4. combinando 2. e 3., se $L'=L+1$ ho le seguenti probabilità di emissione $\lambda$:
$$\frac{\lambda(EL')}{\lambda(ML)}=\frac{\lambda(EL')}{\lambda(EL)} \frac{\lambda(EL)}{\lambda(ML)}\simeq10^{-5}\times10^{2}\simeq10^{-3}$$
$$\frac{\lambda(ML')}{\lambda(EL)}=\frac{\lambda(ML')}{\lambda(ML)} \frac{\lambda(ML)}{\lambda(EL)}\simeq10^{-5}\times10^{-2}\simeq10^{-7}$$
