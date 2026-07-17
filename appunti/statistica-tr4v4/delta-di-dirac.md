---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 24-02-2025 17:58:17
links:
  - "[[lecture-21022025131008|Lecture 21022025131008]]"
---
# Delta di Dirac
---
## Introduzione
> Sia $\Omega = \mathbb{R}$ lo [[spazio-campionario|spazio campionario]], e $x_{0} \in \mathbb{R}$ un numero fissato, allora la funzione
> $$\delta_{x_{0}} : \mathscr{P}(\mathbb{R}) \to [0, 1]$$
> tale che
> $$\delta_{x_{0}}(A) = \begin{cases}1 & x_{0} \in A \\ 0 & x_{0} \notin A\end{cases} \ \ \ \forall A \subseteq \mathbb{R}$$
> e' detta **delta di Dirac** in $x_{0}$, ed e' una [[probabilita-discreta|probabilita' discreta]] che forma lo [[spazio-di-probabilita|spazio di probabilita']] $(\mathbb{R}, \delta_{x_0})$.

## Utilita'
Tramite la delta di Dirac, **siamo in grado di costruire tutte le probabilita' discrete**. In particolare, fissati:
- $\Omega = \mathbb{R}$
- $n$ [[esito|esiti]] $x_{1}, \cdots, x_{n}$
- $n$ pesi $p_{1}, \cdots, p_{n} : p_{i} \in [0, 1] \land \sum\limits_{i=1}^{n} p_{i} = 1$

allora possiamo definire la probabilita' discreta $\mathbb{P}$ sull'[[evento|evento]] $A$ come
$$\mathbb{P}(A) = \sum\limits_{i=1}^{n} p_{i} \delta_{x_{i}}(A)$$
ossia come **[[combinazione-lineare|combinazione lineare]] convessa**.

Ogni peso $p_{i}$ esplicita la probabilita' dell'esito $x_{i}$. Per cui se l'evento $A$ e' composto da tot. $x_{i}$, allora _$\mathbb{P}(A)$ sara' calcolato come la somma dei pesi associati agli esiti favorevoli di $A$_.

## Esempio
Consideriamo l'esperimento aleatorio del lancio di dadi. Si ha che $\Omega = \{1, 2, 3, 4, 5, 6\}$, allora possiamo scrivere $\mathbb{P}$ come funzione di probabilita' discreta. Infatti, a meno di dadi truccati, possiamo considerare la probabilita' di uscita di ogni faccia come equiprobabile[^1]: i pesi $p_{i}$ saranno tutti $\frac{1}{6}$, per cui
$$\mathbb{P}(A) = \sum\limits_{i=1}^{6} \frac{1}{6} \delta_{i}(A)$$

## Referenze
[^1]: [[principio-di-ragione-non-sufficiente|Principio di ragione non sufficiente]]