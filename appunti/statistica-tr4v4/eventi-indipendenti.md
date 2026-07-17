---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 04-03-2025 11:32:22
links:
  - "[[lecture-28022025132238|Lecture 28022025132238]]"
  - "[[lecture-04032025133148|Lecture 04032025133148]]"
---
# Eventi indipendenti
---
## Introduzione
> Due [[evento|eventi]] $A, B$ si dicono **indipendenti** se
> $$\mathbb{P}(A \cap B) = \mathbb{P}(A) \mathbb{P}(B)$$
> ossia se il verificarsi di $B$ non altera la probabilita' di $A$, infatti $\mathbb{P}(A|B) = \mathbb{P}(A), \ \ \ \mathbb{P}(B) > 0$.
> In tal caso si indica l'indipendenza con
> $$A \perp\!\!\!\perp B$$
> <u>Nota bene</u>: si tratta di una _proprieta' simmetrica_, ossia se $A \perp\!\!\!\perp B$ allora $B \perp\!\!\!\perp A$.

<u>Attenzione</u>: _indipendenza $\neq$ disgiunzione_. Infatti se $\mathbb{P}(A \cap B) = \mathbb{P}(A) \mathbb{P}(B)$ e $A \cap B = \varnothing$, allora si deve avere $\mathbb{P}(A) = 0$ o $\mathbb{P}(B) = 0$.

## Teoremi
### Legame con probabilità condizionata
Il legame con la [[probabilita-condizionata|probabilita' condizionata]] si evince dal seguente teorema:
> Se $\mathbb{P}(B) > 0$ allora $$A \perp\!\!\!\perp B \iff \mathbb{P}(A|B) = \mathbb{P}(A)$$
> Se $\mathbb{P}(A) > 0$ allora $$A \perp\!\!\!\perp B \iff \mathbb{P}(B|A) = \mathbb{P}(B)$$In altri termini, se $\mathbb{P}(A) > 0$ e $\mathbb{P}(B) > 0$, le tre uguaglianze sono equivalenti:
> - $\mathbb{P}(A \cap B) = \mathbb{P}(A) \mathbb{P}(B)$
> - $\mathbb{P}(A|B) = \mathbb{P}(A)$
> - $\mathbb{P}(B|A) = \mathbb{P}(B)$

La dimostrazione segue dalla definizione di probabilità condizionata.

### Indipendenza complementare
> Vale che
> $$A \perp\!\!\!\perp B \implies A^{C}  \perp\!\!\!\perp B \land A \perp\!\!\!\perp B^{C} \land A^{C}  \perp\!\!\!\perp B^{C}$$

#### Dimostrazione
Se $A \perp\!\!\!\perp B$ allora $\mathbb{P}(A \cap B) = \mathbb{P}(A) \mathbb{P}(B)$. Dimostro solo $A^{C}  \perp\!\!\!\perp B$ (le altre sono equivalenti).

Devo dimostrare $A^{C}  \perp\!\!\!\perp B$, ossia $\mathbb{P}(A^{C} \cap B) = \mathbb{P}(A^{C}) \mathbb{P}(B)$. So che $\mathbb{P}(A^{C}) = 1 - \mathbb{P}(A)$, per cui $\mathbb{P}(A^{C}) \mathbb{P}(B) = \mathbb{P}(B) - \mathbb{P}(A) \mathbb{P}(B)$. Dall'ipotesi, so che $\mathbb{P}(A)\mathbb{P}(B) = \mathbb{P}(A \cap B)$, per cui devo dimostrare $\mathbb{P}(A^{C} \cap B) = \mathbb{P}(B) - \mathbb{P}(A \cap B)$, ossia $\mathbb{P}(B) = \mathbb{P}(A \cap B) + \mathbb{P}(A^{C} \cap B)$.
Ma questo e' ovvio: infatti
$$B = \Omega \cap B = (A \cup A^{C}) \cap B = (A \cap B) \cup (A^{C} \cap B)$$
e per l'_[[assiomi-della-probabilita-conseguenze|additivita' finita]]_ si ha proprio
$$\mathbb{P}(B) = \mathbb{P}(A \cap B) + \mathbb{P}(A^{C} \cap B)$$

**Qed**.

### Generalizzazione
> Una famiglia di $n$ eventi $A_{1}, \cdots, A_{n}$ si dicono **indipendenti** se valgono simultaneamente le seguenti uguaglianze:
> $$\forall k \in \{2, \cdots, n\}, \forall i_{1, \cdots, k} \in \{1, \cdots, n\}. \ \ \ \ \ \ \mathbb{P}(A_{i1} \cap \cdots \cap A_{ik}) = \mathbb{P}(A_{i1}) \cdot \cdots \cdot \mathbb{P}(A_{ik})$$

## Esercizi
### Gioco del lotto
![[gioco-del-lotto.png]]

#### 1.
Dobbiamo determinare lo [[spazio-di-probabilita|spazio di probabilita']] $(\Omega, \mathbb{P})$. Possiamo intuire come sia $\Omega$: infatti, l'insieme degli [[esito|esiti]] possibili dell'[[esperimento-aleatorio|esperimento aleatorio]] sara' costituito da delle _cinquine_ $(x_{1}, x_{2}, x_{3}, x_{4}, x_{5})$ di numeri da $1$ a $90$ senza ripetizioni. Formalmente si avra':
$$\Omega = \{(x_{1}, x_{2}, x_{3}, x_{4}, x_{5}) | x_{i} \in \{1, \cdots, 90\} \land i \neq j \implies x_i \neq x_j\}$$
In questo modo catturiamo la proprieta' di _non reimmissione_. Possiamo anche calcolare intuitivamente la cardinalita' di $\Omega$ come
$$|\Omega| = 90 \cdot 89 \cdot 88 \cdot 87 \cdot 86$$

Per determinare $\mathbb{P}$, dobbiamo dividere l'esperimento in $5$ [[sottoesperimento-aleatorio|sottoesperimenti aleatori]], e quindi creare una famiglia di eventi
$$E_{i, x_{i}} = \text{"estraggo il numero } x_{i} \text{ alla i-esima estrazione"}$$

Definiti questi eventi, non ci resta che esprimere la probabilita' che vogliamo sapere: vogliamo infatti combinarli uno in seguito all'altro, tramite l'intersezione.
$$\mathbb{P}(E_{1, x_{1}} \cap E_{2, x_{2}} \cap E_{3, x_{3}} \cap E_{4, x_{4}} \cap E_{5, x_{5}})$$

Possiamo allora sviluppare con la [[regola-della-catena|regola della catena]], e ottenere
$$\mathbb{P}(E_{1, x_{1}}) \mathbb{P}(E_{2,x_{2}} | E_{1, x_{1}}) \mathbb{P}(E_{3,x_{3}} | E_{1,x_{1}} \cap E_{2, x_{2}}) \mathbb{P}(E_{4,x_{4}} | E_{1,x_{1}} \cap E_{2, x_{2}} \cap E_{3, x_{3}}) \mathbb{P}(E_{5, x_{5}} | E_{1,x_{1}} \cap E_{2, x_{2}} \cap E_{3, x_{3}} \cap E_{4, x_{4}})$$

Ora siamo in grado di sapere quanto vale questa probabilita'. Infatti, assumendo che l'estrazione per ogni sottoesperimento sia la [[probabilita-uniforme|probabilita' uniforme]], possiamo usare la [[formula-di-laplace|Formula di Laplace]] su ogni probabilita' condizionata e non. Infatti avremo che:
- $\mathbb{P}(E_{1, x_{1}}) = \frac{1}{90}$
- $\mathbb{P}(E_{2, x_{2}} | E_{1, x_{1}}) = \frac{1}{89}$
- $\mathbb{P}(E_{3, x_{3}} | E_{1, x_{1}} \cap E_{2, x_{2}}) = \frac{1}{88}$
- $\mathbb{P}(E_{4, x_{4}} | E_{1, x_{1}} \cap E_{2, x_{2}} \cap E_{3, x_{3}}) = \frac{1}{87}$
- $\mathbb{P}(E_{5, x_{5}} | E_{1, x_{1}} \cap E_{2, x_{2}} \cap E_{3, x_{3}} \cap E_{4, x_{4}}) = \frac{1}{86}$

Quindi
$$\mathbb{P}(E_{1,x_{1}} \cap E_{2,x_{2}} \cap E_{3,x_{3}} \cap E_{4,x_{4}} \cap E_{5,x_{5}}) = \frac{1}{90 \cdot 89 \cdot 88 \cdot 87 \cdot 86}$$
ovvero, proprio
$$\frac{1}{|\Omega|} \implies \mathbb{P} \text{ e' la probabilita' uniforme}$$

Questo e' ovvio: rispetto allo spazio campionario del gioco del lotto, _una combinazione di numeri rispetto a un'altra non ha piu' probabilita' di vincere_!

#### 2.
Se le estrazioni avvengono con reimmissione, allora **la prima cosa che cambia e' proprio lo spazio campionario**! Questo _non ha piu' dei vincoli di non-ripetizione_:
$$\Omega = \{(x_{1}, x_{2}, x_{3}, x_{4}, x_{5}) | x_{i} \in \{1, \cdots, 90\}\}$$

Di conseguenza, la sua cardinalita' sara' diversa:
$$|\Omega| = 90^{5}$$

Per determinare $\mathbb{P}$ procediamo nello stesso modo di prima, ovvero creando una famiglia di eventi ognuna associata a un'estrazione:
$$E_{i, x_{i}} = \text{"estraggo il numero } x_{i} \text{ alla i-esima estrazione"}$$

Ugualmente al caso precedente, quindi, si vuole trovare la probabilita'
$$\mathbb{P}(E_{1, x_{1}} \cap E_{2, x_{2}} \cap E_{3, x_{3}} \cap E_{4, x_{4}} \cap E_{5, x_{5}})$$

Ora, pero', c'e' una differenza sostanziale: se sviluppassimo con la regola della catena, noteremmo che in realta' **gli eventi tra di loro sono indipendenti**. In altri termini, presa un'estrazione $E_{i, x_{i}}$ e un'altra $E_{j, x_{j}}$, si avra' che
$$\mathbb{P}(E_{i, x_{i}} | E_{j, x_{j}}) = \mathbb{P}(E_{i, x_{i}})$$
Infatti c'e' reimmissione, per cui _tra un'estrazione e l'altra la probabilita' rimane invariata_!

Quindi, otteniamo semplicemente che
$$\mathbb{P}(E_{1, x_{1}} \cap E_{2, x_{2}} \cap E_{3, x_{3}} \cap E_{4, x_{4}} \cap E_{5, x_{5}}) = \mathbb{P}(E_{1, x_{1}}) \mathbb{P}(E_{3, x_{3}}) \mathbb{P}(E_{3, x_{3}}) \mathbb{P}(E_{4, x_{4}}) \mathbb{P}(E_{5, x_{5}})$$
e assumendo sempre che ogni estrazione presenti probabilita' uniforme, questo diventa
$$\mathbb{P}(E_{1, x_{1}}) \mathbb{P}(E_{3, x_{3}}) \mathbb{P}(E_{3, x_{3}}) \mathbb{P}(E_{4, x_{4}}) \mathbb{P}(E_{5, x_{5}}) = \frac{1}{90^{5}} = \frac{1}{|\Omega|}$$
il che dimostra, ancora una volta, che $\mathbb{P}$ e' la probabilita' uniforme.

## Referenze
- [[formula-delle-probabilita-totali|Formula delle probabilità totali]]