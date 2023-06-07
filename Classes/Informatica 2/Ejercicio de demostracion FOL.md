05-06-2023
---
# Ejercicio de demostracion FOL

## Estudiantes

1. Los estudiantes juegan tenis, futbol o ajedrez
2. Todo lo que sea ajedrez no es vigoroso
3. Todos los que son saludables juegan algo vigoroso
4. Todos los que juegan ajedrez no juegan futbol
5. Conclusion: Si todo estudiante es saludable, entonces todo estudiante que juega ajedrez juega tenis

### Desarrollo

1. $\forall X \ estudiante(X) \rightarrow (juega(X,ajedrez) \ \vee \ juega(X,tenis) \ \vee \ juega(X,futbol))$
2. $\forall X \ ajedrez(X) \rightarrow \neg vigoroso(X)$
3. $\forall X \ saludable(X) \rightarrow \exists Y \ juega(X,Y) \ \wedge \ vigoroso(Y)$
4. $\forall X \ juega(X,ajedrez) \rightarrow \neg juega(X,futbol)$
5. $\forall X \ estudiante(X) \ \wedge \ saludable(X) \rightarrow (\forall Y \ ajedrez(Y) \ \wedge \ juega(X,Y) \rightarrow juega(X,tenis))$