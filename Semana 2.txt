## Ataques de ciberseguridad pasados

Muchos de los ataques no son del todo nuevos, los atacantes alteran o mejoran métodos anteriores.
Comprender los ataques pasados, puede orientarnos acerca de cómo manejar o investigar incidentes en tu trabajo como analista de seguridad. 

### Términos:

`computer virus:` Un virus informático es un código malicioso, escrito para interferir con las operaciones informáticas y causar daños a los datos y el software. El virus de adhiere a programas o documentos en una computadora. Luego se propaga e infecta una o más computadoras en una red. Un `worm o gusado` es un tipo de virus informático que puede duplicarse y propagarse por su cuenta, sin participación humana.
Hoy en día, los virus son más conocidos como software malicioso, `malware` que es un software diseñado para dañar dispositivos o redes.

### Dos ataques tempranos de software malicioso o `malware`:

#### El virus Brain y el gusano Morris (Brain virus or Morris worm)

Fueron creados por desarrolladores de software malicioso para cumplir tareas específicas. Sin embargo, los desarrolladores subestimaron el impacto que su `malware` tendría y la cantidad de computadoras que este iba a afectar.

En 1986, los hermanos Alvi crearon el `brain virus` si bien la intención del virus era rastrear copias ilegales de software médico y evitar las licencias piratas lo que el virus terminó haciendo fue inesperado.
Una vez que una persona usaba una copia pirata del software el virus infectaba esa computadora. Luego, cualquier disco que se insertara en la computadora también se infectaba. El virus se propaga a una computadora nueva cada vez que alguien usaba uno de los discos infectados. Desapercibido, se propagó por todo el mundo en un par de meses. aunque la intención no era destruir datos o hardware, el virus ralentizó la productividad e impactó significativamente en las operaciones comerciales. 
El brain virus alteró radicalmente la indrustria informática. Destacó la necesidad para mantener la seguridad y productividad.

Otro ataque a computadoras influyente fue `Morris worm`. En 1988, Robert Morris desarrolló un programa para calcular el tamaño de internet y se instaló en otras computadoras para calcular el número de equipos conectados a internet. Sin emabrgo, el programa no logró hacer un seguimiento de las computadoras que ya había puesto en riesgo, y seguía reinstalándose hasta que las computadoras se quedaron sin memoria y colapsaron. Cerca de 6000 computadoras se vieron afectadas lo cual representaba el 10% de internet en ese momento. Este ataque costó millones de dólares en daños debido a alteraciones en las empresas y a los esfuerzos necesarios para eliminar el gusano. Después del `morris worm` se establecieron equipos de respuesta ante emergencias informáticas, conocidos conocidos como CERT. Para responder a incidentes de seguridad informática. Los CERT aún existen, pero su lugar en la industria de la seguridad se amplió, e incluye más responsabilidades. 

### Ataques en la era digital

Los agentes de amenaza ya no nececistaban de discos físicos para propagar virus. Analizaremos dos ataques notables que dependieron de internet: `Loveletter attack` y `la fuga de información de Equifax`.
En el año 200, Onel De Guzmán creó el malware `LoveLetter` para robar credenciales de inicio de sesión en internet. Este ataque se extendió rápidamente y se aprovechó de personas que no habían aprendido a sospechar de los correos electrónicos no deseados. 
Los usuarios recibieron un correo con un "
te ami" en el asunto. Cada correo contenía un archivo adjunto titulado "Carta de amor para tí". Al abrir el archivo adjunto el software malicioso escaneaba la libreta de direcciones de un usuario.
Luego, se enviaba automáticamente a casa persona en la lista a cada persona en la lista e instalaba un programa para recopilar información de usuario y contraseñas. Las personas pensaban que recibían un correo de un amigo, pero en realidad era software malicioso, `LoveLetter` terminó infectando a 45 millones de computadoras y se cree que causó daños por más de 10 mil millones de dólares. El ataque de `LoveLetter` es el primer ejemplo de ingeniería social. 


### Social engineering

La ingeniería social es una manipulación técnica que explota el error humano para obtener información privada, acceso u objetos de valor. Luego, los atacantes entendieron el poder de la ingeniería social. EL número de ataques de ingeniería social aumenta con cada nueva aplicación de redes sociales que permite acceso público a los datos de personas.
Hoy se prioriza muchisimo la conveniencia sobre la privacidad. El resultado de este cambio evolutivo es que estas herramientas pueden derivar en una vulnerabilidad mayor si no se usan apropiadamente. Como profesional de la seguridad, tu rol es identificar y gestionar un uso inapropiado de la tecnología que pueda poner a tu organización y todas las personas asociadas a ella en riesgo. Una forma de proteger a tu organización son las capacitaciones internas regulares. Como futuro analista de seguridad, puede que se te pida que la dirijas o que pariticipes de ellas. Hoy en día, es común que se capacite a los empleados acerca de cómo identificar ataques de ingeniería social.
Específicamente el `pishing` a través de correos que reciben. 
El `pishing` es el uso de comunicaciones digitales para engañar personas y provocar que revelen datos confidenciales o para propagar software malicioso.

### Fuga de información de Equifax

En 2017, atacantes se filtraron con éxito en la agencia de infromes de crédito Equifax. Esto dio lugar a una de las fugas de información más grandes de las que se tenga registro. Se robaron maás de 143 millones de registros de clientes, y la fuga afectó a casi el 40% de todos los estadounidenses. Los registros contenían información personal identificable como números de seguridad social, fechas de nacimiento, licencias de conducir, domicilios y números de tarjetas de crédito. Desde el punto de vista de la seguridad la duga se produjo debido a múltiples fallas por parte de Equifax.
No fue una única vulnerabilidad que los atacantes aprovecharon, sino varias. La empresa no tomó las medidas necesarias para reparar múltiples vulnerabilidades conocidas en los meses previos a la fuga. Al final, Equifax llegó a un acuerdo con el gobierno de los EE.UU y pagó más de 575 millones de dólares para resolver reclamos de los clientes y cubrir las multas requeridas. 
Al observar tendencias, patrones y métodologías similares tal vez puedas identificar una posible fuga y limitar daños futuros.


### Pishing

Phishing es el uso de comunicaciones digitales en las que se suplanta la identidad de una persona o empresa con el objetivo de engañar a otras personas para que revelen datos confidenciales o implementen un software malicioso.

Algunos de los tipos más comunes de ataques de phishing actuales son: 

Compromiso del correo electrónico empresarial (BEC): el agente de amenaza envía un mensaje de correo electrónico que parece provenir de una fuente conocida, para efectuar una solicitud aparentemente legítima de información o intentar que realice una acción, con el fin de obtener un beneficio financiero.

Phishing localizado (Spear phishing): un tipo de phishing focalizado en el que se envía un correo electrónico malicioso a un/a usuario/a o a un grupo de usuarios/as específicos/as, que parece provenir de una fuente confiable.

Ataque “caza de ballenas” (Whaling): un tipo de phishing localizado mediante el cual los agentes de amenaza buscan acceder a los datos confidenciales de ejecutivos/as de una empresa.

Vishing: un tipo de estafa por suplantación de identidad en la que se busca obtener información sensible a través de una llamada telefónica.

Smishing: ataque de phishing por SMS que implica el uso de mensajes de texto para engañar a los/las usuarios/as, con el fin de obtener información confidencial o hacerse pasar por una fuente conocida.

### Software malicioso

El software malicioso es un software diseñado para dañar dispositivos o redes. El propósito principal de quienes realizan el ataque es obtener dinero o, en algunos casos, información que pueda utilizarse en contra de una persona, una organización o un territorio. 

Algunos de los tipos más comunes de ataques de software malicioso actuales son: 

Virus informático: un código malicioso creado para interferir con las operaciones de la computadora y dañar datos, software y hardware. El virus se instala en programas o documentos de una computadora y luego, se propaga e infecta una o más computadoras en una red.

Gusano: un software malicioso que puede duplicarse y propagarse por sí mismo en los sistemas. 

Ransomware (secuestro de datos): un ataque malicioso en el que los agentes de amenaza cifran los datos de una organización y exigen un pago (rescate) para restablecer el acceso a ellos. 

Spyware: un tipo de software malicioso que se usa para recabar y vender información sin consentimiento. El spyware se puede usar para acceder a dispositivos, lo cual permite a los agentes de amenaza recopilar datos personales, como correos electrónicos, mensajes de texto, grabaciones de voz e imagen y ubicaciones de índole privada.

### Ingeniería social

La ingeniería social es una técnica de manipulación que aprovecha errores humanos para obtener información privada, acceso a sistemas o bienes de valor. A menudo, los errores humanos se deben al exceso de confianza en alguien. La misión de un agente de amenaza que actúa como ingeniero social es crear un entorno de confianza falso y mentir para aprovecharse del mayor número posible de gente. 

Algunos de los tipos más comunes de ataques de ingeniería social actuales son:

Ataque de suplantación de identidad en redes sociales (Phishing en redes sociales): un tipo de ataque en el que el agente de amenaza contacta a la víctima en alguna red social, con el fin de robar información personal o tomar el control de la cuenta.

Ataque de “agujero de agua”: un agente de amenaza ataca un sitio web visitado con frecuencia por un grupo específico de usuarios/as.

Cebo USB: un agente de amenaza deja estratégicamente una unidad USB que contiene software malicioso para que un/a empleado/a la encuentre y la instale, con el fin de causar la infección involuntaria de una red. 

    Ingeniería social física: un agente de amenaza se hace pasar por una persona ligada a la empresa para obtener acceso no autorizado a una ubicación física.

### Principios de la ingeniería social

La ingeniería social es asombrosamente eficaz porque las personas suelen ser confiadas y tienen muy arraigado el respeto a la autoridad. La cantidad de ataques de ingeniería social aumenta a medida que crece la cantidad de aplicaciones de redes sociales que permiten el acceso público a los datos de las personas. Aunque compartir datos personales (como tu ubicación o fotos) puede ser conveniente, también plantea un riesgo.

Los motivos por los cuales los ataques de ingeniería social son eficaces son:

Autoridad: los agentes de amenaza se hacen pasar por personas con autoridad porque los individuos suelen respetarlas. 

Intimidación: los agentes de amenaza utilizan tácticas de hostigamiento, como asustar a las víctimas para que sigan sus órdenes. 

Consenso/prueba social: como las personas a veces hacen cosas convencidas de que otras también las hacen, los agentes de amenaza utilizan esta confianza en los demás para dar una impresión de legitimidad. Por ejemplo, para obtener acceso a datos privados, un agente de amenaza puede decir a un/a empleado/a que otros miembros de la empresa ya le han otorgado el acceso en otras ocasiones.

Escasez: el agente de amenaza le da a entender a la persona que existe disponibilidad limitada de ciertos bienes o servicios, para convencerla de hacer algo.

Familiaridad: los agentes de amenaza establecen falsos lazos emocionales con los/las usuarios/as de quienes desean aprovecharse,para lograr su objetivo.  

Confianza: los agentes de amenaza establecen una relación afectiva con los/las usuarios/as, que les permite aprovecharse de ellos con el paso del tiempo. Hacen uso de esta relación para ganarse la confianza de la víctima y acceder a su información personal.

Urgencia: un agente de amenaza persuade a las personas para que respondan con rapidez sin hacer preguntas.


### Los ocho dominios de seguridad del CIISP

El CISSP define ocho dominios en total: 

`Security and risk management:`Gestión de riesgos y seguridad.

`Asset security:` Seguridad de los activos.

`Security architecture and engineering:` Arquitectura e ingeniería de seguridad.

`Comunnications and network security:` Seguridad de la comunicación y la red.

`Identity and access management:` Gestión de accesos e identidad.

`Security assessment and testing:` 
Evaluación de seguridad y pruebas.

`Security Operations:` operaciones de seguridad.

`Software development security:` seguridad de desarrollo de software.


### Security and risk management: 

Se centra en definir metas y objetivos de seguridad, mitigación de riesgos, cumplimiento, continuidad del negocio y la ley.

Por ejemplo: los analista de seguridad pueden tener que actualizar las políticas de una empresa relacionadas con la información de salud privada, si se hace un cambio a una regulación de cumplimiento federal como la ley de transferencia y responsabilidad de seguros médicos, o HIPAA.

### Asset security:

Este se centra en la seguridad de activos digitales y físicos. También se relaciona con el almacenamiento, mantenimiento, retención y destrucción de datos. Al trabajar con este dominio, los analistas de seguridad podrían tener la tarea de asegurarse de que los equipos viejos se eliminen y destruyan adecuadamente, incluido todo tipo de información confidencial.

### Security architecture and engineering

Este se centra en optimizar la seguridad de los datos al asegurarse de que las herramientas, sistemas y procesos efectivos estén en su lugar. 
como analista de seguridad, quizá se te pida configurar un firewall. Un cortafuegos es un dispositivo que monitorea y filtra el tráfico que entra y sale de la red informática. Configurar un cortafuegos correctamente ayuda a prevenir ataques que podrían afectar la productividad. 


### Communication and network security:

Este se centra en la gestión y seguridad de las redes físicas y las comunicaciones inalámbricas. Como analista de seguridad, tal vez se te pida que analices el comportamiento de los usuarios dentro de tu organización. Imagina que descubres que los usuarios se conectan a puntos de acceso inalámbricos no seguros. Esto podría exponer a la organización y sus empleados a ataques. Para garantizar que las comunicaciones sean seguras, crearías una política de red para prevenir y mitigar la exposición. Mantener la seguridad de una organización es un esfuerzo de equipo, y tiene muchas partes móviles. Como analista de nivel incial seguirás desarrollando tus habilidades aprendiendo a mitigar los riesgos.


### Identity and acess management

Se enfoca en mantener seguros los datos al garantizar que se sigan políticas establecidas para controlar y administrar activos físicos, como espacios de oficina, y activos lógicos, como redes y aplicaciones. Validar las identidades de empleados y documentar roles de acceso es fundamental para resguardar la seguridad digital y física de la organización.
Por ejemplo: como analista de seguridad, quizá se te asigne la configuración de la tarjeta de acceso a edificios de los empleados. 

### Security asessment and testing

Este dominio se centra en realizar pruebas de control de seguridad, recolectar y analizar datos y realizar auditorías de seguridad para monitorear riesgos, amenazas y vulnerabilidades. Los analistas de seguridad pueden realizar auditorías periódicas de permisos de usuarios para asegurarse de que tengan el nivel de acceso correcto.
Por ejemplo: el acceso a la información de la nómina, suele limitarse a ciertos empleados, asi que se le puede pedir a los analistas que auditen permisos regurlarmente para asegurarse de que ninguna persona no autorizada pueda ver los salarios de los empleados.

### Security operations

Este se dedica a la realización de investigaciones y la implementación de medidas preventivas. Imagina que tú, como analista de seguridad, recibes una alerta de que un dispositivo desconocido se conectó a tu red interna. Deberás seguir las políticas y procedimientos de la organización para deterner rápidamente la potencial amenaza. 

### Software development security

Este se centra en el uso de prácticas seguras de codificación, que son una serie de recomendaciones que se utilizan para crear aplicaciones y servicios seguros. Un analista en seguridad puede trabajar con equipos de desarrolladores de software para garantizar que las prácticas de seguridad se incorporen en el ciclo de vida del desarrollo de software. Por ejemplo, uno de tus equipos asociados está creando una nueva aplicación móvil, se te puede pedir que brindes asesoramiento acerca de las políticas de contraseñas o que te asegures de que los datos de usuario se protegen y gestionan adecuadamente. 

### Tipos de hackers

Un/a hacker es cualquier persona o grupo que utiliza computadoras para acceder a datos sin autorización. Puede tratarse de una persona sin experiencia o profesional, experta en tecnología, que usa sus habilidades para diversos fines. Estas son las tres categorías principales de hackers:

Los/las hackers autorizados/as también se denominan hackers éticos. Respetan un código de ética y cumplen la ley para realizar evaluaciones de riesgos de una organización. Su motivación es proteger a las personas y a las organizaciones de los agentes de amenaza maliciosos.

Los/las hackers semiautorizados/as se consideran investigadores/as. Buscan vulnerabilidades, pero no aprovechan las que identifican.

Los/las hackers no autorizados/as también se denominan hackers no éticos. Son agentes de amenaza maliciosos/as que no cumplen ni respetan la ley. Su objetivo es recopilar y vender información confidencial para obtener un beneficio financiero.   






