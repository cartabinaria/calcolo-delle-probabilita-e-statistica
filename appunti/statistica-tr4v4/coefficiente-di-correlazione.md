---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 19-05-2025 21:22:32
links:
  - "[[lecture-29042025132447|Lecture 29042025132447]]"
---
# Coefficiente di correlazione
---
## Introduzione
> Sia $(X, Y)$ un [[vettore-aleatorio|vettore aleatorio]], allora si definisce **coefficiente di correlazione** tra $X$ e $Y$ il valore
> $$\rho_{X, Y} = \frac{Cov(X, Y)}{\sqrt{Var(X)Var(Y)}} \in [-1, 1]$$

## Casi
Il coefficiente ha un significato profondo sulla relazione lineare tra $X$ e $Y$:
- $\rho_{X, Y} = \pm 1 \iff Y = aX + b$ per qualche $a, b \in \mathbb{R}$;
- $\rho_{X, Y} \in (0, 1) \iff \text{approssimativamente dipendenza lineare}$ --> caso della [[regressione-lineare|regressione lineare]];
- $\rho_{X, Y} = 0 \iff \text{non ho alcuna dipendenza lineare}$.

Quindi, **l'[[indipendenza-di-variabili-aleatorie|indipendenza]] e' un qualcosa di molto più forte**, perché _elimina una qualunque dipendenza funzionale, per cui anche quella lineare_. Se invece sappiamo che la covarianza è 0, possiamo solo escludere la dipendenza lineare!

## Referenze