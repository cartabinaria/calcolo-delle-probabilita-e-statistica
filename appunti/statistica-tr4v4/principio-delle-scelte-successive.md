---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 28-03-2025 12:20:49
links:
  - "[[lecture-07032025131750|Lecture 07032025131750]]"
  - "[[lecture-14032025131849|Lecture 14032025131849]]"
---
# Principio delle scelte successive
---
## Introduzione
> Il **principio (o metodo) delle scelte successive** (o **P/MSS**) e' uno schema usato nel [[calcolo-combinatorio|calcolo combinatorio]] per calcolare la [[cardinalita|cardinalita']] di un [[insieme|insieme]]. Esso afferma che supponendo che ciascun elemento di un insieme $A$ possa essere determinato da una e una sola sequenza di $k$ scelte successive, in cui ogni scelta viene effettuata tra un numero fissato di possibilita' $n_{1}, \cdots, n_{k}$ (indipendenti tra loro) tale che:
> - la prima scelta viene effettuata tra $n_{1}$ possibilita';
> - ...
> - la $k$-esima scelta viene effettuata tra $n_{k}$ possibilita';
> 
> allora la cardinalita' di $A$ e' pari a
> $$|A| = n_{1} \cdot \ldots \cdot n_{k}$$

## Esempi
### Password
Su un alfabeto di 36 caratteri $\{a, \cdots, z, 0, \cdots, 9\}$ (alfanumerico), quante password di 8 caratteri possono essere generate? In breve, dobbiamo calcolare la cardinalita' dello [[spazio-campionario|spazio campionario]]
$$\Omega = \{1, \cdots, 36\}^{8}$$
(dove $\cdot^{8}$ significa che e' in [[prodotto-cartesiano|prodotto cartesiano]] con se stesso 8 volte).

Applichiamo il PSS, elencando le $k=8$ possibili scelte:
1. scelgo uno tra i 36 caratteri possibili --> $n_{1} = 36$;
2. scelgo uno tra i 36 caratteri possibili --> $n_{2} = 36$;
3. scelgo uno tra i 36 caratteri possibili --> $n_{3} = 36$;
4. scelgo uno tra i 36 caratteri possibili --> $n_{4} = 36$;
5. scelgo uno tra i 36 caratteri possibili --> $n_{5} = 36$;
6. scelgo uno tra i 36 caratteri possibili --> $n_{6} = 36$;
7. scelgo uno tra i 36 caratteri possibili --> $n_{7} = 36$;
8. scelgo uno tra i 36 caratteri possibili --> $n_{8} = 36$.

Di conseguenza
$$|\Omega| = n_{1} \cdot n_{2} \cdot n_{3} \cdot n_{4} \cdot n_{5} \cdot n_{6} \cdot n_{7} \cdot n_{8} = 36^{8}$$

Se invece volessimo calcolare il numero di password che non contengono ripetizioni, applicheremmo il principio, sempre tra $k = 8$ scelte, nel seguente modo:
1. scelgo uno tra i 36 caratteri possibili --> $n_{1} = 36$;
2. scelgo uno tra i 35 caratteri possibili (_devi escludere quello usato prima_!) --> $n_{2} = 35$;
3. scelgo uno tra i 34 caratteri possibili --> $n_{3} = 34$;
4. scelgo uno tra i 33 caratteri possibili --> $n_{4} = 33$;
5. scelgo uno tra i 32 caratteri possibili --> $n_{5} = 32$;
6. scelgo uno tra i 31 caratteri possibili --> $n_{6} = 31$;
7. scelgo uno tra i 30 caratteri possibili --> $n_{7} = 30$;
8. scelgo uno tra i 29 caratteri possibili --> $n_{8} = 29$.

Di conseguenza
$$|\Omega| = 36 \cdot 35 \cdot 34 \cdot 33 \cdot 32 \cdot 31 \cdot 30 \cdot 29 = \frac{36!}{28!} = \frac{36!}{(36 - 8)!}$$

### Poker
Consideriamo ora un mazzo di carte francesi, ossia 52 carti composte da 13 numeri $\times$ 4 semi. Vogliamo determinare la cardinalita' di $A$ insieme dei _full_: un sottoinsieme di 5 carte costituito dall'unione di un tris e di una coppia.

Procediamo con il PSS, considerando 4 scelte:
1. scelgo il numero del tris, tra i 13 possibili --> $n_{1} = 13$;
2. scelgo il seme del tris, tra i 4 possibili (perche' per ogni tris di carte, le combinazioni di 3 semi ne escludono sempre 1, per cui i semi esclusi in totale saranno 4) --> $n_{2} = 4$;
3. scelgo il numero della coppia, tra i 12 possibili (non posso usare lo stesso numero del tris!) --> $n_{3} = 12$;
4. scelgo il seme della coppia, tra i 6 possibili ($\{\{c, p\}, \{c, q\}, \{c, f\}, \{p, q\}, \{p, f\}, \{q, f\}\}$) --> $n_{4} = 6$.

Di conseguenza
$$|A| = 13 \cdot 4 \cdot 12 \cdot 6 = 3744$$

Ci chiediamo adesso, di calcolare l'insieme delle _doppie coppie_: un sottoinsieme di 5 carte costituito da due coppie diverse e una carta libera.

Verrebbe da ragionare come nel caso precedente, quindi considerando le seguenti 6 scelte:
1. scelgo il numero della prima coppia, tra i 13 possibili --> $n_{1} = 13$;
2. scelgo il seme della prima coppia, tra i 6 possibili --> $n_{2} = 6$;
3. scelgo il numero della seconda coppia, tra i 12 possibili --> $n_{3} = 12$;
4. scelgo il seme della seconda coppia, tra i $6$ possibili --> $n_{4} = 6$;
5. scelgo il numero della carta libera, tra i 11 possibili --> $n_{5} = 11$;
6. scelgo il seme della carta libera, tra i 4 possibili --> $n_{6} = 4$.

Seguendo questo ragionamento verrebbe
$$|A| = 13 \cdot 6 \cdot 12 \cdot 6 \cdot 11 \cdot 4 = 247104$$
ma **il risultato e' errato**! Infatti stiamo assumendo che ci sia un ordine nell'uscita delle due coppie: consideriamo due casi separati l'uscita della prima coppia $x$ e poi la coppia $y$ rispetto all'uscita della prima coppia $y$ e poi la coppia $x$. Questi due casi devono collassare, invece.

Di conseguenza, il risultato reale va semplicemente diviso per 2:
$$|A| = 123552$$

<u>Nota bene</u>: questo ragionamento non si applica nel caso del full, perche' tris e coppia non sono interscambiabili; l'ordine di uscita non e' influente perche' il fatto stesso che si tratti di "oggetti" differenti fa collassare tutte le possibili configurazioni dell'ordine delle carte in $\{tris, coppia\}$. Invece due coppie sono lo stesso oggetto, per cui se non si fa attenzione si rischia di considerare doppiamente il caso $\{coppia1, coppia2\}$, in quanto distinto da $\{coppia2, coppia1\}$.

## Costrutti
Questo metodo funziona, ma e' lungo e non ci consente di generalizzare i calcoli e di fornirci strumenti per fare i calcoli in modo sistematico. Per questo si identificano, a partire dal PSS, i seguenti costrutti:
- [[disposizione-semplice|Disposizione semplice]] o [[disposizione-con-ripetizione|con ripetizione]] + [[permutazione|Permutazione]];
- [[combinazione|Combinazione]].

### Schema
Possiamo riassumere i principali costrutti nel seguente schema:
![[tabella-combinatoria.png]]

<u>Osservazione</u>: si osserva come in realta' la combinazione, in quanto composta matematicamente dalla disposizione, non sia essenziale. In altre parole _si potrebbe usare $D_{n,k}$ anche per estrazioni che non considerano l'ordine_.

Si nota, nello schema, un pezzo mancante: l'_insieme che tiene ammette ripetizioni ma non tiene conto dell'ordine_. Di fatto questo insieme non e' di particolare interesse, perche' _nella realta' ci sono poche situazioni modellizzabili con esso_. Anzi, spesso e' l'insieme che rischia di far cadere in tranello nel calcolo di alcune probabilita'[^1].

Tuttavia, il caso mancante e' comunque importante in certi ambiti, e la sua distribuzione prende il nome di [[distribuzione-binomiale|distribuzione binomiale]], cui [[probabilita|probabilita']] e' detta [[probabilita-binomiale|probabilita' binomiale]].

## Referenze

[^1]: si pensi al lancio di due dadi e alla probabilita' di uscita della coppia $(1, 1)$ e della coppia $(1, 3)$.
