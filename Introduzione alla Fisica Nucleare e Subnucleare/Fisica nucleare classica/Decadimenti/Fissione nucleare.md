La **fissione nucleare** è un tipo di [[Decadimento]] nel quale un [[Nucleo atomico|nucleo]] pesante (con $A$ grande) si scinde in due nuclei più piccoli.

Per esempio, prendiamo il $^{238}\text{U}$ che ha un'[[energia di legame]] pari a circa $\sim7.6$ MeV/[[Nucleone]]. Se si scinde a metà, l'uranio si divide in due atomi con $A=119$, che dai dati sperimentale ha energia di legame maggiore: $\sim8.5$ MeV/nucleone.

Considero $R_{0}$ il raggio dell'atomo madre e $R_{1}$ e $R_{2}$ il raggio dei due frammenti. Assumendo $R_{1}\sim R_{2}\sim R_{0}A^{1/3}\sim1.3\times(119)^{1/3}\sim6$ fm.

![[Grafico Fissione nucleare|80%|center]]
Il meccanismo è simile a quello del [[Decadimento Alpha]]. Nel caso di sopra, per superare la barriera Coulombiana, bisogna avere energie superiori al potenziale
$$V=\frac{1}{4\pi\epsilon_{0}} \frac{Z_{1}Z_{2}e^{2}}{R}\sim(1.44\text{ MeV fm})\times \frac{(46)^{2}}{12\text{ fm}}\sim250\text{ MeV}$$
L'energia associata ad un $^{238}\text{U}$ è $E_{i}=238\times7.6\text{ MeV}=1809$ MeV. Quella associata a due atomi di $^{119}\text{Pd}$ è $E_{f}=2\times119\times8.5\text{MeV}=2023$ MeV. Allora $\Delta E=E_{f}-E_{i}=214$ MeV. Per conservare l'energia (quindi $E_{i}=E_{f}$) mancano 214 MeV. Questi MeV mancanti si trovano in altri prodotti della fissione nucleari, come ad esempio [[neutrone|neutroni]], [[elettrone|elettroni]], [[Decadimento Gamma#Radiazione elettromagnetica|radiazione]] $\gamma$ e altro.

Durante la fissione, la geometria del nucleo cambia. Da una sfera, le forze Coulombiane deformano il nucleo in un'ellissoide, finché si spacca in due nuclei più piccoli. Nel deformarsi, aumenta la superficie del nucleo, ma diminuisce la repulsione Coulombiana.

![[Schema Deformazione nucleo in fissione|100%]]

$$a=R(1+\epsilon)\quad;\quad b=R(1+\epsilon)^{-1/2}$$
con $\epsilon$ l'eccentricità: $\epsilon\equiv\beta\sqrt{5/4\pi}$, detto **parametro di deformazione**. La differenza di energia è
$$\Delta E=B(\epsilon)-B(\epsilon=0)=$$
$$=-a_{s}A^{2/3}\left( 1+ \frac{2}{5}\epsilon^{2}+\ldots \right)+a_{s}A^{2/3}+a_{c}Z^{2}A^{-1/3}-a_{c}Z^{2}A^{-1/3}(1- \frac{1}{5}\epsilon^{2}+\ldots)\simeq$$
$$\simeq\left(- \frac{2}{5}a_{s}A^{2/3}+ \frac{1}{5}a_{c}Z^{2}A^{-1/3}\right)\epsilon^{2}$$
Allora la fissione è spontanea se $\Delta E>0$ che accade quando $Z^{2}/A>47$. In altri termini, la fissione nucleare accade solo per atomi pesanti.

Un esempio di fissione con $^{235}_{92}\text{U}_{143}$:
$$^{235}_{92}\text{U}_{143} + n \rightarrow _{37}^{93}\text{Rb}_{56}+_{55}^{141}\text{Cs}_{86}+2n$$
Quindi la fissione produce altri neutroni. Questi neutroni a loro volta possono indurre ulteriori fissioni nucleari nei nuclei vicini, iniziando così una reazione a catena che emette grandi quantità di energie con poca energia iniziale (quella necessaria per sparare i primi neutroni).
![[Grafico Fissione uranio 235|80%|center]]
Nel caso della fissione spontanea o indotta da neutroni *termici* (ossia ad energia basse nell'ordine dei keV), è improbabile che gli atomi frammento abbiano $A$ simili. La ragione è sconosciuta. Nel caso di fissione indotta da neutroni ad alte energie (nell'ordine dei MeV), è più probabile che $A_{1}\sim A_{2}$.

I neutroni emessi dalla fissione si dividono in due tipi:
- i neutroni *pronti* sono prodotti dalla fissione stessa e hanno $t\leq10^{-16}$ s
- i neutroni *ritardati* sono prodotti più tardi dai decadimenti successivi causati dalla fissione. Difatti, i prodotti iniziale decadono a loro volta emettendo radiazione $\beta$ e $\gamma$.
### Energia della fissione
Prendiamo di nuovo la fissione dell'uranio 235.
$$^{235}_{92}\text{U}_{143} + n \rightarrow ^{236}\text{U}^{*} \rightarrow\ldots$$
L'energia di eccitazione è
$$E_{ecc}=[m(^{236}\text{U}^{*})-m(^{235}\text{U})]c^{2}=6.5\text{ MeV}$$
con $m(^{236}\text{U}^{*})=m(^{235}\text{U})+m_{n}$. Da calcoli del [[Modello a shell nucleare]] (e anche misure sperimentali), ottengo $E_{attivazione}$ (l'energia necessaria a superare la barriera di potenziale) per $^{235}\text{U}$ pari a 6.2 MeV, quindi $^{235}\text{U}$ può fissionare anche con neutroni termici, dato che $E_{ecc}-E_{attivazione}$ è bassa. Nella fissione
$$^{235}_{92}\text{U}_{143} + n \rightarrow ^{236}\text{U}^{*} \rightarrow ^{93}\text{Rb}+^{141}\text{Cs}+2n$$
rilascio $Q-\text{valore}=181$ MeV di energia. I due neutroni emessi hanno energia media $\left\langle E_{n} \right\rangle\sim2$ MeV, quindi a loro volta possono innescare fissione anche con alte energie. L'energia degli altri prodotti sono $E_{\beta}\sim19$ MeV, $E_{\gamma,\text{dec.}}\sim7$ MeV e $E_{\gamma,\text{pronto}}\sim8$ MeV.

Lo stesso calcolo per $^{238}\text{U}$ ci dà $E_{ecc}=4.8$ MeV e $E_{att}=6.6$ MeV, quindi abbiamo bisogno di neutroni ad alte energie.

La dinamica della reazione è:
1. i neutroni "portano via" un impulso piccolo
2. $m_{1}v_{1}=m_{2}v_{2}$ per i frammenti
3. $$\frac{T_{1}}{T_{2}}=\frac{\frac{1}{2}m_{1}v_{1}^{2}}{\frac{1}{2}m_{2}v_{2}^{2}}\sim \frac{m_{2}}{m_{1}}$$
