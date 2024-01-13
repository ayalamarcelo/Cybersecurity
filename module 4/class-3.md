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
Si usamos el comando `ls-l`, veremos los permisos del archivo. Muestra los permisos del único archivo en este directorio: access.txt. Antes vimos cómo leer estos permisos. Los caracteres del segundo al cuarto indican que el usuario tenía permisos de lectura y escritura. Los caracteres quintoa séptimo indican que el grupo solo tiene permisos de lectura. Los caracteres octavo a décimo muestran que el tipo otros usuarios solo tiene permisos de lectura. Debemos ajustar los permisos. Queremos que los analistas del grupo security tengan permiso de escritura, pero deseamos quitar los permisos de lectura para otros usuarios. Agregamos entonces permisos de escritura para grupo y quitamos los de otros usuarios. Ejecutamos ls-l de nuevo. Esto muestra un cambio en los permisos de access.txt. El segmento central de permisos de grupo w se agregó para dar permisos de escritura. Otro cambio es que la r se eliminó en el último segmento, lo que indica que se quitaron los permisos de lectura para otros usuarios.

## Permisos de lectura

En Linux, los permisos se representan con una cadena de 10 caracteres. Estos son algunos permisos:

   * read (lectura): para archivos, es la capacidad de leer el contenido de los archivos; para directorios, es la capacidad de leer todo el contenido del directorio, incluidos los archivos y subdirectorios

   * write (escritura): para archivos, es la capacidad de realizar modificaciones en el contenido de los archivos; para directorios, es la capacidad de crear archivos nuevos en el directorio

   * execute (ejecución): para archivos, es la capacidad de ejecutar el archivo si se trata de un programa; para directorios, es la capacidad de ingresar al directorio y acceder a sus archivos.
   
Estos permisos se otorgan a los siguientes tipos de propietarios:

   * user (usuario): propietario del archivo

   * group (grupo): un grupo más grande del que el propietario forma parte

   * other (otros usuarios): todos los demás usuarios del sistema.

## Exploración de los permisos existentes

Puedes usar el comando ls para investigar quién tiene permisos en archivos y directorios. Antes, aprendiste que ls muestra los nombres de los archivos y directorios en el directorio de trabajo actual.

Existen otras opciones que puedes agregar al comando ls para que sea más específico. Algunas de estas opciones proporcionan detalles sobre los permisos. Estas son algunas que utilizan el comando ls y resultan importantes para las/los analistas de seguridad:

    ls -a: muestra archivos ocultos. Los archivos ocultos comienzan con un punto (.) al principio.

    ls -l: muestra permisos para archivos y directorios. También muestra otra información adicional, incluido el nombre del propietario, el grupo, el tamaño del archivo y la hora en que fueron modificados por última vez.

    ls -la: muestra los permisos de archivo y directorios, incluidos los archivos ocultos. Se trata de una combinación de las otras dos opciones.

Cambio de permisos

El principio de mínimo privilegio es el concepto de otorgar solo el acceso y la autorización mínimos necesarios para ejecutar una tarea o función. En otras palabras, los/las usuarios/as no deben tener privilegios que estén más allá de lo necesario. No seguir el principio del mínimo privilegio puede crear riesgos de seguridad.

El comando chmod puede ayudarte a administrar esta autorización. El comando chmod cambia los permisos en archivos y directorios. 

## Cómo usar chmod

El comando chmod requiere dos argumentos. El primer argumento indica cómo cambiar los permisos, y el segundo indica el archivo o directorio para el que quieres cambiar los permisos. Por ejemplo, el siguiente comando agregaría todos los permisos a login_sessions.txt:

chmod u+rwx,g+rwx,o+rwx login_sessions.txt

Si quisieras quitar todos los permisos, podrías usar

chmod u-rwx,g-rwx,o-rwx login_sessions.txt

Otra forma de asignar estos permisos es usar el signo igual (=) en este primer argumento. Al usar = con chmod, se establecen o asignan los permisos exactamente según se especificó. Por ejemplo, el siguiente comando establecería permisos de lectura para login_sessions.txt para usuario, grupo y otros usuarios:

chmod u=r,g=r,o=r login_sessions.txt

Este comando sobreescribe permisos existentes. Por ejemplo, si antes el usuario tenía permisos de escritura, estos permisos de escritura se eliminan después de especificar permisos de solo lectura con =.

## El principio de mínimo privilegio en acción

Como analista de seguridad, es posible que te encuentres en una situación como esta: hay un archivo llamado bonuses.txt dentro de un directorio de remuneración. El propietario de este archivo es un miembro del departamento de Recursos Humanos cuyo nombre de usuario es hrrep1. Se decidió que hrrep1 necesita acceso a este archivo. Pero, dado que este archivo contiene información confidencial, nadie más en el grupo hr debería acceder a él.

Ejecutas ls -l para verificar los permisos de los archivos en el directorio de remuneración y descubres que los permisos para bonuses.txt son -rw-rw----. El tipo propietario del grupo tiene permisos de lectura y escritura que no se alinean con el principio de mínimo privilegio. 

Para remediar la situación, ingresas chmod g-rw bonuses.txt. Ahora, solo puede acceder a este archivo el/la usuario/a que lo necesita para llevar a cabo sus responsabilidades laborales.

## Situación

En este caso, debes examinar y administrar los permisos de los archivos del directorio /home/researcher2/projects para el usuario researcher2.

El usuario researcher2 es parte del grupo research_team.

Debes verificar los permisos para todos los archivos del directorio, incluidos los archivos ocultos, para asegurarte de que coincidan con el grado de autorización que debería otorgarse. De no ser así, debes cambiar los permisos.

Estos son los pasos que seguirás: Primero, verificarás los permisos del usuario y el grupo para todos los archivos del directorio projects. A continuación, verificarás si algún archivo tiene permisos incorrectos y los modificarás según sea necesario. Por último, verificarás los permisos del directorio /home/researcher2/drafts y los modificarás para quitar los accesos no autorizados.

## Agrega y elimina usuarios
Esto se relaciona con el concepto de autenticación. La autenticación es el proceso en el que el usuario demuestra quien dice ser en el sistema. Así como en un edificio físico, no todos los usuarios pueden entrar, no todos los usuarios deben poder acceder al sistema. Pero hay que garantizar que quienes deban acceder puedan hacerlo. Es por eso que necesitamos agregar usuarios. Los nuevos usuarios pueden serlo para la organización o para el grupo. Esto podría deberse a un cambio en la estructura de la organización o a un orden de la gerencia de mover a alguein. Asimismo, cuando los usuarios se van de la empresa, deben eliminarse. Ya no deben tener acceso a ninguna parte del sistema. Si solo cambian de grupo, deben eliminarse de los grupos a los que ya no pertenecen. Vimos por qué es importante agregar y eliminar usuarios. Ahora hablemos de otro tipo de usuario: el usuario root, o raíz. Un usuario root o raíz, o superusuario, tiene privilegiois elevados para modificar el sistema. Los usuarios normales tienen limitaciones, el usuario root, no. Quienes deben realizar ciertas tareas pueden agregarse temporalmente como usuarios root. Los usuarios root puede crear, modificar o eliminar cualquier archivo y ejecutar cualquier programa. Solo los usuarios root o cuentas con privilegios de raíz pueden agregar usuarios nuevos. Quizás te preguntes cómo alguien se convierte en superusuario. Una forma es iniciar sesión como usuario root, ero ejecutar comandos como usuario root puede ser problemático. EL primer problema de iniciar sesión como usuario root es el riesgo de seguridad. Los atacante intentarán vulnerar la cuenta raíz. Como es la cuenta más poderosa, para protegerse, debe tener el inciio de sesión desactivado. Otro problema es que es muy fácilcometer errores irreversibles. Es muy fácil escribir el comando incorrecto en la CLI, y si estás como usuario root, corres más riesgo de cometer errores irreversibles, como eliminar un directorio de forma permanente. Finalmente, está el probelma de la rendición de cuentas. En un entorno multiusuario como Linux, hay muchos usuarios. Si alguien inició sesión como root, no hay forma de rastrear quién ejecutó un comando determinado.

Una solución para resolver este problema es `sudo`. El comando sudo concede permisos elevados de forma temporal a usuarios específicos. ESte es un enfoque más controlado que el de usuario root, que ejecuta comandos con privilegios de root. Sudo resuleve muchos problemas asociados con el usuario root. Sudo viene del inglés "super user do", y permite ejecutar mucho problemas como usuario elevado sin iniciar ni cerrar sesión de otra cuenta. Al ejecutar sudo se te pedirá la contraseña del usuario de la sesión actual. No todos los usuarios de un sistema pueden convertirse en superusuarios. Los usuarios deben recibir acceso sudo con un archivo de confirguración llamado archivos sudoers. Luego de haber aprendido sobre sudo, veamos cómo usarlo con otro comando para agregar usuarios. Este comando es `useradd`, useradd agrega in usuario al sistema. Solo los usuarios root o con privilegios sudo pueden usar un comando useradd. 

Agregar un usuario desde sistema con `useradd`:

```Bash
$ sudo useradd salesrep7

```

Eliminar un usuario desde sistema con `userdel`:

```Bash
$ sudo userdel salesrep7
```

## Uso responsable de sudo

Anteriormente, exploraste la autorización, la autenticación y los comandos de Linux con sudo, useradd y userdel. El comando sudo es importante para las/los analistas de seguridad porque permite a los/las usuarios/as tener permisos elevados sin arriesgar el sistema ejecutando comandos como usuario root. En esta lectura, continuarás explorando la autorización, la autenticación y los comandos de Linux y aprenderás dos comandos más que se pueden usar con sudo: usermod y chown. 
Uso responsable de sudo

Para administrar la autorización y la autenticación, tienes que ser un usuario root o un usuario con privilegios elevados para modificar el sistema. El usuario root (raíz) también puede llamarse “superusuario”. Para convertirte en usuario root, debes iniciar sesión como tal. Sin embargo, no se recomienda ejecutar comandos como usuario root en Linux, ya que pueden surgir riesgos de seguridad si un agente de amenaza compromete esa cuenta. También es fácil cometer errores irreversibles, y el sistema no puede rastrear quién ejecutó un comando. Por estas razones, en lugar de iniciar sesión como usuario root, se recomienda usar sudo en Linux cuando necesites privilegios elevados.

El comando sudo otorga temporalmente permisos elevados a usuarios específicos. El nombre de este comando proviene de “super user do” (“superusuario” y “hacer”). Para que puedan usar sudo, se les debe otorgar acceso a los usuarios a través de un archivo de configuración, que se llama “sudoers file”. Si bien es preferible usar sudo a iniciar sesión como usuario root, es importante tener en cuenta que los usuarios con permisos elevados para usar sudo podrían estar en mayor riesgo en caso de un ataque.

Esta situación puede compararse con la de un hotel que tiene una llave maestra. La llave maestra se puede usar para acceder a cualquier habitación del hotel. Algunos/as trabajadores necesitan esta llave para realizar su trabajo. Por ejemplo, para limpiar todas las habitaciones, la persona a cargo debería escanear la tarjeta de identificación y, luego, usar esta llave maestra. Sin embargo, si una persona ajena a la red del hotel obtuviera acceso a la tarjeta de identificación y la llave maestra de la persona a cargo de la limpieza, podría acceder a cualquier habitación del hotel. En este ejemplo, la persona a cargo de la limpieza con la llave maestra representa a un/a usuario/a que usa sudo para obtener privilegios elevados. Debido a los peligros que sudo supone, solo quienes estrictamente necesitan usarlo deben tener estos permisos.

Además, incluso si necesitas acceso a sudo, debes tener cuidado y usarlo solo con los comandos que necesitas. La ejecución de comandos con sudo permite a los/las usuarios/as eludir los controles de seguridad típicos que existen para evitar que un/a atacante obtenga acceso elevado.

Nota: Ten cuidado de no usar sudo si estás copiando comandos de una fuente en línea. Es importante que no uses sudo por accidente. 
Autenticación y autorización con sudo

Puedes usar sudo para muchas tareas de gestión de autenticación y autorización. Como recordatorio, la autenticación es el proceso de verificar quién es una persona, mientras que la autorización es el concepto de otorgar acceso a recursos específicos en un sistema. Estos son algunos de los comandos clave que se utilizan para estas tareas:

### useradd

El comando useradd agrega un usuario al sistema. Para agregar un usuario con el nombre de usuario fgarcia con sudo, ingresa sudo useradd fgarcia. Existen otras opciones que puedes usar con useradd:

    -g: Establece el grupo predeterminado del usuario, también conocido como su grupo principal.

    -G: Agrega al usuario a grupos adicionales, también llamados grupos complementarios o secundarios.

Para usar la opción -g, debe especificarse el grupo principal después de -g. Por ejemplo, al ingresar sudo useradd -g security fgarcia, se agrega a fgarcia como un nuevo usuario y se le asigna security como grupo principal.

Para usar la opción -G, debe incluirse el grupo complementario en el comando después de -G. Con la opción -G, puedes agregar más de un grupo complementario a la vez. Al ingresar sudo useradd -G finance,admin fgarcia, se agrega a fgarcia como usuario nuevo y se lo añade a los grupos existentes finance y admin.

### usermod

El comando usermod modifica las cuentas de usuario existentes. Las mismas opciones -g y -G del comando useradd pueden utilizarse con usermod si el usuario ya existe. 

Para cambiar el grupo principal de un usuario existente, debes usar la opción -g. Por ejemplo, al ingresar sudo usermod -g executive fgarcia, se cambiaría el grupo principal de fgarcia a executive.

Para agregar un grupo complementario para un usuario existente, debes usar la opción -G. También necesitas una opción -a, que agrega al usuario a un grupo existente y solo se usa con la opción -G. Por ejemplo, al ingresar sudo usermod -a -G marketing fgarcia, se agregaría el usuario existente fgarcia al grupo complementario marketing.

Nota: Al cambiar el grupo complementario de un usuario existente, si no incluyes la opción -a, -G reemplazará a cualquier grupo complementario existente con aquellos  que se especifiquen después de usermod. El uso de -a con -G asegura que se agreguen los nuevos grupos, pero no se reemplaza a los grupos existentes.

Hay otras opciones que puedes usar con usermod para especificar cómo quieres modificar el usuario, entre ellas, las siguientes:

    -d: Cambia el directorio de inicio del usuario.

    -l: Cambia el nombre de inicio de sesión del usuario.

    -L: Bloquea la cuenta para que el usuario no pueda iniciar sesión.

La opción siempre va después del comando usermod. Por ejemplo, para cambiar el directorio de inicio de fgarcia a /home/garcia_f, ingresa sudo usermod -d /home/garcia_f fgarcia. La opción -d va justo después del comando usermod y antes de los otros dos argumentos necesarios.

### userdel

El comando userdel elimina a un usuario del sistema. Por ejemplo, al ingresar sudo userdel fgarcia, se elimina a fgarcia como usuario. Ten cuidado antes de eliminar a un usuario con este comando.

El comando userdel no elimina los archivos en el directorio de inicio del usuario, a menos que se use la opción -r. Al ingresar sudo userdel -r fgarcia, se eliminaría a fgarcia como usuario y se eliminarían todos los archivos en su directorio de inicio. Antes de eliminar cualquier archivo de usuario, debes asegurarte de tener copias de seguridad en caso de que las necesites más adelante.

Nota: En lugar de eliminar al usuario, podrías considerar desactivar su cuenta con usermod -L. Esto le impide al usuario iniciar sesión y te otorga acceso a su cuenta y sus permisos asociados. Por ejemplo, si un usuario abandona una organización, esta opción te permitiría identificar los archivos sobre los que tiene propiedad, por lo que podrías transferir esta propiedad a otros usuarios.

### chown

El comando chown cambia la propiedad de un archivo o un directorio. Puedes usar chown para cambiar la propiedad del usuario o del grupo. Para cambiar el usuario propietario del archivo access.txt a fgarcia, ingresa sudo chown fgarcia access.txt. Para cambiar el grupo propietario del archivo access.txt a security, ingresa sudo chown :security access.txt. Tienes que ingresar dos puntos (:) antes de security para designarlo como un nombre de grupo.

Al igual que con useradd, usermod y userdel, existen otras opciones que puedes usar con chown.

## Ejericio

En esta situación, un nuevo empleado con el nombre de usuario researcher9 se une a una organización. Debes agregarlo al sistema y seguir administrando su acceso durante su permanencia en la organización.

Estos son los pasos que seguirás: En primer lugar, agregarás un nuevo empleado al sistema y, luego, al grupo primario correspondiente. En segundo lugar, harás que este empleado sea propietario de un archivo relacionado con un proyecto en particular. En tercer lugar, agregarás al nuevo empleado a un grupo complementario. Por último, borrarás al empleado del sistema.
Nota: Cuando comiences este lab, verás que ya accediste como usuario analyst y que el directorio actual de trabajo es tu directorio principal, /home/analyst.

Es hora de practicar cómo administrar el acceso de los usuarios en Linux.

### Tarea 1: Agrega un usuario nuevo

1. Escribe un comando para agregar al sistema a un usuario llamado reseracher9.

A continuación, debes agregar al usuario nuevo al grupo `research_team`.

2. Usa el comando usermod y la opción -g para agregar a researcher9 al grupo research_team y establecerlo como su grupo primario.

### Respuesta
`sudo useradd researcher9`
`sudo usermod research_team researcher9`

### Tarea 2: Asigna la propiedad del archivo

El nuevo empleado, researcher9, se ocupará del archivo project_r. En esta tarea, debes indicar que es el propietario del archivo project_r.txt.

El archivo project_r.txt se encuentra en el directorio /home/researcher2/projects y su propietario es el usuario researcher2.

    Usa el comando chown para establecer a researcher9 como el propietario de /home/researcher2/projects/project_r.txt.

Haz clic en Revisar mi progreso para verificar que completaste esta tarea correctamente.

#### Respuesta
`sudo chown researcher9 /home/researcher2/projects/project_r.txt`

### Tarea 3: Agrega al usuario a un grupo secundario

Después de un par de meses, este empleado tiene otro rol en la organización, y ahora trabaja tanto en el departamento de Investigación como en el de Ventas.

En esta tarea, debes agregar a researcher9 a un grupo secundario (sales_team). Su grupo primario aún es research_team.

    Usa el comando usermod con las opciones -a y -G para agregar a researcher9 al grupo sales_team y establecerlo como su grupo secundario.

#### Solución

`sudo usermod -a -G sales_team researcher9`

### Tarea 4: Borra un usuario.

1. Ejecuta un comando para borrar a researcher9 del sistema:

`sudo userdel researcher9`

2. Ejecuta el siguiente comando para borrar el grupo researcher9, que ya no es necesario:
   
`sudo groupdel researcher9`

## Páginas man dentro del shell
En Linux puedes obtener ayuda en líneas de comandos. Por ejemplo, `man` muestra información sobre otros comandos y cómo funcionan. El nombre de este comando viene de la palabra manual.

`$ man usermod` devuelve información con una descripción general.

Cuando queremos saber rápido qué hace un comando, usamos `whatis`. Muestra una descripción de un comando en una sola línea.

`$ whatis tail`

`Apropos` busca una determinada cadena en las descripciones del manual.

`$ apropos password`
`$ apropos -a change password`

### Tarea 1: Obtener más información sobre los comandos

1. `whatis cat`

2. Usa el comando `man` para obtener más detalles sobre `cat`.

3. `press Q para salir de la línea de comandos`.

4. Usa apropos para encontrar un comando que muestre la primera parte de un archivo.

`apropos -a first part file`

### Tarea 2: Explora el comando useradd

1. Usa el comando de Linux más adeacuado para obtener ayuda con el comando useradd y explora todas su opciones.

`man useradd`

### Tarea 3: Explora los comandos rm y rmdir

1. Usa el comando linux más adeacuado para recordar qué hace cada comando.

`whatis rm y rmdir`

### Tarea 4: Determina qué comando usar

En esta tarea, imagina que necesitas crear un grupo nuevo pero que no puedes recordar qué comando usar. Debes identificar un comando adecuado mediante la búsqueda con palabras clave. En este caso, usa las palabras clave create new group.

    Usa el comando de Linux más adecuado con estas palabras clave para identificar qué comando usar.

`apropos -a create new group`

### Tarea 1: Profundiza tus conocimientos sobre los comandos

1. Ejecuta el comando `whatis` para obtener una descripción breve de cat.
2. Usa el comando `man` para obtener más detalles sobre cat.
4. Usa `apropos` para encontrar un comando que presente como resultado la primera parte de un archivo:
`apropos -a first part file`

### Tarea 2: Explora el comando useradd

1. Usa el comando de linux más adeacuado para obtener ayuda con el comando useradd.

`man useradd`

### Tarea 3: Comando rm y rmdir

`whatis rm`
`wathis rmdir`