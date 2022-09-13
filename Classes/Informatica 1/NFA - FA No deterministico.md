06-09-2022
---
# NFA - Non-deterministic FA

Permiten que de un estado pueda accederse a mas de un estado.

## Ejemplo
Diseñar un FA que reconozca cualquier cadena en $\{0, 1\}^*$ que termine en 0100.

#### DFA
![[info1-eg-dfa.png]]

#### NFA
![[info1-eg-nfa.png]]

Una cadena puede terminar en varios estados. Si al menos uno es final, la cadena es reconocida.

## Caracteristicas generales
- Desde un estado podemos ir a mas de un estado
- El movimiento de cada una de las "ramas" es independiente a las otras
- No por llegar al mismo estamos estamos mas "presentes" en algun estado
- Una "rama" se detiene independientemente de las demas (delta indefinida)
- Se reconoce la cadena cuando se llega por lo menos a un estado final, partiendo del estado final y leyendo toda la cadena

## Definicion formal
### Elementos
$A = (Q, \Sigma, \delta, q_0, F)$

$Q$ is a *finite* set of states
$\Sigma$ is a *finite* input slphabet
$q_0$ is the initial/starting state, $q_0 \in Q$
$F$ is a set of final/accepting states, $F \subseteq Q$
$\delta$ is a transition function

$\delta: (Q \times \Sigma) \rightarrow P(Q)$ *Power set of Q*
*$P(Q) = \{z \ | \ z \subseteq Q\}$*

e.g.:
$\delta(q_0, a) = \{q_1, q_2\}$
$\delta(q_1, b) = \{q_1\}$
$\delta(q_4, b) = \emptyset$ *(mejor llamarle indefinido que vacio)*
$...$

### Funcionamiento
Se puede extender la funcion $\delta$ al dominio $Q \times \Sigma^*$ de la siguiente forma:
Sea $\delta^*: Q \times \Sigma^* \rightarrow P(Q)$ tal que

$\delta^*(q, \varepsilon) = \{q\}$ *(caso base)*

$\delta^*(q, xi) = \cup_{q' \in \delta^*(q, x)} \delta(q', i)$
$x \in \Sigma^*, i \in \Sigma$ *(caso inductivo)*

### Uso
#### Cadena reconocida si y solo si
$x \in \Sigma^* \ | \ \delta^*(q_0, x) \ \cap \ F \ne \emptyset$

#### Lenguaje reconocido
Esta formado por todas las cadenas reconocidas
si A es una NFA, entonces L(A)
L(A) = {x | x es reconocido por A}

## Propiedad general de funcionamiento
### DFA
$\delta^*(q, x) = q' \wedge \delta^*(q', y) = q'' \rightarrow \delta^*(q, xy) = q''$

### NFA
$q' \in \delta^*(q, x) \wedge q'' \in \delta^*(q', y) \rightarrow q'' \in \delta^*(q, xy)$

## Ejercicio FA (no deterministico) #todo 
FA que reconoce cualquier cadena de $\{0, 1\}^*$ que termina con 111

### Demostracion de correccion
$L(A) = \{0, 1\}^*111$
- $L(A) \subseteq \{0, 1\}^*111$
- $\{0, 1\}^*111 \subseteq L(A)$
