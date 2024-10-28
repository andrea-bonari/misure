>[!note]
>L'interpolazione è una tecnica che permette di rappresentare dei dati discreti con una funzione continua detta interpolante, che ci fornisce l'andamento presunto della relazione ingresso-uscita.

### Interpolazione lineare
>[!note]
>È la più semplice interpolazione possibile. Consiste nel congiungere i punti con una spezzata.
>![[Pasted image 20241025101214.png]]

### Interpolazione polinomiale cubica
>[!note]
>Consiste nell'utilizzare una curva che passa per i punti sperimentali, mantenendo continue la derivata prima e seconda. La funzione è detta spline ed è definita come: $$S_{i}(x)=ax^{3}+bx^{2}+cx+d$$
>Le condizioni sono per la funzione sono le seguenti:
>-  Proprietà di interpolazione $S(x_{i})=f(x_{i})$
>- Continuità delle spline $S_{i-1}(x_{i})=S_{i}(x_{i})\quad \forall i=1,\cdots,n-1$
>- Continuità delle derivate $S_{i-1}'(x_{1})=S_{i}'(x_{i})\quad S_{i-1}''(x_{1})=S_{i}''(x_{i})\quad \forall i=\,\cdots,n-1$
>
>Otteniamo quindi $4n-2$ condizioni. Abbiamo quindi bisogno di altre due condizioni che possono essere di questo tipo: $$S'(x_{i})=\text{const}\quad S'(x_{n})=\text{const}$$
>![[Pasted image 20241025102434.png]]

### Interpolazione a seno cardinale
>[!note]
>È utilizzata per la ricostruzione di segnali campionati nel tempo. Si ricava matematicamente dall'operazione di filtraggio passa-basso ideale del segnale campionato. Nel dominio del tempo consiste in una convoluzione del segnale campionato con la funzione $\text{sinc}= \frac{\sin(x)}{x}$.
>![[Pasted image 20241025102606.png]]



