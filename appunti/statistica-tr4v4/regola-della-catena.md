---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 04-03-2025 10:42:33
links:
  - "[[lecture-25022025133832|Lecture 25022025133832]]"
---
# Regola della catena
---
## Introduzione
> Siano $A, B$ due [[evento|eventi]] con $\mathbb{P}(B) > 0$, allora vale la **regola della catena**
> $$\mathbb{P}(A \cap B) = \mathbb{P}(A | B) \mathbb{P}(B)$$
> dove $\mathbb{P}(A|B)$ e' la [[probabilita-condizionata|probabilita' condizionata]]. La vera regola viene considerata la sua generalizzazione a $n$ intersezioni, ovvero considerata la [[successione-numerica|successione]] di insiemi $(A_{i})_{i=1, \cdots, n}$ con $\mathbb{P}(A_{1} \cap \cdots \cap A_{n-1}) > 0$, allora vale che
> $$\mathbb{P}(A_{1} \cap \cdots \cap A_{n}) = \mathbb{P}(A_{n} | A_{1} \cap \cdots \cap A_{n-1}) \cdot \mathbb{P}(A_{n-1}|A_{1} \cap \cdots \cap A_{n-2}) \cdot \ldots \cdot \mathbb{P}(A_{2}|A_{1}) \cdot \mathbb{P}(A_{1})$$

## Dimostrazione
Uso _l'associativita' e la commutativita' dell'intersezione_ per riscrivere $\mathbb{P}(A_{1} \cap \cdots \cap A_{n})$ come
$$\mathbb{P}(A_{n} \cap (A_{1} \cap \cdots \cap A_{n-1}))$$

A questo punto, sapendo per ipotesi che $\mathbb{P}(A_{1} \cap \cdots \cap A_{n-1}) > 0$, uso la regola della catena per due eventi considerando $A = A_{n}$ e $B = A_{1} \cap \cdots \cap A_{n-1}$, e ottengo
$$\mathbb{P}(A_{n} | A_{1} \cap \cdots \cap A_{n-1}) \cdot \mathbb{P}(A_{1} \cap \cdots \cap A_{n-1})$$

Posso reiterare questo procedimento in quanto $\mathbb{P}(A_{1} \cap \cdots \cap A_{n-1}) > \mathbb{P}(A_{1} \cap \cdots \cap A_{n-2}) > 0$.

**Qed**.

## Referenze