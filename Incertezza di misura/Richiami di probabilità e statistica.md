>[!note]
>La probabilità è una stima in termini numerici della possibilità di accadere un evento: $$p\in[0,1]$$

Sia $x\in\mathbb{R}$ una variabile casuale:

La probabilità che: $$P(a\leq x\leq b)=\int^{b}_{a}p(x)\text{ d}x$$
Dove $p(x)$ è la funzione di densità di probabilità. Essa descrive il processo casuale considerato assegnando la probabilità per i possibili valori d'uscita. Esiste la proprietà: $$\int_{-\infty}^{+\infty}p(x)\text{ d}x=1$$

Esistono degli stimatori che ci consentono di conoscere, in senso statistico, alcuni parametri caratteristici del processo casuale. In particolare media e varianza permettono di stimare la tendenza centrale e la dispersione dei valori $x$ associabili a $x$.

Per quanto riguarda la media: $$\mu(x)=\mu_{x}=E\set{x}=\int_{-\infty}^{+\infty}x p(x)\text{ d}x$$
Mentre la varianza: $$\sigma^{2}(x)=\sigma^{2}_{x}=E\set{[x-\mu_{x}]^{2}}=\int^{+\infty}_{-\infty}[x-\mu_{x}]^{2}p(x)\text{ d}x$$
Definiamo la deviazione standard come: $$\sigma_{x}=\sqrt{\sigma^{2}_{x}}$$
### PDF normale
>[!note]
>È la PDF più comune per la descrizione della media di fenomeni casuali quali le misure: $$p(x)= \frac{1}{\sqrt{2\pi}\sigma}e^{-\frac{[x-\mu]^{2}}{2\sigma^{2}}}$$
>Le aree sottese dalla curva PDF sono le probabilità di avere valori in un dato intervallo di valori sull'asse reale.
>![[Pasted image 20241003091605.png]]
>Lontano dalla media $\mu$, rispetto a $\sigma$, la PDF diviene molto bassa e dunque le aree sottese sono molto piccole: $$\begin{align*}
1\sigma\qquad 68.27\% \\
2\sigma\qquad 95.45\%\\
3\sigma\qquad 99.73\%
\end{align*}$$

### PDF uniforme
>[!note]
>![[Pasted image 20241003091916.png]]
>Possiamo dire che: $$p(x)=\begin{cases}
>0& x<a_{0}-a \\
>\frac{1}{2}a& a_{0}-a\leq x\leq a_{0}+a \\
>0& x>a_{0}+a
>\end{cases}$$
>Il valore medio: $$\mu(x)=E[x]=\int^{+\infty}_{-\infty} x\space p(x)\text{ d}x=a_{0}$$
>Mentre la deviazione standard: $$\sigma(x)=\frac{\Delta x}{\sqrt{12}}$$

>[!example] Dimostrazione valore medio
>$$\begin{align*}
\mu(x)&= \int^{+\infty}_{-\infty}x\space p(x)\text{ d}x=\int^{a_{0}+a}_{a_{0}-a}x\frac{1}{2a}\text{ d}x\\
&= \frac{1}{2a} \left[ \frac{x^{2}}{2}\right]^{a_{0}+a}_{a_{0}-a}= \frac{1}{2a}\cdot \frac{2a_{0}a+2a_{0}a}{2}&=a_{0}
\end{align*}$$

>[!example] Dimostrazione deviazione standard
>$$\begin{align*}
\sigma^{2}(x) &= E[(x-\mu(x))^{2}]=\int^{+\infty}_{-\infty}(x-\mu(x))^{2}\space p(x)\text{ d}x\\
&= \int^{a_{0}+a}_{a_{0}-a}(x-a_{0})^{2} \frac{1}{2a} \text{ d}x= \frac{1}{2a}\left[ \frac{(x-a_{0})^{3}}{3}\right]^{a_{0}+a}_{a_{0}-a}\\
&= \frac{1}{2a} \left[ \frac{a^{3}}{3}- \left(- \frac{a^{3}}{3}\right)\right]= \frac{a^{2}}{3}&= \frac{(\Delta x)^{2}}{12}
\end{align*}$$

### PDF triangolare
>[!note]
>![[Pasted image 20241003093013.png]]
>Possiamo dire che: $$\mu(x)=a_{0}$$
>$$\sigma(x)= \frac{\Delta x}{\sqrt{24}}$$

