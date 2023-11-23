# ¿Qué son las redes?

Para entender la importancia de proteger una red. Una red es un grupo de dispositivos conectados. En casa, podrías ser tu computadora, celular y dispositivos inteligentes, como tu aire acondicionado. En la oficina, podrían ser equipos, impresoras y servidores.
Los dispositivos en una red pueden comunicarse entre sí mediante cables de red o conexiones inalábricas. Las redes de tu casa y oficina y oficina pueden comunicarse con redes en otros lugares y sus dispositivos. Los dispositivos deben encontrarse entre sí en una red para comunicarse. Para ello, usan direcciones únicas, o identificadores. Estas garantizan que se comunican con el dispositivos correcto.
Se llaman direcciones IP y MAC. Los dispositivos se comunican en dos tipos de redes, una red de área local, o LAN, y una red de área amplia, o WAN, cubre zonas geográficas grandes, como una ciudad, estado o país. Internet es como una gran WAN. Una persona en San Francisco pueden comunicarse y compartir recursos con otra en Dublín mediante la WAN.
Ahora conoces la estructura y los tipos de redes.

## Herramientas de red

Aquí aprenderás sobre los dispositivos comunes que conforman una red. Empecemos. Un hub es un dispositivo de red que transmite información a todos los dispositivos de la red. Un hub es como una torre de radio que difunde una señal a una radio sintonizada en la frecuencia correcta. Otro dispositivo de red es un switch. Un switch establece conexiones entre ciertos dispositivos en una red enviando y recibiendo datos entre ellos. Un switch tiene capacidades superiores a una hub. Solo transfiere datos al destino previsto. Así, el switch es más seguro que el hub, controla el flujo de tráfico y mejora el rendimiento de la red. Otro dispositivo es el router. Un router es un dispositivo de red que conecta varias redes. Por ejemplo, si una computadora en una red envía información a una tableta en otra red, se transfiere de la siguiente forma. Primero, la información va de la computadora al router. El router lee la dirección de destino y reenvía los datos al router deseado. Finalmente el router receptor envía la información a la tableta. Por último, hablemos de los módems. Un módem es un dispositivo que conecta el router a internet y da acceso a internet a la LAN. Por ejemplo, si la computadora de una red envía información al router y este transfiere la información por le módem a internet. El módem del destinatario recibe la información y la transfiere al router. Finalmente el router del destinatario la envía al dispositivo de destino. Las herramientas de red como hubs, switches, routers y módems son dispositivos físicos. Pero muchas de sus funciones se pueden realizar mediante herramientas de virtualización. Las herramientas de virtualización son software que realizan operaciones de red. Llevan a cabo operaciones que normalmente realiza un hub, switch, router o módem. Las ofrecen proveedores de servicios en la nube. Estas herramientas permiten ahorrar costos y obtener escabilidad. Verás más al respecto más adelante. Viste algunos dispositivos comunes que forman una red. 

## Componentes, dispositivos y diagramas de red

* Arquitectura de red

Una vez tengas una comprensión básica de la arquitectura de red, que también se denomina diseño de redes, aprenderás sobre las vulnerabilidades de seguridad inherentes a todas las redes cómo los agentes de amenaza intentan aprovecharlas. en esta lectura, examinarás los dispositivos y conexiones de red, y analizarás un diagrama de red simple, similar a los que utilizan a diario las y los profesionales de seguridad de redes. Como analista de seguridad, una de tus tareas será configurar las herramientas, los dispositivos y protocolos necesarios para observar y proteger el tráfico de red.

## Dispositivos en una red

Los dispositivos de red son aquellos que mantienen la información y los servicios para los usuarios de una red. Estos dispositivos se conectan mediante conexiones cableadas e inalámbricas. Después de establecer una conexión a la red, los dispositivos envían paquetes de datos, que proporcionan información sobre el origen y el destino de los datos.

## Computadoras de escritorio y dispositivos móviles

La mayoría de los usuarios de internet están familiarizados con los dispositivos de uso cotidiano, como computadoras personales, portátiles, teléfonos móviles y tabletas. Cada equipo tiene una dirección MAC y una dirección IP únicas, las cuales lo identifican en la red, y una interfaz de red que envía y recibe paquetes de datos. Estos dispositivos pueden conectarse a la red a través de un cable o una conexión inalámbrica.

## Cortafuegos (firewalls)

Un cortafuegos(firewall) es un dispositivo de seguridad de red que monitore el tráfico hacia o desde tu red. Además, los cortafuegos pueden restringir el tráfico de red específico, tanto de entrada como de salida, según la configuración de reglas de seguridad que realiza la organización. Los firewalls suelen ubicarse entre la red interna segura y controlada y los recursos de red no confiables fuera de la organización, como internet.

## Servidores

Los servidores proporcionan un servicio para otros dispositvos en la red. Los dispositivos que se conectan a un servidor se denominan clientes. El siguiente gra´fico ilustra este modelo, conocido como modelo-cliente-servidor. Aquí, los clientes envían solicitudes al servidor para obtener información y servicios, y el servidor se encarga de cumplir estas solicitudes. Algunos ejemplos comunes incluyen servidores DNS, que realizan búsquedas de nombres de domnio para sitios web, servidores de archivos, que almacenan y recuperan archivos de una base de datos, y servidores de correos corporativos, que organizan el correo de una empresa.

## Hubs y switches

Los hubs y los switches son dispositivos utilizados para dirigir el tráfico en una red local. Un hub es un dispositivo que proporciona un punto de conexión común para todos los dispositivos conectados directamente a él. Además, repite toda la información a todos los puertos. Sin embargo, desde el punto de vista de la seguridad, los hubs son vulnerables a la interceptación de datos Por esta razón, en las redes modernas se utilizan con menos frecuencia y se prefieren los switches.

Un switch reenvía paquetes entre los dipositivos conectados directamente a él. Mantiene una tabla de direcciones de control de acceso al medio (MAC), que asocia la direcciones MAC de los dipositivos en la red con los números de puerto en el switch, y reenvía los paquetes de datos entrantes en función de la dirección MAC de destino. Los switches forman parte de la capa de enlace de datos en el modelo TCP/IP.

## Enrutadores (routers)

Los enrutadores (routers) se encuentran entre las redes y el tráfico directo, según la dirección IP de la red de destino. En el modelo TCP/IP, forman parte de la capa de red. La dirección IP de la red de destino se encuentra en el encabezado IP. El router lee la información del encabezado y reenvía el paquete al siguiente router que aparece en la ruta y así sucesivamente hasta que el paquete llega a la red de destino. Los routers también pueden incluir una función de firewall, que permite o bloqyea el tráfico entrante de acuerdo a la información que se transmite. Esto evita que el tráfico malicioso ingrese en la red privada.

## Módems y puntos de acceso inalámrbicos

* Módems

Los módems suelen interactuar con un proveedor de servicios de internet (ISP, por sus siglas en inglés). Los ISP proporcionan conectividad a internet a través de líneas telefónicas o cables coaxiales. Los módems reciben transmisiones de internet y las traducen en señales digitales que pueden ser entendidas por los dispositivos en la red. Por lo general, los módems se conectan a un router que toma las transmisiones decodificadas y las envía a la red local.

*Nota:* Las redes empresariales que usan las grandes organizaciones para conectar a sus usuarios y dispositivos suele utilizar otras tecnologías de banda ancha para manejar el tráfico de alto volumen, en lugar de utilizar un módem.

## Punto de acceso inalámbrico

Un punto de acceso inalámbrico envía y recibe señales digitales a través de ondas de radio, creando una red inalámbrica. Los dispositivos con adaptadores inalámbricos se conectan al punto de acceso utilizando Wi-Fi. El Wi-Fi se refiere a un conjunto de estándares utilizados por los dispositivos de red para comunicarse de forma inalámbrica. Los puntos de acceso inalámbrico y los dispositivos conectados a ellos utilizan protocolos Wi-Fi para mandar datos a través de ondas de radio a routers y switches, y dirigirlos a lo largo del camino hacia su destino final.

## Uso de diagramas de red como analista de seguridad

Los diagramas de red permiten a los/las administradores/as de red y al personal de seguridad imaginar la arquitectura y el diseño de la red privada de su organización.

Son mapas topográficos que muestran los dispositivos en la red y cómo se conectan. Utilizan pequeños gráficos representativos para reproducir cada dispositivo de red y líneas de puntos para mostrar cómo estos se conectan entre sí. Las/los analistas de seguridad utilizan diagramas de red para aprender sobre la arquitectura de red y cómo diseñar redes. 

# Computación en la nube y redes definidas por software

En esta sección del curso, has estado aprendiendo sobre la arquitectura básica de las redes. Has visto cómo dispositivos físicos , como estaciones de trabajo, servidores, routers y switches, se conectan entre sí para crear una red. Las redes pueden cubrir áreas geográficas pequeñas, como es el caso de una red de área local (LAN), o pueden abarcar una gran área geográfica, como una ciudad, un estado o un país, como es el caso de una red de área amplia (WAN). Además, has aprendido acerca de la computación en la nube, también conocida como cloud computing, y su crecimiento en los últimos años.

En esta lectura, examinarás más a fondo los conceptos de computación en la nube y redes en la nube. También, aprenderás sobre las redes definidas por software, las herramientas de virtualización y la diferencia entre un servidor en la nube y un servidor web. Además, te contaremos las ventajas de alojar redes en la nube y por qué esto beneficia a las grandes organizaciones.
Procesos de computación en la nube

Las redes tradicionales se llaman redes locales, y esto implica que todos los dispositivos utilizados para las operaciones de red se mantienen en una ubicación física propiedad de la empresa, como, por ejemplo, en un edificio de oficinas. En cambio, la computación en la nube se refiere a la práctica de utilizar servidores remotos, aplicaciones y servicios de red que se alojan en Internet.

Un proveedor de servicios en la nube (CSP, por sus siglas en inglés) es una empresa que ofrece servicios de computación en la nube. Este tipo de compañía posee grandes centros de datos ubicados en diferentes partes del mundo, los cuales albergan millones de servidores. Los centros de datos brindan servicios tecnológicos, como almacenamiento y capacidad de procesamiento a una escala tan grande que pueden vender sus servicios a otras empresas. Las empresas pagan por el almacenamiento y los servicios que necesitan y los consumen a través de la consola web o la interfaz de programación de aplicaciones (API) del CSP.

Los servicios ofrecidos por los proveedores de servicios en la nube (CSP) se clasifican en tres categorías principales:

    Software como servicio (SaaS): se refiere a suites de software operadas por el CSP que una empresa puede usar de forma remota sin alojar el software. 

    Infraestructura como servicio (Iaas): se refiere al uso de componentes informáticos virtuales ofrecidos por el CSP. Estos incluyen almacenamiento y contenedores virtuales que se configuran de forma remota a través de la API o la consola web del CSP. Los servicios de almacenamiento y computación en la nube se pueden utilizar para operar aplicaciones existentes y otras cargas de trabajo tecnológicas sin hacer grandes modificaciones. Las aplicaciones existentes se pueden modificar para aprovechar las funcionalidades de disponibilidad, rendimiento y seguridad que son exclusivas de los servicios de proveedores en la nube.

Plataforma como servicio (PaaS): se refiere a herramientas que los/las desarrolladores/as de aplicaciones pueden utilizar para diseñar aplicaciones personalizadas para su empresa. Estas aplicaciones se diseñan y alojan en la nube, y se utilizan para satisfacer las necesidades específicas del negocio de una empresa.

## Entornos de nube híbrida

Un entorno de nube híbrida implica que las organizaciones utilizan los servicios de un CSP, junto con sus propios equipos, redes y almacenamiento locales. Además, cuando las organizaciones utilizan más de un CSP, se denomina entorno multinube o de nube múltiple. La gran mayoría de las empresas optan por entornos de nube híbrida para reducir costos y, a la vez, tener un mayor control sobre los recursos de su red.

## Redes definidas por software

Los proveedores de servicios en la nube (CSP) ofrecen herramientas de redes similares a los dispositivos físicos que aprendiste en esta sección. A continuación, repasarás las redes definidas por software en la nube. Las redes definidas por software (SDN) están compuestas por dispositivos y servicios de red virtuales. Al igual que los CSP proporcionan computadoras virtuales, muchas SDN ofrecen switches, enrutadores, cortafuegos (firewalls) y otros componentes virtuales. La mayoría de los dispositivos de hardware de red modernos también admiten la virtualización de redes y las redes definidas por software. Esto significa que los enrutadores y los switches físicos utilizan software para el enrutamiento de paquetes. En el caso de las redes en la nube, las herramientas SDN se alojan en servidores ubicados en el centro de datos del CSP.

## Beneficios de la computación en la nube y las redes definidas por software

La confiabilidad, la disminución de costos y el aumento de la escalabilidad son tres de las principales razones por las que la computación en la nube es tan atractiva para las empresas.

*Confiabilidad*

La confiabilidad en la computación en la nube se basa en la disponibilidad de los servicios y recursos, la seguridad de las conexiones y la frecuencia con la que los servicios operan de manera efectiva. Además, permite a los/las empleados/as y clientes acceder a los recursos que necesitan de forma consistente y con interrupciones mínimas.

*Costos*

Tradicionalmente, las empresas han tenido que proporcionar su propia infraestructura de red, al menos para las conexiones a Internet, lo cual implicaba que podían existir costos iniciales potencialmente significativos. Sin embargo, debido a que los CSP tienen centros de datos tan grandes, pueden ofrecer dispositivos y servicios virtuales a un costo inferior para que las empresas instalen, actualicen y gestionen los componentes y el software por sí mismas.

*Escalabilidad*

Otro desafío que enfrentan las empresas con la computación tradicional es la escalabilidad. Cuando las organizaciones experimentan un aumento en sus necesidades comerciales, pueden verse obligadas a adquirir más equipos y software para poder satisfacer esa demanda. Sin embargo, ¿qué sucede si el negocio disminuye poco después? Si bien el gasto se justifica por tener los componentes actualizados, puede no tener un negocio suficiente que lo respalde. Los CSP, por su parte, reducen este riesgo al ofrecer un modelo de consumo de servicios elástico, basado en la utilidad y adaptado a las necesidades específicas. De esta manera,  las empresas solo pagan por lo que necesitan cuando lo necesitan y no deben realizar gastos innecesarios durante periodos de baja demanda. 

Los cambios se pueden realizar a través de los CSP, las API o la consola web de manera mucho más rápida que si las/los técnicos/as de red tuvieran que adquirir su propio hardware y configurarlo. Por ejemplo, si una empresa necesita protegerse contra una amenaza a su red, los firewalls de aplicaciones web (WAF), los sistemas de detección/protección contra intrusiones (IDS/IPS) o los firewalls L3/L4 se pueden configurar rápidamente cuando sea necesario, lo que genera un mejor rendimiento y seguridad de la red.
Conclusiones clave

En esta lectura, has aprendido más sobre la computación en la nube y las redes en la nube. Descubriste que los CSP son empresas que poseen grandes centros de datos distribuidos por todo el mundo, que albergan millones de servidores y ofrecen servicios de tecnología avanzados, incluyendo computación, almacenamiento y redes, a través de Internet. 

Por otro lado, las redes definidas por software (SDN) representan un enfoque para la gestión de redes que permite configuraciones dinámicas y eficientes desde el punto de vista programático para mejorar el rendimiento y el monitoreo de la red. Esto hace que se parezca más a la computación en la nube que a la administración de redes tradicional. Al optar por los CSP para proporcionar servicios de redes en lugar de construir y mantener su propia infraestructura de red, las organizaciones pueden mejorar la confiabilidad, reducir costos y escalar rápidamente.

## Modelo TCP/IP
El modelo TCP/IP significa protocolo de control de transmisión y protocolo de internet. Es el modelo estándar usado para la comunicación en red. Analicemos este modelo, definamos TCP e IP por separado. TCP, o protocolo de control de transmisión, es un protocolo de comunicación en internet que permite a dos dispositivos establecer una conexión y trasmitir datos. El protocolo incluye instrucciones para organizar datos y enviarlos por la red. También conecta dos dispositivos y garantiza que los paquetes lleguen a su destino. IP en TCP/IP significa protocolo de internet. El IP son estándares para enrutar y direccionar paquetes entre dispositivos en una red. La parte IP incluye la dirección IP, que es la dirección de cada red privada. Verás más al respecto más adelante. Al enviar y recibir paquetes de datos por una red, un puerto es una ubicación de software que organiza el envío y recepción de datos entre dos dispositivos. Los puertos dividen el tráfico de red en segmentos según el servicio que darán.
Las computadoras que envían y reciben estos segmentos los priorizan y procesan según su número de puerto. Es como enviar una carta a alguien en un departamento. El repartidor sabe cómo encontrar el edificio y también el departamento exacto donde vive el destinatario. Los paquetes de datos le indican al dispositivo receptor qué hacer con la información. Estas instrucciones vienen en forma de un número de puerto. Los números de puerto permiten que las computadoras dividan el tráfico de red y prioricen las operaciones que realizarán con datos. Algunos números de puerto comunes son: puerto 25, para correo electrónico; puerto 443, para la comunicación segura en Internet; y puerto 20, para transferir archivos grandes. Como aprendiste aquí, mucha información e instrucciones están contenidas en los paquetes de datos mientras viajan a través de una red.

## Las cuatro capas del modelo TCP - IP

Tras ver la estructura de una red y cómo ocurren las comunicaciones, debes saber cómo se identifican los problemas que podrían surgir. El modelo TCP/IP es un marco usado para ver cómo se organizan y transmiten los datos por la red. El modelo TCP/IP tiene cuatro capas. Estas son la capa de acceso a la red, capa de Internet, capa de transporte y capa de aplicación. Conocer cómo el modelo TCP/IP organiza la actividad de la red permite monitorear y protegerse contra los riesgos. Analicemos cada capa. La primera es la capa de acceso a la red. Esta se ocupa de crear paquetes de datos y transmitirlos por una red. Incluye dispositivos de hardware conectados a cables físicos y switches que envían datos a su destino. La segunda es la capa de Internet. Ahí las direcciones IP se adjuntan a paquetes para indicar la ubicación del emisor y receptor. Esta capa también se enfoca en cómo las redes se conectan entre sí. Por ejemplo, los paquetes con información que determina si quedarse en la LAN o enviarse a una red remota, como Internet. La capa de transporte incluye protocolos para controlar el flujo de tráfico en una red. Estos permiten o niegan la comunicación con otros dispositivos e incluyen información del estado de la conexión. En esta capa se controlan errores, que garantiza que los datos fluyan sin problemas a través de la red. Finalmente, en la capa de aplicación, los protocolos determinan cómo interactúan los paquetes de datos con los dispositivos receptores. Las funciones organizadas aquí son las transferencias de archivos y servicios de correo. Ahora conoces el modelo TCP/IP y sus cuatro capas.

## Capas de acceso a la red

La caoa de acceso a la red, a veces llamada caoa de enlace de datos, organiza el envío y la recepción de paquetes de datos dentro de una sola red. Esta capa corresponde alhardqare físico involucrado en la transmisión de red. Los hubs, módems, cables y cableado se consideran parte de esta etapa. El protocolo de resolución de direcciones (ARP, por sus siglas en inglés) forma parte de la capa de acceso a la red. El arp ayuda a la IP a dirigir paquetes de datos al mapear direcciones IP a direcciones MAC en la misma red física.

## Capa de internet

La capa de internet, a veces denominada capa de red, es responsable de garantizar la entrega al host de destino, que potencialmente puede residir en una red diferente. La capa de internet determina qué protocolo es el encargado de entregar los paquetes de datos. A continuación, se presentan algunos de los protocolos comunes que operan en la capa de internet:

**Protocolo de internet (IP):** Envía los paquetes de datos al destino correcto y se basa en el protocolo de control de transmisión-protocolo de datagramas de usuario (TCP-UDP) para entregarlos al servicio correspondiente. Los paquetes de IP posibilitan la comunicación entre dos redes, ya que enrutan desde la red de origen hasta la de destino. El IP retransmite cualquier dato que se haya paerdido o dañado.

**Protocolo de mensajes de control de internet(ICMP):** Comparte información de errores y actualizaciones de estado de los paquetes de datos. Resulta útil para detectar y solucionar errores de red y, además, informa sobre paquetes que fueron descartado o desaparecieron durante el tránsito, problemas de conectividad de red y paquetes redirigidos a otros enrutadores.

## Capa de transporte

La capa de transporte es responsable de entregar datos de manera confiable entre dos sistemas o redes. El protocolo de control de transmisión (TCP) y el de datagramas de usuario (UDP) son los dos protocolos de transporte que se producen en esta capa.

**Protocolo de control de transmisión(TCP)**

El TCP garantiza que los datos se transmitan de forma segura al servicio de destino. Contiene el número de puerto del servicio de destino previsto, que reside en el encabezado TCP de un paquete TCP-IP.

**Protocolo de datagramas de usuario (UDP)**

Las aplicaciones que no están afectadas por la confiabilidad de la transmisión usan el protocolo UDP. Los datos enviados a través de UDP no son objeto de un seguimiento tan exhaustivo como los enviados mediante TCP. Debido a que el UDP no establece conexiones de red, se utiliza principalmente para aplicaciones sensibles al rendimiento que operan en tiempo real, como la transmisión de video.

**Capa de aplicación**

La capa de aplicación en el modelo TCP-IP es similar a las capas de aplicación, presentación y sesión del modelo OSI. Es la responsable de realizar solicitudes de red o de responder a solicitudes. Además, esta capa define a qué servicios y aplicaciones de internet puede acceder cualquier usuario. Algunos de los protocolos comunes utilizados en esta capa son:

* Protocolo de transferencia de hipertexto (HTTP)
* Protocolo simple de transferencia de correo (SMTP)
* Secure shell o shell seguro (SSH)
* Protocolo de transferencia de archivos (FTP)
* Sistema de nombres de dominio (DNS)

Los protocolos de capa de aplicación se basan en capas subyacentes para transferir los datos a través de la red.

## Comparación del modelo TCP-IP con el modelo OSI

El modelo OSI organiza visualmente los protocolos de red en diferentes capas. Las y los profesionales de redes suelen usar este modelo para comunicarse entre sí sobre posibles fuentes de problemas o amenazas de seguridad.
El modelo TCP-IP combina múltiples capas de modelo OSI. Ambos modelos comparten muchas similitudes, ya que definen estándares para las redes y dividen el proceso de comunicación de red en diferentes capas. Sin embargo, el modelo TCP-IP es una versión simplificada del modelo OSI.

## Conclusión

Los modelos TCP-IP y OSI son marcos conceptuales que ayudam a las y los profesionales de redes a visualizar los proceso y protocolos con respecto a la transmisión de datos entre dos o más sistemas. El modelo TCP-IP contiene cuatro capas y el modelo OSI siete.

# El modelo OSI

**Comparación entre el modelo TCP-IP y el modelo OSI**

El modelo TCP-IP es un marco utilizado para visualizar cómo se organizan y transmiten los datos a través de una red. Este modelo ayuda a los ingenieros y analistas de seguridad de redes a diseñar la red de datos, conceptualizar procesos y comunicar dónde se producen las interrupciones o amenazas de seguridad.
El modelo TCP-IP tiene cuatro capas: de acceso a la red, de internet, de transporte y de aplicacióm. Al analizar los eventos de la red, los profesionales de seguridad pueden determinar en qué cepa o capas se produjo el ataque, basándose en los procesos involucrados en el incidente.
En cambio, el modelo OSI es un concepto estandarizado que describe las siete capas que las computadoras utilizan para comunicarse y enviar datos a través de la red. Las y los profesionales de seguridad y de redes suelen utilizarlo para comunicarse entre sí sobre posibles fuentes de problemas o amenazas de seguridad.
Algunas organizaciones dependen en gran medida del modelo TCP-IP, mientras que otras prefieren usar el modelo OSI. Como analista, es importante conocer los dos modelos, dado que ambos son útiles para comprender cómo funcionan las redes.

**Capa 7: Capa de aplicación**

La capa de aplicación incluye procesos que involucran directamente al usuario cotidiano. Esta caoa incluye todos los protocolos de red que la aplicaciones de software utilizan para conectarlo a internet. Esta característica es la que identifica a la capa de aplicación: conexión de usuarios a la red a través de aplicaciones y solicitudes.
Un ejemplo de un tipo de comunicación que ocurre en la capa de aplicación es el uso de un navegador web. El navegador internet utiliza HTTP o HTTPS para enviar y recibir información del servidor del sitio web. La aplicación de correo electrónico utiliza el protocolo simple de transferencia de correo (SMTP) para transmitir información de correo electrónico. Además, los navegadores web utilizan el protocolo del sistema de nombre de dominio (DNS) para traducir los nombres de dominio del sitio web en direcciones IP, que identidican el servidor web que aloja la información del sitio.

**Capa 6: Capa de presentacióm**

La funciones en la capa de presentación incluyen la traducción de datos y el cifrado para la red. Esta capa agrega y reemplaza datos con formatos que pueden ser entendidos por las aplicaciones (capa 7), en los sistemas de envío y recepción. Los formatos que están más cerca del usuario final, es decir, donde se encuentra la aplicación o dispositivo que utiliza el usuario para interactuar con la red o recibir información, pueden ser diferentes de los del sistema receptor. Los procesos en la capa de presentación requieren el uso de un formato estandarizado.
Algunas funciones de formateo que se producen en la capa seis incluyen cifrado que se da en esta capa es SSL, que cifra los datos entre los servidores web y los navegadores como parte de sitios web con HTTPS.

**Capa 5: Capa de sesión**

Una sesión indica cuando se establece una conexión entre dos dispositivos. Una sesión abierta permite que los dispositivos se comuniquen entre sí. El objetivo de los protocolos de la capa de sesión es mantener la sesión abierta mientras se transiferen datos y cerrarla una vez que se completa la transmisión.
La capa de sesión también es responsable de actividades como la autenticación , reconexión y establecimiento de puntos de control durante una transferencia de datos. Si la sesión se interrumpe, los puntos de control aseguran que, cuando se restablece la conexión, la transmisión se retome desde el último punto de control de la sesión. Las sesiones incluyen una solicitud y respuesta entre aplicaciones. Las funciones en la capa de sesión responden a solicitudes de servicio de procesos en la capa de presentación (capa 6) y envían solicitudes de servicios a la capa de transporte (capa 4).

**Capa 4: Capa de transporte**

La caoa de transporte es la responsable de enviar datos entre dispositivos. Además, esta capa maneja la velocidad y el flujo de transferencia, y divide los datos en segmentos más pequeños para facilitar el envío. La segmentación es el proceso de dividir una gran transmisión de datos en piezas más pequeñas que puedan ser procesadas por el sistema receptor. Para que se puedan procesar en la capa de sesión (capa 5), estos segmentos tienen que volverse a ensamblar en su destino. La velocidad y la tasa de transmisión también tienen que coincidir con la velocidad de conexión del sistema de destino. TCP y UDP son protocolos de capa de transporte.

**Capa 3: Capa de red**

La capa de red supervisa la recepción de los paquetes desde la capa de enlace de datos (capa 2) y las entrega al destino previsto. El destino previsto puede encontrarse en función de la dirección que reside en el marco de los paquetes de datos. Estos paquetes incluyen direcciones IP, que indican a los routers dónde enviarlos y se enrutan desde la red de envío hacia la red de recepción.

**Capa 2: Capa de enlace de datos**

La caoa de enlace de datos organiza el envío y la rececpción de paquetes de datos dentro de una sola red. Esta capa incluye los switches en la red local y las tarjetas de interfaz de red en los dispositivos locales.
En la capa de enlace de datos se utilizan protocolos de control de red (NCP), el control de enlace de datos de alto nivel (HDLC) y el protocolo de control de enlace de datos sincrónico (SDLC).

**Capa 1: Capa física**

Como su nombre lo indica, la capa física corresponde al hardware físico utilizado en la transmisión de la red. Los hubs, los módems y el cableado que los conecta se consideran parte de esta capa. para viajes a través de un cable Ethernet o coaxial, un paquete de datos debe ser traducido en una sencuencia de ceros y unos, que se envían a través de los cables y coneciones físicas, se recibe y, luego, pasa a los niveles superiores del modelo OSI.


## Direcciones IP y comunicacines de red

Veamos cómo se usan las direcciones IP para comunicarse por una red. IP significa protocolo de Internet. Un protocolo de Internet, o dirección IP, es una cadena única de caracteres que identifica la ubicación de un dispositivo en Internet. Cada dispositivo tiene una dirección IP única, al igual que toda casa tiene su dirección postal. Hay dos tipos de direcciones IP: IP versión 4, o IPv4, e IP versión 6, o IPv6. Veamos ejemplos de una dirección IPv4. Las direcciones IPv4 se escriben con 4 números de 1, 2 o 3 dígitos separados por un punto. En los inicios de Internet,todas las direcciones IP eran IPV4. Pero el uso de Internet creció y estas direcciones empezaron a agotarse, por lo que se desarrolló IPv6. Las direcciones IPv6 tienen hasta 32 caracteres. De esta forma, puede haber más dispositivos conectados a Internet sin agotar las direcciones como ocurrió con IPv4. Las direcciones IP pueden ser públicas o privadas. Tu proveedor de Internet asigna una dirección IP pública que se conecta a tu ubicación geográfica. Las comunicaciones de tu dispositivo en Internet por la red tienen la misma dirección pública. Así como todos en una casa tienen la misma dirección postal, todos los dispositivos tienen la misma dirección IP pública. Las direcciones IP privadas solo las ven otros dispositivos en la misma red local. Así todos los dispositivos en tu red doméstica pueden comunicarse entre sí usando direcciones IP únicas que el resto no puede ver. La dirección MAC es otra que se usa en comunicaciones de red. Es un identificador alfanumérico único que se asigna a cada dispositivo físico en la red. Al recibir un paquete, el switch lee la dirección MAC del dispositivo destinatario y le asigna un puerto. Anota esta información en una tabla de direcciones MAC. La tabla de direcciones MAC es como una agenda que el switch usa para enviar paquetes a dispositivos. Aquí aprendiste sobre direcciones IPv4 e IPv6. Viste cómo las direcciones IP y MAC se usan en la comunicación en red y la diferencia entre una dirección IP privada y pública. 

## Componentes de la comunicación en la capa de red

**Operaciones en la capa de red**

Las funciones en la capa de red organizan la dirección y la entrega de paquetes de datos a través de la red e internet desde el dispositivo host hasta el de destino. Esto incluye dirigir los paquetes de un enrutador a otro a través de internet, basándose en la dirección del protocolo de internet (IP) de la red de destino. La dirección IP de destino se encuentra dentro del encabezado de cada paquete de datos. Esta dirección se almacenerá en tablas de enrutamiento a lo largo del camino del paquete hacia su destino, para futuros propósitos de enrutamiento.
Todos los paquetes de datos incluyen una dirección de IP; esto se denomina paquete IP o datagrama. Un router utiliza la dirección IP para enrutar paquetes de una red a otra, basándose en la información contenido en el encabezado IP de un paquete de datos. La información del encabezado no comunica solo la dirección del destino. También incluye información, como la dirección IP de origen, el tamaño del paquete y qué protocolo se utilizará para el área de datos del paquete.

## Formato de un paquete IPv4

A continuación, puedes ver el formato de un paquete IP versión 4 (IPv4) y un gráfico que detalla el encabezado del paquete. Un paquete IPv4 se compone de dos secciones, el encabezado y los datos:

   * El tamaño del encabezado IP oscila entre 20 y 60 bytes. Incluye la información de enrutamiento IP que los dispositivos utilizan para dirigir el paquete. El formati de un encabezado de paquete IP está determinado por el protocolo IPv4.
   
   * La longitud de la sección de datos de un paquete IPv4 puede variar mucho, pero el tamaño máximo posible de un paquete IP es 65.536 bytes. Contiene el mensaje que se transfiere a la transmisión, como la información del sitio web o el texto del correo electrónico.

Hay 13 campos dentro del encabezado un paquete IPv4:

   *  **Versión:** el primer encabezado de 4 bits indica a los dispositivos receptores qué protocolo está utilizado el paquete. EL paquete utilizado en la ilustración anterior es un paquete IPv4.

   * **Longitud del encabezado IP (HLEN):** HLEN es la longitud del encabezado del paquete. Este valor indica dónde termina el encabezado del paquete y comienza el segmento de datos.

   * **Tipo de servicio (ToS):** los routers priorizan los paquetes a entregar con el fin de mantener la calidad del servicio en la red. El campo ToS proporciona esta información al router.

   * **Longitud total:** este campo comunica la longitud total de todo el paquete IP, incluidos el encabezado y los datos. El tamaño máximo de un paquete IPv4 es de 65.535 bytes.

   * **Identificación:** si el paquete IPv4 es superior a 65535 bytes, se divide o fragmenta en paquetes IP más pequeños. El campo de identificación proporciona un identificador único para todos los fragmentos del paquete IP original para que puedan volver a ensamblarse cuando lleguen a su destino.

   * **Indicadores:** este campo proporciona al dispositivo de enrutamiento más información sobre si el paquete original se fragmentó y si hay más fragmentos en tránsito.

   * **Desplazamiento de fragmentación:** el campo de desplazamiento de fragmento indica a los dispositivos de enrutamiento a qué parte del paquete original pertenece el fragmento.

   * **Período de vida (TTL):** evita que los routers reenvíen los paquetes de datos de manera indefinida. Contiene un contador que determina la fuente. El contador disminuye de a uno, a medida que pasa por cada router. Cuando el contador TTL llega a cero, el router descartará el paquete y enviará al emisor un mensaje de tiempo superado ICMP.

   * **Protocolo:** este campo indica al dispositivo receptor qué protocolo se utilizará para el área de datos del paquete.

   * **Suma de comprobación del encabezado:** este campo contiene una suma de comprobación que se puede usar para detecta si la cabecera IP en tránsito está dañada. Los paquetes dañados se descartan.

   * **Dirección IP de origen:** es la dirección IPv4 del dispositivo emisor.

   * **Dirección IP de destino:** es la dirección IPv4 del dispositivo receptor.

   * **Opciones:** este campo permite aplicar opcinoes de seguridad al paquete si el valor HLEN es mayor que cinco. Además, comunica estas alternativas a los dispositivos de enrutamiento.

## Diferencia entre IPv4 e IPv6

Es una parte anterior de este curso, aprendiste sobre la historia de las direcciones IP. Con el crecimiento de internet, se hizo evidente que todas las direcciones IPv4 se consumirían en algún momento, lo que se conoce como el agotamiento de direcciones IPv4. En ese momento, nadie había anticipado la cantidad de dispositivos informáticos que necesitarían una dirección IP en el futuro. En respuesta a esta problemática, se desarrolló IPv6, co el fin de mitigar el agotamiento de direcciones IPv4 y abordar otras preocupaciones relacionadas con esto.
Una de las principales diferencias entre IPv4 e IPv6 es la longitud de las direcciones. Las direcciones IPv4 son numéricas, están compuestas por 4 bytes y adminten hasta 4300 millones de direcciones posibles. Un ejemplo sería: 1998.51.100.0. En cambio, las direcciones IPv6 son hexadecimales, están compuestas por 16 bytes y permiten hasta 340 undecillones de direcciones (la cifra 340 seguida de 36 0). Un ejemplo de una dirección IPv6 sería: 2002:0db8:0000:0000:0000:ff21:0023:1234.
También hay algunas diferencias en el diseño del encabezado de un paquete IPv6. El formato del IPv6 es mucho más simple que el del IPv4. Por ejemplo, el encabezado del IPv4 incluye los campos HLEN, identificación e indicadores, mientras que el IPv6 no lo hace. EL encabezado del IPv6 tiene otros campos que no están incluidos en IPv4, como etqueta de flujo y clase de tráfico.
Hay algunas diferencias de seguridad importante entre IPv4 e IPv6. IPv6 ofrece un enrutamiento más eficiente y elimina las colisiones de direcciones privadas que puede ocurrir en IPv4 cuando dos dispositivos de la misma red intentan usar la misma dirección.

## Protocolos de red
Las redes se benefician de tener reglas. Las reglas garantizan que los datos enviados lleguen a su destino. Estas reglas se denominan protocolos de red. Estos son un conjunto de reglas usadas por dos o más dispositivos en una red para describir el orden de entrega y la estructura de los datos. Veamos en un escenario algunos tipos de protocolos de red y cómo funcionan juntos en una red. Imagina que deseas ver un sitio de recetas. Ingresas la dirección del sitio en la barra del navegador. Por ejemplo, wwww.recetasricas.org. Antes de acceder al sitio, tu dispositivo se comunica con servidor web. Esa comunicación usa un protocolo llamado protocolo de control de transmisión, o TCP. Este protocolo de comunicación por internet permite conectar dos dispositivos y enviar datos entre ellos. El TCP verifica ambos dispositivos antes de permitir más comunicaciones. Esto suele denominarse protocolo de enlace. Tras establecer la comunicacióm con un protocolo de enlase TCP, se realiza una solicitud a la red. En nuestro ejemplo, solicitamos datos del servidor de Recetas Ricas. Sus servidores responderán la solicitud y enviarán paquetes a tu dispositivo para ver la página web. Los paquetes de datos se mueven por la red entre dispositivos como routers. El protocolo de resolucióm de direcciones, o ARP, sirve para definir la dirección MAC del siguiente router o dispositivo. Esto garantiza que los datos lleguen a su destino. Tras establecer la comunicación y reconocer el dispositivo de destino, puedes acceder al sitio web Recetas Ricas. El protocolo seguro de transferencia de hipertexto, o HTTOS, es un protocolo de red que brinda un método seguro de comunicación entre servidores de clientes y de sitios. Permite al navegador solicitar una página de forma segura al servidor del sitio web y recibir una página web como respuesta. Ahora veremos el protocolo llamado sistema de nombres de dominio, o DNS, un protocolo de red que traduce nombres de dominio de internet a direcciones IP. El DNS envía el nombre de dominio y la dirección web a un servidor DNS que obtiene la dirección IP del sitio que quieres ver, en este caso, Recetas Ricas. La dirección IP se incluye como dirección de destino de los paquetes que van al servidor web del sitio. Solo al visitar un sitio, el dispositvo en tu red usa cuatro protocolos, TCP, ARP, HTTPS y DNS.