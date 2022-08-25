22-08-2022
---

# Modelos computacionales
- Descripcion de una maquina (operacionales)
- Conceptos matematicos
- Manipulable por medios logicos
- Abstracto

Procesa cadenas, que pueden ser reconocidas o no reconocidas.
Un input incorrecto termina en error, mientras que una cadena procesada completamente y termina con el FA en un estado final es reconocida. 

# Simbologia
- Estado/nodo : circulo
- Estado final: doble circulo
- Transicion: flecha

# JFlap
Para escribir y simular FAs: JFLAP71.jar

# Ejercicios propuestos
Hopcroft -> Seccion 2.2.6

## Marble rolling game
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

[[FA - Marble rolling game|Solucion]]

## Division por 5
Conjunto de todas las cadenas que comienzan con 1 que, cuando se interpretan como un numero binario entero, son divisibles por 5.
E.g. 101, 1111, 1010 pertenecen al lenguaje
0, 111 no pertenecen

### Proceso de resolucion
Pensar en numeros mod 5:
1001 mod 101 = 9 mod 5 = 4
Ya que agregar un bit al final es equiv a x2, y (5+n)x2 = 10 + 2n y el 10 puede ser descartado, el 2n importa.

0 (final) ->
- 0
- 1

1 (inicial) ->
- 10: 2
- 11: 3

10->
- 100: 4
- 101: 5 -> 0

11->
- 110: 6 -> 1
- 111: 7 -> 10

100->
- 1001: 9 -> 4
- 1000: 8 -> 3