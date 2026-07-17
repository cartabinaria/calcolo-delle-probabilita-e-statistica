---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 30-03-2025 18:56:58
links:
  - "[[lecture-14032025131849|Lecture 14032025131849]]"
---
# Probabilita' binomiale
---
## Introduzione
Consideriamo l'[[esperimento-aleatorio|esperimento aleatorio]] di un urna con $b$ palline bianche e $r$ rosse, da cui si effettuano $n$ estrazioni con reimmissione. Vogliamo calcolare la [[probabilita|probabilita']] dell'[[evento|evento]]
$$A_{k} = \text{si estraggono k palline bianche}$$

Come [[spazio-campionario|spazio campionario]] fissiamo
$$\Omega = DR_{b+r, n}$$
ovvero le [[disposizione-con-ripetizione|disposizioni con ripetizione]], con $\mathbb{P}$ [[probabilita-uniforme|uniforme]]. Quindi avremo
$$\mathbb{P}(\{w\}) = \frac{1}{(b+r)^{n}}$$

Quindi, per trovare $\mathbb{P}(A_{k})$ dobbiamo trovare $|A_{k}|$, allora usiamo il [[principio-delle-scelte-successive|principio delle scelte successive]]:
1. scelta della sequenza di $k$ palline bianche estratte: $|DR_{b,k}|$
2. scelta della sequenza di $n-k$ palline rosse estratte: $|DR_{r,n-k}|$
3. scelta delle $k$ estrazioni in cui escono palline bianche: $|C_{n,k}|$

Otteniamo che
$$\mathbb{P}(A_{k}) = \frac{|A_{k}|}{|\Omega|} = \frac{|DR_{b,k}| \cdot |DR_{r,n-k}| \cdot |C_{n,k}|}{|DR_{b+r,n}|} = \binom{n}{k} p^{k} (1-p)^{n-k}$$
dove $p = \frac{b}{b+r}$.

Se facciamo variare $k$ tra $0$ e $n$ in $\hat{\Omega} = \{0, \cdots, n\}$ e calcoliamo $\mathbb{P}(\{k\})$ otteniamo proprio che
$$\mathbb{P}(\{k\}) = \binom{n}{k} p^{k} (1-p)^{n-k}$$

e $\mathbb{P}$ si chiama **probabilita' binomiale**.

## Referenze