12-09-2022
---
# FA - $FA-\varepsilon$

Un FA no deterministico con transiciones que pueden activarse *sin necesitar procesar algun simbolo*. Estas transiciones se representan con $\varepsilon$, pero *$\varepsilon$ no es un simbolo* ni parte de algun alfabeto de entrada.

Las transiciones con $\varepsilon$ se activan sin importar el siguiente simbolo de entrada. Es necesariamente no deterministico, *todos los estados alcanzables sin procesar simbolos se activan* al mismo tiempo, *sin perder el estado actual*.

## Elementos
A $NFA-\varepsilon$ is a five-tuple:

$A = (Q, \Sigma, \delta, q_0, F)$

Q: A finite set of states
$\Sigma$: A finite input alphabet
$q_0$: Initial state in Q
F: A set of final/accepting states, which is a subset of Q ($F \subseteq Q$)
$\delta$: A transition function (next-state function)
$\delta: Q \times (\Sigma \cup \{\varepsilon\}) \rightarrow P(Q)$ *Power set of Q*

## Funcionamiento
*Funcion auxiliar*:
$CLAUSURA_\varepsilon$: $Q \rightarrow P(Q)$

$CLAUSURA_\varepsilon (q)$:
$q \in CLAUSURA_\varepsilon (q)$ *Caso base*
$q' \in CLAUSURA_\varepsilon(q) \wedge q'' \in \delta(q', \varepsilon) \rightarrow q'' \in CLAUSURA_\varepsilon(q)$ *Caso inductivo*

### Definicion
$\delta^*(q, \varepsilon) = CLAUSURA(q)$ *Caso base*

$q'' \in \delta(q', i) \rightarrow \delta^*(q, xi) = \cup_{q' \in \delta^*(q, x)} \delta(q', i) \cup CLAUSURA(q'')$
$x \in \Sigma^*, i \in \Sigma$ *Caso inductivo*

## Uso
#### Cadena reconocida si y solo si
$x \in \Sigma^* \ | \ \delta^*(q_0, x) \ \cap \ F \ne \emptyset$

#### Lenguaje reconocido
Esta formado por todas las cadenas reconocidas
si A es una $NFA_\varepsilon$, entonces L(A)
L(A) = {x | x es reconocido por A}