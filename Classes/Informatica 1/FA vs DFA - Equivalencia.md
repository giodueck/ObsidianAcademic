07-09-2022
---
# FA vs DFA - Equivalencia

L(DFA) = L(NFA)

*Doble inclusion*
Para todo DFA A existe un NFA B tal que L(B) = L(A)
Para todo NFA B existe un DFA A tal que L(A) = L(B)

**Los DFA son tan potentes como los NFA**

## Construccion de DFA a partir de NFA
Para todo NFA $B = (Q, \Sigma, \delta, q_0, F)$ existe un DFA $A = (Q_D, \Sigma, \delta_D, q_{0D}, F_D)$ tal que L(A) = L(B)

Dar un procedimiento para que a partir de un NFA se construya un DFA que reconozca el mismo lenguaje. Demostrar formalmente la correccion del procedimiento.

### Fundamentacion de un procedimiento
![[info-1-ej-nfa-2.png]]

### Definicion formal

Para todo NFA $B = (Q, \Sigma, \delta, q_0, F)$ existe un DFA $A = (Q_D, \Sigma, \delta_D, q_{0D}, F_D)$ tal que L(A) = L(B)

$Q_D = P(Q)$
$\delta_D(q_D, i) = \cup_{q \in q_D } \ \delta(qy, i)$
$q_{0D} = \{q_0\}$
$F_D = \{q_D \ | \ q_D \cap F \ne \emptyset\}$

### Demostracion
$\delta^*(\{q\}, x) = \delta^*(q, x)$

### Ejercicios tipo tema parcial
- Demostrar que L(FA) son cerrados respecto a la operacion "reversion"
	- Para todo FA A, existe un FA B, tal que $L(B) = L(A)^R$
- Demostrar que L(FA) son cerrados respecto a la operacion *
### Otros ejercicios
*En el PPT*
