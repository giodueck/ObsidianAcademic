19-09-2022
---
# PDA - Teoremas
## Comportamiento
si $<q, x, \varphi> \ \vdash^* \ <q', \varepsilon, \varphi'>$ 
entonces $<q, x$*$y$*$, \varphi> \ \vdash^* \ <q',$ *$y$*$, \varphi'>$

si $<q, x, \varphi> \ \vdash^* \ <q', x', \varepsilon>$
entonces $<q, x, \varphi$*$\beta$*$> \ \vdash^* \ <q', x',$ *$\beta$*$>$

*Combinando:*
si $<q, x, \varphi> \ \vdash^* \ <q', \varepsilon, \varepsilon>$
entonces $<q, x$*$y$*$, \varphi$*$\beta$*$> \ \vdash^* \ <q',$ *$y$*$,$ *$\beta$*$>$

### Ejercicio
Demostrar que $L(A) = T = \{a^nb^{2n} \ | \ n \ge 1\}$

Parte 1) $T \subseteq L(A)$ *toda cadena con el patron deseado es reconocida*

$<q_0, a^nb^{2n}, Z> \ \vdash^* \ <q_2, \varepsilon, Z>, n \ge 1$

1.a) $<q_0, a, Z> \ \vdash \ <q_0, \varepsilon, \$\$Z>$
1.b) $<q_0, a^m, \$> \ \vdash^* \ <q_0, \varepsilon, \$^{2m}\$>, m \ge 0$
1.c) $<q_0, b, \$> \ \vdash \ <q_1, \varepsilon, \varepsilon>$
1.d) $<q_1, b^m, \$^m> \ \vdash \ <q_1, \varepsilon, \varepsilon>, m \ge 0$
1.e) $<q_1, \varepsilon, Z> \ \vdash \ <q_2, \varepsilon, Z>$

#todo continuar (fotos)

## Limitaciones
No existe PDA que reconozca:
- $ww^R$. $w \in \{a, b\}^*$ *$w^R$ es la reversa de $w$*
- el lenguaje $L = \{a^nb^nc^n | n > 0\}$
- el lenguaje $wcw$
- el lenguaje $L = \{a^nb^m \ | \ n > 0, m = n \ \vee \ m = 2n\}$. *Esto implica que los lenguajes reconocidos PDAs no son cerrados con respecto a la UNION*
Son cerrados al complemento respecto a $\Sigma^*$ (ver construccion en Ghezzi)