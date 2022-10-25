25-10-2022
---
# Enumeracion de TM
## Gödelizacion
A cada TM le corresponde una posicion dentro de las TM

Podemos tener el RUC (C.I.) de una TM
$TM = \{M_1, M_2, M_3, M_4, ...\}$
Ese es el numero de Gödel

$M_i$ se lee
la TM con numero Gödel **i** o **i**-esima TM

$M_i \ne M_j$ si $i \ne j$

## Funciones computables
$TM = \{M_1, M_2, M_3, M_4, ...\}$
$F_M = \{f_1, f_2, f_3, f_4, ...\}$
$L_M = \{L_1, L_2, L_3, L_4, ...\}$

$f_i$ es la funcion computada por la $M_i$
$L_i$ es el lenguaje reconocido por la $M_i$

Obs.: $F_M, L_M$ no son conjuntos, ya que pueden haber elementos repetidos. Es decir dos TM diferentes pueden reconocer el mismo lenguaje. $F_M, L_M$ son secuencias que permiten repeticiones.
*No es cierto que*
- *$f_i \ne f_j$ si $i \ne j$*
- *$L_i \ne L_j$ si $i \ne j$*

### Funcion computable
Sea cualquier enumeracion $TM = \{M_1, M_2, M_3, M_4, ...\}$, $f_i$ la funcion computada por la i-esima TM y $L_i$ el lenguaje reconocido por la i-esima TM
- Una funcion t es computable si y solo si $\exists x_0$ tal que $t = f_{x_0}$
- Un lenguaje l es reconocible (decidible, efectivo) si $\exists x_0$ tal que $l = L_{x_0}$ / $l = L(M_{x_0})$

## Las TM son omnipotentes?
Todas las funciones computables?
- Para toda funcion h, existe un $x_0$ tal que $f_{x_0} = h$?
Cuantas son "todas las funciones"?
Cuantas son "todas las TM"? Cuantas son las "funciones computables"?
- Son equipotentes con los naturales
	- A cada numero natural le corresponde una TM
	- A cada TM le corresponde un numero natural
	- $|TM| = \aleph_0$ = Cardinalidad de los naturales
- A lo maximo existen $\aleph_0$ funciones computables

### Cuantas son "todas las funciones"?
$f: N \rightarrow N$ ?
$f: N \times N \rightarrow N$ ?
.
.
.
*$f: N \rightarrow \{0, 1\}$* $= 2^{|N|} = 2^{\aleph_0}$

## La luz al final del tunel
No nos interesan "todas" las funciones sino solamente las funciones (o problemas) que podemos "plantear", "describir", "enunciar", "escribir", ...
- Vamos a necesitar un "alfabeto"
- Funciones que podemos "plantear" = cadenas de ese alfabeto
- Alfabeto = {numeros, logica, algebra, C, Java}
- {numeros, logica, algebra, C, Java}*
Estas funciones se llaman **FD**, funciones denotables.

Si estan basadas en un alfabeto, y cada funcion es una cadena, entondes $|FD| = \aleph_0$

**Por lo tanto, tanto las funciones computables como las denotables tienen el mismo orden de infinitud.**


### Las preguntas revisadas
Toda funcion denotable, es computable?
Cada funcion que podemos escribir, se puede computar?
Cada problema que podemos imaginarnos tiene solucion?
Todo lenguaje definido puede ser reconocido por una TM?

## Turng machine enumeradora
Existe un algoritmo que reciba un numero de Gödel y genere el dibujo (o la delta) de la TM correspondiente?

Segun la tesis de Church (parte 2), cualquier algoritmo puede codificarse en una maquina de turing o formalismo equivalente.
$\therefore$ existe una TM **Enumeradora**

Si existe un algoritmo "Sistema Operativo", debe existir una TM "Sistea operativo"
- Es decir, un algoritmo que se pueda comportar como cualquier otro algoritmo
- Una TM "SO" recibe como entrada otra TM

Esta TM es la **Maquina Universal de Turing** (UTM)
- Recibe dos entradas:
	$utm(x, y) = f_y(x)$

