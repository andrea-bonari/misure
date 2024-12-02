>[!note]
>Disponendo di un voltmetro che quantizza un segnale $s(t)$ mediante $n$ bit, si avrà un passo di quantizzazione: $$\Delta V= \frac{D}{2^{n}}$$
>Se $D$ è la dinamica del segnale e anche del voltmetro, si ha una varianza ("incertezza di quantizzazione"): $$\sigma^{2}_{q}= \frac{Q^{2}}{12}= \frac{1}{12} \left(\frac{D}{2^{n}}\right)^{2}= \frac{\sigma^{2}_{s}}{2^{2n}}$$
>In un convertitore ideale: $$n= \frac{1}{2}\log_{2} \left(\frac{\sigma_{s}^{2}}{\sigma^{2}_{q}}\right)$$
>Tuttavia in un convertitore reale: $$\sigma_{c}^{2}=\sigma_{q}^{2}+\sigma^{2}_{n,AD}+\sigma^{2}_{m,\text{ext}}>\sigma_{q}^{2}$$
>Definiamo quindi il numero di bit equivalenti come: $$n_{e}\equiv \frac{1}{2}\log_{2} \left(\frac{\sigma^{2}_{s}}{\sigma^{2}_{c}}\right)=n - \frac{1}{2}\log_{2}\left(1+\frac{\sigma^{2}_{n,\text{AD}}+\sigma^{2}_{n,\text{EXT}}}{\sigma^{2}_{q}}\right)$$

