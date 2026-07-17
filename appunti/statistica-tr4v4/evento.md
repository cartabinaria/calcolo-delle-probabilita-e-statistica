---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 20-02-2025 11:28:03
links:
  - "[[lecture-18022025132744|Lecture 18022025132744]]"
  - "[[lecture-21022025131008|Lecture 21022025131008]]"
---
# Evento
---
## Introduzione
> Un **evento** e' un'affermazione che riguarda l'[[esito|esito]] di un [[esperimento-aleatorio|esperimento aleatorio]], di cui posso dire con certezza se e' vero o falso solo una volta noto il risultato. Insiemisticamente, parlando, se $\Omega$ e' lo [[spazio-campionario|spazio campionario]], allora un evento e' il sottoinsieme di $\Omega$ degli [[esiti-favorevoli|esiti favorevoli]].

Per esempio: nel caso del lancio di un dado, l'evento $A$ puo' essere _"esce un numero pari"_, e se quindi $\Omega = \{1, 2, 3, 4, 5, 6\}$ allora $A \subseteq \Omega = \{2, 4, 6\}$.

## Notazione
Alcuni eventi prendono un certo nome a seconda delle loro caratteristiche:
- $\Omega$ è **evento certo** --> l'intero spazio campionario rappresenta un evento che per forza deve essere vero ad ogni esperimento
- $\varnothing$ è **evento impossibile** --> l'esperimento dovrebbe risultare in nessuno degli esiti dello spazio campionario, per cui è sempre falso
- $A = \{w\}$ è **evento elementare**
- $A : \mathbb{P}(A) = 1$ e' **evento quasi certo**
- $A : \mathbb{P}(A) = 0$ e' **evento quasi impossibile**

<u>Nota bene</u>: la differenza tra gli eventi "quasi" con quelli "non quasi" sta nella definizione; _gli eventi certi e impossibili sono espressi in termini di insiemi, mentre quelli quasi certi e quasi impossibili in termini della funzione di probabilità $\mathbb{P}$_ (che puo' variare).

### Esempi
Per esempio nel caso del lancio di un dado:
- $A =$ "esce un numero naturale compreso tra 1 e 6"
- $B =$ "esce un numero > 6"
- $C =$ "esce il numero 2"
- se $\Omega = \{1, 2, 3, 4, 5, 6\}$ allora
	- $A = \Omega$
	- $B = \varnothing$
	- $C = \{2\}$
- se invece $\Omega = \mathbb{R}$ allora
	- $A = \{1, 2, 3, 4, 5, 6\} \neq \Omega$
	- $B = (6, +\infty)$
	- $C = \{2\}$

Sempre considerando il lancio di un dado e la funzione di probabilita' discreta $\mathbb{P}(A) = \sum\limits_{i=1}^{6} \frac{1}{6} \delta_{i}(A)$, allora
- $A = \{1, 2, 3, 4, 5, 6\} \implies \mathbb{P}(A) = 1$, quindi $A$ e' _quasi certo_
- $A = (6, +\infty) \implies \mathbb{P}(A) = 0$, quindi $A$ e' _quasi impossibile_
- $A = \{1, 2, 3, 4, 5, 6, 8, 10\} \implies \mathbb{P}(A) = 1$, perche' nella sommatoria i [[delta-di-dirac|delta di Dirac]] per $8$ e $10$ restituiscono $0$ (non vengono considerati)

Di conseguenza **gli eventi quasi certi e quasi impossibili sono tantissimi**, spesso molti di piu' degli altri.

## Referenze
- [[esito|Esito]]
- [[esiti-favorevoli|Esiti favorevoli]]