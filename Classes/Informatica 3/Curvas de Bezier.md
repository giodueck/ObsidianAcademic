01-09-2023
---
# Curvas de Bézier

## Contenido
- Curvas de Bézier
	- Que son
	- Construcción recursiva (Metodo de Casteljau)
	- Algoritmo de Bézier
	- Demostración

## Curvas de Bézier
### Qué son
Son curvas paramétricas usadas en gráficos y campos relacionados.

Proveen una forma concisa de representar curvas por medio de ciertos puntos de control.

Son usadas en gráficos vectoriales para representar curvas o "caminos" infinitamente escalables y superar las limitaciones de gráficos rasterizados.

### Construcción recursiva
Método de Casteljau

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

## Algoritmo de Bézier
Dada $t$ que varía de 0 a 1:
$B(t) = \sum_{i=0}^{n} \binom{n}{i} (1-t)^{n-i} t^i P_i$

#### Curvas lineales
$B(t) = (1-t) P_0 + t P_1$

#### Curvas cuadráticas
$B(t) = (1-t)^2 P_0 + 2(1-t) t P_1 + t^2 P_2$

#### Curvas cúbicas
$B(t) = (1-t)^3 P_0 + 3(1-t)^2 t P_1 + 3 (1-t) t^2 P_2 + t^3 P_3$

## Demostración
```cpp
for (float t = 0; t <= 1; t += interval)
{
	// p = (1-t)*(1-t)*points[0] + 2*t*(1-t)*controlPoints[1] + t*t*points[2];

	p = {0, 0};

	for (int i = 0; i <= n; i++)
	{
		p += binomial(n, i) * powf((1-t), n - i) * powf(t, i) * points[i];
	}
	
	Draw(p);
}
```