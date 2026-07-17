---
tags:
  - category/note
  - status/ongoing
  - topic/calcolo-delle-probabilità-e-statistica
date: 22-04-2025 13:28:29
links:
  - "[[lecture-04042025131943|Lecture 04042025131943]]"
  - "[[lecture-08042025133009|Lecture 08042025133009]]"
---
# Variabile aleatoria continua
---
## Introduzione
> Sia $(\Omega, \mathbb{P})$ uno [[spazio-di-probabilita|spazio di probabilita']] e $X$ una [[variabile-aleatoria|variabile aleatoria]], si dice che $X$ e' una **variabile aleatoria continua** se esiste una [[densita-continua|densita' continua]] $f_{X}$ tale che
> $$\mathbb{P}(a \leq X \leq b) = \int_{a}^{b} f_{X}(x) \ dx \ \ \ \forall [a, b] \subseteq \mathbb{R}$$
> o piu' in generale
> $$\mathbb{P}_{X}(B) = \mathbb{P}(X \in B) = \int_{B} f_{X}(x) \ dx \ \ \ \forall B \subseteq \mathbb{R}$$

<u>Nota bene</u>: vale che **$p_{X}(x)$ su $X$ variabile aleatoria continua, e' sempre uguale a 0**. Infatti $$p_{X}(x) = \mathbb{P}(X = x) = \mathbb{P}(x \leq X \leq x) = \int_{x}^{x} f_{X}(t) \, dt = 0$$.

## Funzione di ripartizione
La [[funzione-di-ripartizione|funzione di ripartizione]] su una variabile aleatoria continua si definisce come
$$F_{X}(x) := \mathbb{P}(X \leq x) = \int_{-\infty}^{x} f_{X}(y) \ dy$$

Si nota come, essendo la [[densita-discreta|densita' discreta]] $p_{X}$ uguale a 0 per ogni $x$, significa che $F_{X}$ non avra' salti: e' per forza una [[funzioni-continue|funzione continua]].

### Casi particolari
E' importante notare che
$$\mathbb{P}(a < X \leq b) = \mathbb{P}(a \leq X < b) = \mathbb{P}(a < X < b) = \mathbb{P}(a \leq X \leq b) =$$
$$= \int_{a}^{b} f_{X}(x) \, dx = F_{X}(b) - F_{X}(a)$$

e quindi anche che
$$\mathbb{P}(X < x) = \mathbb{P}(X \leq x) = F_{X}(x)$$
$$\mathbb{P}(X \geq x) = \mathbb{P}(X > x) = 1 - \mathbb{P}(X \leq x) = 1 - F_{X}(x) = \int_{x}^{+\infty} f_{X}(y) \, dy$$

## Osservazioni
### Univocita'
> Data $X$ una variabile aleatoria continua, la sua _densita' non e' univocamente determinata_. In particolare, _se $g$ e' una funzione che e' uguale a $f_{X}$ a meno di un insieme finito di valori, allora anche $g$ e' una densita' continua_.

### Integrabilita'
Sappiamo che la funzione di ripartizione di una variabile aleatoria continua e' una [[funzione-integrale|funzione integrale]] (anche detta _assolutamente continua_). Ma nella pratica e' difficile dimostrare che una funzione e' integrale: di solito si assume che $X$ sia continua, il quale implica che $F_{X}$ sia integrale; o altrimenti si dimostra che _$F_{X} \in C^{1}$ a tratti_ ([[classe-c|classe C]]), ovvero che
- $F_{X}$ e' continua;
- $F_{X}$ e' derivabile tranne che in un numero finito o numerabile di punti;
- $F'_{X}$ e' continua (tranne che per quei punti in cui $F_{X}$ non e' derivabile).

Ad ogni modo, definita una funzione di ripartizione $F_{X}$, la densita' continua $f_{X}$ e' definita come
$$f_{X}(x) = F_{X}^{'}(x)$$
per ogni $x \in \mathbb{R}$ in cui $F_{X}$ e' derivabile. Negli altri punti, si pone $f_{X}$ in modo arbitrario.

### $Y = h(X)$
Sappiamo che se $X$ e' discreta, allora anche $Y = h(X)$ e' discreta (e' dimostrabile, ma lo diamo per assunto).

Se $X$ e' continua, allora $Y = h(X)$ puo' essere:
- [[variabile-aleatoria-discreta|discreta]];
- continua;
- [[variabile-aleatoria-mista|mista]].

Per ognuno di questi 3 casi, si vuole trovare la funzione di ripartizione $F_{Y}$ a partire da $F_{X}$, e in seguito da questa ottenere la densita' $f_{Y}$.

#### Caso discreto
Questo e' il caso facile, in cui da $X$ continua ottengo $Y$ discreta. In questo caso si deve avere che $Y$ assume un numero finito o numerabile di valori ($S_{Y}$).

Si procede calcolando di conseguenza i valori della densita' discreta $p_{Y}$, e da questi si calcola la funzione di ripartizione $F_{Y}$.

#### Caso continuo
Qui invece da $X$ continua ottengo $Y$ continua. Come calcolo la funzione di ripartizione $F_{Y}$?
Intanto noto che
$$F_{Y}(y) = \mathbb{P}(Y \leq y) = \mathbb{P}(h(X) \leq y)$$
e distinguo quindi i due casi:
- $h$ e' invertibile --> $F_{Y}(y)$ come $$F_{Y}(y) = \mathbb{P}(X \leq h^{-1}(y)) = F_{X}(h^{-1}(y))$$;
- $h$ non invertibile --> e' piu' complesso.

Infatti, in quest'ultimo caso _e' necessario stare attenti nel modo in cui i punti del supporto $S_{X}$ vengono mappati in $S_{Y}$_.

Per esempio, se $Y = X^{2}$, allora si avrà che $S_{Y} = [0, +\infty)$, e in particolare:
- $y < 0 \implies F_{Y}(y) = 0$;
- $y \geq 0 \implies F_{Y}(y) = \mathbb{P}(Y \leq y) = \mathbb{P}(X^{2} \leq y) = \mathbb{P}(-\sqrt{y} \leq X \leq \sqrt{y}) = F_{X}(\sqrt{y}) - F_{X}(-\sqrt{y})$

Prendiamo un altro esempio in cui $X$ è continua e definita dalla funzione di ripartizione
$$F_{X}(x) = \begin{cases} 0 & x \leq 0 \\ 1 - e^{-x} & x \geq 0 \end{cases}$$

<u>Nota bene</u>: in quanto $X$ continua, anche $F_{X}$ lo dovrà essere, per questo si sottolinea la doppia uguaglianza dei valori per $x = 0$.

Si chiede di determinare la funzione di ripartizione e la densità di $Y=e^{X}$. Procediamo definendo prima $F_{Y}$:
$$F_{Y}(y) = \mathbb{P}(Y \leq y) = \mathbb{P}(e^{X} \leq y)$$

Quindi, volendo passare per $F_{X}$, dobbiamo risolvere la disequazione $e^{X} \leq y$ per $X$. Distinguiamo i due casi:
- $y \leq 0 \implies \mathbb{P}(e^{X} \leq y) = \mathbb{P}(\varnothing) = 0$;
- $y > 0 \implies \mathbb{P}(e^{X} \leq y) = \mathbb{P}(X \leq \ln{y}) = F_{X}(\ln{y})$.

A questo punto usiamo la definizione di $F_{X}$:
$$F_{X}(\ln y) = \begin{cases} 0 & \ln{y} \leq 0 \\ 1 - e^{-\ln{y}} & \ln{y} \geq 0 \end{cases} = \begin{cases} 0 & 0 < y \leq 1 \\ 1 - \frac{1}{y} & y > 1 \end{cases}$$

In conclusione otteniamo come funzione di ripartizione $F_{Y}$
$$F_{Y}(y) = \begin{cases} 0 & y \leq 1 \\ 1 - \frac{1}{y} & y > 1 \end{cases}$$
e come densità continua $f_{Y}$
$$f_{Y}(y) = \begin{cases} 0 & y \leq 1 \\ \frac{1}{y^{2}} & y > 1 \end{cases}$$
dove abbiamo posto in modo arbitrario $f_{Y}(1) = 0$, in quanto 1 sarebbe il punto di congiunzione nella funzione di ripartizione.

#### Caso misto
%% Da completare %%

## Esempi
### Tempo di vita di una componente
Prendiamo $X$ variabile aleatoria continua che rappresenta il tempo di vita di una componente. La sua densita' continua e' definita come
$$f_{X}(x) = \begin{cases} 0 & x < 0 \\ e^{-x} & x \geq 0 \end{cases}$$

Vogliamo calcolare la funzione di ripartizione $F_{X}(x)$. Semplicemente integriamo la densita' continua su $(-\infty, x]$, spezzando l'integrale in due parti:
- per $x < 0$ --> l'integrale e' nullo, quindi $F_{X}(x) = 0$;
- per $x \geq 0$ --> l'integrale e' definito come $$F_{X}(x) = \int_{-\infty}^{x} f_{X}(y) \, dy = \int_{-\infty}^{0} f_{X}(y) \, dy + \int_{0}^{x} f_{X}(y) \, dy = 0 + \int_{0}^{x} e^{-y} \, dy = -[e^{-y}]_{0}^{x} = -e^{-x} + 1 = 1 - e^{-x}$$.

![[variabili-aleatorie-continue-1.png]]

## Referenze
- [[variabile-aleatoria-mista|Variabile aleatoria mista]]