---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 30-03-2025 13:54:31
links:
  - "[[lecture-07032025131750|Lecture 07032025131750]]"
---
# Disposizione con ripetizione
---
## Introduzione
> Dato un insieme $E$ con $|E| = n$, indichiamo con **disposizioni con ripetizione** l'insieme delle _sequenze ordinate di $k \in \mathbb{N}$ elementi di $E$ non necessariamente distinti_ con
> $$DR_{n,k} = \{(x_{1}, \cdots, x_{k}) : x_{i} \in E\} = E \times \cdots \times E \ \ (k \text{ volte})$$
> tale che
> $$|DR_{n, k}| = n^{k}$$

## Esempi
### Urna
Prendiamo un'urna con $n$ palline numerate $E = \{1, \cdots, n\}$, e vogliamo estrarre $k$ palline con reimmisione. Allora lo [[spazio-campionario|spazio campionario]] $\Omega$ sara' proprio
$$\Omega = E \times \cdots \times E \ \ (k \text{ volte}) = DR_{n,k}$$

Ognuna di queste sequenze ha uguale probabilita', per cui $\mathbb{P}$ e' la [[probabilita-uniforme|probabilita' uniforme]]. Di conseguenza
$$\mathbb{P}(\{w_{i}\}) = n^{-k} \ \ \ \forall w_{i} \in \Omega$$

## Referenze