---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 30-03-2025 19:42:55
links:
  - "[[lecture-18032025131728|Lecture 18032025131728]]"
  - "[[lecture-21032025132255|Lecture 21032025132255]]"
---
# Variabile aleatoria discreta
---
## Introduzione
> Sia $(\Omega, \mathbb{P})$ uno [[spazio-di-probabilita|spazio di probabilita']] e $X$ una [[variabile-aleatoria|variabile aleatoria]], si dice che $X$ e' una **variabile aleatoria discreta** se esiste un sottoinsieme $S_{X} \subseteq \mathbb{R}$ finito o al piu' infinito [[numerabilita|numerabile]] tale che
> - $p_{X}(x_{i}) > 0 \ \ \ \forall x_{i} \in S_{X}$ (minimalita' di $S_{X}$);
> - $\mathbb{P}(X \in S_{X}) = \sum\limits_{i} p_{X}(x_{i}) = 1$.
> 
> dove $p_{X}$ e' la [[densita-discreta|densita' discreta]] di $X$. Tale sottoinsieme $S_{X}$ si chiama **supporto** di $X$.

Potremmo definire il supporto come tutti i valori possibili assunti dalla variabile aleatoria con probabilita' positiva:
$$S_{X} = \{x \in \mathbb{R} | \mathbb{P}(X = x) > 0\} = \{x \in \mathbb{R} | p_{X}(x) > 0\}$$

## Casi
Analizziamo i casi tradizionali di [[variabile-aleatoria-costante|variabile aleatoria costante]] e [[variabile-aleatoria-indicatrice|variabile aleatoria indicatrice]], per dimostrare che in entrambi i casi si tratta di variabili aleatorie discrete.

### Variabile aleatoria costante
Se scegliamo il supporto $S_{X} = \{a\}$, dove $a \in \mathbb{R}$ e' il valore costante della variabile aleatoria $X$, allora possiamo costruire la tabella discreta

| $X$     | $a$ |
| ------- | --- |
| $p_{X}$ | $1$ |

### Variabile aleatoria indicatrice
In questo caso, se scegliamo il supporto $S_{X} = \{0, 1\}$, allora possiamo costruire la tabella discreta

| $X$     | $0$                 | $1$             |
| ------- | ------------------- | --------------- |
| $p_{X}$ | $1 - \mathbb{P}(A)$ | $\mathbb{P}(A)$ |

## Esempi
### Lancio di dadi
![[variabile-aleatoria-discreta-es1.png]]

Prima di tutto determiniamo lo spazio campionario come $\Omega = DR_{6,2}$ ([[disposizione-con-ripetizione|disposizione con ripetizione]]). A questo punto, la variabile aleatoria $X$ sara' definita come
$$X((w_{1}, w_{2})) = \min\{w_{1}, w_{2}\}$$

Per mostrare che $X$ e' discreta dobbiamo determinare il suo supporto $S_{X}$ tale che valgono le sue proprieta'. Scegliamo in particolare l'insieme $S_{X} = \{1, 2, 3, 4, 5, 6\} \subseteq \mathbb{R}$, e dimostriamo la valenza di:
- $p_{X}(x_{i}) > 0 \ \ \ \forall x_{i} \in S_{X} \iff \mathbb{P}(X = x_{i}) > 0 \ \ \ \forall x_{i} \in S_{X} \iff \mathbb{P}(\{(w_{1}, w_{2}) \in \Omega | X((w_{1}, w_{2})) = x_{i}\}) \ \ \ \forall x_{i} \in S_{X}$
	- e questo e' sempre strettamente positivo per tutti i valori di $S_{X}$, infatti esistera' sempre un esito non banale che verra' mappato da $X$ in $x_{i}$;
- $\mathbb{P}(X \in S_{X}) = \mathbb{P}(\{(w_{1}, w_{2}) \in \Omega | X((w_{1}, w_{2})) \in \{1, 2, 3, 4, 5, 6\}\}) = 1$
	- il che e' ovvio.

Per determinare $p_{X}$ analizziamo come si comporta la probabilita' per ogni elemento del supporto:
- $x = 1$ --> $p_{X}(1) = \mathbb{P}(X = 1) = \mathbb{P}(\{(1, 1), (1, 2), (1, 3), (1, 4), (1, 5), (1, 6), (2, 1), (3, 1), (4, 1), (5, 1), (6, 1)\}) = \frac{11}{36}$
- $x = 2$ --> $p_{X}(2) = \mathbb{P}(X = 2) = \mathbb{P}(\{(2, 2), (2, 3), (2, 4), (2, 5), (2, 6), (3, 2), (4, 2), (5, 2), (6, 2)\}) = \frac{9}{36}$
- $x = 3$ --> $p_{X}(3) = \mathbb{P}(X = 3) = \cdots = \frac{7}{36}$
- $x = 4$ --> $p_{X}(4) = \mathbb{P}(X = 4) = \cdots = \frac{5}{36}$
- $x = 5$ --> $p_{X}(5) = \mathbb{P}(X = 5) = \cdots = \frac{3}{36}$
- $x = 6$ --> $p_{X}(6) = \mathbb{P}(X = 6) = \cdots = \frac{1}{36}$

## Referenze
- [[valore-atteso|Valore atteso]]
- [[varianza|Varianza]]