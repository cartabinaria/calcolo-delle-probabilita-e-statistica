---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 28-04-2025 23:13:04
links:
  - "[[lecture-11042025131834|Lecture 11042025131834]]"
---
# Distribuzione normale standard
---
## Introduzione
> La **distribuzione normale standard** e' una [[distribuzione-normale|distribuzione normale]] con media $\mu = 0$ e varianza $\sigma^{2} = 1$. In tal caso, si dice che $X$ ha la legge normale standard, e si indica
> $$X \sim \mathcal{N}(0, 1)$$

Questa distribuzione e' cosi' importante da aver coniato simboli propri per rappresentare la [[densita-continua|densita' continua]] e la [[funzione-di-ripartizione|funzione di ripartizione]], rispettivamente pari a
$$\varphi(x) = \frac{1}{\sqrt{2 \pi}} e^{- \frac{x^{2}}{2}}$$
$$\Phi(x) = \int_{-\infty}^{x} \frac{1}{\sqrt{2 \pi}} e^{- \frac{y^{2}}{2}} \, dy$$

Questa distribuzione si dimostra essere una generalizzazione della distribuzione normale, attraverso il processo di [[standardizzazione|standardizzazione]].

## Proprieta'
### Valore atteso
Il [[valore-atteso|valore atteso]] di una variabile aleatoria continua con distribuzione normale standard e' quindi
$$\mathbb{E}[X] = 0$$

### Varianza
La [[varianza|varianza]] di una variabile aleatoria continua con distribuzione normale standard e' quindi
$$Var(X) = 1$$

### $\Phi(0)$
Per costruzione, la [[funzione-di-ripartizione|funzione di ripartizione]] di una distribuzione normale standard nel punto $0$ e' pari a
$$\Phi(0) = \int_{-\infty}^{0} \frac{1}{\sqrt{2 \pi}} e^{- \frac{y^{2}}{2}} \, dy = \frac{1}{2}$$

### $\Phi(-x)$
In quanto simmetrica rispetto all'origine la densita' $\varphi(x)$, l'area nell'intervallo $(-\infty, -x)$ e' uguale a quella nell'intervallo $(x, +\infty)$, quindi
$$\Phi(-x) = \int_{-\infty}^{-x} \frac{1}{\sqrt{2 \pi}} e^{- \frac{y^{2}}{2}} \, dy = \int_{x}^{+\infty} \frac{1}{\sqrt{2 \pi}} e^{- \frac{y^{2}}{2}} \, dy = 1 - \Phi(x)$$

## Referenze