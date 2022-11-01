27-09-2022
---
# Gramaticas

No son formalismos operacionales (no son maquinas)

## Definicion formal
### Elementos
Gramatica $G = <V_N, V_T, P, S>$

$V_N$ = Alfabeto de simbolos no-terminales
$V_T$ = Alfabeto de simbolos terminales
$V = V_N \cup V_T$
$P \subseteq P(V_N^+ \times V^*)$ *Conjunto de reglas (producciones)*
$S \in V_N$ *Start symbol*

### Funcionamiento
$G = <\{S\}, \{a, b\}, P_1, S>$
$P = \{<S, aSb>, <S, ab>\} = \{S \rightarrow aSb, S \rightarrow ab\}$

**Funcionamiento**
*Reemplazar algun lado izquierdo por algun lado derecho (derivacion inmeditata)*
$S \Rightarrow aSb \Rightarrow aaSbb \Rightarrow aaaSbbb \Rightarrow aaaabbbb$
El operador $\Rightarrow$ se puede extender a $\Rightarrow^*$

**Definicion formal**
$x\alpha y \Rightarrow x\beta y$ si $\alpha \rightarrow \beta\in P$

### Uso
Una cadena $x \in V_1^*$ es *generada* por una gramatica $G = <V_N, V_T, P, S>$
Ssi $S^* \Rightarrow^* x$

El lenguaje generado por una gramatica
$L(G) = \{x \ | \ x$ es *generada* por G $\}$

## Ejemplo de gramaticas
$G_2 = <\{S, A, B, C, D\}, \{a, b, c\}, P_2, S>$

$P_2 = \{S \rightarrow aACD, A \rightarrow aAC, A\rightarrow \varepsilon, B \rightarrow b, CD \rightarrow BDc, CB \rightarrow BC, D \rightarrow \varepsilon\}$

$L(G_2) = \{a^nb^nc^n \ | \ n \ge 1\}$

### Mas ejemplos
**$a^nb^n$**
$S \rightarrow aSb$
$S \rightarrow \varepsilon$

**$ww^R$**
$P \rightarrow aPa$
$P \rightarrow bPb$
$P \rightarrow \varepsilon$

**Cantidad par de 0s**
$S \rightarrow 1S \ | \ 0A0S \ | \ \varepsilon$
$A \rightarrow 1A \ | \ \varepsilon$

## Clasificacion de gramaticas
Depende del tipo de produccion (reglas)
$\alpha \rightarrow \beta$

### Gramatica regular
$|\alpha| = 1$
$\beta = aB (a \in V_T, B \in V_N)$
$\beta = a$
$\beta = \varepsilon$

### Gramatica libre de contexto (Context-free)
$|\alpha| = 1$

### Gramatica no restringida (Dependiente del contexto)
*No tiene restricciones aplicable a la forma de las producciones*

## Relacion con los demas formalismos
L(DFA) = L(FA) = L($FA_\varepsilon$) = L(RE) = L(RG)

L(NPDA) = L(CFG)

