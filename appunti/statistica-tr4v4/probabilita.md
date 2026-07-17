---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 20-02-2025 10:35:51
links:
  - "[[lecture-18022025132744|Lecture 18022025132744]]"
  - "[[lecture-21022025131008|Lecture 21022025131008]]"
---
# Probabilita'
---
## Definizione
E' "vietato" dare una definizione di probabilita', in quanto e' un _concetto primitivo_. Ciascuno di noi ha dentro di se' una sua interpretazione del concetto di probabilita'. Quindi, la domanda "cos'e' la probabilita'?" riguarda la filosofia, non la matematica.

Se volessimo pero' uniformare il concetto di probabilita' in una sorta di definizione matematica, allora potremmo dire che **la probabilita' e' la misura dell'avverabilita' di un evento**.

Se prendo una [[logica-proposizionale|proposizione]] $A$, posso associarci una quantita' della sua probabilita'. In una logica binaria ([[logica-classica|classica]]), avrei solo due possibili valori: _vero_ o _falso_. La probabilita' $\mathbb{P}$, invece, la misuriamo in valori continui da 0 a 1, tale che:
- $\mathbb{P}(A) = 0 \implies$ $A$ e' falsa;
- $\mathbb{P}(A) = 1 \implies$ $A$ e' vera.

## Assegnamento
Ma come si assegna la probabilita' ad una proposizione? Anche in questo caso la domanda non riguarda la matematica, ma la statistica: infatti **si stima la probabilita' di un evento**.

Esistono in particolare 2 approcci per stimare la probabilita' di un evento:
- _approccio frequentista_ --> ripeto l'esperimento, colleziono i dati e conto il numero di volte in cui si verifica $A$ fratto il numero totale di esperimenti, $$\mathbb{P}(A) \approx \frac{\text{num. di volte che si verifica A nel campione}}{n}$$
- _approccio bayesiano_ --> prima di procedere con l'esperimento, si raccolgono tutte le informazioni a disposizione sul fenomeno studiato, per giungere a un'assegnazione iniziale (detta _a priori_)

E' preferito l'approccio bayesiano nei casi in cui e' facile ottenere informazioni a priori sul fenomeno (sfruttando la sua _simmetria_), o in cui e' impossibile ripetere l'esperimento.

## Formalmente
> Definiti gli [[assiomi-della-probabilita|assiomi della probabilita']] possiamo definire la probabilita' come una [[funzione-matematica|funzione]] che ad ogni sottoinsieme $A$ dello [[spazio-campionario|spazio campionario]] $\Omega$ fa corrispondere un [[numeri-reali|reale]] in $[0, 1]$:
> $$\mathbb{P}: \mathscr{P}(\Omega) \to [0, 1]$$
> dove $\mathscr{P}$ e' l'[[assioma-dell-insieme-potenza|insieme delle parti]].

## Referenze
- [[probabilita-discreta|Probabilita' discreta]]
- [[probabilita-uniforme|Probabilita' uniforme]]