## Distribuciones de Linux
Las versiones de linux se llaman distribuciones. Algunos las llaman "distros" o "sabores". Debes conocer la distribución que usas para saber qué herramientas y apps hay. Por ejemplo, Debian y ubuntu son distribuciones con herramientas distintas. Usemos una analogía para describir las distribuciones. El SO es como un vehículo. Primero empezamos con el motor, o sea el kernel. Al igual que el motor hace que el vehículo funcione, el kernel es el componente más importante de Linux. Como el kernel es de código abierto, cualquiera puede modificarlo y crear una nueva distribución. Es como si un fabricante de vehículos modifica un motor y crea varios vehículos: camiones, autos, furgonetas, descapotables, autobuses, aviones, etc. Estos vehículos son como las distintas distribuciones de Linux. Un autobús se usa para transportar a mucha gente; un camión, para transportar mercancía a largas distanciasñ un avión, para transportar pasajeros o mercancías por aire. Así como cada vehículo cumple un objetivo, las distribuciones se usan por distintos motivos. Además, los vehículos tienen componentes que los distinguen uno del otro. Los aviones tiene paneles con botones y perillas. Los autos tienen cuatro llantas, los camiones más. Las distribuciones contienen distintos programas preinstalados, interfaces de usuario y mucho más. Depende much de las necesidades del usuario, pero algunas distribuciones se eligen según la preferencia, al igual que se elige un auto deportivo. La ventaja de usar Linux es que se puede personalizar. Las distribuciones tienen el kernel, utilidades, sistema de gestión de paquetes y un instalador. Antes vimo que Linux es de código abierto, cualquiera puede contribuir al código fuente. Así se crean las distribuciones. Todas se derivan de otra distribución, pero algunas son distribuciones madre. Red hat es la madre de CentOS, slackware es la madre de SUSE. Ubuntu y Kali Linux se derivan de Debian. 

## Kali LINUX
Una distribución usada mucho en seguridad es una marca de Offensive Security, derivado de Debian. Esta distribución de código abierto se creó para el pentesting y análisis forense digital. Kali Linux tiene herramientas preinstaladas. Ten en cuenta que debe usarse en una máquina virtual. Así se evitan daños en el sistema si sus herramientas se usan mal. Otra ventaja es que con la máquina virtual puedes revertir a un estado anterior. Con el tiempo, algunos profesionales se especializan en pentesting. Es una prueba de penetración, un ataque simulado para identificar vulnerabilidades en sistemas, red, sitios, apps y procesos. Kali Linux tiene herramientas que sirven para el pentesting.

Veamos algunos ejemplos. Metasploit sirve para buscar y explotar vulnerabilidades en equipos. Con Buro Suite se buscan debilidades en apps web. Finalmente Jhon the Ripper sirve para adivinar contraseñas. Como analista, puede encargarte del análisis forense digital. El análisis forense digital consiste en recopilar y analizar datos para determinar qué ocurrió tras un ataque. Por ejemplo, podrías investigar datos relacionados con la actividad de red. Kali Linux también sirve para los profesionales en el campo forense digital. Tiene muchas herramientas para eso. Tcpdump analiza paquetes de línea de comandos. Se usa para capturar el tráfico de red. Wireshark es otra herramienta usada comúnmente en la seguridad. Tiene una GUI que puede usarse para analizar tráfico de red en vivo y capturado. Un último ejemplo, Autopsy es una herramienta forense para analizar discos duros y smartphones. Estas son algunas herramientas incluidad en Kali Linux. La distrubución ofrece muchas herramientas de pentesting y análisis forse digital.

## Instalación software kali linux
* Tarea 1: Asegúrate de que la aplicación APT esté instalada

`$ apt`
APT es el administrador de paquetes recomendado para Debian.

* Tarea 2: Instala y desinstala la aplicación Suricata

`$ sudo apt install suricata`

Usar el administrador de paquetes para instalar la aplicación suricata.

>[!Note]
> Los comandos `apt install` y `apt remove` deben incluir el comando `sudo` como prefijo ya que se requieren privilegios elevados para instalar y desinstalar software en Linux. Es posibble que demore algunos minutos.

Verificar que esté instalada, para ello ejecutamos la aplicación instalada recientemente.

`$ suricata`

Cuando se instale, se presentará la información de uso y la versión.

Ahora utilizaremos el administrador de paquetes para desinstalar Suricata.

`sudo apt remove suricata`

Para verificar que se haya desinstalado solo ejecutamos el comando de la aplicación nuevamente.

`$ suricata` y luego presiona intro.

Si está desinstalado, aparecerá un mensaje de error `-bash: /usr/bin/suricata: No such file or directory`.

* Tarea 3: Instala la aplicación tcpdump

En esta tarea, debemos instalar la aplicación tcpdump. Se trata de una herramienta de línea de comandos que se puede usar para capturar tráfico de red en una shell Bash de Linux.

Usa el administrador de paquetes APT para instalar tcpdump.

`sudo apt install tcpdump`

* Tarea 4: Genera una lista de las aplicaciones instaladas.

A continuación, debes confirmar que instalaste las aplicaciones indicadas. Es importante confirmar que se instalaron las aplicaciones correctas. Te suferimos que también verifiques con frecuencia que se hayan instalados las versiones adecuadas.

1. Usa el apt para generar una lista de todas las aplicaciones instaladas.

`apt list --installed`

* Tarea 5: Reinstala la aplicación Suricata

`sudo apt install suricata`

## Introducción a Shell
Esta parte de la arquitectura de Linux es donde trabajarás como analista. Antes vimos el shell con otros componentes de Linux, pero veamos qué es y qué lo hace. El shell intepreta líneas de comandos. Es decir, te comunica con el SO mediante la línea de comandos. Antes vimos la interfaz de línea de comandos. Básicamente, eso es el shell. El shell ofrece la línea de comandos para que interactúes con el SO.

Para decirle al SO qué hacer, ingresas comandos en esta interfaz. Un comando le indica a la computadora que haga algo. El shell se comunica con el kernel para ejecutar comandos. Antes vimos cómo el SO permite que el usuario se comunique con la computadora. EL shell es la parte del SO que logra esto.

Es como un intérprete útil entre tú y el sistema. No hablas el idioma de la computadora, binario, así que no puedes comunicarte de forma directa. El shell te ayuda con eso. El so necesita el shell para la mayoría del trabajao, pero es una interfaz entre tú y el sistema. Te permite hacer cálculos, realizar pruebas y ejecutar apps. Sobre todo, te permite combinar estas operaciones y conectar apps entre sí para realizar tareas complejas y automatizadas. Hay muchas distrbicuiones de Linux y también muchos tipos de shells.

## Entrada y salida del shell
Al comunicarte con el shell, los comandos en este pueden recibir datos, producir salidas o dar mensajes de error. Veamos que la entrada estándar, salida estándar y mensajes de error. La entrada estándar es información que recibe el SO por la línea de comandos. Es como preguntarle a tu amiga algo en una conversación. La información se ingresa al shell mediante el teclado. Si el shel interpreta tu solicitud, le pide al kernel los recursos para ejecutar la tarea. Veamos el comando echo, que emite una cadena de texto especificada. Los datos de cadena son una secuencia ordenada de caracteres. En nuestro ejemplo, solo produce la cadena "Hello".

Como entrada, escribiremos "echo hello" en el shell.

Luego presionamos intro para obtener la salida. Pero antes, profundicemos en el concepto de salida. La salida estándar es la información que devuelve el SO por el shell. Así como tu amiga responde a tu pregunta, la salida es la respuesta de una computadora a tu mando.

La saluda es lo que recibes. Retomemos nuestro ejemplo y enviemos la entrada "echo hello" al SO presionando intro. De inmediato, el shell devuelve la salida "hello". Finalmente el error estándar tiene mensajes de error que devuelve el SO por el shell. El sistema da un mensaje de error si no puede responder al comando. Esto puede ocurrir al escribir mal un comando o si el sistema no conoce la respuesta al comando. También puede ocurrir porque no tenemos los permisos para ejecutar un comando. Veremos otro ejemplo de error estándar. Ingresemos "eco hello" en el shell. Observa que escribí "eco" y no "echo". Al presionar intro aparece un mensaje de error.