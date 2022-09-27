20-09-2022
---
# PDA - NPDA
$L(DFA) \subset L(PDA)$
**NPDA: Non-deterministic Push Down Automaton**
$L(PDA) \subset L(NPDA)$

## Elementos
Un NPDA $A = (Q, \Sigma, \Gamma, \delta, q_0, Z_0, F)$

Q = conjunto de estados
$\Sigma$ = alfabeto de entrada
$\Gamma$ = alfabeto de pila (puede ser igual a $\Sigma$)
$\delta: Q \times (\Sigma \cup \{\varepsilon\}) \times \Gamma \rightarrow P_F(Q \times \Gamma^*)$ *$P_F$ denota un conjunto de partes donde los elementos sean finitos*
$q_0 \in Q$ *estado inicial*
$Z_0 \in \Gamma$ *simbolo inicial de pila, fondo de pila*
$F \subseteq Q$

### Funcion siguiente estado
Ejemplo
$\delta(q_0, b, \$) = \{<q_1, \$>, <q_4, \varepsilon>\}$

## Funcionamiento
Es identico al PDA excepto que
$<q, x, \varphi> \ \vdash \ <q', x', \varphi'>$ si $<q', \alpha> \in \delta(q, i, A)$

## Uso
Un NPDA $A = (Q, \Sigma, \Gamma, \delta, q_0, Z_0, F)$ reconoce una cadena $x \in \Sigma^*$ si y solo si
$<> \ \vdash \ <>$ #todo completar

## Definicion formal
#todo completar

## Ejercicios
#todo 

## Propiedades
#rodo
