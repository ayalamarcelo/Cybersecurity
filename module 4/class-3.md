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


