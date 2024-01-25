# Introducción a SQL y las bases de datos

Podemos definir una base de datos como una recopilación organizada de datos. Suele compararse las bases de datos con las hojas de cálculo. Quizás conozcas google sheets u otro programa de hojas de cálculo común. Si bien estos programas proveen manera convenientes de almacenar datos, las hojas de cálculo suele estar diseñadas para un usuario único o un equipo pequeño, y almacenar altas cantidades de datos.

Las bases de datos pueden realizar tareas complejas al acceder a daros. Como analista, a menudo deberás acceder a bases de datos con datos útiles. Por ejemplo, pueden ser bases con datos de intentos de inicio de sesión, software y actualizaciones, o equipos y propietarios. Las bases de datos nos permiten almacenar muchos datos a los que podemos acceder rápida y fácilmente. Hay muchas formas de estructurar una base datos. Aquí trabajaremos con bases de datos relacionales. Una base de datos relacional se estructura con tablas relacionadas entre sí. Las tablas contiene filas, también llamadas registros. Estas tiene datos específicos relacionados con las columnas. Por ejemplo, la primera fila es un registro de un empleado cuya identidicación es 1000 y que trabaja en Marketing. Las bases relacionales suele temer varias tablas. Este es un ejemplo en el que hay dos tablas de una bd más grande, una con empleados de la empresa, y otr con los equipos que se les dio. podemos conectar dos tabla. Aqui las relacionamos con la columna employee_id. Las columnas que relacionan dos tablas entre sí se llaman claves. Hay dos tipos de clave. La primera es la clave primaria. La clave primaria es una columna en la que cada fila tiene una entra única. No debe tener valores duplicados, valores nulos ni valores vacíos. Con las clave primaria, identificamos de forma única cada fila de la tabla. En la tabla employess, employee_id es una clave primaria. Cada valor de employee_id es único, y no hay valores duplicados ni vacíos. La segunda es la clave foránea, o externa. Es una columna es una tabla que es una clave primaria en otra tabla. Con la clave foránea, conectamos dos tablas. En el ejemplo, la columna employee_id también está en la tabla machines. Una tabla solo puede tener una clave primaria, pero varias foráneas.

## Consulta de base de datos con SQL

SQL significa lenguaje de consulta estructurado.
Se define a consulta (Query) como una solicitud de datos de una tabla o una combinación de tablas.
Recuperar registros de SQL (log) guarda eventos ocurridos en los sistema de una organización. 
SQL puede buscar entre millones de puntos de datos y extraer datos de filas relevantes mediante una consulta que se ejecuta en segundos.

## Filtrado de SQL versus filtrado de Linux

Filtrado de SQL versus filtrado de Linux

Anteriormente, estudiaste los comandos de Linux que te permiten filtrar por información específica, contenida en archivos o directorios. También, analizaste cómo SQL te ayuda a filtrar con eficacia para obtener la información que necesitas. En esta lectura, conocerás las diferencias entre las dos herramientas, en lo que respecta al filtrado. Además, aprenderás cómo acceder a SQL a través de la línea de comandos de Linux.
Acceso a SQL

Existen numerosas interfaces para acceder a SQL. Una de ellas es a través de la línea de comandos de Linux. 

Dado que existen muchas versiones de SQL, para acceder desde Linux, debes escribir un comando para la versión de SQL que quieres usar. Por ejemplo, si deseas acceder a SQLite, puedes ingresar el comando sqlite3 en la línea de comandos.

Luego de realizar esto, cualquier comando escrito en la línea de comandos se dirigirá a SQL en lugar de a los comandos de Linux.
Diferencias entre el filtrado de Linux y el de SQL 

Aunque tanto Linux como SQL te permiten filtrar datos, existen algunas diferencias que es necesario tener en cuenta, a la hora de elegir qué opción utilizar.

### Estructura

SQL ofrece mucha más estructura que Linux, que tiene un estilo más libre y menos ordenado.

Por ejemplo, si quieres acceder a un registro de intentos de inicio de sesión de los/las empleados/as, Linux imprimirá los datos como una línea de texto sin esta organización. En cambio, SQL te entregará cada registro separado en columnas, por lo cual te facilitará el análisis de una columna específica.

En términos de estructura, SQL proporciona resultados más fáciles de leer y pueden ajustarse más rápidamente que mediante Linux.

### Combinación de tablas

Algunas decisiones sobre seguridad requieren información de distintas tablas, una posibilidad que solo SQL ofrece. Mientras que con SQL, las/los analistas pueden combinar varias tablas cuando devuelve datos, Linux no tiene esa misma funcionalidad, ya que no permite que los datos se asocien con otra información que tengas en tu computadora. Para un/a analista que tiene que revisar registros de seguridad, esto resulta restrictivo.

### Mejores usos

Como analista de ciberseguridad, es importante que entiendas cuándo puedes usar cada herramienta. Si bien SQL posee una estructura más organizada y te permite combinar tablas, esto no significa que no haya situaciones que te exijan filtrar datos en Linux.

Una gran cantidad de datos utilizados en ciberseguridad se almacenarán en un formato de base de datos que funciona con SQL. Sin embargo, otros registros pueden estar en un formato que no es compatible con este lenguaje. Por ejemplo, si los datos se almacenan en un archivo de texto, no puedes buscarlos con SQL. En esos casos, es útil saber cómo filtrar en Linux. 

## Consultas Básicas
Vamos a determinar qué computadora se asignó a un empleado determinado. 

| Employees |
|:---------:|
| employee_id |
| device_id |
| username |
| department |
| Office |

Digamos que tenemos acceso a la tabla employees la tabla tiene 5 columnas. Escribiremos una consulta a la tabla que devuelve solo esas dos primeras columnas.

Las dos palabras claves que necesitamos para consultas básicas de SQL son SELECT y FROM.

SELECT indica qué columnas devolver.
FROM indica qué tabla consultar.

```SQL
SELECT employee_id, device_id
FROM employees;
```

**Sintáxis**: En SQL, las palabras clave no distinguen mayúsculas y minúsculas. 

```SQL
SELECT *
FROM employees;
```

* Selecciona todo.

## Cómo consultar una base de datos

Anteriormente, aprendiste la importancia de la herramienta SQL en el ámbito de la ciberseguridad y su relevancia para consultar bases de datos. Analizaste algunas consultas SQL básicas y palabras clave utilizadas para extraer la información que necesitas de una base de datos. En esta lectura, revisarás esas consultas y aprenderás una nueva palabra clave que te ayudará a organizar tus resultados. Además, aprenderás sobre la base de datos Chinook que usamos en este curso para consultas en lecturas y cuestionarios.
Consulta SQL básica

Existen dos palabras clave fundamentales en cualquier consulta SQL: SELECT y FROM. Las usarás cada vez que desees consultar una base de datos SQL. Si las usas en conjunto, ayudarás a SQL a identificar los datos que necesitas de una base de datos y la tabla de la que los extraes. 

El video demostró esta consulta SQL:

```
SELECT employee_id, device_id

FROM employees;
```

En lecturas y cuestionarios, este curso utiliza una base de datos de ejemplo denominada base de datos Chinook, para ejecutar las consultas. La base de datos Chinook incluye datos que se podrían crear en una empresa de medios digitales. Un/a analista de seguridad contratado/a por esta empresa puede necesitar consultar estos datos. Por ejemplo, la base de datos contiene once tablas, incluida una tabla employees (empleados/as), una tabla customers (clientes) y una tabla invoices (facturas). Estas tablas incluyen datos como nombres y direcciones.

A modo de ejemplo, puedes ejecutar esta consulta para obtener datos de la tabla customers (clientes) de la base de datos Chinook:  

```
1 SELECT customerid, city, country
2 FROM customers;
```
SELECT (seleccionar)

La palabra clave SELECT indica las columnas a devolver. Por ejemplo, puedes devolver la columna customerid (ID del cliente) de la base de datos Chinook con

SELECT customerid

También puedes seleccionar varias columnas separándolas con una coma. Por ejemplo, si quieres obtener las columnas customerid (ID del cliente) y city (ciudad), debes escribir SELECT customerid, city.

Si quieres obtener todas las columnas en una tabla, después de la palabra clave SELECT, puedes escribir un asterisco (*). La primera línea de la consulta será SELECT *.

Nota: Si bien las tablas que estás consultando en este curso son relativamente pequeñas, no te recomendamos usar SELECT * cuando trabajes con bases de datos y tablas grandes; en esos casos, el resultado final puede ser difícil de entender y lento de ejecutar. 

FROM (desde)

La palabra clave SELECT siempre viene con la palabra clave FROM. FROM indica qué tabla consultar. Para usar la palabra clave FROM, debes escribirla después de la palabra clave SELECT, generalmente en una línea nueva, y luego, escribir el nombre de la tabla que estás consultando. Si quieres obtener todas las columnas de la tabla customers (clientes), puedes escribir:

SELECT *

FROM customers;

Cuando quieras finalizar la consulta, escribe punto y coma (;) al final para indicar a SQL que la consulta está completa.

Nota: Los saltos de línea no son necesarios en consultas SQL, pero se suelen usar para facilitar la comprensión de la consulta. Si lo prefieres, también puedes escribir la consulta anterior en una línea como

SELECT * FROM customers;
ORDER BY (ordenar por)

Las tablas de bases de datos suelen ser muy complicadas, y por ello resultan útiles otras palabras clave de SQL. ORDER BY es una palabra clave importante para organizar los datos que extraes de una tabla.

ORDER BY ordena en secuencia los registros devueltos por una consulta con base en una o más columnas especificadas. Este orden puede ser ascendente o descendente.

Orden ascendente

Para usar la palabra clave ORDER BY, escríbela al final de la consulta y especifica una columna en la que se basará el orden. En este ejemplo, SQL devolverá las columnas customerid (ID del cliente), city (ciudad) y country (país) de la tabla customers (clientes), así como los registros se mostrarán secuencialmente en función de la columna city (ciudad):  

```
1 SELECT customerid, city, country
2 FROM customers
3 ORDER BY city;
```
La palabra clave ORDER BY ordena los registros en función de la columna especificada después de esta palabra clave. Por defecto, como se muestra en este ejemplo, la secuencia estará en orden ascendente. Esto significa que:

    si eliges una columna que contiene datos numéricos, esta organiza los resultados de menor a mayor. Por ejemplo, si organizas en función de customerid (ID del cliente), los números de identificación se ordenan de menor a mayor.

    si la columna contiene caracteres alfabéticos, como en el ejemplo con la columna city (ciudad), esta organiza los registros de la A a la Z. 

Orden descendente

También puedes usar ORDER BY con la palabra clave DESC para ordenar los datos en sentido descendente. La palabra clave DESC es la abreviatura de “descendente”, e indica a SQL que ordene los números de mayor a menor o, en el caso de caracteres alfabéticos, de la Z a la A. Para hacerlo, después de ORDER BY, escribe la palabra clave DESC. A modo de ejemplo, puedes ejecutar esta consulta para observar cómo se diferencian los resultados cuando aplicas DESC: 

```
1 SELECT customerid, city, country
2 FROM customers
3 ORDER BY city DESC;
```
Ahora, aparecen primero las ciudades que comienzan con las últimas letras del alfabeto. 

Ordenar en función de varias columnas

Adicionalmente, puedes elegir varias columnas en las que basar el orden. Por ejemplo, primero puedes elegir la columna country (país) y luego, la columna city (ciudad). A continuación, SQL ordena los resultados en función de la columna country (país) y, en el caso de que haya filas con el mismo valor de country (país), las organiza en función de la columna city (ciudad). Puedes practicar este ejemplo para averiguar cómo SQL muestra esto:  

```
1 SELECT customerid, city, country
2 FROM customers
3 ORDER BY country, city;
```
## Realizar una consulta SQL

### Tarea 1: Recupera datos de los dispositivos de los empleados.

1. Ejecuta la siguiente consulta para seleccionar toda la información de dispositivos de la tabla machines:
   
   ```
   SELECT *
   FROM machines;
   ```
2. Ejecuta la siguiente consulta para seleccionar solo las columnas device_id y email_client de la tabla machines. Reemplaza la X y la Y con estos nombres de columna:
   
   ```
   SELECT X, Y
   FROM machines;
   ```
3. Completa la consulta para mostrar solo las columnas device_id, operating_system y OS_patch_date de la tabla machines. Reemplaza la X y la Y y la Z con estos nombres de columna:

  ```
  SELECT X, Y, Z FROM machines;
  ```
### Tarea 2: Investiga la actividad de acceso.

1. Escribe una consulta en SQL para seleccionar las columnas event_id y country de la tabla log_in_attemps.

* Lo mismo de arriba

2. Escribe una consulta en SQL que seleccione las columnas username, logi_date y login_time de la tabla log_in_attempts:

* Lo mismo de arriba
  
3. Escribe la consulta en SQL que seleccione todas las columnas de la tabla log_in_attempts. Para ello, usa un solo símbolo después de la palabra clave SELECT.

 `SELECT * FROM log_int_attempts;`

### Tarea 3: Ordena los datos de intentos de acceso.

1. Ejecuta la siguiente consulta, que ordena los datos log_in_attempts por login_date:

```
SELECT * 
FROM log_in_attempts
ORDER BY login_date;
```
2. Modifica la consulta del paso anterior: agrega la hora de acceso a la cláusula ORDER BY. Debes reemplazar la X con el nombre de columna adecuado:

```
SELECT *
FROM log_in_attempts
ORDER BY login_date, login_time;
```
## Filtros básicos en consultas SQL
El filtrado consiste en seleccionar datos que coincidan con una condición. Un operado es un símbolo o palabra clave que representa una operación.

Por ejemplo: `country = 'USA'`

Para ver los registros que contienen USA en la columna country usamos `country = 'USA'`. Para filtrar en SQL simplemente agregamos una línea a la sentencia SELECT y FROM. Esta línea adicional usa una cláusula WHERE. En SQL, WHERE indica la condición de un filtro. Después de la palabra clave WHERE se inserta la condición específica mediante operadores.

`WHERE country = 'USA'`

En esta condición, indicamos que devuelva todos los registros que contengan un valor en la columna country igual a USA.

```
SELECT *
FROM log_int_attempts
WHERE country = 'USA';
```
Debido al filtro, solo se devuelven las filas cuyo país es USA.
En la tabla employees hay una columna office. Podemos buscar registros en esta columna que coincidan con un patrón. Para buscar un patrón, usamos el signo `%`, que es el comodin de caracteres no especificados. Si ejecutamos el filtro con `'East%'`, se devuelven los registros que empiezan con East. Al buscar patones con este signo, no podemos no podemos usar el operador igual a. En su lugar usamos el operador `LIKE`. LIKE es un operador usado con WHERE para buscar un patrón en una columna. Como LIKE similar al signo =, lo usamos en su lugar. 

`WHERE office LIKE 'East%'`

```
SELECT *
FROM log_in_attempts
WHERE country LIKE 'US%';
```
## La cláusula WHERE y los operadores básicos

Anteriormente, te centraste en cómo refinar tus consultas SQL con la cláusula WHERE para filtrar los resultados. En esta lectura, analizarás en mayor profundidad el uso de la cláusula WHERE, el operador LIKE y el comodín del signo de porcentaje (%). Además, te presentaremos el guion bajo (_), otro comodín que puede ayudarte a filtrar consultas.
Cómo ayuda el filtrado

Como analista de seguridad, a menudo deberás trabajar con registros muy voluminosos y complicados. Para encontrar la información que necesitas, con frecuencia deberás usar SQL para filtrar los registros.

En el contexto de la ciberseguridad, puedes usar filtros para identificar intentos de inicio de sesión de un usuario específico o todos los intentos de inicio de sesión realizados en el momento en que se produjo un incidente de seguridad. Como ejemplo adicional, puedes filtrar para encontrar dispositivos que están ejecutando una versión específica de una aplicación.
WHERE (dónde)

Para crear un filtro en SQL, debes usar la palabra clave WHERE. WHERE indica la condición para un filtro.

Si necesitaras enviar un correo electrónico a empleados/as con el cargo de ‘IT Staff' (personal de TI), podrías usar una consulta como la del ejemplo que se presenta a continuación. Puedes ejecutar este ejemplo para examinar cuáles son los resultados: 

```
SELECT firstname, lastname, title, email
FROM employees
WHERE title = 'IT Staff';
```
### En lugar de devolver todos los registros en la tabla employees (empleados/as), la cláusula WHERE indica a SQL que devuelva solo aquellos que contienen 'IT Staff' (empleados/as de TI) en la columna title (cargo). Esta usa el operador de signo igual (=) para establecer esta condición.

Nota: Debes colocar el punto y coma (;) donde termina la consulta. Cuando agregas un filtro a una consulta básica, el punto y coma se coloca después del filtro. 
Filtrado por patrones

También puedes filtrar en función de un patrón. Por ejemplo, puedes identificar las entradas que comienzan o terminan con uno o varios caracteres determinados. Filtrar en función de un patrón te exige incorporar dos elementos más en tu cláusula WHERE:

    un comodín 

    el operador LIKE

Comodines

Un comodín es un carácter especial que se puede sustituir por cualquier otro carácter. Dos de los comodines más útiles son el signo de porcentaje (%) y el guion bajo (_):

    El signo de porcentaje puede sustituir cualquiera de los demás caracteres. 

    El símbolo de guion bajo solo puede sustituir uno de los demás caracteres.

Puedes colocar estos comodines después de una cadena, antes de una cadena o en ambas ubicaciones, dependiendo del patrón según el cual estás filtrando.

La tabla siguiente incluye estos comodines aplicados a la cadena 'a' y ejemplos de los resultados que devolverá cada patrón.  

| Patrón | Resultados que puede devolver|
|:-------|:-----------------------------|
| 'a%' | apple123, art, a |
| 'a_'| as, an, a7 |
| 'a__' | ant, add, a1c |
| '%a' | pizza, Z6ra, a |
| '_a' | ma, 1a, Ha |
| '%a%' | Again, back, a |
| '_a_' | Car, ban, ea7 |

### LIKE (como)

Para aplicar comodines al filtro, debes usar el operador LIKE en lugar de un signo igual (=). LIKE se usa con WHERE para buscar un patrón en una columna. 

Por ejemplo, si quieres enviar un correo electrónico a empleados/as con el cargo 'IT Staff' (personal de TI) o 'IT Manager' (gerente de TI), puedes usar el operador LIKE combinado con el comodín %:   

```
SELECT lastname, firstname, title, email
FROM employees
WHERE title LIKE 'IT%';
```
Esta consulta devuelve todos los registros con valores en la columna title (cargo) que comienzan con el patrón de 'IT'. Esto significa que se devuelve tanto 'IT Staff' (personal de TI) como 'IT Manager' (gerente de TI).

Como ejemplo adicional, si quieres buscar en la tabla de facturas a todos/as los/las clientes ubicados en estados con la abreviatura 'NY', 'NV', 'NS' o 'NT', puedes usar el patrón 'N_' en la columna state (estado):  

```
SELECT firstname, lastname, state, country
FROM customers
WHERE state LIKE 'N_'
```
Esto devuelve todos los registros con abreviaturas de estado que siguen este patrón.

### Tarea 2: Obtén una lista de todas las máquinas con SO 2

* Selecciona todos los registros de la tabla `machines` con `operating?system` SO 2. Reemplaza la X con la cadena correcta:

```
SELECT device_id, operating_system
FROM machines 
WHERE operating_system = 'OS 2';
``` 
### Tarea 3: Obtén una lista de los empleados de departamentos específicos

1. Filtra las filas obtenidas a partir de la columna department en la tabla employees para incluir únicamente los empleados del departamento Finance. Reemplaza la X con el nombre de la columna apropiada y la Y con el valor adecuado para completar el filtro:

```
SELECT * 
FROM employees 
WHERE department = 'Finance';
```
2. Modifica la consulta anterior para obtener la información de los empleados del departamento de Ventas.

### Tarea 4: Identifica las máquinas de los empleados

1. Escribe una consulta para identificar qué empleado usa la oficina en South-109. (Los datos se deben obtener a partir de la columna office en la tabla employees).

```
SELECT *
FROM employees
WHERE office = 'South-109';
```

2. Modifica la consulta que usaste en el paso anterior para obtener todas las máquinas del edificio South. Usa el operador LIKE con % en esta consulta.

```
SELECT *
FROM employees
WHERE office LIKE 'South%';
```
### Tarea 5: Obtén una lista de empleados en un cierto rango de nombres de usuario

* Escribe una consulta con LIKE para obtener una lista de los empleados con IDs entre 1020 y 1029. (Los datos se deben obtener a partir de la columna employee_id en la tabla employees).

```
SELECT *
FROM employees
WHERE employee_id LIKE '102_';
```
## Filtrar fechas y números
Tres tipos de datos comunes que hay en las bases de datos:

* String
* Numeric
* Date and time

Los datos de cadena consisten en una secuencia organizada de caracteres. Estos caracteres pueden ser números, letras o símbolos. Por ejemplo, verás datos de cadena en nombres de usuario, como analyst10. Los datos numéricos se componen de números, como un recuento de inicios de sesión. A diferencia de las cadenas, en datos numéricos pueden usarse operaciones matemáticas como multiplicación o suma. Los datos de fecha y hora representan una fecha y hora. Antes aplicaos filtro con datos de cadena. Ahora trabajaremos con datos numéricos, y de fecha y hora. Como analista, a menudo tendrás que consultarlos. Por ejemplo, podemos filtrar fechas de parches para ver qué equipos hay que actualizar, o filtrar intento de inicio de sesión para ver únicamente los realizados en un período. Los operadores comunes para trabajar con datos numéricos o de fecha y hora son igual a, mayor que, menor que, no igual a, mayor que o igual a y menor que o igual a. Imagina que quieres los intentos de después de las 18hs. Como esta hora es posterior al horario laboral, quieres buscar patrones sospechosos. Puedes identificar intentos con el operador mayor que en el filtro. Escribi,os la consulta en SQL. Indicamos que queremos seleccionar, o SELECT, en todas las columnas de , o FROM, la tabla log_in_attempts. Luego agregamos el filtro WHERE.

```
Operadores
* =
* >
* <
* <>
* >=
* <=
```
```sql

SELECT *
FROM log_in_attempts
WHERE time > '18:00';
```
* BETWEEN
Podemos filtrar por números y fechas con el operador BETWEEN. Es un operador que filtra números o fechas dentro de un intervalo. Un ejemplo es buscar los parches instalados en un intervalo de tiempo.

```sql

SELECT *
FROM machines
WHERE OS_patch_date BETWEEN '2021-03-01' AND '2021-09-01';
```
>[!Important]
> Para filtrar cadenas, fechas y horas, es importante usar comillas para especificar lo que buscamos, pero para los números no se usan comillas.

## Operadores para filtrar fechas y números

Anteriormente, conociste operadores como menor que (<) o mayor que (>) y analizaste cómo usarlos para filtrar tipos de datos numéricos y de fecha y hora. Esta lectura resume lo que aprendiste y te ofrece ejemplos nuevos del uso de operadores en filtros.
Números, fechas y horas en ciberseguridad

Las/los analistas de seguridad trabajan con más que datos de cadena o datos que consisten en una secuencia ordenada de caracteres. 

También suelen trabajar con datos numéricos, o que consisten en números. Algunos ejemplos de datos numéricos que puedes encontrar en tu trabajo como analista de seguridad son:

    el número de intentos de inicio de sesión

    el recuento de un tipo específico de entrada de registro

    el volumen de datos que se envían desde una fuente

    el volumen de datos que se envían a un destino

También encontrarás datos de fecha y hora, o datos que representan una fecha y una hora. Como primer ejemplo, los registros por lo general colocan una marca de tiempo en cada ítem. Otros datos de fecha y hora pueden incluir:

    fechas de inicio de sesión

    horas de inicio de sesión

    fechas de implementaciones de parches 

    la duración de una conexión

Operadores de comparación

En SQL, el filtrado de datos numéricos y de fecha y hora suele involucrar operadores. Puedes usar los siguientes operadores en tus filtros, para asegurarte de obtener solo las filas que necesitas:

| Operador | Uso |
|:---------|:----|
| < | Menor que |
| > | Mayor que |
| = | Igual que |
| <= | Menor o igual que |
| >= | mayor o igual que |
| <> | no igual que |

Nota: También puedes usar != como operador alternativo para no igual que.

Incorporación de operadores en filtros

Estos operadores de comparación se usan en la cláusula WHERE al final de una consulta. La consulta siguiente usa el operador > para filtrar la columna birthdate (fecha de nacimiento). Puedes ejecutar esta consulta para analizar sus resultados:  

```sql

SELECT firstname, lastname, birthname
FROM employees
WHERE birthdate > '1970-01-01';
```
Esta consulta devuelve el nombre y los apellidos de empleados/as que nacieron después, pero no el '1970-01-01'(o 1º de enero de 1970). Si en lugar de ese operador usaras el operador >=, los resultados también incluirían resultados de la fecha '1970-01-01'.

En otras palabras, el operador > es exclusivo y el operador >= es inclusivo. Un operador exclusivo es el que no incluye el valor de comparación, en cambio un operador inclusivo es el que incluye el valor de comparación.

BETWEEN (entre)

Otro operador que también se usa para datos numéricos y de fecha y hora es el operador BETWEEN. BETWEEN filtra por números o fechas dentro de un rango. Por ejemplo, si quieres encontrar los nombres y apellidos de todos/as los/las empleados/as contratados/as entre el 1º de enero de 2002 y el 1º de enero de 2003, puedes usar el operador BETWEEN de la siguiente manera:  

```sql

SELECT firstname, lastname, hiredate
FROM employees
WHERE hiredate BETWEEN '2002-01-01' AND '2003-01-01';
```
Nota: El operador BETWEEN es inclusivo. Esto significa que los registros con una hiredate (fecha de contratación) del 1º de enero de 2002 o del 1º de enero de 2003 se incluyen en los resultados de la consulta anterior.

### Tarea 1: Recupera intentos de acceso realizados después de una fecha determinada

1. Completa la consulta en SQL para recuperar datos de intentos de acceso realizados después del 2022-05-09. Reemplaza la X con el operador adecuado:

```sql
SELECT *
FROM log_in_attempts
WHERE login_date X '2022-05-09';
```
2. Completa la consulta en SQL para recuperar datos de intentos de acceso realizados a partir del 2022-05-09. Reemplaza la X con el operador adecuado:

```sql

SELECT * 
FROM log_in_attempts 
WHERE login_date X '2022-05-09';
```
### Tarea 2: Recupera los accesos correspondientes a un período

1. Ejecuta la consulta para recuperar los registros que necesitas. Debes insertar las fechas que necesitas en lugar de la X y la Y:

```sql

SELECT * 
FROM log_in_attempts 
WHERE login_date BETWEEN 'X' AND 'Y';
```

### Tarea 3: Investiga los accesos realizados en determinados horarios

1. Escribe una consulta en SQL para recuperar datos de intentos de acceso realizados antes de las 07:00:00.

```sql

SELECT *
FROM log_in_attempts
WHERE login_time < '07:00';
```
2. Modifica la consulta para obtener resultados entre las 06:00:00 y las 07:00:00.

```sql

```

### Tarea 4: Investiga los accesos según el ID de los eventos

1. Escribe una consulta para obtener los intentos de acceso con un event_id mayor que o igual a 100.

```sql

SELECT event_id, username, login_date 
FROM log_in_attempts 
WHERE event_id >= 100;
```
2. Modifica la consulta para obtener resultados de intentos de acceso con un event_id entre 100 y 150.

```sql

SELECT event_id, username, login_date
FROM log_in_attempts 
WHERE event_id BETWEEN 100 AND 150;
```

## Filtros AND, OR y NOT
Para hacer una consulta con varias condiciones usamos el operador AND entre condiciones separadas. 
AND es un operador que especifica que ambas condiciones deben cumplirse a la vez. 

```sql

SELECT *
FROM machines
WHERE operating_system = 'OS 1' AND email_client = 'Email Client 1';
```
El operador OR indica que cualquiera de las dos condiciones debe cumplirse.

```sql

SELECT *
FROM machines
WHERE operatind_system = 'OS 1' OR operating_system = 'OS 3';
```
NOT, este operador niega una condición.

```sql

SELECT *
FROM machines
WHERE NOT operating_system = 'OS 3';
```

### Ejemplos

AND:

```sql
SELECT firstname, lastname, email, country, supportrepid
FROM customers
WHERE supportrepid = 5 AND country = 'USA';
```
OR:

```sql

SELECT firstname, lastname, email, country
FROM customers
WHERE country = 'Canada' OR country = 'USA';
```

NOT:

```sql

SELECT firstname, lastname, email, country
FROM customers
WHERE NOT country = 'USA';
```

Consejo profesional: Otra manera de encontrar valores que no son iguales que cierto valor es usar el operador <> o el operador !=. Por ejemplo, WHERE country <> 'USA' y WHERE country != 'USA' son filtros iguales que WHERE NOT country = 'USA'.

## Combinación de operadores lógicos

Los operadores lógicos se pueden combinar en filtros. Por ejemplo, si sabes que tanto EE.UU. como Canadá no se vieron afectados por un incidente de ciberseguridad, puedes combinar operadores para obtener clientes en todos los países excepto estos dos. En la consulta siguiente, NOT se coloca antes de la primera condición, se combina con una segunda condición con AND y luego también se coloca NOT antes de esa segunda condición. Puedes ejecutarla para revisar los resultados:  

```sql

SELECT firstname, lastname, email, country
FROM customers
WHERE NOT country = 'Canada' AND NOT country = 'USA';
```
## Combina tablas en SQL
Es útil cuando necesitamos información de dos tablas en una base de datos. Digamos que tenemos dos tablas, una sobre vulnerabilidades de distintos SO y otra sobre los equipos de la empresa, incluyendo susSO. AL combinarlas. obtenemos una lista de equipos vulnerables.
Como estamos con dos tablas, debemos indicarle a SQL de qué tabla recopilar las columnas. En la base de datos de ejemplos, tenemos la columna employee_id tanto en la tabla employees y como en la tabla machines. En sentencias SQL con dos columnas, SQL necesita saber a qué columna nos referimos. Para ello, escribimos el nombre de la tabla seguifo de un punto, y luego el nombre de la columna. Así tenemos employees, seguido de un punto y el nombre de la columna. Esta es la columna employee_id de la tabla employees. 

| employees |  | machines |
|:-   ------|  |:---------|
| employee_id | | devide_id |
| device_id |  | employee_id |
| username |  | operating_system |
| department |  | email_client |
| office |  | OS_patch_date |

Del mismo modo, esta es la columna eployee_id de la tabla machines. Tras entender esta sintaxis, apliquémosla a una combinación.

`employees.employee_id`

`machines.employee_id`

La clave primaria de la tabla employees es employee_id, que es una clave foránea en la tabla machines. Employee_id es una clave primaria en la tabla employees porque tiene un valor único en cada fila de la tabla employees y ningún valor vacío. 

### Combinación interna, o `INNER JOIN`
Una combinación interna devuelve filas que coinciden en una columna especificada que existe en más de una tabla. Las tablas suelen tener muchas más fulas, peor para explicar mejor la INNER JOIN solo veremos cuatro filas de la tabla employees y cuatro de la tabla machines. También veremos solo unas columnas de cada tabla en este ejemplo. Digamos que legimos employee_id en ambas tablas para hacer una combinación interna. Veamos las dos filas donde hay una coincidencia.

## Valores NULL
En SQL, NULL representa un valor faltante por cualquier motivo. En este caso, podrían ser equipos no asignados a ningún empleado.


```sql

SELECT username, office, operating_system
FROM employees
INNER JOIN machines ON employees.employee_ID = machines.employee_id;
```
Desglocemos, INNER JOIN indica a SQL que cree la combinación. Luego, nombramos la segunda tabla que quremos combinar con la primera. Esta se llama tabla derecha. Aquí queremos combinar la tabla machines con la tabla employees que ya se indentificó después de FROM. Por último, indicamos a SQL en qué columna basar la combinación. En nuestro casi, usamos la columna employee?id. Como usamos dos tablas, debemos identificar la tabla y seguirña con el nombre de la columna, por lo que tenemos employees.employee_id y machines.employee_id.

`Combinaciones = joins`

## Tipos de combinaciones (joins)
En los ejercicios anteriores, vimos cómo las combinaciones internas sirven al devolver únicamente registros con un mismo valor en columnas especificadas. Pero puede que necesitemos todas las entradas de una tabla o ambas. En este caso, necesitamos combinaciones externas. Hay tres tipos de combinaciones externas, LEFT JOIN, o izquierda, RIGHT JOIN, o derecha y FULL OUTER JOIN, o completa. Al igual que las combinaciones internas, las exteriores combinan dos tablas. Pero no necesitan una coincidencia entre columnas para deovolver una filas. Se devuelven filas según el tipo de unión. LEFT JOIN devuelve todos lo registros de la primera tabla, pero solo devuelve filas de la segunda que coinciden con una columna especificada. Como en el video anterior, veremos este tipo de combinación con solo cuatro filas de dos tablas con pocas columnas. La de employees es la tabla izquierda, o primera tabla, y la de machines es la derecha, o segunda. Realicemos la combinación con employee?id. en esta columna hay una coincidencia para dos de los cuatro registros. Al ejecutar la combinación, SQL devuelve estas filas con el valor coincidente, es resto de filas de la tabla izquierda y todas las columnas de ambas tablas. Los registros izquierdos que no coincidieron pero uferon devueltos con LEFT JOIN tienen valores NULLen columnas que vienen de la tabla machines. Ahora hablemos de combinaciones derechas. RIGHT JOIN devuelve todos los registro de la segunda tabla, pero solo filas de la primera tabla que coinciden con una columna especificada. Con un RIGHT JOIN en el ejemplo anterior, el resultado completo devuelve todas las filas de la segunda tabla y todas las columnas de ambas tablas. Los valores que no existen en ninguna tabla queda con NULL. Ahora hablemos de combinaciones externas completas. FULL OUTER JOIN devuelve todos los registros de ambas tablas. En el ejemplo, una FULL OUTER JOIN devuelve todas las columnas de todas las tablas. Si una fila no tiene valor en una columna, devuelve NULL. Por ejemplo, la tabla machines no tiene filas con employee_id 1190, por lo que los valores de esa fila y de las columnas de la tabla machine son NULL. Para implementar combinaciones izquierdas, derechas y completas en SQL, se usa la misma estructura sintática de INNER JOIN, pero estas palabras clave, LEFT JOIN, RIGHT JOIN y FULL OUTER JOIN. Como analista, no hace falta saber todo esto de memoria. Al saber la combinación que necesitas, puedes encontrar rápido información para ejecutar estas consultas.

```sql
FULL OUTER JOIN machines ON
employees.employee_id = machines.employee_id
```
## Compara tipos de combinaciones (Joins)

Anteriormente, estudiaste las combinaciones en SQL y cómo usarlas para combinar datos de varias tablas cuando estas tienen una columna en común. Además, aprendiste que existen distintos tipos de combinaciones y que cada una de ellas devuelve diferentes filas de las tablas que se combinan. En esta lectura, revisarás estos conceptos y analizarás en mayor profundidad la sintaxis necesaria para cada tipo de combinación.
Combinaciones internas

El primer tipo de combinación que puedes ejecutar es una combinación interna. INNER JOIN devuelve filas que coinciden en una columna especificada que existe en más de una tabla.  

Esta solo devuelve filas donde existe una coincidencia pero, como en otros tipos de combinaciones, devuelve todas las columnas especificadas de todas las tablas combinadas. Por ejemplo, si la consulta combina dos tablas con SELECT *, se devuelven todas las columnas en ambas tablas.

Nota: Si una columna existe en ambas tablas, esta se devuelve dos veces al usar SELECT *.

La sintaxis de una combinación interna

Para escribir una consulta usando INNER JOIN, puedes utilizar la siguiente sintaxis:

SELECT *

FROM employees

INNER JOIN machines ON employees.device_id = machines.device_id;

Debes especificar las dos tablas a combinar incluyendo la tabla primera o izquierda después de FROM y la tabla segunda o derecha después de INNER JOIN.

Después del nombre de la tabla derecha, usa la palabra clave ON y el operador = para indicar la columna en la que estás combinando las tablas. Es importante que especifiques los nombres tanto de la tabla como de la columna en esta parte de la combinación colocando un punto (.) entre la tabla y la columna.  

Además de seleccionar todas las columnas, puedes seleccionar solo ciertas columnas. Por ejemplo, si quieres que la combinación solo devuelva las columnas username (nombre de usuario), operating_system (sistema operativo) y device_id (ID de dispositivo), puedes escribir esta consulta:

SELECT username, operating_system, employees.device_id

FROM  employees

INNER JOIN machines ON employees.device_id = machines.device_id;

Nota: En la consulta de ejemplo, username (nombre de usuario) y operating_system (sistema operativo) solo aparecen en una de las dos tablas, por lo que se escriben solo con el nombre de la columna. Por otra parte, como device_id (ID de dispositivo) aparece en ambas tablas, es necesario indicar cuál devolver, especificando el nombre tanto de la tabla como de la columna (employees.device_id).
Combinaciones externas

Las combinaciones externas amplían lo que se devuelve a partir de una combinación. Cada tipo de combinación externa devuelve todas las filas de una o de ambas tablas.

Combinaciones izquierdas

Cuando combinas dos tablas, LEFT JOIN  devuelve todos los registros de la primera tabla, pero solo devuelve las filas de la segunda tabla que coinciden en una columna especificada.   

La sintaxis para usar LEFT JOIN se demuestra en la consulta siguiente:

SELECT *

FROM employees

LEFT JOIN machines ON employees.device_id = machines.device_id;

Como con todas las combinaciones, debes especificar la tabla primera o izquierda como la tabla que viene después de FROM y la tabla segunda o derecha como la tabla que viene después de LEFT JOIN. En la consulta de ejemplo, como employees (empleados/as) es la tabla izquierda, se devuelven todos sus registros. Solo se devuelven los registros que coinciden en la columna device_id (ID de dispositivo) desde la tabla derecha, machines (equipos). 

Combinaciones derechas

Cuando combinas dos tablas, RIGHT JOIN devuelve todos los registros de la segunda tabla, pero solo devuelve las filas de la primera tabla que coinciden en una columna especificada.  

La consulta siguiente demuestra la sintaxis para RIGHT JOIN:

SELECT *

FROM employees

RIGHT JOIN machines ON employees.device_id = machines.device_id;

RIGHT JOIN tiene la misma sintaxis que LEFT JOIN, con la única diferencia de que la palabra clave RIGHT JOIN ordena a SQL generar resultados distintos. La consulta devuelve todos los registros de machines (equipos), que es la tabla segunda o derecha. Solo se devuelven registros coincidentes de employees (empleados/as), que es la tabla primera o izquierda.

Nota:  Puedes usar LEFT JOIN y RIGHT JOIN y obtener exactamente los mismos resultados si usas las tablas en orden inverso. La consulta RIGHT JOIN siguiente devuelve exactamente el mismo resultado que la consulta LEFT JOIN demostrada en la sección anterior:

SELECT *

FROM machines

RIGHT JOIN employees ON employees.device_id = machines.device_id;

Para cambiar de lugar las tablas izquierda y derecha, solo tienes que modificar el orden de las tablas que aparecen antes y después de la palabra clave utilizada para la combinación.

Combinaciones externas completas 

FULL OUTER JOIN (Combinación externa completa) devuelve todos los registros de ambas tablas. Puedes utilizarla como una manera de fusionar totalmente dos tablas.  

Puedes revisar la sintaxis para usar FULL OUTER JOIN en la consulta siguiente:

SELECT *

FROM employees

FULL OUTER JOIN machines ON employees.device_id = machines.device_id;

Los resultados de una consulta FULL OUTER JOIN incluyen todos los registros de ambas tablas. De manera similar a INNER JOIN, el orden de las tablas no modifica los resultados de la consulta.

### Tarea 1: Une a los empleados con su máquina

Debes usar una unión interna de SQL para obtener los registros que necesitas en función de una columna relacionada. En este caso, ambas tablas incluyen la columna device_id. Esta es la que usarás para realizar la unión.

 1. Ejecuta la siguiente consulta para recuperar todos los registros de la tabla machines:

```sql

SELECT *
FROM machines;
```

2. Completa la consulta para realizar una unión interna entre las tablas machines y employees en la columna device_id. Reemplaza la X y la Y con este nombre de columna:

```sql
SELECT *
FROM machines
INNER JOIN employees ON machines.X = employees.Y;
```
### Tarea 2: Obtén más datos
Para ello, completarás una unión izquierda y una derecha en las tablas employees y machines. Los resultados incluirán todos los registros de una tabla o la otra. Debes vincular estas tablas usando la columna en común device_id.

2. Ejecuta la siguiente consulta en SQL para conectar las tablas machines y employees mediante una unión izquierda. Debes reemplazar la X con la palabra clave en la consulta:

```sql
FROM machines
X JOIN employees ON machines.device_id = employees.device_id;
```
2. Ejecuta la siguiente consulta en SQL para conectar las tablas machines y employees mediante una unión derecha. Debes reemplazar la X con la palabra clave en la consulta para resolver el problema:

```sql
SELECT *
FROM machines
X JOIN employees ON machines.device_id = employees.device_id;
```
### Tarea 3: Recupera datos de intentos de acceso
Para seguir investigando el incidente de seguridad, debes recuperar la información de todos los empleados que realizaron intentos de acceso. Para lograrlo, realizarás una unión interna en las tablas employees y log_in_attempts, y las vincularás con la columna en común username.

* Ejecuta la siguiente consulta en SQL para realizar una unión interna en las tablas employees y log_in_attempts. Reemplaza la X por el nombre de la tabla correcta: Luego, reemplaza la Y y la Z por el nombre de la columna que conecta las dos tablas:

```sql
SELECT *
FROM employees
INNER JOIN X ON Y = Z;
```
SELECT * 
FROM employees 
INNER JOIN log_in_attempts ON employees.username = log_in_attempts.username;

## Aprendizaje continuo en SQL

Has aprendido mucho acerca de SQL, incluso cómo aplicar filtros a consultas SQL y combinar varias tablas en una consulta. En esta lectura, explorarás un ejemplo de algo nuevo que puedes agregar a tu caja de herramientas de SQL: las funciones de agregado. Luego, te centrarás en cómo seguir aprendiendo sobre este y otros temas de SQL por tu cuenta.
Funciones de agregado

En SQL, las funciones de agregado son funciones que realizan un cálculo en varios puntos de datos y devuelven el resultado de este. No devuelven los datos en sí. 

Existen diversas funciones de agregado que realizan distintos cálculos:

    COUNT devuelve un solo número que representa la cantidad de filas devueltas por tu consulta.

    AVG devuelve un solo número que representa el promedio de los datos numéricos en una columna.

    SUM devuelve un solo número que representa la suma de los datos numéricos en una columna. 

Sintaxis de las funciones de agregado

Para usar una función de agregado, coloca la palabra clave para está después de la palabra clave SELECT y luego, entre paréntesis, indica la columna en la que deseas realizar el cálculo.

Por ejemplo, cuando trabajas con la tabla customers (clientes), puedes usar las funciones de agregado para resumir información importante acerca de la tabla. Si quieres averiguar cuántos/as clientes hay en total, puedes usar la función COUNT en cualquier columna y SQL devolverá el número total de registros, excepto los valores NULL (nulos). Puedes ejecutar esta consulta y analizar sus resultados:  

```sql
SELECT COUNT(firstname)
FROM customers;
```
El resultado es una tabla con una columna titulada COUNT(firstname) y una fila que indica el recuento.

Si quieres obtener el número de clientes de un país específico, puedes agregar un filtro a tu consulta:

```sql

SELECT COUNT(firstname)
FROM customers
WHERE country = 'USA';
```
Con este filtro, el recuento es menor porque solo incluye los registros en que la columna country (país) contiene un valor de 'USA'(EE.UU.).

En SQL, existen muchas otras funciones de agregado. La sintaxis de colocarlas después de SELECT es exactamente igual que en la función COUNT.
Sigue aprendiendo sobre SQL

SQL es un lenguaje de consulta ampliamente utilizado, con muchas más palabras clave y aplicaciones. Puedes seguir aprendiendo más sobre funciones de agregado y otros aspectos del uso de SQL por tu cuenta.

Lo más importante es que asumas las tareas nuevas con curiosidad y disposición a identificar nuevas maneras de aplicar SQL en tu trabajo como analista de seguridad. Identifica los resultados de datos que necesitas e intenta usar SQL para obtenerlos.

SQL es una de las herramientas más importantes para trabajar con bases de datos y analizar información, por lo que encontrarás numerosos recursos de apoyo al intentar aprender más sobre él en línea. En primer lugar, procura buscar los conceptos que ya aprendiste y practicaste, para identificar recursos que te ofrezcan explicaciones precisas y fáciles de seguir. Una vez que identifiques estos recursos, puedes usarlos para ampliar tus conocimientos.

También es importante que sigas adquiriendo experiencia práctica con SQL. Además, puedes buscar bases de datos nuevas para ejecutar consultas SQL usando lo que aprendiste.

