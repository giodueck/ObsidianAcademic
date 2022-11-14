14-11-2022
---
# Teorema de punto fijo
*No tiene (tanto) valor por si mismo*

**Enunciado:**
Para toda funcion total y computable "**t**" existe un numero natural p tal que $f_p = f_{t(p)}$
a "p" se le denomina **punto fijo de "t"**.

$\forall t$ total y computable, $\exists p \in N \ | \ f_p = f_{t(p)}$

**Explicacion del enunciado:**
Tomamos $t(n) = n + 1 \rightarrow$ esto significa que existen dos maquinas "vecinas" que computan la misma funcion.

## Demostracion
En el ppt, no se realiza en clase

# Teorema de Desicion de Rice
Sea **F** cualquier conjunto de funciones computables
y sea *S* $(S \subseteq N)$ definida como:
1. Si $x \in S$, entonces $f_x \in F$
2. Si $h \in F$, entonces para todo $f_y = h, y \in S$
S es recursivo si y solo si $F = \emptyset$ o $F = FC$ *(funciones computables)*

*Casos limite*
$F = \emptyset \rightarrow S = \emptyset \rightarrow C_S(x) = 0$
$F = FC \rightarrow S = N \rightarrow C_S(x) = 1$

## Demostracion
Asumimos:
$F \ne \emptyset \rightarrow t \in F \rightarrow \exists i \ | \ f_i = t, i \in S$
$F \ne FC \rightarrow w \notin F \rightarrow \forall j \ | \ f_j = w, j \notin S$
S recursivo $\rightarrow$ Cs es computable
$f_i \in F$
$f_j \notin F$

*Se define la funcion*
$g(x) = if \ Cs(x) = 1 \ then \ j \ else \ i$
g es computable, si Cs es computable y total
Si g es computable y total, tiene su punto fijo.
z es el punto fijo de $g \rightarrow f_z = f_{g(z)}$

g(z) puede retornar 2 valores.
- $g(z) = i$, implica que "salio por el else", implica que $Cs(z) \ne 1$, implica que $Cs(z) = 0$, implica que $f_z \notin F$, pero eso contradice el hecho de que $f_{g(z)}$ siendo $g(z) = i$, se de que $f_i \in F$
- $g(z) = j$, implica que "salio por el then", implica que $Cs(z) = 1$, implica que $f_z \in F$, pero eso contradice el hecho de que $f_{g(z)}$ siendo $g(z) = j$, se de que $f_j \notin F$

#todo Aprender de memoria, pero entender bien

## Aplicacion
$k(x) = if \ f_x \ es \ constante \ then \ 1 \ else \ 0$
$F = \{f_x \ | \ f_x \ es \ constante\}$
$S = \{x \ | \ f_x \ es \ constante\}$

$Cs(x) = if \ x \in S \ then \ 1 \ else \ 0$
$Cs(x) = if \ f_x \ es \ constante \ then \ 1 \ else \ 0$

El teorema de decision de Rice nos dice que ya que F no contiene a todas las funciones (ej. $f(x) = x$) y F no es vacio (ej. $f(x) = 6$), $k(x)$ no es computable.

## Consideraciones
- No dice mada de que el conjunto S se recursivamente enumerable
- El conjunto de funciones F debe ser de funciones computables
- No dice nada acerca de la recursividad o no del conjunto F

## Ejemplos de propiedades no triviales
- Funciones totales
- Funciones que estan definidas para x = 10
- Funciones que tienen a 10 en su imagen
- Maquinas qie pasan por el estado $q_12$
- Maquinas que siempre leen todo el input
- Maquinas que no leen todo el input

# Bonus: Super TM
Hypercomputation:
Conjunto de modelos que superan a las TM
Introducidas por Alan Turing (Oracle): [Hypercomputation](https://en.wikipedia.org/wiki/Hypercomputation)