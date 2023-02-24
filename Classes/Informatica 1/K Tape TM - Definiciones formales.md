17-10-2022
---
# K Tape TM - Definiciones formales

## Elementos
Un TM $M = <Q, \Sigma, \Gamma, \delta, q_0, Z_0, F>$

Q = Conjunto finito de estados
$\Sigma$ = Alfabeto de entrada, $\textblank \in \Sigma$
$\Gamma$ = Alfabeto de memoria, $\textblank \in \Gamma$ *(puede ser igual a $\Sigma$)*
$\delta: (Q-F) \times \Sigma \times \Gamma^k \rightarrow Q \times \Gamma^k \times \{R, L, S\} \times \{R, L, S\}^k$
$q_0 \in Q$ *(estado inicial)*
$Z_0 \in \Gamma$ *(simbolo inicial de las cintas de memoria)*
$F \subseteq Q$

*Ejemplo de $\delta$:*
$\delta(q, a, Z_0, B, C) = \ <q', Z_0, A, R< S, L, R>$

## Funcionamiento
Teniendo en cuenta la cinta de input + 2 cintas de memoria
Configuracion:
$<q, x \uparrow iy, \alpha_1 \uparrow A_1 \beta_1, \alpha_2 \uparrow A_2 \beta_2>, \alpha_1, \alpha_2, \beta_1, \beta_2 \in \Gamma^*, A_1, A_2 \in \Gamma$

Ejemplo:
```
q:
a  b  b  b  b  a
      ^
Z0 A  C  B
   ^
Z0 B  B
      ^
```
Se representa como:
$<q, ab \uparrow bbba, Z_0 \uparrow ABC, Z_0 B \uparrow B>$

*Generalizando:*
$<q, x \uparrow iy, \alpha_1 \uparrow A_1 \beta_1, \alpha_2 \uparrow A_2 \beta_2, ..., \alpha_k \uparrow A_k \beta_k>$

### Transicion
$<q, x \uparrow iy, \alpha_1 \uparrow A_1 \beta_1, \alpha_2 \uparrow A_2 \beta_2> \ \vdash \ <q', x' \uparrow i'y', \alpha_1' \uparrow A_1' \beta_1', \alpha_2' \uparrow A_2' \beta_2'>$
a traves de $\delta(q, i, A_1, A_2) = \ <q, B_1, B_2, M_i, M_1, M_2>$

Para la entrada:
*si $M_i = L$*
$x = x'i'$
$y' = iy$

*si $M_i = S$*
$x' = x$
$y' = y$
$i' = i$

*si $M_i = R$*
$x' = xi$
$y = i'y'$

Para las cintas de memoria:
*si $M_j = L,j = (1, 2)$*
$\alpha_j = \alpha_j'A_j'$
$\beta_j' = B_j \beta_j$

*si $M_j = S, j = (1, 2)$*
$\alpha_j' = \alpha_j$
$\beta_j' = \beta_j$
$A_j' = B_j$

*si $M_j = L,j = (1, 2)$*
$\alpha_j' = \alpha_jB_j$
$\beta_j = A_j' \beta_j'$ 

## Uso
Configuracion inicial: $<q0, \uparrow x, \uparrow Z_0, \uparrow Z_0>$
$x \in \Sigma^*$
x es reconocida si y solo si

$<q_0, \uparrow x, \uparrow Z_0, \uparrow Z_0> \ \vdash^* \ <q_f, x' \uparrow i'y', \alpha_1 \uparrow A_1B_1, \alpha_2 \uparrow A_2B_2>$
$q_f \in F$

El lenguaje reconocido es el conjunto de todas las cadenas reconocidas

## Ejercitario TM 
- Definicion formal estilo JFLAP
- Modificar definicion TM para que primero se mueva el cabezal y luego se escriba
- Simular un DFA por medio de una TM
- Simular un PDA por medio de una TM
- Simular un NPDA por medio de una TM
