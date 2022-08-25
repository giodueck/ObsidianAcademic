24-08-2022
---
# Ejercicios Assembly

## strlen
```
	; R0 -> PUNTERO A LA CADENA
	; R0 <- LARGO DE LA CADENA

	MOV R1, #0 ; contador
while
	LDRB R2, [R0], #1
	CMP R2, #0
	BEQ endwhile
	ADD R1, #1
	B while
endwhile
	MOV R0, R1
```