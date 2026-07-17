---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 14-04-2025 20:44:23
links:
  - "[[lecture-01042025132135|Lecture 01042025132135]]"
---
# Distribuzione di Bernoulli
---
## Introduzione
> La **distribuzione di Bernoulli** e' una [[distribuzioni-notevoli-di-variabili-aleatorie-discrete|distribuzione notevole]] su [[variabile-aleatoria-discreta|variabile aleatoria discreta]] $X$ che _assegna la probabilità $p$ a un certo [[evento|evento]] e la probabilità $1 - p$ al complementare_.
> In tal caso, si dice che $X$ ha la legge di Bernoulli, e si indica
> $$X \sim B(p)$$

Formalmente, fissato un parametro $p \in [0, 1]$, prendiamo $S_{X} = \{0, 1\}$ il supporto di $X$ e la [[densita-discreta|densita' discreta]] $p_{X}$ come

| $X$     | $0$     | $1$ |
| ------- | ------- | --- |
| $p_{X}$ | $1 - p$ | $p$ |

Si ha che le [[variabile-aleatoria-indicatrice|variabili aleatorie indicatrici]] $X = \mathbb{1}_{A}$ con $A$ [[evento|evento]] ($\subseteq \Omega$) sono distribuite secondo la distribuzione di Bernoulli! Infatti se $p = \mathbb{P}(A)$ allora
$$p_{X}(0) = 1 - \mathbb{P}(A) \ \ \ \ \ \ p_{X}(1) = \mathbb{P}(A)$$

## Proprieta'
### Valore atteso
Il [[valore-atteso|valore atteso]] di una variabile aleatoria discreta con distribuzione di Bernoulli e' dato da
$$\mathbb{E}[X] = p$$

### Varianza
La [[varianza|varianza]] di una variabile aleatoria discreta con distribuzione di Bernoulli e' data da
$$Var(X) = p(1 - p)$$

## Referenze