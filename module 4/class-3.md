# Busca archivos con comandos de Linux
En este caso, debes ubicar y analizar la información de ciertos archivos ubicados en el directorio /home/analyst.

Estos son los pasos que seguirás: En primer lugarm obtendrás la información del directorio de trabajo actual en el que te encuentras y mostrarás su contenido. En segundo lugar, nevegarás hasta el directorio `reports` y obtendrás una lista de los subdirectorios que contiene. En tercer lugar, navegarás hasta el subdirectorio `users` y mostrarás los contenidos del archivo `Q1_added_users.txt`. Por último, navegarás hasta el directorio `logs` y mostrarás las primeras 10 líneas de un archivo que contenga.

Tarea 1: Obtén información del directorio actual.

1. Muestra tu directorio de trabajo.  `pwd`

2. Muestra el nombre d elos archivos y directorios en el directorio de trabajo actual.`ls`

Tarea 2: Cambia el directorio y obtén una lista de los subdirectorios.

1. Nevaga hasta el directorio /home/analyst/reports.

`cd reports`

2. Muestra los archivos y subdirectorios en el directorio.

`ls`

Tarea 3: Ubica y lee el contenido de un archivo.

1. Navega hasta el directorio /home/analyst/reports/users.
   
`cd /home/analyst/reports/users`

Ruta de acceso relativa

`cd users`

2. Obtén una lista de los archivos del directorio actual.

`ls`

3. Muestra el contenido del archivo Q1?added_users.txt

`cat Q1_added_users.txt`

>[!Note]
> El comando `cat` muestra el contenido de un archhivo en la shell. Puedes especificar el archivo que quieres visualizar con una ruta de acceso abosluta o realtiva.

`cat /home/analyst/reports/users/Q1_added_users.txt`

Tarea 4: Navega hasta un directorio y ubica un archivo.

1. Navega hasta el directorio /home/analyst/logs.
   
`cd /home/analyst/logs`

2. Muestra el nombre del archivo que contiene.

`ls`

3. Muestra las 10 primeras líneas de este archivo.

`head server_logs.txt`

>[!Note]
> El comando `head` muestra únicamente el comienzo de un archivo, que consiste en diez líneas de forma predeterminada. Puedes especificar cuántas líneas deseas con el argumento `-n`, que específica la cantidad de líneas que se deben mostrar.

## Administra contenido de archivos en Bash
**Encuentra lo que necesitas con Linux**

Ahora que conocimos los comandos básicos pwd, ls y cd y podemos usarlos para navegar por el sistemas de archivos de Linux, veamos un par de formas de buscar lo que necesitas dentro de este sistema. Como analista de seguridad, probablemente debas filtrar la información que necesitas. Filtrar es buscar en el sistema información específica necesaria para resolver problemas complejos. Por ejemplo, imagina que tu equipo indica que un malware contiene una cadena de caracteres. Quizá debas encontrar otros arcchivos con las misma cadena para ver si contienen el mismo malware. Más adelante, profundizaremos en cómo usar SQL para filtrar una base de datos, pero Linux es bueno para iniciar el filtrado básico. Empecemos con grep. El comando grep busca un archivo especificado y devuelve todas las líneas dentro de ese archivo que contienen una cadena específicada. Veamos un ejemplo. Digamos que tenemos un archivo  llamado updates.txt y buscamos líneas con la palabra "OS". Si el archivo es grande, tomaría mucho tiempo realizar un análisis visual. En lugar de hacer eso, tras navegar al directorio que contiene updates.txt, ingresaremos el comando "grep OS updates.txt" en el shell. Observa cómo al comando grep le siguen dos argumentos. El primer argumento es la cadena que buscamos, en este caso, "OS". El segundo argumento es el nombre del archivo en el que estamos buscando: "updates.txt". Al presionar intro, Bash devuelve todas las líneas con la palabra "OS".

Ahora hablemos del pipe, o la pleca. EL pipe es un comando de Linux que puede usarse para varias cosas. En un momento, veremos cómo puede usarse para filtrar. Pero primero hablemos de la idea general del pipe. El comando pipe envía una salida estándar de un comando como entrada estándar en otro comando para procesarlo luego. Lo representa la barra vertical, o pleca. En nuestro contexto, podemos referirnos a él como carácter "pipe" en el sentido de "tubo".

Imagina una tubería física. Las tuberías tienen dos extremos. Por un lado, por ejemplo, entra agua de un tanque de agua caliente. Luego, pasa por la tubería y sale por el otro lado en un fregadero. En linux, el pipe también redirige. La salida de un comando por el tubo y luego se usa en el otro lado. Antes expliqué que grep sirve para filtrar cadenas de caracterres dentro de un archivo. Grep también puede usarse luego de una pleca. Centrémonos en este ejemplo. El primer comando, ls, indica al SO generar los contenidos de archivo y directorio de su subdirectorio reports. Pero como al comando le sigue la pleca, la salida no se devuelve en la pantall, sino que se envía al siguiente comando. Vimos que grep busca una cadena de caracteres. En este caso, "users". Pero ¿dónde busca? Como grep va después de una pleca, la salida del comando anterior indica dónde buscar. En este caos, la salida es una lista de archivos y directorios. Dentro del subdirectorio reports. Devolverá todos los archivos y directorios con la palabra "usuarios".
Exploremos esto en el bash. Para entender mejor cómo funciona le filtro, primero generemos todo en el directorio reports. Como queremos devolver solo los archivos con la palabras "users", combinaremos el comando ls con los comandos pipe y grep. Como muestra la salida, se indicó a Linux devolver solo los archivos con la palabras "users". Los dos archivos sin esta cadena ya no aparecen.

Ahora conoces dos formas de filtrar en linux al trabajar como analista. Navegar por archivos y fitrar es solo parte del conocimiento necesario.

## Filtrar contexnido en Linux
En esta lectura, continuarás explorando los comandos de Linux, que pueden ayudarte a filtrar la información que necesitas. Conocerás un nuevo comando de Linux, `find`, es útil si deseas buscar archivos y directorios para obtener información específica.

**Filtrado para obtener información**

Antes, exploraste cómo el filtrado para obtener información es una habilidad importante para los analista de seguridad. El filtrado es la selección de daros que cumplen una determinada condición. Por ejemplo, si tuvieras un virus en el sistema que solo afectara a los archivos `.txt`, podrías usar el filtrado para encontrar estos archivos rápidamente. EL filtrado te permite buscar en función de criterios específicos, como la extensión de archivo o una cadena de texto.

## grep
El comando `grep`busca un archivo especificado y devuelve todas las líneas del archivo que contienen una cadena especificada. El comando `grep` suele combinars con dos argumentos: una cadena específica a buscar y un archivo específico en el que buscar.

Por ejemplo, si ingresas `grep OS updates.txt`, obtendras todas las líneas que contienen OS en el archivo `updates,txt`. En este ejemplo, OS es la cadena específica a buscar y `updates.txt` es el archivo específico en el que buscar.

## Pipe(pleca)
Para acceder a este comando, se utiliza el carácter pleca, o pipe (|). El comando pipe envía la salida estándar de un comando como entrada estándar a otro comando, para su posterior procesamiento. Como recordatorio, la salida estándar es la información devuelta por el sistema operativo a través del shell, mientras que la entrada estándar es la información recibida por el sistema operativo (SO) a través de la línea de comandos.

El caracter pleaca puede estar en distintas partes de un teclado, pero en general, se encuentra en la misma tecla que el caracter de barra invertida. En algunos teclados, el crácter | puede verse diferente, con un pequeño espacio en el medio de la línea. si no encuentras el carácter, busca donde está ubicado en tu teclado.

Cuando se utiliza con grep, la pleca puede ayudarte a encontrar dorectorios y archivos que contiene una palabra específica en el nombre. Por ejemplo, `ls /home/analyst/reports | grep users`. Antes de la pleca, ls indica que debe hacerse una lista de los nombres de los archivos y directorios en reports. Luego, está salida se envía, como entrada, al comando ubicado después de la pleca. En este caso, grep users devolverá todos los nombres de archivos o directorios que contienen users de la entrada recibida.

>[!Note]
> El comando pipe es una forma general de redireccionamiento en Linux y puede utilizarse para múltiples tareas, además del filtrado. Puedes considerarlo como una herramienta general a utilizar, siempre que quieras que la salida de un comando se convierta en la entrada de otro comando.

## Find
El comando `find` sirve para buscar directorios y archivos que cumplan con criterios especificados. Hay una amplia variedad de criterios que se pueden especificar con `find`. Por ejemplo, puedes buscar archivos y directorios que: 

   * Contengan una cadena específica en el nombre;
   * Tengan un determinado tamaño de archivo; o
   * Se hayan modificado por última vez dentro de un período de tiempo determinado.
  
Cuando usas `find`, el primer argumento después de find indica dónde comenzar a buscar. Por ejemplo, al ingresar `find /home/analyst/projects` se busca todo lo que comienza en el directorio `projects`.

Después de este primer argumento, debes indicar tus criterios para la búsqueda. Si no incluyes un criterio de búsqueda específico con tu segundo argumetno, es probable que tu búsqueda devuelva una gran cantidad de directorios y archivos.

La especificación de criterios implica opciones. Las opciones modifican el comportamiento de un comando y, por lo general, comienzan con un guión (-).

## -name e -iname
Un criterio clave que los analistas podrían usar con `find` es buscar nombres de archivos o directorios que contengan una cadena específica. Debes ingresar la cadena específica que estés buscando entre comillas despupes de las opciones `-name` o `-iname`. La diferencia entre estas dos opciones es que `-name` distingue entre mayúsculas y minúsculas, mientras que `-iname` no lo hace.

Supongamos que quieres buscar todos los archivos en el directorio `projects` que contienen la palabra "log" en el nombre. Para hacerlo, ingresarías `find /home/analyst/projects -name "*log*"`. También podrías ingresar `find /home/analyst/projects -iname "*log*"`.

En estos ejemplos, la salida estaría conformada por todos los archivos del directorio projects que contengan log rodeada de cero más caracteres. La parte del comando que dice `"*log*"` es el criterio de búsqueda que indica que se debe buscar la cadena "log". Cuando la opción es `-name`, no se devolverán los archivos con nombres que incluyan `Log o LOG`, por ejemplo, porque esta opción disrtingue entre mayúsculas y minúsculas. Sin embargo, sí se devolverán si la opción es `-iname`.

>[!Note]
> El asterisco (*) se usa como comodín para representar cero o más caracteres desconocidos.

## -mtime
Los analistas de seguridad también puede usar find para buscar archivos o directorios modificados por última vez, en un período de tiempo determinado. Para esta búsqueda, se puede utilizar la opción `-mtime`. Por ejemplo, al ingresar `find /home.analyst/projects -mtime - 3`, se devuelven todos los archivos y directorios del directorio projects que han sido modificado en los últimos tres días.

La búsqueda de la opción `-mtime` se basa en días, por lo que la entrada `-mtime +1` indica todos los archivos o directorios que se modificaron por última vez hace más de un día y la entrada `-mtime -1` indica todos los archivos o directorios que se modificaron por última vez hace menos de un día.

>[!Note]
> Si quieres basar la búsqueda en minutos en lugar de días, puedes usar la opción `-mmin`.

## Tarea 1: Busca mensajes de error en un archivo de registro

En esta tarea, debes navegar hasta el directorio `/home/analyst/logs` e informar sobre los mensajes de error en el archivo `server_logs.txt`. Usarás `grep` para hacer una búsqueda en el archivo y recuperar solo las entradas correspondientes a errores.

1. Nevagea hasta el directorio `/home/analyst/logs`.

`cd logs`

2. Usa `grep` para filtrar el archivo `server_logs.txt` y obtener todas las líneas que contienen la cadena de texto `error`.

>[!note]
> Si ingresas un comando de forma incorrecta y no regresa a la ventana de la linea de comandos, puede presionar `CTRL+C` para deterner el proceso y forzar la shell a regresar a la ventana de la línea de comandos.

`grep error server_logs.txt`

## Tarea 2: Encuentra archivos que contengan cadenas específicas

En esta tarea, debes navegar hasta el directorio `/home/analyst/reports/users`, y usar los comandos y arguemntos de Linux para buscar archivos de datos del usuario que contengan una cadena específica en su nombre.

1. Navega hasta el directorio `/home/analyst/reports/users`.

`cd /home/analyst/reports/users`

2. Usa el caracter de barra vertical (|), canaliza el resultado del comando `ls` al comando `grep` para enumarar únicamente los archivos que contenga la cadena `Q1` en su nombre.

`ls | grep Q1`

3. Enumera los archivos que contiene la palabra `access` en su nombre.
   
`ls | grep access`

## Tarea 3: Busca más contenido en archivos

En esta tarea, debes buscar información incluida en archivos de los usuarios que se hayan agregado al sistema o que se hayan borrado.

1. Muestra los archivos en el directorio `/home/analyst/reports/users`.
   
`ls`

2. Busca el nombre de usuario `jhill` en el archivo `Q2_deleted_users.txt`.

`grep jhill Q2_deleted_users.txt`

3. Realiza una búsqueda en el archivo `Q4_added_users.txt` para enumerar todos los usuarios que se agregaron al departamento de `human resources`.

`grep "Human Resources" Q4_added_users.txt`

## Crea y modifica directorios y archivos

Al trabajar con datos en seguridad, la organización es clave. Si sabemos dónde está la información, es más fácil detectar problemas y proteger la información. Más atrás, hablamos de navegar entre directorios, pero examinemos los directorios en detalle. Quizás conozcas el conceptos de carpetas para organizar información. En Linux, tenemos directorios. Los directorios ayudan a organizar archivos y subdirectoros. Por ejemplo, en un directorio de informes, una analista quizá deba crear dos subdirectorios: uno de borradores y otro de informes finales. Ahora que sabemos por qué necesitamos directorios, veamos algunos comandos esenciales de Linux para gestionar directorios y archivos. Primero, observemos los comandos para crear y eliminar directorios. El comando `mkdir` crea un nuevo directorio. Por el contrario, `rmdir` quita o elimina directorios. El comando mkdir crea un nuevo directorio. Por el contrario, rmdir quita o elimina un directorio. Algo útil de este comando es su advertencia incorporada que te avisa si un directorio no está vacío. Así evitas eliminar archivos accidentalmente. Luego usarás otros comandos para crear y eliminar archivos. El comando `touch` crea un nuevo archivo, y el comando `rm` quita o elimina un archivo.

Por último, están los comandos para copiar y mover archivos o directorios. El comando `mv` mueve un archivo o directorio a una nueva ubicación, y `cp` copia un archivo o directorio en una nueva ubicación. Ya podemos probar estos comandos. Primero, usemos el comando `pwd`, luego mostremos los nombres de archivos y directorios en el directorio analyst con el comando ls.
Imagina que ya no necesitamos el directorio oldreports que está en el contenido del archivo. Veamos cómo eliminarlo. Ingresamos el comando `rmdir` seguido del nombre del directorio a quitar, "old reports". Podemos usar ls para confirmar que oldreports se eliminó y ya no aparece en el contenido. Ahora hagamos otro cambio. Queremos un nuevo directorio de borradores de informes. Debemos usar el comando `mkdir` e indicar un nombre para el directorio: `drafts`. Si ingresamos ls, observamos el nuevo directorio drafts en el contenido del directorio analyst.

Pasemos al nuevo directorio ingresando `cd drafts`.

Si ejecutamos ls, no devuelve niguna salida. Esto indica que el directorio está vacío. Pero luego le agregamos algunos archivos. Digamos que queremos elaborar nuevos informes de parches de correo y SO recién instalados. Para crear estos archivos, ingresamos `touch email_patches.txt` y luego, `touch OS_patches.txt`.

Al ejecutar ls, se indica que los archivos están ahora en el directorio drafts. ¿Y si solo necesitamos un nuevo informe sobre parches del SO y queremos eliminar el de parches de correo? Para hacerlo, ingresamos `rm` y específicamos los archivos que queremos eliminar como `email_patches.txt`. Al ejecutar ls, confirmamos que se eliminó. Veamos los comandos para mover y copiar. Observamos que hay un archivo "email policy" en la carpeta reports que actualmente está en formatos de borrador. Queremos moverlo a la carpeta drafts recién creada. Para hacerlo, debemos pasar al directorio pasar al directorio que actualmente tiene ese archivo.

Al ejecutar ls ahí, vemos que contiene varios archivos, incluido `email_policy.txt`. Para mover ese archivo, ingresamos el comando `mv` seguido de dos argumentos.

El primero después de mv indentidica el archivo que se va a mover. El segundo indica adónde moverlo.

Si pasamos después de mv identifica el archivo que se va a mover. El segundo indica adónde moverlo.

Si pasamos al directorio drafts y mostramos su contenido, veremos que el archivo email_policy se movió a este directorio.

Volvamos al directorio reports. Al mostrar su contenido de archivos, confirmamos que email_policy ya no está.

Una cosa más. Necesitamos mantener vulnerabilidades.txt en el directorio reports. Pero como afecta un próximo proyecto, también queremos copiarlo en el directorio projects.

Dado que ya estamos en el directorio que contiene este archivo, usaremos el comando cp para copiarlo en el directorio projects. El primer argumento indica que archivo copiar, y el segundo provee la ruta al directorio en que se copiará.

Al presionar intro, se copia el archivo vulnerabilities en el directorio projects, y también deja el oroginal en reports. Veamos un concepto más para modificar archivos. Además de usar comandos, puedes usar aplicaciones para editar archivos. Como analista, los editores de archivos se usan para tus tareas diarias, como redactar informes. Uno de los editores de archivo más populares es nano. Es bueno para principiantes. Puedes acceder a esta herramientas con el comando nano. Familiaricémonos con nano. Agregaremos un título a nuestro nuevo informe OS_patches.txt.

Primero, pasamos al directorio que contiene ese archivo. Luego, ingresamos `nano` seguido del nombre del archivo que queremos editar "OS_patches.txt".

Aparece el editor de archivos nano con el archivo abierto. Por ahora, solo ingresamos el titulo OS patches en el editor. Tenemos que guardar esto antes de volver a la línea de comandos, y para hacerl, presionamos Ctrl + O y luego Intro para guardarlo con el nombre de archivo actual. Para salir, presionamos Ctrl + X.

## Administra directorios y archivos

Antes, exploraste cómo administrar el sistema de archivos utilizando comandos de Linux. Conociste los siguientes comandos: mkdir, rmdir, touch, rm, mv y cp. En esta lectura, revisarás estos comandos, así como el editor de texto nano, y aprenderás otra forma de escribir en archivos.
Cómo crear y modificar directorios

* mkdir

El comando mkdir crea un directorio nuevo. Al igual que todos los comandos que presentamos en esta lectura, puedes ingresar el directorio nuevo como la ruta de archivo absoluta, que comienza desde la raíz, o como una ruta de archivo relativa, que comienza desde el directorio actual.

Por ejemplo, si quieres crear un directorio nuevo llamado network en tu directorio /home/analyst/logs, puedes ingresar mkdir /home/analyst/logs/network para crear este directorio nuevo. Si ya estás en el directorio /home/analyst/logs, también puedes crear este directorio nuevo al ingresar mkdir network.

Consejo profesional: Puedes usar el comando ls para confirmar que se agregó el directorio nuevo.

* rmdir

El comando rmdir elimina o borra un directorio. Por ejemplo, al ingresar rmdir /home/analyst/logs/network, se eliminaría este directorio vacío del sistema de archivos.

Nota: El comando rmdir no puede eliminar directorios que contienen archivos o subdirectorios. Por ejemplo, si ingresas rmdir /home/analyst, obtendrás un mensaje de error. 
Cómo crear y modificar archivos

* touch y rm

El comando touch crea un archivo nuevo. Este archivo no tendrá ningún contenido dentro. Si tu directorio actual es /home/analyst/reports, al ingresar touch permissions.txt, se creará un archivo nuevo en el subdirectorio reports, llamado permissions.txt.

El comando rm elimina o borra un archivo. Este comando debe usarse con cuidado, ya que no es fácil recuperar archivos eliminados con rm. Para eliminar el archivo de permisos que acabas de crear, ingresa rm permissions.txt. 

Consejo profesional: Para verificar que permissions.txt se haya creado o eliminado correctamente, puedes ingresar ls.

* mv y cp

Si estás trabajando con archivos, también puedes usar mv y cp. El comando mv mueve un archivo o directorio a una ubicación nueva, y el comando cp copia un archivo o directorio a una ubicación nueva. El primer argumento después de mv o cp es el archivo o directorio que quieres mover o copiar, mientras que el segundo es la ubicación en la que quieres moverlo o copiarlo.

Para mover permissions.txt al subdirectorio logs, ingresa mv permissions.txt /home/analyst/logs. Al mover un archivo, se elimina de su ubicación original. Sin embargo, al copiarlo, esto no sucede. Para copiar permissions.txt en el subdirectorio logs y mantenerlo en su ubicación original, ingresa cp permissions.txt /home/analyst/logs.

>[!Note]
> El comando mv también puede usarse para cambiar el nombre de un archivo. Para hacerlo, ingresa el nombre nuevo como el segundo argumento en lugar de la ubicación nueva. Por ejemplo, al ingresar mv permissions.txt perm.txt, se cambia el nombre del archivo permissions.txt a perm.txt.

* Editor de texto nano

Nano es un editor de archivos de línea de comandos disponible por defecto en muchas distribuciones de Linux. Muchos/as principiantes lo encuentran fácil de usar, y es muy utilizado en ciberseguridad. Puedes realizar varias tareas básicas en nano, como crear archivos nuevos y modificar contenido de archivos. 

Para abrir un archivo existente en nano desde el directorio que lo contiene, ingresa nano seguido del nombre del archivo. Por ejemplo, al escribir nano permissions.txt desde el directorio /home/analyst/reports, se abre una nueva ventana de edición de nano con el archivo permissions.txt abierto para editar. También puedes proporcionar la ruta de acceso absoluta al archivo si no estás en el directorio que lo contiene.

Para crear un archivo nuevo en nano, ingresa nano seguido de un nombre de archivo nuevo. Por ejemplo, al ingresar nano authorized_users.txt desde el directorio /home/analyst/reports, se crea el archivo authorized_users.txt dentro de ese directorio y se abre en una nueva ventana de edición de nano.

Dado que no hay una función de guardado automático en nano, es importante que guardes tu trabajo antes de salir. Para guardar un archivo en nano, usa el atajo de teclado Ctrl + O. Se te pedirá que confirmes el nombre del archivo antes de guardarlo. Para salir de nano, utiliza el atajo de teclado Ctrl + X.

Nota: Otros editores de texto de línea de comandos populares son Vim y Emacs.
Redireccionamiento de salida estándar

Hay otra forma de escribir en archivos. Anteriormente, aprendiste sobre la entrada estándar y la salida estándar. La entrada estándar es información recibida por el sistema operativo a través de la línea de comandos, mientras que la salida estándar es la información devuelta por el SO a través del shell.

También aprendiste acerca del comando pipe, o pleca. El comando pipe envía la salida estándar de un comando como entrada estándar a otro comando, para su posterior procesamiento. Para usarlo, se ingresa el carácter pleca (|). 

Además de la pleca (|), también puedes usar los operadores del signo “mayor que” (>) y el “doble mayor que” (>>) para redirigir la salida estándar.

Al usarlos con echo, los operadores > y > > pueden servir para enviar la salida de echo a un archivo específico en lugar de a la pantalla. La diferencia entre ambos es que > sobrescribe tu archivo existente, mientras que >> agrega tu contenido al final del archivo existente en lugar de sobrescribirlo. El operador > debe usarse con cuidado, ya que no es fácil recuperar archivos sobrescritos.

Cuando estés dentro del directorio que contiene el archivo permissions.txt, ingresa echo "last updated date" >> permissions.txt y agrega la cadena “last updated date” al contenido del archivo. Al ingresar echo "time" > permissions.txt después de este comando, se sobrescribe todo el contenido del archivo permissions.txt con la cadena “time”.

>[!Note]
> Los operadores > y >> crearán un archivo nuevo si todavía no existe uno con el nombre especificado.

* Conclusiones clave

Saber cómo administrar el sistema de archivos en Linux es una habilidad importante para las/los analistas de seguridad. Estos son algunos comandos útiles para ello: mkdir, rmdir, touch, rm, mv y cp. Cuando un/a analista de seguridad necesita escribir en archivos, puede usar el editor de texto nano o los operadores > y >>.

## Autentica y autoriza usuarios
Un permiso es el tipo de acceso que se da a un archivo o directorio. Los permisos se relacionan con la autorización. La autorización es el concepto de dar acceso a ciertos archivos o directorios. Una buena práctica es dar acceso a los datos solo si es necesario. Hay tres tipos de permisos en Linux que un suaurio autorizado puede tener. El primer tipo es el de lectura. En un archivo, los permisos de lectura permiten leer el contenido del archivo.

En un directorio, este permiso permite leer todos los archivos que este contiene. Luego están los permisos de escritura. Los permisos de escritura en un archivo permiten modificar su contenido.

En un directorio, los permisos de escritura permiten crear nuevos archivos en él. Finalmente están los permisos de ejecución. Los permisos de ejecución en un archivo permiten ejecutarlo si este es ejecutable. Los permisos de ejecución en un directorio permiten entrar en un directorio y acceder a sus archivos. Se dan permisos a tres tipos de propietarios. EL primero es el suaurio. El usuario es el propietario del archivo. Al crear un archivo, eres el propietario del archivo, pero la propiedad puede cambiarse. El siguiente tipo es el grupo. Cada usuario es parte de un grupo. Un grupo consiste en varios usuarios, y esta es una forma de gestionar un entorno multiusuario.

Finalmente, está otros usuarios. Otros usuarios se refiere al resto de usuarios en el sistema. Cualquiera que tenga acceso al siste a pertenece a este grupo. En linux, los permisos de archivo están representados por una cadena de 10 caracteres. Para un directorio con permiso para todo el grupo de usuarios, la cadena sería "drwxrwxrwx". El primer carácter indica el tipo de archivo. Como muestra el ejemplo, d indica un directorio. Pero si este carácter tuviera un guion, se trataría de un archivo normal. El segundo, tercer y cuarto carácter indican los permisos de usuario. En este ejemplo, r indica que el usuario tiene permisos de lectura, w que el usuario tiene permisos de escritura y x que el usuario tiene permisos de ejecución.

Si faltara uno de estos permisos, habría un guion en lugar de la letra. Asimismo, el quinto, sexto y séptimo carácter indican permisos para el siguiente tipo de propietario: grupo. Como puedes ver, el grupo también también tiene permisos de lectura, escritura y ejecución. No hay guiones que indiquen que no se dio alguno de estos permisos.

Los caracteres del octavo al décimo indican permisos para el último tipo de propietario: otros usuarios. En el ejemplo, también tiene permisos de lectura, escritura y ejecución. Garantizar que los archivos y directorios tengan los permisos de acceso correctos es crucial para proteger archivos sensibles y mantener la seguridad de un sistema. Por ejemplo, el departamento de nóminas manjea información sensible. Si alguien fuera de ese grupo pudiera leer este archivo, ocurriría un problema de privacidad. Otro ejemplo es cuando el usuario, grupo y otros usuarios pueden escribir en un archivo. Este tipo de archivo se llama world-writeable, o con permisos de escritura para todos, estos archivos pueden representar un gran riesgo de seguridad.

### Cómo se verificar los permisos
Primero debemos saber qué son las opciones. Las opciones modifican el comportamietno del comando. Las opciones de un comando pueden ser una letra o una palabra. Para verificar los permisos, hay que agregar opciones al comando ls. Primero ls-l muestra permisos para archivos y directorios. Quizás también quieres mostrar archivos ocultos y ver sus permisos. Los archivos ocultos, que tienen un punto antes del nombre, no aparecen al usar ls para mostrar el contenido del archivo. Al ingresar ls-a, se muestran los archivos ocultos.

Estas dos opcinoes pueden combinarse para hacer ambas cosas.

Al ingresar ls-la, se muestran los permisos de archivos y directorios, incluidos los archivos ocultos.

Usemos el comando ls para mostrar su contenido. La salda muestra los archivos del directorio, pero no vemos los permisos. AL usar ls-l en su lugar, vemos información adicional de estos archivos.
Centrémonos en un archivo específico: project1.txt.
Los caracteres segundo a cuarto de los permisos nos muestran que el usuario tiene permisos de lectura y escritura, pero no de ejecución. En los caracteres del quinto al séptimo y del octavo al décimo, la secuencia es r--. Esto indica que el grupo y otros usuarios solo tienen privilegios de lectura. Después de los permisos, ls -l muestra primero el nombre de usuario. Aquí estamos nosotros, analyst. Luego viene el nombre del grupo, en nuestro caso, el grupo security. Ahora usemos ls-a. La salida incluye dos archivos más, archivos ocultos llamados .hidden1.txt y .hidden2.txt.
Por último, podemos usar ls -la para ver los permisos de todos los archivos, incluidos estos archivos ocultos. 

## Cambiar de permisos
Aprenderemos sobre `chmod`, cambia los permisos en archivos y directorios. Este comando significa cambiar modo. Hay dos modos para cambiar permisos, pero veremos el simbólico.
Con `chmod`, debes indentificar el archivo o directorio cuyos permisos cambiarás. Este es el argumento final, en este caso, el archivo access.txt. El primer argumento, agregado después del comando chmod, indica cómo cambiar los permisos. Antes, vimos los tres tipos de propietarios, usuario, grupo y otros usuarios. Para identificarlos con chmod, usamos u para representar al usuario, g para el grupo y o para otros usuarios.

`chmod g+w, o-r access.txt`

En este ejemplo, g indica que cambiaremos los permisos de grupo y o, los permisos de otro. En este argumento, estos tipos de propietario se separan por una coma. Pero queremos agregar o quitar permisos. Para saberlo, usamos operadores matemáticos. El signo + después de g indica que queremos agregar permisos de grupo. El signo + después de g indica que queremos agregar permisos de grupo. El signo - después de o indica que queremos quitarlos de otros usuarios.
Qué cambios queremos hacer: Sabemos que r representa permisos de lectura, w representa permisos de escritura y x representa permisos de ejecución. En este caso, w indica que agregaremos permisos de escritura y x representa permisos de ejecución. En este caso, w indica que agregaremos permisos de escritura al grupo y r que quitamos permisos de lectura a otros usuarios.
Si usamos el comando `ls-l`, veremos los permisos del archivo. Mjuestra los permisos del único archivo en este directorio: access.txt. Antes vimos cómo leer estos permisos. Los caracteres del segundo al cuarto indican que el usuario tenía permisos de lectura y escritura. Los caracteres quintoa séptimo indican que el grupo solo tiene permisos de lectura. Los caracteres octavo a décimo muestran que el tipo otros usuarios solo tiene permisos de lectura. Debemos ajustar los permisos. Queremos que los analistas del grupo security tengan permiso de escritura, pero deseamos quitar los permisos de lectura para otros usuarios. Agregamos entonces permisos de escritura para grupo y quitamos los de otros usuarios. Ejecutamos ls-l de nuevo. Esto muestra un cambio en los permisos de access.txt. El segmento central de permisos de grupo w se agregó para dar permisos de escritura. Otro cambio es que la r se eliminó en el último segmento, lo que indica que se quitaron los permisos de lectura para otros usuarios.

##
