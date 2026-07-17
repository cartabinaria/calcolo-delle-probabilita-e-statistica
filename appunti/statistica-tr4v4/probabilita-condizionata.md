---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 04-03-2025 10:04:41
links:
  - "[[lecture-25022025133832|Lecture 25022025133832]]"
  - "[[lecture-28022025132238|Lecture 28022025132238]]"
---
# Probabilita' condizionata
---
## Introduzione
L'idea della probabilita' condizionata e' quella di **modellizzare la probabilita' di un qualunque evento conoscendo l'avvenimento di un evento precedente**. In particolare risponde alla domanda: _se so che si e' verificato l'evento $B$ e conosco la sua probabilita', qual e' la probabilita' che si sia verificato anche l'evento $A$_?

## Definizione
> La **probabilita' condizionata** e' una [[funzione-matematica|funzione]] di [[probabilita|probabilita']] della forma
> $$\mathbb{P}(\cdot|B) \ \ \ B \subseteq \Omega$$
> , dove $B$ e' un evento dello [[spazio-campionario|spazio campionario]] $\Omega$. Quindi, $\mathbb{P}(A|B)$ _esprime la probabilita' dell'[[evento|evento]] $A$ condizionata all'evento $B$_.
> Formalmente, siano $A, B$ due eventi su uno [[spazio-di-probabilita|spazio di probabilita']] $(\Omega, \mathbb{P})$ con $\mathbb{P}(B) > 0$, allora la probabilita' condizionata a $B$ e' definita come $$\mathbb{P}(A|B) = \frac{\mathbb{P}(A \cap B)}{\mathbb{P}(B)}$$

### Osservazioni
#### Probabilita' uniforme
In caso di [[probabilita-uniforme|probabilita' uniforme]], vale una sorta di [[formula-di-laplace|formula di Laplace]] adattata alla probabilita' condizionata. Infatti si ha che
$$\forall A \subseteq \Omega, \ \mathbb{P}(A) = \frac{|A|}{|\Omega|} \implies \mathbb{P}(A|B) = \frac{\mathbb{P}(A \cap B)}{\mathbb{P}(B)} = \frac{|A \cap B|}{|B|}$$

#### Non commutativita'
L'evento **$B$ e' fissato** nella definizione della probabilita' condizionata, per cui non necessariamente si ha che
$$\mathbb{P}(A|B) \neq \mathbb{P}(B|A)$$

#### $B = \Omega$
In tal caso
$$\mathbb{P}(A|\Omega) = \mathbb{P}(A)$$

#### $A = \Omega$
In tal caso
$$\mathbb{P}(\Omega|B) = 1$$

#### Funzione di probabilita'
Si dimostra che
$$\forall B \subseteq \Omega, \mathbb{P}(\cdot | B) : \mathscr{P}(\Omega) \to [0, 1]$$
ossia che la probabilita' condizionata e' a tutti gli effetti una funzione di probabilita'. In particolare _rispetta gli [[assiomi-della-probabilita|assiomi della probabilita']] e le loro conseguenze_.

## Utilizzo
Di solito, nei problemi di probabilita', _noi siamo a conoscenza della probabilita' condizionata_, o comunque siamo in grado di ricavarla facilmente: infatti, **il vero utilizzo della probabilita' condizionata e' nel ricavare la [[probabilita-dell-intersezione-di-eventi|probabilita' dell'intersezione tra due eventi]]**, usando la [[regola-della-catena|regola della catena]].

## Esercizi
### Urne
![[probabilita-condizionata-es1.png]]

Svolgimento:
- non vogliamo usare lo spazio campionario, nel senso che non ci serve
- affermazioni
	- $A =$ "estrarre nell'ordine una bianca, una rossa e una nera"
	- $\mathbb{P}(A)?$
- devo guardare i sottoesperimenti e capire le relazioni tra di loro
- introduciamo quindi 3 famiglie di eventi
	- $(B_{i})_{i = 1, \cdots, k}$
	- $(R_{i})_{i = 1, \cdots, k}$
	- $(N_{i})_{i = 1, \cdots, k}$
	- dove $k$ sono i sottoesperimenti, in questo caso 3 (perché 3 estrazioni)
- quindi riscrivo $$A = B_{1} \cap R_{2} \cap N_{3}$$
- per cui $$\mathbb{P}(A) = \mathbb{P}(B_{1} \cap R_{2} \cap N_{3}) = \mathbb{P}(B_{1})\mathbb{P}(R_{2}|B_{1})\mathbb{P}(N_{3}|R_{2}\cap B_{1})$$
	- e $\mathbb{P}(B_{1}) = \frac{1}{2}$
	- $\mathbb{P}(R_{2}|B_{1}) = \frac{1}{5}$, non usando la definizione, ma Laplace
	- $\mathbb{P}(N_{3} | R_{2} \cap B_{1}) = \frac{1}{2}$
- quindi, $\mathbb{P}(A) = \frac{1}{20}$

Generalmente, questa tipologia di esercizi si puo' facilmente risolvere usando il [[diagramma-ad-albero|diagramma ad albero]]. In questo esperimento, il diagramma ad albero corrispondente sarebbe:
![[diagramma-ad-albero.png]]

## Referenze
- [[eventi-indipendenti|Eventi indipendenti]]
- [[formula-delle-probabilita-totali|Formula delle probabilità totali]]
- [[formula-di-bayes|Formula di Bayes]]