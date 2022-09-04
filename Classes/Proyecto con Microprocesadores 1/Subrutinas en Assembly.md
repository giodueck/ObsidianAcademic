30-08-2022
---
# Subrutinas en Assembly
Convertir el assembly siguiente en subrutina (inicializacion de un vector)
```
	MOV R2, #0 ; ctr
	MOV R3, #0 ; const 0
while
	CMP R2, R1
	BGE endwhile
	STR R3, [R0], #4
	ADD R2, #1
	B while
endwhile
```

## Parametros
0: puntero al vector
1: valor
2: cantidad de elementos
## Retorno
ninguno
## Subrutina
```
init_vector
	MOV R3, #0 ; ctr
init_vector_while
	CMP R3, R2
	BGE init_vector_endwhile
	STR R1, [R0], #4
	ADD R3, #1
	B init_vector_while
init_vector_endwhile
	BX LR
```