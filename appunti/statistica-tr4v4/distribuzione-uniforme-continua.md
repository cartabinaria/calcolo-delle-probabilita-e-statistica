---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 28-04-2025 19:48:48
links:
  - "[[lecture-11042025131834|Lecture 11042025131834]]"
---
# Distribuzione uniforme continua
---
## Introduzione
> La **distribuzione uniforme continua** e' una [[distribuzioni-notevoli-di-variabili-aleatorie-continue|distribuzione notevole]] su [[variabile-aleatoria-continua|variabile aleatoria continua]] $X$ che _assegna la stessa probabilità a ciascun valore di un intervallo continuo_. In particolare, se $X$ e' uniforme sull'intervallo $[a, b]$, si indica
> $$X \sim Unif(a, b)$$

Formalmente, preso come supporto $S_{X} = (a, b)$ con $a < b$, la [[densita-continua|densita' continua]] $f_{X}$ sara' definita come
$$f_{X}(x) = \frac{1}{b-a} \mathbb{1}_{(a, b)}(x)$$
usando la [[variabile-aleatoria-indicatrice|variabile aleatoria indicatrice]].

<u>Nota bene</u>: l'inclusione degli estremi non cambia la probabilita'.

La [[funzione-di-ripartizione|funzione di ripartizione]] $F_{X}$, di conseguenza sara' definita come:
$$F_{X}(x) = \begin{cases} 0 & x < a \\ 1 & x \geq b \\ \int_{a}^{x} \frac{1}{b-a} \, dy = \frac{x-a}{b-a} & x \in [a, b) \end{cases}$$

## Proprieta'
### Valore atteso
Il [[valore-atteso|valore atteso]] di una variabile aleatoria continua con distribuzione uniforme continua e' dato da
$$\mathbb{E}[X] = \frac{a + b}{2}$$

### Varianza
La [[varianza|varianza]] di una variabile aleatoria continua con distribuzione uniforme continua e' data da
$$Var(X) = \frac{(a - b)^{2}}{12}$$

## Referenze