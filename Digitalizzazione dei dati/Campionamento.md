>[!note]
>Il segnale campionato $v(k T_{c})=x_{c}(t)$ idealmente si ottiene prelevando i campioni in un tempo infinitesimo, ma nella realtà occorre un tempo finito ($T_{w}\neq0$) per prelevare da $v(t)$ il segnale campionato $v(t_{k})$ e per quantizzarlo. 

Da un punto di vista matematico abbiamo un segnale $v(t)=x(t)$ reale e continuo.

Idealmente, nel campionamento, il segnale è moltiplicato per un treno di delta di Dirach $h(t)=\partial(t)$ , tuttavia realmente il segnale è moltiplicato per il treno di rettangoli $h(t)=\text{rect}(t / T_{w})$ in cui ogni rettangolo ha durata finita $T_{w}$.

Il segnale campionato ideale nel dominio temporale è: $$x_{c}(t)=x(t)\sum\limits_{k=-\infty}^{+\infty}\partial(t-kT_{c})$$
Mentre nel dominio spettrale è: $$X_{c}(f)=f_{c}\sum\limits_{k=-\infty}^{+\infty} X(f-mf_{c})$$
### Teorema di Shannon
>[!note]
>Un filtro passa-basso ideale con frequenza di taglio pari alla frequenza di Nyquist $f_{N}= \frac{f_{c}}{2}$ permette di ricostruire il segnale originale, dal segnale campionato, se la massima frequenza $f_\text{max}$ del segnale di ingresso è tale che $f_\text{max}\leq f_{N}$. In caso contrario si potrebbe avere un equivocazione sul segnale ricostruito.

In generare per ridurre gli effetti provocati dall'aliasing e dalla durata finita del campionamento si adottano frequenze di campionamento ben superiori al limite imposto dal teorema di Shannon.

### Campionatore Sample & Hold
>[!note]
>L'interno di un campionatore è il seguente:
>![[Pasted image 20241023151701.png]]
>Ad interruttore chiuso, la tensione campionata viene "memorizzata" su un condensatore (memoria analogica) che poi la mantiene quando l'interruttore è aperto.

