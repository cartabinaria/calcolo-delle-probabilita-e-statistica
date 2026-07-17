---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 28-04-2025 23:27:53
links:
  - "[[lecture-11042025131834|Lecture 11042025131834]]"
---
# Standardizzazione
---
## Introduzione
> La **standardizzazione** e' un processo che consente di passare da una [[variabile-aleatoria-continua|variabile aleatoria continua]] $X$ con [[distribuzione-normale|distribuzione normale]] di [[valore-atteso|media]] $\mu$ e [[varianza|varianza]] $\sigma^{2}$ ad una variabile aleatoria continua $Z$ con [[distribuzione-normale-standard|distribuzione normale standard]]. Formalmente se $X \sim \mathcal{N}(\mu, \sigma^{2})$, si definisce
> $$Z := \frac{X - \mu}{\sigma} \sim \mathcal{N}(0, 1)$$

### Dimostrazione
So per ipotesi che la [[densita-continua|densita' continua]] di $X$ e' data da
$$f_{X}(x) = \frac{1}{\sigma\sqrt{2 \pi}} e^{- \frac{(x - \mu)^{2}}{2 \sigma^{2}}}$$

Devo mostrare
$$f_{Z}(z) = \frac{1}{\sqrt{2 \pi}} e^{- \frac{z^{2}}{2}}$$

Parto definendo la [[funzione-di-ripartizione|funzione di ripartizione]] di $Z$ in funzione di quella di $X$:
$$F_{Z}(z) = P(Z \leq z) = P\left(\frac{X - \mu}{\sigma} \leq z\right) = P(X \leq z \sigma + \mu) = F_{X}(z \sigma + \mu)$$

Ora calcolo la densita' continua di $Z$, semplicemente come derivata di $F_{Z}(z)$:
$$f_{Z}(z) = F_{Z}'(z) = \sigma F_{X}'(z\sigma + \mu) = \sigma f_{X}(z\sigma + \mu) = \sigma \frac{1}{\sigma\sqrt{2 \pi}} e^{- \frac{(z\sigma + \mu - \mu)^{2}}{2 \sigma^{2}}} = \frac{1}{\sqrt{2 \pi}} e^{- \frac{z^{2}}{2}}$$

**Qed**.

## Referenze