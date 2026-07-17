---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 14-04-2025 20:53:11
links:
  - "[[lecture-01042025132135|Lecture 01042025132135]]"
---
# Distribuzione binomiale
---
## Introduzione
> La **distribuzione binomiale** e' una [[distribuzioni-notevoli-di-variabili-aleatorie-discrete|distribuzione notevole]] su [[variabile-aleatoria-discreta|variabile aleatoria discreta]] $X$ che estende la [[distribuzione-di-bernoulli|distribuzione di Bernoulli]] su $n$ [[sottoesperimento-aleatorio|sottoesperimenti]].
> In tal caso, si dice che $X$ ha la legge binomiale, e si indica
> $$X \sim Bin(n, p)$$

### Definizione
In particolare si assume di avere $n$ prove [[indipendenza-di-variabili-aleatorie|indipendenti]] di Bernoulli, ossia $n$ sottoesperimenti aleatori che hanno come esito 0 e 1 con una certa probabilità $p$ e $1 - p$. Definiamo su ogni lancio $i = 1, \cdots, n$ la variabile aleatoria discreta $Y_{i}$ come
$$Y_{i} = \mathbb{1}_{E_{i}} \sim B(p)$$
con $E_{i} =$ "successo all'i-esima prova di Bernoulli" e ovviamente $p = \mathbb{P}(E_{i})$.

Allora, definisco la variabile aleatoria discreta $X$ come
$$X := \sum\limits_{i=1}^{n} Y_{i}$$
e si ha che $X$ ha la legge binomiale, ossia
$$X \sim Bin(n, p)$$

### Supporto e densità
Avremo come supporto di $X$ l'insieme $S_{X} = \{0, \cdots, n\}$ finito. Ma come definisco la [[densita-discreta|densita' discreta]]? In altre parole, devo capire come _calcolare la probabilità di ottenere $x_{i}$ successi su $n$ prove sapendo che la probabilità di successo è $p$ in ogni prova_.

Si definisce la densita' discreta che risponde a questa domanda come
$$p_{X}(x_{i}) = \binom{n}{x_{i}} p^{x_{i}} (1 - p)^{n - x_{i}}$$

dove $\binom{n}{x_{i}}$ e' il [[coefficiente-binomiale|coefficiente binomiale]].

## Proprieta'
### Valore atteso
Il [[valore-atteso|valore atteso]] di una variabile aleatoria discreta con distribuzione binomiale e' dato da
$$\mathbb{E}[X] = np$$

### Varianza
La [[varianza|varianza]] di una variabile aleatoria discreta con distribuzione binomiale e' data da
$$Var(X) = np(1 - p)$$

## Referenze