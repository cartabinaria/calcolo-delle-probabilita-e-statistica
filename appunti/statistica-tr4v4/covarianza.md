---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 19-05-2025 21:15:06
links:
  - "[[lecture-29042025132447|Lecture 29042025132447]]"
---
# Covarianza
---
## Introduzione
> Sia $(X, Y)$ un [[vettore-aleatorio|vettore aleatorio]], allora
> $$Cov(X, Y) = \mathbb{E}[(X - \mathbb{E}[X])(Y - \mathbb{E}[Y])]$$
> equivalente a
> $$Cov(X, Y) = \sum\limits_{i,j} (x_{i} - \mathbb{E}[X])(y_{j} - \mathbb{E}[Y]) p_{(X, Y)}(x_{i}, y_{j})$$

## Incorrelazione
Se
$$Cov(X, Y) = 0$$
allora si dice che $X$ e $Y$ sono **incorrelate**.

## Teoremi
### Lemma
> Sia $(X, Y)$ vettore aleatorio, allora
> $$Cov(X, Y) = \mathbb{E}[XY] - \mathbb{E}[X]\mathbb{E}[Y]$$

### Teorema
> Se $X, Y$ sono [[indipendenza-di-variabili-aleatorie|indipendenti]], allora $Cov(X, Y) = 0$.

<u>Nota bene</u>: non vale il viceversa!

Di fatto, se la covarianza e' 0 significa che non c'e' una dipendenza _lineare_ tra $X$ e $Y$; se invece $X, Y$ sono indipendenti, non c'e' una dipendenza _funzionale_ tra $X$ e $Y$!

## Referenze
- [[coefficiente-di-correlazione|Coefficiente di correlazione]]