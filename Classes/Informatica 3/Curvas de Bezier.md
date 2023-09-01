01-09-2023
---
# Curvas de Bézier

## Contenido
- Curvas de Bézier
	- Que son
	- Construcción intuitiva (Metodo de Casteljau)
	- Algoritmo de Bézier
	- Ejemplo Cuadrático puntual
	- Demostración
- Introducción a PGE
	- Hello World
	- Métodos para pintar pixeles
	- Métodos para captar entradas
	- Explicación del codigo

## Curvas de Bézier
### Qué son
Son curvas paramétricas usadas en gráficos y campos relacionados.

Proveen una forma concisa de representar curvas por medio de ciertos puntos de control.

Son usadas en gráficos vectoriales para representar curvas o "caminos" infinitamente escalables y superar las limitaciones de gráficos rasterizados.

### Construcción intuitiva
Método de Casteljau: definido recursivamente

#### Curvas lineales
Dada $t$ que varía de 0 a 1 y los puntos de control $P_0$ y $P_1$:
- $Q(t)$ se traslada linealmente de $P_0$ a $P_1$

El trayecto de $Q(t)$ representa la curva.

![[Bézier_1_big.gif]]

#### Curvas cuadráticas
Dada $t$ que varía de 0 a 1 y los puntos de control $P_0$, $P_1$ y $P_2$:
- $Q_0(t)$ varía linealmente de $P_0$ a $P_1$
- $Q_1(t)$ varía linealmente de $P_1$ a $P_2$
- $R(t)$ varía linealmente de $Q_0(t)$ a $Q_1(t)$

El trayecto de $R(t)$ representa la curva.

![[Bézier_2_big.gif]]

#### Curvas cúbicas
Se sigue el patrón: se definen puntos que varían a la medida que varía $t$, que a su vez definen nuevos segmentos, y se repite el proceso hasta llegar a un punto.

![[Bézier_3_big.gif]]