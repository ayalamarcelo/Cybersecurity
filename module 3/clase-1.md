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