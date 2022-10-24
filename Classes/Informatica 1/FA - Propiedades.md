29-08-2022
---
# FA - Propiedades
## Teorema
Sea $A = (Q, \Sigma, \delta, q_0, F)$ un DFA
L(A) es infinito si y solo si $\exists x \in \Sigma^* \ | \ x \in L(A) \wedge |x| \ge |Q|$

**Planteo de la demostracion**
Sea $A = (Q, \Sigma, \delta, q_0, F)$ un DFA

### Parte si (cuando)
$\exists x \in \Sigma^*, x \in L(A) \wedge |x| \ge |Q| \rightarrow |L(A)| = \infty$

Ya que al tener $|x| \ge |Q|$, y ser x reconocida, algun estado se activara mas de una vez, es decir existe un ciclo. Por lo tanto x puede tener una longitud arbitrariamente grande.

Dadas las condiciones, siempre existira una division de x compuesta por $x = x_1x_2x_3$ con $x_1,x_3 \in \Sigma^*; x_2 \in \Sigma^+$
$\delta^*(q_0, x_1) = q$
$\delta^*(q, x_2) = q$
$\delta^*(q, x_3) \in F$
$\therefore$ tambien
$\delta^*(q_0, x_1) = q$
$\delta^*(q, x_2) = q$
$\delta^*(q, x_2) = q$
$\delta^*(q, x_3) \in F$

$\forall k \ge 0 \ \delta^*(q0, x_1x_2^kx_3) \in F \rightarrow |L(A)| = \infty$

> [!info]- $\Sigma^*$ vs $\Sigma^+$
> $\Sigma^*$: cualquier cadena con 0 o mas simbolos de $\Sigma$
> $\Sigma^+$: cualquier cadena con 1 o mas simbolos de $\Sigma$

### Parte solo si (siempre)
$|L(A)| = \infty \rightarrow \exists x \in \Sigma^*, x \in L(A) \wedge |x| \ge |Q|$

Si hay infinitas cadenas, alguna cadena tendra longitud mayor a cualquier entero especifico. Esto se da porque con alfabetos finitos, una cota superior de longitud no permite representar infinitas cadenas.

### Lema de Bombeo (Pumping Lemma)
Sea A un FA
$\forall w \in L(A) \ \exists n = |Q| \ | \ |w| \ge n$

Podemos descomponer w en tres cadenas, w = xyz, tales que:
1. $y \ne \varepsilon$
2. $|xz| \le n$
3. $\forall k \ge 0, xy^kz \in L(A)$

#### Cuestiones
- La existencia de un bucle en el grafo que representa a un FA asegura que el lenguaje sea infinito?
	- La existencia de un bucle es condicion necesaria pero no sufuciente para la existencia de un lenguaje reconocido infinito. 
	  El bucle debe ser alcanzable del estado inicial y debe llevar a un estado final
- Cuando el lenguaje reconocido por un FA es vacio?
	- Cuando no hay estado final
	- Cuando ninguna cadena con longitud menor que la cantidad de estados es reconocida
- Cuando el lenguaje reconocido por un FA es finito?
	- Se deben probar bucles, por lo que no sirve probar las cadenas con longitud $\le |Q|$. Se prueban cadenas con longitud $\le 2|Q|$
- Podemos llegar a probar que 2 FAs reconocen el mismo lenguaje?
- Hay una cantidad minima de estados para reconocer un lenguaje en particular?

30-08-2022
---
## Concepto de Cerradura (Closure)
Una operacion cerrada entre dos elementos de un conjunto produce otro elemento del mismo conjunto.

L(A) es cerrado respecto a:
- la interseccion
- la union
- la concatencation
- al complemento (resta de conjuntos)
- a *
- al complemento de $\Sigma^*$
- al homomorfismo (Hopcroft)

### L(A) es cerrado respecto a la interseccion
Sean $L_1, L_2, L_3 \in L(FA)$
$L_3 = L_1 \cap L_2$

Vamos a trabajar sobre los automatas, no los lenguajes directamente
$L(A_1) = L_1$
$L(A_2) = L_2$
$L(A_3) = L_3 = L_1 \cap L_2$ *una cadena reconocida por $L_3$ es reconocida tanto por $L_1$ como por $L_2$*

#### Demostracion
*definicion cerradura general*
$\forall L_1, L_2 \in L(FA)$
$\exists L_3 \in L(FA), L_3 = L_1 \cap L_2$

*equivalente en simbologia de automatas*
$\forall A_1 = (Q_1, \Sigma, \delta_1, q_{01}, F_1), A_2 = (Q_2, \Sigma, \delta_2, q_{02}, F_2)$
$\exists A_3 = (Q_3, \Sigma, \delta_3, q_{03}, F_3) \ | \ L(A_3) = L(A_1) \cap L(A_2)$

\*) Dar un procedimiento para construir un DFA $A_3$
\*\*) Demostrar la correccion del procedimiento

\*) *Lenguaje informal:*
1. Combinamos los estados de $A_1$ y $A_2$
2. Partimos de la combinacion de los estados iniciales
3. Nos movemos simultaneamente con ambos FAs
4. Reconocemos solamente si ambos llegan a estados finales

$Q_3 = Q_1 \times Q_2$ *(regla 1)*

$q_{03} = \ <q_{01}, q_{02}>$ *(regla 2)*

$F_3 = F_1 \times F_2$ *(regla 3)*

$\delta_3(<q_{01}, q_{02}>, i) = \ <\delta_1(q_1, i),\ \delta_2(q_2, i)>$ siempre que $\delta_1(q_1, i)$ y $\delta_2(q_2, i)$ esten definidos *(regla 4)*

\*\*)
$L(A_3) = L(A_1) \cap L(A_2)$
\#) $x \in L(A_3) \rightarrow x \in L(A_1) \wedge x \in L(A_2)$
\#\#) $x \in L(A_1) \wedge x \in L(A_2) \rightarrow x \in L(A_3)$

*Generalizacion*
\#\#) *Utilizando las reglas*
$\delta^*_3(<q_{01}, q_{02}>, x) = <\delta_1^*(q_{01}, x), \delta_2^*(q_{02}, x)>$
si $\delta_1^*(q_{01}, x), \delta_2^*(q_{02}, x)$ estan definidos

*Definicion de lenguaje reconocido*
$\delta_1^*(q_{01}, x) \in F_1 \wedge \delta_2^*(q_{02}, x) \in F_2 \rightarrow \delta^*_3(<q_{01}, q_{02}>, x) \in F_3$

*Por reglas 2. y 3.*
Sean los resultados $\delta_1^*(q_{01}, x) =$ *$qf_1$* y $\delta_2^*(q_{02}, x) =$ *$qf_2$*, entonces $\delta^*_3(<q_{01}, q_{02}>, x) =$*$<qf_1, qf_2>$*

*Generalizando:*
$\delta_1^*(q_{01}, x) = q_1, \delta_2^*(q_{02}, x) = q_2 \rightarrow \delta^*_3(<q_{01}, q_{02}>, x) = <q_1, q_2>$
