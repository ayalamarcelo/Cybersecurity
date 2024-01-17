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