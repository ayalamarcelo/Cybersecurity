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

