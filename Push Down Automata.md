13-09-2022
---
# PDA - Introduction
Los DFA, FA, RE tienen memoria limitada, no recuerdan como llegaron al estado actual.

PDA = FA + Almacenamiento infinito
PDA = FA + Pila de capacidad infinita

## Diferencias principales con los FA
- Puede realizar movimientos con los datos de la pila sin tener en cuenta la entrada (movidas nulas)
- El movimiento depende del estado, de la entrada u del simbolo en el tope de la pila

## Ejercicios
#todo 
Diseñar PDA que reconozcan los siguientes lenguajes
$\{a^nb^m \ | \ m > n, m \ge 0\}$
$\{a^nb^m \ | \ m < n, m > 1\}$
$\{a^nb^m \ | \ m \ne n, m > 1\}$
 $\{wcw^R \ | \ m \ne n, n > 1, m > 1\}$
 $\{a^nb^mc^md^n \ | \ n \ge 0, m \ge 0\}$
 Misma cantidad de a y b en cualquier orden