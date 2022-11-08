07-11-2022
---
# Pertenencia a conjuntos
Hasta ahora vimos resultados basados en computacion de funciones.
Otros resultados pueden obtenerse a traves de la *pertenencia a conjuntos*.

## Definiciones
Sea $S \subseteq \aleph$ cualquier subconjunto de naturales

**Funcion caracteristica/caracterizadora**
La funcion definida como
$Cs(x) = \ if \ x \in S \ then \ 1 \ else \ 0$
es la funcion caracteristica de $S = \{x \ | \ Cs(x) = 1\}$

**Conjunto recursivo**
S es recursivo si y solo si su funcion caracteristica es computable

### Ejemplos de conjuntos recursivos
$S_1 = \aleph$
$S_1$ es recursivo porque su funcion caracteristica
$Cs_1(x) ::= if \ x \in S_1 \ then \ 1 \ else \ 0$
$Cs_1(x) = 1$

$S_2 =$ conjunto de numeros pares
$Cs_2(x) ::= if \ x \in S_2 \ then \ 1 \ else \ 0$
$S_2$ es rec. porque su Cs 
$Cs_2(x) = 1 - (x \ mod \ 2)$ es computable
$Cs_2(x) = if \ (x mod 2)==0 \ then \ 1 \ else \ 0$

## Conjunto recursivamente enumerable
Sea $S = \aleph$ cualquier subconjunto de naturales
#todo ppt

### Ejemplos de conjuntos rec. enum.
#todo ppt

## Teorema
**Todo conjunto recursivo es recursivamente enumerable**
### Demostracion
S es recursivo $\rightarrow$ Cs es computable
Si S es vacio $\rightarrow$ es r.e. por definicion
Si S no es vacio $\rightarrow \exists x_0$ tal que $Ds(x_0) = 1 \rightarrow$ ...
#todo ppt

08-11-2022
---

## Teorema
**Si $S$ y $S' = N - S$ son recursivamente enumerables, entonces S es recursivo**
Si $S$ y $S'$ son recursivamente enumerables, entonces g y g' son computables. $S = I_g, S' = I_{g'}$

### Demostracion
#todo ppt

## Teorema
$S$ es recursivamente enumerable si
1. $S = \emptyset$ o
2. $S = I_g$, g es una funcion total y computable

**$S$ es recursivamente enumerable ssi es dominio de definicion de una funcion parcial y computable**

### Demostracion
$S$ es recursivamente enumerable ssi
$S = D_h$ *h es una funcion parcial y computable*
#todo ppt

## Temas de examen
#todo ppt
