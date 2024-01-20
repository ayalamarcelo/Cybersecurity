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