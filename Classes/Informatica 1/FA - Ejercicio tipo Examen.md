23-08-2022
---
# FA - Ejercicio tipo Examen

## Enunciado
a) Diseñar (dibujar) un DFA $A = (Q, \Sigma, \delta, q_0, F)$ que reconozca $B = \{a^{2n} b^{3m}\ |\ n > 0, m \ge 0\}$, es decir que reconozca el lenguaje compuesto por pares de a's seguidas de triplas de b.

b) Demostrar **formalmente** que el diseño presentado en la parte a) es correcto

*Criterio de evaluacion:* En un examen, la puntuacion aproximada seria de 30% para la parte a) y para la parte b) de 70% multiplicada por la puntuacion dobtenida en la parte a).

## Parte a)
![[Pasted image 20220824150809.png]]

## Parte b)
$L(A) = B$
$B = \{a^{2n} b^{3m}\ |\ n > 0, m \ge 0\}$
Demostrar usando definicion de igualdad de conjuntos:
$L(A) \subseteq B \wedge B \subseteq L(A)$

$x \in L(A) \rightarrow x \in B$
$\wedge$
$x \in B \rightarrow x \in L(A)$

$\delta^*(q_0, x) \in F \rightarrow x \in B$
$\wedge$
$x \in B \rightarrow \delta^*(q_0, x) \in F$

*Por definicion de FA - Uso:*
$\forall x, \delta^*(q_0,x) \in F \rightarrow \exists n, m, n > 0, m \ge 0 \wedge x = a^{2n} b^{3m}$ (Parte \$)
$\wedge$
$\forall n, m, n > 0, m \ge 0 \wedge x = a^{2n} b^{3m} \rightarrow \delta^*(q_0,x) \in F$ (Parte \$\$)

### Parte \$\$: $B \subseteq L(A)$
$x = a^{2n} b^{3m}, n > 0, m \ge 0 \rightarrow \delta^*(q_0,x) \in F$

*Por sustitucion de variable x*
$\forall n > 0, m \ge 0, \delta^*(q_0, a^{2n} b^{3m}) \in F$

*Por division de casos (divide and conquer) (Definicion de FA - elementos)*
$\forall n > 0, m > 0, \delta^*(q_0, a^{2n} b^{3m}) = q_5$ *(Parte \$\$1)*
$\forall n > 0, \delta^*(q_0, a^{2n}) = q_2$ *(Parte \$\$2)*

*Por funcionamiento de DFA*
$\forall n > 0, \delta^*(q_0, a^{2n}) = q_2$ *(Parte \$\$1.1)*
$\forall m > 0, \delta^*(q_2, b^{3m}) = q_5$ *(Parte \$\$1.2)*

#### Demostracion \$\$1.1 y \$\$2
$\forall n > 0, \delta^*(q_0, a^{2n}) = q_2$ **Prueba inductiva**

*Caso base, n = 1*
$\delta^*(q_0, aa) = q_2$

**Demostracion**
*Por funcionamiento de DFA*
$\delta^*(q_0, aa) = \delta(\delta^*(q_0, a), a) = \delta(\delta(\delta^*(q_0, \varepsilon), a), a)$

*por transicion definida*
$\delta(\delta(q0, a), a) = \delta(q1, a)$

*por transicion definida*
$\delta(q1, a) = q2$

$\forall n > 0, \delta^*(q_0, a^{2n}) = q_2$

**Prueba inductiva**
*Caso inductivo*
$\delta^*(q_0, a^{2n}) = q_2 \rightarrow \delta^*(q_0, a^{2(n+1)} = q_2$
$\delta^*(q_0, a^{2(n+1)} = \delta^*(q_0, a^{2n}aa = \delta^*($**$\delta^*(q_0, a^{2n})$**$, aa)$
$= \delta^*(q_2, aa)$
$= \delta(\delta(q_2, a), a) = \delta(q_1, a) = q_2$

### Parte \$: $\delta^*(q_0, x) \in F \rightarrow x = a^{2n} b^{3m}, n > 0, m \ge 0$

*Utilizando el contrarreciproco*
$x \ne a^{2n} b^{3m}, n > 0, m \ge 0 \rightarrow \delta^*(q_0, x) \notin F$

*A partir de ahi se deberian convertir los $\ne$ en $=$*
$\forall w \in \{a, b\}^*$

1. $bw$
2. $a^{2n + 1} b^{3m}$
3. $a^{2n} b^{3m + 1}$
4. $a^{2n} b^{3m + 2}$
5. $\varepsilon$

**Demostracion parte \$**
$\delta^*(q_0, a^{2n + 1} b^{2m}) \notin F$
$\delta^*(q_0, a^{2n + 1} b^{2m}) = \delta^*(\delta^*(q_0,  a^{2n}), ab^{3m})$ *Por funcionamiento de DFA*
$= \delta^*(q_2, ab^{3m})$ *por \$\$1.1*
$= \delta^*(\delta(q_2, a), b^{3m})$ *Por funcionamiento de DFA*
$= \delta^*(q_1, b^{3m})$ *Por definicion de transicion*

*Como $q_1$ no es final, y como $\delta(q_1, b)$ no esta definido, queda demostrado que*
$\delta^*(q_0, a^{2n + 1} b^{2m}) \notin F$

> [!info] Repetir este proceso de demostracion para algunos patrones mas para terminar la demostracion