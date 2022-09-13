13-09-2022
---
# Expresiones Regulares
## Definicion
Sea $A$ un alfabeto y sea $D(w)$ el lenguaje denotado por la expresion regular $w$
1. si *$a \in A$*, entonces $a$ es una expresion regular y denota el lenguaje ${a}$. $D(a) = {a}$
2. si $E_1$ y $E_2$ son expresiones regulares, entonces *$(E_1 + E_2)$* o su equivalente *$(E_1 \cup E_2)$* es una expresion regular y denora la union de los lenguajes denotados por $E_1$ y $E_2$. $D(E_1 + E_2) = D(E_1) \cup D(E_2)$
3. si $E_1$ y $E_2$ son expresiones regulares, *$E_1 \cdot E_2$* es una expresion regular y denota la concatenacion de los lenguajes denotados por $E_1$ y $E_2$
4. Si $E$ es una expresion regular, entonces *$E^\ast$* es una expresion regular y denota el lenguaje que es la aplicacion del operador de Kleene al lenguaje denotado por $E$.
5. Nada mas es una expresion regular.

## Ejemplos
*1* es une RE, denota {*1*}
*2* es una RE, denota {*2*}
*1 + 2* es una RE, denota {*1, 2*}
*(1 + 2) . 2* es una RE, denota {*12, 22*}
*$(1 + 2)^\ast$* es una RE, denota {*$\varepsilon, 1, 2, 11, 12, 21, 22, ...$*} = $\{1, 2\}^*$

$\{a^{2n}b^{3m} \ | \ n > 0, m > 0\} = (aa)(aa)^*(bbb)(bbb)^* = (a \cdot a) \cdot (a \cdot a)^* \cdot (b \cdot b \cdot b) \cdot (b \cdot b \cdot b)^*$

Tambien se extiende usando +
$\{a^{2n}b^{3m} \ | \ n > 0, m > 0\} = (aa)^+(bbb)^+$

## Ejercicios
$A = \{a, b, c\}$
Definir expresiones regulares que denoten
- Cualquier cadena de A* donde el primer y ultimo simbolo sean el mismo
- Cadenas donde el tercer simbolo comenzando desde la derecha sea una "c"
- Cadenas donde existen una cantidad impar de "a"
- Toda subcadena de 3 elementos que tenga una "a"
- Cadenas donde despues de una "a" aparezca una "b" en los siguientes 3 lugares.
#todo 

## Relaciones con los FA
### RE -> FA-$\varepsilon$
1. $a$ es una transicion con un simbolo
2. $R \cup S$ son dos transiciones nulas a sub FAs que reconozcan R y S, y transiciones nulas de ellos a un estado final
3. $R \cdot S$ son dos sub FAs que reconozcan R y S unidas con una transicion nula en serie
4. $R^*$ es una transicion nula a un sub FA que reconozca R, transiciones nulas de R y del inicio a un estado final, y una transicion nula del final al inicio de R. Para que el FA reconozca 0 o mas veces R
