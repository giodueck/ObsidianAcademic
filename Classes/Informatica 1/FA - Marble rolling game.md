24-08-2022
---
# FA - Marble rolling game
En el grafico siguiente, los canales cuya entradas son A y B y cuyas salidas son C y D direccionan canicas que entran por A o B. Cuando uno de los paddles x1..3 direcciona una canica, cambia de direccion. Inicialmente estan orientados hacia la izquierda.

Definir un FA que reconozca las cadenas cuyo resultado es que la ultima canica salga por D
```txt
  |  A  |    |  B  |
 /   /x1 \  /   /x3 \
/    /\   \/    /\   \
|   |  |  /x2  |  |   |
\    \/   /\    \/   /
 \   C   /  \   D   /
```

## Proceso de solucion
Existen 8 estados del sistema y con cada input se transiciona de uno a otro. Existen 16 transiciones, una para cada input para cada estado.

Estado | Binario
------ | -------
     0 | 000
     1 | 001
     2 | 010
     3 | 011
     4 | 100
     5 | 101
     6 | 110
     7 | 111

Inicial | Input | Final | Resultado
------- | ----- | ----- | ---------
0 | A | 4 | C
0 | B | 3 | C
1 | A | 5 | C
1 | B | 0 | D
2 | A | 6 | C
2 | B | 1 | D
3 | A | 7 | C
3 | B | 2 | D
4 | A | 2 | C
4 | B | 7 | C
5 | A | 3 | C
5 | B | 4 | D
6 | A | 0 | D
6 | B | 5 | D
7 | A | 1 | D
7 | B | 6 | D

Resultado | Valido
--------- | ------
0 | T
1 | T
2 | A:F B:T
3 | F
4 | A:F B:T
5 | A:F B:T
6 | A:F B:T
7 | F

Asumiendo que 0 marbles -> Valido, se necesitan 12 estados. Si se quieren solo cadenas no vacias, un estado inicial mas se agrega.