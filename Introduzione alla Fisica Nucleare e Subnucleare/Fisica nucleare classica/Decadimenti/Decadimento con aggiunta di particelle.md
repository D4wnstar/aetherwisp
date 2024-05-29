La [[legge di decadimento radioattivo]] descrive con buona precisione il decadimento di un oggetto esteso composto da [[Nuclide|radionuclidi]]. Perde di validità, tuttavia, una volta che vengono aggiunti [[Nucleo atomico|nuclei]] esternamente al campione. In questo caso, va considerata anche l'aggiunta di [[Particella|particelle]] esterne.

Si definisce **tasso di produzione** $R$ la quantità di conversioni da nucleo stabile ad instabile che accadono quando un bersaglio stabile viene bombardato da un fascio di particelle. Tipicamente è molto basso, quindi il numero di [[atomo|atomi]] stabili che compongono il bersaglio non varia sensibilmente. 

Considerato un flusso di particelle incidenti $I$ (particelle/s$\times$cm$^{2}$), la [[sezione d'urto]] $\sigma$ di questa reazione e il numero di atomo presenti nel bersaglio $N_{0}$ (considerato costante), il tasso di produzione può essere espresso come
$$R=N_{0}\sigma I$$

Consideriamo ora gli $N_{1}$ atomi nuclei radioattivi formati, che decadono con [[Legge di decadimento radioattivo|costante di decadimento]] $\lambda_{1}$ in $N_{2}$ nuclei stabili. Gli $N_{1}$, oltre a diminuire per il loro decadimento, aumentano a causa delle interazioni con il fascio di particelle incidente. La loro variazione è
$$dN_{1}=Rdt-\lambda_{1}N_{1}dt$$
che è un'[[equazione differenziale ordinaria]], risolta da
$$N_{1}(t)=\frac{R}{\lambda_{1}}(1-e^{-\lambda_{1}t})$$
che l'[[attività]] associata è
$$A_{1}(t)=\lambda_{1}N_{1}(t)=R(1-e^{-\lambda_{1}t})$$
Se il tempo di osservazione $t$ è molto minore della [[Legge di decadimento radioattivo|vita media]] $t_{1/2}$ si approssima a
$$A_{1}(t)\simeq R\lambda_{1}t \quad\text{con }t\ll t_{1/2}$$
cioè cresce linearmente con il tempo. Per tempi di osservazione superiori si ha invece
$$A_{1}(t)\simeq R \quad \text{con }t\gg t_{1/2}$$
In questo caso, l'attività generata dai nuclei è pari al tasso di produzione del fascio, quindi si bilanciano a vicenda e il numero di nuclei radioattivi rimane costante. Questo è un esempio di [[equilibrio secolare]].