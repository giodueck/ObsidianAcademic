23-08-2022
---
# Control de flujo en Assembly

## IF
C:
```c
if (R0 == 0)
	R1 = R2 + R3;
else
	R1 = R2 - R3;
```

ARM Assembly:
```
	CMP R0, #0
	BEQ if
; else
	SUB R1, R2, R3
	B endif
if
	ADD R1, R2, R3
endif
```

## WHILE
C:
```c
while (R0 != R1)
	R1 = R1 + 1;
```

ARM Assembly:
```
while
	CMP R0, R1
	BEQ endwhile
	ADD R1, #1
	B while
endwhile
```

## Ejercicios
Inicializar un vector cuyos elementos son de 32 bits a cero.
R0 -> direccion del primer elemento del vector
R1 -> cantidad de elementos del vector

Using pointer arithmetic (modifying pointer)
```c
int32_t ctr = 0;

while (ctr < R1)
{
	*R0 = 0;
	R0++;
	ctr++;
}
```

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

Using array notation (no modification of the pointer)
```c
int32_t ctr = 0;

while (ctr < R1)
{
	R0[ctr] = 0;
	ctr++;
}
```

```
	MOV R2, #0 ; ctr
	MOV R3, #0 ; const 0
	MOV R4, R0 ; copia de R0, a ser incrementada
while
	CMP R2, R1
	BGE endwhile
	STR R3, [R4], #4
	ADD R2, #1
	B while
endwhile
```
