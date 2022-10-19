19-10-2022
---
# Computabilidad
## Introduccion
Donde estamos en la materia:
- **Jerarquia** de formalismos en 4 niveles:
*$FA = NFA = NFA_\varepsilon = RE = GR$* $\subset PDA \subset$ *$NPDA = GCF$* $\subset TM = G = NTM$
- Potencia de reconocimiento. Relacion de la **familia de lenguajes** reconocidos {L(FA)}
- TM son las mas potentes (formalismos **maximales**)
- Que relacion hay con los problemas **reales**?
	- Busqueda de cadenas, sistemas de recomendacion, reconocimiento de patrones, busqueda de soluciones a ecuaciones diferenciales, etc.
- Existe algun formalismo mas potente que la TM?
- Las TM son omnipotentes?

### Problemas reales
Con un cambio de interpretacion se puede convertir cualquier problema en un problema de reconocimiento de cadenas

### Formalismo vs Realidad
Una TM puede verse como una computadora cuyo programa esta hard-coded en su $\delta$.

Las computadoras son menos potentes que los FA. *Seccion 8.6.1 y 8.6.2*
- Una computadora (RAM + DIsco) puede reconocer $a^nb^n, n < k$. k depende de la memoria disponible
- Puedo construir un FA que reconozca el mismo patron para cualquier k

Los algoritmos y las TM son equivalentes

## Tesis de Turing/Church
**Parte 1**: No existe formalismo mas potente para el calculo mecanico (numerico discreto === cadena finita) que las TM. **TM = formalismo maximal**

Es decir, si existe formalismo mas potente que la TM, este no realiza calculo mecanico.

**Parte 2**: Todo algoritmo puede ser codificado en terminos de TM o formalismo equivalente.
Relacion: TM $\Leftrightarrow$ Algoritmo

## TM omnipotente
- Para cada problema hay una solucion?
- Para cada lenguaje, hay una TM que lo reconozca?
- Para cada funcion, hay una TM que la computa?

No puede ser que:
- $L(TM) \cap L = \emptyset$ *(no pueden ser conjuntos disjuntos)*
- $L(TM) - L \ne \emptyset$ *(no puede haber problema que este en L(TM) y no en los problemas posibles)*

Lo que puede ser:
- Que los problemas posibles sean los mismos que L(TM)
- Que el conjunto de problemas posibles sea mayor que L(TM) *(la respuesta correcta)*

## Marco teorico (Problemas y TM)
- Cuantas TM existen?
	- Relacion con el alfabeto (entrada, memoria y salida)
- Cuantos problemas existen?
	- Relacion con las funciones

### Cuantas TM existen?
Podemos utilizar cualquier alfabeto
- cuadrado(10) = 100
- cuadrado(11) = 1001

Podemos tener una secuencia infinita de TM