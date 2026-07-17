---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 19-05-2025 19:55:46
links:
  - "[[lecture-23042025091502|Lecture 23042025091502]]"
  - "[[lecture-29042025132447|Lecture 29042025132447]]"
---
# Vettore aleatorio discreto
---
## Introduzione
> Sia $(\Omega, \mathbb{P})$ [[spazio-di-probabilita|spazio di probabilita']] allora $(X, Y)$ e' un **[[vettore-aleatorio|vettore aleatorio]] discreto** (bidimensionale) se _$X$ e $Y$ sono [[variabile-aleatoria-discreta|variabili aleatorie discrete]]_.

## Indici
I vettori aleatori hanno indici simili ma comunque differenti dalle singole variabili aleatorie. Considerato il caso bidimensionale in particolare si avra':
- _vettore delle medie_ $\in \mathbb{R}^{2}$, quindi $(\mathbb{E}[X], \mathbb{E}[Y])$;
- _[[matrice-delle-covarianze|matrice delle covarianze]]_ $\in \mathbb{R}^{2 \times 2}$.

## Teoremi
### Valore atteso e varianza
> Sia $h: \mathbb{R}^{2} \to \mathbb{R}$ e $(X, Y)$ vettore aleatorio discreto, allora $h(X, Y)$ e' una [[variabile-aleatoria|variabile aleatoria]] e
> - $\mathbb{E}[h(X, Y)] = \sum\limits_{i,j} h(x_{i}, y_{j}) p_{(X, Y)}(x_{i}, y_{j})$ --> [[valore-atteso|valore atteso]];
> - $Var(h(X, Y)) = \mathbb{E}[h^{2}(X, Y)] - (\mathbb{E}[h(X, Y)])^{2}$ --> [[varianza|varianza]].

### Linearita' del valore atteso
> Sia $(X, Y)$ vettore aleatorio discreto e $a, b \in \mathbb{R}$, allora
> $$\mathbb{E}[aX + bY] = a\mathbb{E}[X] + b\mathbb{E}[Y]$$

### Indipendenza
> Sia $(X, Y)$ vettore aleatorio discreto e $X, Y$ [[indipendenza-di-variabili-aleatorie|indipendenti]], allora
> $$\mathbb{E}[XY] = \mathbb{E}[X]\mathbb{E}[Y]$$

## Referenze
- [[densita-congiunta-discreta|Densita' congiunta discreta]]