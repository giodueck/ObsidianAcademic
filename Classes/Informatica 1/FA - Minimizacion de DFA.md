31-08-2022
---
# FA - Minimizacion de DFA
## Conceptos clave
- Redicir al maximo la cantidad de estados
- Equivalencia de estados
- Fusion de estados
- Eliminacion de estados inutiles
Se puede usar para probar que dos FAs reconocen el mismo lenguaje.

Un FA minimo es unico, si se repite el procedimiento, el resultado es el mismo FA.
*$\therefore$ existe un numero minimo de estados para un FA que reconozca cualquier lenguaje A*

## Procedimiento
1. Eliminar estados inalcanzables desde el estado incial. Esto incluye estados no finales de los cuales no se puede salir.
2. Confeccionar una tabla donde exista una sola entrada para cada par de estados diferentes
3. Marcar con una X las entradas que corresponden a pares de estados final y no final
4. Por cada par (p, q) no marcado hacer:
	1. Por cada simbolo de entrada i, calcular el par $(\delta(p, i), \delta(q, i)) = (p', q')$
		1. Si el par (p', q') esta marcado, el par (p, q) tambien se marca
		2. Si el par (p', q') no esta marcado, entonces se ingresa el par (p, q) a la casilla (p', q'). Si se marca la casilla (p', q') mas tarde, la casilla (p, q) tambien se marca como cascade.
5. Repetir el paso 1.
6. Todos los pares no marcados pueden ser fusionados

## Delta parcial
Pares (p, q) que tienen diferentes simbolos de entrada definidos no pueden ser fusionados.