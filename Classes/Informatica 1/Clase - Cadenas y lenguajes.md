16-08-2022
---

# Clase - Cadenas y lenguajes
## Simbolo
Indivisible e inconfuncible con otro
e.g. A, a, b, 0, Z0

## Alfabeto
Conjunto ***finito*** de simbolos
e.g.
- A = {a, b, Z0, 2}
- B = {0, 1}
- C = {a, b, ab, 3} // Simbolo ambiguo

## Cadenas
Secuencia finita de simbolos
e.g.
- w = a, b, a, a
- w = <a, b, a, a>
- w = abaa
- w = a.b.a.a (operacion implicita: concatenacion)

> [!info]+ Representacion preferida: w = abaa
> Necesita de un alfabeto no ambiguo, en caso sea ambiguo se prefiere w = a.ba.a

17-08-2022
---
## Cadenas - Cont.
### Propiedades
Longitud:
- Se utiliza el operador de modulo: | |
- |abaa| = 4
- |a| = 1
- Existe una cadena especial tal que su longitud es 0
	- $\varepsilon$ (epsilon)
	- |$\varepsilon$| = 0 // String nulo o vacio
	- Identidad
		- $\varepsilon w = w \varepsilon = w$

#### Definicion iterativa:
Una cadena s = i, i1, i2, ... ik donde $i \in A$, $0 \leq j \leq k$, $k \in N$
- Longitud de la cadena s: |s| = k

#### Def. recursica
Sea x una cad formada por simb del alfabeto A
|x| = 0 // si x = $\varepsilon$
|x| = 1 + |x'| // si x = ix', i $\in$ A, x' una cadena formada por simbolos de A

## Lenguaje
Conjunto de cadenas
- Finito o infinito
e.g.
- L1 = {ab, ba, aa, bb}
- L2 = {ab, abb, abbb, abbb, ...}
- L3 = {$\varepsilon$, 10, 45, b3r2}
- L4 = $\emptyset$ (cardinalidad 0)
- L5 = {$\varepsilon$} (cardenalidad 1)

Se pueden concatenar, se aplican las operacciones de conjuntos:
- union ($\cup$)
- interseccion ($\cap$)
- complemento ($\prime$)

$L_1 \times L_2 = \{wz\ | \ w\ \in\ L_1, z\ \in\ L_2\}$

- $L \times L = L^2$
- $L^0=\{ \varepsilon \}$

#### Clausura Transitiva:
- $L^+ = L_1 \cup L_2 \cup L_3 ...$
- $L^+ = U_{i=1..\infty} = L_i$

#### Clausura Transitiva y reflexiva
- $L^* = L_0 \cup L_1 \cup L_2 ...$
- $L^* = \{\varepsilon\} \cup L^+$
- (a, b, c)* // Conjunto de cualquier combinacion de a, b, c

## Ejercicio
$s = i_1 i_2 i_3 ... i_k$
Sean $s_1 = i_1 i_2 i_3 ... i_k$ y $s_2 = j_1 j_2 j_3 ... i_k$ dos cadenas basadas en el alfabeto A, con $m, n \in N$

Definir formalmente las propiedades
- Dos cadenas son iguales ($s_1=s_2$)
	- $|s_1| = |s_2|$
	- $\forall_t \ i_t=j_t, 1 \leq t \leq m$
- Una cadena es palindroma
	- $\forall_t \ i_t=i_{k - t + 1} ,\ 1 \leq t \leq k$
- Una cadena es el resultado de reemplazar todas las apariciones de un simbolo por otro (no necesariamente diferente): aababc ==> 11b1b4
	- Sea la cadena inicial $s_1$ y la cadena final $s_2$, entonces $\forall t, u \ i_t=i_u \rightarrow j_t=j_u,\ 1 \leq t \leq k, 1 \leq u \leq k$

## Formas de definir
- Informal
- Descriptiva (con ejemplo)
- Rigurosa (con definicion semi formal)
- Formal (usando simbolos regulares)