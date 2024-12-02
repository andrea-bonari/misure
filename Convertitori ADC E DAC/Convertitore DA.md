>[!note]
>Un convertitore digitale analogico converte un numero di livelli di linee digitali in una tensione quantizzata $V_\text{out}$ analogica.

### Modello a rete R
>[!note]
>Da un'unica tensione di riferimento costante ($V_\text{ref}$) si prelevano $n$ correnti pesate attraverso $n$ interruttori $S_{0},S_{1},\cdots,S_{n-1}$. Su ciascuno switch $S_{i}$ è posta una resistenza $r_{i}=2^{(n-1)-i}R$.
>![[Pasted image 20241127171014.png]]
>Gli switch $S_{i}$ sono comandati dalle cifre binarie $b_{i}$ del numero da convertire in tensione, con pesi tali che $b_{0}$ è il LSB e $b_{n-1}$ è il MSB.
>Infine un operazionale serve da sommatore delle correnti pesate che passano attraverso gli switch e converte la corrente risultante $i_\text{o}$, attraverso la resistenza di feedback, in un'uscita di tensione $V_\text{o}$. $$V_\text{o}=-R_{f}\cdot i_{o}$$
>Le correnti pesate sono pari a: $$i_{i}= \frac{V_\text{ref}}{2^{(n-1)-i}}R=2^{i}\frac{V_\text{ref}}{2^{(n-1)}R}=2^{i}I_\text{min}$$
>Di conseguenza, la corrente complessiva passante dagli switch è: $$i_{o}=\frac{V_\text{ref}}{2^{(n-1)}R}(b_{0}+2b_{1}+\cdots+2^{n-1}b_{n-1})$$
>L'accuratezza del DAC dipende da $V_\text{ref}$, dalle $r_{i}$ e dalla qualità degli switch.







