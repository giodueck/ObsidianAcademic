23-08-2022
---
# FA - Definiciones formales

## Elementos (Dibujo)
A DFA is a five-tuple:
$A = (Q, \Sigma, \delta, q_0, F)$

Q: A finite set of states
$\Sigma$: A finite input alphabet
$q_0$: Initial state in Q
F: A set of final/acceptinf states, which is a subset of Q ($F \subseteq Q$)
$\delta$: A transition function (next-state function)

$\delta: (Q \times \Sigma) \rightarrow Q$
$\delta(q,i)=q'$

#### Ejemplo
Q = {q0, q1, q2, q3}
$\Sigma = \{a, b\}$
$F = \{q3\}$
$q_0=q0$

$\delta(q0,a)=q2$
$\delta(q0,b)=q1$
...

## Funcionamiento
Queremos describir el comportamiento:
$\delta^*(q_1, abbb) = \delta(\delta(\delta(\delta(q_1, a), b), b), b)$

Sea $\delta^*=Q \times \Sigma^* \rightarrow Q$ tal que
$\delta^*(q,\varepsilon)=q;$ *(caso base)*
$\delta^*(q,xi)=\delta(\delta(q,x), i), x \in \Sigma^*, i \in \Sigma$ *(caso inductivo)*

#### Ejemplo
$\delta^*(q,aabbb)=\delta(\delta^*(q,aabb),b)$
$\delta(\delta^*(q,aabbb)=\delta(\delta(\delta^*(q,aab), b),b)$
...
$\delta(\delta^*(q,aabbb)=\delta(\delta(\delta(\delta(\delta(\delta^*(q,\varepsilon),a), a), b), b),b)$ *(se encuentra el caso base)*
$\delta(\delta^*(q,aabbb)=\delta(\delta(\delta(\delta(\delta(q,a), a), b), b),b)$

### Conclusiones
- No se mueve mientras no recibe nada
- No se detiene mientras no recibe nada (no para de funcionar)
- Procesa la cadena tomando un simbolo a la vez
- Procesa la cadena de izquierda a derecha
- Si una transicion esta indefinida, el automara se detiene definitivamente
- A lo maximo, el auotomata se encuentra en un solo estado
- Una movida solo depende del estado en el que esta. No depende de las entradas anteriores
- La existencia de estados finales no asegura que el FA tenga un lenguaje reconocido con al menos 1 cadena

## Uso
Cadena solo reconocida/aceptada si
$x \in \Sigma^* \ | \ \delta^*(q_0,x) \in F$ %% | significa "tal que", "such that"%%

Lenguaje reconocido por un DFA A:
$L(A)=\{x \ | \ x\ es\ reconocida\ por\ A\}$
$L(A)=\{x \ | \ x \in \Sigma^* \ | \ \delta^*(q_0,x) \in F\}$

L(A) para un FA es unico.
Un FA *no* reconoce una cadena por una de dos razones
- Procesa toda la cadena y llega a un estado que no es final
- No llega a procesar toda la cadena, $\delta$ indefinido

Un lenguaje puede ser reconocido por mas de un FFA ssi $q_0 \in F$, el FA reconoce $\varepsilon$

## Propiedades
- Cadenas a procesarse pueden subdividirse en un numero arbitrario de cadenas:
$\delta^*(q0,abbaba)=\delta^*(\delta^*(q0, abb), aba)$

#todo Demostrar que:
$\forall x,y \in \Sigma^*,\ \delta^*(q, xy)=\delta^*(\delta^*(1, x), y)$
o
$\delta^*(q,x)=q' \wedge \delta^*(q',y)=q''\rightarrow \delta^*(q,xy)=q''$

Casos base:
- $x=\varepsilon, y=\varepsilon$
- $x=\varepsilon, y=y$
- $x=x, y=\varepsilon$
Casos inductivos:
- $x=x,y=yj$
- $x=xi,y=y$
- $x=xi,y=yj$

## Ejemplo de ej. de examen
[[FA - Ejercicio tipo Examen]]
