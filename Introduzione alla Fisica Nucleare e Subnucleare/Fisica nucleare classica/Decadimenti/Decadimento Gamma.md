Il **decadimento $\gamma$** è un tipo di [[decadimento]] nel quale un [[nucleone]] in uno [[stato]] eccitato decade in uno stato diseccitato o in quello fondamentale emettendo radiazione $\gamma$ con energia pari alla differenza di energia tra livelli, meno una piccola componente cinetica dovuta al rinculo del nucleo. Spesso segue il [[Decadimento Alpha]] o [[Decadimento Beta|beta]] dato che questi di solito lasciano il [[Nucleo atomico|nucleo]] in uno stato eccitato.
## Bilanciamento energetico
Prendiamo un nucleo di massa $M$ a riposo che decade $\gamma$ da uno stato eccitato con $E_{i}$ ad uno stato con $E_{f}$. Allora
1. il momento lineare si conserva.
2. il momento di rinculo del nucleo finale $p_{R}$ ha energia cinetica $T_{R}=p^{2}_{R}/2M$.
Si conservano energia e momento
$$\begin{cases}
E_{i}=E_{f}+E_{\gamma}+T_{R} \\
0=\vec{p}_{R}+\vec{p}_{\gamma} \rightarrow \vec{p}_{R}=-\vec{p}_{\gamma}
\end{cases}$$
Uso energia relativistica $E_{\gamma}=cp_{\gamma}$ e chiamo $\Delta E=E_{i}-E_{f}$. Si ha
$$\Delta E =E_{\gamma}+ \frac{E_{\gamma}^{2}}{2Mc^{2}}\quad\text{ e }\quad E_{\gamma}=\sqrt{m^{2}_\gamma c^{4}+c^{2}p_{\gamma}^{2}}$$
Ho soluzioni
$$E_{\gamma}=Mc^{2}\left[-1\pm \left(1 + \frac{2\Delta E}{Mc^{2}} \right)^{\frac{1}{2}}\right]$$
L'energia è nell'ordine dei MeV e $Mc^{2}$ è nell'ordine di $A\times10^{3}$ MeV. Quindi $\Delta E$ è molto minore di $Mc^{2}$. Approssimo considerando solo i primi termini.
$$E_{\gamma}\sim\Delta E- \frac{(\Delta E)^{2}}{2Mc^{2}} \rightarrow E_{\gamma}\sim\Delta E$$
perché $\frac{(\Delta E)^{2}}{2Mc^{2}}\sim10^{-5}$, che è il contributo del rinculo. Per $\gamma$ a basse energie si ha $R\sim1$ eV, ma per $\gamma$ ad alte energie si ha $R\sim100$ eV, con energie associate tra i 5 e 10 MeV. Energie così alte possono spostare gli atomi nella materia: questo viene detto *danno da radiazione*.
## Radiazione elettromagnetica
La radiazione $\gamma$ ha un contributo sia elettrico che magnetico.
- La radiazione elettrica è causata da una variazione del campo $\vec{E}$ nel nucleo.
- La radiazione magnetica è causata da una variazione del momento magnetico del nucleo.
La conservazione angolare e di parità determinano le transizioni possibili. La transizione $\gamma$ da un nucleo iniziale con momento angolare $J_{i}$ e parità $\pi_{i}$ ad uno con momento angolare $J_{f}$ e parità $\pi_{f}$. Parità definita in funzione del suo momento angolare come nel [[Modello a shell nucleare]]. Per conservazione angolare
$$\vec{J}_{i}=\vec{J}_{f}+\vec{L}_{\gamma}$$
con $\vec{L}_{\gamma}$ è il momento angolare del $\gamma$.

Un multipolo di ordine $L$ trasferisce un momento angolare $L\hbar$ ($L=1$ per dipolo, $L=2$ per quadripolo, ma non c'è $L=0$, ossia il monopolo). Considero i valori permessi di $L$: $|J_{i}-J_{f}|\leq L \leq J_{i}+J_{f}$. Dalle parità di $i$ ed $f$ determino il tipo (elettrico o magnetico) di transizione. La transizione magnetica
$$\pi(ML)=(-1)^{L+1}$$
ha parità pari se $L$ è dispari. Nel dipolo magnetico, $L=1$ e ha parità pari perché $\vec{\mu}=q\vec{r}\times\vec{v}$, cioè il vettore assiale del momento.

La transizione elettrica
$$\pi(EL)=(-1)^{L}$$
ha parità pari se $L$ è pari. Per il dipolo elettrico, $L=1$, vale $\vec{d}=q\vec{r}$, che è il vettore polare.

Con $\pi_{i}=\pi_{f}$ non ho variazione di parità perché $\Delta\pi=0$. In questo caso, $L_{1}$ e $L_{3}$ sono transizioni magnetiche $M_{1}$ e $M_{3}$ e $L_{2}$ e $L_{4}$ sono transizioni elettriche $E_{2}$ e $E_{4}$.

Con $\pi_{i}\neq\pi_{f}$ ho variazione di parità perché $\Delta \pi\neq0$. Qui le transizioni sono $E_{1},M_{2},E_{3},M_{4}$.
### Regole di selezione
Per l'ordine $L$ vale
$$|J_{i}-J_{f}|\leq L \leq J_{i}+J_{f}$$
 e $L=0$ non è valido. Per la parità
$$\Delta\pi\neq0\quad \rightarrow \quad\text{transizioni pari magnetiche, dispari elettriche}$$
$$\Delta\pi=0\quad \rightarrow \quad\text{transizioni dispari magnetiche, pari elettriche}$$
 Nel caso limite $J_{i}=J_{f}$ si dovrebbe avere $L=0$, ma ciò non è possibile. In questi casi, si ha $L=1$.

Le regole sono le seguenti:
1. la radiazione di polo più basso domina
2. l'emissione di multipolo elettrica è più probabile di quella magnetica di 100 volte
3. l'emissione di multipolo $L+1$ è meno probabile di quella precedente $L$ di $10^{-5}$ volte
4. se $L'=L+1$ ho le seguenti probabilità di emissione $\lambda$
$$\frac{\lambda(EL')}{\lambda(ML)}=\frac{\lambda(EL')}{\lambda(EL)} \frac{\lambda(EL)}{\lambda(ML)}\simeq10^{-5}\times10^{2}\simeq10^{-3}$$
$$\frac{\lambda(ML')}{\lambda(EL)}=\frac{\lambda(ML')}{\lambda(ML)} \frac{\lambda(ML)}{\lambda(EL)}\simeq10^{-5}\times10^{-2}\simeq10^{-7}$$
