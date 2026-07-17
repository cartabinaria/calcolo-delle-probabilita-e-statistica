---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 24-02-2025 19:03:52
links:
  - "[[lecture-21022025131008|Lecture 21022025131008]]"
---
# Probabilita' dell'unione non disgiunta di eventi
---
## Introduzione
> Siano $A, B$ [[evento|eventi]], allora si ha che
> $$\mathbb{P}(A \cup B) = \mathbb{P}(A) + \mathbb{P}(B) - \mathbb{P}(A \cap B)$$

<u>Nota bene</u>: _la formula per 3 insiemi e' decisamente piu' complessa_; in generale la complessita' della formula e' esponenziale rispetto al numero di insiemi coinvolti.
$$\mathbb{P}(A ∪ B ∪ C) = \mathbb{P}(A) + \mathbb{P}(B) + \mathbb{P}(C) − \mathbb{P}(A ∩ B) − \mathbb{P}(A ∩ C) − \mathbb{P}(B ∩ C) + \mathbb{P}(A ∩ B ∩ C).$$

## Dimostrazione
Si considera la proposizione seguente come valida (ovvia):
$$A \cup B = (A \setminus B) \cup (B \setminus A) \cup (B \cap A)$$
Per cui
$$\mathbb{P}(A \cup B) = \mathbb{P}(A \setminus B) + \mathbb{P}(B \setminus A) + \mathbb{P}(A \cap B)$$

A questo punto, considero le due proposizioni:
- $(A \setminus B) \cup (A \cap B) = A$
- $(B \setminus A) \cup (A \cap B) = B$

e sommo e sottraggo alla formula precedente 2 volte il valore $\mathbb{P}(A \cap B)$, cosi' da poter riscrivere le probabilita' senza sottrazioni di insiemi:
$$\mathbb{P}(A \cup B) = \mathbb{P}(A \setminus B) + \mathbb{P}(A \cap B) + \mathbb{P}(B \setminus A) + \mathbb{P}(A \cap B) + \mathbb{P}(A \cap B) - 2\mathbb{P}(A \cap B)$$
che porta proprio a
$$\mathbb{P}(A \cup B) = \mathbb{P}(A) + \mathbb{P}(B) - \mathbb{P}(A \cap B)$$

**Qed.**

## Referenze