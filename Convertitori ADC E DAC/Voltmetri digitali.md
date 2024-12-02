>[!note]
>I voltometri digitali sono impiegati per misurare e acquisire dati. Le caratteristiche tipiche sono la dinamica, il numero di cifre decimali, il numero di bit e la velocità di lettura.

Esistono due tipi di voltometri digitali:
- Differenziali (differenza tra tensione di ingresso e tensione di riferimento)
- Integratori (più accurati, mediano la tensione di ingresso)

La risoluzione dei voltometri è sia dimensionale ($\Delta V$) e adimensionale ($\delta$): $$\Delta V= \frac{D}{N}\qquad \delta= \frac{\Delta V}{D}$$
### Prestazioni dei voltmetri in base all'architettura
>[!note]
>| $$\text{Letture}/s$$                  | $$1/\text{Incertezza}$$ | $$\text{Tipologia}$$ |
>| ------------------------------------- | ----------------------- | -------------------- |
>| Alta: ordine dei $\text{Gsa}/s$       | $$\frac{1}{10^{-3}}$$   | Flash                |
>| Media: ordine dei $\text{Msa}/s$      | $$\frac{1}{10^{-5}}$$   | Approx. successive   |
>| Bassa: ordine dei $\text{sa}/\text{s}$ | $$\frac{1}{10^{-7}}$$   | integratori          |

### Voltmetri differenziali
>[!note]
>Un voltometro differenziale effettua la misura di una tensione incognita $V_{x}$ mediante il confronto diretto con una tensione di riferimento $V_{r}$ disponibile internamente allo strumento. La tensione $V_{r}$ è variabile e per generarla si ricorre ad una tensione $V_{0}$ di elevata accuratezza e stabilità.
>![[Pasted image 20241128113051.png]]
>$V_{r}$ viene variata da $V_{x,\max}$ a $V_{x,\min}$ e si registra quel valore $V_{r}^{*}$ per cui l'uscita del comparatore commuta di livello. $V_{r}^{*}$ viene quindi inviata al display del voltmetro.
>
 
>[!tip] Voltmetro potenziometrico
>![[Pasted image 20241128113340.png]]
>Dove: $$V_{r}=kV_{0}\qquad V_{r}^{*}=k^{*}V_{0}=V_{x}$$
>La risoluzione di misura dipende dalla risoluzione del divisore potenziometrico (e passo del motore). La sensibilità di misura viene aumentata grazie all'amplificazione in ingresso, consentendo di rivelare segnali $V_{x}$ deboli con una maggiore insensibilità al rumore del comparatore. Generalmente ha una risoluzione bassa, una velocità bassa e un costo contenuto, infatti oggi risulta praticamente in disuso.
 
>[!tip] Voltmetro a rampa analogica
>![[Pasted image 20241128114103.png]]
>È una versione a stato solido (veloce e affidabile) del voltmetro potenziometrico. La risoluzione solitamente è di 4 o 5 cifre. Opera secondo una conversione tensione/tempo e la tensione $V_{x}$ viene misurata contando un certo numero di periodi di clock $T_{c}$ in un intervallo di tempo $\Delta T_{G}$ (che è proporzionale al modulo di $V_{x}$): $$|V_{x}|= \frac{\Delta T_{G}}{\frac{T_\text{rampa}}{2}}V_{m}=\frac{2N_{C}T_{C}}{T_\text{rampa}}V_{m}$$
>Il segno di $V_{x}$ si deduce invece da quale comparatore scatta prima.
>Molte volte l'errore può essere solo positivo, o solo negativo, risultato ad es. limitato all'intervallo $[0, T_{C}]$. Altre volte l'errore di quantizzazione si ha sia su $T_\text{start}$ che su $T_\text{stop}$:
>![[Pasted image 20241128114830.png]]
>Da cui ricaviamo le formule: $$\begin{align*}
>&T_\text{stop}-T_\text{start}=\Delta T_{G}\propto |V_{x}|\\
>&\Delta T_{G}=NT_{C}+e_{1}-e_{2}\\
>&\sigma^{2}(\Delta T_{G})=\sigma^{2}(e_{1})+\sigma^{2}(e_{2})\\
>&u(\Delta T_{G})=\sigma^{2}(\Delta T_{G})=\sqrt2 \frac{T_{C}}{\sqrt{12}}
>\end{align*}$$
>La rampa analogica varia linearmente da $-V_{M}$ a $+V_{M}$ con periodo $T_\text{rampa}= \frac{1}{f_\text{rampa}}$. Il tempo di misura è $T_\text{mis}=T_\text{rampa}$. Per una lettura con risoluzione $\delta= \frac{1}{N}= \frac{1}{2N_{c,\max}}$ dove $N_{c,\max}= \frac{N}{2}$ è il massimo valore di conteggi del contatore, deve essere $$f_{c}=N\times f_\text{rampa}=2N_{c,\max}\times f_\text{rampa}\Longrightarrow N= \frac{f_{c}}{f_\text{rampa}}$$
>Di conseguenza: $$\begin{align*}
&\delta= \frac{1}{N}= \frac{\Delta V}{D}= \frac{T_{c}}{T_\text{rampa}}= \frac{f_\text{rampa}}{f_{c}}&\quad \text{risoluzione}\\
&m=\log_{10}(N)=\log_{10}\left( \frac{f_{c}}{f_\text{rampa}}\right)&\quad\text{ cifre decimali}\\
&n=\log_{2}(N)=\log_{2}\left( \frac{f_{c}}{f_\text{rampa}}\right)&\quad\text{bit}\\
\end{align*}$$
>La risoluzione migliora al crescere del rapporto $\frac{f_{c}}{f_\text{rampa}}$. Aggiungiamo infine che $p$ è la pendenza della rampa analogica: $$p= \frac{2V_{M}}{T_\text{rampa}}\quad \left[\frac{\text{V}}{\text{s}}\right]$$
 
>[!tip] Voltmetro a convertitore flash
>È l'architettura di voltometro più veloce, raggiunge frequenza di conversione fino a $50 \text{ GSa/s}$. Tuttavia la complessità circuitale cresce esponenzialmente con il numero di bit e si lavora quindi con una bassa risoluzione.
>![[Pasted image 20241128122233.png]]
>Questo è il convertitore AD utilizzato negli oscilloscopi digitali, dove la risoluzione modesta non è un fattore limitante mentre la velocità è importante.
>La dinamica di misura viene suddivisa in $N=2^{n}$ livelli equispaziati ($\Delta V= \frac{V_{\max}}{2^{n}}$) utilizzando $N-1=2^{n}-1$ soglie (e comparatori). Tipicamente si lavora con $N=256$ livelli e dunque la risoluzione relativa è $\delta= \frac{1}{256}$. È usato per misure su segnali molto veloci ma con accuratezza limitata.

>[!tip] Voltmetro ad approssimazioni successive
>![[Pasted image 20241128161558.png]]
>È un convertitore DA a $n$ bit. Utilizza il metodo di bisezione: si confronta, a partire dal MSB al LSB, con $V_{x}$, e si decide se mantenere il bit a $1$ o riportarlo a $0$.
>La cifra meno significativa a peso $\Delta V= \frac{V_{FS}}{2^{n}}$, mentre la più significativa vale $\frac{V_{FS}}{2}$. Si eseguono $n=\log_{2}(N)$ confronti, ciascuno di durata $mT_{C}$, con $2<m<5$. Il tempo di misura è fissato indipendentemente da $V_{x}$ e vale $T_\text{mis}=nT_\text{confr.}=n(mT_{c})$.
>Il rumore differenziale può portare istantaneamente a errate decisioni sul singolo confronto, e dunque ad un errore di misura.

### Voltmetri a integrazione
>[!note]
>In un voltmetro ad integrazione, il valore di misura dipende dal segnale (tensione) in ingresso secondo una relazione integrale: $$V_{m}\propto \frac{1}{T_{1}}\int_{0}^{T_{1}}V(t)\text{ d}t$$
>Sapendo che $V(t)=V_{x}+\underbrace{V_{d}(t)}_\text{Disturbo}$: $$V_{m}(T_{1})= \frac{1}{T_{1}}\int_{0}^{T_{1}}[V_{x}+V_{d}(t)]\text{ d}t=V_{x}+ \underbrace{\frac{1}{T_{1}}\int_{0}^{T_{1}}V_{d}(t)\text{ d}t}_\text{deve essere nullo}$$
>Se è nota la frequenza del disturbo, può essere utile scegliere un $T_{1}$ opportuno, ma, in generale, per $T_{1}$ lungo la reiezione al disturbo migliora.

>[!example] Dimostrazione
>Avendo un disturbo "sinusoidale qualsiasi" (con fase $\varphi$ arbitraria) su un intervallo di integrazione sempre $T_{1}$ ma centrato su "$t_{0}$ qualsiasi", abbiamo che: $$\begin{align*}
V_{d}(t)&=V_{d,0}\sin(2\pi ft+\phi)&\\
V_{d,m}&= \frac{1}{T}\int\limits_{t_{0}-\frac{T}{2}}^{t_{0} + \frac{T}{2}}V_{d}(t)\text{ d}t=
\frac{1}{T}\int\limits_{t_{0}-\frac{T}{2}}^{t_{0} + \frac{T}{2}}V_{d,0}\sin(2\pi ft+\phi)\text{ d}t=\\
&=\frac{V_{d,0}}{2\pi fT}\left\{\cos\left[2\pi f\left(t_{0}- \frac{T}{2}\right)+\phi\right]-\cos\left[2\pi f\left(t_{0}+ \frac{T}{2}\right)+\phi\right]\right\}\\\\
&= \frac{V_{d,0}}{2\pi fT}2\sin(2\pi ft_{0}+\phi)\sin(2\pi f \frac{T}{2})\\
&=V_{d,0}\frac{\sin(\pi f T)}{\pi fT}\sin(2\pi ft_{0}+\phi)
\end{align*}$$
Massimizzandolo otteniamo: $$V_{d,m}(T)=V_{d,0}\frac{\sin(x)}{x}F(t_{0},\phi)$$
Dove $x=\pi f T$, e $F(t_{0},\phi)=\sin(2\pi f t_{0}+\phi)$.

Lavorando a $f$ e $T$ fissati, e facendo variare arbitrariamente $\varphi$ e/o $t_{0}$, si ottiene per il disturbo integrato un valore efficace: $$V_\text{d,m,eff}=\sqrt{\left\langle V^{2}_{d,m}(T) \right\rangle}= \frac{1}{\sqrt{2}}\frac{|\sin(x)|}{x}V_{d,0}\cong 0.7\cdot V_\text{d,m,max}$$
La trasmissione ($t$) e la reiezione ($r$) del disturbo, in ampiezza, saranno: $$\begin{align*}
t&= \left|\frac{V_{d,m}}{V_{d,0}} \right|=\left|\frac{\sin(x)}{x}\right|\\
r&= \left|\frac{V_{d,0}}{V_{d,m}} \right|=\left|\frac{x}{\sin(x)}\right|
\end{align*}$$
La reiezione cresce (tendenzialmente) al crescere di $x$ e dunque di $f_{d}$ e $T_{1}$ e inoltre $r\to\infty$ se $f_{d}\cdot T_{1}=m$. Quindi la trasmissione di potenza del disturbo è: $$T=t^{2}=\frac{\sin^{2}(x)}{x^{2}}$$
Mentre la reiezione in potenza del disturbo è: $$R=r^{2}=\frac{x^{2}}{\sin^{2}(x)}\qquad R_\text{db}=10\log_{10}(R)=20\log_{10}\left|\frac{x}{\sin(x)}\right|$$
Si usa un circuito integratore:
![[Pasted image 20241128172331.png]]
Dove: $$\begin{align*}
V_{C}&= -Z_{C}I=- \frac{1}{j\omega RC}V_{x}=-\int \frac{V_{x}}{RC}\text{ d}t\\
I&= \frac{V_{x}}{R}
\end{align*}$$
### Voltmetro a doppia rampa
>[!note]
>![[Pasted image 20241129142822.png]]
>Da un punto di vista analitico $T_\text{mis}=T_{u}+T_{d}$ è una variabile che dipende da $V_{x}$ come nel rampa analogica: $$\begin{align*}\\
T_{u}&= N_{u}T_{c}\\
V_{0}&= V_{c}(T_{u})=- \frac{V_{x}T_{u}}{RC}\\
V_{x}&= -V_{r} \frac{T_{d}}{T_{u}}=-V_{r}\frac{N_{d}T_{c}}{N_{u}T_{c}}=-V_{r} \frac{N_{d}}{N_{u}}
\end{align*}$$
La misura è teoricamente insensibile a valori e incertezze di RC e agli altri parametri strumentali ($f_{c}$ e $T_{c}$), che pesano allo stesso modo su rampa di salita e discesa.
L'incertezza di quantizzazione è: $$u_{q}(V_{x})= \frac{\Delta V}{\sqrt{12}}= \left(- \frac{V_{r}}{T_{u}}\right)\cdot \frac{T_{c}}{\sqrt{12}}= - \frac{V_{r}}{N_{u}\sqrt{12}}$$

### ADC Pipeline
>[!note]
>![[Pasted image 20241129144157.png]]
>La massima risoluzione ottenibile si aggira intorno a $24\text{ bit}$ da un minimo di $8\text{ bit}$ con frequenze che vanno da $1 \text{ Msa/s}$ a $200\text{ Msa/s}$. Il tempo di latenza equivale al numero di conversioni $p$ moltiplicato per il tempo di conversione: $$T_\text{latenza}=T_\text{clock}\cdot p$$
