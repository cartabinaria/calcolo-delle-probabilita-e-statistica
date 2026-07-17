---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 10-03-2025 11:24:01
links:
  - "[[lecture-04032025133148|Lecture 04032025133148]]"
---
# Formula di Bayes
---
## Introduzione
> Insieme alla [[regola-della-catena|regola della catena]] e alla [[formula-delle-probabilita-totali|formula delle probabilità totali]], la **formula di Bayes** è una delle principali formule della [[probabilita-condizionata|probabilità condizionata]], e dice che fissati $A, B$ due [[evento|eventi]] tali che $\mathbb{P}(A) > 0$ e $\mathbb{P}(B) > 0$, allora vale
> $$\mathbb{P}(B|A) = \frac{\mathbb{P}(A|B) \mathbb{P}(B)}{\mathbb{P}(A)}$$
> Viene usata quando si vuole calcolare una probabilità condizionata di eventi "_nell'ordine temporale sbagliato_".

## Dimostrazione
Uso la seguente sequenza di uguaglianze:
$$\frac{\mathbb{P}(A|B) \mathbb{P}(B)}{\mathbb{P}(A)} = \frac{\mathbb{P}(A \cap B)}{\mathbb{P}(A)} = \frac{\mathbb{P}(B \cap A)}{\mathbb{P}(A)} = \frac{\mathbb{P}(B|A)\mathbb{P}(A)}{\mathbb{P}(A)} = \mathbb{P}(B|A)$$

<u>Nota bene</u>:
- nella prima uguaglianza uso la regola della catena e il fatto che $\mathbb{P}(B) > 0$;
- nella seconda uguaglianza uso la commutativita' dell'intersezione;
- nella terza uguaglianza uso la regola della catena e il fatto che $\mathbb{P}(A) > 0$;

**Qed**.

## Esercizi
### Urne
![[bayes-urne.png]]

Inanzitutto determiniamo gli eventi, sapendo che ci sono due [[sottoesperimento-aleatorio|sottoesperimenti]]:
- $T =$ "esce testa";
- $C = T^{C} =$ "esce croce";
- $B =$ "esce una pallina bianca";
- $R = B^{C} =$ "esce una pallina rossa";

Non ci resta che formalizzare la probabilita' che vogliamo calcolare:
$$\mathbb{P}(T|B)$$

Notando che l'ordine degli eventi e' "innaturale", usiamo la formula di Bayes:
$$\mathbb{P}(T|B) = \frac{\mathbb{P}(B|T) \mathbb{P}(T)}{\mathbb{P}(B)}$$

Ora:
- $\mathbb{P}(B|T) \mathbb{P}(T)$ e' facile da calcolare, infatti (assumendo probabilita' uniforme) $$\mathbb{P}(B|T) \mathbb{P}(T) = \frac{1}{3} \frac{1}{2} = \frac{1}{6}$$
- $\mathbb{P}(B)$ si deve calcolare usando la formula delle probabilita' totali, ovvero $$\mathbb{P}(B) = \mathbb{P}(B \cap T) + \mathbb{P}(B \cap T^{C}) = \mathbb{P}(B|T)\mathbb{P}(T) + \mathbb{P}(B|T^{C})\mathbb{P}(T^{C}) = \frac{1}{6} + \frac{2}{7} \frac{1}{2} = \frac{1}{6} + \frac{1}{7} = \frac{13}{42}$$
Rimane solo la divisione:
$$\mathbb{P}(T|B) = \frac{\frac{1}{6}}{\frac{13}{42}} = \frac{1}{6} \frac{42}{13} = \frac{7}{13}$$

## Referenze