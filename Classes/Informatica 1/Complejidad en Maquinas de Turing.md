15-11-2022
---
# Complejidad en Maquinas de Turing

Costo temporal = cantidad de cambios de configuracion que se realizan
- $C_0 \vdash C_1 \vdash C_2 \vdash ... \vdash C_I$ (son los cambio de configuracion que se dieron durante la ejecucion de la TM con la entrada en particular x)
- $T_M(x) = t$ (el costo temporal de la TM M al operar sobre el input x es t)

Costo espacial = cantidad de celdas ocupadas *(donde podemos cortar las cintas sin que la TM se de cuenta)*
- Todas las cintas de memoria tienen una estructura comun
	- $\alpha_{ij}A_{ij}B_{ij}$ donde "i" indica el numero de cinta y "j" indica que configuracion es
	- $S_M(x) = \Sigma_{i = 1}^k \max\{|\alpha_{ij}| + 1, 0 \le j \le t\}$

$T_M(x) =$ costo temporal asociado a la TM M al procesar el input "x"
$S_M(x) =$ costo espacial asociado a la TM M al procesar el input "x"

Siempre se busca asociar el costo al "volumen de datos"
$T_M(n) = \max\{T_M(x) \ | \ |x| = n\}$
$S_M(n) = \max\{S_M(x) \ | \ |x| = n\}$

## Ejemplo de calculo de complejidad de una TM
Diseñar una TM que reconozca $a^ib^ic^i$ para $n \ge 0$
#incomplete ppt: revisar, no va a salir en el examen pero es importante saber

