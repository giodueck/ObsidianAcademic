12-09-2023
---
# Practica 2 - MOF y OCL
## Ideas
Metamodelo para sistemas de seguimiento y abordaje de problemas en infraestructura pública.

Ideas principales:
- Problema
- Daños
- Orden de trabajo
- Equipo de trabajo
- Equipamiento
- Materiales
- Usuario
- Empleado

Ideas abstraídas:
- Ticket
- Orden
- Usuario
- Clase

## MOF
Componentes:
- Ticket
- Orden
- Usuario
- Clase (comodín)
- Enum
- Asociaciones

## OCL
Restricciones:
- Una orden siempre se relaciona con un reporte.
- Un reporte esta relacionado con al menos un usuario.
- Además de eso, clases pueden tener cualquier numero de sub o superclases.
- Clases tienen propiedades
