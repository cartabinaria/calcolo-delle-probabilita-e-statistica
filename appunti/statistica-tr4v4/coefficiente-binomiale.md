---
tags:
  - category/note
  - status/finished
  - topic/analisi-I
  - topic/calcolo-delle-probabilità-e-statistica
date: 24-09-2023 18:44:32
links:
  - "[[lecture-22092023133316|Lecture 22092023133316]]"
  - "[[lecture-14032025131849|Lecture 14032025131849]]"
---
# Coefficiente binomiale
---
## Introduzione
> Si scrive come
> $$\binom{n}{k} = \frac{n!}{k!(n-k)!} \ \ \ \forall n,k \in \mathbb{N} \land k \leq n$$

## Casi particolari
Valgono i seguenti casi particolari
$$\binom{n}{0} = 1 = \binom{n}{n}$$
$$\binom{n}{1} = n = \binom{n}{n-1}$$

## Proprieta'
Valgono le seguenti proprieta':
$$\binom{n}{k} = \binom{n}{n-k}$$
$$\binom{n}{k-1} + \binom{n}{k} = \binom{n+1}{k}$$
$$\binom{n}{k} = \binom{n-1}{k-1} + \binom{n-1}{k}$$
anche detta **formula di Stifel**.

## Referenze
- [[binomio-di-newton|Binomio di Newton]]