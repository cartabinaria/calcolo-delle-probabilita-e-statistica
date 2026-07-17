---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 14-04-2025 21:16:19
links:
  - "[[lecture-01042025132135|Lecture 01042025132135]]"
---
# Distribuzione di Poisson
---
## Introduzione
> La **distribuzione di Poisson** e' una [[distribuzioni-notevoli-di-variabili-aleatorie-discrete|distribuzione notevole]] su [[variabile-aleatoria-discreta|variabile aleatoria discreta]] $X$ che _modella il numero di eventi che si verificano in un intervallo di tempo o spazio fisico_.
> In tal caso, si dice che $X$ ha la legge di Poisson, e si indica
> $$X \sim Poi(\lambda), \ \ \ \lambda > 0$$

Si tratta di un caso limite della [[distribuzione-binomiale|distribuzione binomiale]], ossia quando $n \to +\infty$ e $p \to 0$. In tal caso si raggruppano questi due parametri in un unico parametro
$$\lambda = np$$.

### Definizione
Si ha che il supporto $S_{X}$ e' infinito [[numerabilita|numerabile]], e di conseguenza la [[densita-discreta|densita' discreta]] non puo' essere scritta in forma tabellare.

In particolare:
- $S_{X} = \mathbb{N}$;
- $p_{X}(k) = e^{-\lambda} \frac{\lambda^{k}}{k!}$.

Bisognerebbe dimostrare che $p_{X}$ sia effettivamente una densita', e in particolare che
$$\sum\limits_{k=0}^{+\infty} \frac{\lambda^{k}}{k!} = e^{\lambda}$$
(affinche' la sommatoria delle densita' discrete sul supporto faccia 1). Ma questo e' vero: si tratta dello [[polinomi-di-taylor|sviluppo in serie di Taylor dell'esponenziale]]!

## Proprieta'
### Valore atteso
Il [[valore-atteso|valore atteso]] di una variabile aleatoria discreta con distribuzione di Poisson e' dato da
$$\mathbb{E}[X] = \lambda$$

### Varianza
La [[varianza|varianza]] di una variabile aleatoria discreta con distribuzione di Poisson e' data da
$$Var(X) = \lambda$$

## Referenze