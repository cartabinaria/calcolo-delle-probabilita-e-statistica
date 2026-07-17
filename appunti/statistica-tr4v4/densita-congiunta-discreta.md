---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 19-05-2025 20:01:04
links:
  - "[[lecture-23042025091502|Lecture 23042025091502]]"
---
# Densita' congiunta discreta
---
## Introduzione
> Sia $(X, Y)$ un [[vettore-aleatorio-discreto|vettore aleatorio discreto]], allora la funzione $p_{(X, Y)}: \mathbb{R}^{2} \to [0, 1]$ si dice **densita' congiunta discreta** del vettore $(X, Y)$, e si definisce come
> $$p_{(X, Y)}(x, y) := \mathbb{P}(X = x, Y = y)$$

<u>Nota bene</u>: questa identifica univocamente la [[distribuzione-di-una-variabile-aleatoria|legge]] del vettore!

## Supporto
Conoscendo le [[leggi-marginali|leggi marginali]] conosco anche le rispettive [[densita-discreta|densita' discrete]] di $X$ e $Y$, con i supporti $S_{X}, S_{Y}$. Il [[prodotto-cartesiano|prodotto cartesiano]] $S_{X} \times S_{Y}$ sara' una sovrastima del supporto del vettore aleatorio! Ovvero $S_{(X, Y)} \subseteq S_{X} \times S_{Y}$. In particolare
$$S_{(X, Y)} = \{(x, y) \in \mathbb{R}^{2} | p_{(X, Y)}(x, y) > 0\}$$

Di solito lavoreremo con il prodotto cartesiano, e poi ci accorgeremo che per certi valori si avra' $p_{(X, Y)}(x_{i}, y_{j}) = 0$, e quindi $(x_{i}, y_{j})$ dovra' essere escluso da $S_{(X, Y)}$.

## Teoremi
### Densita' congiunta
> Sia $(\Omega, \mathbb{P})$ [[spazio-di-probabilita|spazio di probabilita']] e $(X, Y)$ vettore aleatorio discreto con $p_{X}, S_{X}$ densita' discreta marginale e supporto di $X$, $p_{Y}, S_{Y}$ densita' discreta marginale e supporto di $Y$ e $p_{(X, Y)}$ densita' congiunta discreta di $(X, Y)$. Allora:
> 1. $p_{(X, Y)}(x_{i}, y_{j}) = 0 \ \ \ \forall(x_{i}, y_{j}) \notin S_{X} \times S_{Y}$
> 2. $\sum\limits_{(i, j)} p_{(X, Y)}(x_{i}, y_{j}) = 1$, dove $(i, j) : (x_{i}, y_{j}) \in S_{X} \times S_{Y}$
> 3. $\mathbb{P}_{(X, Y)}(B) = \mathbb{P}((X, Y) \in B) = \sum\limits_{(i, j)} p_{(X, Y)}(x_{i}, y_{j})$, sempre dove $i, j : (x_{i}, y_{j}) \in B$

### Indipendenza
> Sia $(X, Y)$ vettore aleatorio discreto con densita' congiunta $p_{(X, Y)}$, allora $X$ e' [[indipendenza-di-variabili-aleatorie|indipendente]] da $Y$ $\iff$
> $$p_{(X, Y)}(x, y) = p_{X}(x) p_{Y}(y) \ \ \ \forall (x, y) \in S_{X} \times S_{Y}$$

#### Dimostrazione
$\implies$: se $X \perp\!\!\!\perp Y$ allora $\mathbb{P}(X \in B_{1}, Y \in B_{2}) = \mathbb{P}(X \in B_{1}) \mathbb{P}(Y \in B_{2}) \ \ \ \forall B_{1}, B_{2} \subseteq \mathbb{R}$. Basta scegliere $B_{1} = \{x\}$ e $B_{2} = \{y\}$.

$\impliedby$: assumo $p_{(X, Y)}(x, y) = p_{X}(x) p_{Y}(y) \ \ \ \forall (x, y) \in S_{X} \times S_{Y}$. Dimostro l'indipendenza mostrando che
$$\mathbb{P}(X \in B_{1}, Y \in B_{2}) = \sum\limits_{x \in B_{1}, y \in B_{2}} p_{(X, Y)}(x, y) = \sum\limits_{x \in B_{1}, y \in B_{2}} p_{X}(x) p_{Y}(y) = \sum\limits_{x \in B_{1}}p_{X}(x) \sum\limits_{y \in B_{2}}p_{Y}(y)$$
il che ovviamente e' uguale a $\mathbb{P}(X \in B_{1}) \mathbb{P}(Y \in B_{2})$.

## Rapporto con densita' marginali
Se conosco la densita' congiunta posso ricavare le densita' marginali: uso la [[formula-delle-probabilita-totali|formula delle probabilita' totali]]! Infatti vale che
$$p_{X}(x) = \sum\limits_{j : y_{j} \in S_{Y}} p_{(X, Y)}(x, y_{j}) \ \ \ \forall x \in S_{X}$$
e rispettivamente per $p_{Y}$.

Infatti $p_{(X, Y)}(x, y_{j}) = \mathbb{P}(\{X = x\} \cap \{Y = y_{j}\})$ e conoscendo cio' $\forall y_{j} \in S_{Y}$, questo costituisce una [[partizione-dello-spazio-campionario|partizione]] di $\Omega$ ($\{Y = y_{i}\} \cap \{Y = y_{j}\} = \varnothing \ \ i \neq j$ e $\bigcup_{y_{j} \in S_{y}} \{Y = y_{j}\} = \Omega$).

## Tabella
![[tabella-densita-congiunta.png]]

## Referenze