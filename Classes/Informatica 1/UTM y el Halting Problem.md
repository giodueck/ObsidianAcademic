26-10-2022
---
# UTM y el Halting Problem
> [!info] Repasando
> Segun la tesis de Church (parte 2), cualquier algoritmo puede codificarse en una maquina de turing o formalismo equivalente.
> $\therefore$ existe una TM **Enumeradora**
\
> Si existe un algoritmo "Sistema Operativo", debe existir una TM "Sistea operativo"
> - Es decir, un algoritmo que se pueda comportar como cualquier otro algoritmo
> - Una TM "SO" recibe como entrada otra TM o su numero de Gödel
\
> Esta TM es la **Maquina Universal de Turing** (UTM)
> - Recibe dos entradas:
> 	$utm(x, y) = f_y(x)$

## Consideraciones
La funcion $m(x, y) = f_y(x) + 1$ es computable gracias a la UTM.
- La funcion m es computable, pero no necesariamente es una funcion total
- Puede existir alguna combinacion <x, y> que haga que $f_y(x)$ qiede eternamente en un bucle

## The Halting Problem
Enunciado:
No existe TM que pueda computar la siguiente funcion:
##### $g(x, y) = if \ f_y(x) \ne \perp then \ 1 \ else \ 0$

Que significa $f_y(x) \ne \perp$?
$f_y(x)$ simular el comportamiento de la y-esima TM con el input x
$f_y(x) \ne \perp \rightarrow$ La simulacion termino con un resultado
$f_y(x) = \perp \rightarrow$ La simulacion nunca termina (o cuando no reconoce la cadena *pero para nosotros siempre significara que nunca termina*)

En lenguaje natural:
Si la ejecucion de la y-esima TM con el input x termina, entonces 1, sino 0

### Demostracion
Reduccion al absurdo (por contradiccion)

Se asume que existe un TM que computa la funcion g.
Asumimos g computable.

Si g es computable, la funcion
$h(x) = if \ g(x, x) = 0 \ then \ 1 \ else \perp$
tambien es computable

$g(x, y) = if \ f_y(x) \ne \perp then \ 1 \ else \ 0$
$h(x) = if \ g(x, x) = 0 \ then \ 1 \ else \perp$

Si h es computable, tiene su numero de Gödel
$h = f_{x_0}$
*$h = f_{x_0}$ es una notacion corta para $\forall n, f_{x_0}(n) = h(n)$* 

$h(x_0) = 1 \rightarrow g(x_0, x_0) = 0 \rightarrow f_{x_0}(x_0) = \perp$ *(contradiccion)*
$h(x_0) = \perp \rightarrow g(x_0, x_0) = 1 \rightarrow f_{x_0}(x_0) \ne \perp$ *(contradiccion)*

