18-10-2022
---
# TM - Variaciones

## TM Limitadas
TM con alfabeto reducido
- Cualquier alfabeto es adecuado siempre y cuando la cantidad de simbolos $\ge$ 2, tanto para $\Sigma$ como para $\Gamma$
- La TM es insensible a la codificacion
	- Los FA si lo son

### Ejemplo
Diseñar una k-tape TM que reconozca el lenguaje $a^nb^nc^n$
$\Gamma = \{Z, \textblank\}$

Entrada: $aaaa$
*Memoria (version ilimitada)*: $Z\#\#\#\#\textblank$
Memoria: $ZZ \textblank Z  \textblank Z  \textblank Z  \textblank Z \textblank \textblank$ *($ZZ$ representa Z, $\textblank Z$ representa \#)*

### Minimizacion de TM
Cualquier TM puede reducirse en cantidad de estados hasta llegar a contar unicamanete con 3 (2 no finales y 1 final)

El estado actual puede almacenarse en una cinta de memoria adicional, con un estado de preparacion opcional y uno de ejecucion, ambos no finales, y un tercer estado que es final.

## Limitaciones de propiedades
- Las TM son cerradas respecto a la union
- No se pueden establecer si dos TM reconocen el mismo lenguaje (no pasa lo mismo con los FAs)
- Los TM pueden tener un bucle infinito **indetectable** (los bucles infinitos se pueden detectar en los PDA)

## Temas de examen

Definir una TM
- con cintas infinitas a ambos extremos
- con una unica cinta (TM original)
- con movimientos a saltos R, L, S numero desde la posicion actual. 0 se queda, -4 mueve 4 posiciones a la izquierda
- con acceso aleatorio
- con cintas bidimensionales (infinitas hacia arriba y hacia la derecha)
- con mas de un cabezal por cinta