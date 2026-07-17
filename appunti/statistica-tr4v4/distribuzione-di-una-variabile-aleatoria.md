---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 22-03-2025 16:56:58
links:
  - "[[lecture-11032025132556|Lecture 11032025132556]]"
  - "[[lecture-18032025131728|Lecture 18032025131728]]"
---
# Distribuzione di una variabile aleatoria
---
## Introduzione
> Sia $(\Omega, \mathbb{P})$ uno [[spazio-di-probabilita|spazio di probabilita']] e $X: \Omega \to \mathbb{R}$ una [[variabile-aleatoria|variabile aleatoria]], allora si definisce **distribuzione (o legge) di $X$** la [[probabilita|probabilita']]
> $$\mathbb{P}_{X}: \mathscr{P}(\mathbb{R}) \to [0, 1]$$
> definita come
> $$\mathbb{P}_{X}(B) := \mathbb{P}(X^{-1}(B)) = \mathbb{P}(X \in B) \ \ \ \ \ \ \ \forall B \subseteq \mathbb{R}$$
> e si scrive
> $$X \sim \mathbb{P}_{X}$$
> ovvero "$X$ ha la legge $\mathbb{P}_{X}$".

<u>Nota bene</u>: si tratta fondamentalmente della _probabilita' degli eventi generati dalla variabile aleatoria $X$ su un certo sottoinsieme di $\mathbb{R}$_.

Tale distribuzione è comoda: _ci consente di lavorare con insiemi reali per determinare le probabilità degli eventi_! Con le probabilità su $\mathbb{R}$, infatti, posso lavorare sugli intervalli sfruttando la sua [[proprieta-di-completezza-di-r|proprietà del continuo]].

## Probabilità
Vogliamo ora dimostrare che la distribuzione $\mathbb{P}_{X}$ per una qualunque variabile aleatoria $X$ è una funzione di probabilità.

### Dimostrazione
Affinché ciò avvenga è sufficiente verificare i 3 [[assiomi-della-probabilita|assiomi]], in quanto le altre proprietà sono solo delle conseguenze di questi:
1. $$0 \leq \mathbb{P}_{X}(B) \leq 1 \ \ \ \forall B \subseteq \mathbb{R}$$ questo è ovvio, in quanto per definizione $\mathbb{P}_{X}(B) = \mathbb{P}(X \in B)$, e $\mathbb{P}$ è una funzione di probabilità;
2. $$\mathbb{P}_{X}(\mathbb{R}) = 1$$ ovvero $\mathbb{P}(X \in \mathbb{R})$, quindi $\mathbb{P}(\Omega)$, pari a 1 per l'assioma su $\mathbb{P}$;
3. $$(A_{n})_{n \in \mathbb{N}} : A_{i} \cap A_{j} = \varnothing \ \ \ \forall i \neq j \ \ \ \implies \ \ \ \mathbb{P}_{X}\left(\bigcup_{n=1}^{+\infty} A_{n}\right) = \sum\limits_{n=1}^{+\infty} \mathbb{P}_{X}(A_{n})$$ per cui devo dimostrare $\mathbb{P}(X \in \bigcup_{n=1}^{+\infty} A_{n}) = \sum\limits_{n=1}^{+\infty} \mathbb{P}(X \in A_{n})$; per fare ciò, è sufficiente dimostrare che presi due sottoinsiemi $A_{i}, A_{j}$ disgiunti di $\mathbb{R}$, gli insiemi $\{X \in A_{i}\}$ e $\{X \in A_{j}\}$ sono disgiunti; ma questo e' ovvio in quanto $X$ e' una funzione;

**Qed**.

## Casi
Vediamo come si comporta la distribuzione $\mathbb{P}_{X}$ nei due casi fondamentali: [[variabile-aleatoria-costante|variabile aleatoria costante]] e [[variabile-aleatoria-indicatrice|variabile aleatoria indicatrice]].

### Variabile aleatoria costante
Se $X$ e' costante, allora si fissa un $a \in \mathbb{R}$ tale che $X(w) = a \ \ \ \forall w \in \Omega$. Vogliamo determinare $\mathbb{P}_{X}$ per un certo $B \subseteq \mathbb{R}$:
$$\mathbb{P}_{X}(B) = \mathbb{P}(X \in B) = \mathbb{P}(a \in B) = \begin{cases} 1 & a \in B \\ 0 & a \notin B \end{cases}$$

<u>Nota bene</u>: questo e' lo stesso risultato degli [[eventi-generati-da-una-variabile-aleatoria-variabili-aleatorie-costanti|eventi generati da una variabile aleatoria costante]] ($X \in B$), ma di cui calcoliamo la probabilita'!

Questa notazione coincide esattamente con la [[delta-di-dirac|delta di Dirac]] per $a$:
$$\mathbb{P}_{X}(B) = \delta_{a}(B)$$

### Variabile aleatoria indicatrice
Se $X$ e' indicatrice, allora fissato un evento $A \subseteq \Omega$ si ha che $X(w) = \begin{cases} 1 & w \in A \\ 0 & w \notin A \end{cases}$. Vogliamo determinare $\mathbb{P}_{X}$ per un certo $B \subseteq \mathbb{R}$:
$$\mathbb{P}_{X}(B) = \mathbb{P}(X \in B) = \begin{cases} \mathbb{P}(A) & 1 \in B \land 0 \notin B \\ 1 - \mathbb{P}(A) & 1 \notin B \land 0 \in B \\ 1 & 1 \in B \land 0 \in B \\ 0 & 1 \notin B \land 0 \notin B \end{cases}$$

Anche questa distribuzione puo' essere raccolta e definita usando le delta di Dirac:
$$\mathbb{P}_{X}(B) = \mathbb{P}(A)\delta_{1}(B) + (1 - \mathbb{P}(A))\delta_{0}(B)$$

Si dimostra, infatti, che **ogni distribuzione di probabilita' puo' sempre essere scritta come una [[combinazione-lineare|combinazione lineare]] di delta di Dirac**.

## Osservazione
Conoscere $\mathbb{P}_{X}(B) \ \ \ \forall B \subseteq \mathbb{R}$ equivale a conoscere la distribuzione su ogni intervallo $I$ di $\mathbb{R}$ (perche' ogni intervallo e' un sottoinsieme). In particolare ci interessa conoscere $\mathbb{P}_{X}((-\infty, x]) \ \ \ x \in \mathbb{R}$: [[funzione-di-ripartizione|funzione di ripartizione]]. Si dimostra, infatti, che **la distribuzione di una variabile aleatoria $X$ e' caratterizzata da una funzione $F_{X}$** (la funzione di ripartizione).

Infatti, $\mathbb{P}_{X}$ contiene tutte le informazioni di $X$, ma ha come dominio dei sottoinsiemi: e' estremamente scomoda da usare. Si preferisce lavorare con la funzione di ripartizione.

## Referenze