Il **modello a shell** è un modello del nucleo di un [[atomo]]. Da non confondere con il modello a shell dell'atomo stesso, che tratta degli elettroni. Ha i seguenti presupposti:
1. i nucleoni si muovono nel nucleo sottoposti ad un potenziale
2. il potenziale ha origine dagli altri nucleoni

Dall'interpolazione dell'[[Atomo#Energia di legame|energia di legame]] media si trova che alcuni nuclei sono incredibilmente stabili e si trovano di molto al di sopra della curva. Questi nuclei si trovano in corrispondenza di alcuni $N$ e $Z$ specifici detti **numeri magici**: essi sono 2, 8, 20, 28, 50, 82 e 126. Esempi di nuclei (doppiamente) magici sono $_{2}^{4}He_{2}$, $_{8}^{16}O_{8}$, $_{20}^{40}Ca_{20}$, $_{20}^{48}Ca_{28}$ e $_{82}^{208}Pb_{128}$.
### Formulazione con potenziale gaussiano
Per nuclei piccoli ($A\leq7$), la distribuzione dei nucleoni nel nucleo è circa Gaussiana, quindi possiamo approssimare il potenziale con distribuzione spaziale Gaussiana. In altre parole, abbiamo un [[oscillatore armonico]] tridimensionale, che ha potenziale
$$V(r)=\frac{1}{2k}r^{2}$$
La parte angolare della soluzione dipende dalle coordinate $\theta$ e $\phi$ e le ricavo direttamente con le armoniche sferiche
$$Y_{l,m_{l}}(\theta,\phi)$$
con $m_{l}=0,\pm1,\pm2,\ldots$ [[numero quantico]] magnetico e $l=0,1,2,\ldots=s,p,d,f,\ldots$ numero quantico di momento angolare orbitale. Dalla soluzione ricavo i livelli energetici
$$E_{N}=\hbar \omega_{0}\left(N + \frac{3}{2}\right)$$
con $N=0,1,2,\ldots$ i livelli energetici, ossia il numero quantico principale. Vale $l\leq N$. Introducendo $n$ il numero di nodi, possiamo scrivere i livelli come
$$N=2(n-1)+l$$
Ogni livello energetico ha diversi set di numeri quantici che portano allo stesso livello: il numero di set si dice *degenerazione* e ci sono $2l+1$ set. In presenza di [[spin]], diventa $2(2l+1)$.
![[Grafico Modello a shell nucleare|80%|center]]
	Questo modello riproduce i numeri magici con accuratezza fino al 20.