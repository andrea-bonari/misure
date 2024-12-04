>[!note]
>L'oscilloscopio digitale è l'evoluzione dell'oscilloscopio analogico, mitigando le sue debolezze. 
>![[Pasted image 20241202162917.png]]
>A differenza di un oscilloscopio analogico l'oscillogramma non è in tempo reale con il segnale. Inoltre il segnale è visualizzato tramite un display raster. Infine permette di usare dispositivi I/O per il trasferimento dati (interfacce RS-232, GPIB, USB, TCP-IP).

>[!tip] Front-end analogico
>![[Pasted image 20241202163630.png]]
>Il commutatore varia il coefficiente di deflessione secondo i passi tarati con la sequenza 1/2/5, tipicamente da $1\text{ mV/DIV}$ fino a $5\text{ V/DIV}$. Il grado di incertezza che il costruttore assegna alla taratura di questa sezione è dell'ordine dell'1%.

>[!tip] ADC
>![[Pasted image 20241202164225.png]]
>Al fine di massimizzare la frequenza di campionamento, si usa interlacciare più ADC.

Affinché l'occhio possa riconoscere distintamente la forma d'onda, il numero di campioni acquisiti deve essere sufficientemente elevato da non generare ambiguità di percezione. Il valore convenzionale è di almeno 25 punti per periodo, tuttavia usando un interpolatore a $\sin(x)/x$ questi si riducono a $2.5$.

### Trigger
>[!note]
>In base ad una pendenza o un valore può essere generato un segnale di sincronismo: 
>![[Pasted image 20241202193038.png]]
>Esistono modalità di trigger diverse per evitare segnali di trigger date da un rumore.

Durante il campionamento e la conversione le $M$ celle di memoria vengono riempite in modo contiguo. Al verificarsi dell'evento trigger l'unità elaborativa contrassegna il campione acquisito in quell'istante, così da poter identificare i campioni precedenti e quelli successivi al campione/evento di trigger: consente di visualizzare sullo schermo l'andamento del segnale anche "prima" dell'evento di trigger.
![[Pasted image 20241204145206.png]]

### Modalità di campionamento
>[!note]
>Il campionamento di un DSO può avvenire secondo tre differenti modalità:
>- Campionamento in tempo reale
>- Campionamento in tempo equivalente di tipo sequenziale
>- Campionamento in tempo equivalente di tipo casuale

 >[!tip] Campionamento in tempo reale
 >La sequenza dei dati acquisiti rispetta la sequenza temporale dei punti della forma d'onda che evolve sull'asse dei tempi.
 
 >[!tip] Campionamento in tempo equivalente sequenziale
 >Si prendono diversi campioni all'interno di periodi differenti del segnale. Dall'insieme di campioni acquisiti in un tempo più lungo del periodo $T$, si può ricostruire l'andamento della forma d'onda nel singolo periodo.
 >
 >All'interno di ogni evento di trigger, si acquisisce un singolo campione, con ritardo via via crescente. 
 >Per la ripetitività con periodo $T$ del segnale $s(t)$, i campioni prelevati agli istanti di tempo $\tau$ e $\tau+kT$ risultano uguali. Quindi, si può adottare il periodo di campionamento rallentato $T_{C}=kT+\tau$: $$f_{c}^{*}= \frac{1}{\tau}\qquad f_{c}= \frac{1}{kT+\tau}$$
 >
 >Nella frequenza campionata e ricostruita in tempo equivalente, si ottiene una risoluzione temporale $\tau$ tra due campioni adiacenti molto spinta, che non sarebbe ottenibile in tempo reale con lo stesso ADC.
 >![[Pasted image 20241204151253.png]]
 
>[!tip] Campionamento in tempo equivalente casuale
>I campioni vengono prelevati in modo casuale, sia prima, sia dopo gli eventi di trigger. L'intervallo di tempo (positivo o negativo) tra ciascun evento di trigger e il successivo campione deve essere misurato in modo da poter ordinare correttamente i campioni sul display così da ricostruire l'andamento del segnale.
>
>In questo caso $\tau$ non è più la risoluzione temporale del ritardo, ma del contatore elettronico.
>![[Pasted image 20241204151312.png]]

### Risoluzione
>[!note] Risoluzione verticale
>Assegnato un valore del coefficiente di deflessione verticale, il campo dei valori in ampiezza ammessi (dinamica) con quello compreso tra le due linee orizzontali estreme del reticolo sullo schermo ($8\text{ div}\cdot A_{y,V/\text{div}}$).

È possibile migliorare la qualità del segnale acquisito nei seguenti modi:
- Media tra più tracce acquisite
- Sovracampionamento e decimazione
- High definition: come il precedente ma con l'aggiunta di un segnale addizionale a media nulla nel periodo di decimazione.

>[!note] Risoluzione orizzontale
>La limitazione principale della risoluzione temporale è la frequenza di campionamento $f_{c}$:
>- In modalità tempo reale la miglior risoluzione è il minimo $T_{c}$ dell'ADC.
>- In modalità sequenziale in tempo equivalente la risoluzione è limitata dal ritardo $\tau$ tra campioni equivalenti adiacenti.
>- In modalità casuale in tempo equivalente la risoluzione è limitata dalla misura dell'intervallo di misura di tempo tra l'istante di campionamento e l'evento trigger.

### Funzioni digitali
>[!tip] Autoset
>Lo strumento cerca la migliore configurazione dei parametri di misura e la predispone.

>[!tip] Cursori
>Lo strumento aggiunge dei cursori di ampiezza e tempo, che consentono di leggere direttamente sul display misure di differenze di tensione o in intervalli di tempo.

>[!tip] Misure standard automatizzate
>Lo strumento fornisce la possibilità di misurare automaticamente delle misure comuni in ampiezza e in tempo.

>[!tip] Analisi spettrale
>Lo strumento esegue la FFT semplice, o anche analisi più complesse, ad esempio lo spettrogramma.

>[!tip] Pacchetti software
>Vengono forniti dei software che permettono di comunicare con lo strumento tramite protocolli di comunicazione digitali. Questi software generalmente permettono la verifica di compliance e l'analisi di segnali di potenza.

>[!tip] Funzionalità hardware addizionali
>Lo strumento fornisce funzionalità hardware addizionali come:
>- Generatore digitale di segnali
>- Voltmetro digitale
>- Contatore elettronico

### Sonde d'ingresso
>[!note]
>Le sonde di oscilloscopi sono componenti essenziali che permettono di prelevare e inviare segnali da un circuito all'oscilloscopio stesso. Sono costituite da un cavo coassiale con un connettore o puntale alla fine. Esistono diversi tipi di sonde: passive e attive.

>[!tip] Sonde passive
>![[Pasted image 20241204154657.png]]
>Se il cavo di collegamento fa parte di una sonda è possibile compensare l'impedenza di ingresso, grazie alla capacità di compensazione $C_{s}$, in modo che l'attenuazione tra $V_{\text{in}}$ e $V'_\text{in}$ sia indipendente dalla frequenza: $$a= \frac{V_{\text{in}}}{V'_{\text{in}}}= \frac{Z_{i}+Z_{s}}{Z_{i}}= \frac{ \frac{R_{i}}{1+j\omega R_{i}(C_{i}+C_{c})} + \frac{R_{s}}{1+j\omega R_{s}(C_{s})} }{ \frac{R_{i}}{1+j\omega R_{i}(C_{i} + C_{c})} }$$
>Durante la compensazione della sonda si varia la sua capacità $C_{s}$ sino ad ottenere un comportamento equalizzato alla frequenza: $$a= \frac{R_{i}+R_{s}}{R_{i}}$$
>Tipicamente con $R_{i}= 1\text{ M}\ohm$ e $R_{s}=9\text{ M}\ohm$ si attenua il segnale di un fattore di $10$ e si ottiene $R_\text{in}=10\text{ M}\ohm= 10 R_{i}$.
>
>In un segnale ad onda quadra la sonda può essere compensata correttamente, sovracompensata o sottocompensata: ![[Pasted image 20241204155303.png]]

>[!tip] Sonde attive
>Le sonde attive sono utili per fornire alta impedenza d'ingresso anche ad alte frequenze. Le più comuni tipologia di sonde attive sono:
>- sonde differenziali di tensione
>- sonde di corrente

