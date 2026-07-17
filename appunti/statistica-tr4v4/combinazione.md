---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 28-03-2025 13:27:48
links:
  - "[[lecture-07032025131750|Lecture 07032025131750]]"
  - "[[lecture-14032025131849|Lecture 14032025131849]]"
---
# Combinazione
---
## Introduzione
> Dato un insieme $E$ con $|E| = n$, le **combinazioni** sono la classe dei sottoinsiemi di $E$ con $k$ elementi, ossia:
> $$C_{n,k} = \{A \subset E : |A| = k\}$$
> tale che
> $$|C_{n,k}| = \binom{n}{k}$$
> Nella forma piu' "combinatoria" indicano l'insieme delle sequenze non ordinate senza ripetizione: per questo si usa una definizione insiemistica[^1]!

<u>Nota bene</u>: le combinazioni fondamentalmente fanno collassare tutte quelle sequenze delle [[disposizione-semplice|disposizioni semplici]] che contengono gli stessi elementi (non ripetuti) in ordine diverso in un'unico elemento --> $|C_{n,k}| < |D_{n,k}|$.

## Dimostrazione
Vogliamo dimostrare che le combinazioni si calcolano usando il coefficiente binomiale. In altre parole, vogliamo dimostrare proprio che
$$|C_{n,k}| = \frac{n!}{k!(n-k!)}$$

Notiamo che il coefficiente binomiale si puo' riscrivere in termini di [[disposizione-semplice|disposizioni semplici]] e [[permutazione|permutazioni]]:
$$|C_{n,k}| = \frac{|D_{n,k}|}{|P_{k}|}$$

Per cui ci riduciamo a dimostrare
$$|D_{n,k}| = |C_{n,k}| \cdot |P_{k}|$$

ossia che _il numero di sequenze ordinate senza ripetizioni di lunghezza $k$ tra $n$ elementi e' il numero di sequenze non ordinate senza ripetizioni di lunghezza $k$ tra $n$ elementi per il numero di possibili ordinamenti dei $k$ elementi_. Ma vale per il [[principio-delle-scelte-successive|principio delle scelte successive]]:
1. scelta dei $k$ elementi selezionati --> $|C_{n,k}|$;
2. scelta dell'ordinamento dei $k$ elementi selezionati --> $|P_{k}|$.

## Esempi
### Semi
In quanti modi si possono scegliere i semi di una coppia in un mazzo francese, composto quindi da 4 semi? Basta considerare $E$ l'insieme dei semi
$$E = \{c, q, p, f\}$$
e considerare tutti i sottoinsiemi di $E$ con [[cardinalita|cardinalita']] pari a 2, ovvero le combinazioni
$$C_{4,2} = \binom{4}{2} = 6$$

## Referenze
- [[coefficiente-binomiale|Coefficiente binomiale]]

[^1]: gli insiemi non hanno ordine
