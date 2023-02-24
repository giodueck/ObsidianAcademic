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
No existe TM que pueda computar la siguiente funcion:
$$g(x, y) = if \ f_y(x) \ne \perp then \ 1 \ else \ 0$$

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


01-11-2022
---
## Teorema
No existe TM que pueda computar la siguiente funcion:
$$h(x) = If \ f_x \ es \ total \ then \ 1 \ else \ 0$$

No existe TM que pueda determinar que otra TM siempre termina su computacion para todo input.

### Demostracion
Reduccion al absurdo (por contradiccion)

Asumimos h computable.
$TM = \{M_1,$*$M_2$*$,$*$M_3$*$, M_4, M_5, ...,$*$M_{15}$*$, M_{16},$*$M_{17}$*$, ...\}$
$h(1) = 0, h(2) = 1, h(3) = 1, h(4) = 0, h(5) = 0, ..., h(15) = 1, ...$

$TM_T = \{$*$M_2$*$,$*$M_3$*$,$*$M_{15}$*$,$*$M_{17}$*$, ...\}$
$TM_T = \{MT_1,MT_2,MT_3,MT_4,...\}$

Podemos definir una funcion k de la siguiente manera
$k(x) = y$, y es el numero de Gödel de la x-esima TM que computa una funcion total
$k(1) = 2$
$k(2) = 3$
$k(3) = 15$
$k(4) = 17$

#### En terminos de funciones
$F = \{F_1,$*$F_2$*$,$*$F_3$*$, F_4, F_5, ...,$*$F_{15}$*$, F_{16},$*$F_{17}$*$, ...\}$
$h(1) = 0, h(2) = 1, h(3) = 1, h(4) = 0, h(5) = 0, ..., h(15) = 1, ...$

$FT = \{$*$f_2$*$,$*$f_3$*$,$*$f_{15}$*$,$*$f_{17}$*$, ...\}$
$FT = \{ft_1,ft_2,ft_3,ft_4,...\}$

$k(1) = 2$
$k(2) = 3$
...

**Si h es computable, k es computable**

#### Consideraciones adicionales
*k es creciente*: nunca va a decrecer por la forma en que se definio
*k es total*: siempre retorna un resultado

#### Demostracion (continuacion)
Definimos otra funcion:
$v(n) = f_{k(n)}(n) + 1$ * \* *
$v(3) = f_{k(3)}(3) + 1 = f_{15}(3) + 1$ (ejemplo)

De la forma en que esta construida
*v es total*
*v es computable*
v es total $\Rightarrow ft_{w_0} = v$
v es computable $\Rightarrow f_{x_0} = v$ para todo n, $v(n) = f_{x_0}(n)$
$k(w_0) = x_0$
Haciendo $n = w_0$ en * \* *

#incomplete

## Otras funciones incomputables
- k(x) = si $f_x$ es constante entonces 1 sino 0
- k(x, q, z) = si la x-esima TM pasa por el estado q durante el procesamiento de z, entonces 1, sino 0
- k(x, y) = si $f_x = f_y$, entonces 1 sino 0
- k(x) = si $z_0 \in I_{f_x}$, entonces 1 sino 0
*No suelen ponerse como ejercicios, pero algunos de estos problemas se pueden reducir a otros, como el segundo en el Halting problem*

## Consideraciones
La funcion
$$g'(x, y) = if \ f_y(x) \ne \perp \ then \ 1 \ else \ \perp$$
es computable.

*No todo lo que se parece al Halting problem es incomputable*