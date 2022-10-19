19-10-2022
---
# Enumeracion
## Introduccion
Lo que define a una TM es su dibujo
Se podria asignar una `id` a cada TM?
Si, enumeracion.
Para hacer eso se hace una biyeccion con los naturales.

Biyeccion con los naturales
- $E: N \rightarrow \{TM\}$
- $E^{-1}: \{TM\} \rightarrow N$
Orden total
- Es una relacion
	- total
	- no reflexiva
	- antisimetrica
	- transitiva

**Ejemplo de orden total que NO implica una enumeracion:**
Pares de enteros
- p = <p1, p2>
- q = <q1, q2>

N x N = {<1, 1>, <1, 2>, <1, 3>, ...}
Es un orden pero no implica numeracion:
- $E^{-1}<1, 4>\ = 4$
- $E^{-1}<2, 4>\ =\ ?$

**Ordenamiento de pares que SI funciona**
*Clasico ejemplo de poner los valores en los ejes de una grilla y enumerar en diagonal, cada diagonal tendra el conjunto de pares que sume 2, 3, 4, ...*
La relacion *<* se define como:
p *<* q si
1. <p1 + p2> < <q1, q2>
2. <p1 + p2> = <q1, q2>
	p1 < q1
	o p1 = q1 y p2 < q2

E(x, y) = x + (x + y - 1) * (x + y - 2) / 2

**Criterio**: Dividir el conjunto finito en *infinitos subconjuntos finitos*, no en infinitos conjuntos infinitos.

## Ordenamiento de cadenas
Ordenar un conjunto finito es trivial, ej. orden alfabetico.

Sea B = {a, b, c, d} y el orden *<* definido como a *<* b *<* c *<* d

Todas las cadenas formadas con simbolos de B: $B = \{\varepsilon, a, b, c, d, aa, ab, ac, ad, ba, bb, bc, bd, ..., aaa, aab, ...\}$

La cadena **x** esta en una posicion anterior a la cadena **y** (**x** *<* **y**) si
|x| < |y| o

|x| = |y| = n
$x = x_1x_2x_3x_4...x_n$
$y = y_1y_2y_3y_4...y_n$
$\exists i \ | \ \forall j < i, x_j = y_j \wedge x_i$ *$<$* $y_i$

#todo copiar resto del ejemplo (foto)
