---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 22-03-2025 17:48:05
links:
  - "[[lecture-11032025132556|Lecture 11032025132556]]"
  - "[[lecture-18032025131728|Lecture 18032025131728]]"
  - "[[lecture-21032025132255|Lecture 21032025132255]]"
---
# Funzione di ripartizione
---
## Introduzione
> Sia $(\Omega, \mathbb{P})$ uno [[spazio-di-probabilita|spazio di probabilita']] e $X: \Omega \to \mathbb{R}$ una [[variabile-aleatoria|variabile aleatoria]], si chiama **funzione di ripartizione** (o **CDF**) di $X$ la funzione
> $$F_{X}: \mathbb{R} \to [0, 1]$$
> definita come
> $$F_{X}(x) = \mathbb{P}_{X}((-\infty, x]) = \mathbb{P}(X \leq x) \ \ \ \ \ \ \forall x \in \mathbb{R}$$
> ovvero come la [[distribuzione-di-una-variabile-aleatoria|distribuzione]] sull'intervallo $(-\infty, x]$, equivalente alla [[probabilita|probabilita']] che $X$ sia mappata in un valore $\leq x$.
> Si indica, in tal caso, che
> $$X \sim F_{X}$$

## Casi
Vogliamo mostrare come si comporta la funzione di ripartizione di una variabile aleatoria $X$ sui casi fondamentali: [[variabile-aleatoria-costante|variabile aleatoria costante]] e [[variabile-aleatoria-indicatrice|variabile aleatoria indicatrice]].

### Variabile aleatoria costante
Se $X(w) = a \ \ \ \forall w \in \Omega$ con $a \in \mathbb{R}$, allora
$$F_{X}(x) = \mathbb{P}_{X}((-\infty, x]) = \mathbb{P}(X \in (-\infty, x]) = \begin{cases} 1 & a \in (-\infty, x] \\ 0 & a \notin (-\infty, x] \end{cases} = \begin{cases} 1 & x \geq a \\ 0 & x < a \end{cases}$$

![[funzione-ripartizione-costante.png]]

### Variabile aleatoria indicatrice
Se $X(w) = \begin{cases} 1 & w \in A \\ 0 & w \notin A \end{cases}$ per un certo $A \subseteq \Omega$, allora
$$F_{X}(x) = \mathbb{P}_{X}((-\infty, x]) = \mathbb{P}(X \in (-\infty, x]) = \begin{cases} 1 & x \geq 1 \\ 1 - \mathbb{P}(A) & 0 \leq x < 1 \\ 0 & x < 0 \end{cases}$$
![[funzione-ripartizione-indicatrice.png]]

<u>Nota bene</u>: _sembra da questo caso che la funzione di ripartizione non catturi $\mathbb{P}(A)$_, presente invece nella distribuzione $\mathbb{P}_{X}(B)$ per un qualche $B$. La verita' e' che _invece si riesce a ricavare_.

## Teorema
Le caratteristiche fondamentali della funzione di ripartizione sono raccolte nel seguente teorema.
> Sia $(\Omega, \mathbb{P})$ uno spazio di probabilita' e $X: \Omega \to \mathbb{R}$ una variabile aleatoria, allora la funzione di ripartizine $F_{X}$ verifica le seguenti proprieta':
> 1. $F_{X}$ è [[funzioni-monotone|monotona crescente]];
> 2. $F_{X}$ è [[funzioni-continue|continua]] a destra, ossia $\lim_{y \to x^{+}} F_{X}(y) = F_{X}(x) \ \ \ \forall x \in \mathbb{R}$;
> 3. $\lim_{x \to +\infty} F_{X}(x) = 1$;
> 4. $\lim_{x \to -\infty} F_{X}(x) = 0$.

E' di fondamentale importanza il _teorema complementare_ che dimostra che **una qualunque funzione** $G: \mathbb{R} \to [0, 1]$ **che verifica le 4 proprieta', e' una funzione di ripartizione per un qualche spazio di probabilita' e una qualche variabile aleatoria**.

### Dimostrazione
Non dimostriamo i punti 2 e 4 in quanto facilmente deducibili dal punto 3.

#### 1.
Dobbiamo dimostrare
$$\forall x, y. \ x \leq y \ \ \ \ \ \  F_{X}(x) \leq F_{X}(y)$$
Ma questo risulta ovvio dalla [[assiomi-della-probabilita|monotonia della probabilita']], infatti sapendo che $(-\infty, x] \subset (-\infty, y]$, si ha:
$$F_{X}(x) = \mathbb{P}_{X}((-\infty, x]) \leq \mathbb{P}_{X}((-\infty, y]) = F_{X}(y)$$

**Qed**.

#### 3.
Dobbiamo dimostrare
$$\lim_{x \to +\infty} F_{X}(x) = 1$$
ovvero
$$\lim_{x \to +\infty} \mathbb{P}_{X}((-\infty, x]) = \mathbb{P}_{X}(\mathbb{R})$$

Applico il lemma della [[stabilita-della-probabilita-per-limiti-monotoni|stabilita' della probabilita' per limiti monotoni]]: cerco $B_{n}$ tali che $B_{n} \subseteq B_{n+1}, \ \ \bigcup_{n=1}^{+\infty} B_{n} = \mathbb{R}$. Sceglio proprio $B_{n} = (-\infty, n]$, e quindi per il lemma ho
$$\lim_{n \to +\infty} \mathbb{P}_{X}(B_{n}) = \mathbb{P}_{X}(\mathbb{R}) = 1$$

Ora devo passare da $n \in \mathbb{N}$ a $x \in \mathbb{R}$, ma e' facile: infatti $F_{X}$ come dimostrato in precedenza e' monotona crescente, e quindi _ammette limite, e questo e' unico_ (sia per i [[numeri-naturali|naturali]] che per i [[numeri-reali|reali]]). Di conseguenza devo avere
$$\lim_{x \to +\infty} F_{X}(x) = 1$$

## Proprieta'
Sappiamo, dalle proprieta' delle variabili aleatorie, che
$$\mathbb{P}(X \leq x) = \mathbb{P}(X < x) + \mathbb{P}(X = x)$$

Ma dato che $\mathbb{P}(X \leq x) = \mathbb{P}_{X}((-\infty, x])$ e $\mathbb{P}(X < x) = \mathbb{P}_{X}((-\infty, x))$, allora si puo' scrivere la probabilita' che un evento sia mappato in $x$ usando la funzione di ripartizione come
$$\mathbb{P}(X = x) = F_{X}(x) - F_{X}(x^{-}) = \Delta F_{X}(x)$$

![[funzione-ripartizione-delta.png]]

In generale, possiamo scrivere la probabilita' di ogni intervallo in termini di $F_{X}$:
- $(a, b]$, allora $$\mathbb{P}_{X}((a, b]) = F_{X}(b) - F_{X}(a)$$
- $[a, b)$, allora $$\mathbb{P}_{X}([a, b)) = F_{X}(b^{-}) - F_{X}(a^{-})$$
- $(a, b)$, allora $$\mathbb{P}_{X}((a, b)) = F_{X}(b^{-}) - F_{X}(a)$$
- $[a, b]$, allora $$\mathbb{P}_{X}([a, b]) = F_{X}(b) - F_{X}(a^{-})$$

### Variabili aleatorie discrete
Per quanto riguarda le [[variabile-aleatoria-discreta|variabili aleatorie discrete]], vale un teorema che mostra un'equivalenza tra il loro comportamento e la funzione di ripartizione.
> Le seguenti affermazioni sono equivalenti:
> 1. $X$ è una _variabile aleatoria discreta_;
> 2. $F_{X}$ è _costante a tratti_ (a scalini) $$p_{X}(x) = F_{X}(x) - F_{X}(x^{-}) \ \ \ \forall x \in S_{X}$$;
> 3. $$\mathbb{P}_{X}(B) = \mathbb{P}(X \in B) = \sum\limits_{x \in S_{X} \cap B} p_{X}(x) = \sum\limits_{x \in S_{X}} p_{X}(x) \delta_{x}(B)$$ (definizione alternativa usando le [[delta-di-dirac|delta di Dirac]]);

## Referenze