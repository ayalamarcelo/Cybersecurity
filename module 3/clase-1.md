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
