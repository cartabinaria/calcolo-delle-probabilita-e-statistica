---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 06-05-2025 11:00:43
links:
  - "[[lecture-15042025131630|Lecture 15042025131630]]"
---
# Legge congiunta
---
## Introduzione
> Sia $(\Omega, \mathbb{P})$ uno [[spazio-di-probabilita|spazio di probabilita']] e $(X, Y)$ un [[vettore-aleatorio|vettore aleatorio]] bidimensionale su $(\Omega, \mathbb{P})$, definiamo la **legge congiunta** di $X$ e $Y$ la [[probabilita|probabilità]] $$\mathbb{P}_{(X,Y)}: \mathscr{P}(\mathbb{R}^{2}) \to [0, 1]$$
> definita come $\mathbb{P}((X, Y) \in B)$ per un qualche $B \subseteq \mathbb{R}^{2}$. In tal caso, si scrivera'
> $$(X, Y) \sim \mathbb{P}_{(X, Y)}$$

## Relazione con marginali
Dato un vettore aleatorio bidimensionale $(X, Y)$, lavoriamo di solito con i seguenti 3 oggetti:
- legge congiunta $\mathbb{P}_{(X,Y)}$;
- legge marginale $\mathbb{P}_{X}$;
- legge marginale $\mathbb{P}_{Y}$.

Nella legge congiunta ho piu' informazioni che nelle singole marginali: _tiene conto della dipendenza tra $X$ e $Y$_. Di fatto, **se conosco la legge congiunta posso ricavare le marginali, ma non vale il viceversa se non ho informazioni sulle dipendenze tra $X$ e $Y$**.

## Referenze
- [[leggi-marginali|Leggi marginali]]
- [[indipendenza-di-variabili-aleatorie|Indipendenza di variabili aleatorie]]