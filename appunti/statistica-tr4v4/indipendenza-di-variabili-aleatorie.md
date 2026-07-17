---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 06-05-2025 11:06:35
links:
  - "[[lecture-15042025131630|Lecture 15042025131630]]"
---
# Indipendenza di variabili aleatorie
---
## Introduzione
> Sia $(\Omega, \mathbb{P})$ uno [[spazio-di-probabilita|spazio di probabilità]] e $(X, Y)$ un [[vettore-aleatorio|vettore aleatorio]], si dice che $X$ e $Y$ sono **indipendenti**[^1] se
> $$\mathbb{P}(\{X \in B_{1}\} \cap \{Y \in B_{2}\}) = \mathbb{P}(X \in B_{1}) \mathbb{P}(Y \in B_{2}) \ \ \ \forall B_{1}, B_{2} \subseteq \mathbb{R}$$
> anche espresso, con _zucchero sintattico_, in
> $$\mathbb{P}(X \in B_{1}, Y \in B_{2}) = \mathbb{P}(X \in B_{1}) \mathbb{P}(Y \in B_{2}) \ \ \ \forall B_{1}, B_{2} \subseteq \mathbb{R}$$
> . In altre parole, due [[variabile-aleatoria|variabili aleatorie]] si dicono indipendenti se
> $$\mathbb{P}_{(X, Y)}(B_{1} \times B_{2}) = \mathbb{P}_{X}(B_{1}) \mathbb{P}_{Y}(B_{2}) \ \ \ \forall B_{1}, B_{2} \subseteq \mathbb{R}$$
> ossia se **la [[legge-congiunta|legge congiunta]] si fattorizza nelle [[leggi-marginali|leggi marginali]]**.
> In tal caso, si indichera'
> $$X \perp\!\!\!\perp Y$$

## Teoremi
### Lemma
> Se $(X, Y)$ vettore aleatorio e $X \perp\!\!\!\perp Y$, allora per qualunque $f, g: \mathbb{R} \to \mathbb{R}$ vale che $f(X) \perp\!\!\!\perp g(Y)$.

#### Dimostrazione
Per definizione di indipendenza, devo dimostrare
$$\mathbb{P}(f(X) \in B_{1}, g(Y) \in B_{2}) = \mathbb{P}(f(X) \in B_{1})\mathbb{P}(g(Y) \in B_{2}) \ \ \ \forall B_{1}, B_{2} \subseteq \mathbb{R}$$

Fissati $B_{1}, B_{2}$, noto che
$$\mathbb{P}(f(X) \in B_{1}, g(Y) \in B_{2}) = \mathbb{P}(X \in f^{-1}(B_{1}), Y \in f^{-1}(B_{2}))$$

A questo punto questo e' fattorizzabile, in quanto $X, Y$ sono indipendenti.

**Qed**.

### Funzione
> Se $(X, Y)$ vettore aleatorio e $X \perp\!\!\!\perp Y$, allora $\nexists f: \mathbb{R} \to \mathbb{R} : Y = f(X)$ a meno che $f(X) = c$ (costante).

#### Dimostrazione
Per assurdo, assumo che esista una $f$ tale che $Y = f(X)$. Ora scelgo $g(Y) = Y$ (identita'), allora per il lemma sopra dimostrato ho che
$$f(X) \perp\!\!\!\perp g(Y) \implies f(X) \perp\!\!\!\perp f(X)$$

Questo significa che
$$\mathbb{P}(f(X) \in B_{1}, f(X) \in B_{2}) = \mathbb{P}(f(X) \in B_{1})\mathbb{P}(f(X) \in B_{2}) \ \ \ \forall B_{1}, B_{2} \subseteq \mathbb{R}$$

Allora, scelgo $B_{1} = B_{2} = B$, e ho
$$\mathbb{P}(f(X) \in B, f(X) \in B) = \mathbb{P}(f(X) \in B)\mathbb{P}(f(X) \in B)$$

Quindi, svolti i calcoli algebrici ho che vale
$$\mathbb{P}(f(X) \in B) = \mathbb{P}(f(X) \in B)^{2}$$
o equivalentemente
$$\mathbb{P}(f(X) \in B) - \mathbb{P}(f(X) \in B)^{2} = 0$$
$$\mathbb{P}(f(X) \in B) \cdot (1 - \mathbb{P}(f(X) \in B)) = 0$$

Notare che $\mathbb{P}(f(X) \in B) = \mathbb{P}_{Y}(B)$.  E il prodotto puo' essere uguale a $0 \iff \mathbb{P}_{Y}(B) = 0 \lor \mathbb{P}_{Y}(B) = 1$. Quindi puo' assumere solo questi 2 valori. Allora significa che la legge di $Y$ su $B$ puo' essere descritta come un [[delta-di-dirac|delta di Dirac]] per un certo $a \in \mathbb{R}$ mappato da $Y$:
$$\mathbb{P}_{Y}(B) = \delta_{a}(B) = \begin{cases} 0 & a \notin B \\ 1 & a \in B \end{cases}$$

Allora significa che $Y$ puo' mappare solo in $a$, e quindi che e' costante. Ma $Y = f(X)$, che per ipotesi non era costante. Assurdo.

**Qed**.

## Referenze

[^1]: ricorda l'[[eventi-indipendenti|indipendenza tra eventi]]
