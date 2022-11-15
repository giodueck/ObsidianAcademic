15-11-2022
---
# Complejidad

>[!Note]+
> 1. Parte: Modelos
> 2. Parte: Computabilidad (TM)
> 3. Parte: Complejidad (funciones computables)

**Focus**: Funciones computables
Medir la solucion (Medida del problema)
- La complejidad de un problema, se mide a traves de la complejidad de su solucion
- Complejidad y la complicacion no necesariamente van de la mano
	- Simple pero con mucha complejidad (costo): combinatoria
	- Dificil pero de baja complejidad (costo): torres de Hanoi

Fuentes de costo (complejidad)
- Costo de analisis
- Costo de programacion
- Costo de mantenimiento
- **Costo de ejecucion**

## Costo de ejecucion
- Costo temporal:
	Cuanto "tarda" en resolverse el problema
- Costo espacial
	Cuanto "ocupa" al resolverse el problema

Unidades de medida:
- Costo temporal (no se usan segundos)
	- Cantidad de instrucciones ejecutadas (programas C/C++)
	- Cantidad de pasos realizados (TM)
- Costo espacial
	- Cantidad de bytes ocupados (programas, C/C++)
	- Cantidad de celdas ocupadas (TM, todo el contenido significativo, todo el contenido $\ne \textblank$ o hasta la posicion que llega el cabezal)

### Ejemplo: Busqueda secuencial
```c
int busqueda_secuencial(int v[], int n, int busc)
{
	for (int i = 0; i < n; i++)
	{
		if (v[i] == busc) return i;
	}
	return -1;
}
```

#### Analisis de costos
Mejor de los casos:
- El numero buscado se encuentra en la primera posicion
- Costo temporal va a ser una constante (5 instrucciones)

Caso promedio
- Involucra un conocimiento de la distribucion de los datos (no siempre esta disponible)
- No evalua el algoritmo per-se

**Peor de los casos**
- Es el que usaremos
- Para la busqueda secuencial: Se itera por todo el vector y se retorna -1, es decir depende de la longitud n, O(n)

## Conjuncion de conceptos
La complejidad (costo) va a medir el "algoritmo" o la "TM" sin simularlos (analisis estatico del codigo o de la TM)

Costo (temporal o espacial) implica encontrar una funcion dependiente *del tamaño (volumen de datos)* de la entrada
- La funcion recibe como argumento el tamaño de la entrada y su salida es el costo de su *peor caso*
	- Ejemplo de algoritmo de busqueda secuencial:
		- $costo\_secuencial(n) = c_1 + n \cdot c_2$
	- Ejemplo de algoritmo de busqueda binaria
		- $costo\_binario(n) = c_1 + c_2 \cdot n \cdot \log(n)$

## Definicion de complejidad
Teniendo una funcion f (que representa la complejidad/costo) se define una relacion denominada O( ) de la siguiente manera:
- *Orden de funciones*: f es O(g) si $\lim_{n \to \infty} \frac{f(n)}{g(n)} = c$ es una constante real c > 0

### Ejemplos
Algoritmo 1: $20 \times n \times n \rightarrow O(n^2)$
Algoritmo 2: $1 + \frac{n^2}{142} - 20 \times n \rightarrow O(n^2)$
Algoritmo 3: $100 + \log_{10}(n) \rightarrow O(\log(n))$
Algoritmo 4: $400 + n + 500 \log_{10}(n) \rightarrow O(n)$
Algoritmo 5: $\frac{n^5}{10000} \rightarrow O(n^5)$