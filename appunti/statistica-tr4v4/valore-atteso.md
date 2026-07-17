---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 08-04-2025 12:07:36
links:
  - "[[lecture-21032025132255|Lecture 21032025132255]]"
  - "[[lecture-01042025132135|Lecture 01042025132135]]"
  - "[[lecture-11042025131834|Lecture 11042025131834]]"
---
# Valore atteso
---
## Variabili aleatorie discrete
> Sia $X: \Omega \to \mathbb{R}$ una [[variabile-aleatoria-discreta|variabile aleatoria discreta]], il **valore atteso** (o **media**, **speranza**) di $X$ e' definito come
> $$\mathbb{E}[X] := \sum\limits_{x \in S_{X}} x \cdot p_{X}(x)$$
> ossia come la sommatoria di tutti i valori assunti dalla variabile aleatoria $X$ (il suo _supporto_ $S_{X}$) moltiplicati per la loro probabilita' di accadimento (la [[densita-discreta|densita' discreta]] $p_{X}$).

<u>Nota bene</u>: il valore atteso **non necessariamente è uno dei valori del supporto**!

### Esempi
#### Probabilita' uniforme
Se assumiamo che $X$ prenda valori [[probabilita-uniforme|equiprobabili]], allora si deve avere che $S_{X} = \{x_{1}, \cdots, x_{n}\}$ e $p_{X}(x_{k}) = \frac{1}{n}$. Il valore atteso diventa la semplice media aritmetica
$$\mathbb{E}[X] = \sum\limits_{k=1}^{n} p_{X}(x_{k})x_{k} = \frac{1}{n} \sum\limits_{k=1}^{n}x_{k}$$

#### Indicatrice
Se invece $X$ e' una [[variabile-aleatoria-indicatrice|variabile aleatoria indicatrice]] su un [[evento|evento]] fissato $A$, ossia $X = \mathbb{1}_{A}$, allora $S_{X} = \{0, 1\}$ e $p_{X}(x) = \begin{cases} \mathbb{P}(A) & x = 1 \\ 1 - \mathbb{P}(A) & x = 0 \end{cases}$. Di conseguenza
$$\mathbb{E}[X] = 1 \mathbb{P}(A) + 0 (1 - \mathbb{P}(A)) = \mathbb{P}(A)$$

### Teoremi
#### Funzione
> Sia $X$ v.a. discreta e $h: \mathbb{R} \to \mathbb{R}$ allora
> $$\mathbb{E}[h(X)] = \sum\limits_{i} h(x_{i}) p_{X}(x_{i})$$

#### Linearita'
> Siano $X, Y$ v.a. discrete, allora vale
> $$\mathbb{E}[\alpha X + \beta Y] = \alpha \mathbb{E}[X] + \beta \mathbb{E}[Y]$$

##### Dimostrazione
Facciamo la dimostrazione assumendo $Y = g(X)$ (caso semplificato).
Si osserva che $S_{Y} = g(S_{X})$. Ora, per definizione si ha che
$$\mathbb{E}[\alpha X + \beta g(X)] = \sum\limits_{x \in S_{X}} (\alpha x + \beta g(x)) \cdot p_{X}(x) = \alpha \sum\limits_{x \in S_{X}} x \cdot p_{X}(x) + \beta \sum\limits_{x \in S_{X}} g(x) \cdot p_{X}(x) = \alpha \mathbb{E}[X] + \beta \mathbb{E}[Y]$$

## Variabili aleatorie continue
> Sia $X$ una [[variabile-aleatoria-continua|variabile aleatoria continua]], allora si definisce **valore atteso** di $X$ il valore
> $$\mathbb{E}[X] := \int_{\mathbb{R}} x f_{X}(x) \ dx$$
> dove $f_{X}$ e' la [[densita-continua|densita' continua]] di $X$.

### Teoremi
#### Funzione
> Sia $X$ v.a. continua e $h: \mathbb{R} \to \mathbb{R}$ allora
> $$\mathbb{E}[h(X)] = \int_{\mathbb{R}} h(x) f_{X}(x) \ dx$$

## Referenze