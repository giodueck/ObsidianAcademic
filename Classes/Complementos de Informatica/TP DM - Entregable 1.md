08-09-2023
---
# TP DM - Entregable 1

## Prediccion de fraude: Datos abiertos de Aduana
https://www.aduana.gov.py/?page_id=14523

### Problema
Se estima que los ingresos perdidos a causa de fraudes varios son del 50%. Es decir que se podrian aumentar los ingresos al doble de lo que son ahora. Un modelo de prediccion de fraude a nivel de despacho podria reducir la cantidad de ingresos no percibidos.

#### Objetivos
Predecir despachos potencialmente fraudulentos y evaluarlos en un semaforo, en donde rojo indica una cierta certeza de fraude, verde indica una cierta certeza de ausencia de fraude, y amarillo indica una prediccion incierta.

Las evaluaciones verdes y rojas deberian minimizar las predicciones faltas, en aprticular los falsos positivos. Los falsos negativos no crean costos adicionales, pero los falsos positivos pueden causar gastos por investigaciones sobre despachos honestos.

#### Observaciones
Usar datos de dos meses

### Aduana
La resolución N° 978/22 de la DNA establece la misión, la visión y la declaración de propósito de la Aduana.

#### Misión
> Somos una institución autónoma, facilitadora del comercio internacional, responsable de una eficiente recaudación de los tributos, investida de competencia para la aplicación de la legislación aduanera en la fiscalización y control del ingreso, egreso, circulación de mercaderías, medios de transportes, unidades de cargas, depósitos y personas, comprometidos con la rendición de cuentas al ciudadano para el desarrollo del país

\- RESOLUCIÓN DNA N° 978/22

#### Visión
> Ser una institución líder nacional e internacionalmente, sustentada en su gestión, infraestructura, tecnologia de vanguardia y talento humano competente, comprometido e íntegro

\- RESOLUCIÓN DNA N° 978/22

#### Declaración de Propósito
> - Seremos una institución que liderará las mejoras al comercio exterior del Paraguay reconocidos internacionalmente por su modelo de gestión y mejores prácticas aduaneras
> - Con normativa clara y actualizada, con procedimientos predecibles, ágiles ajustados a estándares de Gobiemo Electrónico basados en la innovación, la automatización y la eliminación de la discrecionalidad
> - Realizaremos un control de las mercaderías, personas, medios de transporte y unidades de carga en base a la gestión de riesgos, impulsando la facilitación del comercio, seguridad en la cadena logística, la competitividad, conectándonos con nuestros grupos de interés y protegiendo a Ia sociedad paraguaya en general, contribuyendo de esta manera al desarrollo y estabilidad económica del país
> - Buscaremos acrecentar la capacitación a los funcionarios para reconoccr y valorar su dedicación, honestidad, intcgridad y entrega. Y nos reconocerán como servidores públicos, íntegros e inflexibles ante la corrupción

\- RESOLUCIÓN DNA N° 978/22

### Valoración de la situación
#### Inventario de recursos
La aduana cuenta con una colección de datos abiertos sobre despachos para cada mes. Actualmente se registran alrededor de 350,000 despachos por mes, clasificados por importacion o exportacion, despachante, rubro de la mercaderia, fechas y montos relacionados al despacho, entre otros datos.

#### Requisitos, supuestos y restricciones
**Requisitos**: Detección y prevencion de un 20% de los casos de fraude en la Aduana.

**Supuestos**: La DNA cuenta con la capacidad para accionar sobre una mayor cantidad de supuestos fraudes.

**Restricciones**: Las operaciones de la Aduana deben seguir con el tiempo operativo dentro del 5% de los tiempos actuales. La cantidad de falsos positivos no debe superar un margen de error del 5% del total de positivos. 

#### Riesgos y contingencias
Costes por investigacion de fraude

Costes de los falsos positivos

#### Costes y beneficios
Ingresos actuales y una deteccion del 20% de fraudes

Costes adicionales por deteccion de fraudes

### Determinar objetivos de DM
#### Metas de Data Mining
Segmentar los despachos para encontrar anomalías y por lo tanto posibles fraudes.

#### Criterios de éxito de Data Mining
Se considerará un éxito la detección de un porcentaje mayor al margen de error de casos anómalos y una fidelidad significante para casos designados como posibles fraudes.