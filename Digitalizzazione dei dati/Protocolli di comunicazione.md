### Interfaccia seriale RS-232
>[!note]
>![[Pasted image 20241024105959.png]]
>La comunicazione seriale è a tre vie:
>- Ricezione
>- Trasmissione
>- Ground
>
>Ci sono altre linee però non sono richieste

Da un punto di vista elettronico $1$ significa una tensione compresa tra $+3V$ e $+12V$, mentre $0$ significa una tensione compresa tra $-3V$ e $-12V$.

I parametri fondamentali sono:
- baud rate (velocità di trasmissione)
- data bits
- stop bits
- parity bit

### Interfaccia IEEE-488 (GPIB)
>[!note]
>Anche conosciuta come interfaccia parallela. Ha:
>- 8 linee dati, 5 linee di gestione dell'interfaccia e 3 linee di handshake
>- codice di trasferimento di ASCII a 7 bit e un bit di parità
>
>Può collegare un massimo di 15 dispositivi con una lunghezza massima di collegamento pari a $20\text{ m}$. Ha una velocità massima di $1\frac{\text{ Mbyte}}{s}$. Ogni dispositivo collegato ha un suo indirizzo GPIB, e può assumere 3 ruoli (assumibili contemporaneamente):
>- LISTENER
>- TALKER
>- CONTROLLER

### Interaccia USB
>[!note]
>L'interfaccia Universal Serial Bus è uno standard di comunicazione seriale che permette di collegare diverse periferiche. È composto da 4 pin:
>1. VBUS: alimentazione ($+5V$)
>2. $D^{-}$: ricezione
>3. $D^{+}$: trasmissione
>4. GND: riferimento di massa
>
>![[Pasted image 20241024112613.png]]
>
>Fino alla versione 2.0 si utilizzava una connessione half duplex, mentre nella 3.0 si usa full duplex. Può operare in diverse modalità:
>- Control: operazioni di comando e stato
>- Interrupt: latenze garantite, pochi dati trasferiti
>- Bulk: latenze non garantite, trasferimento di un grosso pacchetto di dati
>- Isosinchronous: trasferimento continuo di dati

### Interfaccia USB-C
>[!note]
>Il connettore USB-C è un evoluzione di USB non retrocompatibile. È nato per un esigenza di mercato e ha 24 pin. Implementa il protocollo thunderbolt.
>![[Pasted image 20241024113918.png]]

