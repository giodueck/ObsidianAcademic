02-11-2022
---
# Computabilidad avanzada
Podemos tender a pensar que ahora sabemos cuales funciones son computables y cuales no.

Realidad:
- Existen funciones para las cuales no existe demostracion de que sean computables o incomputables
- La funcion que recibe una funcion y verifica si es computable o no, es incomputable
- Existen funciones que son computables, pero no se puede encontrar una TM que la compute

## Funciones sospechosas
$g(x) =$ el x-esimo digito decimal de $\pi$.
$g(1) = 1$
$g(2) = 4$
$g(3) = 1$
$g(4) = 5$
**Esta funcion es computable**

$g_1(x) =$ si la codificacion decimal de x aparece en la expansion de $\pi$, entonces 1, sino 0
$g_1(1) = 1$
$g_1(92) = 1$
$g_1(925) =$(si no existe?)$= 0$
**Hasta que no se demuestre $\pi$ racional, $g_1$ es incomputable**

$g_2(x) =$ si en la expansion decimal de $\pi$ existen exactamente x digitos "9" consecutivos, entonces 1 sino 0
$g_2(1) = 1$
$g_2(2) = 1$
$g_2(3) = ?$
**$g_2$ no es computable**

$g_3(x) =$ si en la expansion decimal de $\pi$ existen *por lo menos* x digitos "9" consecutivos, entonces 1 sino 0
$g_3(1) = 1$
$g_3(2) = 1$
$g_3(3) = 1$
$g_3(4) = 1$
**Esta funcion *es* computable, pero no sabemos *como* computar**

Computabilidad de $g_3$:
La expansion de $\pi$ tiene una cantidad maximo de digitos "9" consecutivos.
Llamamos a ese numero k.
$g_3(x) = \ if \ x \le k \ then \ 1 \ else \ 0$

Candidatas:
$g_3(x) = 1$, $k = \infty$
$g_3(x) = \ if \ x \le 1 \ then \ 1 \ else \ 0$, $k = 1$
$g_3(x) = \ if \ x \le 2 \ then \ 1 \ else \ 0$, $k = 2$
...
**$\therefore$ es computable, pero no podemos decir cual maquina es la que computa la funcion.**

$g_4(x) =$ si el ultimo teorema de Fermat es verdadero, entonces 1 sino 0 ($a^n + b^n = c^n$)
**Hasta hace poco esta funcion no sabiamos computar, pero siempre fue computable porque es una funcion constante: 1 o 0**

$g_5(x, y) =$ si en la expansion de $\pi$ existe una serie de digitos w con |w| = x repetida (no necesariamente consecutivas) por lo menos "y" veces entonces 1 sino 0
$g_5(1, 2) =$
$g_5(1, 3) =$

El enunciado de una funcion no es su algoritmo
- Enunciado, largo y complejo
- Algoritmo: = $g_5(x, y) = 1$

## Conclusion
Encontramos problemas incomputables
Encontramos problemas cuya incomputabilidad es incierta
Encontramos problemas cuya incomputabilidad es inutil