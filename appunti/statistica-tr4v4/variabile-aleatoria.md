---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 20-03-2025 19:53:30
links:
  - "[[lecture-11032025132556|Lecture 11032025132556]]"
  - "[[lecture-18032025131728|Lecture 18032025131728]]"
---
# Variabile aleatoria
---
## Introduzione
> Una **variabile aleatoria** e' un'_affermazione riguardante l'ipotetico risultato di un [[esperimento-aleatorio|esperimento aleatorio]]_, che identifica uno e un solo [[numeri-reali|numero reale]] una volta noto l'esito dell'esperimento.
> Visto formalmente, in termini matematici si definisce come una [[funzione-matematica|funzione]]
> $$X: \Omega \to \mathbb{R}$$
> dove $\Omega$ e' lo [[spazio-campionario|spazio campionario]].

<u>Osservazione</u>: qualunque funzione da $\Omega$ a $\mathbb{R}$ e' una variabile aleatoria[^1].

### Esempio
Possiamo definire sull'esperimento del lancio di 2 dadi una variabile aleatoria del tipo
$$X = \text{la somma dei due lanci}$$
o le altre seguenti
$$Y = \text{il prodotto dei due lanci}$$
$$Z = \text{risultato del primo lancio}$$

A questo punto, definito lo spazio campionario come $\Omega = DR_{6,2} = \{(w_{1}, w_{2}) | w_{i} \in \{1, 2, 3, 4, 5, 6\}\}$, matematicamente le variabili aleatorie diventano:
$$X((w_{1}, w_{2})) = w_{1} + w_{2}$$
$$Y((w_{1}, w_{2})) = w_{1} \cdot w_{2}$$
$$Z((w_{1}, w_{2})) = w_{1}$$

## Proposizioni
### Uguaglianze
Valgono le seguenti 2 uguaglianze:
$$\mathbb{P}(X \leq x) = \mathbb{P}(X < x) + \mathbb{P}(X = x)$$
$$\mathbb{P}(X \leq x) = 1 - \mathbb{P}(X > x)$$

Questo significa che:
1. la [[probabilita|probabilita']] che un qualunque esito $w$ sia mappato da $X$ in un valore $\leq x (\in \mathbb{R})$ e' uguale alla probabilita' che sia mappato in un valore strettamente minore di $x$ piu' la probabilita' che sia mappato proprio in $x$;
2. la probabilita' che un qualunque esito $w$ sia mappato da $X$ in un valore $\leq x$ e' uguale a 1 meno la probabilita' che sia mappato in un valore strettamente maggiore di $x$;

#### Dimostrazione
Per definizione
$$X \leq x := \{w | X(w) \leq x\} \ \ \ \ \ \ \ X < x := \{w | X(w) < x\} \ \ \ \ \ \ \ X = x := \{w | X(w) = x\}$$

Sappiamo che il primo insieme e' l'unione dei due successivi. In altre parole, applicando la funzione di probabilita' $\mathbb{P}$ ad ambo le parti, si ha
$$\mathbb{P}(\{w | X(w) \leq x\}) = \mathbb{P}(\{w | X(w) < x\} \cup \{w | X(w) = x\})$$

Ora, per l'[[assiomi-della-probabilita|assioma di additivita']] si ha proprio:
$$\mathbb{P}(\{w | X(w) \leq x\}) = \mathbb{P}(\{w | X(w) < x\}) + \mathbb{P}(\{w | X(w) = x\})$$

**Qed**.

Per la seconda uguaglianza si procede allo stesso modo:
$$X \leq x := \{w | X(w) \leq x\} \ \ \ \ \ \ \ X > x := \{w | X(w) > x\}$$

Dalle proprieta' degli insiemi, risulta ovvio come il primo sia il complementare del secondo. Applicando $\mathbb{P}$ ad entrambi i membri, si ottiene
$$\mathbb{P}(\{w | X(w) \leq x\}) = \mathbb{P}(\{w | X(w) > x\}^{C})$$

Ora, per l'assioma del complemento, si ha proprio:
$$\mathbb{P}(\{w | X(w) \leq x\}) = 1 - \mathbb{P}(\{w | X(w) > x\})$$

**Qed**.

## Referenze
- [[variabile-aleatoria-costante|Variabile aleatoria costante]]
- [[variabile-aleatoria-indicatrice|Variabile aleatoria indicatrice]]
- [[eventi-generati-da-una-variabile-aleatoria|Eventi generati da una variabile aleatoria]]
- [[distribuzione-di-una-variabile-aleatoria|Distribuzione di una variabile aleatoria]]
- [[funzione-di-ripartizione|Funzione di ripartizione]]
- [[variabile-aleatoria-discreta|Variabile aleatoria discreta]]
- [[variabile-aleatoria-continua|Variabile aleatoria continua]]

[^1]: in realta' si dovrebbe dire che ogni funzione e' misurabile
