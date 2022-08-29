29-08-2022
---
# FA - Propiedades
## Teorema
Sea $A = (Q, \Sigma, \delta, q_0, F)$ un DFA
*L(A) es infinito*
si y solo si $\exists x \in \Sigma^*, x \in L(A) \wedge |x| \ge |Q|$

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