24-10-2022
---
# Ordenamiento de FAs
## Ejemplo
### Restricciones
- Ignorar los estados finales y el estado inicial, o sea $F = \emptyset, q0 = q_0$
- Normalizacion de los nombres: todos los DFA con un estado tienen el estado $q_0$, todos los DFA con dos estados tienen los estados $q_0$ y $q_1$, y asi en adelante
- Alfabeto de entrada {a, b, c}

### Idea general
1. Organizar todos los DFA de la siguiente manera
	{{1 estado}, {2 estados}, {3 estados}, ...}
	*1.1. Contar cuantos DFA de n estados existen*
	$\delta: Q \times \{a, b, c\} \rightarrow Q$
	$|[\delta]| = |Q|^{3|Q|}$ *Cardinalidad del rango a la potencia de la cardinalidad del dominio*
	Considerando la posibilidad de delta parcial: $|[\delta]| = (|Q| + 1)^{3|Q|}$
	Para el ejemplo: {{|Q| = 1 |FA| = 8}, {|Q| = 2 |FA| = 739}, {|Q| = 3 |FA| = 262144}, ...}

2. Ordenar **internamente** los conjuntos

### Ordenamiento
Sean $A1 = (Q_1, \Sigma, \delta_1, q_0, \emptyset)$ y $A2 = (Q_2, \Sigma, \delta_2, q_0, \emptyset)$

A1 *<* A2 si
- $|Q_1| < |Q_2|$
- $|Q_1| = |Q_2|$
	- Definimos $\perp < q_0 < q_1 < q_2 < \ ... \ < q_n$
	- Definimos $a < b < c$
	- Definimos <q, i> $<$ <q', i'> si
		- $q < q'$
		- $q = q', i < i'$
	- Si existe el par <p, j> tal que
		- $\delta_1(p, j) < \delta_2(p, j)$
		- y para todo par <p', j'> $<$ <p, j>, $\delta_1(p', j') = \delta_2(p', j')$

#todo desarrollo y ejemplo en foto
#todo Ejercicio en el ppt

## Recomendaciones
- Delinear los primeros criterios para dividir un conjunto infinito, en infinitos conjuntos finitos
- Contar cuantos elementos tiene cada conjunto finito
- Aplicar "informalmente" el criterio para saber cuales son los primeros elementos y ultimos elementos de cada subconjunto
- Empezar las primeras pruebas del procedimiento encontrado el siguiente y el anterior de cualquier ejemplo