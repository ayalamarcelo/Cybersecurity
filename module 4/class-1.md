# Introducción a los sistemas operativos
Un sistema operativo es la interfaz entre el hardware y el usurario. El sistema operativo, o SO, es el responsable de que la computadora funcione bien y sea fácil de usar. Veamos qué es el hardware. El hardware se refiere a los componentes físicos de una computadora. Las primeras computadoras no tenían la interfaz de SO que usamos diario. En los años 50, en mayor desafío de las primeras computadoras era el tiempo que llevaba ejecutar un programa. Las computadoras no ejecutaban varios programas simultáneamente. Había que esperar a que un programa terminara de ejecutarse, reiniciar la computadora y cargar otro programa. Desde entonces los SO han evolucionado y ya no perdemos tiempo de esta forma. Gracias a los SO y su evolución, las computadoras ahora son eficientes. Ejecutan varias aplicaciones a la vez y acceden a dispositivos externos como impresoras, teclados y mouses. Los sistemas operativos también son importantes porque posibilitan la comunicación entre las personas y las computadoras. Las computadoras se comunican en lenguaje binario, que se compone de unos y ceros. El sistema operativo proporciona una interfaz para cerrar esta brecha de comunicación entre las personas y las computadoras, permitiéndote interactuar con la computadora de formas complejas. Los sistemas operativos son fundamentales para el uso de las computadoras. La seguridad del SO también es fundamental para la seguridad de la computadora. Esto implica asegurar archivos, acceso a datos y autenticación de usuarios para la seguridad de la computadora. Esto implica asegurar archivos, acceso a datos y autenticación de usuarios para proteger y prevenir amenazas como virus, gusanos y malware. Saber cómo funcionan los SO es esencial para realizar tareas de seguridad. Por ejemplo, como analista de seguridad, puede que seas responsable de configurar y mantener la seguridad de un sistema mediante la gestión de acceso. También puedes ser responsable de gestionar y configurar firewalls, establecer políticas de seguridad, activar protección contra virus y realizar auditorías, informes y registros para detectar comportamientos inusuales.

## Arranque de la computadora

Cuando arrancas o enciendes tu computadora, se activa un microchip BIOS o UEFI. El sistema básico de entrada/salida (BIOS) es un microchip que contiene instrucciones de carga para la computadora y que es común en los sistemas más antiguos. La interfaz de firmware extensible unificada (UEFI) es un microchip que contiene instrucciones de carga para la computadora y reemplaza al BIOS en los sistemas más modernos.

Tanto los chips BIOS como los UEFI realizan la misma función en el arranque de una computadora. El BIOS era el chip estándar hasta 2007, cuando el uso de los chips UEFI se incrementó. Ahora, la mayoría de las computadoras nuevas incluyen un chip UEFI, que proporciona funcionalidades de seguridad mejoradas.

Los microchips BIOS o UEFI contienen una variedad de instrucciones de carga para la computadora. Por ejemplo, una de estas consiste en verificar el estado del hardware de la computadora.

La última instrucción del BIOS o UEFI activa el cargador de arranque. El cargador de arranque es un programa de software que inicia el sistema operativo. Una vez que el sistema operativo termina de arrancar, la computadora está lista para su uso. 

**Completar una tarea**

Como se mencionó con anterioridad, los sistemas operativos nos ayudan a utilizar las computadoras de manera más eficiente. Cuando un equipo pasa por el proceso de arranque, para completar una tarea en una computadora se debe realizar otro proceso que contiene cuatro partes.

Muestra un proceso que va del/la usuario/a a la aplicación, a los sistemas operativos y por último, al hardware.

* Usuario/a

En la primera parte está el/la usuario/a, que inicia el proceso para hacer algo con la computadora. Como tú ahora mismo, que iniciaste el proceso de acceder a esta lectura.

* Aplicación

La aplicación es el programa de software con el que los/as usuarios/as interactúan para completar una tarea. Por ejemplo, si deseas hacer un cálculo, utilizarás la aplicación de la calculadora. Si deseas escribir un informe, en cambio, usarás una aplicación de procesamiento de textos. Esta es la segunda parte del proceso.

* Sistema operativo**

* El sistema operativo recibe la solicitud del/la usuario/a desde la aplicación. Su tarea es interpretar la solicitud y dirigir el flujo. Para completar la tarea, el sistema operativo la envía a los componentes del hardware. 

* Hardware

El hardware es donde se realiza todo el procesamiento para completar las tareas iniciadas por el/la usuario/a. Por ejemplo, cuando una persona quiere calcular un número, la unidad central de procesamiento (CPU) realiza el cálculo. Otro ejemplo, cuando un/a usuario/a desea guardar un archivo, otro componente del hardware, el disco duro, se encarga de hacerlo. 

Después de que el hardware realiza el trabajo, envía el resultado a través del sistema operativo a la aplicación para mostrárselo al/la usuario/a.

## Línea de comandos en uso
**CLI frente a GUI**

## CLI frente a GUI
Una interfaz gráfica de usuario(GUI) utiliza íconos en la pantalla para gestionar las distintas tareas de la computadora. Una interfaz de línea de comandos(CLI), en cambio, es una interfaz de usuario basada en texto que utiliza comandos para interactuar con la computadora.

**Pantalla**
Una diferecia importante entre estas dos interfaces es cómo se presentab en la pantalla. Una interfaz gráfica de usuario tiene gráficos e íconos, como los íconos en tu escritorio o la barra de tareas para iniciar programas. Al contrario, una CLI solo tiene texto. Se asemeja a las líneas de código.

**Función**
Estas dos interfaces también difieren en su funcionamiento. Una GUI es una interfaz que solo te permite realizar una solicitud a la vex. Sin embargo, una CLI te permite realizar múltiples solicitudes al mismo tiempo.

### Ventajas de una CLI en ciberseguridad
La elección entre utilizar una GUI o una CLI se basa en parte en las preferencia personales, pero los analista de seguridad deberían poder usar ambas interfaces. El uso de una CLI puede ofrecer ciertas ventajas.

**Eficiencia**
Algunas personas prefieren la CLI porque se puede utilizar más rápidamente, cuando se sabe cómo administrarla. Para un usuario nuevo, una gui puede ser más eficiente, ya que es más fácil de navegar para principiantes.

Dado que una CLI puede aceptar múltiples solicitudes al mismo tiempo, es más potente cuando necesitas realizar múltiples tareas de manera eficiente. Por ejemplo, si tuvieras que crear varios archivos nuevos en tu sistema, podrías realizar rápidamente esta tarea en una CLI. Si estuvieras utilizando una  GUI, esto podría llevar mucho más tiempo, ya que tendrías que repetir los mismo pasos para cada archivo nuevo.

### Archivo de historial
Para los analista, el uso de la CLI de Linux es útil porque registra un archivo de historial de todos los comandos y acciones. Si estuvieras utilizando una GUI, tus acciones no se guardarían necesariamente en un archivo de historial.

Por ejemplo, podrías encontrarte en una situación en la que estás respondiendo a un incidente utilizando u manual de estrategias. Sus instrucciones requieren que ejecutes una serie de comandos diferentes. Si utilizas una CLI, podrías consultar el historial y asegurarte de que todos los comandos se utilizaron correctamente. Esto podría ser útil si hubiera habido problemas con el manual y tuvieras que revisar los pasos que realizaste en la línea de comandos.

Además, si sospechas que un atacante ha comprometido tu sistema, podrías rastrear sus acciones utilizando el archivo de historial.

## Arquitectura de Linux
El **usuario** es quien interatúa con la computadora. En linux, tú eres el primer elemento de la arquitectura del SO. Tú inicias las tareas o comandos que el SO ejecutará. Linux es un sistema multiusuario. Es decir que más de un usuario puede usar los recursos a la vez.
El segundo elemento de la arquitectura son las **apps** dentro de un sistema. Una app es un programa de tareas, como un procesador de textos o una calculadora. Quizá notes que app y programa se usan indistintamente. Por ejemplo, una app de Linux popular que veremos después es Nano. Nano es un editor de texto. En esta sencilla app tomas notas en la pantalla. Las apps de Linux suelen distribuirse mediante gestores de paquetes. El siguiente componente es el **shell**. Es importante porque permite comunicarte con el sistema. Este interpreta la línea de comandos. Procesa comandos y produce los resultados. Te puede sonar familiar. Antes vimos los dos tipos de interfaz de usuario: la GUI y el CLI. El shell es como una CLI. Otro elemento es el estándar de jerarquía del sistema de archivos (FHS). Es el componente del SO de Linux que organiza los datos. El **FHS** es como un archivador de datos. EL FHS es la forma de almacenar datos en un sistema. Organiza los datos para encontrarlps cuando el sistema accede a ellos. Después está el **kernel**. Es un componente de Linux que gestiona procesos y memoria.

El kerner se comunica con el hardware y ejecuta comandos enviados por el shell. Usa conductores para posibilitar que las apps ejecuten tareas. Con el kernel de linux, el sistema asigna recursos de forma más eficiente y funciona más rápidamente. El último componente de la arquitectura es el **hardware**. Se refiere a los componentes físicos de la computadora. Puedes comparar esto con apps descargables en un sistema. El hardware se refiere a la CPU, mouse, teclado, etc.