26-09-2023
---
# Stuxnet (2010)

> [!cite]-
> https://darknetdiaries.com/transcript/29/
> https://www.washingtonpost.com/world/national-security/stuxnet-was-work-of-us-and-israeli-experts-officials-say/2012/06/01/gJQAlnEy6U_story.html
> https://www.nytimes.com/2012/06/01/world/middleeast/obama-ordered-wave-of-cyberattacks-against-iran.html
> Book: Countdown to Zero Day: Stuxnet and the Launch of the World's First Digital Weapon - by Kim Zetter
> https://web.archive.org/web/20190709162859/https://www.symantec.com/content/en/us/enterprise/media/security_response/whitepapers/w32_stuxnet_dossier.pdf
> https://www.infoworld.com/article/2626009/is-stuxnet-the--best--malware-ever-.html

Stuxnet es el malware más sofisticado jamás encontrado. Según varios reportes, es la obra de las agencias de inteligencia de los Estados Unidos e Israel, y es generalmente considerada la primera arma cibernética y el incidente que inició la era de la guerra cibernética.

Las versiones más antiguas descubiertas datan a junio de 2009. Sin embargo, la versión descubierta en 2010 hacía uso de varios *exploits* (FOOTNOTE del inglés, fragmento de software utilizado en la explotación de una vulnerabilidad de software) críticos de Microsoft Windows y poseía capacidades impensables para la época. Con un total de cuatro zero-days, Stuxnet tiene una complejidad incomparable. Donde un malware común normalmente emplea tácticas de ingeniería social y no más de un zero-day, aquí se emplean cuatro en un solo ataque.

\

La misión de Stuxnet era una de sabotaje como alternativa a un conflicto tradicional. Los EE.UU. habían descubierto que Irán, por medio de un físico llamado A.Q. Khan en Pakistan, lanzó un programa de enriquecimiento nuclear entre 1998 y 1999 y comenzó a comprar diseños para una fábrica de centrífugas. La CIA y la inteligencia británica habían infiltrado la cadena de suministro de A.Q. Khan y lograron interceptar un envío de centrifugas a Libia. En 2004, la Agencia Internacional de Energía Atómica de las Naciones Unidas investigó al programa libio y la CIA adquirió los materiales del programa.

Las centrífugas se estudiaron extensivamente, lo que permitió crear un virus sigiloso que es capaz destruir equipamiento industrial físico, por primera vez en la historia. Con estos hallazgos, las administraciones del presidente Bush y más tarde la del presidente Obama aprobaron el programa, que fue nombrado Operación *Olympic Games* (Juegos Olímpicos).

La versión inicial, sin embargo, tenía una falta: no lograba alcanzar a todas las computadoras necesarias, las que controlaban al sistema de control industrial. Por este motivo se agregaron exploits agresivos que permitieron al virus (1) esparcirse por la red local de una máquina infectada, (2) obtener privilegios elevados y (3) esconder la presencia y acciones del sistema operativo. 

El ataque inició con una infiltración física del malware a la planta nuclear Natanz, que se encuentra en una zona remota y desconectada de internet. Una vez que Stuxnet logra infectar a la primera máquina, infecta rápidamente a toda computadora con Windows en la red en busca de instalaciones de software Siemens para el control de las centrífugas. Una vez encontradas estas computadoras críticas, monitorea el comportamiento normal de los sistemas de control antes de interferir en su operación.

Stuxnet era capaz de alterar las frecuencias a las que operaban las centrífugas; al mismo tiempo reportaba frecuencias normales al sistema de monitoreo. De esta forma, las centrífugas se desgastan y hasta autodestruyen mucho más rápidamente. Se estiman que alrededor de 1.000 centrífugas fueron dañadas durante la operación, y el gas de uranio que contenían, desperdiciado.

El virus finalmente fue descubierto por analistas de VirusBlokAda, un proveedor de antivirus, al escapar de la planta por medio de una computadora transportada fuera del predio. Un reporte por Symantec luego afirmó que computadoras alrededor del mundo habian sido infectadas, con la gran mayoría de ellas en Irán. Se reportaron también que varios de los exploits utilizados ya se habían encontrado anteriormente por otras operaciones del APT Equation Group, por lo cual el ataque les fue atribuído.

Stuxnet inició debates sobre la guerra en el plano de la información. Fue la primera vez que un virus mostró la capacidad de subvertir sistemas de control industrial de manera tan sofisticada. Hasta este punto, la guerra cibernética no se había definido. El hecho de ser un ataque cibernético otorga cierta negación plausible (que no es posible con un ataque con misiles o bombas), y tampoco es claro si un ataque cibernético constituye un acto de guerra.