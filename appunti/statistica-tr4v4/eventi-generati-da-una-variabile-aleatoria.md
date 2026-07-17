---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 20-03-2025 20:38:00
links:
  - "[[lecture-11032025132556|Lecture 11032025132556]]"
---
# Eventi generati da una variabile aleatoria
---
## Introduzione
> Un [[evento|evento]] $E \subseteq \Omega$ e' **generato** da una [[variabile-aleatoria|variabile aleatoria]] $X$ se
> $$\exists B \subseteq \mathbb{R} : E = \{w \in \Omega | X(w) \in B\}$$
> o in altri termini, se si puo' trovare un sottoinsieme $B$ di $\mathbb{R}$ tale che ogni esito dell'evento $E$ viene mappato da $X$ in $B$. Volendo usare un po' di zucchero sintattico, si potrebbe esprimere questa condizione anche come
> $$\exists B \subseteq \mathbb{R} : E = X^{-1}(B)$$
> ossia se e' possibile trovare tale sottoinsieme $B$ tale che $E$ e' la [[controimmagine|controimmagine]] di $X$ per $B$ (l'unione delle controimmagini dei singoli elementi di $B$).
> L'insieme degli eventi generati da una variabile aleatoria $X$ si indica con
> $$\sigma(X)$$

### Esempio
Se prendiamo nell'[[esperimento-aleatorio|esperimento aleatorio]] del lancio di due dadi, come variabile aleatoria
$$X = \text{risultato della somma dei lanci}$$
allora l'evento
$$A = \text{la somma e' 3}$$
puo' essere generato da $X$ trovando il sottoinsieme $B$ di $\mathbb{R}$ tale che $X$ mappi ogni elemento di $A$ in $B$:
$$B = \{3\}$$
Quindi posso esprimere $A$ in termini di $X$ come
$$A = \{X \in \{3\}\} = X^{-1}(\{3\})$$

E ancora, se considero l'evento
$$C = \text{la somma e'} \leq 5$$
allora il sottoinsieme $B$ tale la controimmagine di $X$ per $B$ sia proprio $C$ non e' altro che
$$B = (-\infty, 5]$$

Di conseguenza
$$C = X^{-1}((-\infty, 5])$$

### Osservazione
Per ogni variabile aleatoria $X$, ho che
$$\Omega = \{X \in \mathbb{R}\}$$
$$\varnothing = \{X \in \varnothing\}$$

## Casi
Spesso, ci si chiede _data una variabile aleatoria $X$ quale siano gli eventi da essa generati_: in altri termini si vuole determinare $\sigma(X)$.

### Variabili aleatorie costanti
Se $X$ e' una [[variabile-aleatoria-costante|variabile aleatoria costante]], allora fissato $a \in \mathbb{R}$ si ha
$$X(w) = a \ \ \ \forall w \in \Omega$$

Per trovare $\sigma(X)$, consideriamo un evento generico $E$. Questo e' generato da $X$ se $\exists B \subseteq \mathbb{R}$ tale che $E = \{w \in \Omega : X(w) \in B\}$. Allora, una volta fissato $B$, se sappiamo che $X(w) = a$ per ogni $w$, allora il tutto dipende semplicemente da $a$!
$$E = \{w | X(w) \in B\} = \{w | a \in B\} = \begin{cases} \Omega & a \in B \\ \varnothing & a \notin B \end{cases}$$

Di conseguenza
$$\sigma(X) = \{\Omega, \varnothing\}$$

### Variabili aleatorie indicatrici
In questo caso, fissiamo un evento $A \subseteq \Omega$, e definiamo quindi $X$ come
$$X(w) = \begin{cases} 1 & w \in A \\ 0 & w \notin A \end{cases}$$

Per capire quali sono gli eventi generati da $X$, consideriamo un evento generico $E$. Questo e' generato da $X$ se $\exists B \subseteq \mathbb{R}$ tale che $E = \{w \in \Omega : X(w) \in B\}$. Fissato $B$, allora $E$ diventa
$$E = \{w | X(w) \in B\} = \begin{cases} A & 1 \in B \land 0 \notin B \\ A^{C} & 1 \notin B \land 0 \in B \\ \Omega & 1 \in B \land 0 \in B \\ \varnothing & 1 \notin B \land 0 \notin B \end{cases}$$

Di conseguenza
$$\sigma(X) = \{A, A^{C}, \Omega, \varnothing\}$$

## Referenze