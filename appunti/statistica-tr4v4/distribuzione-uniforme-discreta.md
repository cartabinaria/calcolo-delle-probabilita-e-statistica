---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 14-04-2025 20:30:53
links:
  - "[[lecture-01042025132135|Lecture 01042025132135]]"
---
# Distribuzione uniforme discreta
---
## Introduzione
> La **distribuzione uniforme discreta** e' una [[distribuzioni-notevoli-di-variabili-aleatorie-discrete|distribuzione notevole]] su [[variabile-aleatoria-discreta|variabile aleatoria discreta]] $X$ che _assegna la stessa probabilità a ciascun valore di un insieme finito di valori possibili_.
> In tal caso, si dice che $X$ ha la legge uniforme sul supporto, e si indica
> $$X \sim Unif(\{x_{1}, \cdots, x_{n}\})$$

Formalmente, preso $S_{X} = \{x_{1}, \cdots, x_{n}\}$ il supporto di $X$, la [[densita-discreta|densita' discreta]] $p_{X}$ sara' del tipo

| $X$     | $x_{1}$       | $x_{2}$       | $\cdots$ | $x_{n}$       |
| ------- | ------------- | ------------- | -------- | ------------- |
| $p_{X}$ | $\frac{1}{n}$ | $\frac{1}{n}$ | $\cdots$ | $\frac{1}{n}$ |

o in altri termini
$$p_{X}(x_{i}) = \frac{1}{n} \ \ \ \forall x_{i} \in S_{X}$$

## Proprieta'
### Valore atteso
Il [[valore-atteso|valore atteso]] di una variabile aleatoria discreta con distribuzione uniforme discreta e' dato da, come possiamo immaginare, la media aritmetica
$$\mathbb{E}[X] = \frac{x_{1} + \cdots + x_{n}}{n}$$

### Varianza
La [[varianza|varianza]] di una variabile aleatoria discreta con distribuzione uniforme discreta e' data da
$$Var(X) = \frac{1}{n} \sum\limits_{i=1}^{n} (x_{i} - \mathbb{E}[X])^{2}$$

## Referenze