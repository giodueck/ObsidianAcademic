18-09-2023
---
# APTs - Definiciones y glosario
## APT
Una Amenaza Avanzada Persistente, o APT (Advanced Persistent Threat, por sus siglas en inglés) es un actor sigiloso, típicamente un grupo perteneciente a o apoyado por un estado, que gana acceso no autorizado a una red de computadoras y permanece sin detectarse por un tiempo extendido. 

Una entidad se clasifica como APT si es:
- Avanzada (Advanced): Los operadores detras del grupo *poseen un espectro completo de herramientas de recolección de inteligencia*. Incluyen herramientas propias y open-source, pero pueden también incluir a la organización de inteligencia del estado.
- Persistente (Persistent): Los operadores *poseen objetivos a largo plazo*, y no buscan información oportunísticamente por motivos de ganancia financiera u otros. Este tipo de objetivo *sugiere que el atacante es guiado por una entidad externa*. Los objetivos del atacante necesitan de un acceso permanente al objetivo, y al ser expulsados típicamente reintentan ganar acceso, y lo logran.
- Amenaza (Threat): Los atacantes son una amenaza porque *tienen tanto capacidad como intención*. Son manejados por acciones humanas y no simplemente por código automatizado. Son operadores capacitados, organizados y bien financiados. *No se limitan a grupos apoyados por estados*.

> [!cite]-
> https://www.itgovernance.co.uk/advanced-persistent-threats-apt
> https://www.cybereason.com/blog/advanced-persistent-threat-apt

## Arma Cibernética
Comúnmente se refiere a malware empleado por parte de agencias militares, paramilitares o de inteligencia en un ataque cibernético. Esto incluye, entre otros, virus, trotanos, spyware y gusanos.

A diferencia de malware desarrollado para el crimen cibernético, como adware o ransomware, las armas cibernéticas típicamente son creadas por un APT o actor apoyado por un gobierno y pueden ser altamente selectivas en su objetivo.

> [!cite]-
> https://en.wikipedia.org/wiki/Cyberweapon
> https://www.jstor.org/stable/26427378

## Ciberdelito
Delito cibernético, o ciberdelito, es todo crimen o delito que involucra una computadora o redes de computadoras. Existen varias clases de crimen cibernético, desde fraude y lavado de dinero hasta crímenes financieros, estafas, extorsión, tráfico de drogas y materiales de abuso sexual de niños.

En la mayoría de los casos, el delito se comete con el fin de lucrar. Por lo tanto, en muchos casos, operaciones ejecutadas por APTs son especiales en el mundo del ciberdelito y son más similares al espionaje.

Se hará esta distinción en el resto del documento: una acción es claramente un ciberdelito si busca lucrar o ataca a la sociedad civil sin objetivos militares, de lo contrario típicamente se puede hablar de una guerra o arma cibernética. Aun así, veremos más adelante que esta distinción no siempre se puede hacer claramente.

> [!cite]-
> https://www.britannica.com/topic/cybercrime

## Malware
Malware (*malicious software*, o software malicioso) es cualquier software diseñado para causar disrupción en una computadora, servidor, cliente o red, filtrar información privada, ganar acceso no autorizado, privar de acceso a información, o de otra forma irrumpe en la seguridad o privacidad informática de un usuario.

> [!cite]-
> https://web.archive.org/web/20230110063748/https://www.mecs-press.net/ijeme/ijeme-v8-n2/IJEME-V8-N2-3.pdf

### Ransomware
Malware que *bloquea el acceso a información o sistemas informáticos y amenaza con publicar o destruir dicha información a menos que se pague un rescate*. Ransomware simple puede simplemente bloquear el acceso al sistema operativo sin dañar archivos, pero malware más avanzados usan técnicas de encripción, que efectivamente destruyen la información, y exigen un pago a cambio de la llave.

> [!cite]-
> https://www.theguardian.com/technology/askjack/2016/jul/28/how-can-i-remove-ransomware-infection

### Rootkit
Una colección de software diseñado para dar acceso a una computadora de forma no permitida normalmente. "Root" se refiere al superusuario "root" en sistemas Unix-like, y "kit" al conjunto de herramientas.

Típicamente pueden ocultar su presencia sin dejar de permanecer activos, e incluso pueden proveer una forma de instalar otros tipos de malware sin ser detectados.

> [!cite]-
> https://www.kaspersky.com/resource-center/definitions/what-is-rootkit

### Spyware
Spyware es software de espionage (*spying software*, en inglés). Es todo software con comportamiento maligno que apunta a la recolección de información sobre una persona u organización y enviarla a otra entidad de una forma que hiere al usuario violando su privacidad, amenazando su seguridad, entre otras formas.

Frecuentemente está asociado a software publicitario, y su funcionalidad está incluida en muchas aplicaciones legítimas. Sin embargo, también se emplea en programas varios y malware empleado por gobiernos y APTs.

> [!cite]-
> https://www.bloomberg.com/news/articles/2019-04-10/is-anyone-listening-to-you-on-alexa-a-global-team-reviews-audio
> http://archive.today/2023.02.24-075828/https://www.vice.com/en/article/wnxpjm/nso-group-new-big-player-in-government-spyware
> https://web.archive.org/web/20101226203055/http://www.ftc.gov/os/2005/03/050307spywarerpt.pdf

### Troyano
Cualquier malware que engaña al usuario y *oculta sus intenciones haciéndose pasar por software legítimo*. Su nombre proviene del caballo de Troya.

> [!cite]-
> https://techterms.com/definition/trojanhorse

### Virus
Malware que, una vez ejecutado, se reproduce mediante inyección de código en otro programa. Si es exitoso, se dice que este programa está infectado. Típicamente *requiere de un programa huésped y una acción por parte del usuario*, el virus debe ser ejecutado.

> [!cite]-
> https://www.avast.com/c-worm-vs-virus

### Wiper
Todo malware diseñado para borrar (wipe, en inglés) un medio de almacenamiento de datos.

> [!cite]-
> https://en.wikipedia.org/wiki/Wiper_(malware)

### Worm
Malware independiente que se reproduce para alcanzar a otras computadoras. Típicamente lo hace a través de redes de computadoras, pero puede también hacer uso de medios físicos. A diferencia de un virus, es un programa independiente que *no necesita de interacción con el usuario*.

> [!cite]-
> https://www.avast.com/c-worm-vs-virus

## Ingeniería Social
Cualquier acto que intente o logre influenciar a una persona a actuar de una manera que pueda o no ser de beneficio es un acto de ingeniería social. La principal forma de ingeniería social en la ciberseguridad es el phishing, pero también existen técnicas que involucran hacerse pasar por otra persona, llamadas de voz o mensajes SMS.

> [!cite]-
> https://www.social-engineer.org/framework/general-discussion/social-engineering-defined/

## Phishing
Phishing proviene de "fishing" en inglés, y consiste en una táctica de ingeniería social para "pescar" víctimas mediante un engaño. La forma más típica es mediante un correo electrónico, en el cual el atacante intenta parecer lo más cercanamente posible a algún servicio legítimo o alguna persona de confianza, con el fin de vulnerar a la víctima de alguna forma.

Spear-phishing es una variante del phishing con un enfoque muy preciso en cuanto a su objetivo, mientras que campañas de phishing típicas suelen no ser muy selectivas.

> [!cite]-
> https://www.bbc.com/mundo/noticias-47212337
> https://usa.kaspersky.com/resource-center/definitions/spear-phishing

## Zero-Day
Un Zero-day es una vulnerabilidad en un sistema informático que previamente era desconocida. El nombre se refiere al tiempo que un proveedor conoce la vulnerabilidad.

Zero-days pueden ser explotados mientras no son conocidos por cualquier grupo para cualquier objetivo, incluyendo la infiltración de malware, spyware, o acceso indebido a información. Son mitigados mediante un parche por parte del proveedor, y una vez descubiertos empieza una carrera por el proveedor para lanzarlo.

> [!cite]-
> https://web.archive.org/web/20170704035927/http://www.pctools.com/security-news/zero-day-vulnerability/