---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 10-03-2025 11:13:31
links:
  - "[[lecture-28022025132238|Lecture 28022025132238]]"
---
# Formula delle probabilità totali
---
## Introduzione
> Presa una famiglia di [[evento|eventi]] $A_{i, \cdots, n}$, tali che
> $$\bigcup_{i=1}^{n} A_{i} = \Omega \ \ \ \ \ \ \ \ \ \ A_{i} \cap A_{j} = \varnothing \ \ \ \forall i \neq j$$
> ossia che sono una [[partizione-dello-spazio-campionario|partizione]] dello [[spazio-campionario|spazio campionario]] $\Omega$, allora per ogni evento $B$ vale
> $$B = \bigcup_{i=1}^{n} (B \cap A_{i})$$
> e quindi, per la [[assiomi-della-probabilita-conseguenze|proprietà di additività finita]]
> $$\mathbb{P}(B) = \sum\limits_{i=1}^{n} \mathbb{P}(B \cap A_{i})$$
> detta **formula delle probabilità totali**. Inoltre, se si assume (e di solito e' cosi') $\mathbb{P}(A_{i}) > 0 \ \ \ \forall i$, allora possiamo applicare la [[regola-della-catena|regola della catena]] per scrivere la formula come
> $$\mathbb{P}(B) = \sum\limits_{i=1}^{n} \mathbb{P}(B|A_{i})\mathbb{P}(A_{i})$$

![[formula-probabilita-totali.png]]

## Dimostrazione
So che
$$\bigcup_{i=1}^{n} A_{i} = \Omega \ \ \ \ \ \ \ \ \ \ A_{i} \cap A_{j} = \varnothing \ \ \ \forall i \neq j$$

Devo dimostrare che fissato un evento $B \subseteq \Omega$, allora
$$B = \bigcup_{i=1}^{n} (B \cap A_{i})$$

Noto che
$$B = B \cap \Omega = B \cap \bigcup_{i=1}^{n} A_{i} = \bigcup_{i=1}^{n} (B \cap A_{i})$$
Sapendo che gli $A_{i}$ sono disgiunti, allora lo sono anche i $B \cap A_{i}$[^1]. Quindi posso usare la proprieta' dell'attivita' finita della probabilita' e ottenere
$$\mathbb{P}(B) = \sum\limits_{i=1}^{n} \mathbb{P}(B \cap A_{i})$$
**Qed**.

## Esercizi
### Urna
![[urna-probabilita-totali.png]]

<u>Nota bene</u>: _non abbiamo alcuna necessita' di costruire lo spazio campionario_!

#### Con formule
Prima di tutto, andiamo a considerare per ognuno dei due [[sottoesperimento-aleatorio|sottoesperimenti]] (le estrazioni), gli eventi associati: costruiamo la famiglia di eventi
- $B_{1} =$ "la prima estratta e' bianca";
- $R_{1} =$ "la prima estratta e' rossa";
- $B_{2} =$ "la seconda estratta e' bianca";
- $R_{2} =$ "la seconda estratta e' rossa";

Una volta che abbiamo tutti gli eventi sottomano, scriviamo cio' che vogliamo conoscere:
$$\mathbb{P}(B_{2})$$

Ora, $B_{2}$ puo' capitare in due distinti casi:
1. alla prima estrazione e' avvenuto $B_{1}$;
2. alla prima estrazione e' avvenuto $R_{1}$;

Notiamo anche, che $B_{1} = R_{1}^{C}$, o in altre parole: $B_{1}$ ed $R_{1}$ formano una partizione di $\Omega$. Infatti
$$B_{1} \cup R_{1} = \Omega \ \ \ \ \ \ B_{1} \cap R_{1} = \varnothing$$

Quindi, possiamo usare la formula delle probabilita' totali su $B_{2}$:
$$\mathbb{P}(B_{2}) = \mathbb{P}(B_{2} \cap B_{1}) + \mathbb{P}(B_{2} \cap R_{1})$$
che, usando la regola della catena, possiamo sviluppare in
$$\mathbb{P}(B_{2}) = \mathbb{P}(B_{2}|B_{1})\mathbb{P}(B_{1}) + \mathbb{P}(B_{2}|R_{1})\mathbb{P}(R_{1})$$

Allora non ci resta che calcolare, _assumendo che le singole estrazioni siano la [[probabilita-uniforme|probabilita' uniforme]]_:
- $\mathbb{P}(B_{1}) = \frac{6}{10} = \frac{3}{5}$
- $\mathbb{P}(R_{1}) = \frac{4}{10} = \frac{2}{5}$
- $\mathbb{P}(B_{2}|B_{1}) = \frac{5}{9}$
- $\mathbb{P}(B_{2}|R_{1}) = \frac{6}{9} = \frac{2}{3}$

Quindi
$$\mathbb{P}(B_{2}) = \frac{5}{9} \frac{3}{5} + \frac{2}{3} \frac{2}{5} = \frac{1}{3} + \frac{4}{15} = \frac{9}{15} = \frac{3}{5}$$

#### Con diagramma ad albero
Allo stesso risultato ci si puo' arrivare costruendosi il [[diagramma-ad-albero|diagramma ad albero]]:
![[diagramma-ad-albero-urne.png]]

Una volta costruito, per conoscere $\mathbb{P}(B_{2})$, sara' sufficiente sommare le probabilita' di tutti i cammini che da $\Omega$ conducono a $B_{2}$.

## Referenze

[^1]: supponiamo per assurdo che $(B \cap A_{i}) \cap A_{j} \neq \varnothing$; per l'associativita' dell'intersezione, significa che $B \cap (A_i \cap A_j) \neq \varnothing$; ma questo e' un assurdo, perche' per ipotesi $A_i \cap A_j = \varnothing$, e un qualunque insieme $B$ intersecato con il vuoto da' il vuoto.
