14-09-2022
---
# PDA - Definiciones formales
## Caracteristicas generales
- Puede moverse con input o sin el (ignorandolo), pero *no ambos*
- *Siempre* extrae el simbolo en el tope de la pila al leerlo
- El movimiento solamente depende de tres condiciones:
	1. estado actual
	2. el simbolo leido (o ignorado)
	3. el tope de la pila
- Puede ingresar a *bucles infinitos* (simplemente operando con la pila)
- La cadena se reconoce una vez que *alcance un estado final y se haya procesado completamente. No implica que el PDA se detenga* al terminar de procesar la cadena, puede que siga moviendose (inclusive infinitamente) despues de haber reconocido una cadena
- *No* puede operar con una pila vacia

## Elementos
Un PDA $A = (Q, \Sigma, \Gamma, \delta, q_0, Z_0, F)$

Q = conjunto de estados
$\Sigma$ = alfabeto de entrada
$\Gamma$ = alfabeto de pila
$\delta: Q \times (\Sigma \cup \{\varepsilon\}) \times \Gamma \rightarrow Q \times \Gamma^*$
*si $\delta(q, i, A)$ esta definido entonces $\delta(q, \varepsilon, A)$ esta indefinido*
$q_0 \in Q$ *(estado inicial)*
$Z_0 \in \Gamma$ *simbolo inicial de pila, fondo de pila*
$F \subseteq Q$

e.g.:
$\delta(q, a, \#) = <q', A\#>$

## Funcionamiento
*Instantanea (estado o configuracion)*
$c \in Q \times \Sigma^* \times \Gamma^*$
*<estado actual, input por leer, contenido de la pila>*
$c = <q_2, bb, AAZ>$
$c = <q, x, \varphi>$

**Avance (relacion de transicion)**
Un PDA A avanza desde una configuracion c hasta una config. c'
$c \vdash c'$
$<q, x, \varphi> \ \vdash \ <q', x', \varphi'>$ *por medio de*
$\delta(q, i, a) = <q', a>$
*si* $x = ix', \varphi = A\beta, \varphi' = a\beta$
$\delta(q, \varepsilon, A) = <q', a>$
*si* $x = x', \varphi = A\beta, \varphi' = a\beta$

#todo ejercicios ppt - funcionamiento

## Uso
### Reconocimiento por estado final
Un PDA $A = (Q, \Sigma, \Gamma, \delta, q_0, Z_0, F)$ reconoce una cadena $x \in \Sigma^*$ si y solo si
$<q_0, x, Z_0> \ \vdash^* <q_f, \varepsilon, \varphi>$
con $q_f \in F$
$\varphi \in \Gamma^*$

Una cadena es reconocida si se termino de leerla y en algun momento se alcanza un estado final.
Lenguaje reconocido es el conjunto de todas las cadenas reconocidas.

### Reconocimiento por pila vacia
Un PDA $A = (Q, \Sigma, \Gamma, \delta, q_0, Z_0, F)$ reconoce una cadena $x \in \Sigma^*$ si y solo si
$<q_0, x, Z_0> \ \vdash^* \ <q, \varepsilon, \varepsilon>$
con $q \in Q$

Una cadena es reconocida si se termino de leerla y la pila esta vacia.
Lenguaje reconocido es el conjunto de todas las cadenas reconocidas.