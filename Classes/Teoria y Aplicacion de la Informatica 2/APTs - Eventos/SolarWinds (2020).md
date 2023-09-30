30-09-2023
---
# SolarWinds (2020)

> [!cite]-
> https://www.wired.com/story/the-untold-story-of-solarwinds-the-boldest-supply-chain-hack-ever/
> https://www.npr.org/2021/04/16/985439655/a-worst-nightmare-cyberattack-the-untold-story-of-the-solarwinds-hack
> https://web.archive.org/web/20220107190742/https://www.fireeye.com/blog/products-and-services/2020/12/global-intrusion-campaign-leverages-software-supply-chain-compromise.html
> https://www.mandiant.com/resources/blog/evasive-attacker-leverages-solarwinds-supply-chain-compromises-with-sunburst-backdoor
> https://www.youtube.com/watch?v=jxTxGlE9X5s

En diciembre de 2020, Fireeye descubrió una intrusión en sus sistemas que compartió con el mundo. El ministerio de defensa estadounidense inició una investigación relacionada a una brecha similar en sus sistemas, asi también empresas como Microsoft y Mandiant.

La investigación rápidamente concluyó que el actor mostraba señales de ser un grupo ruso, cuyo objetivo era principalmente el ciberespionaje antes que la destrucción. En 2022, Mandiant reveló al actor, llamado *Dark Halo* y *UNC2452*, como APT29, también conocido como Cozy Bear.

Entre marzo y mayo, los atacantes logran infiltrarse en los sistemas de la empresa SolarWinds, la cual provee Orion, un producto de monitoreo de redes. Este producto es usado en muchas empresas importantes de diversos sectores, como Fireeye y Microsoft, y en muchas organizaciones gubernamentales.

El ataque consiste de un troyano de acceso remoto, o RAT. Una actualización se publica con código malicioso, llamado SUNBURST, que permite a los atacantes acceder a cualquier sistema de forma sigilosa. Para evitar que se descubra la manipulación del código, los atacantes incluyeron fragmentos de software en el proceso de construcción de Orion. Esto permitió inyectar el código malicioso sin modificar el código legible por humanos, antes de generar la firma digital que previene la modificación posterior de la herramienta y que asegura que el producto no fue manipulado.

Un ataque de este tipo se denomina un ataque de cadena de suministro, y con los miles de clientes se lograría atacar a muchos objetivos de forma sencilla. Protegerse de este tipo de actores implica, por lo tanto, no solo verificar los sistemas y productos propios de una organización, sino también la verificación de toda herramienta proveída por terceros. Se estima que unos 18.000 clientes fueron infectados, de los cuales alrededor de mil fueron atacados.

Entre las víctimas más importantes se encuentra Fireeye, una empresa de ciberseguridad, que estimó que muchas herramientas de testeo de penetración, es decir herramientas de hackeo, fueron robadas. 

Con ocho meses entre la infección inicial y la detección, el ataque reveló el aumento drástico en las capacidades de APT29. Revela también un nuevo nivel de sofisticación en la seguridad operacional (OPSEC) de grupos adversarios, un alto grado de persistencia y un abordaje cada vez más agresivo a la recolección de información. El presidente de Fireeye afirmó que el ataque a SolarWinds fue uno de los más sofisticados visto en la historia de la empresa.

El presidente de los EE.UU. Joe Biden respondió con medidas y sanciones agresivas de una manera no vista frecuentemente. El ataque fue comparado con Moonlight Maze por varios analistas de seguridad y como una declaración implícita de guerra por otros, reforzando la retórica de disuación por medio de medidas contra actores cibernéticos hostiles. Este tipo de ataques surgen como la mejor, y tal vez la única, alternativa a un ataque convencional, ya que los EE.UU. poseen las fuerzas militares más poderosas del mundo.