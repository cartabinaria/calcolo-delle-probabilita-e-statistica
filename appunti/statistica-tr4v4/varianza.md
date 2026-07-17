---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 14-04-2025 19:55:15
links:
  - "[[lecture-21032025132255|Lecture 21032025132255]]"
  - "[[lecture-11042025131834|Lecture 11042025131834]]"
---
# Varianza
---
## Variabili aleatorie discrete
> Sia $X$ una [[variabile-aleatoria-discreta|variabile aleatoria discreta]] con supporto $S_{X}$, allora si definisce **varianza** di $X$ il valore
> $$Var(X) := \mathbb{E}[(X - \mathbb{E}[X])^{2}]$$
> ossia una _media degli errori quadrati rispetto al [[valore-atteso|valore atteso]]_.

<u>Osservazione</u>: per la definizione di valore atteso, la varianza di $X$ puo' anche essere vista come
$$Var(X) = \sum\limits_{x \in S_{X}} (x - \mathbb{E}[X])^{2} \cdot p_{X}(x)$$

### Teoremi
#### Calcolo
> $$Var(X) = \mathbb{E}[X^{2}] - (\mathbb{E}[X])^{2} = \sum\limits_{x \in S_{X}}x^{2}p_{X}(x) - \left(\sum\limits_{x \in S_{X}} x p_{X}(x)\right)^{2}$$

##### Dimostrazione
Sfruttiamo la linearita' del valore atteso:
$$Var(X) = \mathbb{E}[(X - \mathbb{E}[X])^{2}] = \mathbb{E}[X^{2} - 2\mathbb{E}[X]X + (\mathbb{E}[X])^{2}] = \mathbb{E}[X^{2}] - 2\mathbb{E}[\mathbb{E}[X]X] + \mathbb{E}[(\mathbb{E}[X])^{2}]$$

e usando ancora la linearita' e il fatto che $\mathbb{E}[(\mathbb{E}[X])^{2}] = (\mathbb{E}[X])^{2}$ diventa
$$\mathbb{E}[X^{2}] - 2\mathbb{E}[\mathbb{E}[X]X] + \mathbb{E}[(\mathbb{E}[X])^{2}] = \mathbb{E}[X^{2}] - 2\mathbb{E}[X]\mathbb{E}[X] + (\mathbb{E}[X])^{2} = \mathbb{E}[X^{2}] - (\mathbb{E}[X])^{2}$$

**Qed**.

#### Proprieta'
> Sia $X$ variabile aleatoria discreta, allora valgono:
> 1. $Var(X) \geq 0$;
> 2. $Var(X) = 0 \iff X \text{ costante}$;
> 3. $Var(aX + b) = a^{2} Var(X)$

### Osservazioni
Se _togliessi il quadrato dalla formula otterrei una varianza molto simile al valore atteso_: questo perche' i valori negativi, nei casi di simmetria, andrebbero ad annullare quelli positivi.

Se invece usassi il [[valore-assoluto|valore assoluto]], idealmente otterrei la stessa cosa, ma per ragioni di [[funzioni-derivabili|derivabilita']] si preferisce usare il quadrato. Come conseguenza, pero', si ha che il valore della _varianza dev'essere messa sotto radice quadrata per ottenere quella che si chiama [[deviazione-standard|deviazione standard]]_.

## Variabili aleatorie continue
> Sia $X$ una [[variabile-aleatoria-continua|variabile aleatoria continua]] con [[densita-continua|densita' continua]] $f_{X}$, allora si definisce **varianza** di $X$ il valore
> $$Var(X) := \mathbb{E}[(X - \mathbb{E}[X])^{2}] = \int_{\mathbb{R}} (x - \mathbb{E}[X])^{2} f_{X}(x) \ dx$$

## Referenze