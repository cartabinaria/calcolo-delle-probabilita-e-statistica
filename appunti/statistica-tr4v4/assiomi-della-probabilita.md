---
tags:
  - category/note
  - status/finished
  - topic/calcolo-delle-probabilità-e-statistica
date: 24-02-2025 17:28:05
links:
  - "[[lecture-21022025131008|Lecture 21022025131008]]"
---
# Assiomi della probabilita'
---
## Introduzione
> Gli **assiomi della probabilita'** sono:
> - _assioma I_ --> a ciascun sottoinsieme $A$ di $\Omega$ ([[spazio-campionario|spazio campionario]]) e' assegnato un numero $\mathbb{P}(A)$ che verifica $$0 \leq \mathbb{P}(A) \leq 1$$, che si chiama **probabilita'** dell'[[evento|evento]] $A$;
> - _assioma II_ --> $$\mathbb{P}(\Omega) = 1$$
> - _assioma III_ --> vale la **$\sigma$-additivita'** (o **additivita' numerabile**), ovvero $$(A_{n})_{n \in \mathbb{N}} : A_{i} \cap A_{j} = \varnothing \ \ \ \forall i \neq j \ \ \ \implies \ \ \ \mathbb{P}\left(\bigcup_{n=1}^{+\infty} A_{n}\right) = \sum\limits_{n=1}^{+\infty} \mathbb{P}(A_{n})$$, o in altre parole _la probabilita' dell'unione di eventi disgiunti e' la somma delle probabilita' dei singoli eventi_.

## Conseguenze
Le principali conseguenze degli assiomi della probabilita' si riassumono nel seguente teorema:
> Sia $\Omega$ spazio campionario e $\mathbb{P}$ funzione di probabilita' su $\Omega$ (quindi $(\Omega, \mathbb{P})$ [[spazio-di-probabilita|spazio di probabilita']]), dagli assiomi I, II e III deduciamo che:
> 1. $$\mathbb{P}(\varnothing) = 0$$
> 2. **additivita' finita**, ovvero $$(A_{i})_{i=1, \cdots, n} : A_{i} \cap A_{j} = \varnothing \ \ \ \forall i \neq j \ \ \ \implies \ \ \ \mathbb{P}\left(\bigcup_{i=1}^{n} A_{i}\right) = \sum\limits_{i=1}^{n} \mathbb{P}(A_{i})$$
> 3. **complementare**, ovvero $$\mathbb{P}(A^{C}) = 1 - \mathbb{P}(A)$$
> 4. **monotonia**, ovvero $$A, B : A \subseteq B \implies \mathbb{P}(A) \leq \mathbb{P}(B)$$

### Dimostrazione
#### 1.
Per dimostrare $\mathbb{P}(\varnothing) = 0$ uso la $\sigma$-additivita'. Mi costruisco quindi una successione $(A_{n})_{n \in \mathbb{N}}$ di insiemi disgiunti, tale che
$$A_{i} = \varnothing \ \ \ \forall i \in \mathbb{N}$$
che mantiene la disgiunzione in quanto $\varnothing \cap \varnothing = \varnothing$.
Adesso osservo che
$$\bigcup_{n=1}^{+\infty}A_{i} = \bigcup_{n=1}^{+\infty} \varnothing = \varnothing$$
per cui, per la $\sigma$-additivita',
$$\mathbb{P}\left(\bigcup_{n=1}^{+\infty} A_{i}\right) = \sum\limits_{n=1}^{+\infty} \mathbb{P}(A_{i}) = \sum\limits_{n=1}^{+\infty} \mathbb{P}(\varnothing)$$

Percio', abbiamo che
$$\sum\limits_{n=1}^{+\infty} \mathbb{P}(\varnothing) = \mathbb{P}(\varnothing)$$
e per via dell'assioma I, bisogna avere che
$$\sum\limits_{n=1}^{+\infty} \mathbb{P}(\varnothing) \in [0, 1]$$
Quindi, tra i 2 seguenti casi
$$\sum\limits_{n=1}^{+\infty} \mathbb{P}(\varnothing) = \begin{cases}
+\infty & \mathbb{P}(\varnothing) > 0 \\
0 & \mathbb{P}(\varnothing) = 0
\end{cases}$$

soltanto il secondo e' accettato. Ergo $\mathbb{P}(\varnothing)$ deve essere $0$.

**Qed.**

#### 2.
Per dimostrare l'additivita' finita, sfrutto l'additivita' numerabile. In particolare fisso una successione finita di insiemi disgiunti $(A_{i})_{i=1, \cdots, n}$. Quindi mi creo una successione $(B_{n})_{n \in \mathbb{N}}$ tale che
$$\begin{cases}
B_{i} = A_{i} & i \leq n \\
B_{i} = \varnothing & i > n
\end{cases}$$

Ora, l'additivita' numerabile mi dice che
$$\mathbb{P}\left(\bigcup_{n=1}^{+\infty} B_{n}\right) = \sum\limits_{n=1}^{+\infty} \mathbb{P}(B_{n})$$
Ma, per come la successione $B_{n}$ e' stata costruita, si ha proprio che
$$\bigcup_{n=1}^{+\infty} B_{n} = \bigcup_{i=1}^{n} A_{i}$$
e
$$\sum\limits_{n=1}^{+\infty} \mathbb{P}(B_{n}) = \sum\limits_{i=1}^{n} \mathbb{P}(A_{i}) + \sum\limits_{i=n+1}^{+\infty} \mathbb{P}(\varnothing)$$
che, dalla proposizione precedente ($\mathbb{P}(\varnothing) = 0$), equivale a
$$\sum\limits_{n=1}^{+\infty} \mathbb{P}(B_{n}) = \sum\limits_{i=1}^{n} \mathbb{P}(A_{i})$$

Riunendo le parti si ottiene proprio
$$\mathbb{P}\left(\bigcup_{i=1}^{n} A_{i}\right) = \sum\limits_{i=1}^{n} \mathbb{P}(A_{i})$$
**Qed.**

#### 3.
Per dimostrare il complementare, possiamo usare il secondo assioma ($\mathbb{P}(\Omega) = 1$). Infatti, risulta ovvio che
$$A \cup A^{C} = \Omega$$
da cui
$$\mathbb{P}(A \cup A^{C}) = 1$$

Ora, per l'additivita' finita appena dimostrata, sappiamo che
$$\mathbb{P}(A \cup A^{C}) = \mathbb{P}(A) + \mathbb{P}(A^{C}) = 1$$
da cui
$$\mathbb{P}(A^{C}) = 1 - \mathbb{P}(A)$$

**Qed**.

#### 4.
Per dimostrare la monotonia, sfruttiamo l'equivalenza seguente:
$$A \subseteq B \implies A \cup B \setminus A = B$$
A questo punto, vale allora
$$\mathbb{P}(A \cup B \setminus A) = \mathbb{P}(B)$$
da cui, per l'additivita' finita
$$\mathbb{P}(A) + \mathbb{P}(B \setminus A) = \mathbb{P}(B)$$

Di conseguenza, essendo per il primo assioma $\mathbb{P}(B \setminus A) \geq 0$, allora concludo che
$$\mathbb{P}(A) \leq \mathbb{P}(B)$$

**Qed.**

## Referenze
- [[probabilita-dell-unione-non-disgiunta-di-eventi|Probabilita' dell'unione non disgiunta di eventi]]