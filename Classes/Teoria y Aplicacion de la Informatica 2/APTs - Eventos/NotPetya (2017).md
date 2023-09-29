28-09-2023
---
# NotPetya (2017)

> [!cite]-
> https://www.wired.com/story/notpetya-cyberattack-ukraine-russia-code-crashed-the-world/
> https://www.justice.gov/opa/pr/six-russian-gru-officers-charged-connection-worldwide-deployment-destructive-malware-and
> https://darknetdiaries.com/transcript/54/
> Book: Sandworm: A New Era of Cyberwar and the Hunt for the Kremlin's Most Dangerous Hackers
> https://www.kaspersky.com/blog/new-ransomware-epidemics/17314/
> https://securelist.com/schroedingers-petya/78870/

Antes de la invasión a gran escala, Rusia invadió a Ucrania en 2014 y anexó al territorio de Crimea. Desde entonces, ha estado ocupando el territorio de Donbas y causando sufrimiento para el país ex soviético, que en el pasado se había llamado el granero de la Unión Soviética.

Entre 2014 y 2022 ha regido un caos en el plano cibernético, el cual expertos clasifican como la primera guerra cibernética real. El grupo Sandworm, un APT operado por la unidad militar 74455 de la GRU, el servicio de inteligencia militar de Rusia, ha realizado varios ataques cibernéticos sobre la infraestructura militar y civil de Ucrania. Entre los primeros, están varios ataques destructivos a la red eléctrica del país en 2015 y 2016.

En 2017, Sandworm lanza el virus más tarde denominado "NotPetya" (FOOTNOTE: un ransomware llamado Petya fue usado como la base de este ataque, pero las modificaciones eran substanciales tanto en su forma de destrucción de datos como en su forma de propagación. Por esta razón, Kaspersky lo llamó ExPetr, o NotPetya.) por medio de una actualización maliciosa al programa M.E.Doc, servicio al cual se habían infiltrado unos meses antes. M.E.Doc es un software para el manejo de impuestos en Ucrania, por lo que una infección a este programa resultaría en una infección a la nación entera. Para infectar a las demás computadoras, se empleó una versión modificada de ETERNALBLUE, el mismo exploit usado en WannaCry.

En realidad, NotPetya no era realmente un ransomware, ya que los autores no proveían los datos necesarios para generar una clave de decodificación. Esto significa que en realidad era un *wiper*, con el objetivo de destruir datos y sistemas informáticos a escala masiva, tanto en empresas como instituciones públicas.

Residentes de Ucrania perdieron acceso al pago electrónico del transporte público y la mayoría de los ATMs, supermercados perdieron la habilidad de vender sus productos ya que las cajas se encontraban mostrando una pantalla como en la figura XYZ. Todo servicio conectado directa o indirectamente a internet se vió afectado.

Pero un worm no conoce límites geográficos. Aunque la mayor parte de las infecciones se dieron en Ucrania, Rusia también se vió muy afectada ya que tenía muchas conexiones con Ucrania. Empresas multinacionales con sedes en Ucrania también fueron atacadas.

Uno de los casos más destructivos en empresas es el de Maersk, la empresa de transporte marítimo. Esta perdió la gran mayoría de sus sistemas informáticos, lo que causó filas de decenas de miles de camiones con pedidos que no podían completar, en algunos casos de productos perecederos. Barcos llenos de contenedores llegaban a puertos, pero nadie sabía qué contenido tenían los contenedores. El incidente casi destruyó a la empresa, y causó la reconstrucción total de su infraestructura de TIC.

Andy Greenberg, un experto en el grupo Sandworm, llamó al ataque de NotPetya el más destructivo de la historia. Ataques de esta escala brindan un ejemplo de lo que es la guerra cibernética, y de lo que son capaces los grupos APT cuando tienen acceso a armas cibernéticas de grado militar como lo fue ETERNALBLUE.