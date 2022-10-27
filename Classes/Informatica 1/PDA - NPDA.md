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
$<q_0, x, Z_0> \ \vdash^* \ <q_f, \varepsilon, \varphi>$
con $q_f \in F$, $\varphi \in \Gamma^*$

### Reconocimiento por estado final
Una cadena es reconocida si se termino de leerla y en algun momento se alcanza un estado final.
Lenguaje reconocido es el conjunto de todas las cadenas reconocidas

## Ejercicios PDA / NPDA
- Definir una variacion de PDA que en vez de trabajar con pilas opere sobre una cola. Definir elementos, funcionamiento y uso y establecer y demostrar la relacion de potencia con los PDA tradicionales.
- Sea una clase de PDA que solo permita en su alfabeto de stack los símbolos ${Z_0,0,1}$.
  Este PDA limitado en alfabeto de stack, también está limitado en su capacidad de reconocer lenguajes? ¿el reducir el alfabeto hace que el PDA sea menos potente?
- Definir una variación de autómata a PILA donde el PDA tenga dos pilas. Llamaremos a este formalismo 2PDA. Los movimientos dependen del símbolo leido y del tope de ambas pilas. La operación sobre las pilas es independiente, por ejemplo, una pila puede crecer mientras otra decrecer.
  Definir: elementos, funcionamiento, utilización
  Explicar detalladamente la relación de potencia con los PDA con una sola pila y con los NPDA
- Definir una variación de PDA donde la capacidad de la pila esté limitada a k símbolos.
  El alfabeto puede ser cualquiera, pero la capacidad de la pila es limitada
  Si durante el proceso, la capacidad de la pila se sobrepasa, entonces el PDA descarta los símbolos que no puede almacenar y continua con su ejecución
  Demostrar la relación de potencia con los FAs
- Modificar la definición del PDA de tal forma a que la lectura del stack no implique el borrado del tope. En otras palabras, cuando el PDA lee el tope (durante un movimiento) no lo borra automáticamente.

### Tema de examen real
Definir (de ser posible) un NPDA que reconozca el lenguaje $L = \{a^nb^m \ | \ n \le m \le 2n\}$. Demostrar formalmente la correccion del NPDA o explicar la imposibilidad de encontrarlo debifo a que no es reconocido por ningun NPDA.

## Propiedades
Los L(NPDA) son cerrados respecto a la union
Los L(PDA) son cerrados respecto al complemento respecto a $\Sigma^*$