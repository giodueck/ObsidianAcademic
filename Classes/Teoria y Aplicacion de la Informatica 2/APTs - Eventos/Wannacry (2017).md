27-09-2023
---
# Wannacry (2017)

> [!cite]-
> https://darknetdiaries.com/transcript/73/
> https://www.justice.gov/opa/pr/north-korean-regime-backed-programmer-charged-conspiracy-conduct-multiple-cyber-attacks-and
> https://www.mandiant.com/resources/blog/wannacry-malware-profile

En mayo de 2017, el ciberataque más devastador hasta entonces empezó. Un ransomware llamado WannaCry, usando el exploit ETERNALBLUE, se estaba propagando por las computadoras de organizaciones e individuos, encriptando archivos, y demandando un pago por la recuperación de la información.

ETERNALBLUE, una de las ciberarmas de la NSA robadas por los Shadow Brokers, se aprovecha de una vulnerabilidad de ejecución remota de código en el protocolo de transferencia de archivos SMB en Windows. MS17-010, como la llamó Microsoft, es una vulnerabilidad tan severa que hasta productos viejos sin garantía de soporte recibieron un parche para mitigarla, y WannaCry demostró por primera vez esta severidad a gran escala.

Dentro de pocos minutos, el virus es capaz de infectar una organización entera. Entre las afectadas está la NHS, el servicio nacional de la salud del Reino Unido. Este se vió obligado a desconectar a varios hospitales del internet, varios otros tuvieron que suspender sus actividades o continuarlas en papel y pizarras. 

El virus consiste de dos módulos: un gusano, que mediante ETERNALBLUE se propaga a nuevas máquinas, descarga y ejecuta las herramientas para ejecutar el ataque sobre los archivos, y las herramientas de encripción, que causan un daño crítico a los archivos de una computadora. Finalmente, una pantalla de ransomware informa a la víctima de su destino y propone las instrucciones para la decodificación de sus archivos: un pago de US\$ 300 a US\$ 600 en Bitcoin.

Sin embargo, el virus posee un punto débil. Un *killswitch*, un interruptor de apagado, que consiste en una prueba de conexión a una URL de nombre aparentemente aleatorio. Cuando un analista independiente registra el nombre de dominio unas horas luego del inicio del ataque, encuentra que al lograr conectarse, el virus desactiva la herramienta de encripción y detiene el ataque. Múltiples versiones aparecieron luego de activarse el killswitch, tanto con un URL diferente como sin killswitch, pero ya no llegaron a causar el mismo impacto que la primera oleada.