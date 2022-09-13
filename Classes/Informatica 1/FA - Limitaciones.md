12-09-2022
---
# FA - Limitaciones
## Teorema
No existe DA (o formalismo equivalente) que reconozca el lenguaje $L = \{a^nb^n \ | \ n \ge 0\}$

### Demostracion - Reduccion al absurdo (por contradiccion)
- Asumimos que existe un FA que reconoce $L = \{a^nb^n \ | \ n \ge 0\}$

Si existe tal FA, entonces existen dos numeros diferentes enteros diferentes ($n_1 \ne n_2$) tal que $\delta^*(q_0, a^{n_1}) = \delta^*(q_0, a^{n_2})$

Como $\delta^*(q_0, a^{n_1}b^{n_1}) = \delta^*(\delta^*(q_0, a^{n_1}) , b^{n_1}) = \delta^*(\delta^*(q_0, a^{n_2}) , b^{n_1}) \in F$ entonces reconoce $a^{n_2}b^{n_1}$

$\therefore$ no existe este FA

- Existe un FA B tal que $\forall n > 0, x = a^nb^n \rightarrow x \in L(B)$?
- Que parte de la definicion del FA debera cambiarse para que reconozca el lenguaje $x = a^nb^n$?

